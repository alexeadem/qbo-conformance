# CNCF conformance results with `qbo` Cloud

# Requirements
> * Chrome or Firefox browser
> * Email authenticated by Google (Google Account)

# Request access to `Qbo` Cloud

> Email `support@qbo.io` and provide a google email in your request that you'll use to authenticate in Qbo Cloud.

# Login to the `Qbo` console

> Once you receive an email confirmation you can login to:

https://console.cloud.qbo.io:9601

# Run conformance test

> Conformance test are run with `qbot`. `qbot` is a typing bot that will type the commands for you. Alternatevely you can type the command yourself in the shell.


`qbot` will perform the following tasks:
* Create a `qbo` cluster
* Configure `kubectl`
* Download and configure `sonobuoy` 
* Run confomance test on the version entered.

`qbot` usage:

```bash
./qbot help
>>> ./qbot help                 -- Show usage
>>> ./qbot list                 -- List available Kubernetes image tags
>>> ./qbot conformance {tag}    -- Run CNCF conformance results for qbo
```

List available Kubernetes tags:

```bash
./qbot list
```


Select version and run conformance test. Example: 
```bash
./qbot conformance v1.28.0
```
Get results
```bash
cat /tmp/qbo/sonobuoy/v1.28.0/qbo/e2e.log | grep Pass
```
> For more information visit: https://docs.qbo.io/
EOF
