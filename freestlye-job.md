Create a simple freestyle job 
Note;
In order to have tool available in the jenkins UI, you have to first install it as plugin
Freestyle jobs as the name implies are not used for production but rather freestyles.
goto create job, Enter the name of the job and select freestyle job.
goto configuration. Under Build Steps, select "add build step" then select execute shell. This allows you to enter commands such as you will execute inside the jenkins container. Just like running commands on the jenkins cli.
