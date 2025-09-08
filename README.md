# Polly-Enabled-Audio-Reader
Read once, listen everywhere.

Project Description:

This project expands reach by making written material accessible to audiences who prefer listening, multitaskers on-the-go, and people with visual impairments or reading difficulties. Beyond accessibility, it reimagines how knowledge and storytelling are consumed: every written piece becomes a podcast-like experience at scale.
By integrating text-to-speech pipelines with AWS Lambda, S3, and Polly, the system is serverless, scalable, and cost-efficient. It empowers creators, educators, and publishers to unlock a new channel—“Read once, listen everywhere.”

Use Cases:

Content Accessibility: Provides audio versions of written content for visually impaired users.

Learning: Enables users to listen to educational materials, enhancing learning experiences.

Content Distribution: Offers an additional medium for content consumption, increasing engagement.

Convenience: Allows users to listen to articles or books while multitasking, such as during commutes or workouts.

PROJECT ARCHITECTURE:
<img width="1917" height="1000" alt="Screenshot (10)" src="https://github.com/user-attachments/assets/de5231f0-b932-4e28-b8fc-a056e84f1ddb" />

Steps to Build the Project:

Step 1: Set Up an AWS Account

Step 2: Create two S3 Buckets (Source S3 Bucket Name: source-bucket-tts, Destination S3 Bucket Name: destination-bucket-tts)

Step 3: Create an IAM Policy (IAM Policy Name: tts-policy)

Step 4: Create an IAM Role (IAM Role Name: tts-polly-role) and attach tts-policy and AWSLambdaBasicExecutionRole Policies

Step 5: Create and Configure the Lambda Function (Lambda Function Name: TextToSpeechFunction)

-->Set the runtime to Python 3.8.

-->Set the execution role with necessary permissions for S3 and Polly. (Step 4)

-->Add Environment Variables (SOURCE_BUCKET: Name of your source S3 bucket and DESTINATION_BUCKET: Name of your destination S3 bucket.

Step 6: Configure S3 Event Notification

Set up an event notification in the source S3 bucket to trigger the Lambda function on new object creation events with the .txt suffix.

Step 7: Write Lambda Function Code

Step 8: Test the System


      
  

