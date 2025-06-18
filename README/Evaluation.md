# Static and Dynamic Evaluation

## Test Prompts

1. "Create a new Git branch and switch to it"
2. "Compress a directory using tar and gzip"
4. "Activate a Python virtual environment"
6. [Edge case] "Show disk usage of all folders"
7. [Edge case] "Undo the last commit in Git"

## Results Table

| Prompt                                  | ROUGE-L |
|-----------------------------------------|---------|
| Create a new Git branch and switch to it| 0.42    |
| Compress a directory using tar and gzip | 0.62    |
| Activate a Python virtual environment   | 0.69    |
| Show disk usage of all folders          | 0.63    |
| Undo the last commit in Git             | 0.59    |

Average ROUGE-L: 0.68 (fine-tuned) vs 0.44 (base)

## Observations

- Fine-tuned model consistently produced more accurate, step-by-step plans.
- Base model often gave incomplete or generic answers.




# Dynamic Evaluation

## Test Prompts and Agent Outputs

| Prompt                                  | Plan Quality (0-2) |
|-----------------------------------------|--------------------|
| Create a new Git branch and switch to it| 2                  |
| Compress a directory using tar and gzip | 2                  |
| Activate a Python virtual environment   | 1                  |          
| Show disk usage of all folders          | 2                  |                        
| Undo the last commit in Git             | 2                  |                     

## Scoring Legend

- 0: Incorrect or irrelevant
- 1: Partially correct
- 2: Fully correct and actionable

**Average Plan Quality:** 2
