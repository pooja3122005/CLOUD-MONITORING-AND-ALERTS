# CLOUD-MONITORING-AND-ALERTS

**COMPANY**:CODTECH IT SOLUTIONS

**NAME**: POOJA.U

**INTERN ID**:CT04DG1131

**DOMAIN**: CLOUD COMPUTING

**DURATION**: 4 WEEKS

**MENTOR**: NEELA SANTOSH

**DESCRIPTION**

**Introduction to Cloud Monitoring and Alerts**
Monitoring cloud-based applications is essential for ensuring they remain reliable, performant, and available to users. In this setup, AWS CloudWatch was used to configure a robust monitoring and alerting system for a sample application hosted on an Amazon EC2 instance. The goal was to visualize application metrics through a dashboard and implement alerts that notify the operations team when specific thresholds are exceeded.

 **Deploying the Application**
 To begin the monitoring setup, a basic web server was deployed on an Amazon EC2 instance. This instance served as the testbed for collecting and analyzing operational data. Since EC2 integrates seamlessly with CloudWatch, it automatically provides access to several default metrics, including CPU utilization, network activity, and disk I/O operations. These metrics are essential for understanding the performance and health of the application.

**Enabling Detailed Monitoring**
By default, CloudWatch collects metrics at five-minute intervals. To get more granular data, detailed monitoring was enabled, reducing the interval to one minute. Furthermore, to collect deeper system-level metrics—such as memory usage, disk space, and custom application logs—the CloudWatch Agent was installed and configured on the EC2 instance. This agent pushed additional data to CloudWatch, offering better visibility into the internal state of the server.

**Creating the CloudWatch Dashboard**
With metrics flowing into CloudWatch, a custom dashboard was created to visualize the data in real time. Named `dashboard1`, this dashboard included various widgets tailored to the application:
**Line charts** showing CPU utilization and memory usage trends over time.
**Number displays** for current disk space and active HTTP requests.
**Network traffic graphs** to monitor bandwidth usage.
**Optional log widgets**, depending on whether CloudWatch Logs were enabled.
This dashboard served as a centralized hub for monitoring the health and performance of the application at a glance.

 **Configuring CloudWatch Alarms**
Monitoring is only useful if it can trigger action when something goes wrong. For this reason, **CloudWatch Alarms** were configured to detect and respond to abnormal conditions:
* An alarm for **high CPU usage** was set to trigger when utilization exceeded 80% for more than five minutes.
* Another alarm monitored **disk space**, activating if free storage dropped below 1GB.
* Additional alarms could monitor **network traffic spikes**, **error rates**, or **response times**, depending on application needs.
These alarms allow the system to react to early signs of failure or overload.

 **Setting Up Alerts with SNS**
To make sure alarms lead to real-world actions, **Amazon SNS (Simple Notification Service)** was used to send alerts. A notification topic named `alaram1` was created, and email addresses of the system administrators were subscribed to it. When an alarm is triggered, CloudWatch publishes a message to the SNS topic, which then forwards the alert to all subscribers via email.

This ensures that critical issues are communicated immediately, enabling quick responses and minimizing downtime.

 **Testing and Verification**
To verify the entire setup, simulated scenarios were executed. For instance, the EC2 instance was stressed to push CPU utilization above the configured threshold. Likewise, disk usage was artificially increased to trigger the low-space alarm. Each time, the dashboard updated in real time, and alert emails were successfully received, confirming the system was working correctly.

**Conclusion**
This cloud monitoring and alerting setup demonstrates how **AWS CloudWatch**, combined with SNS, can be used to monitor a cloud-based application effectively. From deploying the monitoring agent and building a real-time dashboard to configuring alarms and setting up automated notifications, each step ensures that application health is continuously tracked and that issues are detected and communicated without delay. This proactive approach to monitoring is crucial for maintaining high availability and optimal performance in modern cloud environments.


**OUTPUT**

