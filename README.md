# Rubric


## Create and Customize Amazon Q Application

![First](./initial-application-schedule-in-training.png)


## Upload Static PDF and Connect Amazon S3

![Second](s3-synced.png)
![Second](./daily-sync-s3-update-1.png)
![Second](./daily-sync-s3-update-2.png)
![Second](s3-contents-1.png)
![Second](s3-contents-2.png)
![Second](s3-contents-3.png)

### Missing Screenshots, second submission
![Second](s3-manual-upload-1.png)
![Second](s3-manual-upload-2.png)

## Secure the Application

The acl contents 
```json
[
    {
        "keyPrefix": "s3://career-bucket-project/Data/Medicine/",
        "aclEntries": [
            {
                "Name": "career.coach.one",
                "Type": "GROUP",
                "Access": "ALLOW"
            }
        ]
    },
        {
        "keyPrefix": "s3://career-bucket-project/Data/",
        "aclEntries": [
            {
                "Name": "career.coach.two",
                "Type": "GROUP",
                "Access": "DENY"
            }
        ]
    }
]

```
![Third](./acl-s3.png)
This run is by coach.one

![Third](./coach-one.png)

Coach.two is blocked from the resources, so the fallback works and q app uses the general knowledge. This confirms that the acl policy works. 


![Third](./acl-coachtwo.png)
![Third](./acl-coachtwo-2.png)

The blocked words.

![Third](./blocked-words.png)

## Publish and Share the Application

From this single screenshot, you can see that the app is shared as it is in the apps directory, I have added some custom tags and tag the app. Also verified the app. 

![Fourth](custom-tags-verified.png)


