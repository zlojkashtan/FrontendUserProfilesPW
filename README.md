FrontendUserProfilesPW Installation & Configuration
---------------------------------------------------------------------------
1. Upload all files & Install module
2. Add 

	<pre><code>$fup = $modules->get('FrontendUserProfile');</code></pre>
	at the beginning of file *head.inc*
3. Add 
	
	<pre><code>if ($page->renderLogoutForm()) echo "<li>".$page->renderLogoutForm()."</li>";</code></pre>
	after 

	<pre><code>echo "<li><a$class href='{$child->url}'>{$child->title}</a></li>"; \n }</code></pre>
4. Add 
	<pre><code>
	<?php if ($message = $page->getMessage()): ?>
    	<p style="color:<?php echo $message['type'] ?>;"><?php echo $message['content']; ?></p>
    <?php endif; ?>
	
	<?php echo $page->renderLoginForm(); ?>
	</code></pre>
	after
	
	<pre><code>
	<div id="bodycopy">
	</code></pre>


REQUIREMENTS
---------------------------------------------------------------------------
1. Fieldtype DropDown by Hani79 (https://github.com/Hani79/Processwire_FieldType_Select_Drop_Down)

FrontendUserProfilesPW, Copyright 2013 by Orkhan Maharramli