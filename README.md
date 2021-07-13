# COMMUNITY

> 강수아, 박종서 
> Android(Java), NodeJS, MongoDB

## DATABASE
  
   - MongoDB 를 사용해서 3개의 모델을 MongoSchema를 통해 만듬 (User, Table, Comment)
   - NodeJS의 router 를 이용해 '/user', '/table', '/comment' 세 개의 url 구분
   - NodeJS의 mongoose 를 이용해 Table과 Comment의 CRUD 구현

## 로그인 및 회원가입
  <img src= "https://user-images.githubusercontent.com/63537847/125448289-20d9d367-e33e-456f-a859-c234e328204d.png" width = "200" height = "400"> <img src = "https://user-images.githubusercontent.com/63537847/125448631-eb37713a-a96f-4341-9b60-f9892c7b5fc2.png" width="200" height="400">
  - 이름, 이메일, 비밀번호 등을 입력하고 버튼 누르면 db에 저장됨
  - 로그인하면 retrofit을 사용하여 서버로 아이디와 비밀번호가 보내지고 db에 있는 내용과 일치하면 로그인 성공함
  - 카카오톡 sdk를 사용해서 카카오 로그인 가능함 
  - 한 번 카카오로 로그인하면 자동 로그인이 되어 그 이후에는 로그인 할 필요가 없음 
  
## 3가지의 탭으로 이동 
  <img src= "https://user-images.githubusercontent.com/63537847/125448509-09b5c0cd-0ded-42df-90ad-9b3bcb5ade74.png" width = "200" height = "400">   
  
  - 3개의 탭이 있는 게시판으로 가는 버튼   
  - 내가 쓴 글을 모아서 볼 수 있는 탭으로 가는 버튼      
  - 내가 쓴 댓글들을 모아서 볼 수 있는 탭으로 가는 버튼      
  
  
   
## 1) 게시판 
 ## > 프로필 탭 
   <img src="https://user-images.githubusercontent.com/63537847/125449519-ff2c6473-c86f-4a37-ac85-6581861933c6.png" width="200" height="400">
   
   - 카카오톡으로 로그인을 하면 프로필사진, 이름, 이메일, 생일을 가져와서 화면에 뜨게 함
   - 일반 로그인을 사용한 경우 default 사진을 사용하고 나머지 이름, 이메일, 생일은 사용자가 회원가입할 때 작성한 정보를 사용해서 화면에 뜨게 함 
   - 상단의 뒤로가기 버튼을 누르면 다시 3개의 버튼이 있는 페이지로 돌아감 
  
  
  ## > 게시글 탭 
   <img src ="https://user-images.githubusercontent.com/63537847/125450998-7c8f0e4f-e5c0-40ef-b84c-db2cd2028b1b.png" width = "200" height="400"> <img src="https://user-images.githubusercontent.com/63537847/125451763-434c3654-f058-46ef-af60-c5ba46f0b6e4.png" width="200" height="400"> <img src="https://user-images.githubusercontent.com/63537847/125451439-de9a0f84-af41-49fe-9e95-7c0c6272d760.png" width ="200" height="400"> <img src="https://user-images.githubusercontent.com/63537847/125451504-a35dfb3b-8593-47bf-ac69-0068c5725976.png" width="200" height="400"> <img src="https://user-images.githubusercontent.com/63537847/125451640-6d5bb7b6-d78d-47fa-93f0-80f6e0195b5f.png" width="200" height="400"> <img src="https://user-images.githubusercontent.com/63537847/125453182-2edaa7f0-b7fd-45bd-ab9c-59448443870f.png" width="200" height="400"> <img src="https://user-images.githubusercontent.com/63537847/125452559-19bba78d-5684-4f11-8256-8cf35c5a24e3.png" width="200" height="400">
   - 하단에 있는 플로팅 버튼을 클릭하면 새 글을 쓸 수 있는 Fragment가 뜸 
   - 새 글을 작성하면 다시 원래 게시글 탭으로 돌아오고 내가 쓴 글이 바로 update된 것을 볼 수 있음 
   - 게시판에서 글을 클릭하면 글의 세부사항이 담긴 페이지가 뜸 
   - 제목, 작성자, 작성일, 글의 내용, 그리고 댓글이 뜸 
   - 본인이 쓴 글을 클릭하면 오른쪽 상단에 수정 버튼이 보임. 해당 버튼을 클릭하면 글을 수정할 수 있음
   - 본인이 쓴 글이 아닌 경우, 수정 버튼이 보이지 않음 
   - 본인이 쓴 글을 길게 클릭한 경우 글을 삭제할 수 있음 

   
   
  ##  > 채팅 탭 
   <img src ="https://user-images.githubusercontent.com/63537847/125454502-6ae5ce43-1731-4509-97ea-e6c20df78829.png" width="200" height="400"> <img src="https://user-images.githubusercontent.com/63537847/125454595-1bc131b3-567c-4440-af60-73d6d56660cc.png" width="200" height="400"> <img src ="https://user-images.githubusercontent.com/63537847/125454654-1661626e-b310-49c8-bb36-f4a37f93fd7f.png" width="200" height="400">
   
   - 본인의 이름을 입력하고 채팅방으로 입장
   - socket을 사용해서 하나의 서버 내에서 사용자들끼리 채팅을 할 수 있도록 함 
   - 사용자가 서버에 들어오지 않으면 글을 써도 send 버튼이 생기지 않음
   - 사용자들이 채팅방으로 들어오면 send 버튼이 생기고 글과 사진을 보낼 수 있음 
   
  ## 2) 내가 쓴 글 
   <img src ="https://user-images.githubusercontent.com/63537847/125455510-71f39810-59a4-4dbe-9f0e-b5929d662135.png" width="200" height="400"> 
   
   - 내가 쓴 글들을 탭에서 볼 수 있음 
   - db에서 name을 이용하여 내가 쓴 글들을 끌어옴 
    
    
  ## 3) 내가 쓴 댓글 
   <img src="https://user-images.githubusercontent.com/63537847/125455823-c1203850-daf3-4237-9d72-c9e6f0407d9f.png" width="200" height="400">
   
   - 내가 쓴 글과 비슷하게 db에서 댓글들을 가져옴 
