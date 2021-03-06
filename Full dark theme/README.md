<h1>Full dark theme for firefox</h1>
<p>Following the method described here, you will be able to give dark colors to firefox as shown in the following picture:</p>

<img src="https://i.imgur.com/zNKhEV6.png" title="Dark firefox UI with custom background" />

<img src="https://i.imgur.com/bEleqP7.png" title="Dark addons" />

<h2>Installation</h2>

<p><strong>Note: As of Firefox 69, you will need to enable the use of these files through a configuration setting.</strong> The preference in question is <code>toolkit.legacyUserProfileCustomizations.stylesheets</code>. Here is how you change its value:
<ol>
	<li>Load <code>about:config</code> in the Firefox address bar.</li>
    	<li>Confirm that you will be careful.</li>
    	<li>Search for <code>toolkit.legacyUserProfileCustomizations.stylesheets</code> using the search at the top.</li>
	<li>Toggle the preference. <code>True</code> means Firefox supports the CSS files, <code>False</code> that it ignores them.</li>
</ol>

<h4>Step by step:</h4>
<ul>
  <li>Type <code>about:support</code> in your URL bar, then go to that page.</li>
  <li>Click the "open folder" button inside the "profile folder" section.</li>
  <li>Create a folder named "chrome" in your profile folder if it doesn't exist yet.</li>
  <li>Place all files (.css files) from this folder to the "chrome" folder.</li>
  <li><b>Optional</b>: If you want to use the custom dark scrollbars, or dark tooltips, you will also have to enable JS injection through the method explained <a href="https://github.com/Izheil/Quantum-Nox-Firefox-Dark-Full-Theme/tree/master/Multirow%20and%20other%20functions/JS%20Loader">here</a>.</li>
  <li><b>Optional</b>: Edit userChrome.css to change any style you aren't fully convinced with (or to give a different style to the unread tabs, etc...).</li>
  <li><b>Optional</b>: You can also edit userChrome.css to change the background of the <code>about:home</code> page.</li>
  <li><b>Optional</b>: If you want a different style for the scrollbars or the tooltips, use any of the alternatives on the <a href="https://github.com/Izheil/Quantum-Nox-Firefox-Dark-Full-Theme/tree/master/Full%20dark%20theme/Alternative%20scrollbars%20%26%20tooltips">Alternative scrollbars & tooltips</a> folder.</li>
  <li><b>Optional</b>: If you want the default scrollbar style (userChrome still paints it dark), or white tooltips, don't copy the relevant CSS files for them.</li>
  <li><b>Optional</b>: If you want a dark version of either of the addons mentioned in the <a href="https://github.com/Izheil/Quantum-Nox-Firefox-Dark-Full-Theme#addon-dark-themes">addons dark themes section</a> in the front page of this repository, change the UUID's of them inside <code>addons.css</code>. An explanation on how to do so is given inside the file.</li>
</ul>

<p>If you have copied everything right, the folders structure should look something like this:</p>
<p>Structure of <a href="https://github.com/Izheil/Quantum-Nox-Firefox-Dark-Full-Theme/tree/master/Full%20dark%20theme#the-chrome-folder">the chrome folder</a> files inside your profile folder:</p>
<ul>
  <li><b>utils (folder)</b></li>
  <li>addons.css</li>
  <li>scrollbars.as.css</li>
  <li>setAttribute_unread.uc.js</li>
  <li>Sync-tabs-sidebar.as.css</li>
  <li>tooltips.as.css</li>
  <li>userChrome.css</li>
  <li>userContent.css</li>
</ul>

<p>Structure of <a href="https://github.com/Izheil/Quantum-Nox-Firefox-Dark-Full-Theme/tree/master/Full%20dark%20theme#Firefox-root-folder">firefox root folder</a> files (where your firefox is installed):</p>
<ul>
  <li>browser (folder)</li>
  <li>defaults (folder)</li>
  <ul>
    <li>pref (folder)</li>
    <ul>
      <li>channel-prefs.js</li>
      <li><b>config-prefs.js</b></li>
    </ul>
  </ul>
  <li>fonts (folder)</li>
  <li>gmp-clearkey (folder)</li>
  <li>META-INF (folder)</li>
  <li>uninstall (folder)</li>
  <li>firefox.exe/firefox</li>
  <li><b>config.js</b></li>
  <li>Other .dll files</li>
</ul>

<p>Bolded files or folders mark the required things to enable JS injection.</p>

<h2>The userChrome.css file</h2>

<p>The userChrome file turns dark all context menus, bookmarks, the url bar, the search bar, the main menu, and the toolbar. 
It will, although, not turn dark the extension popups you may have. <p>
<img src="https://i.imgur.com/wWjBcqz.png" title="Dark search menu (spanish)" />
<img src="https://i.imgur.com/7zj3SSq.png" title="Dark context menu (spanish)" />
<p>It will also turn dark the autocomplete popups (mostly a side-effect)</p>
<p>userChrome.css is also the file that enables loading of external (placed in the chrome folder) .css and .js files through the use of <code>userChrome.xml</code> (such as <code>scrollbars.as.css</code> or <code>MultiRowTabLiteforFx.uc.js</code>).</p>

