* Everything in region: eu-central-1

# Create Service

* Create Stack: website-beta-ide
* Create User "website-beta-ide-uploader" with Programmatic Access and Inline Policy "policy"
```
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "VisualEditor0",
            "Effect": "Allow",
            "Action": [
                "s3:PutObject",
                "s3:GetObject",
                "s3:ListBucket",
                "s3:DeleteObject",
                "s3:PutObjectAcl"
            ],
            "Resource": [
                "arn:aws:s3:::cube-codes-website-beta-ide-storage/*",
                "arn:aws:s3:::cube-codes-website-beta-ide-storage"
            ]
        }
    ]
}
```

* Create CNAME entry in DNS from DomainName to CloudFront Hostname