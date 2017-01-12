<<<<<<< HEAD
# pythonSignApk
python签名apk的脚本，同时支持v1和v2签名

* 由于android7.0开始采用v2签名，以前的美团等多渠道打包方式会导致v2签名失效；虽然暂时可以使用v2SigningEnabled false关闭，但不保证今后也能使用；为彻底解决问题，就些了这个脚本对多渠道包进行重新签名。
* 请自行配置jarsigner zipalign apksigner 的环境变量

* v2签名apksigner说明：
~~~~
--ks <filename>
The signer's private key and certificate chain reside in the given Java-based KeyStore file. If the filename is set to "NONE", the KeyStore containing the key and certificate doesn't need a file specified, which is the case for some PKCS #11 KeyStores.
--ks-key-alias <alias>
The name of the alias that represents the signer's private key and certificate data within the KeyStore. If the KeyStore associated with the signer contains multiple keys, you must specify this option.
--ks-pass <input-format>
The password for the KeyStore that contains the signer's private key and certificate. You must provide a password to open a KeyStore. The apksigner tool supports the following formats:

pass:<password> – Password provided inline with the rest of the apksigner sign command.
env:<name> – Password is stored in the given environment variable.
file:<filename> – Password is stored as a single line in the given file.
stdin – Password is provided as a single line in the standard input stream. This is the default behavior for --ks-pass.
Note: If you include multiple passwords in the same file, specify them on separate lines. The apksigner tool associates passwords with an APK's signers based on the order in which you specify the signers. If you've provided two passwords for a signer, apksigner interprets the first password as the KeyStore password and the second one as the key password.
~~~~
https://developer.android.com/studio/command-line/apksigner.html
=======
# pythonSignApk
>>>>>>> 16e75ea60619f2ce7257674bce4eb93771af9a12
