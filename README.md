<div align="center">
  <img src="img/intro.png" height = "200"/>
  <p style="font-size:1.2rem"><a target="_blank" href="https://talktolisten.com">Talk To Listen</a></p>
</div>

Discover a new world of interaction with 'Talk To Listen' on your mobile phone – where your voice brings characters to life! Engage in seamless conversations with a diverse universe of characters, each boasting their own unique personality and voice. 

Check out [website](https://talktolisten.com) for download links and previews.

### Features
- **Voice-Activated Conversations**: Interact with characters using your voice, you don't have to type anything, or touch the screen, just talk and listen.
- **Diverse Characters**: Engage with a wide range of characters, each with their own unique personality and voice.
- **Real-Time Interaction**: Experience real-time responses to your voice commands.
- **Group Conversations**: Talk with multiple characters at once.
- **Immersive Storytelling**: Dive into a world of storytelling and adventure.
- **Customizable Characters**: Personalize your characters with unique traits and characteristics.
- **Cross-Platform Compatibility**: Access 'Talk To Listen' on any device, anytime, anywhere.
- **Multi-Language Support**: Communicate with characters in multiple languages.
- **Safe and Secure**: Enjoy a safe and secure environment for conversations, generating content that is safe for all ages.

## Tech Stack
<div style="background-color: #fff; width: 100%;" align="center">
  <img src="https://ttl.blob.core.windows.net/ttl-presentation/tech-stack.png" width = "100%"/>
</div>

## Architecture
<div style="background-color: #fff; width: 100%;" align="center">
  <img src="https://ttl.blob.core.windows.net/ttl-presentation/architecture.png" width = "100%"/>
</div>

## Overview
The application's architecture is distributed, with several components interacting to provide the overall functionality. The front-end is built with Expo React Native, Redux, Firebase, and Axios, while the back-end uses FastAPI, SQLAlchemy, Firebase, Docker, and other technologies. The data is stored in a PostgreSQL database, and the application uses GitHub Actions, Docker, and Azure services for continuous integration and deployment. It also integrates with third-party APIs for features like voice live streaming and text to speech.

### 1. Infrastructure 
- Tech: Azure Virtual Machine, Azure Application Gateway, Azure Load Balancer, Azure Virtual Network, Azure Network Security Group.
- **Azure Application Gateway**: A web traffic load balancer to manage traffic to your web applications. (This is expensive, so it is likely to be removed in the future.)
- **Azure Load Balancer**: Distributes incoming network traffic across multiple virtual machines to ensure high availability and fault tolerance.
- **Azure Virtual Network**: Connects virtual machines to each other and to other Azure services securely. The virtual machined are only accessible through this internal load balancer.
- **Azure Network Security Group**: Provides network security by filtering inbound and outbound traffic to the virtual machines.

### 2. Front-end
- Tech: Expo React Native (JavaScript), Redux, Firebase, Axios, Expo Update.
- [GitHub](https://github.com/Talktolisten/talktolisten-frontend)

---

- **Expo React Native (JavaScript)**: A cross-platform framework for building mobile applications using JavaScript and React. It allows developers to write code once and deploy it on both iOS and Android platforms.
- **Expo Update**: Service that allows over-the-air updates for Talk To Listen. The app can be updated immediately without going through the app store. Any bugs or issues can be fixed quickly and efficiently.
- **Redux**: A state management library for JavaScript applications. It helps manage the application's state in a predictable way.
- **Firebase**: Provide secure authentication for users and store data in real-time.
- **Axios**: A promise-based HTTP client that makes it easy to send asynchronous HTTP requests to the backend server.

### 3. Back-end
- Tech: FastAPI(Python), SQLAlchemy, Firebase, Docker, Nginx, Gunicorn, Alembic, Pydantic, Pytest, RESTful APIs, Azure Virtual Machine.
- [GitHub](https://github.com/Talktolisten/talktolisten-backend)
- [API Documentation](https://ttl-api-reference.vercel.app)

---

- **FastAPI( Python)**: Modern, fast (high-performance) Python framework for building APIs.
- **RESTful APIs**: The backend services expose RESTful APIs that the frontend can consume to interact with the application.
- **Azure Virtual Machines**: Multiple virtual machines are used to host the backend services. The virtual machines are duplicated to ensure high availability and fault tolerance. Talk To Listen uses Azure Virtual Machines to host the backend services, and always has more than one instance running to ensure that the application is always available.
- **SQLAlchemy**: A Python SQL toolkit and Object-Relational Mapping (ORM) library that provides a set of high-level APIs for working with databases.
- **Firebase**: Provides secure authentication with frontend and backend services. Only allowed users can access the application.
- **Docker**: The backend services are containerized using Docker to ensure consistency and portability across different environments.
- **PyTest**: All backend services are tested using PyTest to ensure that they work as expected.
- **SSL/TLS**: The backend services use SSL/TLS to encrypt data in transit and ensure secure communication between the frontend and backend.

### 4. Database
- Tech: PostgreSQL, Azure Database for PostgreSQL, Azure Blob Storage, Azure CDN (Content Delivery Network).

---

- **PostgreSQL**: Talk To Listen uses PostgreSQL as the primary database to store user data, character information, and other application data.
- **Azure Database for PostgreSQL**: A fully managed database service that provides high availability, scalability, and security for PostgreSQL databases.
- **Azure Blob Storage**: Used to store large amounts of unstructured data, such as images, audio files, and other media files.
- **Azure CDN (Content Delivery Network)**: The Azure CDN is used to cache static content, such as images and media files, to improve performance and reduce latency for users.

#### Design
- The database schema is designed to store user data, character information, and other application data in a structured and efficient manner.
- **Entity-Relationship Diagram**: The database schema is designed using an Entity-Relationship Diagram (ERD) to visualize the relationships between different entities and attributes.
  
<div style="background-color: #fff; width: 100%; border-radius:1rem">
  <img src="https://mermaid.ink/img/pako:eNqFktFugjAUhl-FnGt5Ae4YI45sDkLRKxJS26M2A0pKMTHguwtlTOKY61XTfuf7T9PTApMcwQFUr4IeFS3S0urXlvix1XW2LVuztz-Cd5_YL2FCLMdKIRdfWKcwwv3pfyzP9pcJn7s3PiHu2jccU0j1ovUJNZd5b25imBP9Zem6-3VFlRZMVHPPFPGo2mMuy2OdaTmRuzDwfrhBb5RKngXHOjtLwTA7SLXU4Fi68Ip1HG4jkznLj9w4Cbwgcj_HDFGyvOF_tnx3PPYNKyhQFVTw_qPboTgFfcICUxhQjgfa5HrQXnuUNlqSS8nA0arBFTQV71v9no7pELnQUm3G2TEjdL0BuQ6zJA?type=png" width = "100%"/>
</div>

- **UML Diagram**: The database schema is designed using a Unified Modeling Language (UML) diagram to visualize the classes, attributes, and relationships between different entities.

<div style="background-color: #fff; width: 100%; border-radius:1rem">
    <img src="https://mermaid.ink/img/pako:eNqtVluv2jAM_itRHhkcjV1eeDybtocdpCNN28OEFKVtKNnapsoFqTriv89pCpTGAXbhhcqfHdufHccvNFeFoCuaV9yYj5KXmtebhsCvl5BvRmjyEiT-tzBWy6YkDuRMFmRFnr_gaMNrESNlzWUVi7dSG8twE4gjggpuBSlUNhJZWQtjed2SXAuAC8ZtfJhxmcm1bK1UTYxmUsXCVqutrARrZW6dRgIEr9aZWG53Yhz0qydp7Iw8Kksq-Qviy5QdrA5jyr3CmHHZWAKqabY9iFNndkpbVogrKV8Fb6aeA9Gl0t39dfDZ7JXMRcjnE5JPqYWw8DGxalzN8h23ZiL3ZCLsH71nXcJNq-We5x3iXzSF0FHh-qswVK5jvsWx6n33uUX1G2WMVTDAeA0DdrVMQQWibhU4S-FQzL28SCyV8PnmNaXjJdryXSX--PLdLImBE6DdnK4QZtfCGAgm4rYOcoRdj_qOQVrNQ6VWrmUJhSGi4fB_SLXvFMz9SAVu8FQjU6oSvCHSeBSh4wPEHXFxTiY1lhNchAGzTENv0tDbNPQuDb2fQncMjv4pGEoyMr_g5bOvKkrOtN7P6Ow56eDXMcFhbH5zdsbz538zAC-JuYOFVIUQ8BzhTxg1owAP06WBPfmxzKIQkP3hr_xPGYIAwkc_pjd0uaFktljA1wy-phGtQB7eDRqs_KN7r5G_ske7yNvrhwdvuz6VaENDqElXty1STvou9_o7Pj09KKDKLddW5rIdezg6P2n3lsuxWSYq1ZSGWXU0Ck9dUDuR9qgGL-G1MSw8PlulkWxOVuEoJPV0YOd7jkd3xie-Lq9HT58y9gqBuNEljXROa6FhuS1gme77fUPD_ke9ciG23FXW-ziAKndWfe2anK62vDJiTl3rN9ph_z5JRSGt0uthQ_d_c3Db_FAKdKx24vAbOkyIsg?type=png" width="100%" />
</div>

### 5. Continuous Integration/Continuous Deployment
- Tech: Git/GitHub, GitHub Actions, Docker, Azure Virtual Machine

--- 

- **Git/GitHub**: The source code is stored in GitHub repositories for version control and collaboration.
- **GitHub Actions**: Used for continuous integration and continuous deployment (CI/CD) to automate the build, test, and deployment processes for the backend services.
- **Docker**: The backend services are containerized using Docker to ensure consistency and portability across different environments.
- **Azure Virtual Machine**: The backend services are deployed on Azure Virtual Machines using Docker containers.

<div style="background-color: #fff; width: 100%; border-radius:1rem">
    <img src="https://mermaid.ink/img/pako:eNqVlF1r2zAUhv-KUG82SOKxXJR5MEjsZBusMNqym6QXinQci8hS0EeyLs5_77HlQJy1bDEYxPH7nI-XYx0oNwJoSgtl9rxk1pPHfKkJPpPFV-kTfL-F1RMZDr_UDyZYDiRDgtwxzdZQgfY1mb6LKjLhXhrt3scE0xbKvidZTn7KLSipoSbZITd8A_YYRVkrmgapBCbWnqHI1iRfTP4EC-SXtD4wheV4iV-ezqH7oMkjOO9qMls0B3IPLijvOtWsVc0BxIrxTU0mMZy34Ry2yjzXZL74IXdAZnonrdHNPEhHIVeSb8iElBYKsqSl91uXJsla-jKsRtxUS3ounL4tTApgHsdxCYsO9cnsktzv9yPRuvR3mfxSzBqjRpXk1jhT-LYe6GFwiQO7kxyr7qKLwyq66JJ-ytllSqztRmftg3698fn_99KAJ5Q5lyOGBUghlUpvig_FwHlrNpDejMfj7jzcS-HL9OP29-cLsmvmRH-6jo7OdvBqdWXpdi0jK8R1rG-W9dS0uL2KVc2WRvT232XPYFxgNPo8HW5qZ2AvmnXG9IJ5HLgXm8VBerF52yCG6IBWYCsmBV4qh0aypL7Ei2JJUzwKKBj-os02HFHKgjcPz5rT1NsAAxq2gnnIJVtbVtG0YMphFIT0xt7Fi6q9r44vcRKTXg?type=png" width="100%" />
</div>

<!-- ### 6. Talk To Listen LLM
- Other from GPT, and Google Gemini, some characters are generated by Talk To Listen LLM.
- Talk To Listen LLM is fine-tuned on the Talk To Listen dataset. The model is based on the Zephyr-7B and is optimized for generating human-like responses in a conversational setting and can adapt to different characters' personalities.
- Model fine-tuning: [GitHub Repository](https://github.com/Talktolisten/talktolisten-ttl-LLM-dev)
- Model deployment: [GitHub Repository](https://github.com/Talktolisten/talktolisten-LLM-prod) -->

### 6. Third-party APIs
- Voice Live Streaming: [Deepgram](https://www.deepgram.com/)
- Text To Speech: [EleventLabs](https://elevenlabs.io), [Azure Text To Speech](https://azure.microsoft.com/en-us/products/ai-services/ai-speech)
- Image generation: [Azure OpenAI service - Dall-e 3](https://azure.microsoft.com/en-us/products/ai-services/openai-service)

## Upcoming Features
- **Voice cloning Support**: I'm testing an open-source voice cloning model to allow users to clone their voice and use it in the app. This will make the conversations more personal and engaging.
- **Lock Screen Support**: I'm working on adding lock screen support, which will allow users to interact with the app even when their screen is locked. This feature will enhance the app's usability on the go, save battery life, and provide convenience for users who use earphones.
<!-- - **Tuning Gemini Pro**: I'm working on tuning the Gemini Pro model to let the characters talk more naturally and life-like. -->

## Developer
- Hieu "Leo" Nguyen. 
- [Website](https://www.mywebleo.com) and [GitHub](https://github.com/hieuminh65)
- The code is only for showcasing purposes and under the Apache 2.0 License.
