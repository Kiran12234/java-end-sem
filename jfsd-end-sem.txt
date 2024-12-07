@Controller
public class GreetingController {
    @RequestMapping("/greet")
    public String greet(@RequestParam("username") String username, Model model) {
        model.addAttribute("message", "Hello, " + username + "!");
        return "greet";
    }
}



@Controller
public class AboutController {
    @RequestMapping("/about")
    public String about() {
        return "about";
    }
}


@Controller
public class Demo1Controller {
    @RequestMapping("/demo1")
    public String demo1(@RequestParam("age") int age, @RequestParam("country") String country, Model model) {
        model.addAttribute("age", age);
        model.addAttribute("country", country);
        return "demo1";
    }
}


@Controller
public class ArithmeticController {
    @RequestMapping("/demo2/{num1}/{num2}")
    public String arithmetic(@PathVariable int num1, @PathVariable int num2, Model model) {
        model.addAttribute("subtraction", num1 - num2);
        model.addAttribute("division", num1 / num2);
        return "arithmetic";
    }
}




@Controller
public class ProductFormController {
    @RequestMapping("/productform")
    public String productForm() {
        return "productform";
    }
}


@Controller
public class MultiplicationController {
    @RequestMapping("/multiplyNumbers")
    public String multiply(@RequestParam("num1") int num1, @RequestParam("num2") int num2, Model model) {
        model.addAttribute("result", num1 * num2);
        return "multiplication";
    }
}



@Controller
public class ReverseController {
    @RequestMapping("/reverse")
    public String reverse(@RequestParam("str1") String str1, @RequestParam("str2") String str2, Model model) {
        model.addAttribute("reversed1", new StringBuilder(str1).reverse().toString());
        model.addAttribute("reversed2", new StringBuilder(str2).reverse().toString());
        return "reverse";
    }
}


@Controller
public class CalculateController {
    @RequestMapping("/calculate")
    public String calculate(@RequestParam("num1") int num1, @RequestParam("num2") int num2, Model model) {
        model.addAttribute("addition", num1 + num2);
        model.addAttribute("subtraction", num1 - num2);
        return "calculate";
    }
}

