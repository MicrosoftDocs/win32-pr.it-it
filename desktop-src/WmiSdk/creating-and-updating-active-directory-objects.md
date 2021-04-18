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
# <a name="creating-and-updating-active-directory-objects"></a><span data-ttu-id="ac88a-103">Creazione e aggiornamento di oggetti Active Directory</span><span class="sxs-lookup"><span data-stu-id="ac88a-103">Creating and Updating Active Directory Objects</span></span>

<span data-ttu-id="ac88a-104">È possibile utilizzare gli oggetti Active Directory per individuare le risorse in un dominio di rete del computer, ad esempio utenti, criteri di sicurezza, stampanti, componenti distribuiti e altre risorse.</span><span class="sxs-lookup"><span data-stu-id="ac88a-104">Active Directory objects can be used to locate resources in a computer network domain, such as users, security policies, printers, distributed components, and other resources.</span></span> <span data-ttu-id="ac88a-105">Active Directory gli oggetti possono essere creati e aggiornati tramite WMI.</span><span class="sxs-lookup"><span data-stu-id="ac88a-105">Active Directory objects can be created and updated using WMI.</span></span> <span data-ttu-id="ac88a-106">È possibile aggiornare un oggetto Active Directory quando le nuove informazioni sull'oggetto diventano disponibili tramite la notifica degli eventi WMI.</span><span class="sxs-lookup"><span data-stu-id="ac88a-106">You can update an Active Directory object when new information about the object becomes available by using WMI event notification.</span></span> <span data-ttu-id="ac88a-107">Ad esempio, dopo aver creato un Active Directory oggetto utente, è possibile rilevare la relativa creazione con una query di eventi in WMI e quando viene ricevuto l'evento, è possibile aggiornare l'oggetto con nuove informazioni.</span><span class="sxs-lookup"><span data-stu-id="ac88a-107">For example, once an Active Directory user object is created, you can detect its creation with an event query in WMI and when the event is received, you can update the object with new information.</span></span>

<span data-ttu-id="ac88a-108">Nell'esempio di codice seguente viene creata una nuova istanza WMI della classe che rappresenta l'oggetto Active Directory utente.</span><span class="sxs-lookup"><span data-stu-id="ac88a-108">The following code example creates a new WMI instance of the class that represents the Active Directory user object.</span></span> <span data-ttu-id="ac88a-109">Nell'esempio viene illustrato come assegnare valori a diverse proprietà necessarie per creare la nuova istanza di Active Directory utente.</span><span class="sxs-lookup"><span data-stu-id="ac88a-109">The example shows how to assign values to various properties required to create the new Active Directory user instance.</span></span>


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



<span data-ttu-id="ac88a-110">Nell'esempio di codice seguente viene aggiornata un'istanza WMI di un oggetto Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ac88a-110">The following code example updates a WMI instance of an Active Directory object.</span></span> <span data-ttu-id="ac88a-111">In questo esempio, l'attributo DisplayName viene aggiornato.</span><span class="sxs-lookup"><span data-stu-id="ac88a-111">In this example, the displayname attribute is updated.</span></span>


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



 

 



