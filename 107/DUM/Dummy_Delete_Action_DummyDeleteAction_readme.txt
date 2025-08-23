		DummyExtractAction  readme

                          August 2012
_________________________________________________________________

Lorem "ipsum" dolor sit 'amet', consectetur adipiscing elit. Curabitu
r egestas, lorem id sagittis elementum, sem lorem tempus dui, ac
porttitor tortor sapien in sapien. Donec in orci vitae urn


Contents:

1.0   Fix Name
2.0   Product(s)/Component(s) Affected
3.0   Fix Requirements
4.0   Fix Contents
5.0   Platform Support
6.0   Installation
7.0   Uninstallation
8.0   Cautions and Warnings
9.0   Globalization 
10.0  Copyright
11.0  Contacting Us



1.0 Fix Name

webMethods 1SYNC Module 6.5.2 Fix 6 (ONESYNC_6.5.2_Fix6).



2.0 Product(s)/Component(s) Affected

This fix affects webMethods 1SYNC Module 6.5.2.



3.0 Fix Requirements

None.



4.0 Fix Contents

This fix addresses the following issues:


SYN-57
Update webMethods 1SYNC Module 6.5.2 to include the 1SYNC IM
Release 6.8 schema changes.

This issue is resolved. webMethods 1SYNC Module 6.5.2 now includes
the 1SYNC IM Release 6.8 schema changes. 


SYN-49 (ONESYNC_6.5.2_Fix4)
Update webMethods 1SYNC Module 6.5.2 to include the 1SYNC IM
Release 6.6 schema changes.

This issue is resolved. webMethods 1SYNC Module 6.5.2 now includes
the 1SYNC IM Release 6.6 schema changes. 


SYN-38 (ONESYNC_6.5.2_Fix3)
Update webMethods 1SYNC Module 6.5.2 with the revised XML schema
released by 1SYNC on 10/22/2008.

Currently, webMethods 1SYNC Module 6.5.2 does not include the 
IM 6.4 XML schema released by 1SYNC.

This issue is now resolved.

SYN-36 (ONESYNC_6.5.2_Fix3)
webMethods 1SYNC Module 6.5.2 on Integration Server 7.1.2 throws 
an exception while sending documents to 1SYNC.

1SYNC Module 6.5.2 on Integration Server 7.1.2 throws the 
following exception while sending documents to 1SYNC:

  com.wm.lang.flow.FlowException: Error trapped in service
  : wm.ip.sync.transport:send Error: [ISC.0049.9010] Service
  'wm.tn.route:routeBizdoc' invoking unknown service 
  'pub.prt.tn:handleBizDoc' at '$default'. The service may 
  have been renamed, moved or disabled.
  
This error message occurs when the process runtime is not 
configured in the webMethods Integration Server. When the 
webMethods 1SYNC Module 6.5.2 sends a document to 1SYNC, it 
extracts the conversation ID of the document, and then Trading 
Networks invokes the process runtime to execute a process model 
associated with the document type. If the process runtime is not 
installed when 1SYNC Module is sending the document, an exception 
occurs.

This issue is resolved either by installing the WmPRT package or 
by setting the value of the 1Sync.ignorePRTDocument parameter to 
'true'. When the process runtime is not installed in Integration 
Server, to prevent the exception, set the value of the new 
1Sync.ignorePRTDocument configuration parameter to 'true' in the 
<Integration_Server>\packages\Wm1SYNC\config\config.cnf file.

1-1RKLXT (OneSYNC_6-5-2_Fix1)
Reference to wm.ip.util:formatErrorMessage service not completely
removed from webMethods 1SYNC Module 6.5.2.

If webMethods 1SYNC Module 6.5.2 has to run on webMethods
Integration Server 7.1, all the dependencies on WmIPRoot package
should be removed from the module. But,
wm.ip.sync.common.profile:getTPAInfo and
wm.ip.sync.common.profile:getProfile services are still dependent
on wm.ip.util:formatErrorMessage service. Due to these
dependencies, webMethods 1SYNC Module 6.5.2 cannot run on
webMethods Integration Server 7.1.

