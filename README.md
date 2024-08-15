### **Amazon-Bedrock-Translation-POC**

**Product Description:**

The **Amazon-Bedrock-Translation-POC** is a sample code repository designed to showcase the use of Amazon Bedrock and Generative AI for translating text from one language to another. This proof of concept (POC) provides a simple and user-friendly frontend interface that allows users to perform translations efficiently. The repository includes three distinct interfaces—Text, Chat, and File—each catering to different translation needs. With minimal setup, users can leverage the powerful language models provided by Amazon Bedrock to translate text, analyze the translation's accuracy, and display the results through an intuitive web application.

---

### **Step-by-Step Guide:**

#### **Prerequisites:**

1. **Amazon Bedrock Access:** Ensure that you have access to Amazon Bedrock and have configured the necessary credentials using the AWS CLI.
2. **Python 3.10:** Install Python 3.10 on your machine, as this is the most stable version for the required packages. You can download it [here](https://www.python.org/downloads/release/python-3100/).

---

#### **Step 1: Clone the Repository**

1. Open your terminal and clone the repository using the following command:

   ```bash
   git clone https://github.com/aws-samples/genai-quickstart-pocs.git
   ```

2. After cloning the repository, open it in your preferred code editor. The repository contains the following key files:
   - **Text.py:** The frontend application for translating text.
   - **Chat.py:** The frontend application for translating chat conversations.
   - **File.py:** The frontend application for translating uploaded text files.
   - **amazon_bedrock_translation.py:** Contains methods for interacting with Amazon Bedrock.
   - **requirements.txt:** Lists all the necessary packages for running the application.

---

#### **Step 2: Set Up a Python Virtual Environment**

1. Navigate to the root directory of the cloned repository and set up a Python virtual environment:

   ```bash
   pip install virtualenv
   python3.10 -m venv venv
   ```

2. Activate the virtual environment:

   ```bash
   source venv/bin/activate
   ```

3. Install the required packages listed in the `requirements.txt` file:

   ```bash
   pip install -r requirements.txt
   ```

---

#### **Step 3: Configure Environment Variables**

1. Create a `.env` file in the root directory of the repository.
2. Add your AWS CLI profile name to the `.env` file:

   ```bash
   profile_name=<AWS_CLI_PROFILE_NAME>
   ```

3. If necessary, update the region and endpoint in the `prompt_finder_and_invoke_llm.py` file based on your Amazon Bedrock configuration:

   ```python
   bedrock = boto3.client('bedrock-runtime', 'us-east-1', endpoint_url='https://bedrock-runtime.us-east-1.amazonaws.com')
   ```

4. Customize the translation model by modifying the `amazon_bedrock_translation.py` file. The `llm_answer_generator` function can be adjusted to use different models by changing the `modelId` variable.

---

#### **Step 4: Run the Application**

1. After completing the setup, start the application by running the following command in your terminal:

   ```bash
   streamlit run Text.py
   ```

2. The application will launch in your default web browser, where you can begin translating text, chat conversations, or files.

