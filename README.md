## _Group name (Group2)_
Deep Learning เป็นการเรียนรู้เชิงลึกที่เลียนแบบการทำงานของโครงข่ายประสาทของมนุษย์ โดยมีการทำงานซ้อนกันหลายๆ ชั้นหรือเรียกว่า Layer จากข้อมูลตัวอย่างเพื่อหา Pattern ของข้อมูล 
โดยการศึกษาในครั้งนี้มีจุดมุ่งหมายเพื่อเปรียบเทียบประสิทธิภาพของ **`Traditional Machine Learning (ML)`** และ **`Multilayer Perceptron (MLP)`** รวมถึงการปรับ Hyperparameter เพื่อความสมบูรณ์ของโมเดล ทางทีมคาดหวังว่าจะได้ประสบการณ์ในเรื่องนี้ และเป็นประโยชน์ต่อผู้ที่กำลังสนใจในเรียนนี้ 

## _Key Highlight_
- XX
- XX
- XX

## 1. Introduction
การศึกษาในครั้งนี้ใช้ข้อมูลเรื่อง Stroke Prediction โดยข้อมูลจะมีลักษณะเป็น **`Binary classification`** คือการทำนายว่าผู้ป่วยคนนั้นมีโอกาสเป็นผู้ป่วยเป็นโรคหลอดเลือดสมองหรือไม่ (1: หากผู้ป่วยเป็นโรคหลอดเลือดสมอง, 0: หากผู้ป่วยไม่เป็นโรคหลอดเลือดสมอง) ซึ่งพิจารณาจากรายละเอียดข้อมูลของผู้ป่วยเช่น อายุ, เพศ, โรคความดันโลหิตสูง, โรคหัวใจ และค่าเฉลี่ยน้ำตาลในเลือดเป็นต้น

## 2. Data

### Data source
**Dataset descrption:**: Stroke Prediction Dataset (Ref: [Stroke Prediction Dataset | Kaggle](https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset))))<br>
**Total Patient:** 5,110 <br>
**Total Features:** 11 <br>
**Fields:**
1) id: รหัสประจำตัวผู้ป่วย 
2) gender: "Male", "Female" หรือ "Other"  
3) age: อายุของผู้ป่วย  
4) hypertension: 0 หากผู้ป่วยไม่เป็นโรคความดันโลหิตสูง, 1 หากผู้ป่วยไม่เป็นโรคความดันโลหิตสูง  
5) heart_disease: 0 หากผู้ป่วยไม่เป็นโรคหัวใจ, 1 หากผู้ป่วยเป็นโรคหัวใจ
6) ever_married: "No" หรือ "Yes"  
7) work_type: "children", "Govt_jov", "Never_worked", "Private" หรือ "Self-employed"  
8) Residence_type: "Rural" หรือ "Urban"  
9) avg_glucose_level: ค่าเฉลี่ยน้ำตาลในเลือด  
10) bmi: ดัชนีมวลกาย
11) smoking_status: "formerly smoked", "never smoked", "smokes" หรือ "Unknown"*  
*Note: "Unknown" ในคอลัมน์ smoking_status หมายถึงไม่มีข้อมูลสำหรับผู้ป่วยรายนี้* <br>



### EDA

### Data preparation
การเตรียมข้อมูลก่อน train model เราทำการ drop ค่า outliner ออก หลังจากนั้นจึงจัดการข้อมูล Binary category และ Multicategory โดยใช้ **`One-Hot encoding`** เพื่อเปลี่ยนข้อมูลที่เก็บในลักษณะ categorical ให้อยู่ในรูป Binary values เนื่องจากการทำ Machine leaning นั้น ต้องการข้อมูลในรูปแบบตัวเลขเพื่อใช้ในการ train และ predict โดยแปลงค่าในคอลัมน์ gender, ever_married, work_type, residence_type และ smoking_status เพื่อให้อยู่ในรูปแบบดังกล่าว <br>

และเนื่องจากข้อมูลของเรามีความ imbalance เราจึงเลือกใช้ **`SMOTE`** (synthetic minority over-sampling technique) ซึ่งเป็นเทคนิคที่ใช้ในการแก้ปัญหาการจำแนกข้อมูลที่ไม่สมดุลและทำการ normalize ค่าด้วย MinMaxScaler

![image](https://user-images.githubusercontent.com/101736826/187707794-38780d34-8cc0-4fd0-95de-48e3eda8c46f.png)

### Data pre-processing

### Data postprocessing

### Data splitting (train/val/test) 

## 3. Network architecture

## 4. Training

## 5. Results


## 3. Experiment result and discussion
สำหรับการ train model หนึ่งในสิ่งสำคัญคือการเลือกใช้ฟีเจอร์เพื่อไม่ให้ model มีความ overfit มากเกินไป ดังนั้น เราจึงเริ่มจากการดูค่า correlation ของตัวแปรต่างๆ ต่อการเป็นโรคหลอดเลือดสมอง (stroke) ซึ่งหาก correlation มีค่ามาก หมายถึงมีความสัมพันธ์ต่อการเป็น stroke มาก เช่น อายุ การเป็นโรคหัวใจ เป็นต้น <br>

สำหรับการ normalization เราใช้ min-max normalization


## 4. Conclusion


### Pros and Cons
- เปรียบเทียบข้อดีข้อเสียของการใช้ ML และ MLP

## 5. Recommendation




## _End Credit_
<table>
  <tr>
    <td>6410422005</td>
    <td>Metpiya Learakkakorn</td>
    <td>Prepare datase, Data cleaning, EDA, Traditional Machine Learning (ML), Multilayer Perceptron (MLP)</td>
  </tr>
  <tr>
    <td>6410422015</td>
    <td>Khodchapan Vitheethum</td>
    <td>Prepare datase, Data cleaning, EDA, Traditional Machine Learning (ML), Multilayer Perceptron (MLP)</td>
  </tr>
  <tr>
    <td>6410422017</td>
    <td>Peerat Pookpanich</td>
    <td>Prepare datase, Data cleaning, EDA, Traditional Machine Learning (ML), Multilayer Perceptron (MLP)</td>
  </tr>
  <tr>
    <td>6410422031</td>
    <td>Anyamanee Pornpanvattana</td>
    <td>Prepare datase, Data cleaning, EDA, Traditional Machine Learning (ML), Multilayer Perceptron (MLP)</td>
  </tr>
</table>
