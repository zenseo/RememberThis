RememberThis
================================================================================

Remember list for MODX Revolution.

Features:
--------------------------------------------------------------------------------
RememberThis is small session based remembering snippet solution for MODX 
Revolution. It displays the session based list and a link to add elements to
the list.

The data added to the list could be retreived from MODX resources or from xPDO 
packages. If the added data is retreived from xPDO package, the row is 
referenced by the primary key of the class.

Adding and removing elements from the list could be made by url params or by 
AJAX. A jQuery AJAX script is used by default.

Installation:
--------------------------------------------------------------------------------
MODX Package Management

Usage:
--------------------------------------------------------------------------------

Most of the snippet template settings should be made in the MODX system settings
and are used in snippet and ajax mode.

The package contains two snippets and a formit hook, that use the following
parameters:

RememberThisAdd
---------------

Property | Description                                | Default
-------- | ------------------------------------------ | -------
addTpl   | Template for the add link.                 | tplRememberThisAdd
addId    | This value (and the correspondenting data) | Current resource id
         | is added to the list.                      |

RememberThisList
----------------

Property     | Description                                       | Default
------------ | ------------------------------------------------- | -------
rowTpl       | Row template for the list output.                 | tplRememberThisRow
outerTpl     | Outer template for the list output, if the list   | tplRememberThisOuter
             | is not empty.                                     |
noResultsTpl | Template that is displayed, if the list is empty. | tplRememberThisNoResults
scriptTpl    | Template for the javascript call.                 | tplRememberThisScript

RememberThis (FormIt hook)
----------------

Property | Description                                     | Default
-------- | ----------------------------------------------- | -------
rowTpl   | Row template for the list output.               | tplRememberThisRow
outerTpl | Outer template for the list output, if the list | tplRememberThisOuter
         | is not empty.                                   |

System Settings
---------------

Property       | Description                                       | Default
-------------- | ------------------------------------------------- | -------
rowTpl         | Row template for the list output.                 | tplRememberThisRow
outerTpl       | Outer template for the list output, if the list   | tplRememberThisOuter
               | is not empty. Will be surrounded by a div with    |
               | class 'rememberthis'                              |
addTpl         | Template for the add link.                        | tplRememberThisAdd
noResultsTpl   | Template that is displayed, if the list is empty. | tplRememberThisNoResults
itemTitleTpl   | Template for one list item.                       | tplRememberThisItemTitle
ajaxLoaderImg  | Image file, that is shown during AJAX requests.   | FontAwesome fa-refresh
tvPrefix       | Prefix for template variables in template chunks. | tv.
addQuery       | Query key, used to add elements to the list.      | add
deleteQuery    | Query key, used to remove elements from the list. | delete
language       | Snippet language.                                 | en
packagename    | xPDO package name where the added data is         |
               | retreived from. If empty, the data is retrieved   |
               | from resources. The data row is selected by the   |
               | id column of the package or ModResource.          | -
classname      | xPDO class name where the added data is           |
               | retreived from.                                   | -
joins          | Joins defined in the xPDO class, to retreive      |
               | the added data.                                   | -
jQueryPath     | Path to jQuery script.                            | -
includeScripts | Include javascripts (at the end of the body).     | yes
includeCss     | Include css (at the end of the head).             | yes
debug          | Display debug informations.                       | no

The following templating system settings could be overridden in the snippet calls:
rowTpl, outerTpl, addTpl, noResultsTpl

In template chunks all resource fields of the MODX resources could be used as
placeholder including template variables with the prefix 'tv.' could be used. 
If a xPDO package is used, all fields of this package could be used as
placeholder.
