<!-- wp:paragraph -->
<p><sub>If you are reading this article, you have probably watched the <a href="https://www.youtube.com/watch?v=WfPk86Qf1Lo&amp;t=1s" target="_blank" rel="noreferrer noopener">YouTube(click here)</a> video. To jump right to the links and the code, <a href="#links-and-codes">click here</a>.</sub></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>The lockdown has compelled each one of us to attend online classes and honestly it is much of a headache. Why is that so? With the comfort that our house offers us, it is quite hard to maintain a constant attendance. So, I have come up with a solution to it! You can make a bot that will join/attend your classes for you! Yes, you've heard it right! </p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><strong>I would like to highlight the point that please use these steps as an enrichment and not a path to escape from your classes. So, Lets dive right into it!</strong></p>
<!-- /wp:paragraph -->

<!-- wp:heading -->
<h2>Step 1- Installing the Repository</h2>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>The first step would be to go to <a href="https://github.com/prokan468/AutoBot_Joins_Teams/" target="_blank" rel="noreferrer noopener">GitHub (click here)</a> and download the zip file under code. As you can see below:-</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":1837,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://raniac.in/wp-content/uploads/2020/12/TobiasPankner_Teams-Auto-Joiner_-Python-script-to-automatically-join-Microsoft-Teams-meetings.-Google-Chrome-09-12-2020-00_00_13-1024x522.png" alt="installing the repository from github" class="wp-image-1837"/></figure>
<!-- /wp:image -->

