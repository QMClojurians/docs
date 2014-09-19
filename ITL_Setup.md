##ITL Clojure setup

This is a short guide on how to get a clojure setup working on the ITL machines under Linux. This will be using [Leinigen](https://github.com/technomancy/leiningen) and a Clojure Emacs config to actually work in. This will provide useful features such as autocompletion, bracket matching and a REPL to run your code in. However with Leinigen installed, you will also be able to start a REPL through the terminal if you prefer.

####Installing Leinigen
We will be mostly following [this guide](http://leiningen.org/), but with a couple of work arounds for the ITL machines. This guide is great if you set up on your own computer though!

+	Create a folder in your home directory called **my_scripts**
+	Visit [here](http://leiningen.org/#install) and right click on the link to "lein script" and save it in your newly create **my_scripts** folder. Just call it **lein** with no file extension.
+	Open a terminal, navigate to your **my_scripts** folder and type

	``chmod a+x lein``

+	Now run the script by typing ``lein`` in the terminal. (If the script ran successfully, you should be able to type ``lein`` again and see a list of the available options for the command).
+	The problem now is that you will have to re-run this script every time that you start a new session, so we will fix that now.
+	In the terminal, type ``gedit .bashrc``, then view the file in gedit. This may or may not be empty.
+	At the start of the file, add the following line but replace **YOURITLLOGIN** with your ITL username eg. mdh30
	``export PATH=/homes/YOURITLLOGIN/my_scripts:$PATH``

lein should now be installed and runnable every time you log in!
Test it now with ``lein repl`` (this may take a little while)
try typing ``(+ 2 2)``


####Getting the Emacs Config

You can use whatever editor you like. This is just a guide to changing the config of emacs on the ITL to be a good clojure setup, where you will be able to compile and run your code, and start a REPL to test out anything you want.

+	Your home directory should contain a folder called ".emacs.d" check this in the terminal now with ``ls -a``
+	Assuming you could see the ".emacs.d" directory, clone our simple clojure emacs config by typing in the terminal:
	``git clone https://github.com/maxdh/first-clojure-emacs.git .emacs.d``
+	Try opening emacs! (either ``emacs`` in the terminal, or find it in the applications menu)


We will add a help guide to get you started with the Clojure-Emacs commands. But first, go through the **Emacs tutorial**. When you open Emacs, you can see a link to this on the left hand side of the page.
