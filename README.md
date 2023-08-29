# Board-project

<p>spring boot로 게시판을 만들어보자</p>

<li>DB : maria DB</li>
<li>DBMS : DBeaver</li>
<li>JDBC : MyBatis</li>
<li>View : Thymeleaf</li>
<li>Build Tool : Gradle</li>
<li>IDE : IntelliJ</li>
<li>Java version : 11</li>

## 폴더 구조
```
📦src
 ┣ 📂main
 ┃ ┣ 📂java
 ┃ ┃ ┗ 📂com
 ┃ ┃ ┃ ┗ 📂study
 ┃ ┃ ┃ ┃ ┣ 📂aop
 ┃ ┃ ┃ ┃ ┃ ┗ 📜LoggerAspect.java
 ┃ ┃ ┃ ┃ ┣ 📂common
 ┃ ┃ ┃ ┃ ┃ ┣ 📂dto
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜MessageDto.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ 📜SearchDto.java
 ┃ ┃ ┃ ┃ ┃ ┣ 📂file
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ 📜FileUtils.java
 ┃ ┃ ┃ ┃ ┃ ┗ 📂paging
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜Pagination.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ 📜PagingResponse.java
 ┃ ┃ ┃ ┃ ┣ 📂config
 ┃ ┃ ┃ ┃ ┃ ┣ 📜DatabaseConfig.java
 ┃ ┃ ┃ ┃ ┃ ┣ 📜SecurityConfig.java
 ┃ ┃ ┃ ┃ ┃ ┗ 📜WebMvcConfig.java
 ┃ ┃ ┃ ┃ ┣ 📂domain
 ┃ ┃ ┃ ┃ ┃ ┣ 📂comment
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜CommentApiController.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜CommentMapper.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜CommentRequest.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜CommentResponse.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜CommentSearchDto.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ 📜CommentService.java
 ┃ ┃ ┃ ┃ ┃ ┣ 📂file
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜FileApiController.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜FileMapper.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜FileRequest.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜FileResponse.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ 📜FileService.java
 ┃ ┃ ┃ ┃ ┃ ┣ 📂member
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜Gender.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜MemberController.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜MemberMapper.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜MemberRequest.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜MemberResponse.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ 📜MemberService.java
 ┃ ┃ ┃ ┃ ┃ ┗ 📂post
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜PostController.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜PostMapper.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜PostRequest.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┣ 📜PostResponse.java
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ 📜PostService.java
 ┃ ┃ ┃ ┃ ┣ 📂interceptor
 ┃ ┃ ┃ ┃ ┃ ┣ 📜LoggerInterceptor.java
 ┃ ┃ ┃ ┃ ┃ ┗ 📜LoginCheckInterceptor.java
 ┃ ┃ ┃ ┃ ┣ 📜BoardApplication.java
 ┃ ┃ ┃ ┃ ┗ 📜RestApiTestController.java
 ┃ ┗ 📂resources
 ┃ ┃ ┣ 📂mappers
 ┃ ┃ ┃ ┣ 📜CommentMapper.xml
 ┃ ┃ ┃ ┣ 📜FileMapper.xml
 ┃ ┃ ┃ ┣ 📜MemberMapper.xml
 ┃ ┃ ┃ ┗ 📜PostMapper.xml
 ┃ ┃ ┣ 📂static
 ┃ ┃ ┃ ┣ 📂css
 ┃ ┃ ┃ ┃ ┣ 📜button.css
 ┃ ┃ ┃ ┃ ┣ 📜common.css
 ┃ ┃ ┃ ┃ ┣ 📜content.css
 ┃ ┃ ┃ ┃ ┗ 📜default.css
 ┃ ┃ ┃ ┣ 📂images
 ┃ ┃ ┃ ┃ ┣ 📜default_profile.png
 ┃ ┃ ┃ ┃ ┣ 📜icons.png
 ┃ ┃ ┃ ┃ ┣ 📜icon_cal.png
 ┃ ┃ ┃ ┃ ┣ 📜icon_errorpage.png
 ┃ ┃ ┃ ┃ ┣ 📜logo.png
 ┃ ┃ ┃ ┃ ┣ 📜noimg_profile.gif
 ┃ ┃ ┃ ┃ ┗ 📜no_img.gif
 ┃ ┃ ┃ ┗ 📂js
 ┃ ┃ ┃ ┃ ┣ 📂jquery-ui-1.12.1.custom
 ┃ ┃ ┃ ┃ ┃ ┣ 📂images
 ┃ ┃ ┃ ┃ ┃ ┃ ┗ 📜ui-icons_444444_256x240.png
 ┃ ┃ ┃ ┃ ┃ ┣ 📜jquery-ui.css
 ┃ ┃ ┃ ┃ ┃ ┣ 📜jquery-ui.min.css
 ┃ ┃ ┃ ┃ ┃ ┗ 📜jquery-ui.min.js
 ┃ ┃ ┃ ┃ ┣ 📜common.js
 ┃ ┃ ┃ ┃ ┣ 📜function.js
 ┃ ┃ ┃ ┃ ┗ 📜jquery-3.6.0.min.js
 ┃ ┃ ┣ 📂templates
 ┃ ┃ ┃ ┣ 📂common
 ┃ ┃ ┃ ┃ ┗ 📜messageRedirect.html
 ┃ ┃ ┃ ┣ 📂fragments
 ┃ ┃ ┃ ┃ ┣ 📜body.html
 ┃ ┃ ┃ ┃ ┗ 📜header.html
 ┃ ┃ ┃ ┣ 📂layout
 ┃ ┃ ┃ ┃ ┗ 📜basic.html
 ┃ ┃ ┃ ┣ 📂member
 ┃ ┃ ┃ ┃ ┗ 📜login.html
 ┃ ┃ ┃ ┗ 📂post
 ┃ ┃ ┃ ┃ ┣ 📜list.html
 ┃ ┃ ┃ ┃ ┣ 📜view.html
 ┃ ┃ ┃ ┃ ┗ 📜write.html
 ┃ ┃ ┣ 📜application.properties
 ┃ ┃ ┣ 📜log4jdbc.log4j2.properties
 ┃ ┃ ┗ 📜logback-spring.xml
 ┗ 📂test
 ┃ ┗ 📂java
 ┃ ┃ ┗ 📂com
 ┃ ┃ ┃ ┗ 📂study
 ┃ ┃ ┃ ┃ ┣ 📜BoardApplicationTests.java
 ┃ ┃ ┃ ┃ ┣ 📜PostMapperTest.java
 ┃ ┃ ┃ ┃ ┗ 📜PostServiceTest.java

```