# iOS App Signer
This is a helper app to sign iOS IPA files with a new Signing Certificate and Provisioning Profile. 

## Improvements over the Original Code
- Add ability to copy, cut and paste in text fields
- Bulk signing of IPA files

## Requirements
- macOS El Capitan or later
- Xcode 7 or later

## Usage
First select an IPA (or URL to an IPA), a Signing Certificate from your Mac’s Keychain and a Provisioning Profile. Then you can sign the IPA using two modes:

### Single Mode
Fill out the fields for Bundle ID, App Display Name, Build Number and Version String, or fill them empty to remain unchanged. Then click Start and your signed IPA file will be soon ready.

### Bulk Mode
Select a Config File adhering to the format below:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
<plist version="1.0">
<dict>
	<key>CFBundleVersion</key>
	<string></string>
	<key>CFBundleShortVersionString</key>
	<string></string>
	<key>Stores</key>
	<dict>
		<key></key>
		<string></string>
	</dict>
</dict>
</plist>
```

This mode will a signed IPA for each key in the `Stores` dictionary. It starts with the `CFBundleVersion` and `CFBundleShortVersionString` as the base and increments them accordingly for each Store. 

## Credits
[iOS App Signer](https://github.com/DanTheMan827/ios-app-signer)
[iReSign](https://github.com/maciekish/iReSign)
