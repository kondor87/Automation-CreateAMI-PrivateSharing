# Automation-CreateAMI-PrivateSharing
A lambda function that permit to schedule a creation of AMI and Sharing with other accounts

This Function is usefull when we want automate the generation of AMI and automatically sharing with other account.

In this part of code you need to change the account ID:

        `image.modify_attribute(
                Attribute='launchPermission',
                LaunchPermission={
                    'Add': [
                        {
             #            'Group': 'all',
                         'UserId': '151539401663' <---
                        }
                     ]
                },
                OperationType='add',
                UserIds=['151539401663'] <---
            )`          

