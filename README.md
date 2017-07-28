# cf-ssh-host
Unmapped empty static Cloud Foundry webapp which can be used for SSH dial-in without impacting hot applications

# Usage
Simply run

    cf push

inside the cloned folder. After finishing that,

    cf ssh ssh-host

returns a remote shell running on the deployed container.

## Opening a tunnel to a remote host
In some cases, you don't have direct access to CF-managed services, e.g. databases running inside the private lan on the other side.
To overcome this, the CF CLI offers the possibility to open a tunnel to a remote host through the deployed ssh-host app:

    cf ssh ssh-host -L 15432:your.remote-host.com:5432

After that, all requests to localhost:15432 are forwarded to your.remote-host.com:5432 through the SSH tunnel.

## Further features

cf ssh offers some more features. Check them out!

    cf ssh --help

## Troubleshooting
If you have issues with the ssh dial-in, there could be several open setup issues:
Please check the CF docs for more details:
-  https://docs.cloudfoundry.org/devguide/deploy-apps/app-ssh-overview.html
-  https://docs.cloudfoundry.org/devguide/deploy-apps/ssh-apps.html
