###### 构造器
```java
public EventPublishingRunListener(SpringApplication application, String[] args) {  
   this.application = application;  
   this.args = args;  
   this.initialMulticaster = new SimpleApplicationEventMulticaster();  
   for (ApplicationListener<?> listener : application.getListeners()) {  
      this.initialMulticaster.addApplicationListener(listener);  
   }  
}
```