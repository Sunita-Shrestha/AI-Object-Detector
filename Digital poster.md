# Rock–Paper–Scissors Classifier (Handling Two Objects)

This project uses **Google Teachable Machine** to classify webcam images into four classes:

- **Background**
- **Rock**
- **Paper**
- **Scissors**

Model link:  
👉 https://teachablemachine.withgoogle.com/models/gMDmFqKFo/

---

##  Why This Is Supervised Learning

This is a **supervised learning** project because:

- I manually provided labeled images for each class.
- The model learns by mapping input images to the labels I defined.
- Training involves comparing predictions with the correct labels and adjusting the model to reduce errors.

**In summary:**  
> It is supervised learning because the model is trained on examples with human‑assigned labels.

---

## 🧪 What Happens When I Hold Two Objects at Once?

Teachable Machine models are **single‑label classifiers**.  
This means:

- They always choose **one** class as the final prediction.
- They were trained with **only one object per image**, so showing multiple objects creates confusion.

### Example Behavior

When showing **two gestures at the same time** (for example, a scissors sign and a paper hand shape), the model output may look like this:

- **Scissors: 75%**  
- **Paper: 25%**  
- Other classes: low values

### Why This Happens

The model tries to interpret the entire image as **one category**, so it:

- Focuses on whichever gesture is **more visible**,  
- Takes up more of the frame,  
- Or looks most similar to the examples in the training set.

Because of this, the model guesses **one best match**, even though the input contains multiple gestures.

**In short:**  
> When I hold two objects at once, the model becomes uncertain but still chooses the gesture that appears strongest in the image.

---
The model predicts probabilities for each class.

Example output:

<img width="370" height="800" alt="rock" src="https://github.com/user-attachments/assets/09f49a77-ac89-4327-87a2-e079b1b2f201" />
<img width="370" height="800" alt="papper" src="https://github.com/user-attachments/assets/a4882b93-080b-4a59-bf17-7143e16db016" />
<br><br>
<img width="370" height="800" alt="paper-scissor" src="https://github.com/user-attachments/assets/41a2936e-67e5-44c5-8add-f49569659525" />
<img width="370" height="800" alt="scissors" src="https://github.com/user-attachments/assets/f5f52c7c-600d-4acf-902c-9800b3b43918" />

