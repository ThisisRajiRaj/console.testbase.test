## Simple console app to showcase using Test Base to test your applications

### HeightGained
The app is a calculator to compute vertical gain based on 
grade % and horizontal distance traveled. It can do the math
in metric system or US customary units. This app is simply a sample/test 
app to try out the functionality of Test Base.

#### Usage
```
    HeightGained.exe gradeinPercent distance useMetricUnits
    gradeinPercent and distance should be numeric
    useMetricUnits should be 1 for using meters instead of miles and feet
```

### Scripts to submit HeightGained to TestBase 
Install, close, and uninstall scripts simply returns 0
Launch script launches the app and returns 0 if the execution was successful

### Using Test Base API
TestBase.py shows using Test Base API to list test summaries. The python function
returns 0 if there was no test failure in the last 24 hours, 1 if there was no run 
in the last 24 hours, and -1 if there was a failure in the last 24 hours.

In order to run the python script, set the following environment variables. To get the client ID and secret,
run install Azure CLI, run az login from commandline, and then run az ad sp create-for-rbac
```
AZURE_TENANT_ID=<tenand id>
AZURE_CLIENT_ID=<appId from sp create-for-rbac>
AZURE_CLIENT_SECRET=<password from sp create-for-rbac>
AZURE_SUBSCRIPTION_ID=<subscription id>
RESOURCE_GROUP_NAME=<resource group name for test base account>
TESTBASE_ACCOUNT_NAME=<test base account name>
```

For more info, visit [Test Base Blog](https://techcommunity.microsoft.com/t5/test-base-blog/test-base-for-microsoft-365-sdk-amp-apis-now-available/ba-p/2888698)
