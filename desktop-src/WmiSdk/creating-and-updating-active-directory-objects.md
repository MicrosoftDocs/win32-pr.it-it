---
description: È possibile utilizzare gli oggetti Active Directory per individuare le risorse in un dominio di rete del computer, ad esempio utenti, criteri di sicurezza, stampanti, componenti distribuiti e altre risorse.
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
ms.openlocfilehash: 0b36a12860ea2c2dc9085b784fdaf85cd95ab87f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310389"
---
# <a name="creating-and-updating-active-directory-objects"></a>Creazione e aggiornamento di oggetti Active Directory

È possibile utilizzare gli oggetti Active Directory per individuare le risorse in un dominio di rete del computer, ad esempio utenti, criteri di sicurezza, stampanti, componenti distribuiti e altre risorse. Active Directory gli oggetti possono essere creati e aggiornati tramite WMI. È possibile aggiornare un oggetto Active Directory quando le nuove informazioni sull'oggetto diventano disponibili tramite la notifica degli eventi WMI. Ad esempio, dopo aver creato un Active Directory oggetto utente, è possibile rilevare la relativa creazione con una query di eventi in WMI e quando viene ricevuto l'evento, è possibile aggiornare l'oggetto con nuove informazioni.

Nell'esempio di codice seguente viene creata una nuova istanza WMI della classe che rappresenta l'oggetto Active Directory utente. Nell'esempio viene illustrato come assegnare valori a diverse proprietà necessarie per creare la nuova istanza di Active Directory utente.


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



Nell'esempio di codice seguente viene aggiornata un'istanza WMI di un oggetto Active Directory. In questo esempio, l'attributo DisplayName viene aggiornato.


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



 

 



