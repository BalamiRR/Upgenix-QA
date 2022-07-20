# Upgenix-QA
Automating the Upgenix browser
<p align="left"> 

<a href="https://www.java.com" target="_blank" rel="noreferrer"> 
  <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/java/java-original.svg" alt="java" width="60" height="60"/> 
</a> 

<a href="https://www.selenium.dev" target="_blank" rel="noreferrer">
  <img src="https://selenium.dev/images/selenium_logo_square_green.png" alt="selenium" width="60" height="60"/> 
</a>    

<a href="https://www.oracle.com/" target="_blank" rel="noreferrer"> 
  <img src="https://lisacrispin.com/wp-content/uploads/2019/01/Screen-Shot-2019-01-17-at-12.13.33-PM.png" alt="oracle" width="60" height="60"/> 
</a>

<a href="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSPEOYG6Ap6vFoqv5bNXkDvnCa1yAqbDr_f_YQhXa97QwYXvNqWIvnCzpFJJz1ZwcLrwbM&usqp=CAU" rel="noreferrer">
  <img src="https://www.codeaffine.com/wp-content/uploads/2016/02/junit-lambda.png" width="115" height="60"/> 
</a> 
<a href="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSPEOYG6Ap6vFoqv5bNXkDvnCa1yAqbDr_f_YQhXa97QwYXvNqWIvnCzpFJJz1ZwcLrwbM&usqp=CAU" rel="noreferrer">
  <img src="https://i0.wp.com/invotra.com/wp-content/uploads/2019/09/jira_software_logo-e1571063680300.png?fit=768%2C216&ssl=1" width="150" height="60"/> 
</a> 
</p>


### selenium-cucumber-java

This repository contains a collection of sample `Upgenix-QA` projects and libraries that demonstrate how to
use the tool and develop automation script using the Cucumber BDD framework with Java as programming language.
It generate JSON, HTML and Txt reporters as well. It also generate `screen shots` for your tests if you enable it and
also generate `error shots` for your failed test cases as well.

### Installation (pre-requisites)

1. JDK 1.8+ 
2. Maven 
3. IntelliJ
4. IntelliJ Plugins for
    - Maven
    - Cucumber
5. Browser driver (make sure you have your desired browser driver and class path is set)

### Framework set up

Git:

    git clone https://github.com/BalamiRR/Upgenix-QA.git
 
Manually :

Fork / Clone repository from [here](https://github.com/BalamiRR/Upgenix-QA/archive/main.zip) or download zip and set
it up in your local workspace.



### Using canned test in the project:


```
import io.cucumber.junit.Cucumber;
import io.cucumber.junit.CucumberOptions;
import org.junit.runner.RunWith;

@RunWith(Cucumber.class)
@CucumberOptions(
    plugin = {
        "html:target/cucumber-reports.html",
        "json:target/cucumber.json",
        "rerun:target/rerun.txt",
        "me.jvt.cucumber.report.PrettyReports:target/cucumber"
    },
    features = "src/main/resources/features",
    glue = "com/upgenix/step_definitions",
    dryRun = false,
    tags = "@LogOut"
)
public class CukesRunner {



}
```
