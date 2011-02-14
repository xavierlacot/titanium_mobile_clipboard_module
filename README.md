Appcelerator Titanium iPhone Clipboard Module
=============================================

# Goals and usage

This module allows to access the iPhone's clipboard from Titanium apps using a simple javascript API. It has been tested with Titanium Mobile 1.5.1.

Do not use this module, which remains here as an example. Rather use the official Titanium implementation, which has landed in the framework since [https://github.com/appcelerator/titanium_mobile/commit/a44c1b0de5412fe5b76ca74335d793b50c773885](https://github.com/appcelerator/titanium_mobile/commit/a44c1b0de5412fe5b76ca74335d793b50c773885). See the API documentation at [http://developer.appcelerator.com/apidoc/mobile/latest/Titanium.UI.Clipboard-module](http://developer.appcelerator.com/apidoc/mobile/latest/Titanium.UI.Clipboard-module).

# Usage

Add the following to the tiapp.xml file of your project:


    <modules>
      <module version="0.2">com.xavcc.Clipboard</module>
    </modules>


In you js code, simply write:


    // pre-condition: assume the clipboard contains some text

    // load he module
    var clipboard = require(‘com.xavcc.Clipboard’);

    var testvar = clipboard.getText();
    testvar = testvar + ', modified value';
    clipboard.setText(testvar)

    // post-condition: the clipboard now contains a modified value


# Installation

The module has to be built using XCode. See [http://assets.appcelerator.com.s3.amazonaws.com/docs/Module_Developers_Guide_iOS.pdf](http://assets.appcelerator.com.s3.amazonaws.com/docs/Module_Developers_Guide_iOS.pdf) for more informations.

Basically, you are required to run the command 'build.py' in the module. This will generate a zip file which has to be copied in the folder "/Library/Application Support/Titanium/"

# License

This module is licensed under the MIT license.