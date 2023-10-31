#数据与数据标注文件
将标注好的图片数据(jpg)与其对应的标注文件(xml)分别放在
PaddleDetection-release-2.6\dataset\layout_detection目录下的两个文件夹内
注意默认的标注文件夹名称为ANNOTATION，图片文件夹名称为JPG

# 划分数据集
将getlist.py与createlist.py 放在PaddleDetection-release-2.6\dataset\layout_detection目录下,并依次执行即可

#训练数据
在./PaddleDetection-release-2.6目录下进入终端执行：
python tools/train.py -c configs/yolov3/layout_detection.yml --eval -o use_gpu=true

#预测数据
继续在当前目录下执行，预测图片放在PaddleDetection-release-2.6/test2023/文件夹下
python tools/infer.py -c configs/yolov3/layout_detection.yml -o use_gpu=true --infer_dir=test2023 --save_results=true
