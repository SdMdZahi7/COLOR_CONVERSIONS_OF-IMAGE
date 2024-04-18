# COLOR_CONVERSIONS_OF-IMAGE
## AIM
To write a python program using OpenCV to do the following image manipulations.

i) Read, display, and write an image.

ii) Access the rows and columns in an image.

iii) Cut and paste a small portion of the image.

iv)To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.


## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Choose an image and save it as a filename.jpg ,
### Step2:
Use imread(filename, flags) to read the file.
### Step3:
Use imshow(window_name, image) to display the image.
### Step4:
Use imwrite(filename, image) to write the image.
### Step5:
End the program and close the output image windows.
### Step6:
Convert BGR and RGB to HSV and GRAY
### Step7:
Convert HSV to RGB and BGR
### Step8:
Convert RGB and BGR to YCrCb
### Step9:
Split and Merge RGB Image
### Step10:
Split and merge HSV Image

##### Program:
### Developed By: SYED MUHAMMED ZAHI  
### Register Number: 212221230114


### i) Read and display the image

```Python
    import cv2
    image=cv2.imread('car.jpeg',1)
    image=cv2.resize(image,(400,300))
    cv2.imshow('Zahi',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
``` 
  </td>
  <td>

### OUTPUT:

![image](https://github.com/SdMdZahi7/COLOR_CONVERSIONS_OF-IMAGE/assets/94187572/04acbf44-3e8a-4a19-9c76-9de0cb5f8c18)

</td>
  </tr>

   <tr>
    <td width=50%>


### ii)Write the image

```Python
    image=cv2.imread('car.jpeg',0)
    cv2.imwrite('d.jpeg',image)
```
  </td>
  <td>

### OUTPUT:

![image](https://github.com/SdMdZahi7/COLOR_CONVERSIONS_OF-IMAGE/assets/94187572/c8c829c8-b66d-481d-a223-aa1a0451acb0)


  </td>
  </tr>
  <tr>
    <td width=50%>

### iii)Shape of the Image
```Python
    import cv2
    image=cv2.imread('car.jpeg',1)
    print(image.shape)
```
  </td>
  <td>

### OUTPUT:
![image](https://github.com/SdMdZahi7/COLOR_CONVERSIONS_OF-IMAGE/assets/94187572/c40eff41-f5f5-46d5-962c-1fe100621bcf)

  </td>
  </tr>
  <tr>
    <td>
      

### iv)Access rows and columns
```Python
    import random
    import cv2
    image=cv2.imread('car.jpeg',1)
    image=cv2.resize(image,(400,400))
    for i in range (150,200):
      for j in range(image.shape[1]):
          image[i][j]=[random.randint(0,255),
                       random.randint(0,255),
                       random.randint(0,255)] 
    cv2.imshow('car part image',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
```
  </td>
  <td width="50%">

### OUTPUT:

![image](https://github.com/SdMdZahi7/COLOR_CONVERSIONS_OF-IMAGE/assets/94187572/191e823d-aa4e-453d-b800-bd32aa89cd5a)

  </td>
  </tr>
  <tr>
    <td width=50%>
      


### v)Cut and paste portion of image
 ```Python
   import cv2
   image=cv2.imread('car.jpeg',1)
   image=cv2.resize(image,(400,400))
   tag =image[130:200,110:190]
   image[110:180,120:200] = tag
   cv2.imshow('cut and paste',image)
   cv2.waitKey(0)
   cv2.destroyAllWindows()
```
  </td>
  <td>
    
### OUTPUT:
![image](https://github.com/SdMdZahi7/COLOR_CONVERSIONS_OF-IMAGE/assets/94187572/df0fabaa-2d22-4af5-9e42-62c4cc04834f)

  </td>
  </tr>
</table>



### vi) BGR and RGB to HSV and GRAY
```Python
import cv2
img = cv2.imread('car.jpeg',1)
img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)
hsv1 = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV',hsv1)
hsv2 = cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv2)
gray1 = cv2.cvtColor(img,cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY',gray1)
gray2 = cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### OUTPUT:
![image](https://github.com/SdMdZahi7/COLOR_CONVERSIONS_OF-IMAGE/assets/94187572/558624dc-209f-41e8-9d70-d440776faa81)
![image](https://github.com/SdMdZahi7/COLOR_CONVERSIONS_OF-IMAGE/assets/94187572/ba1d2df5-8fbe-4dfa-b0fd-967145aaf478)





### vii) HSV to RGB and BGR
```Python
import cv2
img = cv2.imread('car.jpeg')
img = cv2.resize(img,(300,200))
img = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('Original HSV Image',img)
RGB = cv2.cvtColor(img,cv2.COLOR_HSV2RGB)
cv2.imshow('2HSV2BGR',RGB)
BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',BGR)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### OUTPUT:
![image](https://github.com/SdMdZahi7/COLOR_CONVERSIONS_OF-IMAGE/assets/94187572/40e9a919-92eb-4391-8c77-4a47bb91eeb0)


### viii) RGB and BGR to YCrCb
```Python
import cv2
img = cv2.imread('car.jpeg')
img = cv2.resize(img,(300,200))
cv2.imshow('Original RGB Image',img)
YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)
YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR-2-YCrCb',YCrCb2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### OUTPUT:
![image](https://github.com/SdMdZahi7/COLOR_CONVERSIONS_OF-IMAGE/assets/94187572/b12ebf3a-fe43-4447-a705-f5800849bfa2)

### ix) Split and merge RGB Image
```Python
import cv2
img = cv2.imread('car.jpeg',1)
img = cv2.resize(img,(300,200))
R = img[:,:,2]
G = img[:,:,1]
B = img[:,:,0]
cv2.imshow('R-Channel',R)
cv2.imshow('G-Channel',G)
cv2.imshow('B-Channel',B)
merged = cv2.merge((B,G,R))
cv2.imshow('Merged RGB image',merged)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### OUTPUT:
![image](https://github.com/SdMdZahi7/COLOR_CONVERSIONS_OF-IMAGE/assets/94187572/477cf326-ac6e-434a-8c38-2a9eff0dc3d7)


### x) Split and merge HSV Image
```Python
import cv2
img = cv2.imread("car.jpeg",1)
img = cv2.resize(img,(300,200))
img=cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
H,S,V=cv2.split(img)
cv2.imshow('Hue',H)
cv2.imshow('Saturation',S)
cv2.imshow('Value',V)
merged = cv2.merge((H,S,V))
cv2.imshow('Merged',merged)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### OUTPUT:
![image](https://github.com/SdMdZahi7/COLOR_CONVERSIONS_OF-IMAGE/assets/94187572/59b8c464-db75-400d-9749-de3595b9da9d)




## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.







