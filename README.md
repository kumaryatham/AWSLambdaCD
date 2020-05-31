Here is the process to configure CD: https://www.youtube.com/watch?v=aGI4Wlm5c9U

Serverless deployment continuous deployment workflow
    Deploy lambda function codebase into github repository
    Maintain two files
        SAM Template ( Serverless Application Model )
            Its similar to cloudformation with minor changes
        CodeBuild Spec
            YAML
            Its will convert SAM to cloudformation
    Once we make the changes on this git repo, automatically build trigger and pipeline executes
    Before the AWS end we need to create below stuff
        Create Service Role
            S3
            CodePipeline
            Lambda
            API Gateway
            Cloudformation
        Application Setup
            SAM Template ( samTemplate.yaml)
            CodeBuildSpec ( BuildSpec.yml)
        Create Pipeline
            Code Pipeline Stages
                Source
                Build
                Create Change Set
                Approve Change Set
                Execute Change Set
