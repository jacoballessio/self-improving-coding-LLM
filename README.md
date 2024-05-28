# self-improving-coding-LLM
Coding LLM system that tests and iterates on code until it is successful, and then uses the successful code to further refine the model. 
This process should make outputs more accurate, but it may also lead to emergent properties (for example, a more accurate coding model might have better reasoning skills).

# Plan
The plan is to set up a code interpreter with a local LLM. For now we will use Code LLaMA-3-70b. 
The code interpreter should create a project folder and populate it with the necessary python files.
Then, it will generate tests and use some pre-defined tests to make sure the code works as intended.
It then runs these tests, evaluates output, and decides what modifications need to be made.
Once the tests all pass, the new code is considered complete. The completed code will be ran through a system that will modify the response to use to new code.
The chat context and new response will be stored in a file for fine-tuning the model.
Then we fine-tune the model on all the new data we have generated.
Repeat.

We can try running it on leetcode questions and have it improve at those types of problems. 
We should keep track of the performance of the original model, the output of the process, and the fine-tuned model.
For each problem we should do 5 attempts. Add a point for each successful attempt. Once all problems have been tried, our performance will be measured as n/m where n is the number of successful attempts and m is the total number of attempts.
The we can compare the results between the original model, the process output, and the fine-tuned model.
