1. First List down the Functional requirements and clarify with the interviewer whether that is fine for the
required scope or not. Add/ Remove/ scale up / scale down the requirements based on the feed back.

2. List down the non-functional requirements. If possible map each non functional requirement with a functional
requirement and say why we need this assumption.
    - Availability
    - Usability
        - What expertise a user needs to leverage this system - No technical knowledge/ less technical knowledge.
        - how to support disable people.
    - Scalability
        - Handle eventual user and data growth.
    - Elasticity.
        - Handle sudden spikes in the system.
    - Consistency or Eventual Consistency
        - Is it data critical system to populate data to all nodes immediately -- > Consistency is the key Factor
        - Is the system needs to be available to the customer and it can be consistent after some time --> Eventual
        Consistency
    - Degree of Reliability
    - Latency and Rendering
        - Mention the latency in ms.
        - Systems with high latency can load quickly to provide seamless solutions.
    - Compatibility with all devices, Internalization, Security.

3. Design constraints.
    - Discuss design constraints, including the read/write heavy nature of the system and the importance of storage for 
crucial data. Consider the type of data that is critical and
     - Consider the type of data that is critical and non-critical, and determine the appropriate storage solution.

4. Capacity Constraints and Cost Estimation
    - Estimate the total users and active users/day.
    -  Estimate the capacity for a single entity
        - Photo - 200KB
        - Video - 5MB
        - Text  -  10KB
    - Estimate the new total capacity for a day and second using (active users * cap of a single entity).
    - Using this calculate the capacity for next 10 years and say that your storage system will scale and handle this.

5. Higher level system design
    - Outline the high-level system design, including the choice between a monolithic or microservice architecture.
    - Take a use case. Build a microservice for that use case, Connect with the database and user and explain.
        - Eg: A DB microservice could receive the request from the user, store the images and videos in S3, 
        store the metadata in a NoSQL database, and return the response to the user
    - Speak about how we are going to store the meta data (Photo ID a s a key and S3 location, photo desc,
    uploaded time as values)

   
