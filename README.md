# EXNO-5-DS-DATA VISUALIZATION USING MATPLOT LIBRARY

# Aim:
  To Perform Data Visualization using matplot python library for the given datas.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding and Output:
```
import pandas as pd
import numpy as np
import seaborn as sns
import matplotlib.pyplot as plt
from scipy.interpolate import make_interp_spline
x_values=[0,1,2,3,4,5]
y_values=[0,1,4,9,16,25]
plt.plot(x_values,y_values)
plt.show()
x = [1, 2, 3, 4, 5]
y = [3, 6, 2, 7, 1]
plt.plot(x, y, label="Line Graph", color="blue", marker="o")
plt.xlabel("X Axis")
plt.ylabel("Y Axis")
plt.legend()
plt.title("Simple Line Graph")
plt.show()
x1 = [1,2,3]
y1 = [2,4,1]
x2 = [1,2,3]
y2 = [4,1,3]
plt.plot(x1, y1, label="line 1", color="red")
plt.plot(x2, y2, label="line 2", color="green")
plt.scatter(x1, y1, color="red")
plt.scatter(x2, y2, color="green")
plt.xlabel("X Axis")
plt.ylabel("Y Axis")
plt.legend()
plt.title("Two Line Graph")
plt.show()
x=[1,2,3,4,5,6]
y=[2,4,1,5,2,6]
plt.plot(x,y,color='green',linestyle='dashed',linewidth=3,marker='o',markerfacecolor='blue') 
plt.ylim(1,8)
plt.xlim(1,8)
plt.xlabel('x-axis')
plt.ylabel('y-axis')
plt.title('Some cool customizations')
plt.show()
x_values = [0,1,2,3,4,5]
y_values = [0,1,4,9,16,25]
plt.plot(x_values, y_values)
plt.fill_between(x_values, y_values, color="lightblue", alpha=0.5)
plt.title("Fill Between Graph")
plt.show()
x = np.array([1,2,3,4,5,6,7,8,9,10])
y = np.array([2,4,5,7,8,8,9,10,11,12])
x_new = np.linspace(x.min(), x.max(), 300)
spl = make_interp_spline(x, y, k=3)
y_smooth = spl(x_new)
plt.plot(x_new, y_smooth)
plt.title("Smooth Curve")
plt.show()
values = [5, 6, 3, 7, 2]
names  = ["A", "B", "C", "D", "E"]
plt.bar(names, values, color='orange')
plt.xlabel("Names")
plt.ylabel("Values")
plt.title("Bar Graph")
plt.show()
c1 = ['red', 'green', 'blue', 'yellow', 'purple']
plt.bar(names, values, color=c1)
plt.show()
df = sns.load_dataset("tips")
avg_total_bill = df.groupby("day")["total_bill"].mean()
avg_tip = df.groupby("day")["tip"].mean()
plt.figure(figsize=(8, 6))
p1 = plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill')
p2 = plt.bar(avg_tip.index, avg_tip, bottom=avg_total_bill, label='Tip')
plt.xlabel('Day of the Week')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Day')
plt.legend()
plt.show()
x_values = [0,1,2,3,4,5]
y_values = [0,1,4,9,16,25]
plt.scatter(x_values, y_values)
plt.title("Scatter Plot")
plt.show()

activities = ['eat', 'sleep', 'work', 'play']
slices = [3, 7, 8, 6]
colors = ['r', 'y', 'g', 'b']
plt.pie(slices, labels=activities, colors=colors, autopct='%1.1f%%', startangle=90)
plt.title("Pie Chart")
plt.show()
x=np.arange(0,4*np.pi,0.1)
y=np.sin(x)
plt.title("sine wave form")
plt.plot(x,y)
plt.show()
x=[1,2,3,4,5]
y1=[10,12,14,16,18]
y2=[5,7,9,11,13]
y3=[2,4,6,8,10]
plt.fill_between(x,y1,color='blue')
plt.fill_between(x,y2,color='green')
plt.plot(x,y1,color='red')
plt.plot(x,y2,color='black')
plt.legend(['y1','y2'])
plt.show()
import numpy as np
import matplotlib.pyplot as plt
from scipy.interpolate import make_interp_spline
x=np.array([1,2,3,4,5,6,7,8,9,10])
y=np.array([2,4,5,7,8,8,9,10,11,12])
spl=make_interp_spline(x,y)
x_smooth=np.linspace(x.min(),x.max(),100)
y_smooth=spl(x_smooth)
plt.plot(x,y,'o',label='data')
plt.plot(x_smooth,y_smooth,'-',label='Spline')
plt.legend()
plt.show()
values=[5,6,3,7,2]
names=["A","B","C","D","E"]
plt.barh(names,values,color="yellowgreen")
plt.show()
x=[2,8,10]
y=[11,16,9]
x2=[3,9,11]
y2=[6,15,7]
plt.bar(x,y,color='r')
plt.bar(x2,y2,color='g')
plt.title('Bar graph')
plt.ylabel('Y axis')
plt.xlabel('X axis')
plt.show()
x=[2,1,6,4,2,4,8,9,4,2,4,10,6,4,5,7,7,3,2,7,5,3,5,9,2,1]
plt.hist(x,bins=10,color='blue',alpha=0.5)
plt.show()
data = [42, 55, 67, 68, 70, 72, 75, 79, 81, 88, 95, 102, 140, 160]
plt.boxplot(data)
plt.title("Simple Boxplot")
plt.ylabel("Values")
plt.show()
```


