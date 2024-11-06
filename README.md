# ace-box-sandbox-demo-apps

This External Use Case for the acebox deploys an environment with a few demo apps.

## Version and compatibility

Please add a note pointing out which versions of the external use case are compatible with the respective ACE-Box versions:

| Release | Verified against ACE-Box version | Comment |
| --- | --- | --- |
| v1.0.0 | v1.26.9 ||

### Required extra vars

|Variable name|Description|
|---|---|
|dt_environment_url_gen3|Dynatrace Gen3 environment url, e.g. `https://<YOUR ENVIRONMENT ID>.sprint.apps.dynatracelabs.com`|
|dt_oauth_sso_endpoint|Dynatrace OAuth endpoint, e.g. `https://sso-sprint.dynatracelabs.com/sso/oauth2/token`|
|dt_oauth_client_id|Dynatrace OAuth client id. Make sure ALL scopes of `app-engine`, `storage`, `automation`, `state`, `state-management`, `document`, `davis`, `settings` and `hub`  are assigned to your OAuth client|
|dt_oauth_client_secret|Dynatrace OAuth client secret|
|dt_oauth_account_urn|Dynatrace OAuth account URN|

Extra vars can be set e.g. as Terraform variables:

```
extra_vars = {
  dt_environment_url_gen3 = "https://<YOUR ENVIRONMENT ID>.sprint.apps.dynatracelabs.com"
  dt_oauth_sso_endpoint   = "https://sso-sprint.dynatracelabs.com/sso/oauth2/token"
  ...
}
```

## What's inside

The following modules are deployed:
- k3s
- Dynatrace Operator
- Synthetic Activegate
- EasyTravel
- EasyTrade
- Unguard
- Hipstershop