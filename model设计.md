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
          '1': 
          {
           name: '',
           grade: '',
           description: '',
           teachers: [ {/*与登录时teacher基本信息相同*/},{} ],
           exams: ['1','2','3'], 
           homeworks: ['1','2','3']
          },
         '2':     {} , 
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
         1': {
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
