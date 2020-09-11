#lab: Getting Started with Cloud Marketplace
## Objective :learn how to launch a solution using Cloud Marketplace.

##stepsA:
1. Sign in to the Google Cloud Platform (GCP) Console
2. Open Google Console

## StepB:
1.Use Cloud Marketplace to deploy a LAMP stack
2.launch LAMP Certified by Bitnami
3.Click Deploy

##Stepc:
1.Verify your deployment
2click SSH on Get started with LAMP Certified by Bitnami
3. In the just-created SSH window, to change the current working directory to /opt/bitnami with the following
```
cd /opt/bitnami

```        

4.  copy the phpinfo.php script from the installation directory to a publicly accessible location under the web server document root, execute the following command:    ```

 sudo sh -c 'echo "<?php phpinfo(); ?>" > apache2/htdocs/phpinfo.php'

```

5.close the SSH window, execute the following command:   ```
          exit
```

6. open a new browser and type in ```

http://SITE_ADDRESS/phpinfo.php

```
where SITE_ADDRESS is your URL
7. close.
