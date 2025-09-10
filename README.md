# Exno.3-Scenario-Based Report Development Utilizing Diverse Prompting Techniques
### DATE: 10.09.2025                                                                    
### REGISTER NUMBER : 212223050013
## Aim: To design an AI-powered chatbot that assists customers in resolving issues related to product troubleshooting, order tracking, and general inquiries. The chatbot should handle various customer queries efficiently while maintaining a conversational and user-friendly tone. In this experiment, we will employ different prompt patterns to guide the development process of the chatbot, ranging from basic task-oriented prompts to more complex, persona-driven prompts.

## Algorithm:  1. Direct Instruction Prompts
Objective: Guide the chatbot to respond concisely to customer inquiries.
Prompt Pattern:
Prompt: "When a customer asks for the status of their order, reply with: 'Your order is currently being processed and will be delivered by [date].'"
2. Contextual Prompting
Objective: Incorporate specific context to provide detailed answers based on the user’s previous interaction.
Prompt Pattern:
Prompt: "If the customer previously mentioned that they haven’t received their order, say, 'I see that you mentioned your order hasn't arrived yet. Let me check the details for you and get back shortly.'"
3. Persona-Based Prompting
Objective: Design the chatbot to adopt a specific persona, making the interaction more engaging.
Prompt Pattern:
Prompt: "Pretend you are a friendly, helpful customer service representative. Use a conversational tone, such as 'Hey there! I’m here to help with any questions you might have. Let’s get your issue sorted!'"
4. Few-Shot Prompting
Objective: Teach the AI how to respond using a few examples, enabling it to generalize for similar situations.
Prompt Pattern:
Prompt: "Here are some examples of how to handle technical questions:
'My phone isn't charging.' → 'Have you tried using a different cable? If that doesn’t work, it may be an issue with the port.'
'The screen is flickering.' → 'It sounds like a display issue. Have you tried restarting the device?'
Now, respond to: 'My app keeps crashing.'"
5. Chain of Thought Prompting
Objective: Use a step-by-step reasoning approach for resolving more complex or technical issues.
Prompt Pattern:
Prompt: "When a customer reports their laptop overheating, guide them through the following steps:
Ask if they are using the laptop on a soft surface.
Suggest moving the laptop to a flat, hard surface for better airflow.
Ask if they’ve cleaned the vents recently.
Recommend restarting the device to see if the issue persists.
Now, solve: 'My laptop fan is making a loud noise.'"
6. Instruction with Constraints
Objective: Instruct the chatbot to provide assistance while adhering to specific constraints (e.g., response length or tone).
Prompt Pattern:
Prompt: "Respond to order inquiries in no more than 50 words and avoid using technical jargon. For example, 'Your order is on the way and should arrive by [date]. Feel free to reach out if you need anything else.'"
7. Reflective Prompting
Objective: Ensure that the chatbot reflects the user’s query back to them before providing a response, reducing misunderstandings.
Prompt Pattern:
Prompt: "When a customer asks for help, first reflect their question back to them. For example, if they ask 'How can I reset my password?' respond with 'You're asking how to reset your password, correct? Here’s how you can do it.'"

## OUTPUT 

### Introduction:

Modern businesses rely heavily on chatbots to improve customer experience. Unlike static FAQ pages, AI-powered chatbots can interpret natural language, respond conversationally, and adapt to the customer’s tone. However, the quality of chatbot responses depends heavily on prompt engineering techniques used during design.

In this experiment, we analyze four different types of prompt engineering:

1. Straightforward Prompts

2. Tabular Format Prompting

3. Missing Word Prompting

4. Preceding Question Prompting

Each technique is explained with examples from a customer support chatbot handling product troubleshooting, order tracking, and general inquiries.

## 1. Straightforward Prompts
### Explanation:

Straightforward prompts are the most basic yet essential type of prompting. They give the chatbot direct, clear instructions without additional structure. This makes them fast, easy to design, and highly suitable for handling simple, transactional queries.

Straightforward prompts leverage the model’s ability to interpret natural language and produce immediate responses. Customers typically phrase their requests directly, and the chatbot mirrors that style.

#### Examples:

a) Order Tracking

User Prompt: “Track my order number 12458.”

Chatbot Response: “Your order #12458 is currently in transit and will be delivered tomorrow.”

b) General Inquiry

User Prompt: “What are your customer care working hours?”

Chatbot Response: “Our customer care team is available from 9 AM to 9 PM, Monday to Saturday.”

c) Troubleshooting

User Prompt: “My laptop battery is draining too fast. What should I do?”

Chatbot Response: “Please reduce screen brightness, close unused apps, and check if a software update is available.”

#### Benefits:

1. Quick and efficient for short tasks

2. No extra design overhead

3. Natural for most users

#### Limitations:

Lacks structured presentation

May struggle with ambiguous queries

