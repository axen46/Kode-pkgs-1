import cv2
import os 
from glob import glob
p=os.getcwd()
size=[[0,0],[128,0],[256,0],[384,0],[0,128],[120,128],[256,128],[384,128],[0,256],[128,256],[256,256],[384,256],[0,384],[128,384],[256,384],[384,384]]
path=p+'/7class/'
class_type=os.listdir(path)
print(class_type)
for new in class_type:
    print(new)
    if new!='.DS_Store':


        os.makedirs(p+'/'+new)
        os.chdir(p+'/'+new)
    else:
        continue
    
    for imagefile in glob(path+new+"/*"):
        for i in range(0,16):
            try:
                filename=imagefile.split('/')[-1]
                print(imagefile)
                image=cv2.imread(imagefile)
                crop=image[size[i][1]:size[i][1]+128,size[i][0]:size[i][0]+128]
                cv2.imwrite(str(size[i][0])+'-'+str(size[i][1])+'-'+filename,crop)
            except:
                continue
    os.chdir(p)
print("success")
