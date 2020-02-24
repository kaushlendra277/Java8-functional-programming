## Use of .collect

```java

Stream.of("zoo".split(""))
      // {z=[z], o=[o, o]}
      // .collect(Collectors.groupingBy(String  :: new))
      // {z=1, o=2}
      //.collect(Collectors.groupingBy(String  :: new, Collectors.counting())); 
      // {z=[z], o=[o, o]}
      // for custom POJOs it is more meaningful
      .collect(Collectors.groupingBy(
						String  :: toLowerCase, 
						Collectors.mapping(String  :: new, Collectors.toList())
						)
					);
```