<img width="585" height="422" alt="image" src="https://github.com/user-attachments/assets/06f609a2-3201-4d70-9183-f42daf93e5da" />
<img width="622" height="449" alt="image" src="https://github.com/user-attachments/assets/f2ded53e-7ed3-42f8-b320-ba5ef167005c" />
<img width="602" height="439" alt="image" src="https://github.com/user-attachments/assets/193e4759-7bf3-4163-abe5-f1cbb71a270f" />
<img width="572" height="457" alt="image" src="https://github.com/user-attachments/assets/9be82ba8-3910-4e22-bd43-fcdad6708e67" />
<img width="558" height="427" alt="image" src="https://github.com/user-attachments/assets/6fa98738-e590-4ab7-a0bb-fb268e676b4e" />

<img width="578" height="438" alt="image" src="https://github.com/user-attachments/assets/d9b938a0-2cae-4f8e-982b-d2226a19ba06" />

<img width="586" height="455" alt="image" src="https://github.com/user-attachments/assets/190e41ee-312f-4732-8939-3bd1e44ff669" />
<img width="557" height="416" alt="image" src="https://github.com/user-attachments/assets/31eaa336-849d-406e-adeb-3ed9ed97af0c" />

<img width="749" height="540" alt="image" src="https://github.com/user-attachments/assets/cdd5b358-0ee8-4087-b918-689075af15d8" />

<img width="589" height="435" alt="image" src="https://github.com/user-attachments/assets/18087290-886d-4ad3-a361-c227901e092f" />

<img width="470" height="393" alt="image" src="https://github.com/user-attachments/assets/fbffc7ae-3ebe-4e65-a2e8-529e781362e9" />
<img width="603" height="424" alt="image" src="https://github.com/user-attachments/assets/b7408084-d001-4e7b-b648-ba332f5dc361" />
<img width="625" height="420" alt="image" src="https://github.com/user-attachments/assets/08df224f-253b-468c-b049-df7b7294a76a" />

<img width="587" height="411" alt="image" src="https://github.com/user-attachments/assets/91a62fa7-9cae-4d18-af9d-f1284c938b70" />

<img width="557" height="411" alt="image" src="https://github.com/user-attachments/assets/57392dab-abbb-4d26-92e1-3984fc41dd2d" />
<img width="580" height="445" alt="image" src="https://github.com/user-attachments/assets/9775e2c6-4d55-4294-aa13-57e8db457951" />

<img width="552" height="408" alt="image" src="https://github.com/user-attachments/assets/0245ec1c-7937-4465-8cad-0d9c6e0bbfaf" />
<img width="606" height="438" alt="image" src="https://github.com/user-attachments/assets/bc8eab79-f21f-49dc-81b9-b7df58bf0564" />




# Result:
 Include your result here
