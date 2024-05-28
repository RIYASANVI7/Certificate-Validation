# Certificate-Generation and validation using blockchain technology
This repository is a team-based project which presents the development of a Blockchain-based Educational Certificate Verification decentralized application (DApp) aimed at enhancing the security, transparency, and efficiency of certificate verification processes. Traditional methods of certificate issuance and verification are often slow, insecure, and prone to fraud. In response,
this project explores the potential of blockchain technology to address these challenges.
The DApp streamlines certificate generation and validation by leveraging blockchain’s decentralized and tamper-proof nature. Through automation and transparency, the system
aims to reduce the risk of fraud and improve the reliability of certificate records. The
report outlines the system architecture, implementation details, and future directions
for research and development. Overall, the project represents a significant step towards
creating a more secure and efficient certificate verification ecosystem in the digital age.


Proposed Approach:
System Architecture:-
The system consists of two main entities: the Institute and the Verifier. 
• Institute: Responsible for generating and issuing certificates. The Institute has
the functionality to create certificates and store them securely on the blockchain.
Additionally, a digital PDF copy of each certificate is stored on IPFS to ensure easy
access and retrieval.
• Verifier: Responsible for verifying the authenticity of certificates. The Verifier
can upload a certificate PDF or input the certificate ID to validate its authenticity
against the blockchain records.


Technology Stack:
The proposed system utilizes the following technologies:
• Ganache-CLI: A local blockchain network for development and testing. GanacheCLI simulates the Ethereum blockchain, allowing for efficient testing of smart contracts in a controlled environment.
• Truffle: A development framework for Ethereum that facilitates the development,
testing, and deployment of smart contracts.
• Streamlit: A framework for building the front-end of the DApp. Streamlit is used
to create an interactive and user-friendly web interface for both the Institute and
the Verifier.
• Pinata: An IPFS client used for decentralized storage of certificate PDFs. Pinata
ensures that the certificates are accessible and tamper-proof.


 System Workflow:
The workflow of the proposed certificate verification system is as follows:
Certificate Issuance (Institute)
1. **Certificate Creation:**
• The Institute generates a certificate with relevant details such as the recipient’s
name, course details, date of issuance, and unique certificate ID.
• The certificate details are then hashed and stored on the Ethereum blockchain to
ensure immutability.
2. Storing the Certificate:
• A digital PDF copy of the certificate is created and uploaded to IPFS via Pinata.
• The IPFS hash of the certificate PDF is stored on the blockchain, linking the digital
document to the blockchain record.
3. Viewing Certificates:
• The Institute can view all issued certificates through the web interface, providing
transparency and easy access to certificate records.
Certificate Verification (Verifier)
1. Verification Request:
• The Verifier can either upload the certificate PDF or input the unique certificate
ID through the web interface.
2. Blockchain Validation:
• The system retrieves the stored hash and IPFS link from the blockchain based on
the provided certificate ID.
• If a certificate PDF is uploaded, its hash is compared to the hash stored on the
blockchain.
• If the hashes match, the certificate is considered authentic. If not, the certificate is
flagged as potentially fraudulent.
3. Result Display:
• The verification result, along with the details of the certificate, is displayed to the
Verifier through the web interface.


Implementation:
To install Truffle and Ganache-CLI globally, execute the following command in the
terminal:
npm install -g truffle ganache-cli

Project Initialization
To initialize the project directory as a Truffle project, follow these steps:
1. Create a new directory named CertificateValidationSystem.
2. Open the directory in the terminal/command prompt.
3. Run the following command to initialize the project:
truffle init
This command will create the necessary project structure with directories for contracts, migrations, and tests.

The frontend of the DApp is developed using Streamlit, a Python library for building
interactive web applications. Streamlit provides a simple and intuitive interface for users
to interact with the DApp.
The frontend interface includes the following functionalities:
• Certificate Generation Form: Allows the Institute to input certificate details
and generate new certificates.
• Certificate Verification Form: Enables the Verifier to verify the authenticity of
certificates by entering the certificate ID or uploading a certificate PDF.

Once deployed, the DApp is accessible through a web browser, allowing users to
generate and verify certificates securely.
Comprehensive testing is essential to ensure the functionality, reliability, and security
of the Certificate Validation DApp. Testing includes unit tests for smart contracts, integration tests for frontend-backend interactions, and end-to-end tests for the complete
DApp workflow.
The testing process involves:
1.To run it, first open a terminal and enter the command:
ganache-cli -h 127.0.0.1 -p 8545
2.Next, to deploy our contracts on ganache-cli, open command prompt in our project’s
root directory and enter the following command:
truffle migrate
3.Now, to finally start the streamlit app, open the application directory inside our project
in command prompt and enter the command:
streamlit run app.py
• Writing test cases to cover all functionalities and edge cases.
• Executing tests using Truffle for smart contracts and automated testing frameworks
for frontend and backend components.
• Analyzing test results and debugging any issues encountered.
By conducting thorough testing, any potential bugs or vulnerabilities can be identified
and addressed before deploying the DApp to production.
