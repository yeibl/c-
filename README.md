# 知识点

开发过程中遇到的问题，解决方案，知识点的记录

## 1、.net core  vscode 模板生成
### a、安装 dotnet tool install --global dotnet-aspnet-codegenerator --version 2.2.3 
### b、dotnet aspnet-codegenerator controller -name  TeacherLession  -actions -outDir Areas/SystemAdmin/Controllers

## 2、.net core linq partition by 实现
```
lessions.GroupBy(g => new { g.subject_id, g.class_id, g.teacher_id })
.SelectMany(s =>s.Select((j, i) => new { j.teacher_id, j.teacher_name, rn = i + 1 })).Where(p => p.rn == 1).ToList();
```

## 3、mongo db  query
```
db.getCollection('ErrorLog').find({$and:[{"logTime":{$gte:ISODate("2019-12-10")}},{"ex":/韬/}]})
```


