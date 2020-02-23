## Use of .collect

```java

Stream.of("zoo".split(""))
      // {z=[z], o=[o, o]}
      // .collect(Collectors.groupingBy(String  :: new))
      // {z=1, o=2}
      .collect(Collectors.groupingBy(String  :: new, Collectors.counting())); 
      
```
