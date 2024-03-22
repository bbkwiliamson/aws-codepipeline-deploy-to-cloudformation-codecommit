# aws-codepipeline-deploy-to-cloudformation-codecommit


on the roles, there is permission boundary which is currently on the template commended.
that is because you might not need it, is just for extra layer of applying least privilege rule on permissions.

secondly on the ACTIONS part, there is *, which represent all permissions or just means admin permission. both the service role and the deploy role must have all the permissions it needs for the pipeline to be successfull.

parameters are used in order to make sure that the same template can be used by various teams and deploy with different naming and avoid conflicts

the other template. s3.yml, is used to show you an example of how this works. you take the template and push it to your repo which is created, whether manually on the console or via git, once the changes are merged, the pipeline will kickoff.

the codepipeline template has comments and those comments MUST be adhered to, for the successfull implementation of the pipeline.
