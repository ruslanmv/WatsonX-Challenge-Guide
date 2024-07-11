**WatsonX Challenge: Track 7 - InstructLab**
=====================================================

**Introduction**
---------------

Welcome to the WatsonX Challenge, Track 7 - InstructLab! In this challenge, we aim to increase the number of IBMers trained on InstructLab's capabilities to drive innovation across our portfolio and make our Granite model better by contributing new knowledge and skills from IBMers.

**Objective**
------------

The objective of this challenge is to modify existing or add new knowledge and skills to improve the accuracy of answers provided by Granite. To achieve this, you will suggest a use case for embedding the Granite model into your software or hardware product/solution, demonstrate its limitations, and then use InstructLab to modify and/or generate data towards improving the Granite model for your use case.

**Technical Requirements**
-------------------------

To participate in this challenge, you must meet the following technical requirements:

* Be a developer with the ability to:
	+ Install and operate the iLab CLI
	+ Use GitHub, e.g., open pull requests (PRs) to a GitHub repository
* Be part of a product team who wants to customize IBM Granite models to their use case
* Be a practitioner of gen AI and LLMs with some experience
* Have an Apple M1/M2/M3 MacBook with approximately 32 GB RAM
* Have a C++ compiler and Python 3.9+ (<3.12 for PyTorch JIT) installed
* Have approximately 60GB disk space available

**Challenge Steps**
-------------------

To complete this challenge, follow these steps:

1. **Suggest a use case**: Identify a use case for embedding the Granite model into your software or hardware product/solution.
2. **Demonstrate limitations**: Show that the Granite model is not initially helpful for solving the use case, but can be solved with another potentially larger model.
3. **Use InstructLab**: Modify and/or generate data towards improving the Granite model for your use case using InstructLab.


### The challenge
**What is your goal?**
For this track, your team of technical IBMers and developers will suggest a use case for embedding the Granite model into your software or hardware product/solution. An example use case might be creating a virtual assistant on your product to help onboard new users.

You will demonstrate that the Granite model is not initially helpful for solving the use case. Then you will use InstructLab to modify and/or generate data towards improving the Granite model for your use case.
We require challenge teams to generate synthetic data using the merlinite-7b-lab-gguf model, and to train and test a base student model and their trained model with either merlinite-7b-lab-gguf model or granite-7b-lab-gguf model.

### Challenge steps
1. **Suggest a use case**: Identify a use case for embedding the Granite model into your software or hardware product/solution.
2. **Demonstrate limitations**: Show that the Granite model is not initially helpful for solving the use case, but can be solved with another potentially larger model.
3. **Use InstructLab**: Modify and/or generate data towards improving the Granite model for your use case using InstructLab.
4. **Evaluation**: Evaluate the results using both the base student model and the trained model. 

### Resources
- **Tool access**: InstructLab guidance
- **Technical skills and hardware requirements**: Listed above
- **Learning resources**: Listed above
- **Data privacy**: Ensure compliance with IBM's data privacy and security guidelines

### Submission
Whether you're competing to win with a solution that could be scaled across the company or participating to improve your own productivity in a simple but meaningful way, every submission represents a way in which we are all using this transformative technology and collectively serves as an example for our clients and partners how generative AI is transforming business.​​​ Submit it all, no usage is too small!

**Submission Steps:**
1. **Deliverables folder (URL)**: Provide a folder containing your summary document and supplementary files showing your work (`initial_results.csv` and `instructlab_results.csv`). Ensure the link to the folder is accessible internally to all IBMers.
2. **Summary document**: Explain the importance of your use case for the specific IBM product – i.e., whether it is a new feature, or enhancing an existing feature, and summarize the work as requested in the detailed list below.

**Summary Document Must Include:**
- The link to your pull request in [IBM GitHub](https://github.ibm.com/instructlab-at-ibm/taxonomy-2024-watsonx-challenge).
- The name and description of the IBM product, the use case, and description of how the use case is relevant for the product.
- Describe the data (at least 25 examples), the metric used for evaluation (manual or automatically computed), and how the metric is relevant to the use case.
- The results with granite-13b-chat-v2 and llama-3-8b-instruct for the use case. This section should contain details about the prompt and all parameters used for the model (decoding strategy, temperature, top-p etc), and some discussion about what doesn't work with the IBM Granite model, but works with the other open-source model.
- Describe what you have tried in the taxonomy (steps 3-5), what the generated data looks like, and why it is or is not suitable.
- Summarize the evaluation results of the base student model and the trained model. Include a qualitative discussion of what worked well, or what didn’t.
- (Optional, for bonus points): Include a testimonial from your IBM product's product manager that the use case is important and has market value.

**Supplementary Files Requirements:**
- **initial_results.csv**:
  - `input_example`
  - `prompt_granite` (contains the instruction and input example, exactly as provided to the model)
  - `result_granite`
  - `result_granite_goodness`
  - `result_granite_commentary` (optional)
  - `prompt_llama` (contains the instruction and input example, exactly as provided to the model)
  - `result_llama`
  - `result_llama_goodness`
  - `result_llama_commentary` (optional)

- **instructlab_results.csv**:
  - `input_example`
  - `prompt_base_model` (contains the instruction and input example, exactly as provided to the model)
  - `result_base_model`
  - `result_base_model_goodness`
  - `result_base_model_commentary` (optional)
  - `prompt_trained_model` (contains the instruction and input example, exactly as provided to the model)
  - `result_trained_model`
  - `result_trained_model_goodness`
  - `result_trained_model_commentary` (optional)

- **Link to taxonomy pull request (URL)**: Provide the link to your taxonomy pull request in [IBM GitHub](https://github.ibm.com/instructlab-at-ibm/taxonomy-2024-watsonx-challenge). The pull request should be to the main branch.
- **Name of IBM product(s) that your work applies to (free text)**: Name of the IBM product(s) for which the use case/feature you chose is relevant.
- **Percentage of time saved (number)**: Share how much time can the customers of the IBM product save by utilizing the feature you propose (expressed as a percentage). Enter a value between 1 and

 100. 100% means that particular task can be fully automated using the feature you proposed.
- **Explain percentage of time saved (free text)**: Describe how you arrived at your "percentage of time saved" answer, with calculations clearly shown. For example, if a customer took 30 minutes to perform a given task, but the feature proposed would save 15 minutes, then the percentage of time saved is 50%.

**Note:** The selected submissions will have their model trained for testing and available for the submitting team to try out for one month following the challenge. Product teams who are happy with their taxonomy created during the challenge can take their taxonomy and submit it through the standard process to improve Granite vNext.


**Learning Resources**
---------------------

To help you prepare for this challenge, we recommend the following learning resources:

| Reference | Description | Link |
| --- | --- | --- |
| InstructLab Demo | Lowering the barrier to AI model development | [https://www.youtube.com/watch?v=pgK-70iLz_o](https://www.youtube.com/watch?v=pgK-70iLz_o) |
| The technology behind InstructLab | A low-cost way to customize LLMs | [https://research.ibm.com/blog/instruct-lab](https://research.ibm.com/blog/instruct-lab) |
| AI Assistants Level 1 learning course | Required learning course for the challenge | [TBD] |

**Important Notes**
------------------

* Participants must follow the data privacy and security guidelines outlined in Terms and Conditions Section 13 and continue to adhere to IBM Business Conduct Guidelines.
* This challenge is open to technical IBMers only.
* Team size is limited to up to 10 people.

By following these steps and guidelines, you'll be well on your way to completing the WatsonX Challenge, Track 7 - InstructLab. Good luck!
