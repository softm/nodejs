## 책
 - Nodejs : https://drive.google.com/drive/u/1/folders/1FuC_7mvQIjZzsp0QaW1pKPBd9p3y3tmN

 - Typescript : https://drive.google.com/drive/u/1/folders/1RtYRhM1eBD8-vB33PLwbQb7Tfb7Wt7Qx

#### # 참고 
   - [https://velopert.com/241](https://velopert.com/241)

#### # [Node.js?](https://nodejs.org/ko/)
  - Chrome V8 JavaScript 엔진으로 빌드된 JavaScript Runtime.
  - 2009년에 Ryan Dahl에 의해 개발.
  - 이벤트 기반, 논 블로킹 I/O 모델.
  - Node.js의 패키지 생태계인 npm은 세계에서 가장 큰 오픈 소스 라이브러리.

  - 비동기 I/O 처리 .
  - 빠른 속도
  - 단일 쓰레드 / 뛰어난 확장성
  - 노  버퍼링
  - 라이센스: MIT License

#### # REPL (Read Eval Print Loop)
  - 읽고 값을 계산하고 출력하는 일을 반복하는 행위를 REPL 루프라고한다.
  - Node.js는 REPL 환경은 테스팅 및 디버깅에 이용된다.
  - REPL Command
```
Ctrl+C          – 현재 명령어 종료
Ctrl+C (2번)    – Node REPL 종료
Ctrl+D          – Node REPL 종료
위/아래 키      – 명령어 히스토리 탐색.
Tab             – 현재 입력란에 쓴 값으로 시작하는 명령어 / 변수 목록을 확인합니다.
.help           – Print this help message
.break          – 멀티 라인 표현식 입력 도중 입력 종료
.clear          – .break 와 동일
.save filename  – Node REPL 세션을 파일 저장
.load filename  – Node REPL 세션에 파일 로드
.editor         - Enter editor mode
```

#### # 윈도우모듈 설치함.
  1. [https://nodejs.org/ko/](https://nodejs.org/ko/)
  2. 다운로드.
  3. 설치 실행.

#### # 테스트실행.
  1. Win + R
  2. cmd [Enter]
  3. node [Enter]
  4. 1+1[Enter]

#### # Hello World.
  1. app.js 작성( C:\nodetest\app.js )
```javascript
const http = require('http');

const hostname = '127.0.0.1';
const port = 3000;

const server = http.createServer((req, res) => {
  res.statusCode = 200;
  res.setHeader('Content-Type', 'text/plain');
  res.end('Hello World\n');
});

server.listen(port, hostname, () => {
  console.log(`Server running at http://${hostname}:${port}/`);
});
```

  2. Node실행
   1. Win + R
   2. cmd [Enter]
   3. cd C:\nodetest\[Enter]
   4. node app.js [Enter]
   5. http://localhost:3000

#### # 변수사용.
```bash
$ node
> x = 10
10
> var y = 5
undefined
> x + y
15
> console.log("Value is " + ( x + y ))
Value is 15
undefined
```

#### # Multi-Line 표현식 사용
  - do-while 루프 REPL
```bash
$ node
> var x = 0
undefined
> do {
... x++;
... console.log("x: " + x);
... } while ( x < 3 );
x: 1
x: 2
x: 3
undefined
>
```

#### # Underscore ( _ ) 변수
  - _ 변수는 최근 결과값을 지칭.
```bash
$ node
> var x = 10;
undefined
> var y = 5;
undefined
> x + y;
15
> var sum = _
undefined
> console.log(sum)
15
undefined
>
```

#### # Node Package Manager (NPM)
  - NPMSearch (https://npmsearch.com/) Node.js 패키지/모듈 저장소.
  - Node.js 패키지 설치 및 버전 / 호환성 관리 커맨드라인 유틸리티.

#### # version 확인
```
$ npm --version
6.1.0
```

#### # 최신업데이트
```
$ npm install npm -g
```

#### # 모듈 인스톨 ( exoress 모듈 )
```
$ npm install express
```
#### # 글로벌 vs 로컬 모듈 설치
  - 로컬모드 설치(기본) :> npm이 실행된 디렉토리 경로의 node_modules디렉토리에 설치됨.
```
$ npm install express
```

  - 글로벌모드 설치 ( -g <:: global 설치모드)
```
$ npm install express -g
```

#### # 모듈 제거
```
$ npm uninstall express
```

#### # 모듈 업데이트
```
$ npm update express
```

#### # 모듈 검색
```
$ npm search express
```

== 미정리 ==============================================
http://www.easyspub.co.kr
<< 자료실 (회원가입 무료)

console : dir, time, time End
__filename, __dirname
process : argv, env, exit()
var modules = require('module1');
modules.함수이름();
                 ^^^^^^^^^^^^^^^^^^^^^^^^^^
exports.함수이름 = 함수정의
exports.add = function(a,b) {
               return a + b
           }
 var calc = {}
            calc.add = function(a,b) {
                 return a + b
            };
            module.exports = calc;
npm install nconf
npm uninstaller nconf
npm install nconf --save : dependencies 속성 package.json에 추가.
var nconf = require('nconf');
           nconf.env();
          console.log('OS : %so, nconf.get('OS'));
내장모듈 정보 : http://nodes.org/api
시스템정보 내장모듈 
var os = require'(os');
os.hostname() 
os.totalmem()
os.freemem()
os.cpus()
os.networkInterfaces()
파일패스 path 모듈
var path = require'(path');
path.join()
path.dirname()
path.basename()
path.extname()
Javascript 자료형
Boolean
Number
String
undefined
null
Object
Array.forEach(function(item,index){
              console.log('배열 요소 #' + index : %s', item.name);
Array 함수
push
pop
unshift
splice
slice
           }
var url = require'(url');
var curURL = url.parse('http://m.naver.com/search.naver?query=steve+job&where=m');
var curStr = url.format(curURL);
var os = require'(querystring');
Event Emitter
on(event,listener)
once(event,listener)
removeListener(event,listener)
process.on('exit', function(){
               console.log('exit ~');
           }
setTimeout(function(){
            process.exit();
           });
process.on('tick', function(count){
              console.log('exit ~ %s',count);
           }
setTimeout(function(){
                process.emit('tick', 2);
           });
calc3.js
          var util = require('util');
           var EventEmitter = require('event').EventEmitter;
           var Calc = function(){
                 var self = this;
                 this.on('stop', function(){
                     console.log('stop이젠트 호출 ~');
                  } ;
            } ;
            util.inherits(Calc, EventEmitter);
            Calc.prototype.add = function(a,b){
                 return a+b;
            }
            module.exports = Calc;
            module.exports.title = 'calculator';
var Calc = require('./calc3');
           var calc = new Calc();
           calc.emit('stop');
var fs = require('fs');
           var data = fs.readFileSync('package.json', 'utf8');
readFile
readFileSync
writeFile
writeFileSync
open
read
write
close
createReadStream
createWriteStream

Request객체
req.query
req.body
req.header(name)

var fs = require('fs');
           var http = require('http');
           var server =            http.createServer(function(req,res){
                 var instream =                  fs.createReadStream(./'output.txt');
                 instrem.pipe(res);
          });
          server.listen(7001,'127.0.0.1');

var http = require('http');
           var server =   http.createServer();
          var port = 3000;
          server.listen(port,function(){});
listen : 서버 시작
connection : 클라이언트 연결
request : 클라이언트 요청
close : 서버 종료
Express
set(name,value) : 서버 설정을 뤼한 속성을 지정합니다.
get(name) : 서버 설정을 위해 지정한 속성을 꺼내 옵니다.
use([path],function [,functio  ... ]) : 미들웨어 함수를 사용합니다.
get([path],function) : 특덩 패스로 요청된 정보를 처리합니다.
npm install express --save
           var app = express();
           app.set('port', process.env.PORT || 3000);
           http.createServer(app).listen(app.ger('port'), function(){
      console.log('Express Start : ' + app.get('port'));
}

var express = require('express')
    , http = require('http');
var app = express();
app.use(function(req,res,next){
console.log('첫 번째 미들웨어에서 요청을 처리함');

var userAgent = req.header('User-Agent');
var paramName = req.query.name;

res.writeHead('200',{'Contet-Type':'text/html;charset=utf8'});
res.end('<h1>Express Server Response Result</h1>');
}

app.use(function(req,res,next){
     console.log('첫 번째 미들웨어 요청');
      req.user = 'mike';
      next();
}
static 미들웨어
nom install serve-static --save
var static = require('serve-static');
app.use('public',static(path.join(__dirname,'public');




app.use('/', function(req,res,next){
console.log('두 번째 미들웨어 요청');
res.writeHead('200',{'Contet-Type':'text/html;charset=utf8'});
res.end('<h1>Express Server Response Result : ' + req.user + </h1>');
}
Express Method
send
status
sensStatus
redirect
render

app.use(function(req,res,next){
      console.log('첫 번째 미들웨어 요청');
      req.user = 'mike';
      res send({name:'softm', age:44});
      // res.status(403).send('Forbidden');
      // res.sendStatus(404);
}
body-parser 미들웨어
POST 요청 파라메터 확인.
npm install body-parser --save
var pyramid = req.body.id
body 객체 안에 바인딩됨.
var paramId = req.body.id || req.query.id;
POST 에 값이 없으면 GET 값이용.
var express = require('express')
     , http = require('http')
     , path = require('path');

var bodyParser = require('body-parser')
    , static = require('serve-static'); 

var app = express();

app.set('port', process.env.PORT || 3000);

app.use(bodyParser.urlencoded({ extended : false }));

app.use(bodyParser.json());

app.use('public',static(path.join(__dirname,'public');

app.use(function(req,res,next){
     console.log('두 번째 미들웨어 요청');

      var paramId = req.body.id || req.query.id;
      var paramPassword = req.body.password || req.query.password;

      res.writeHead('200',{'Contet-Type':'text/html;charset=utf8'});
      res.write('<h1>Express Server Response Result </h1>');
      res.write('<div>Param id  : ' +  paramId + </div>');
      res.write('<div>Param password : ' + paramPassword + </div>');
      res.end();
}

Route
Express 기능으로 경로로 처리를 맵핑
router.route(요청패스).get()
router.route(요청패스).post()
Route 메소드
get
post
put
delete
all
var router = express.Router();

router.route('process/login/:name').post(function(req,res){
var paramName = req.params.name;

var paramId = req.body.id || req.query.id;
var paramPassword = req.body.password || req.query.password;

res.writeHead('200',{'Contet-Type':'text/html;charset=utf8'});
res.write('<h1>Express Server Response Result </h1>');
res.write('<div>Param id : ' + paramId + </div>');
res.write('<div>Param password : ' +  paramPassword + </div>');
res.end();
}

app.use('/', router);

오류페이지 보여주기
app.all('*', function(req,res) {
     res.status(404).send('<h1>Error</h1>');
}

express-error-handler
npm install express-error-handler --save
var expressErrorHandler = require('express-error-handler');

var error Handler = expressErrorHandler({
static: {
     '404': './public/404.html'
}
});

app.use( expressErrorHandler.httpError(404));
app.use( errorHandler);

쿠키 : cookie-parser
npm install cookie-parser --save
var cookieParser = require('cookie-parser');

app.use(cookieParser);

var route = express.Router();

router.route('/process/showCookie').post(function(req,res){
     res.send(req.cookies);
});

router.route('/process/setUserCookie').post(function(req,res){
       res.cookie('users, {
             id: 'softm',
             name:'김지훈',
             authorized: true
       });

       res.redirect('/process/showCookie');
});

app.use('/', router);


세션 express-session
npm install express-session --save
var cookieParser = require('cookie-parser');
var expressSession = require('express-session');

app.use(cookieParser);
app.use(expressSession({
       secret:'my keys',
       resave: true,
       SaveInitialized:true
});

router.route('/process/login').post(function(req,res){

      var paramId = req.body.id || req.query.id;
      var paramPassword = req.body.password || req.query.password;

if( req.session.user){
     res.redirect('/public/product.html');
} else {
       req.session.user = {
             id: 'softm',
             name:'김지훈',
             authorized: true
       }
}

});
파일업로드 multer

모듈 패턴 -experts객체 속성
users.js
exports.getUser = function(){
      rerurn { id:'test', name:'소냐'};
}
exports.group = { id:'group1', name:'가수'};

module_test.js
var user = require('user1');
user1.getUser().name;
user1.group.name;

UI 라이브러리
http://semantic-ui.com
npm install semantic-ui --save
부트스트랩
타이톤(Titon)

MVC 패턴
익스프레스 뷰엔진
npm install ejs --save
pug 뷰 템플릿 : http://pugjs.org


패스포트 로그인
OAuth 인증 방식
패스포트 미들웨어
npm install passport-local --save
npm install passport --save
npm install connect-flash --save
npm install passport-facebook --save

채팅서버
npm install socket.io --save
npm install cors --save : app.use(cors());

JSON-RPC : Remote Procedure Call
http://www.jsonrpc.org
http://en.wikipedia.org/wiki/JSON-RPC
npm install jayson --save

암호화
http://code.google.com/p/crypto-js
npm install crypto-js --save
모바일 푸시
npm install node-gcm 0 --save











