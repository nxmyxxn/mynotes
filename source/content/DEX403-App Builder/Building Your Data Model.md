
What is an Object on the Salesforce Platform?
Analogous to database tables


각 object = 업무
field 정보로 이루어져 있음

standard
custom
system obejcts provide data for salesforce platform operation
- metadata 들어가 있음

Lead
우리 제품에 관심을 갖는 사람. **후보군**

Lead에서 **Convert**
마케팅 활동  -> lead 파악하고 -> (opportunity는 옵션) account, contact 으로 넘기기
![[Pasted image 20250526113937.png||400]]
Campaign 아래 Campaign Memeber가 있음
campaign에는 cost, times(start-end)이 있음

campaign memeber은 사람임
즉 contact, lead를 campaign memeber에 넣어

marketing cloud
campaign lead 집중한 것

Sales cloud
?

service cloud
account case contact 중심

e-commerce

customer community (고객에게 보여줌)
저 그림에서 어느 부분까지 자름
partner commnuity (파터너사에게 보여줌)
저 그림에서 어느 부분까지 자름


Salesforce ID
데이터가 저장되는 순간에 pk 만들어져
a key that uniquely identifies each record("pk")

object 업무
record 일 - owner 지정하게 되어있음
queue 기다리는 사람들 구성


Global Picklist
global picklists may be reused on different objects

Object Have Relationships
Data Model : Account and Contact Objects
![[Pasted image 20250526134234.png||500]]

Object Relationships
- Lookup(parent-child): 서로 참조만 하는 관계임
certification - course

- Master-Detail
course-delivery


Lookup vs Master-Detail Relationships 
#lookup #relationship

| Lookup Relatioships                       | Master-Detail Relationships        |
| ----------------------------------------- | ---------------------------------- |
| Parent is not arequired field by default. | Parent field on child is required. |
|                                           |                                    |
|                                           |                                    |
|                                           |                                    |

contact은 입력할수도있고 안할수도있는 룩업


Junction Object
many to many -> one to many 두 개로 만들 수 있도록 연결해주는 Held

![[Pasted image 20250526145130.png]]

formula field
값이 저장되는 게 아니라 수식이 저장됨
global search 등으로 찾으면 안나옴
반면 list view, dashboard 등에서 계산되서 보여줌
근데 너무 많아지면 performance 낮아짐

roll-up 은 값이 저장됨
master-detail안에서만?

cross-object formula
object간 lookup relationship이 될 수 있는
최대 10개 까지 가져와서 보여줄 수 있는(object 선택>선택>선택>...>)

![[Pasted image 20250526170230.png]]

#### Using the Certification App
Our team sends contractor technicians out into the field to install and repair our server and networking equipment. 
The custom Certification app lets us manage the training and certification of all technicians.

- **Contractor technicians**: 현장에 나가 장비 설치·수리하는 사람들 = 교육 대상자
- **Training and certification**: 이 사람들을 **교육 시키고 자격증을 관리**하려는 목적
- 즉, **technicians가 수업 듣고 자격증 따고 하는 거임**

Account는 Technicians 제공하는 업체. 즉 Service Vendor

Contact는  (교육 받고 현장 나가는) Technician.
Account 아래 여러 Contact 있을 수 있지만 없어도 됨
Contact가 있어야 Attendee 있을 수 있음. Contact 하나 이지만 Attendee 여러 개일 수 있음.(한 명이 여러 수업 들을 수 있으니)

Certification App에 들어가서 <span style="color:rgb(0, 176, 80)">Course</span> Tab에 들어가면 Course 목록이 나옴. (ex. ADX 201, DEX 403 etc.)
Course에 들어가 Related 탭을 눌러 <span style="color:rgb(0, 176, 80)">CourseDelilvery</span> 목록을 볼 수 있음. (ex. ADX 201 강의에 대해 5/25-5/31 강의, 6/13-6/20 강의 etc.)
또 Delivery 하나 선택해서 들어가 보면 <span style="color:rgb(0, 176, 80)">Attendee</span> 목록 볼 수 있음. (수강생 정보)