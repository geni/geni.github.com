Our vision at Geni is to solve the problem of genealogy by empowering genealogists all over the world to work together and create the world's single family tree. Of course, to solve such a large problem, there are many smaller problems that must be solved first.

It's almost a certainty that one of your ancestors lived in a different region and spoke a different language than you speak.  In fact, there's even a great chance that one or more of your close relatives doesn't even speak the same language that you do.

As our community grew, we realized that a significant portion of our users spoke and wrote in languages other than English, but Geni was an English-only site.  For us to truly realize our vision, it became obvious that we must allow people that read any language to use our product.  We needed to implement a translation solution.

<h3>Existing Translation Solutions</h3> 
There were several third-party options available, including the <a href="http://ruby-i18n.org/2008/7/31/welcome-to-the-future-of-i18n-in-ruby-on-rails">i18n support for Ruby</a> and <a href="http://www.facebook.com/translations/">Facebook's Translations app</a>. We decided that i18n was not a realistic solution; Geni changes too frequently and the support for outdated translations was prohibitive.

Facebook's option, while very attractive, forces users to have Facebook accounts because it is built on the Connect platform (great for Facebook, but not good for people that don't use Facebook).  In addition, with Facebook, all translated text is stored/owned by Facebook, and it is all rendered after the pageload using JavaScript. This can be slow and messy, and it doesn't truly solve the problem of internationalization because (most) robots will only see the site in its original language. If a search engine can't read your site in various languages, how can it direct users of various languages to your site as a resource?

Ultimately we decided that the existing solutions weren't good enough, so we decided to build our own. This shouldn't be a surprise to anyone familiar with the <a href="http://www.socaltech.com/interview_with_david_sacks__geni_and_yammer/s-0017613.html">origins of Yammer</a>.
<a href="http://www.tr8n.org"><img class="alignright" title="Tr8n" src="http://www.tr8n.org/tr8n/images/tr8n_logo2.png" alt="Translation Software" width="255" height="164" /></a> 

<h3>Introducing tr8n as Open Source Software</h3> 
The solution we created is so dynamic, and it has worked so well, that we have decided to make it available for use as an open source project. Today we officially announce our release of <a href="http://www.tr8n.org/">tr8n</a> to the Ruby development community.

Tr8n is a Rails engine plugin that provides a framework for crowd-sourcing translations into hundreds of languages. The power of the engine comes from its intuitive and friendly user interface that allows site users and/or professional translators to rapidly translate the site into supported languages.

The flexible and robust rules engine that powers tr8n allows for any combination of language specific rules in any translatable sentence. Translators can create rules for phrases and sentences that depend on gender rules, number rules or other rules supported by the engine. The language specific rules can be configured by the language managers for any language.

The engine comes with a set of powerful administration tools that allow site admins to manage any aspect of the engine; including the enabling and disabling of its features and the monitoring of the translation process. Tr8n translation engine is based on a robust and flexible pluggable architecture where language rule types and the syntax of the "tr" tokens can be configured or extended by RoR developers for any application deployment.

<h3>tr8n on Geni</h3> 
Our implementation of tr8n has been an enormous success, with over 150,000 translations in 70 languages. To experiment with tr8n, stop by <a href="http://www.geni.com/">Geni.com</a>, sign up for an account, and you'll immediately be able to use the translation tools:

<img class="aligncenter" src="/images/tr8n-language-dropdown.png" alt="" width="417" height="350" /> 

Clicking on the language drop-down displays the initial tr8n dialog, where you can choose your language and opt to use the translation tools.

After enabling tr8n translations, all content on the page that has been properly wrapped will appear with green links. To edit a word, phrase or sentence, right-click on it and you'll be provided another tr8n menu that allows you to view current translations, vote for them, or add your own:

<img class="aligncenter" title="tr8n menu" src="/images/tr8n-translation-interface.png" alt="" width="541" height="342" /> 

<h3>tr8n Resources</h3> 
There are several resources available for developers that are interested in tr8n:
<ul> 
<li><a href="http://www.tr8n.org">Official tr8n site</a></li> 
<li><a href="http://wiki.tr8n.org">tr8n documentation wiki</a></li> 
<li><a href="https://github.com/berk/tr8n">tr8n source on github</a></li> 
</ul> 
