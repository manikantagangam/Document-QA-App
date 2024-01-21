# Document-QA-App

Document-QA-App is a Streamlit web application that allows users to explore and ask questions about the content of PDF documents. The system utilizes natural language processing techniques, including text splitting, embeddings, and a question-answering model powered by OpenAI's language model.

## How to Run

1. **Download Repository:**

   - Clone or download the repository to your local machine.

2. **Set Up Environment:**

   - Open a terminal and navigate to the project directory.
   - Install the required dependencies by running the following command:
     ```bash
     pip install -r requirements.txt
     ```

3. **Generate OpenAI API Key:**

   - Obtain an API key from the [OpenAI website](https://platform.openai.com/api-keys).

4. **Create .env File:**

   - Create a new file named `.env` in the project directory.
   - Use the provided `.env.example` as a template and add your OpenAI API key to the `.env` file.

5. **Run the Application:**

   - Execute the following command to run the Streamlit app:
     ```bash
     streamlit run app.py
     ```

6. **Explore and Ask Questions:**
   - Open a browser and navigate to the provided local address (usually http://localhost:8501).
   - Upload a PDF document and ask questions based on its content.

## How it Works

- The application reads the PDF and splits the text into smaller chunks suitable for feeding into a Language Model (LLM).
- OpenAI embeddings are used to create vector representations of the text chunks.
- The application identifies chunks that are semantically similar to the user's question and provides those chunks to the LLM for response generation.
- Streamlit is employed to create the graphical user interface, and Langchain is used to interact with the Language Model.

## Project Structure

- `app.py`: Main script containing the Streamlit application.
- `requirements.txt`: File specifying the required Python dependencies.
- `.env`: Configuration file for storing sensitive information such as API keys.
- `.env.example`: Example template for the `.env` file.
