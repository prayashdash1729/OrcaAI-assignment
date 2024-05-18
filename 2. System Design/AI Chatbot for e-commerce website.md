You have been given access to OpenAI's GPT-4 API. Describe how you would use this model to build a customer support chatbot for an e-commerce website. Outline the steps using a flowchart or points.


## Steps

1. The user interacts with the UI element of the chatbot to put a query.
2. Query is passed through a basic spell checker to correct any spelling mistakes.
3. Identification of user use case from the query (Intent classification)-
    - Useer query can be of different types like-
        - query for order status
        - query for order status
        - query for a product information
        - query for return policy
        - query for technical support
4. If use case is not identified, then we return to the user again to re-enter query.
5. If use case is identified, then we pass the query to GPT to extract information about query (intent related attribute extraction).
    - Some examples may be-
        - User id
        - Order id
        - Product details
        - Technical support details
6. We then pass on the details to the CRM or databases to get responses for each user.
7. Response is generated and sent back to the user.
6. Meanwhile, a record of responses of users and system is kept in a backend database.
7. For model retraining, we use sucessful user queries and model inferences for those queries.
    - Lets say a user has generated 4 queries and the last one was succesful. We can use the response to retrain the model on the first 3 queries that failed.



![Alt text](Flowchart.svg)


### Example

User Interaction:
- User: "What's the status of my order #12345?"
Spell Check:
- Correct any typos or spelling errors.
Intent Classification:
- Determine that the user is asking for "order status."
Intent Attribute Extraction:
- Extract "order #12345" and possibly the user ID from the query.
Query CRM/Database:
- Query the CRM/database for the status of order #12345.
Generate Response:
- GPT-4 processes the retrieved order status information and generates a response.
Example Response
- "Your order #12345 is currently being processed and is expected to ship within 2 days."
Send Response to User:
The chatbot displays the response to the user.
Log Interaction:
- Log the query and response for future analysis and model improvement.
Model Retraining:
- Use logged interactions, especially successful ones, to refine the model's performance over time.