<h2>The userContent.css file</h2>

<p>The userContent file will turn dark all the <code>about:about</code> pages.</p>
<img src="https://i.imgur.com/mKWPUSk.png" title="Dark firefox about: pages" />
<img src="https://i.imgur.com/97ebC1x.png" title="Dark addons page" />

<h2>Firefox root folder</h2>
<p>The root folder is where both the executable and the "defaults" folder of your current installed firefox are located</p>
<h4>For Windows, you can find firefox root folder here:</h4>

<pre>32bits Firefox -> C:\Program Files (x86)\Mozilla Firefox\
64bits Firefox -> C:\Program Files\Mozilla Firefox\</pre>

<p>If you have a 32-bits Windows, you will only see the 64-bits path.</p>

<h4>For Linux, you can find the root folder by default in this path:</h4>

<pre>/usr/lib/firefox/browser</pre>

<p>In some cases you might find a difference between 32 and 64 bits program installation paths in Linux, in that case you'd find the path here:</p> 

<pre>/usr/lib64/firefox/browser</pre>

<p>The installation directory path may also vary depending on the distribution, and if you use a package manager to install the application from their repository.</p>

<h4>For Mac, you can find the root folder in this path:</h4>

<pre>/Applications/Firefox.app/Contents/resources</pre>

<p>To open "Firefox.app", Ctrl-click it and select Show Package Contents. If you simply click it, you will start the application.</p>

<h2>The chrome folder</h2>
<p>The fastest way to find it is to just type <code>about:support</code> on the URL bar of your firefox, and then click the <b>open folder</b> button inside the "profile folder" section. After this, your profile folder will be open.</p>

<p><i>You may or may not see the chrome folder. If you don't see it, just create it and place inside the userContent.css and userChrome.css files.</i></p>

<p>If you want to know the exact location for profile folders (information taken from <a href="http://kb.mozillazine.org/Profile_folder_-_Firefox">here</a>):</p>

<h4>On Windows 7 and above, profile folders are in this location, by default:</h4>

<pre>C:\Users\(Windows login/user name)\AppData\Roaming\Mozilla\Firefox\Profiles\(profile folder)</pre>

<p><i>If you have never used userChrome.css or userContent.css before, you will have to create a folder named "chrome" inside the profile folder, which is where you will have to place these files.</i></p>

<p>This is where you would have to place the files once you have created the chrome folder:</p>

<pre>C:\Users\(Windows login/user name)\AppData\Roaming\Mozilla\Firefox\Profiles\(profile folder)\chrome\</pre>
  
<p>The AppData folder is a hidden folder; to show hidden folders, open a Windows Explorer window and choose "Tools → Folder Options → View (tab) → Show hidden files and folders".</p>

<p>You can also use this path to find the profile folder, even when it is hidden:</p>

<pre>%APPDATA%\Mozilla\Firefox\Profiles\(profile folder)</pre>

<h4>On Linux, profile folders are located in this other location:</h4>

<pre>/home/(Your-username)/.mozilla/firefox/(profile folder)</pre>

<p><i>If you have never used userChrome.css or userContent.css before, you will have to create a folder named "chrome" inside the profile folder, which is where you will have to place these files.</i></p>

<p>This is where you would have to place the files once you have created the chrome folder:</p>

<pre>/home/(Your-username)/.mozilla/firefox/(profile folder)/chrome/</pre>

<p>The ".mozilla" folder is a hidden folder. To show hidden files in Nautilus (Gnome desktop's default file browser), choose "View -> Show Hidden Files". On others such as Dolphin (Kubuntu's default file browser), you'd have to choose "Control -> Hidden files"</p>

<h4>On Mac, profile folders are in one of these locations:</h4>

<pre>~/Library/Application Support/Firefox/Profiles/(profile folder)
~/Library/Mozilla/Firefox/Profiles/(profile folder)</pre>

<p><i>If you have never used userChrome.css or userContent.css before, you will have to create a folder named "chrome" inside the profile folder, which is where you will have to place these files.</i></p>

<p>This is where you would have to place the files once you have created the chrome folder:</p>

<pre>~/Library/Application Support/Firefox/Profiles/(profile folder)/chrome
~/Library/Mozilla/Firefox/Profiles/(profile folder)/chrome/</pre>

<p>The tilde character (~) refers to the current user's Home folder, so ~/Library is the /Macintosh HD/Users/(username)/Library folder. For OS X 10.7 Lion and above, the ~/Library folder is hidden by default.</p>

<p>You can make them visible by typing the following in a terminal window.</p>
<pre>defaults write com.apple.finder AppleShowAllFiles TRUE
killall Finder</pre>
<p>This will also cause any file icons to take on a hazy, 50% alpha look. To restore the old settings (hide the files and make the icons look normal) issue the same commands again, but enter FALSE instead of TRUE.<p>

<p>It will also turn dark the <a href="https://addons.mozilla.org">Mozilla addons page</a>, both the old and the new, the file explorer inside firefox, and the "view source of page" page.</p>
