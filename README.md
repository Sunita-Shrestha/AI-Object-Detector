# Rock–Paper–Scissor
## Image Classifier (Teachable Machine)

This project uses **Google Teachable Machine** to classify webcam images into four categories:

- **background**
- **rock**
- **paper**
- **scissor**

View the trained model here:  
👉 https://teachablemachine.withgoogle.com/models/gMDmFqKFo/

---

## 🧠 Why Is This “Supervised Learning”?

This is an example of **supervised learning** because:

- You manually provided **labeled training data** for each class.
- The model learned to associate images with the correct **labels** you assigned.
- During training, the algorithm compares its predictions to the correct labels and adjusts itself to improve accuracy.

**In short:**  
> It is supervised learning because the model learns from examples that *I* labeled.

---

## 🧪 Edge Cases

### ❓ What happens if you hold two objects at once?

If two objects (e.g., papper + scissor) appear in the camera at the same time:

- The model becomes **confused**, because it was only trained with **one object per image**.
- It will still try to choose **one single class**, even if the input doesn’t match perfectly.
- It usually picks:
  - the object that covers more of the image, **or**
  - the one that more closely resembles its training examples.

**In short:**  
> The model guesses the closest match because it does not understand multi‑object images.

---
The model predicts probabilities for each class.

Example output:
<img width="377" height="803" alt="paper-scissor" src="https://github.com/user-attachments/assets/e64b41b5-4d11-4cbc-95cd-53bfcbd68d55" />
<img width="372" height="806" alt="scissors" src="https://github.com/user-attachments/assets/afc055e0-f7db-40ee-b451-00235e8eba4e" />
<img width="370" height="807" alt="rock" src="https://github.com/user-attachments/assets/fb0a1066-f6c3-4319-aea5-7bf620c1f85e" />
<img width="393" height="795" alt="papper" src="https://github.com/user-attachments/assets/0afda9db-950f-4256-87f8-d4b02e2874e0" />