<!-- wp:heading -->
<h2>Step 2- Extracting the File</h2>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>Next, extract the file inside to whatever location you want. (I'd suggest desktop simply)</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":1835,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://raniac.in/wp-content/uploads/2020/12/Screenshot-2020-12-08-235943-1024x546.png" alt="extracting the file" class="wp-image-1835"/></figure>
<!-- /wp:image -->

<!-- wp:heading -->
<h2>Step 3- The Configuration</h2>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>Inside the folder, you will see a config.json.example or the config.json file, open that and enter all your credentials and how you want thing to be. These are things that are in the config file;</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":1839,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://raniac.in/wp-content/uploads/2020/12/config.json-Notepad-09-12-2020-00_04_49-1024x513.png" alt="configuration of the bot" class="wp-image-1839"/></figure>
<!-- /wp:image -->

<!-- wp:heading {"level":4} -->
<h4>email and Password</h4>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>What you have to do now is pretty simple. Enter your username and password between the two quotations .</p>
<!-- /wp:paragraph -->

<!-- wp:heading {"level":4} -->
<h4>run_at_time</h4>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>Second is the run at time, where you can specify the time at which you want the bot to start looking for the meetings. For example, lets say, your class is at 5:00pm and you want to set up your bot at 3:00pm, so what you can do is write 16:55 (in 24-hours format) in front of "run_at_time". That is all! Now, the bot will start looking for the meeting at 4:55pm.</p>
<!-- /wp:paragraph -->

<!-- wp:heading {"level":4} -->
<h4>meeting_mode</h4>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>The input that you put in here will specify where the bot will go to. <br>If you put <strong>1,</strong> the bot will join the meeting that is mentioned in the <strong>teams tab as well as calendar tab</strong>.<br>When you key in <strong>2,</strong> the bot will go to the <strong>teams tab</strong>, search for a meeting there and join the meeting.<br>If you put <strong>3,</strong> the bot will go to the <strong>calendars tab</strong>, see if the current time correlated with the time mentioned in the meeting in calendar and join accordingly.</p>
<!-- /wp:paragraph -->

<!-- wp:heading {"level":4} -->
<h4>organisation_num</h4>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>In your teams account, if you have only one organization, that is your school, (this is the case for most of the people), leave it as 1. But if you have more than one organizations, then enter the number of the organization you want the bot to enter.</p>
<!-- /wp:paragraph -->

<!-- wp:heading {"level":4} -->
<h4>random_delay</h4>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>By default, the boolean value of random_delay is set as false but I'd suggest you to change it to true. If you are to do so, before joining the meeting, the bot will take a pause of 20 seconds so that it appears human-like. If you are to leave it as false, you'd be added into the meeting in milliseconds and that might be something you would not want.</p>
<!-- /wp:paragraph -->

<!-- wp:heading {"level":4} -->
<h4>check_interval</h4>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>The time gap between every search that the bot makes is known as check interval. To understand this, when you open the command line, you are able to see that the bot looks for a new meeting every 10 seconds like what you mentioned in front of the "check_interval" variable. I'd suggest you to leave this as default i.e., 10.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":1852,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://raniac.in/wp-content/uploads/2020/12/Films-TV-09-12-2020-01_04_51-1024x576.png" alt="bot looking for meetings" class="wp-image-1852"/></figure>
<!-- /wp:image -->

<!-- wp:heading {"level":4} -->
<h4>auto_leave_after_min</h4>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>Once you have joined the meeting, you have to ensure that you dont stay in it for hours. So to insure that, you have an auto leave variable. <br>Here, if you mention any negative number, the bot will exit the meeting <strong><span style="text-decoration: underline;">after</span></strong> the specified number/minutes. <br>"leave_if_last": false<br>When you mention any positive number, the bot will exit the meeting <strong><span style="text-decoration: underline;">before</span></strong> the specified number/minutes.<br>If you leave it as 0, then the meeting would be exitted on the exact time the meeting is set to end by the organiser/teacher.</p>
<!-- /wp:paragraph -->

<!-- wp:heading {"level":4} -->
<h4>headless</h4>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>The headless variable is another boolean value. <br>If set as true, whatever the bot does, from logging into your account, to entering your meeting and to exiting your meeting, the bot will do it in the background and would not open a browser in the front for you to see.<br>If you set it as false, which I suggest you to do, the bot will show you all the steps that it takes in the front.</p>
<!-- /wp:paragraph -->

<!-- wp:heading {"level":4} -->
<h4>mute_audio</h4>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>When you set your mute audio variable as true, the bot will mute your microphone so this is obviously what I'd suggest.</p>
<!-- /wp:paragraph -->

<!-- wp:heading {"level":4} -->
<h4>chrome_type</h4>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>With this variable, you can decide whether you want to use Chrome, Chromium, Microsoft Edge as the browser that the bot uses. I would suggest you to leave it as default, i.e. Chrome</p>
<!-- /wp:paragraph -->

<!-- wp:heading {"level":4} -->
<h4>blacklist</h4>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>The last variable that you will see is the blacklist. This is used when you want to blacklist a meeting you do not want to join. Being a student, you obviously do not have the choice, so what you do here is backspace everything from the word blacklist to the last symbol in the document and add a curly bracket in the end.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Now that your config file is all set, remove the example at the end of the file and save it as config.json.</p>
<!-- /wp:paragraph -->

<!-- wp:heading -->
<h2>Step 4- Creating a Code Loop</h2>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>The next step would be to create a command that runs the python file in a loop. To do so, open notepad, and enter the following code into it:-</p>
<!-- /wp:paragraph -->

<!-- wp:coblocks/highlight -->
<p class="wp-block-coblocks-highlight"><mark class="wp-block-coblocks-highlight__content">:loop<br>auto_joiner.py<br>goto loop</mark></p>
<!-- /wp:coblocks/highlight -->

<!-- wp:paragraph -->
<p>Once you do so, save the file as "autorun.bat". (UPDATE- I've just added my <a href="https://github.com/prokan468/AutoBot_Joins_Teams" target="_blank" rel="noreferrer noopener">new repository on GitHub</a> from where if you download the zip file, you do not have to follow this step!)</p>
<!-- /wp:paragraph -->

<!-- wp:heading -->
<h2>Step 5- Downloading Python</h2>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>Before proceeding further, go to <a href="https://www.python.org/downloads" target="_blank" rel="noreferrer noopener">https://www.python.org/downloads</a>/ to download the latest version of python onto your PC.</p>
<!-- /wp:paragraph -->

<!-- wp:heading -->
<h2>Step 6- Running the Bot</h2>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>Now, this is where you would start seeing the magic happening. Double click the batch file that you just created, the autorun.bat file. </p>
<!-- /wp:paragraph -->

<!-- wp:image {"id":1855,"sizeSlug":"large","linkDestination":"none"} -->
<figure class="wp-block-image size-large"><img src="https://raniac.in/wp-content/uploads/2020/12/Screenshot-2020-12-09-011226-1024x543.png" alt="commands of the bot" class="wp-image-1855"/></figure>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>The command prompt will open and it will open a browser on its own. You would be able to see your username and password entered by itself. The bot will start looking for meetings and when it finds one, it will join it.</p>
<!-- /wp:paragraph -->

<!-- wp:heading -->
<h2>The End</h2>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>That is all! You now have a bot that will join and leave your meeting whenever you want it to. But this does not mean that you skip your classes and leave it upon the bot to do what you should be doing. Towards the end of the day, you will be the one sitting in the examination hall, not your bot!</p>
<!-- /wp:paragraph -->

<!-- wp:heading -->
<h2 id="links-and-codes">Links and Codes</h2>
<!-- /wp:heading -->

<!-- wp:coblocks/alert -->
<div class="wp-block-coblocks-alert"><p class="wp-block-coblocks-alert__title"><strong><span style="text-decoration: underline;">Links</span></strong></p><p class="wp-block-coblocks-alert__text">YouTube Tutorial- <a href="https://www.youtube.com/watch?v=WfPk86Qf1Lo&amp;t=1s" target="_blank" rel="noreferrer noopener">https://www.youtube.com/watch?v=WfPk86Qf1Lo&amp;t=1s</a><br>GitHub Repository- <a href="https://github.com/prokan468/AutoBot_Joins_Teams" target="_blank" rel="noreferrer noopener">https://github.com/prokan468/AutoBot_Joins_Teams<br></a>Python Download-<a href="https://www.python.org/downloads/" target="_blank" rel="noreferrer noopener"> https://www.python.org/downloads/</a></p></div>
<!-- /wp:coblocks/alert -->

<!-- wp:coblocks/alert -->
<div class="wp-block-coblocks-alert"><p class="wp-block-coblocks-alert__title"><strong><span style="text-decoration: underline;">Batch File Code</span></strong></p><p class="wp-block-coblocks-alert__text">:loop<br>auto_joiner.py<br>goto loop</p></div>
<!-- /wp:coblocks/alert -->

<!-- wp:paragraph -->
<p><sub>If you are reading this article, you have probably watched the <a href="https://www.youtube.com/watch?v=WfPk86Qf1Lo&amp;t=1s" target="_blank" rel="noreferrer noopener">YouTube(click here)</a> video. Thank you for your support, do comment down below whether you enjoyed this content and if we should continue making this type of <a href="https://raniac.in/?p=1829">content</a>.</sub></p>
<!-- /wp:paragraph -->
