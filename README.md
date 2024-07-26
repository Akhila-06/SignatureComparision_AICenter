# SignatureComparision_AICenter

For the Signature Comparison project using UiPath AI Center, we're utilizing an already trained machine learning model to determine if two signatures are from the same person. Here's a step-by-step guide:

**Project Setup**
**Create a Project in AI Center:**
    -Navigate to UiPath Orchestrator -> Admin -> AI Center.
    -Create a new project named "SignatureComparison".
**Create an ML Package:**
    -Go to ML Packages in the AI Center.
    -Select Out of the box Packages.
    -Choose UiPath Image Analysis -> SignatureComparison.
**Create an ML Skill:**
    -Deploy the ML Package by creating an ML Skill.
    -Testing and Deployment
**Test the ML Model in UiPath Studio:**
    -Open UiPath Studio and install the ML Services package via the "Manage Packages" option.
    -Use the MLSkill activity to test the model.
**Create a Workflow:**
    -Create a workflow that takes two input images (one original and one potentially forged signature).
    -Use the MLSkill activity to compare the signatures.
The output will be in the following format:
json
Copy code
{
  "is_same_author": true,
  "similarity": 1.0
}
The is_same_author field indicates whether the signatures are from the same person, and the similarity score represents the confidence level of the comparison.
This process allows to use UiPath's AI Center to verify the authenticity of signatures without needing to train the model, as it's pre-trained
