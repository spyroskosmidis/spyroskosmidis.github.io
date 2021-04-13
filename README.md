Welcome to the R tutorial page!
<!DOCTYPE html>

<html xmlns="http://www.w3.org/1999/xhtml">

<head>

<meta charset="utf-8">
<meta http-equiv="Content-Type" content="text/html; charset=utf-8" />
<meta name="generator" content="pandoc" />



<meta name="progressive" content="false" />
<meta name="allow-skip" content="false" />

<title>Oxford R Tutorial</title>


<!-- highlightjs -->
<style type="text/css">code{white-space: pre;}</style>
<style type="text/css">
  pre:not([class]) {
    background-color: white;
  }
</style>
<script type="text/javascript">
if (window.hljs) {
  hljs.configure({languages: []});
  hljs.initHighlightingOnLoad();
  if (document.readyState && document.readyState === "complete") {
    window.setTimeout(function() { hljs.initHighlighting(); }, 0);
  }
}
</script>

<!-- taken from https://github.com/rstudio/rmarkdown/blob/67b7f5fc779e4cfdfd0f021d3d7745b6b6e17149/inst/rmd/h/default.html#L296-L362 -->
<!-- tabsets -->

<style type="text/css">
.tabset-dropdown > .nav-tabs {
  display: inline-table;
  max-height: 500px;
  min-height: 44px;
  overflow-y: auto;
  background: white;
  border: 1px solid #ddd;
  border-radius: 4px;
}

.tabset-dropdown > .nav-tabs > li.active:before {
  content: "";
  font-family: 'Glyphicons Halflings';
  display: inline-block;
  padding: 10px;
  border-right: 1px solid #ddd;
}

.tabset-dropdown > .nav-tabs.nav-tabs-open > li.active:before {
  content: "&#xe258;";
  border: none;
}

.tabset-dropdown > .nav-tabs.nav-tabs-open:before {
  content: "";
  font-family: 'Glyphicons Halflings';
  display: inline-block;
  padding: 10px;
  border-right: 1px solid #ddd;
}

.tabset-dropdown > .nav-tabs > li.active {
  display: block;
}

.tabset-dropdown > .nav-tabs > li > a,
.tabset-dropdown > .nav-tabs > li > a:focus,
.tabset-dropdown > .nav-tabs > li > a:hover {
  border: none;
  display: inline-block;
  border-radius: 4px;
}

.tabset-dropdown > .nav-tabs.nav-tabs-open > li {
  display: block;
  float: none;
}

.tabset-dropdown > .nav-tabs > li {
  display: none;
}
</style>

<script>
$(document).ready(function () {
  window.buildTabsets("section-TOC");
});

$(document).ready(function () {
  $('.tabset-dropdown > .nav-tabs > li').click(function () {
    $(this).parent().toggleClass('nav-tabs-open')
  });
});
</script>
<!-- end tabsets -->



</head>

<body>



<div class="pageContent band">
<div class="bandContent page">

<div class="topics">

<div id="section-basic-r" class="section level2">
<h2>Basic R</h2>
<p>Dear Students,</p>
<p>Those not familiar with R and RStudio might benefit from the information below!</p>
<p>R is a free statistical software that is used for all levels of statistical analysis and RStudio is a very useful interface for R. If you want to use R and Rstudio in your computer you should download the latest versions from the following website.</p>
<p><a href="https://www.rstudio.com/products/rstudio/download/" class="uri">https://www.rstudio.com/products/rstudio/download/</a></p>
<p>and for R click here:</p>
<p><a href="https://www.r-project.org/" class="uri">https://www.r-project.org/</a></p>
<p><strong>R Capabilities</strong></p>
<p>R can do a number of jobs ranging from simple algebraic calculations to advanced level simulations.</p>
<p>Here is a simple example to see how R can be used to do simple calculations!</p>
<div id="section-r-as-a-calculator-i" class="section level3">
<h3>R as a calculator I</h3>
<p>Write the R code required to add two plus two:</p>
<div class="tutorial-exercise" data-label="two-plus-two" data-caption="Code" data-completion="1" data-diagnostics="1" data-startover="1" data-lines="0">
<script type="application/json" data-opts-chunk="1">{"fig.width":6.5,"fig.height":4,"fig.retina":2,"fig.align":"default","fig.keep":"high","fig.show":"asis","out.width":624,"warning":true,"error":false,"message":true,"exercise.df_print":"paged","exercise.checker":"NULL"}</script>
</div>
</div>
<div id="section-r-as-a-calculator-ii" class="section level3">
<h3>R as a calculator II</h3>
<p>Can you find the answer for the following equation?</p>
<p><span class="math display">\[(17+(6*2))/29\]</span>:</p>
<div class="tutorial-exercise" data-label="with_brackets" data-caption="Code" data-completion="1" data-diagnostics="1" data-startover="1" data-lines="0">
<script type="application/json" data-opts-chunk="1">{"fig.width":6.5,"fig.height":4,"fig.retina":2,"fig.align":"default","fig.keep":"high","fig.show":"asis","out.width":624,"warning":true,"error":false,"message":true,"exercise.df_print":"paged","exercise.checker":"NULL"}</script>
</div>
</div>
<div id="section-understanding-objects" class="section level3">
<h3>Understanding objects!</h3>
<p>In R most pieces of information are stored what we call <strong>objects</strong>. For example you can create an <strong>object</strong> that contains the information from the previous equation.</p>
<p><span class="math display">\[(17+(6*2))/29\]</span></p>
<p>By typing the name of the object (which can be given whatever name you think is suitable), you should be getting the result of the equation</p>
<pre class="r"><code>object.eq &lt;- (17+(6*2))/29
object.eq</code></pre>
<pre><code>## [1] 1</code></pre>
<p>The content of an object does not need to be numeric;</p>
<pre class="r"><code>one&lt;-&quot;I&quot;
two&lt;-&quot;love&quot;
three&lt;- &quot;Oxford&quot;

one </code></pre>
<pre><code>## [1] &quot;I&quot;</code></pre>
<pre class="r"><code>two</code></pre>
<pre><code>## [1] &quot;love&quot;</code></pre>
<pre class="r"><code>three</code></pre>
<pre><code>## [1] &quot;Oxford&quot;</code></pre>
<p>We could make that look a bit better by typing cbind(one, two, three)!</p>
<pre class="r"><code>cbind(one, two, three)</code></pre>
<pre><code>##      one two    three   
## [1,] &quot;I&quot; &quot;love&quot; &quot;Oxford&quot;</code></pre>
<p>Give it a go!</p>
<p>Create an object that contains an equation that equals 5 (2+3, 1+4, 1*5, 10/2 etc). Feel free to call it whatever you want</p>
<div class="tutorial-exercise" data-label="with_brackets_one" data-caption="Code" data-completion="1" data-diagnostics="1" data-startover="1" data-lines="0">
<script type="application/json" data-opts-chunk="1">{"fig.width":6.5,"fig.height":4,"fig.retina":2,"fig.align":"default","fig.keep":"high","fig.show":"asis","out.width":624,"warning":true,"error":false,"message":true,"exercise.df_print":"paged","exercise.checker":"NULL"}</script>
</div>
<p>Now, replicate what I did with the <em>I love Oxford</em> example above, but this time write My name is <em>yourname</em></p>
<div class="tutorial-exercise" data-label="non-numeric" data-caption="Code" data-completion="1" data-diagnostics="1" data-startover="1" data-lines="0">
<script type="application/json" data-opts-chunk="1">{"fig.width":6.5,"fig.height":4,"fig.retina":2,"fig.align":"default","fig.keep":"high","fig.show":"asis","out.width":624,"warning":true,"error":false,"message":true,"exercise.df_print":"paged","exercise.checker":"NULL"}</script>
</div>
</div>
<div id="section-creating-a-data.frame" class="section level3">
<h3>Creating a data.frame</h3>
<p>For most of your work you will be analysing datasets created by others. But R can also be used as an Excel file.</p>
<p>For example, if you want to create to columns of data that contain information for 5 rows the following code should do the trick:</p>
<pre class="r"><code>col.one&lt;-c(4,8,16,20,21)
col.two&lt;-c(3,2,18,22,36)


