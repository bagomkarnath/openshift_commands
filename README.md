### openshift_commands

***

   <!-- login -->   oc login -u username -p password master-api</br>
   <!-- new project --> oc new-projet project-name</br>
   <!-- Run a container image from Dockerfile in github --> oc new-app --name app-name https://github.com/RedHatTraining/DO288-apps#branch-name --contxt-dir folder-name</br>
   <!-- check build logs --> oc logs -f bc/app-name</br>
   <!-- get all running pods --> oc get pods</br>
   <!-- logs of a pod --> oc logs pod-name</br>
   <!-- delete all pods for an app --> oc delete all -l app=app-name</br>
   <!-- dockerfile Expose port --> EXPOSE 8080</br>
   <!-- dockerfile running web server in an unprivileged port --> RUN sed -i "s/Listen 80/Listen 8080/g" /etc/httpd/conf/httpd.conf</br>
   <!-- dockerfile changing group id and permission of the folder --> RUN chgrp -R 0 /var/log/httpd /var/run/httpd && chmod -R g=u /var/log/httpd /var/run/httpd</br>
   <!-- dockerfile user instruction for an unprivileged user --> USER 1001</br>
   <!-- expose service --> oc expose svc/app-name</br>
   <!-- get route --> oc get route</br>
   <!-- delete project --> oc delete project project-name
