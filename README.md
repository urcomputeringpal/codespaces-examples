# codespaces-examples

## Prebuild Failure Notification Issues

[This action](https://github.com/urcomputeringpal/codespaces-examples/blob/main/.github/workflows/codespaces-prebuilds-failure-issues.yaml) can be copied/pasted into any repository that contains a Codespaces Prebuild to open an issue when a prebuild configuration fails and close it when it's working again.

## Known Issues

### Forwarded Ports are unstable after rebuild if using Docker Compose

Sometimes they don't work at all, sometimes they drop every other request. Manually stopping and then stopping the port-forward seems to work around the problem.

Reproduction and details here: https://github.com/jnewland/devcontainer-example/tree/docker-compose-port-forward

### Notification of failed Codespaces Prebuilds require Actions notifications to be enabled

GitHub's built-in feature for being notified if Codespace prebuilds fail has an undocumented dependency:

![image](https://user-images.githubusercontent.com/47/189713795-cc788c7c-0765-436a-a13a-07517aecc984.png)

For some reason, this requires any user configured to receive those notifications to also have a setting enabled that would send them notifications for _all other failing Actions workflows they trigger_. This is unfortunately a totally overwhelming amount of email for anyone, but especially too much email for an integrator of a tool like Actions that requires 'live debugging' and the judicious use of workarounds that require Personal Access tokens. 😅 I have heard legends that getting the results of all builds that you trigger in your inbox is a MSFT cultural norm, but it's not really my cup of tea.

![image](https://user-images.githubusercontent.com/47/189713696-ec9dc530-1327-4161-b2b5-f0b8ce7507a9.png)

https://docs.github.com/en/actions/monitoring-and-troubleshooting-workflows/notifications-for-workflow-runs

## Contact

Interested in help with your repository's Codespaces configuration? [Get in touch!](https://urcomputeringpal.com/services)