### openshift_commands

***

   <!-- login -->   oc login -u username -p password master-api</br>
   <!-- new project --> oc new-projet project-name</br>
   <!-- Run a container image from Dockerfile in github --> oc new-app --name app-name https://github.com/RedHatTraining/DO288-apps#branch-name --contxt-dir folder-name</br>
   <!-- check build logs --> oc logs -f bc/app-name
