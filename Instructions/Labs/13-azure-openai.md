# Module 13: Explore Azure OpenAI Service

## Lab overview

In this exercise, you'll explore Azure OpenAI Service and use it to deploy and experiment with generative AI models.
Azure OpenAI Service brings the generative AI models developed by OpenAI to the Azure platform, enabling you to develop powerful AI solutions that benefit from the security, scalability, and integration of services provided by the Azure cloud platform.

## Lab objectives

In this lab, you will perform:
- Provision an Azure OpenAI resource
- Deploy and Interact with Language Generation Model
- Explore Image Generation with DALL-E
- Use the *Chat* playground to work with the model
- Use the *DALL-E* playground to generate images

## Estimated timing: 45 minutes

## Exercise 1: Explore Azure OpenAI Service

### Task 1: Provision an Azure OpenAI resource

1. In another browser tab, open the Azure portal at [https://portal.azure.com](https://portal.azure.com?azure-portal=true)

    - **Email/Username:** <inject key="AzureAdUserEmail"></inject>
    
    - **Password:** <inject key="AzureAdUserPassword"></inject>
    
1. Select **Yes** when asked for **Stay signed in**

1. Search for **Azure OpenAI** and click on **Create** resource with the following settings:

    - **Subscription**: Select your **existing azure subscription**.
    - **Resource group**: Select **ODL-AI-900-13-<inject key="DeploymentID" enableCopy="false" />-02**
    - **Region**: Select **<inject key="location" enableCopy="false"/>** 
    - **Name**: **openai<inject key="DeploymentID" enableCopy="false" />**
    - **Pricing tier**: Standard S0

2. Click **Next** twice and click on **Review and Create**. Click on **Create**.

3. Wait for deployment to complete. Then go to the deployed Azure OpenAI resource in the Azure portal.

### Task 2: Explore Azure OpenAI Studio

You can deploy, manage, and explore models in your Azure OpenAI Service by using Azure OpenAI Studio.

1. On the **Overview** page for your Azure OpenAI resource, click on the **Go to Azure OpenAI Studio** button to open Azure OpenAI Studio in a new browser tab. Alternatively, navigate to [Azure OpenAI Studio](https://oai.azure.com/) directly.

    When you first open Azure OpenAI Studio, it should look similar to this:

    ![Screenshot of Azure OpenAI Studio.](./media/generative-ai/ai-studio.png)

1. View the pages available in the pane on the left. You can always return to the home page at the top. Additionally, OpenAI Studio provides multiple pages where you can:
    - Experiment with models in a *playground*.
    - Manage model deployments and data.

### Task 3: Deploy a model for language generation

To experiment with natural language generation, you must first deploy a model.

1. On the **Models** page view the available models in your Azure OpenAI service instance.
1. Select any of the **gpt-35-turbo** models for which the **Deployable** status is **Yes**, and then select **Deploy**:

    ![Screenshot of the Models page in Azure AI Studio.](./media/generative-ai/deploy-model.png)

1. Create a new deployment with the following settings:
    - **Model**: gpt-35-turbo
    - **Model version**: Auto-update to default
    - **Deployment name**: **model<inject key="DeploymentID" enableCopy="false" />**

### Task 4: Use the *Chat* playground to work with the model

Now that you have deployed a model, you can use it in the *Chat* playground to generate natural language output from prompts that you submit in a chat interface.

1. In [Azure OpenAI Studio](https://oai.azure.com/), navigate to the **Chat** playground in the left pane.

    The *Chat* playground provides a chatbot interface with which you can interact with your deployed model, as shown here:

    ![Screenshot of the Chat playground in Azure OpenAI Studio.](./media/generative-ai/chat-playground.png)

1. In the **Configuration** pane, ensure that your model deployment is selected.
1. In the **Assistant setup** pane, select the **Default** system message template, and view the system message this template creates. The system message defines how the model will behave in your chat session. Click on **Save changes** on the top.
1. In the **Chat session** section, enter the following user message.

    ```
   What is generative AI?
    ```

1. Observe the output returned by the model, which should provide a definition of generative AI.
1. Enter the following user message as a follow-up question:

    ```
   What are three benefits it provides?
    ```

1. Review the output, noting that the chat session has kept track of the previous input and response to provide context (so it correctly interprets "it" as referring to "generative AI") and that it provides a suitable response based on what was requested (it should return three benefits of generative AI).

### Task 5: Use the *DALL-E* playground to generate images

In addition to language generation models, Azure OpenAI Service supports the DALL-E 2 model for image generation.

> **Note**: You must have applied for and received access to DALL-E functionality in your Azure OpenAI service access application to complete this section of the exercise.

1. In [Azure OpenAI Studio](https://oai.azure.com/), navigate to the **DALL-E** playground in the left pane.
1. Enter the following prompt:

    ```
    A robot eating spaghetti
    ```

1. Select **Generate** and view the results, which should consist of an image based on the description you provided in the prompt, similar to this:

    ![Screenshot of the DALL-E playgrund in Azure OpenAI Studio.](./media/generative-ai/dall-e-playground.png)

1. Generate a second image by modifying the prompt to:

    ```
    A robot eating spaghetti in the style of Rembrandt
    ```
1. Verify that the new image matches the requirements of the prompt, similar to this:

    ![Screenshot of DALL-E generated images in Azure OpenAI Studio.](./media/generative-ai/dall-e-results.png)

### Review

In this lab, you have completed:
- Provisioned an Azure OpenAI resource
- Deployed and Interact with Language Generation Model
- Explored Image Generation with DALL-E
- Used the *Chat* playground to work with the model
- Used the *DALL-E* playground to generate images

## You have successfully completed this lab.