col.one</code></pre>
<pre><code>## [1]  4  8 16 20 21</code></pre>
<pre class="r"><code>col.two</code></pre>
<pre><code>## [1]  3  2 18 22 36</code></pre>
<p>With the following code you can put it together in a single data.frame called df (or whatever you think it should be called)</p>
<pre class="r"><code>df&lt;- as.data.frame(cbind(col.one, col.two))



#You can print the data in your console
print(df)</code></pre>
<pre><code>##   col.one col.two
## 1       4       3
## 2       8       2
## 3      16      18
## 4      20      22
## 5      21      36</code></pre>
<pre class="r"><code>df</code></pre>
<div data-pagedtable="false">
<script data-pagedtable-source type="application/json">
{"columns":[{"label":["col.one"],"name":[1],"type":["dbl"],"align":["right"]},{"label":["col.two"],"name":[2],"type":["dbl"],"align":["right"]}],"data":[{"1":"4","2":"3"},{"1":"8","2":"2"},{"1":"16","2":"18"},{"1":"20","2":"22"},{"1":"21","2":"36"}],"options":{"columns":{"min":{},"max":[10]},"rows":{"min":[10],"max":[10]},"pages":{}}}
  </script>
</div>
<pre class="r"><code>#If you are on RStudio you can double click the data in the Global Environment. A spreadsheet will open!</code></pre>
<p>Say now you are interested in some summary information. What is the mean of these variables?</p>
<pre class="r"><code>mean(df$col.one)</code></pre>
<pre><code>## [1] 13.8</code></pre>
<pre class="r"><code>##and check manually

meanofcolone&lt;-(4+8+16+20+21)/5
meanofcolone</code></pre>
<pre><code>## [1] 13.8</code></pre>
<p>Where did the df$col.one come from? Well, when you are dealing with a data frame in R you need to tell it which variable to choose for the analysis. The above for example tells R; go to the data frame called <em>df</em> and pick the variable/column <em>col.one</em></p>
<p>Can you do the same with <em>col.two</em>? No need to do the manual check!</p>
<div class="tutorial-exercise" data-label="col_two_ex" data-caption="Code" data-completion="1" data-diagnostics="1" data-startover="1" data-lines="0">
<script type="application/json" data-opts-chunk="1">{"fig.width":6.5,"fig.height":4,"fig.retina":2,"fig.align":"default","fig.keep":"high","fig.show":"asis","out.width":624,"warning":true,"error":false,"message":true,"exercise.df_print":"paged","exercise.checker":"NULL"}</script>
</div>
<div class="tutorial-exercise-support" data-label="col_two_ex-solution" data-caption="Code" data-completion="1" data-diagnostics="1" data-startover="1" data-lines="0">
<pre class="text"><code>mean(df$col.two)</code></pre>
</div>
<p>There is a handy function in R that can give you additional information:</p>
<pre class="r"><code>summary(df$col.two)</code></pre>
<pre><code>##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
##     2.0     3.0    18.0    16.2    22.0    36.0</code></pre>
<p>The <em>summary</em> command show you the min/max, the media and 25th and 75th percentile data point. If you need more information about your data, <em>var</em> and <em>sd</em> can be used to get the variance and the standard deviation of the variables!</p>
<p>Now that you have a better understanding of how R operates let’s try and find information that is not readily available. For example what is the value of col.one in the second row?</p>
<pre class="r"><code>df[2,1]</code></pre>
<pre><code>## [1] 8</code></pre>
<p>For example what is the value of col.one in the second and third row?</p>
<pre class="r"><code>df[c(2,3),1]</code></pre>
<pre><code>## [1]  8 16</code></pre>
<p>What if we are interested in the second column (and still second row)?</p>
<pre class="r"><code>df[2,2]</code></pre>
<pre><code>## [1] 2</code></pre>
<p>You can check again to make sure you got this right:</p>
<pre class="r"><code>df</code></pre>
<div data-pagedtable="false">
<script data-pagedtable-source type="application/json">
{"columns":[{"label":["col.one"],"name":[1],"type":["dbl"],"align":["right"]},{"label":["col.two"],"name":[2],"type":["dbl"],"align":["right"]}],"data":[{"1":"4","2":"3"},{"1":"8","2":"2"},{"1":"16","2":"18"},{"1":"20","2":"22"},{"1":"21","2":"36"}],"options":{"columns":{"min":{},"max":[10]},"rows":{"min":[10],"max":[10]},"pages":{}}}
  </script>
</div>
<p>The logic is fairly simple. For a data.frame <em>df</em> the brackets allow you to check specific dimensions. Within brackets the rows come first and then come the columns. In other words, df[1,2], will give you the first row of the second column. HINT: A good way to remember this is to think of [Ray, Charles] (or [Rows, Columns]).</p>
<p>Try the following:</p>
<p>What are the values in the 5th row of columns one and two?</p>
<div class="tutorial-exercise" data-label="col_two_two" data-caption="Code" data-completion="1" data-diagnostics="1" data-startover="1" data-lines="0">
<script type="application/json" data-opts-chunk="1">{"fig.width":6.5,"fig.height":4,"fig.retina":2,"fig.align":"default","fig.keep":"high","fig.show":"asis","out.width":624,"warning":true,"error":false,"message":true,"exercise.df_print":"paged","exercise.checker":"NULL"}</script>
</div>
<div class="tutorial-exercise-support" data-label="col_two_two-solution" data-caption="Code" data-completion="1" data-diagnostics="1" data-startover="1" data-lines="0">
<pre class="text"><code>df[5,c(1,2)]</code></pre>
</div>
</div>
</div>
<div id="section-relationships" class="section level2">
<h2>Relationships</h2>
<p>Let’s start thinking about statistical relationships (without entering the discussion about estimators or statistical theory).</p>
<p>Let’s plot the two variables we created</p>
<pre class="r"><code>plot(df$col.one, df$col.two)</code></pre>
<p><img src="LearningR_files/figure-html/unnamed-chunk-12-1.png" width="624" /></p>
<p>Now let’s try and estimate the relationship using OLS regression. What do you think? Can we fit a line in the above scatterplot?</p>
<p>Let’s plot the two variables we created</p>
<pre class="r"><code>first.ols&lt;-lm(df$col.two~df$col.one)
summary(first.ols)</code></pre>
<pre><code>## 
## Call:
## lm(formula = df$col.two ~ df$col.one)
## 
## Residuals:
##      1      2      3      4      5 
##  3.985 -4.029 -2.058 -5.072  7.174 
## 
## Coefficients:
##             Estimate Std. Error t value Pr(&gt;|t|)  
## (Intercept)  -7.9991     6.2955  -1.271   0.2935  
## df$col.one    1.7536     0.4103   4.274   0.0235 *
## ---
## Signif. codes:  0 &#39;***&#39; 0.001 &#39;**&#39; 0.01 &#39;*&#39; 0.05 &#39;.&#39; 0.1 &#39; &#39; 1
## 
## Residual standard error: 6.152 on 3 degrees of freedom
## Multiple R-squared:  0.8589, Adjusted R-squared:  0.8119 
## F-statistic: 18.26 on 1 and 3 DF,  p-value: 0.02352</code></pre>
<pre class="r"><code>#Note that you might also see this written as follows

first.ols.alt&lt;-lm(col.two~col.one, data=df)
summary(first.ols.alt)</code></pre>
<pre><code>## 
## Call:
## lm(formula = col.two ~ col.one, data = df)
## 
## Residuals:
##      1      2      3      4      5 
##  3.985 -4.029 -2.058 -5.072  7.174 
## 
## Coefficients:
##             Estimate Std. Error t value Pr(&gt;|t|)  
## (Intercept)  -7.9991     6.2955  -1.271   0.2935  
## col.one       1.7536     0.4103   4.274   0.0235 *
## ---
## Signif. codes:  0 &#39;***&#39; 0.001 &#39;**&#39; 0.01 &#39;*&#39; 0.05 &#39;.&#39; 0.1 &#39; &#39; 1
## 
## Residual standard error: 6.152 on 3 degrees of freedom
## Multiple R-squared:  0.8589, Adjusted R-squared:  0.8119 
## F-statistic: 18.26 on 1 and 3 DF,  p-value: 0.02352</code></pre>
<p>So here is your first OLS model. It does not make a lot of sense when you look at the results, but it generally shouldn’t as it is a small number of random numbers. BUt what you should learn from this is the general infrastructure of the code.</p>
<ol style="list-style-type: decimal">
<li>We store our model in an object that contains the command</li>
<li>The command tells R which estimator to use (lm in our case stands for linear model)</li>
<li>The DV variable is placed on the left hand side and the independent variable is placed on the right hand side. The two variables are connected by <strong>~</strong>.</li>
</ol>
<p>If you have additional independent variables you add it with a plus sign. Say for example that I have a third column (or variable).</p>
<pre class="r"><code>col.three&lt;- c(5,9,21, 5,22)

