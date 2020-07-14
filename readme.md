This sample shows how to have completion of one pipeline, trigger another

1. Edit `first.yaml` and update the URL of to your concourse instance
2. Set both pipelines:
   1. `fly -t example set-pipeline -c first.yaml -p first`
   2. `fly -t example set-pipeline -c second.yaml -p second`
3. Trigger job in first pipeline
   1. `fly -t example trigger-job -j first/trigger-job`
4. Observe how second pipeline is triggered when first one completes

