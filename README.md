# codespaces-examples

## Prebuild Failure Notification Issues

[This action](https://github.com/urcomputeringpal/codespaces-examples/blob/main/.github/workflows/codespaces-prebuilds-failure-issues.yaml) can be copied/pasted into any repository that contains a Codespaces Prebuild to open an issue when a prebuild configuration fails and close it when it's working again.

## Known Issues

### Forwarded Ports are unstable after rebuild if using Docker Compose

### Notification of failed Codespaces Prebuilds require Actions notifications to be enabled

This setting has an undocumented dependency:

![image](https://user-images.githubusercontent.com/47/189713795-cc788c7c-0765-436a-a13a-07517aecc984.png)

To be notificated of the failure of Codespaces Prebuilds (which appear to be implemented as a "Dynamic Github Action") a user must have the following setting enabled to allow notifications from GitHub Actions:

![image](https://user-images.githubusercontent.com/47/189713696-ec9dc530-1327-4161-b2b5-f0b8ce7507a9.png)

https://docs.github.com/en/actions/monitoring-and-troubleshooting-workflows/notifications-for-workflow-runs
