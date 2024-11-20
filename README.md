# 🌟 Simplifying Terraform debugging and logging with practical TF_LOG usage 🌟




![new](https://github.com/user-attachments/assets/92e64a40-5032-490e-a8d3-3b73fd8f263e)





## Overview

In Terraform, the log levels help in diagnosing issues or understanding the internal operations during Terraform’s execution. You can set the log level by using the TF_LOG environment variable.


# Here are the log levels available in Terraform:
1.	**TRACE**: This is the most verbose logging level. It provides step-by-step tracing of the Terraform operations and is typically used for debugging and development purposes.
2.	**DEBUG**: Provides detailed logs that include information about resource lifecycle actions, like creation, updating, and deletion. It also shows more internal details than the INFO level.
3.	**INFO**: Provides condensed, high-level command output, which is suitable for regular operations. It’s less verbose than DEBUG.
4.	**WARN**: This level logs any potential issues or warnings that might affect Terraform’s operation. These aren’t necessarily errors, but they might be concerns or information that users should be aware of.
5.	**ERROR**: Only error messages are shown at this log level. This will highlight any issues that are preventing Terraform from executing as expected.


## Enabling TF_LOG

Terraform provides the `TF_LOG` environment variable for controlling log verbosity. You can choose from different levels like `TRACE`, `DEBUG`, `INFO`, `WARN`, and `ERROR`.

### Steps to Enable TF_LOG

1. **Set TF_LOG for detailed trace logs:**

    ```powershell
    $env:TF_LOG = "TRACE"
    terraform fmt; terraform validate; terraform apply;
    ```





    ![1-trace](https://github.com/user-attachments/assets/37972410-ce7d-4a60-ae93-e26b4da3caf4)





####################################################################################
   


2. **Set TF_LOG for error-level logging:**

    ```powershell
    $env:TF_LOG = "ERROR"
    terraform fmt; terraform validate; terraform plan;
    ```





    ![2-error](https://github.com/user-attachments/assets/ab239bbb-341e-4145-8289-a1f0f947a9be)







   #################################################################################################





3. **Write logs to a file:**

    ```powershell
    $env:TF_LOG = "TRACE"
    $env:TF_LOG_PATH = "./logs/terraform.log"
    terraform apply --auto-approve
    ```


This would store the logs in terraform.log in the current directory. Remember that setting a verbose log level like TRACE or DEBUG will produce a lot of output, so use it judiciously.



![3-writing-logs-to-file](https://github.com/user-attachments/assets/50fa8a46-abc6-4a9c-88ca-3da57e02fe09)


































![3-writing-logs-to-file1](https://github.com/user-attachments/assets/2685ad1b-3f3f-4d17-8b1a-902681d1a21e)












# Conclusion:
By leveraging TF_LOG, Terraform users can significantly improve their debugging and troubleshooting workflows. This approach simplifies the process of identifying and resolving issues in infrastructure code, providing clear and actionable insights through detailed logging. With practical TF_LOG usage, managing Terraform configurations becomes more efficient and reliable, allowing teams to better maintain and scale their infrastructure with confidence.