#connect it to the original data.frame
df= cbind(df, col.three)

#Check everything has worked
df</code></pre>
<div data-pagedtable="false">
<script data-pagedtable-source type="application/json">
{"columns":[{"label":["col.one"],"name":[1],"type":["dbl"],"align":["right"]},{"label":["col.two"],"name":[2],"type":["dbl"],"align":["right"]},{"label":["col.three"],"name":[3],"type":["dbl"],"align":["right"]}],"data":[{"1":"4","2":"3","3":"5"},{"1":"8","2":"2","3":"9"},{"1":"16","2":"18","3":"21"},{"1":"20","2":"22","3":"5"},{"1":"21","2":"36","3":"22"}],"options":{"columns":{"min":{},"max":[10]},"rows":{"min":[10],"max":[10]},"pages":{}}}
  </script>
</div>
<pre class="r"><code>#Estimate

first.ols&lt;-lm(df$col.one~df$col.two+ df$col.three)
summary(first.ols)</code></pre>
<pre><code>## 
## Call:
## lm(formula = df$col.one ~ df$col.two + df$col.three)
## 
## Residuals:
##      1      2      3      4      5 
## -3.567  1.358  2.103  2.404 -2.299 
## 
## Coefficients:
##              Estimate Std. Error t value Pr(&gt;|t|)  
## (Intercept)   6.47907    3.36350   1.926   0.1939  
## df$col.two    0.52786    0.17820   2.962   0.0976 .
## df$col.three -0.09922    0.29831  -0.333   0.7710  
## ---
## Signif. codes:  0 &#39;***&#39; 0.001 &#39;**&#39; 0.01 &#39;*&#39; 0.05 &#39;.&#39; 0.1 &#39; &#39; 1
## 
## Residual standard error: 3.876 on 2 degrees of freedom
## Multiple R-squared:  0.8663, Adjusted R-squared:  0.7326 
## F-statistic:  6.48 on 2 and 2 DF,  p-value: 0.1337</code></pre>
</div>
<div id="section-packages" class="section level2">
<h2>Packages</h2>
<p>One of the key features of R is that it is based on user written packages. These packages need to be installed and loaded. You should install these packages once, but then load them every time you revisit your project. Let’s do a very basic example of how this works.In your own machines don’t add the # key before the command!</p>
<pre class="r"><code>#The following installs ggplot2 which is a prominent plotting package
#install.packages(&quot;ggplot2&quot;)
#Once it is installed, you load it in the following way:
library(ggplot2)</code></pre>
<p>Once a package is loaded you can use it. R comes with a help function (help(ggplot2)), though most of the help will come from searching the web. Try to install and load a different package called swirl.</p>
<div class="tutorial-exercise" data-label="swirl" data-caption="Code" data-completion="1" data-diagnostics="1" data-startover="1" data-lines="0">
<script type="application/json" data-opts-chunk="1">{"fig.width":6.5,"fig.height":4,"fig.retina":2,"fig.align":"default","fig.keep":"high","fig.show":"asis","out.width":624,"warning":true,"error":false,"message":true,"exercise.df_print":"paged","exercise.checker":"NULL"}</script>
</div>
<div class="tutorial-exercise-support" data-label="swirl-solution" data-caption="Code" data-completion="1" data-diagnostics="1" data-startover="1" data-lines="0">
<pre class="text"><code>install.packages(&quot;swirl&quot;)
library(swirl)</code></pre>
</div>
<p><em>swirl</em> can in fact be a very useful resource for learning! Check it out when you get the time! But since we opened the <em>ggplot2</em> door it would be nice to see what it does.</p>
<pre class="r"><code>ggplot(df, aes(x=col.one, y=col.two)) + 
  geom_point()+
  geom_smooth(method=lm)</code></pre>
<pre><code>## `geom_smooth()` using formula &#39;y ~ x&#39;</code></pre>
<p><img src="LearningR_files/figure-html/unnamed-chunk-16-1.png" width="624" /> You could elaborate on the basic ggplot plot</p>
<pre class="r"><code>ggplot(df, aes(x=col.one, y=col.two)) + 
  geom_point()+
  geom_smooth(method=lm, col=&quot;red&quot;)+ ylab(&quot;Y&quot;)+ xlab(&quot;X&quot;)+theme_bw()</code></pre>
<pre><code>## `geom_smooth()` using formula &#39;y ~ x&#39;</code></pre>
<p><img src="LearningR_files/figure-html/unnamed-chunk-17-1.png" width="624" /></p>
</div>
<div id="section-loading-data" class="section level2">
<h2>Loading data</h2>
<p>So far we have assumed that you create the data yourself. Often times this is not the case. Say or example that you want to load a dataset that is stored in your personal computer. I think it is good practice to set the working directory</p>
<p><em>setwd(/users/etcetc)</em> is the basic command to do this. If you find this difficult you can always click on Session&gt;Set Working Directory and then set the directory manually. It is good practice to copy and paste what appear in the console to your syntax.</p>
<p>Once you have done this, you need to figure out what type of data you will be importing in RStudio. You have a number of options here and perhaps the most convenient way is to File&gt;Import Dataset and follow the instructions. As always try to copy and paste the code to your script so that you can quickly run the code the next time you are working on the project.</p>
<p>Let’s do a quick example here with a .csv file</p>
<p>The command to open a .csv file that is stored in your working directory is <em>read.csv(“name_of_file.csv”)</em>. Note that you could have the full extension there and avoid the <em>setwd</em> route. But, again, in your first R sessions using the interface is probably the best decision.</p>
</div>
<div id="section-quiz" class="section level2">
<h2>Quiz</h2>
<p>Just to have a bit fof fun andd make sure you have understood the basics of R, here is a -very- easy quiz for you.</p>
<p><div class="panel-heading tutorial-quiz-title">Quiz</div><div class="panel panel-default">
<div data-label="quiz-1" class="tutorial-question panel-body">
<div id="quiz-1-answer_container" class="shiny-html-output"></div>
<div id="quiz-1-message_container" class="shiny-html-output"></div>
<div id="quiz-1-action_button_container" class="shiny-html-output"></div>
<script>if (Tutorial.triggerMathJax) Tutorial.triggerMathJax()</script>
</div>
</div><div class="panel panel-default">
<div data-label="quiz-2" class="tutorial-question panel-body">
<div id="quiz-2-answer_container" class="shiny-html-output"></div>
<div id="quiz-2-message_container" class="shiny-html-output"></div>
<div id="quiz-2-action_button_container" class="shiny-html-output"></div>
<script>if (Tutorial.triggerMathJax) Tutorial.triggerMathJax()</script>
</div>
</div><div class="panel panel-default">
<div data-label="quiz-3" class="tutorial-question panel-body">
<div id="quiz-3-answer_container" class="shiny-html-output"></div>
<div id="quiz-3-message_container" class="shiny-html-output"></div>
<div id="quiz-3-action_button_container" class="shiny-html-output"></div>
<script>if (Tutorial.triggerMathJax) Tutorial.triggerMathJax()</script>
</div>
</div></p>

<script type="application/shiny-prerendered" data-context="server-start">
library(learnr)
knitr::opts_chunk$set(echo = FALSE)
</script>
 
<script type="application/shiny-prerendered" data-context="server">
learnr:::register_http_handlers(session, metadata = NULL)
</script>
 
<script type="application/shiny-prerendered" data-context="server">
session$onSessionEnded(function() {
        learnr:::session_stop_event(session)
      })
</script>
 
<script type="application/shiny-prerendered" data-context="server">
`tutorial-exercise-two-plus-two-result` <- learnr:::setup_exercise_handler(reactive(req(input$`tutorial-exercise-two-plus-two-code-editor`)), session)
output$`tutorial-exercise-two-plus-two-output` <- renderUI({
  `tutorial-exercise-two-plus-two-result`()
})
</script>
 
