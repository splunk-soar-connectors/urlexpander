[comment]: # "Auto-generated SOAR connector documentation"
# URL Expander

Publisher: Robert Martin  
Connector Version: 1\.0\.2  
Product Vendor: Generic  
Product Name: URLexpander  
Product Version Supported (regex): "\.\*"  
Minimum Product Version: 3\.0\.251  

Expands shortened URLs

[comment]: # "File: readme.md"
[comment]: # ""
[comment]: # "Licensed under the Apache License, Version 2.0 (the 'License');"
[comment]: # "you may not use this file except in compliance with the License."
[comment]: # "You may obtain a copy of the License at"
[comment]: # ""
[comment]: # "    http://www.apache.org/licenses/LICENSE-2.0"
[comment]: # ""
[comment]: # "Unless required by applicable law or agreed to in writing, software distributed under"
[comment]: # "the License is distributed on an 'AS IS' BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND,"
[comment]: # "either express or implied. See the License for the specific language governing permissions"
[comment]: # "and limitations under the License."
[comment]: # ""



### Configuration Variables
The below configuration variables are required for this Connector to operate.  These variables are specified when configuring a URLexpander asset in SOAR.

VARIABLE | REQUIRED | TYPE | DESCRIPTION
-------- | -------- | ---- | -----------
**bitly\_server** |  required  | string | Bit\.ly server IP/Hostname
**bitly\_apikey** |  required  | password | OAuth Token
**googl\_server** |  required  | string | Goo\.gl server IP/Hostname
**googl\_apikey** |  required  | password | API Key

### Supported Actions  
[test connectivity](#action-test-connectivity) - Validate the asset configuration for connectivity\.  
[lookup url](#action-lookup-url) - Expand bit\.ly or goo\.gl url  

## action: 'test connectivity'
Validate the asset configuration for connectivity\.

Type: **test**  
Read only: **True**

#### Action Parameters
No parameters are required for this action

#### Action Output
No Output  

## action: 'lookup url'
Expand bit\.ly or goo\.gl url

Type: **investigate**  
Read only: **True**

#### Action Parameters
PARAMETER | REQUIRED | DESCRIPTION | TYPE | CONTAINS
--------- | -------- | ----------- | ---- | --------
**short\_url** |  required  | Shortened url | string |  `url` 

#### Action Output
DATA PATH | TYPE | CONTAINS
--------- | ---- | --------
action\_result\.status | string | 
action\_result\.summary | string | 
action\_result\.message | string | 
action\_result\.parameter\.short\_url | string |  `url` 
action\_result\.data\.\*\.longUrl | string |  `url` 