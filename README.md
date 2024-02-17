                                                **AWS-cost_optimization**
                                                
We'll create a Lambda function that identifies EBS snapshots that are no longer associated with any active EC2 instance and deletes them to save on storage costs

Step: 1 Create Lambda function and enter code from cost_optimize.py file into it.

![Screenshot 2024-02-17 172945](https://github.com/hijackhim/AWS-cost_optimization/assets/105789918/90118ba9-20c3-48a9-8ede-d39af8bdabfc)

![Screenshot 2024-02-17 172936](https://github.com/hijackhim/AWS-cost_optimization/assets/105789918/b0256e23-ffe4-490a-b109-50eb1ba8fe50)

Step: 2 Create a EC2 instance and hence Volume will be automatically attached with it.

![image](https://github.com/hijackhim/AWS-cost_optimization/assets/105789918/bd592e91-0377-41b5-8409-219088989afb)

Step: 3 Create a Snapshot of the volume created with the EC2 instance.

![Screenshot 2024-02-17 173545](https://github.com/hijackhim/AWS-cost_optimization/assets/105789918/ef60cb48-fede-46cd-bde8-7367eb3587b5)

Step: 4 Now Deploy and test the Lambda function created in the first step.

Step: 5 Now nothing will happen until we terminate the instance which we created before and along with it instance volume will also be deleted from the record.

![Screenshot 2024-02-17 182216](https://github.com/hijackhim/AWS-cost_optimization/assets/105789918/16e00b22-9965-4d43-95c1-e6e2915c8d41)

Step: 6 Now test the Lambda function again and hence snapshot will be deleted automatically as Lambda function is coded to do so i.e. if there is a snapshot which is associated with volume, which is not present then snapshot will get deleted.

![Screenshot 2024-02-17 182446](https://github.com/hijackhim/AWS-cost_optimization/assets/105789918/5b545143-4fb5-4363-8a1e-a7b4cc6da550)

![Screenshot 2024-02-17 182519](https://github.com/hijackhim/AWS-cost_optimization/assets/105789918/081e7048-2d3c-4074-b9cf-6a112879f669)

To make this process automatic we can define rules in the CloudWatch and then cloudwatch triger lambda to do same task after certain time period.
