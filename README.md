# cf-ssh-host
Unmapped empty static Cloud Foundry webapp which can be used for SSH dial-in without impacting hot applications

# Usage
Simply run

    cf push

inside the cloned folder. After finishing that,

    cf ssh ssh-host

returns a remote shell running on the deployed container.

If you have issues with the ssh dial-in, there could be several open setup issues:
Please check the CF docs for more details:
-  https://docs.cloudfoundry.org/devguide/deploy-apps/app-ssh-overview.html
-  https://docs.cloudfoundry.org/devguide/deploy-apps/ssh-apps.html