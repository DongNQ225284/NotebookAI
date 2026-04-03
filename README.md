# NotebookAI

Repo này là bộ notebook học và thực hành về `Machine Learning` và `Deep Learning`, tập trung vào việc đi từ các thuật toán nền tảng đến các mô hình neural network và bài toán phân loại ảnh.

Hiện tại đây là repo theo hướng `learning notes + experiments`, không phải một ứng dụng hoàn chỉnh.

## Nội dung chính

- `machine_learning_basics/`: các notebook nền tảng như `KNN`, `Linear Regression`, `Naive Bayes`, `Gradient Descent`, `PLA`, `Logistic Regression`, `SVM`, kèm ghi chú toán học.
- `deep_learning_basics/`: các notebook giải thích và cài đặt ý tưởng `Linear Regression`, `Logistic Regression`, `Neural Network`.
- `keras_introduction/`: phần nhập môn deep learning với `Keras`, gồm `Neural Network` và `CNN`.
- `image_classification/`: các notebook về phân loại ảnh với `Decision Tree`, `KNN`, `Random Forest`, `SVM`, `VGG/ResNet`, `Zero-shot`.

## Lộ trình đọc gợi ý

Nếu bạn muốn đi từ dễ đến khó:

1. `machine_learning_basics/math_basic.md`
2. `machine_learning_basics/100.knn.ipynb`
3. `machine_learning_basics/200.linear_regression.ipynb`
4. `machine_learning_basics/501.gradient_descent.ipynb`
5. `machine_learning_basics/601.logistic_regression.ipynb`
6. `deep_learning_basics/300.neural_network.ipynb`
7. `keras_introduction/100.neural_network.ipynb`
8. `keras_introduction/200.cnn.ipynb`
9. `image_classification/200.vgg_resnet.ipynb`
10. `image_classification/300.zeroshot.ipynb`

## Notebook nên xem trước

Nếu chỉ xem nhanh để hiểu repo:

- `machine_learning_basics/501.gradient_descent.ipynb`: minh họa gradient descent.
- `deep_learning_basics/300.neural_network.ipynb`: phần neural network cơ bản.
- `keras_introduction/200.cnn.ipynb`: nhập môn CNN bằng Keras.
- `image_classification/200.vgg_resnet.ipynb`: giới thiệu VGG/ResNet cho bài toán ảnh.

## Công nghệ đang dùng

Repo hiện chủ yếu dựa trên notebook Python. Các thư viện được dùng hoặc nhiều khả năng cần có gồm:

- `numpy`
- `pandas`
- `matplotlib`
- `scikit-learn`
- `tensorflow`
- `keras`
- `torch`
- `Pillow`
- `clip`

## Cách chạy

1. Cài Python 3.10 hoặc phiên bản gần tương đương.
2. Tạo virtual environment.
3. Cài các thư viện cần thiết.
4. Mở notebook bằng `Jupyter Notebook` hoặc `JupyterLab`.

Ví dụ:

```bash
python -m venv .venv
.venv\Scripts\activate
pip install requirement.txt
```

## Mục tiêu repo

Mục tiêu của repo là:

- Ôn lại nền tảng toán và thuật toán machine learning,
- Hiểu cách hoạt động của các mô hình deep learning cơ bản,
- Thực hành nhanh trên notebook trước khi chuyển sang project có cấu trúc hơn.
