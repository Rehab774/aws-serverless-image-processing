# 🖼️ AWS Serverless Image Processing System

A complete serverless image processing application that automatically resizes images uploaded to Amazon S3 using AWS Lambda, stores metadata in DynamoDB, and provides a REST API for uploads via API Gateway.

## 📋 Project Overview

This project demonstrates a event-driven serverless architecture for image processing. When images are uploaded to an S3 bucket, AWS Lambda functions are automatically triggered to process the images and store metadata.

## 🏗️ Architecture Diagram

![Architecture Diagram](/architecture-diagram.png)

## ⚡ AWS Services Used

- **Amazon S3** - Storage for original and processed images
- **AWS Lambda** - Serverless compute for image processing
- **Amazon DynamoDB** - Metadata storage for processed images
- **Amazon API Gateway** - REST API for image uploads

## 🔄 Workflow

1. **Image Upload**: Users upload images via API Gateway or directly to S3
2. **Automatic Processing**: S3 triggers Lambda function on new uploads
3. **Image Resizing**: Lambda resizes images to 500px max dimension
4. **Metadata Storage**: Processing details stored in DynamoDB
5. **Result Storage**: Resized images saved to processed S3 bucket

## 🚀 Deployment

### Prerequisites
- AWS Account
- Python 3.9+

### Steps
1. Create S3 buckets for original and processed images
2. Deploy Lambda functions with required IAM roles
3. Set up DynamoDB table for metadata
4. Configure API Gateway endpoints
5. Test the image processing pipeline

## 🛠️ Features

- ✅ Automatic image resizing (500px max dimension)
- ✅ Serverless architecture - no servers to manage
- ✅ REST API for image uploads via API Gateway
- ✅ Metadata tracking in DynamoDB (filename, sizes, timestamps)
- ✅ Event-driven processing with S3 triggers
- ✅ Scalable and cost-effective AWS services

## 🔧 Technical Details

### Lambda Functions
- **resizeImageFunction**: Triggered by S3 uploads, resizes images using Pillow
- **apiImageUploadFunction**: Handles API requests for direct image uploads

### AWS Configuration
- S3 buckets with proper IAM permissions
- Lambda functions with appropriate timeouts and memory
- DynamoDB table for storing image metadata
- API Gateway with CORS enabled

## 📞 Contact

For questions about this serverless image processing project, please refer to the AWS documentation or open an issue in this repository.

---

*Built with AWS Serverless Technologies 🚀*
