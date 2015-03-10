XDCC Bot Leeching Script adds quick access to a collection of XDCC commands, along with a little functionality to make using pack lists easier.

This script was originally intended to be completely ported from the original mIRC script back in 2010 (which included state tracking and assisted queueing etc), but as I used XDCC bots infrequently I never completed the job. If there is sufficient demand I can pick this up again (say so in the issue tracker! See later).

Last updated on 10.03.15 for v1.1.


Installation
============

To load the script into KVIrc (which then persists until you uninstall) and run its startup alias, in a KVIrc console window:

    /parse <path to script file, speechmark-delimited if the path contains spaces>
    /XDCCBotLeechingScript::Startup

Once the script is installed, XDCCBotLeechingScript::Startup is automatically called when KVIrc is started.


Uninstallation
==============

In a KVIrc console window:

    /XDCCBotLeechingScript::uninstall::uninstall


Configuration
=============

This script is extremely simple, there is no configuration.


Nick Menu Integration
=====================

The script's main purpose currently is to add various XDCC commands to the nick menu (right-click the XDCC bot in the nick list):

![Nick menu](https://github.com/OmegaPhil/kvirc-xdcc-bot-leeching-script/blob/master/doc/nick-menu.png?raw=true)

The commands are grouped by type. If there is a command you would find handy, please make a feature request on the issue tracker (see later).

With the listing commands at the top, after sending a command to the bot, the script expects an incoming pack list - once such a txt file has succeeded downloading, the script automatically opens it via the xdg-open command.

Use of 'Get pack...' launches the following dialog:

![XDCC Send dialog](https://github.com/OmegaPhil/kvirc-xdcc-bot-leeching-script/blob/master/doc/xdcc-send-dialog.png?raw=true)

Submit the pack number here and the bot is PM'd the command.

'Get packs (BATCH)...' - launches the following dialog:

![XDCC Batch dialog](https://github.com/OmegaPhil/kvirc-xdcc-bot-leeching-script/blob/master/doc/xdcc-batch-dialog.png?raw=true)

Submit a valid packrange here (without XDCC BATCH) - read on for more detail on this command:

For some time now, the best iroffer bot to use as a botmaster is [iroffer dinoex mod](http://iroffer.dinoex.de/projects/iroffer). Along with much other functionality, this has offered a much more efficient command for users to download packs off a bot for years now - XDCC BATCH. With this, you can queue up one or more ranges of packs in a single command. See documentation [here](http://iroffer.dinoex.de/projects/iroffer/wiki/Xdcc_usercommands#XDCC-BATCH) - two basic commands as an example:

Fetch packs 21 and 89:

    XDCC BATCH 21,89

Fetch packs 100 through 200:

    XDCC BATCH 100-200

Of course the usual slot and queue limits still apply - anything over the limits will be rejected by the bot (the part of the range within your limits will be queued up).

If your botmaster doesn't know about dinoex mod, educate them! It has been around for many years.


Alias/Scripting Usage
=====================

The script is fully commented so should be fairly accessible for those wanting to see how to take its use further - for alias usage, see comments preceeding the alias, or run the alias without parameters for help/errors.


Development
===========

Try out my modification of the [geany](http://www.geany.org/) IDE, extending it to syntax highlight, parse KVIrc Script for aliases, events, variables, shortcut for loading scripts into KVIrc etc: [Github documentation](https://github.com/OmegaPhil/geany-kvircscript/wiki/README---KVIrc-Script-Integration).


Bugs And Feature Requests
=========================

Please create an issue on the [Github issue tracker](https://github.com/OmegaPhil/kvirc-xdcc-bot-leeching-script/issues).


Contact Details
===============

OmegaPhil@startmail.com