## 2. Tabular Format Prompting
### Explanation:

Tabular prompts organize chatbot responses into a row-column format, making information structured, scannable, and easy to follow. This is extremely useful when presenting step-by-step instructions, comparisons, or status updates.

By guiding the chatbot to produce tables, customer support becomes clearer and more professional, reducing confusion.

#### Examples:

a) Troubleshooting a Smart TV

User Prompt: “My Smart TV isn’t connecting to Wi-Fi. Show me the troubleshooting steps.”

Chatbot Response:

| Step | Action                               | Expected Outcome             |
| ---- | ------------------------------------ | ---------------------------- |
| 1    | Restart your Wi-Fi router            | Internet connection resets   |
| 2    | Go to Settings > Network on your TV  | Detect available networks    |
| 3    | Re-enter Wi-Fi password              | Device should connect        |
| 4    | Try another device on the same Wi-Fi | Confirms if issue is with TV |


b) Order Status Comparison

User Prompt: “Show me the status of my last 3 orders.”

Chatbot Response:

| Order No. | Status     | Delivery Date      |
| --------- | ---------- | ------------------ |
| #12458    | In Transit | Sept 12            |
| #12459    | Delivered  | Sept 5             |
| #12460    | Processing | Sept 15 (Expected) |

#### Benefits:

1. Highly structured & user-friendly

2. Reduces misunderstandings

3. Best for troubleshooting and tracking

#### Limitations:

Slightly longer prompt design

Not ideal for casual, conversational responses

## 3. Missing Word Prompting
### Explanation:

This technique involves filling in blanks or helping users complete partial sentences. Many customers type incomplete queries or vague instructions — the chatbot can intelligently infer and complete them.

Missing word prompting enhances interactivity and ensures the chatbot remains helpful even with incomplete inputs.

#### Examples:

a) Order Delay

User Prompt: “My delivery is ____”

Chatbot Response: “Do you mean your delivery is delayed? Let me check your tracking details.”

b) Troubleshooting Prompt

Prompt to User: “To restart your router, press the ____ button for 10 seconds.”

Chatbot Response: “To restart your router, press the reset button for 10 seconds.”

c) General Inquiry

User Prompt: “Customer support is available ____”

Chatbot Response: “Customer support is available Monday to Saturday, from 9 AM to 9 PM.”

#### Benefits:

1. Handles incomplete queries effectively

2. Encourages conversational flow

3. Good for interactive FAQs and tutorials

#### Limitations:

Risk of incorrect assumption

Requires well-trained context understanding

## 4. Preceding Question Prompting
### Explanation:

This technique ensures the chatbot uses previous context (a preceding question or statement) to generate meaningful answers. Unlike straightforward prompts, it does not treat each query in isolation.

This makes conversations more natural, personalized, and continuous, improving customer satisfaction.

#### Examples:

a) Troubleshooting Smartphone Issue

User: “My phone is heating up.”

Chatbot: “Are you using it while charging?”

User: “Yes.”

Chatbot Response: “Since you mentioned you’re charging while using it, the heating is normal. Please avoid heavy usage while charging.”

b) Order Tracking

User: “Where is my order?”

Chatbot: “Can you provide your order number?”

User: “It’s 12458.”

Chatbot Response: “Thanks! Order #12458 is currently in transit and will arrive tomorrow.”

c) General Inquiry

User: “Do you provide international shipping?”

Chatbot: “Yes, we do. Which country are you asking about?”

User: “Canada.”

Chatbot Response: “We deliver to Canada within 7–10 business days.”

#### Benefits:

1. Maintains context across conversation

2. Provides personalized answers

3. Enhances natural user experience

#### Limitations:

Needs memory handling capability

Risk of misunderstanding past context

## Comparison Table of Techniques

| Technique                    | Best Use Case                       | Example Strength            | Limitation                 |
| ---------------------------- | ----------------------------------- | --------------------------- | -------------------------- |
| Straightforward Prompts      | Quick tasks (order tracking, FAQs)  | Fast, simple responses      | Ambiguity not handled well |
| Tabular Format Prompting     | Troubleshooting, status comparisons | Clear, structured responses | Less conversational        |
| Missing Word Prompting       | Incomplete user queries             | Handles gaps smartly        | May misinterpret blanks    |
| Preceding Question Prompting | Conversational support              | Context-aware replies       | Needs context memory       |

## Conclusion

By applying different prompt engineering techniques, the chatbot becomes smarter and more user-friendly.

1. Straightforward prompts handle quick queries like order tracking.

2. Tabular prompts organize complex troubleshooting into clear steps.

3. Missing word prompts improve interactivity by handling incomplete queries.

4. Preceding question prompts make conversations contextual and natural.

Thus, the chatbot can provide efficient, accurate, and customer-friendly assistance, meeting the aim of this experiment.



# Result: Thus the Prompts were exected succcessfully .