This issue is resolved. webMethods 1SYNC Module 6.5.2 is now
compatible with webMethods Integration Server 7.1.
wm.ip.sync.common.profile:getTPAInfo and
wm.ip.sync.common.profile:getProfile services now call
wm.ip.logutil:formatErrorMessage service instead of calling
wm.ip.util:formatErrorMessage service.

1-1S0JFR
Update webMethods 1SYNC Module 6.5.2 with the revised XML Schema
released by 1SYNC on 12/14/2007.

webMethods 1SYNC Module 6.5.2 has not yet included the latest XML
Schema released by 1SYNC.

This issue is now resolved.

1-1S0JH2
In wm.ip.sync.recs:docType_ns_catalogueItemNotification and
wm.ip.sync.recs:docType_ns_catalogueRequest Integration Server
documents, the attrGroup and attrGroupMany element names are
prefixed with "ns:" namespace (ns:attrGroup and
ns:attrGroupMany).

When the Integration Server creates a document from an XML schema
and if there is a reference to any Integration Server document in
that schema, then the attrGroup and attrGroupMany elements are
prefixed with "ns:" namespace. This behavior is normal, however
some users may not want the element names to be prefixed with
"ns:" namespace.

This issue is now resolved. The attrGroup and attrGroupMany
element names are no longer prefixed with "ns:" namespace.



5.0 Platform Support

This fix is supported on all platforms supported by 
webMethods 1SYNC Module 6.5.2.



6.0 Installation

Install the fix using the Software AG Update Manager.
For instructions, see Using the Software AG Update Manager
located either in the _documentation directory or on the 
documentation Web site at http://documentation.softwareag.com.



7.0 Uninstall

Uninstall the fix using the Software AG Update Manager.
For instructions, see Using the Software AG Update Manager.

NOTE: This procedure can only be used to uninstall the most
recently installed fix. This action will revert your installation
to the previously installed fix. You cannot use this procedure to
uninstall a previously installed fix.


8.0 Cautions and Warnings

None.



9.0 Globalization

This fix conforms to the internationalization standards of the
webMethods product suite and includes support for operation in
any country, locale, or language as specified in the webMethods
Installation Guide. It was not tested with non-English
configurations and non-ASCII data. However, this fix has no
globalization impact and can be applied to systems running in 
any supported locale or configuration.


9.1 Localization

This fix does not require an updated Language Pack. It might
contain new messages and these messages will appear in English.



10.0 Copyright

Copyright ? 2011  Software AG, Darmstadt, Germany and/or 
Software AG USA, Inc., Reston, VA, United States of America,
and/or their licensors.

Detailed information on trademarks and patents owned by 
Software AG and/or its subsidiaries is located at 
http://documentation.softwareag.com/legal/.

Use of this software is subject to adherence to Software AG?s 
licensing conditions and terms. These terms are part of the 
product documentation, located at 
http://documentation.softwareag.com/legal/ and/or in the root 
installation directory of the licensed product(s).

This software may include portions of third-party products.  For 
third-party copyright notices and license terms, please refer to
"License Texts, Copyright Notices and Disclaimers of Third Party
Products." This document is part of the product documentation,
located at http://documentation.softwareag.com/legal/ and/or in 
the root installation directory of the licensed product(s).



11.0 Contacting Us

Authorized technical support contacts can reach Software AG
Global Support in the following ways:

  Web: https://empower.softwareag.com (online support center)
  
  E-mail: empower@softwareag.com
  
You can find complete contact information in our Global Support
Contact Directory at:

https://empower.softwareag.com/public_directory.asp

You can also visit our Software AG Developer Communities to access 
additional articles, demos, and tutorials, technical information, 
samples, useful resources, online discussion forums moderated by 
Software AG professionals, and more at:

http://communities.softwareag.com/ecosystem/communities/public/index.html