<script type="application/shiny-prerendered" data-context="server">
`tutorial-exercise-with_brackets-result` <- learnr:::setup_exercise_handler(reactive(req(input$`tutorial-exercise-with_brackets-code-editor`)), session)
output$`tutorial-exercise-with_brackets-output` <- renderUI({
  `tutorial-exercise-with_brackets-result`()
})
</script>
 
<script type="application/shiny-prerendered" data-context="server">
`tutorial-exercise-with_brackets_one-result` <- learnr:::setup_exercise_handler(reactive(req(input$`tutorial-exercise-with_brackets_one-code-editor`)), session)
output$`tutorial-exercise-with_brackets_one-output` <- renderUI({
  `tutorial-exercise-with_brackets_one-result`()
})
</script>
 
<script type="application/shiny-prerendered" data-context="server">
`tutorial-exercise-non-numeric-result` <- learnr:::setup_exercise_handler(reactive(req(input$`tutorial-exercise-non-numeric-code-editor`)), session)
output$`tutorial-exercise-non-numeric-output` <- renderUI({
  `tutorial-exercise-non-numeric-result`()
})
</script>
 
<script type="application/shiny-prerendered" data-context="server">
`tutorial-exercise-col_two_ex-result` <- learnr:::setup_exercise_handler(reactive(req(input$`tutorial-exercise-col_two_ex-code-editor`)), session)
output$`tutorial-exercise-col_two_ex-output` <- renderUI({
  `tutorial-exercise-col_two_ex-result`()
})
</script>
 
<script type="application/shiny-prerendered" data-context="server">
`tutorial-exercise-col_two_two-result` <- learnr:::setup_exercise_handler(reactive(req(input$`tutorial-exercise-col_two_two-code-editor`)), session)
output$`tutorial-exercise-col_two_two-output` <- renderUI({
  `tutorial-exercise-col_two_two-result`()
})
</script>
 
<script type="application/shiny-prerendered" data-context="server">
`tutorial-exercise-swirl-result` <- learnr:::setup_exercise_handler(reactive(req(input$`tutorial-exercise-swirl-code-editor`)), session)
output$`tutorial-exercise-swirl-output` <- renderUI({
  `tutorial-exercise-swirl-result`()
})
</script>
 
<script type="application/shiny-prerendered" data-context="server">
learnr:::question_prerendered_chunk(structure(list(type = "learnr_radio", label = "quiz-1", question = structure("Say one wants to get the median value of col.one. Which of the following is the correct command?", html = TRUE, class = c("html", "character")), answers = list(structure(list(id = "lnr_ans_5546218",     option = "summary(col.one)", value = "summary(col.one)",     label = structure("summary(col.one)", html = TRUE, class = c("html",     "character")), correct = FALSE, message = NULL), class = c("tutorial_question_answer", "tutorial_quiz_answer")), structure(list(id = "lnr_ans_34c1730",     option = "mean(df$col.one", value = "mean(df$col.one", label = structure("mean(df$col.one", html = TRUE, class = c("html",     "character")), correct = FALSE, message = NULL), class = c("tutorial_question_answer", "tutorial_quiz_answer")), structure(list(id = "lnr_ans_62dc919",     option = "summary(df$col.one)", value = "summary(df$col.one)",     label = structure("summary(df$col.one)", html = TRUE, class = c("html",     "character")), correct = TRUE, message = NULL), class = c("tutorial_question_answer", "tutorial_quiz_answer")), structure(list(id = "lnr_ans_31153c3",     option = "sd(col.one)", value = "sd(col.one)", label = structure("sd(col.one)", html = TRUE, class = c("html",     "character")), correct = FALSE, message = NULL), class = c("tutorial_question_answer", "tutorial_quiz_answer"))), button_labels = list(submit = structure("Submit Answer", html = TRUE, class = c("html", "character")), try_again = structure("Try Again", html = TRUE, class = c("html", "character"))), messages = list(correct = structure("Correct!", html = TRUE, class = c("html", "character")), try_again = structure("Incorrect", html = TRUE, class = c("html", "character")), incorrect = structure("Incorrect", html = TRUE, class = c("html", "character")), message = NULL, post_message = NULL), ids = list(    answer = "quiz-1-answer", question = "quiz-1"), loading = structure("<strong>Loading:<\u002fstrong> \nSay one wants to get the median value of col.one. Which of the following is the correct command?\n<br/><br/><br/>", html = TRUE, class = c("html", "character")), random_answer_order = FALSE, allow_retry = FALSE,     seed = 46126611.4785206, options = list()), class = c("learnr_radio", "tutorial_question")))
</script>
 
<script type="application/shiny-prerendered" data-context="server">
learnr:::question_prerendered_chunk(structure(list(type = "learnr_radio", label = "quiz-2", question = structure("Which of the R packages listed below are used to create plots?", html = TRUE, class = c("html", "character")), answers = list(structure(list(id = "lnr_ans_21b375",     option = "ggplot", value = "ggplot", label = structure("ggplot", html = TRUE, class = c("html",     "character")), correct = TRUE, message = NULL), class = c("tutorial_question_answer", "tutorial_quiz_answer")), structure(list(id = "lnr_ans_5ed0d91",     option = "tools", value = "tools", label = structure("tools", html = TRUE, class = c("html",     "character")), correct = FALSE, message = NULL), class = c("tutorial_question_answer", "tutorial_quiz_answer")), structure(list(id = "lnr_ans_74eed1a",     option = "stats", value = "stats", label = structure("stats", html = TRUE, class = c("html",     "character")), correct = FALSE, message = NULL), class = c("tutorial_question_answer", "tutorial_quiz_answer"))), button_labels = list(submit = structure("Submit Answer", html = TRUE, class = c("html", "character")), try_again = structure("Try Again", html = TRUE, class = c("html", "character"))), messages = list(correct = structure("Correct!", html = TRUE, class = c("html", "character")), try_again = structure("Incorrect", html = TRUE, class = c("html", "character")), incorrect = structure("Incorrect", html = TRUE, class = c("html", "character")), message = NULL, post_message = NULL), ids = list(    answer = "quiz-2-answer", question = "quiz-2"), loading = structure("<strong>Loading:<\u002fstrong> \nWhich of the R packages listed below are used to create plots?\n<br/><br/><br/>", html = TRUE, class = c("html", "character")), random_answer_order = FALSE, allow_retry = FALSE,     seed = 649838266.197395, options = list()), class = c("learnr_radio", "tutorial_question")))
</script>
 
<script type="application/shiny-prerendered" data-context="server">
learnr:::question_prerendered_chunk(structure(list(type = "learnr_checkbox", label = "quiz-3", question = structure("Which of the following get the 4th observation of col.three", html = TRUE, class = c("html", "character")), answers = list(structure(list(id = "lnr_ans_e018364",     option = "df[4,3]", value = "df[4,3]", label = structure("df[4,3]", html = TRUE, class = c("html",     "character")), correct = TRUE, message = NULL), class = c("tutorial_question_answer", "tutorial_quiz_answer")), structure(list(id = "lnr_ans_e5e684e",     option = "df[3,4]", value = "df[3,4]", label = structure("df[3,4]", html = TRUE, class = c("html",     "character")), correct = FALSE, message = NULL), class = c("tutorial_question_answer", "tutorial_quiz_answer")), structure(list(id = "lnr_ans_580f9ea",     option = "df$col.three[3]", value = "df$col.three[3]", label = structure("df$col.three[3]", html = TRUE, class = c("html",     "character")), correct = TRUE, message = NULL), class = c("tutorial_question_answer", "tutorial_quiz_answer"))), button_labels = list(submit = structure("Submit Answer", html = TRUE, class = c("html", "character")), try_again = structure("Try Again", html = TRUE, class = c("html", "character"))), messages = list(correct = structure("Correct!", html = TRUE, class = c("html", "character")), try_again = structure("Incorrect", html = TRUE, class = c("html", "character")), incorrect = structure("Incorrect", html = TRUE, class = c("html", "character")), message = NULL, post_message = NULL), ids = list(    answer = "quiz-3-answer", question = "quiz-3"), loading = structure("<strong>Loading:<\u002fstrong> \nWhich of the following get the 4th observation of col.three\n<br/><br/><br/>", html = TRUE, class = c("html", "character")), random_answer_order = FALSE, allow_retry = FALSE,     seed = 148680525.930765, options = list()), class = c("learnr_checkbox", "tutorial_question")))
</script>
 <!--html_preserve-->
