# Model 设计

---

## studentInfo

```js
namespace: "student"
state: 
    {
       username: 'sbin'
       type: 'student'
       avatar: 'image url' 
       gender: 'male'
       email: 'xxx@xxx.com'
       gitId: '',
       number: '141250106', 
       courses: ['1','2','3']
    }
```

## courseInfo

```js
namespace: 'course' 
state: 
    {
      course_list: 
        { 
          '1': {
           name: '',
           grade: '',
           description: '',
           teachers: [ {/*与登录时teacher基本信息相同*/},{} ],
           exams: ['1','2','3'], 
           homeworks: ['1','2','3']
          },
         '2': {} , 
         '3': {}
       }
     }
```

## examInfo

```js
namespace: 'exam', 
state: 
    {
      exam_list:
       {
         '1': {
           title: '软工二考试',
           description: 'string',
           startAt: 'yyyy-MM-dd hh:mm:ss', 
           endAt: 'yyyy-MM-dd hh:mm:ss', 
           isStarted: 'true',
           isEnd: 'false',
           gitInitStatus:'fail'|'success'|'notBegun'|'undergoing',
           questions: ['1','2','3']         },
       }
    }

```

## homeworkInfo

>与examInfo保持一致


## questionInfo 

```js
namespace: 'question', 
state: {
    question_list: { 
        '1': {
            question:{
               id: 123
               title: 'string', 
               description: 'string',
               type: '编程题',
            } 
            //以下三项若为空,则显示为分析中,前端自行判断
            score: 10, 
            scoreReportUrl: 'url', 
            analysisReportUrl: 'url'          },         '2': {},         '3': {}     }}
```