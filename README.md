# 프로그래밍 배우고 싶을 때

프로그래머스 : https://programmers.co.kr/   에서 코딩 테스트학시

백준코딩 : https://www.acmicpc.net/

<CNN기반의 딥러닝 모델>

스탠포드, cs231
+ https://www.google.com/search?q=cs231n&oq=cs231n&aqs=chrome..69i57j0i512l9.2758j0j7&sourceid=chrome&ie=UTF-8
+ https://www.youtube.com/results?search_query=cs231n
강의 공부 해보기

RGB 말고 YUV란 것도 있음

L2: 모델 과적합 방지

4. Dropout : 중요한 가중치, 필요없는 가중치 구별해서 필요없는거 없애는거
dropout과 비슷하지만 다른 방법 'model pruning' : 모델에서 중요도가 낮은 뉴런을 제거하여 직접적인 모델 크기의 감소 (dropout : 뉴런자체를 잠깐 사용하지 않고 사용하고 그래서 사라지지는 않음)

distillation : 작은 모델에 큰 모델의 정보를 전달하여 작은 모델의 정확도를 향상시킴
knowledge-distillation(지식 증류)
엄청 똑똑한 선생님 모델(teacher model)을 만들고
Teacher model설정
→ ex) conv layer가 100개
Student model 설정
→ ex) conv layer 10개

→→선생님 모델을 학생 모델에 가르쳐준다라는 의미 / 모델 압축방법이 있다~

ㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡ

Lecture 18 : Famous Architecture (기계학습개론)
LeNet : The most widel known CNN architecture for MNIST
AlexNet :
특징 : ReLU for activation function  / local response normliztion scheme / overlappping poling : kernel size > stride / similar to LeNet-5 → only much larger and deeper /two regulariztion : dropout & data augmentation 사용 / +offsets은 bias와 비슷 /
VGGNet : prs : very simple and classical architecture / famous one is vgg16(config, D)
ResNet...

+CVPR 학술대회
+방송공학회
+scholar.google.com
+KISS
+DBpia
+ICCV / NPIS 학술대회

2. Network in network
GoogleNet
(by pushing the top-five error rate below 7%) / having parameters much more efficiently tan provious architectures /

3. 
잔차학습(ResNet) : stack of rus / batch norm / no pooling layer 
Inception=v4 : residual connection / 

SENET, 2017

→ github에서 코드들 검색하면서 숙지하기!
ex) https://github.com/search?q=classification 하면 분류 관련 코딩들 나옴
→ https://paperswithcode.com/(여기도 참고하면 좋음)


+ https://www.notion.so/ko-kr/ (자료 정리하거나 일기형식 뭐 그런거 할 수 있는 사이트)(참고)(해보고 싶으면 하기)

ㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡ

slack 강의 관련 hymenoptera 파일 지정된 폴더에 압축 풀기
conda activate pytorch
cd ~~~~
jupyter notebook

ㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡ
-새로 폴더를 만들어서 코드를 작성하기

가상환경 설정부터 모델을 만드는 과정
여태 했던 것들 참조해서 만들기! / 웬만하면 직접 만들기

1. 가상환경 설정하기
conda create -n my_env python=3.8

2. 실행에 필요한 pytorch 설치하기

3. 데이터셋 설정하기    (torchvision datasets)
(classification에 맞는 데이터셋)

4. 모델 설정하기
(기본적인 CNN사용해도 되지만(일반적으로convolution해도 되지만) / alexnet 가져다 써도 됨(다양한 CNN모델을 사용해도 됨)
LeNET, SENet, GoogleNet, Inceoption v3, ResNet(얘는 사용하기 어렵)..., VGGnet
기존 코드에서 함수단위(def선언) class단위를 참조해서 작성.

5. 훈련하기

6. 모델 평가하기
+ 시각화하는것은 해도 되고 안해도 무방
→ accuracy
전체 (분류 된) 클래스를 출력하거나 / 모델 자체의 accuracy를 출력시키면 됨.
