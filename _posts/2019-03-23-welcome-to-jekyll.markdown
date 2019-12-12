---
layout: Chuyên Mục của tui
title:  "lap trinh java web"
date:   ‎12-‎Dec-‎19 5:52:48 PM tại your tv
categories: Spring MVC, Spring Boot
---
đây là đoạn code demo thôi
```javascript
@Controller
public class RegistrationController {
  @Autowired
  public UserService userService;
  @RequestMapping(value = "/register", method = RequestMethod.GET)
  public ModelAndView showRegister(HttpServletRequest request, HttpServletResponse response) {
    ModelAndView mav = new ModelAndView("register");
    mav.addObject("user", new User());
    return mav;
  }
  @RequestMapping(value = "/registerProcess", method = RequestMethod.POST)
  public ModelAndView addUser(HttpServletRequest request, HttpServletResponse response,
  @ModelAttribute("user") User user) {
  userService.register(user);
  return new ModelAndView("welcome", "firstname", user.getFirstname());
  }
}
```

Tác giả [link lam cv][link-lam-cv] .Check out the [Jekyll docs][jekyll-docs] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll Talk][jekyll-talk].

[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
[link-lam-cv]: https://viblo.asia/p/hoc-va-lam-website-trong-vong-30-phut-voi-github-YWOZrzMyZQ0

