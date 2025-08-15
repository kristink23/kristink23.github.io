The artifact I selected for this portion of my capstone is the same Weight Tracking App I used in earlier enhancements, but now fully migrated to AWS Amplify with DynamoDB and Cognito. Originally, the app kept entries in a local SQLite database, flat and single‐user only. This new version stores data in the cloud, separates each user’s entries, and requires email verification before login. 

I chose this artifact because it let me demonstrate end‐to‐end cloud integration and secure, multi‐user data design, which are skills I hadn’t showcased yet. In its earlier form, the app didn’t scale across devices, lacked user separation, and risked data loss if the device failed. My enhancements include: 

- Cloud Storage Migration: I replaced all SQLite logic with Amplify DataStore and GraphQL operations, automatically syncing with a DynamoDB backend. 

- Multi‐User Schema: I redesigned the table to use userId as the partition key and entryId as the sort key, so each user only sees their own records. 

- Secure Access Control: I configured Cognito to enforce email verification and token‐based authentication on every API call. 

- Offline Resilience: With Amplify’s local cache, users can log entries offline, and changes should sync on reconnect. 

- Manifest & Build Configuration: I added placeholder substitutions for deep‐link schemes and fixed dependency mismatches in my Gradle catalogs. 

These enhancements align directly with my Module One plan to “modernize the data layer with cloud services, normalize the schema, and secure access with Cognito.” They also satisfy Outcome 2 (integrate third‐party cloud services) and Outcome 4 (design secure, multi‐layer architectures). The updates needed to my original outcome‐coverage plan are only which AWS system I used. However, this artifact fully demonstrates the competencies I was aiming for. 

Working through this migration taught me a great deal about the AWS developer ecosystem. I learned to navigate the Amplify CLI (including provisioning GraphQL APIs and IAM roles), debug CloudFormation permission errors, and resolve version‐catalog issues in Gradle. Pivoting mid‐week from the deprecated AWS Mobile SDK to Amplify Gen 1 forced me to master placeholder substitution in AndroidManifest.xml and troubleshoot missing generated classes. Finally, implementing offline sync reinforced the importance of handling asynchronous updates gracefully in the ViewModel and UI. Though each step introduced new challenges, especially around build configurations and authentication flows, the result is a robust, scalable app that demonstrates my ability to architect cloud‐native mobile solutions. 
