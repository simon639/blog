*abc*

```java
@SpringBootApplication
    public class DemoApplication implements CommandLineRunner {
    private static final Logger log = LoggerFactory.getLogger(DemoApplication.class);

    public static void main(String[] args) {
	SpringApplicationBuilder builder = new SpringApplicationBuilder(DemoApplication.class);
	if (args.length > 0 && "runserver".equals(args[0])) {
	    System.out.println("runserver");
	} else {
	    builder.web(WebApplicationType.NONE);
	}
	builder.run(args);
    }

        @Override
	public void run(String... args) {
	    System.out.println("Done");
	}
}
```
