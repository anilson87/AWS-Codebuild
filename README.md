# AWS-Codebuild
1- Create lambda function \
2- Create buildspec.yml and lambda_function.py \
3- Create AWS Codebuild project, connect it to Github repository by creating Github token and entering token while creating the project \
4- Select webhook if you want to trigger build when you push something to repository \
5- Modify codebuild policy \
{ \
            "Effect": "Allow", \
            "Action": [ \
                "lambda:AddPermission", \
                "lambda:RemovePermission", \
                "lambda:CreateAlias", \
                "lambda:UpdateAlias", \
                "lambda:DeleteAlias", \
                "lambda:UpdateFunctionCode", \
                "lambda:UpdateFunctionConfiguration", \
                "lambda:PutFunctionConcurrency", \
                "lambda:DeleteFunctionConcurrency", \
                "lambda:PublishVersion" \
            ], \
            "Resource": "arn:aws:lambda:us-east-1:086796595852:function:github-codebuild-demo" \
        }, \
