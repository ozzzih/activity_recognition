# activity_recognition
## activity recognition using deep learning with sensor data

### data: DLA dataset
url-https://www.dlr.de/kn/en/desktopdefault.aspx/tabid-12705/22182_read-50785/

### First: Data load and Processing 
**dataload.ipynb** 파일을 이용하여 다운받은 DLA데이터셋을 load 및 전처리 한다.
* matfile형태로 저장되어 있는 데이터셋을 압축해제 후, 접근
* acc와 gyro센서 columns들만 이용  

---------------------------------------------------
< 기존 columns>


<img width="598" alt="image" src="https://user-images.githubusercontent.com/90295119/224652160-b7dda19b-2e5f-4b0d-bc26-e6fa68867568.png">

----------------------------------------------------
<전처리 후 columns>


<img width="338" alt="image" src="https://user-images.githubusercontent.com/90295119/224652989-6a341110-c5ac-445a-a425-533abab47816.png">

----------------------------------------------------
* length=128, overlap=64로 설정
연속적인 센서데이터셋에서 length만큼의 segment 형성

segment1형성 후 시작점으로부터 overlap크기만큼 이동 후 length만큼의 segment2형성

segment2형성 후 시작점으로부터 overlap크기만큼 이동 후 length만큼의 segment3형성

....


### Second: Making a model

**makemodel.ipynb**파일을 이용

CNN-LSTM 모델 학습.