<script type="application/shiny-prerendered" data-context="dependencies">
{"type":"list","attributes":{},"value":[{"type":"list","attributes":{"names":{"type":"character","attributes":{},"value":["name","version","src","meta","script","stylesheet","head","attachment","package","all_files","pkgVersion"]},"class":{"type":"character","attributes":{},"value":["html_dependency"]}},"value":[{"type":"character","attributes":{},"value":["jquery"]},{"type":"character","attributes":{},"value":["1.11.3"]},{"type":"list","attributes":{"names":{"type":"character","attributes":{},"value":["file"]}},"value":[{"type":"character","attributes":{},"value":["rmd/h/jquery"]}]},{"type":"NULL"},{"type":"character","attributes":{},"value":["jquery.min.js"]},{"type":"NULL"},{"type":"NULL"},{"type":"NULL"},{"type":"character","attributes":{},"value":["rmarkdown"]},{"type":"logical","attributes":{},"value":[true]},{"type":"character","attributes":{},"value":["2.4"]}]},{"type":"list","attributes":{"names":{"type":"character","attributes":{},"value":["name","version","src","meta","script","stylesheet","head","attachment","package","all_files","pkgVersion"]},"class":{"type":"character","attributes":{},"value":["html_dependency"]}},"value":[{"type":"character","attributes":{},"value":["bootstrap"]},{"type":"character","attributes":{},"value":["3.3.5"]},{"type":"list","attributes":{"names":{"type":"character","attributes":{},"value":["file"]}},"value":[{"type":"character","attributes":{},"value":["rmd/h/bootstrap"]}]},{"type":"list","attributes":{"names":{"type":"character","attributes":{},"value":["viewport"]}},"value":[{"type":"character","attributes":{},"value":["width=device-width, initial-scale=1"]}]},{"type":"character","attributes":{},"value":["js/bootstrap.min.js","shim/html5shiv.min.js","shim/respond.min.js"]},{"type":"character","attributes":{},"value":["css/cerulean.min.css"]},{"type":"NULL"},{"type":"NULL"},{"type":"character","attributes":{},"value":["rmarkdown"]},{"type":"logical","attributes":{},"value":[true]},{"type":"character","attributes":{},"value":["2.4"]}]},{"type":"list","attributes":{"names":{"type":"character","attributes":{},"value":["name","version","src","meta","script","stylesheet","head","attachment","package","all_files","pkgVersion"]},"class":{"type":"character","attributes":{},"value":["html_dependency"]}},"value":[{"type":"character","attributes":{},"value":["pagedtable"]},{"type":"character","attributes":{},"value":["1.1"]},{"type":"list","attributes":{"names":{"type":"character","attributes":{},"value":["file"]}},"value":[{"type":"character","attributes":{},"value":["rmd/h/pagedtable-1.1"]}]},{"type":"NULL"},{"type":"character","attributes":{},"value":["js/pagedtable.js"]},{"type":"character","attributes":{},"value":["css/pagedtable.css"]},{"type":"NULL"},{"type":"NULL"},{"type":"character","attributes":{},"value":["rmarkdown"]},{"type":"logical","attributes":{},"value":[true]},{"type":"character","attributes":{},"value":["2.4"]}]},{"type":"list","attributes":{"names":{"type":"character","attributes":{},"value":["name","version","src","meta","script","stylesheet","head","attachment","package","all_files","pkgVersion"]},"class":{"type":"character","attributes":{},"value":["html_dependency"]}},"value":[{"type":"character","attributes":{},"value":["highlightjs"]},{"type":"character","attributes":{},"value":["9.12.0"]},{"type":"list","attributes":{"names":{"type":"character","attributes":{},"value":["file"]}},"value":[{"type":"character","attributes":{},"value":["rmd/h/highlightjs"]}]},{"type":"NULL"},{"type":"character","attributes":{},"value":["highlight.js"]},{"type":"character","attributes":{},"value":["textmate.css"]},{"type":"NULL"},{"type":"NULL"},{"type":"character","attributes":{},"value":["rmarkdown"]},{"type":"logical","attributes":{},"value":[true]},{"type":"character","attributes":{},"value":["2.4"]}]},{"type":"list","attributes":{"names":{"type":"character","attributes":{},"value":["name","version","src","meta","script","stylesheet","head","attachment","package","all_files","pkgVersion"]},"class":{"type":"character","attributes":{},"value":["html_dependency"]}},"value":[{"type":"character","attributes":{},"value":["tutorial"]},{"type":"character","attributes":{},"value":["0.10.1"]},{"type":"list","attributes":{"names":{"type":"character","attributes":{},"value":["file"]}},"value":[{"type":"character","attributes":{},"value":["lib/tutorial"]}]},{"type":"NULL"},{"type":"character","attributes":{},"value":["tutorial.js"]},{"type":"character","attributes":{},"value":["tutorial.css"]},{"type":"NULL"},{"type":"NULL"},{"type":"character","attributes":{},"value":["learnr"]},{"type":"logical","attributes":{},"value":[true]},{"type":"character","attributes":{},"value":["0.10.1"]}]},{"type":"list","attributes":{"names":{"type":"character","attributes":{},"value":["name","version","src","meta","script","stylesheet","head","attachment","package","all_files","pkgVersion"]},"class":{"type":"character","attributes":{},"value":["html_dependency"]}},"value":[{"type":"character","attributes":{},"value":["tutorial-autocompletion"]},{"type":"character","attributes":{},"value":["0.10.1"]},{"type":"list","attributes":{"names":{"type":"character","attributes":{},"value":["file"]}},"value":[{"type":"character","attributes":{},"value":["lib/tutorial"]}]},{"type":"NULL"},{"type":"character","attributes":{},"value":["tutorial-autocompletion.js"]},{"type":"NULL"},{"type":"NULL"},{"type":"NULL"},{"type":"character","attributes":{},"value":["learnr"]},{"type":"logical","attributes":{},"value":[true]},{"type":"character","attributes":{},"value":["0.10.1"]}]},{"type":"list","attributes":{"names":{"type":"character","attributes":{},"value":["name","version","src","meta","script","stylesheet","head","attachment","package","all_files","pkgVersion"]},"class":{"type":"character","attributes":{},"value":["html_dependency"]}},"value":[{"type":"character","attributes":{},"value":["tutorial-diagnostics"]},{"type":"character","attributes":{},"value":["0.10.1"]},{"type":"list","attributes":{"names":{"type":"character","attributes":{},"value":["file"]}},"value":[{"type":"character","attributes":{},"value":["lib/tutorial"]}]},{"type":"NULL"},{"type":"character","attributes":{},"value":["tutorial-diagnostics.js"]},{"type":"NULL"},{"type":"NULL"},{"type":"NULL"},{"type":"character","attributes":{},"value":["learnr"]},{"type":"logical","attributes":{},"value":[true]},{"type":"character","attributes":{},"value":["0.10.1"]}]},{"type":"list","attributes":{"names":{"type":"character","attributes":{},"value":["name","version","src","meta","script","stylesheet","head","attachment","package","all_files","pkgVersion"]},"class":{"type":"character","attributes":{},"value":["html_dependency"]}},"value":[{"type":"character","attributes":{},"value":["tutorial-format"]},{"type":"character","attributes":{},"value":["0.10.1"]},{"type":"list","attributes":{"names":{"type":"character","attributes":{},"value":["file"]}},"value":[{"type":"character","attributes":{},"value":["rmarkdown/templates/tutorial/resources"]}]},{"type":"NULL"},{"type":"character","attributes":{},"value":["tutorial-format.js"]},{"type":"character","attributes":{},"value":["tutorial-format.css","rstudio-theme.css"]},{"type":"NULL"},{"type":"NULL"},{"type":"character","attributes":{},"value":["learnr"]},{"type":"logical","attributes":{},"value":[true]},{"type":"character","attributes":{},"value":["0.10.1"]}]},{"type":"list","attributes":{"names":{"type":"character","attributes":{},"value":["name","version","src","meta","script","stylesheet","head","attachment","package","all_files","pkgVersion"]},"class":{"type":"character","attributes":{},"value":["html_dependency"]}},"value":[{"type":"character","attributes":{},"value":["jquery"]},{"type":"character","attributes":{},"value":["1.11.3"]},{"type":"list","attributes":{"names":{"type":"character","attributes":{},"value":["file"]}},"value":[{"type":"character","attributes":{},"value":["rmd/h/jquery"]}]},{"type":"NULL"},{"type":"character","attributes":{},"value":["jquery.min.js"]},{"type":"NULL"},{"type":"NULL"},{"type":"NULL"},{"type":"character","attributes":{},"value":["rmarkdown"]},{"type":"logical","attributes":{},"value":[true]},{"type":"character","attributes":{},"value":["2.4"]}]},{"type":"list","attributes":{"names":{"type":"character","attributes":{},"value":["name","version","src","meta","script","stylesheet","head","attachment","package","all_files","pkgVersion"]},"class":{"type":"character","attributes":{},"value":["html_dependency"]}},"value":[{"type":"character","attributes":{},"value":["navigation"]},{"type":"character","attributes":{},"value":["1.1"]},{"type":"list","attributes":{"names":{"type":"character","attributes":{},"value":["file"]}},"value":[{"type":"character","attributes":{},"value":["rmd/h/navigation-1.1"]}]},{"type":"NULL"},{"type":"character","attributes":{},"value":["tabsets.js"]},{"type":"NULL"},{"type":"NULL"},{"type":"NULL"},{"type":"character","attributes":{},"value":["rmarkdown"]},{"type":"logical","attributes":{},"value":[true]},{"type":"character","attributes":{},"value":["2.4"]}]},{"type":"list","attributes":{"names":{"type":"character","attributes":{},"value":["name","version","src","meta","script","stylesheet","head","attachment","package","all_files","pkgVersion"]},"class":{"type":"character","attributes":{},"value":["html_dependency"]}},"value":[{"type":"character","attributes":{},"value":["highlightjs"]},{"type":"character","attributes":{},"value":["9.12.0"]},{"type":"list","attributes":{"names":{"type":"character","attributes":{},"value":["file"]}},"value":[{"type":"character","attributes":{},"value":["rmd/h/highlightjs"]}]},{"type":"NULL"},{"type":"character","attributes":{},"value":["highlight.js"]},{"type":"character","attributes":{},"value":["default.css"]},{"type":"NULL"},{"type":"NULL"},{"type":"character","attributes":{},"value":["rmarkdown"]},{"type":"logical","attributes":{},"value":[true]},{"type":"character","attributes":{},"value":["2.4"]}]},{"type":"list","attributes":{"names":{"type":"character","attributes":{},"value":["name","version","src","meta","script","stylesheet","head","attachment","package","all_files","pkgVersion"]},"class":{"type":"character","attributes":{},"value":["html_dependency"]}},"value":[{"type":"character","attributes":{},"value":["jquery"]},{"type":"character","attributes":{},"value":["1.11.3"]},{"type":"list","attributes":{"names":{"type":"character","attributes":{},"value":["file"]}},"value":[{"type":"character","attributes":{},"value":["rmd/h/jquery"]}]},{"type":"NULL"},{"type":"character","attributes":{},"value":["jquery.min.js"]},{"type":"NULL"},{"type":"NULL"},{"type":"NULL"},{"type":"character","attributes":{},"value":["rmarkdown"]},{"type":"logical","attributes":{},"value":[true]},{"type":"character","attributes":{},"value":["2.4"]}]},{"type":"list","attributes":{"names":{"type":"character","attributes":{},"value":["name","version","src","meta","script","stylesheet","head","attachment","package","all_files","pkgVersion"]},"class":{"type":"character","attributes":{},"value":["html_dependency"]}},"value":[{"type":"character","attributes":{},"value":["font-awesome"]},{"type":"character","attributes":{},"value":["5.1.0"]},{"type":"list","attributes":{"names":{"type":"character","attributes":{},"value":["file"]}},"value":[{"type":"character","attributes":{},"value":["rmd/h/fontawesome"]}]},{"type":"NULL"},{"type":"NULL"},{"type":"character","attributes":{},"value":["css/all.css","css/v4-shims.css"]},{"type":"NULL"},{"type":"NULL"},{"type":"character","attributes":{},"value":["rmarkdown"]},{"type":"logical","attributes":{},"value":[true]},{"type":"character","attributes":{},"value":["2.4"]}]},{"type":"list","attributes":{"names":{"type":"character","attributes":{},"value":["name","version","src","meta","script","stylesheet","head","attachment","package","all_files","pkgVersion"]},"class":{"type":"character","attributes":{},"value":["html_dependency"]}},"value":[{"type":"character","attributes":{},"value":["bootbox"]},{"type":"character","attributes":{},"value":["4.4.0"]},{"type":"list","attributes":{"names":{"type":"character","attributes":{},"value":["file"]}},"value":[{"type":"character","attributes":{},"value":["lib/bootbox"]}]},{"type":"NULL"},{"type":"character","attributes":{},"value":["bootbox.min.js"]},{"type":"NULL"},{"type":"NULL"},{"type":"NULL"},{"type":"character","attributes":{},"value":["learnr"]},{"type":"logical","attributes":{},"value":[true]},{"type":"character","attributes":{},"value":["0.10.1"]}]},{"type":"list","attributes":{"names":{"type":"character","attributes":{},"value":["name","version","src","meta","script","stylesheet","head","attachment","package","all_files","pkgVersion"]},"class":{"type":"character","attributes":{},"value":["html_dependency"]}},"value":[{"type":"character","attributes":{},"value":["idb-keyvalue"]},{"type":"character","attributes":{},"value":["3.2.0"]},{"type":"list","attributes":{"names":{"type":"character","attributes":{},"value":["file"]}},"value":[{"type":"character","attributes":{},"value":["lib/idb-keyval"]}]},{"type":"NULL"},{"type":"character","attributes":{},"value":["idb-keyval-iife-compat.min.js"]},{"type":"NULL"},{"type":"NULL"},{"type":"NULL"},{"type":"character","attributes":{},"value":["learnr"]},{"type":"logical","attributes":{},"value":[false]},{"type":"character","attributes":{},"value":["0.10.1"]}]},{"type":"list","attributes":{"names":{"type":"character","attributes":{},"value":["name","version","src","meta","script","stylesheet","head","attachment","package","all_files","pkgVersion"]},"class":{"type":"character","attributes":{},"value":["html_dependency"]}},"value":[{"type":"character","attributes":{},"value":["tutorial"]},{"type":"character","attributes":{},"value":["0.10.1"]},{"type":"list","attributes":{"names":{"type":"character","attributes":{},"value":["file"]}},"value":[{"type":"character","attributes":{},"value":["lib/tutorial"]}]},{"type":"NULL"},{"type":"character","attributes":{},"value":["tutorial.js"]},{"type":"character","attributes":{},"value":["tutorial.css"]},{"type":"NULL"},{"type":"NULL"},{"type":"character","attributes":{},"value":["learnr"]},{"type":"logical","attributes":{},"value":[true]},{"type":"character","attributes":{},"value":["0.10.1"]}]},{"type":"list","attributes":{"names":{"type":"character","attributes":{},"value":["name","version","src","meta","script","stylesheet","head","attachment","package","all_files","pkgVersion"]},"class":{"type":"character","attributes":{},"value":["html_dependency"]}},"value":[{"type":"character","attributes":{},"value":["tutorial-autocompletion"]},{"type":"character","attributes":{},"value":["0.10.1"]},{"type":"list","attributes":{"names":{"type":"character","attributes":{},"value":["file"]}},"value":[{"type":"character","attributes":{},"value":["lib/tutorial"]}]},{"type":"NULL"},{"type":"character","attributes":{},"value":["tutorial-autocompletion.js"]},{"type":"NULL"},{"type":"NULL"},{"type":"NULL"},{"type":"character","attributes":{},"value":["learnr"]},{"type":"logical","attributes":{},"value":[true]},{"type":"character","attributes":{},"value":["0.10.1"]}]},{"type":"list","attributes":{"names":{"type":"character","attributes":{},"value":["name","version","src","meta","script","stylesheet","head","attachment","package","all_files","pkgVersion"]},"class":{"type":"character","attributes":{},"value":["html_dependency"]}},"value":[{"type":"character","attributes":{},"value":["tutorial-diagnostics"]},{"type":"character","attributes":{},"value":["0.10.1"]},{"type":"list","attributes":{"names":{"type":"character","attributes":{},"value":["file"]}},"value":[{"type":"character","attributes":{},"value":["lib/tutorial"]}]},{"type":"NULL"},{"type":"character","attributes":{},"value":["tutorial-diagnostics.js"]},{"type":"NULL"},{"type":"NULL"},{"type":"NULL"},{"type":"character","attributes":{},"value":["learnr"]},{"type":"logical","attributes":{},"value":[true]},{"type":"character","attributes":{},"value":["0.10.1"]}]},{"type":"list","attributes":{"names":{"type":"character","attributes":{},"value":["name","version","src","meta","script","stylesheet","head","attachment","package","all_files","pkgVersion"]},"class":{"type":"character","attributes":{},"value":["html_dependency"]}},"value":[{"type":"character","attributes":{},"value":["ace"]},{"type":"character","attributes":{},"value":["1.2.6"]},{"type":"list","attributes":{"names":{"type":"character","attributes":{},"value":["file"]}},"value":[{"type":"character","attributes":{},"value":["lib/ace"]}]},{"type":"NULL"},{"type":"character","attributes":{},"value":["ace.js"]},{"type":"NULL"},{"type":"NULL"},{"type":"NULL"},{"type":"character","attributes":{},"value":["learnr"]},{"type":"logical","attributes":{},"value":[true]},{"type":"character","attributes":{},"value":["0.10.1"]}]},{"type":"list","attributes":{"names":{"type":"character","attributes":{},"value":["name","version","src","meta","script","stylesheet","head","attachment","package","all_files","pkgVersion"]},"class":{"type":"character","attributes":{},"value":["html_dependency"]}},"value":[{"type":"character","attributes":{},"value":["clipboardjs"]},{"type":"character","attributes":{},"value":["1.5.15"]},{"type":"list","attributes":{"names":{"type":"character","attributes":{},"value":["file"]}},"value":[{"type":"character","attributes":{},"value":["lib/clipboardjs"]}]},{"type":"NULL"},{"type":"character","attributes":{},"value":["clipboard.min.js"]},{"type":"NULL"},{"type":"NULL"},{"type":"NULL"},{"type":"character","attributes":{},"value":["learnr"]},{"type":"logical","attributes":{},"value":[true]},{"type":"character","attributes":{},"value":["0.10.1"]}]},{"type":"list","attributes":{"names":{"type":"character","attributes":{},"value":["name","version","src","meta","script","stylesheet","head","attachment","package","all_files","pkgVersion"]},"class":{"type":"character","attributes":{},"value":["html_dependency"]}},"value":[{"type":"character","attributes":{},"value":["ace"]},{"type":"character","attributes":{},"value":["1.2.6"]},{"type":"list","attributes":{"names":{"type":"character","attributes":{},"value":["file"]}},"value":[{"type":"character","attributes":{},"value":["lib/ace"]}]},{"type":"NULL"},{"type":"character","attributes":{},"value":["ace.js"]},{"type":"NULL"},{"type":"NULL"},{"type":"NULL"},{"type":"character","attributes":{},"value":["learnr"]},{"type":"logical","attributes":{},"value":[true]},{"type":"character","attributes":{},"value":["0.10.1"]}]},{"type":"list","attributes":{"names":{"type":"character","attributes":{},"value":["name","version","src","meta","script","stylesheet","head","attachment","package","all_files","pkgVersion"]},"class":{"type":"character","attributes":{},"value":["html_dependency"]}},"value":[{"type":"character","attributes":{},"value":["clipboardjs"]},{"type":"character","attributes":{},"value":["1.5.15"]},{"type":"list","attributes":{"names":{"type":"character","attributes":{},"value":["file"]}},"value":[{"type":"character","attributes":{},"value":["lib/clipboardjs"]}]},{"type":"NULL"},{"type":"character","attributes":{},"value":["clipboard.min.js"]},{"type":"NULL"},{"type":"NULL"},{"type":"NULL"},{"type":"character","attributes":{},"value":["learnr"]},{"type":"logical","attributes":{},"value":[true]},{"type":"character","attributes":{},"value":["0.10.1"]}]},{"type":"list","attributes":{"names":{"type":"character","attributes":{},"value":["name","version","src","meta","script","stylesheet","head","attachment","package","all_files","pkgVersion"]},"class":{"type":"character","attributes":{},"value":["html_dependency"]}},"value":[{"type":"character","attributes":{},"value":["ace"]},{"type":"character","attributes":{},"value":["1.2.6"]},{"type":"list","attributes":{"names":{"type":"character","attributes":{},"value":["file"]}},"value":[{"type":"character","attributes":{},"value":["lib/ace"]}]},{"type":"NULL"},{"type":"character","attributes":{},"value":["ace.js"]},{"type":"NULL"},{"type":"NULL"},{"type":"NULL"},{"type":"character","attributes":{},"value":["learnr"]},{"type":"logical","attributes":{},"value":[true]},{"type":"character","attributes":{},"value":["0.10.1"]}]},{"type":"list","attributes":{"names":{"type":"character","attributes":{},"value":["name","version","src","meta","script","stylesheet","head","attachment","package","all_files","pkgVersion"]},"class":{"type":"character","attributes":{},"value":["html_dependency"]}},"value":[{"type":"character","attributes":{},"value":["clipboardjs"]},{"type":"character","attributes":{},"value":["1.5.15"]},{"type":"list","attributes":{"names":{"type":"character","attributes":{},"value":["file"]}},"value":[{"type":"character","attributes":{},"value":["lib/clipboardjs"]}]},{"type":"NULL"},{"type":"character","attributes":{},"value":["clipboard.min.js"]},{"type":"NULL"},{"type":"NULL"},{"type":"NULL"},{"type":"character","attributes":{},"value":["learnr"]},{"type":"logical","attributes":{},"value":[true]},{"type":"character","attributes":{},"value":["0.10.1"]}]},{"type":"list","attributes":{"names":{"type":"character","attributes":{},"value":["name","version","src","meta","script","stylesheet","head","attachment","package","all_files","pkgVersion"]},"class":{"type":"character","attributes":{},"value":["html_dependency"]}},"value":[{"type":"character","attributes":{},"value":["ace"]},{"type":"character","attributes":{},"value":["1.2.6"]},{"type":"list","attributes":{"names":{"type":"character","attributes":{},"value":["file"]}},"value":[{"type":"character","attributes":{},"value":["lib/ace"]}]},{"type":"NULL"},{"type":"character","attributes":{},"value":["ace.js"]},{"type":"NULL"},{"type":"NULL"},{"type":"NULL"},{"type":"character","attributes":{},"value":["learnr"]},{"type":"logical","attributes":{},"value":[true]},{"type":"character","attributes":{},"value":["0.10.1"]}]},{"type":"list","attributes":{"names":{"type":"character","attributes":{},"value":["name","version","src","meta","script","stylesheet","head","attachment","package","all_files","pkgVersion"]},"class":{"type":"character","attributes":{},"value":["html_dependency"]}},"value":[{"type":"character","attributes":{},"value":["clipboardjs"]},{"type":"character","attributes":{},"value":["1.5.15"]},{"type":"list","attributes":{"names":{"type":"character","attributes":{},"value":["file"]}},"value":[{"type":"character","attributes":{},"value":["lib/clipboardjs"]}]},{"type":"NULL"},{"type":"character","attributes":{},"value":["clipboard.min.js"]},{"type":"NULL"},{"type":"NULL"},{"type":"NULL"},{"type":"character","attributes":{},"value":["learnr"]},{"type":"logical","attributes":{},"value":[true]},{"type":"character","attributes":{},"value":["0.10.1"]}]},{"type":"list","attributes":{"names":{"type":"character","attributes":{},"value":["name","version","src","meta","script","stylesheet","head","attachment","package","all_files","pkgVersion"]},"class":{"type":"character","attributes":{},"value":["html_dependency"]}},"value":[{"type":"character","attributes":{},"value":["ace"]},{"type":"character","attributes":{},"value":["1.2.6"]},{"type":"list","attributes":{"names":{"type":"character","attributes":{},"value":["file"]}},"value":[{"type":"character","attributes":{},"value":["lib/ace"]}]},{"type":"NULL"},{"type":"character","attributes":{},"value":["ace.js"]},{"type":"NULL"},{"type":"NULL"},{"type":"NULL"},{"type":"character","attributes":{},"value":["learnr"]},{"type":"logical","attributes":{},"value":[true]},{"type":"character","attributes":{},"value":["0.10.1"]}]},{"type":"list","attributes":{"names":{"type":"character","attributes":{},"value":["name","version","src","meta","script","stylesheet","head","attachment","package","all_files","pkgVersion"]},"class":{"type":"character","attributes":{},"value":["html_dependency"]}},"value":[{"type":"character","attributes":{},"value":["clipboardjs"]},{"type":"character","attributes":{},"value":["1.5.15"]},{"type":"list","attributes":{"names":{"type":"character","attributes":{},"value":["file"]}},"value":[{"type":"character","attributes":{},"value":["lib/clipboardjs"]}]},{"type":"NULL"},{"type":"character","attributes":{},"value":["clipboard.min.js"]},{"type":"NULL"},{"type":"NULL"},{"type":"NULL"},{"type":"character","attributes":{},"value":["learnr"]},{"type":"logical","attributes":{},"value":[true]},{"type":"character","attributes":{},"value":["0.10.1"]}]},{"type":"list","attributes":{"names":{"type":"character","attributes":{},"value":["name","version","src","meta","script","stylesheet","head","attachment","package","all_files","pkgVersion"]},"class":{"type":"character","attributes":{},"value":["html_dependency"]}},"value":[{"type":"character","attributes":{},"value":["ace"]},{"type":"character","attributes":{},"value":["1.2.6"]},{"type":"list","attributes":{"names":{"type":"character","attributes":{},"value":["file"]}},"value":[{"type":"character","attributes":{},"value":["lib/ace"]}]},{"type":"NULL"},{"type":"character","attributes":{},"value":["ace.js"]},{"type":"NULL"},{"type":"NULL"},{"type":"NULL"},{"type":"character","attributes":{},"value":["learnr"]},{"type":"logical","attributes":{},"value":[true]},{"type":"character","attributes":{},"value":["0.10.1"]}]},{"type":"list","attributes":{"names":{"type":"character","attributes":{},"value":["name","version","src","meta","script","stylesheet","head","attachment","package","all_files","pkgVersion"]},"class":{"type":"character","attributes":{},"value":["html_dependency"]}},"value":[{"type":"character","attributes":{},"value":["clipboardjs"]},{"type":"character","attributes":{},"value":["1.5.15"]},{"type":"list","attributes":{"names":{"type":"character","attributes":{},"value":["file"]}},"value":[{"type":"character","attributes":{},"value":["lib/clipboardjs"]}]},{"type":"NULL"},{"type":"character","attributes":{},"value":["clipboard.min.js"]},{"type":"NULL"},{"type":"NULL"},{"type":"NULL"},{"type":"character","attributes":{},"value":["learnr"]},{"type":"logical","attributes":{},"value":[true]},{"type":"character","attributes":{},"value":["0.10.1"]}]},{"type":"list","attributes":{"names":{"type":"character","attributes":{},"value":["name","version","src","meta","script","stylesheet","head","attachment","package","all_files","pkgVersion"]},"class":{"type":"character","attributes":{},"value":["html_dependency"]}},"value":[{"type":"character","attributes":{},"value":["ace"]},{"type":"character","attributes":{},"value":["1.2.6"]},{"type":"list","attributes":{"names":{"type":"character","attributes":{},"value":["file"]}},"value":[{"type":"character","attributes":{},"value":["lib/ace"]}]},{"type":"NULL"},{"type":"character","attributes":{},"value":["ace.js"]},{"type":"NULL"},{"type":"NULL"},{"type":"NULL"},{"type":"character","attributes":{},"value":["learnr"]},{"type":"logical","attributes":{},"value":[true]},{"type":"character","attributes":{},"value":["0.10.1"]}]},{"type":"list","attributes":{"names":{"type":"character","attributes":{},"value":["name","version","src","meta","script","stylesheet","head","attachment","package","all_files","pkgVersion"]},"class":{"type":"character","attributes":{},"value":["html_dependency"]}},"value":[{"type":"character","attributes":{},"value":["clipboardjs"]},{"type":"character","attributes":{},"value":["1.5.15"]},{"type":"list","attributes":{"names":{"type":"character","attributes":{},"value":["file"]}},"value":[{"type":"character","attributes":{},"value":["lib/clipboardjs"]}]},{"type":"NULL"},{"type":"character","attributes":{},"value":["clipboard.min.js"]},{"type":"NULL"},{"type":"NULL"},{"type":"NULL"},{"type":"character","attributes":{},"value":["learnr"]},{"type":"logical","attributes":{},"value":[true]},{"type":"character","attributes":{},"value":["0.10.1"]}]}]}
</script>
<!--/html_preserve-->
<!--html_preserve-->
<script type="application/shiny-prerendered" data-context="execution_dependencies">
{"type":"list","attributes":{"names":{"type":"character","attributes":{},"value":["packages"]}},"value":[{"type":"list","attributes":{"names":{"type":"character","attributes":{},"value":["packages","version"]},"class":{"type":"character","attributes":{},"value":["data.frame"]},"row.names":{"type":"integer","attributes":{},"value":[1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18,19,20,21,22,23,24,25,26,27,28,29,30,31,32,33,34,35,36,37,38,39,40,41,42,43,44,45,46,47,48,49,50,51,52,53,54,55,56,57,58,59,60,61,62,63,64,65,66]}},"value":[{"type":"character","attributes":{},"value":["assertthat","backports","base","checkmate","colorspace","compiler","crayon","datasets","DBI","digest","dplyr","ellipsis","evaluate","fansi","farver","fastmap","generics","ggplot2","glue","graphics","grDevices","grid","gtable","htmltools","htmlwidgets","httpuv","jsonlite","knitr","labeling","later","lattice","learnr","lifecycle","magrittr","markdown","Matrix","methods","mgcv","mime","munsell","nlme","pillar","pkgconfig","promises","purrr","R6","Rcpp","rlang","rmarkdown","rprojroot","scales","shiny","splines","stats","stringi","stringr","tibble","tidyselect","tools","utf8","utils","vctrs","withr","xfun","xtable","yaml"]},{"type":"character","attributes":{},"value":["0.2.1","1.2.0","4.0.3","2.0.0","1.4-1","4.0.3","1.3.4","4.0.3","1.1.0","0.6.27","1.0.5","0.3.1","0.14","0.4.1","2.0.3","1.0.1","0.1.0","3.3.3","1.4.2","4.0.3","4.0.3","4.0.3","0.3.0","0.5.0","1.5.2","1.5.4","1.7.2","1.30","0.3","1.1.0.1","0.20-41","0.10.1","1.0.0","2.0.1","1.1","1.2-18","4.0.3","1.8-33","0.9","0.5.0","3.1-149","1.5.1","2.0.3","1.1.1","0.3.4","2.5.0","1.0.5","0.4.10","2.4","2.0.2","1.1.1","1.5.0","4.0.3","4.0.3","1.5.3","1.4.0","3.1.0","1.1.0","4.0.3","1.1.4","4.0.3","0.3.6","2.3.0","0.18","1.8-4","2.2.1"]}]}]}
</script>
<!--/html_preserve-->
</div>

</div> <!-- topics -->

<div class="topicsContainer">
<div class="topicsPositioner">
<div class="band">
<div class="bandContent topicsListContainer">

<!-- begin doc-metadata -->
<div id="doc-metadata">
<h2 class="title toc-ignore" style="display:none;">Oxford R Tutorial</h2>
</div>
<!-- end doc-metadata -->

</div> <!-- bandContent.topicsListContainer -->
</div> <!-- band -->
</div> <!-- topicsPositioner -->
</div> <!-- topicsContainer -->


</div> <!-- bandContent page -->
</div> <!-- pageContent band -->




<script>
// add bootstrap table styles to pandoc tables
function bootstrapStylePandocTables() {
  $('tr.header').parent('thead').parent('table').addClass('table table-condensed');
}
$(document).ready(function () {
  bootstrapStylePandocTables();
});
</script>


<!-- dynamically load mathjax for compatibility with self-contained -->
<script>
  (function () {
    var script = document.createElement("script");
    script.type = "text/javascript";
    script.src  = "https://mathjax.rstudio.com/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML";
    document.getElementsByTagName("head")[0].appendChild(script);
  })();
</script>


</body>

</html>
