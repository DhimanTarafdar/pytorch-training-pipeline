# PyTorch Training Pipeline 

এই নোটবুকে **Breast Cancer Detection**  এর জন্য PyTorch দিয়ে একটি সহজ Neural Network তৈরি করা হয়েছে — সম্পূর্ণ scratch থেকে, কোনো built-in layer ছাড়াই।

---

## ধাপসমূহ

### ১. ডেটা লোড ও প্রস্তুতি
- GitHub থেকে Breast Cancer dataset লোড করা হয়েছে
- অপ্রয়োজনীয় কলাম (`id`, `Unnamed: 32`) বাদ দেওয়া হয়েছে
- `train_test_split` দিয়ে ৮০% train, ২০% test ভাগ করা হয়েছে
- `StandardScaler` দিয়ে feature scaling করা হয়েছে
- `LabelEncoder` দিয়ে target label (M/B) কে 0/1 এ রূপান্তর করা হয়েছে

### ২. Tensor রূপান্তর
- NumPy array গুলোকে PyTorch Tensor এ convert করা হয়েছে

### ৩. মডেল তৈরি
- `MySimpleNN` নামে একটি custom class তৈরি করা হয়েছে
- **Sigmoid** activation function ব্যবহার করা হয়েছে
- **Binary Cross-Entropy** loss function manually implement করা হয়েছে

### ৪. Training
- Learning Rate: `0.1`
- Epochs: `25`
- Manual **Gradient Descent** দিয়ে weights ও bias আপডেট করা হয়েছে

### ৫. মূল্যায়ন (Evaluation)
- Test data তে prediction করে accuracy বের করা হয়েছে

---




| `Pandas` | ডেটা লোড ও প্রসেসিং |
| `NumPy` | Array অপারেশন |
| `Scikit-learn` | Scaling, Encoding, Train-test split |# pytorch-training-pipeline
