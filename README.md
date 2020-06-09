# Drupal 8 WXT on OpenShift

Built with s2i, based on the [ISED fork of Drupal WxT](https://github.com/ised-isde-canada/site-wxt/tree/ised).

Build, deploy, install with a Tekton pipeline.

## Limitations

Probably lots... really just a testt to see how easily this could be done with Tekton.

## How to Run

```
$ oc apply -k overlays
$ oc create -f pipelinerun/run-install.yaml
```

This will take a few minutes, as it will run the s2i build, deploy the conatiner, then do the actual Drupal install with drush.