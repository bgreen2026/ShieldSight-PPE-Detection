Entry 1

Date: July 2, 2026
Tool: ChatGPT

Question/Problem:
I needed help choosing a project topic and dataset that would satisfy the project requirements while still being manageable within the project timeline.

What AI Suggested:
ChatGPT helped me explore the idea of creating a PPE detection system using YOLO11 and discussed using a construction safety dataset. It also suggested focusing on a smaller number of classes that were directly related to the purpose of the project.

What I Learned:
I learned that narrowing the scope of a computer vision project can make the project more manageable while still solving a meaningful problem.

How I Applied It:
I selected PPE detection as my project and used the Construction Site Safety dataset as the basis for developing ShieldSight.

Entry 2

Date: July 10, 2026
Tool: ChatGPT

Question/Problem:
I wasn't sure how to verify the class names or whether they needed to match the order in the dataset.

What AI Suggested:
ChatGPT explained how to compare the dataset class names with the YAML configuration file and verify the class order before training.

What I Learned:
I learned that YOLO uses class indexes in the label files, so the class names and indexes need to match correctly. A model could still train even if the configuration was wrong, but the resulting labels could be incorrect.

How I Applied It:
I checked the class names and configuration before moving forward with model training.

Entry 3

Date: July 18, 2026
Tool: ChatGPT

Question/Problem:
I wasn't sure whether I should continue using all ten classes in the original dataset or create a filtered dataset containing only the classes needed for ShieldSight.

What AI Suggested:
ChatGPT explained the advantages of narrowing the dataset to the classes directly related to the project: Person, Hardhat, NO-Hardhat, Safety Vest, and NO-Safety Vest.

What I Learned:
I learned that limiting the dataset to the classes needed for the project could make the model and results easier to evaluate and keep the project focused on its intended purpose.

How I Applied It:
I created a five-class version of the dataset and used it for my final model.

Entry 4

Date: July 20, 2026
Tool: ChatGPT

Question/Problem:
Training on the CPU was taking several hours, and I wasn't sure whether changing the Colab runtime would help.

What AI Suggested:
ChatGPT explained the difference between CPU and GPU training and recommended using the T4 GPU available in Google Colab for the YOLO training process.

What I Learned:
I learned that GPU acceleration is useful for deep learning because it can perform many of the calculations required during training more efficiently.

How I Applied It:
I changed the Colab runtime to a T4 GPU, which made the training process much more practical.

Entry 5

Date: July 21, 2026
Tool: ChatGPT

Question/Problem:
I wasn't sure whether I should use my short training run as the final model or continue with a longer training run.

What AI Suggested:
ChatGPT suggested using the shorter run to confirm that the dataset and training process worked correctly before completing the longer final training run.

What I Learned:
I learned that a short training run can be useful for testing the pipeline before spending more time and resources on final training.

How I Applied It:
I used the shorter run as a test and then completed the longer training run with my five-class dataset for the final model.

Entry 6

Date: July 22, 2026
Tool: ChatGPT

Question/Problem:
I needed help understanding the validation metrics produced by my final model.

What AI Suggested:
ChatGPT explained Precision, Recall, mAP50, and mAP50-95 and helped me understand what each metric showed about the model's performance.

What I Learned:
I learned that the metrics measure different parts of object detection performance. Precision shows how often the model's detections are correct, while Recall shows how many actual objects the model successfully finds. mAP provides a broader measurement of detection performance.

How I Applied It:
I used the validation metrics to evaluate ShieldSight and report the final results: Precision 0.888, Recall 0.705, mAP50 0.788, and mAP50-95 0.473.

Entry 7

Date: July 28, 2026
Tool: ChatGPT

Question/Problem:
I needed to determine how to identify and explain meaningful failure cases instead of only showing successful predictions.

What AI Suggested:
ChatGPT suggested testing the model on different types of construction images and comparing the visible PPE with the model's detections. It also helped me connect individual failures to the validation results.

What I Learned:
I learned that failure analysis is important because overall performance metrics do not show exactly where a model struggles. One of my test images contained a worker without a hardhat, but ShieldSight detected the person without identifying NO-Hardhat. This was consistent with NO-Hardhat having the lowest recall in my class-level validation results.

How I Applied It:
I kept the missing-hardhat prediction as a failure case instead of removing it. I plan to use it to explain one of ShieldSight's limitations and how the model could be improved.


Entry 8

Date: July 29, 2026
Tool: ChatGPT

Question/Problem:
I needed help reviewing and organizing my AI Usage Log to make sure it accurately reflected how I used AI throughout the ShieldSight project and met the final project requirements.

What AI Suggested:
ChatGPT helped me organize the log into clear entries that included the problem I was working on, the guidance AI provided, what I learned from the guidance, and how I applied it to my project. It also helped me identify important parts of the development process that should be included, such as dataset preparation, training, model evaluation, failure analysis, and building the final demo.

What I Learned:
I learned that documenting AI use should explain more than just what questions I asked. The log should also show what I learned from using AI and how I used that information while completing the project.

How I Applied It:
I reviewed my previous AI interactions, organized them by the different stages of the project, and created a final AI Usage Log that shows how AI supported my learning and development of ShieldSight.
