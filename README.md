def lambda_handler(event, context):
    # Extract the bucket name from the event
    bucket_name = event['Records'][0]['s3']['bucket']['name']
    
    # Your desired logic here
    print(f"New object uploaded to bucket: {bucket_name}")
    
    return {
        'statusCode': 200,
        'body': json.dumps('Lambda function executed successfully!')
    }
