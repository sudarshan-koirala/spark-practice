# spark-practice
Learning spark the right way

### Steps to create new spark project in Google Cloud Platform
1. Create a project from the navigation bar > new project
2. Create a instance by choosing Dataproc from menu > Enable Dataproc API
3. Create a bucket by choosing Storage from menu > Create new bucket
4. Create service account and add role for the account (Compute OS Login and Dataproc Editor), this is done to use Dataproc and login to the cluster from local machine (other than gcp console itself)
5. Install gcloud sdk in you local machine [mac-example](https://www.youtube.com/watch?v=3wPl-AnegI4&ab_channel=TonyTeachesTech)
6. **First do the authentication of gcloud `gcloud auth login`** 
7. Create a key locally example -> `gcloud iam service-accounts keys create key.json  --iam-account=my-iam-account@my-project.iam.gserviceaccount.com` [Link to gcp website](https://cloud.google.com/sdk/gcloud/reference/iam/service-accounts/keys/create)
8. Authenticate gcp with gcloud auth example -> `gcloud auth activate-service-account test-service-account@google.com  --key-file=/path/key.json --project=testproject` [Link to gcp website](https://cloud.google.com/sdk/gcloud/reference/auth/activate-service-account)
9. Connect the cluster with command from view gcloud command next to ssh dropdown. For example -> `gcloud beta compute ssh --zone "us-central1-a" "mysimbdp-m" --project "learning-bigdata-2021"`
10. Now, you are connected to gcp console through your local machine.
