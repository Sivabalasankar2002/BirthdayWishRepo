🎉 Auto Birthday Wish Lambda Function (Google Chat + AWS)

This Lambda function automatically wishes team members a happy birthday via **Google Chat**, using a scheduled AWS Lambda job and **DynamoDB** as the birthday record source.

⚡ Designed for HR teams, PeopleOps, or developers who want to automate team engagement!

🛠️ What This Does

✅ Daily scan of birthday records  
✅ Matches today's date  
✅ Sends custom birthday message to a Google Chat space  
✅ Fully serverless and free-tier friendly

📦 Requirements

- AWS account with:
  - DynamoDB table: `BirthdayWishes`
  - EventBridge schedule
  - IAM role for Lambda with read access to DynamoDB
- Google Chat space with webhook enabled

🧾 DynamoDB Table Schema

- **Table Name**: `BirthdayWishes`
- **Partition Key**: `email` (String)
- **Billing Mode**: On-Demand (recommended)

Sample Item:

```json
{
  "email": "sivabalasankar2002@gmail.com",
  "name": "Sivabalasankar",
  "dob": "2002-02-09",
  "message": "🎉 Happy Birthday Sivabalasankar! Hope your day is amazing!"
}
