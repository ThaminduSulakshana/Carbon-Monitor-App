
The web page looks like this.
-
![Screenshot 2023-01-14 at 1 47 50 PM](https://user-images.githubusercontent.com/8187657/212475098-463548cb-6c91-4e67-93a9-b6e0e0b73e16.png)


The **List VMs** button prints out the list of VMs for which the carbon emissions have been computed. The list returned by this button continues to grow.
The **Get Carbon Emission** button can be used to retrieve the carbon emission report for the provided VM.

Note that at the moment the data is artificially generated but a real source of data could be integrated to this system.

## Unit test
Unit test can be run by executing **./run_unit_test**

## Integration test
Integration test can be run by executing **./run_integration_test**

## CI/CD
On every push a github action is triggered that runs the unit and the integration test. After that a docker image is created that is deployed to the heroku. The file **.github/workflows/ci.yml** can be changed to alter the deployment strategy accordingly. The docker file **Dockerfile** creates the heroku docker image.
