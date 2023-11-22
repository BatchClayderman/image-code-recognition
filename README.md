### 此项目为提供论文数据可用性而创建，转载自以下归属第二作者的链接：

1) [https://github.com/hengyi666/pytorch-code-recognition](https://github.com/hengyi666/pytorch-code-recognition)
2) [https://github.com/HengY1Cola/Jnu-Stuhealth/blob/main/handleValidate.py](https://github.com/HengY1Cola/Jnu-Stuhealth/blob/main/handleValidate.py)

# 基于CNN识别验证码(Pytorch)

##  前言

参考链接：[https://github.com/dee1024/pytorch-captcha-recognition](https://github.com/dee1024/pytorch-captcha-recognition)

VeriBypasser 系统：[https://github.com/BatchClayderman/VeriBypasser/tree/main](https://github.com/BatchClayderman/VeriBypasser/tree/main)

这个学期选了**人工智能**专业课(bushi🐶)!

这就是我们小组的**期末作业**了，既然要做，那就开源搞一个能用于**实战**的。

然后就**重构**了一下，以及弄了下**拓展**。

##  效果与原理

**训练集**: （使用常用的 Python 验证码生成库 ImageCaptcha）

```
Training set : 100k
Test set: 5k
```

------

> 准确率的话是数量越多越趋近最后的准确值(会存在偏差)

|      类型      | 准确率 |                             权重                             | 提取码 |
| :------------: | :----: | :----------------------------------------------------------: | :----: |
|  4位数字+大写  | 85.2%  | [下载链接]( https://pan.baidu.com/s/1IC7qvrJKrwygMT5r_hN8aA ) |  spdc  |
| 4位数字+大小写 | 72.38% | [下载链接](https://pan.baidu.com/s/1ubshKMdjuRSvc7405cON8w)  |  he0w  |

<img src="https://dailypic.hengyimonster.top/rate72.png" alt="image-20211211200828095" style="zoom:66%;" />

##  快速开始

- **步骤一：设置**

到setting.py下设置`CHOOSE_LIST`以及`MAX_CAPTCHA`

<img src="https://dailypic.hengyimonster.top/image-20211211201535432.png" alt="image-20211211201535432" style="zoom:30%;" />

- **步骤二：创建属于自己的训练集**

到setting.py下设置`count`以及`path`

可以选择的参数已经在注释中了。

> 这里建议：
>
> 训练集的数量10k+（推荐100K的训练集）
>
> 验证集的数量1k+

```bash
$ python makeImage.py 
```



<img src="https://dailypic.hengyimonster.top/image-20211211201749408.png" alt="image-20211211201749408" style="zoom:30%;" />

- **步骤三：训练模型**

生成的文件会存在`./result`中

```bash
$ python train.py
```

- **步骤四：测试模型**

```bash
$ python test.py
```

- **步骤五：模型做预测**

```bash
$ python predict.py
```

## 日志与展望

- 日志📝 
  - 2021-12-11:  代码基本成型。4位数字+大写字母的争取率稳定在85%左右
  - 2021-12-18:  4位数字+大小写字母模型经过一周训练最高73%左右
  - 2021-12-19：上传基本成型的仓库。
- 展望🦅

  - 准确率能够来到90以上。

##  联系方式

期待您的PR

以及不要脸的🙇‍♀️您的更加优秀的超参数。

我们是来自**暨南大学**某不知名小组～

**负责人**联系邮箱📮 2911567026@qq.com

***

### This project was created to provide paper data availability and is reproduced from the following link attributed to the second author:

1) [https://github.com/hengyi666/pytorch-code-recognition](https://github.com/hengyi666/pytorch-code-recognition)
2) [https://github.com/HengY1Cola/Jnu-Stuhealth/blob/main/handleValidate.py](https://github.com/HengY1Cola/Jnu-Stuhealth/blob/main/handleValidate.py)

# Image verification code recognition based on CNN (Pytorch)

## Preface

Reference link: [https://github.com/dee1024/pytorch-captcha-recognition](https://github.com/dee1024/pytorch-captcha-recognition)

The VeriBypasser system：[https://github.com/BatchClayderman/VeriBypasser/tree/main](https://github.com/BatchClayderman/VeriBypasser/tree/main)

This semester I chose the **artificial intelligence** professional course (bushi🐶)!

This is the **final homework** of our group. Since we have to do it, we should open source and develop one that can be used in **actual combat**.

Then I refactored it and did some expansion.

## Effect and principle

**Training set**: (using the commonly used Python verification code generation library ImageCaptcha)

```
Training set: 100k
Test set: 5k
```

------

> In terms of accuracy, the greater the number, the closer it is to the final accurate value (there will be a deviation)

| Type | Accuracy | Weight | Extraction code |
| :---------------------: | :----: | :-------------------------- --------------------------------: | :----: |
| 4 digits + uppercase letters | 85.2% | [Download link]( https://pan.baidu.com/s/1IC7qvrJKrwygMT5r_hN8aA ) | spdc |
| 4 digits + uppercase and lowercase | 72.38% | [Download link](https://pan.baidu.com/s/1ubshKMdjuRSvc7405cON8w) | he0w |

<img src="https://dailypic.hengyimonster.top/rate72.png" alt="image-20211211200828095" style="zoom:66%;" />

## Quick start

- **Step 1: Setup**

Go to setting.py to set `CHOOSE_LIST` and `MAX_CAPTCHA`

<img src="https://dailypic.hengyimonster.top/image-20211211201535432.png" alt="image-20211211201535432" style="zoom:30%;" />

- **Step 2: Create your own training set**

Go to setting.py to set `count` and `path`

The optional parameters are already in the comments.

> Here are suggestions:
>
> The number of training sets is 10k+ (a training set of 100K is recommended)
>
>The number of validation sets is 1k+

```bash
$ python makeImage.py
```



<img src="https://dailypic.hengyimonster.top/image-20211211201749408.png" alt="image-20211211201749408" style="zoom:30%;" />

- **Step 3: Train the model**

The generated files will be stored in `./result`

```bash
$ pythontrain.py
```

- **Step 4: Test the model**

```bash
$pythontest.py
```

- **Step 5: Model prediction**

```bash
$ python predict.py
```

## Log and Outlook

- Log 📝
   - 2021-12-11: The code is basically formed. The winning rate for 4-digit numbers + capital letters is stable at around 85%
   - 2021-12-18: The 4-digit number + uppercase and lowercase letter model reached a maximum of about 73% after a week of training
   - 2021-12-19: Upload the basically formed warehouse.
- Outlook 🦅

   - The accuracy rate can reach above 90.

##  Contact information

Looking forward to your PR

And shameless🙇‍♀️your more excellent hyperparameters.

We are an unknown group from **Jinan University**~

**Responsible person** contact email📮 2911567026@qq.com
