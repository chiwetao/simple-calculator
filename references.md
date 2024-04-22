# Using Generative AI
Here are the prompts and responses I got using AI (Google's Gemini and OpenAI's ChatGPT) while working on HW4.

## Prompt 1: Asking for help with Part II (Sketching)
**Prompt:** hi! i'm trying to make a simple calculator app. can you give me an example of a sketch for this?

**AI Response:** Sure! Here's a simple sketch for a calculator app:

![AI_Sketch1](/ai_responses/ai_sketch.png)

In this sketch:

- The "Display" is where the numbers and results will be shown.
- The buttons [0-9] represent digits.
- The buttons [÷], [×], [-], and [+] represent mathematical operations: division, multiplication, subtraction, and addition respectively.
- The [.] button represents the decimal point.
- The [=] button is for calculating the result.
- You can customize this design further based on your preferences and platform requirements. This is just a basic example to get you started.

____
**My Response Prompt:** great work! i think i want the clear,  %, / and x button under the display. i also want the -, + and = button going down the side, then all the numbers in the middle. also add a button for two zeros '00' beside the zero button.

**AI Response:** Sure, here's an updated sketch based on your requirements:

![AI_Sketch2](/ai_responses/ai_sketch2.png)

In this updated sketch:

- The [C] button is for clearing the display.
- The [%] button represents percentage functionality.
- The [÷] and [×] buttons are for division and multiplication respectively.
- The [+] and [-] buttons are for addition and subtraction respectively.
- The [=] button is for calculating the result.
- The [00] button represents a double zero option.
- All numbers [0-9] and the decimal point [.] are centered.
Feel free to adjust the layout further to suit your preferences!

## Prompt 2: Asking for help to make my buttons fill their columns
**Prompt:** hi again! so i've coded up the basic format for my calculator, but all my buttons are small. i want them to fill their columns.
this is a little snippet of my code to help:

![Code_Snippet](/ai_responses/code_snippet.png)


**AI Response:** To make your buttons fill their respective columns in your calculator layout, you can utilize Bootstrap's grid system and flex utilities. Here's how you can modify your code:

![Code_Snippet](/ai_responses/ai_codehelp.png)

By adding the w-100 class to each button, you're making them fill the width of their parent column (BCol). This will cause each button to expand horizontally to fill its column.

## Prompt 3: Asking for help to make my Clear function
**Prompt:** hi i'm programming a calculator app. i want to write a function to clear my input. can you give me an example of how i would do that? (Note: i had to introduce the problem again because I accidentally closed my last session)

**AI Response:** Certainly! Here's an example of how you can write a function to clear the input in a calculator app using Python:

![Code_Snippet](/ai_responses/prompt3_response1.png)

This function clear_input takes a string input_text as input and returns an empty string, effectively clearing the input. You can call this function whenever you need to clear the input in your calculator app.

____
**My Response Prompt:** this is a good start but I actually want to write my code using Vue version 3.

**AI Response:** Sure! In Vue.js version 3, you can achieve this by using a data property to hold the input value and a method to clear it. Here's an example:

![Code_Snippet](/ai_responses/prompt3_response2.png)

In this example:

- We have an input field bound to the inputText data property using v-model.
- We have a button that triggers the clearInput method when clicked.
- The clearInput method simply sets the inputText to an empty string, effectively clearing the input.
- You can integrate this code into your Vue.js version 3 project for clearing the input in your calculator app.


# Reflection
I used generative AI to help with troubleshooting the size of my buttons and then for clues on how to make my clear function and also to sketch my initial design. I found it to be very helpful and I did't have to prompt it many times to get a sufficient answer. I think this is because in my prompts (especially prompt 1 & 2), I gave specific instructions and also gave a piece/snippet of my code so it could understand what programming language and version I was hoping for it to help me with. For prompt 3, if i had just copied and pasted that code, it definitely would not have worked, but it did give me an example of how I would implement it, which i could adapt to my work!
