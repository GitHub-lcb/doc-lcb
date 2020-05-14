# Java面试指南

## 1.重要的技术点

```java
Redis
	缓存
	数据结构
	分布式锁
	4.0新特性--》限流组件
    
    
public void test(){
    log.info("this is new world");
}
```



## 2.项目突出点

```java
JVM优化
数据库查询优化
bug修复
系统异常处理
```

## 3.代码测试

```java
package com.lcb.demo.web;

import com.lcb.demo.pojo.Param;
import com.lcb.demo.pojo.Result;
import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.PostMapping;
import org.springframework.web.bind.annotation.RequestBody;
import org.springframework.web.bind.annotation.RestController;

import java.util.Map;

@RestController
public class LcbTestController {

    @GetMapping("/test")
    public String test(){
        return "success";
    }

    @PostMapping("/test2")
    public Result test2(@RequestBody Param map){

        Result result = new Result();
        result.setCode(200);
        result.setMsg("success");
        result.setData(map);
        return result;
    }
}

```

