---
description: Gli oggetti Active Directory possono essere usati per individuare le risorse in un dominio di rete del computer, ad esempio utenti, criteri di sicurezza, stampanti, componenti distribuiti e altre risorse.
ms.assetid: 96f89537-9419-495e-819c-fd07ba546620
ms.tgt_platform: multiple
title: Creazione e aggiornamento di oggetti Active Directory
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0e2b1cee8010a5eff143fc7ff073eeea5e83b3b46cb41177e5ddbde5e931e056
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119374831"
---
# <a name="creating-and-updating-active-directory-objects"></a>Creazione e aggiornamento di oggetti Active Directory

Gli oggetti Active Directory possono essere usati per individuare le risorse in un dominio di rete del computer, ad esempio utenti, criteri di sicurezza, stampanti, componenti distribuiti e altre risorse. Gli oggetti Active Directory possono essere creati e aggiornati tramite WMI. È possibile aggiornare un oggetto di Active Directory quando diventano disponibili nuove informazioni sull'oggetto usando la notifica degli eventi WMI. Ad esempio, dopo aver creato un oggetto utente di Active Directory, è possibile rilevarne la creazione con una query di eventi in WMI e, quando viene ricevuto l'evento, è possibile aggiornare l'oggetto con nuove informazioni.

Nell'esempio di codice seguente viene creata una nuova istanza WMI della classe che rappresenta l'oggetto utente di Active Directory. Nell'esempio viene illustrato come assegnare valori a varie proprietà necessarie per creare la nuova istanza utente di Active Directory.


```VB
Const cUserID = "WMIUser"
Const cComputerName = "LocalHost"
Const cWMInamespace = "root/directory/LDAP"
Const cWMIclass = "ds_user"

Const ADS_UF_ACCOUNTDISABLE = &h000002

Set objWMILocator = _
    CreateObject("WbemScripting.SWbemLocator")
objWMILocator.Security_.AuthenticationLevel = _
    wbemAuthenticationLevelDefault

Set objWMIServices = objWMILocator. _
    ConnectServer(cComputerName, cWMInamespace, "", "")

Set objWMIClass = objWMIServices.Get(cWMIclass)

Set objWMIInstance = objWMIClass.SpawnInstance_

objWMIInstance.DS_sAMAccountName = userID
objWMIInstance.ADSIPath = "LDAP://CN=" & userID & _
    ",CN=Users,DC=LissWare,DC=Net"

objWMIInstance.Put_ (wbemChangeFlagCreateOrUpdate Or _
    wbemFlagReturnWhenComplete)

WScript.Echo "Active Directory user created."
```



Nell'esempio di codice seguente viene aggiornata un'istanza WMI di un oggetto Active Directory. In questo esempio l'attributo displayname viene aggiornato.


```VB
set svc = getObject("Winmgmts:root\directory\ldap")

' A context object is used to tell the provider which
' specific properties are going to be updated.  
' In most cases, when you update a WMI object you do not
' need to specify an additional context object. 
' However,  if a context object is not supplied for a
' directory service provider, the update fails.

set octx = createobject( _
    "wbemscripting.swbemnamedvalueset")
octx.add "__PUT_EXT_PROPERTIES", array("ds_displayname")
octx.add "__PUT_EXTENSIONS", true
octx.add "__PUT_EXT_CLIENT_REQUEST", true


set objEnum = svc.execQuery( _
    "select * from ds_computer where ds_cn = 'userName'", "WQL", 32)

for each obj in objEnum
 obj.ds_DisplayName = "updatedName"
 obj.put_ 1, octx
next

WScript.Echo "Active Directory user successfully updated"
```



 

 



