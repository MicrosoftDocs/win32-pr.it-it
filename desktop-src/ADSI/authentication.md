---
title: Autenticazione (ADSI)
description: In ADSI le credenziali che sono costituite da un nome utente e una password vengono utilizzate per fornire o limitare l'accesso agli oggetti nel servizio directory.
ms.assetid: eef6451d-ebb8-4e22-84f4-61b8be73068a
ms.tgt_platform: multiple
keywords:
- Autenticazione ADSI
- ADSI, uso, autenticazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad32b2f32f115b20c99e47578ad76b73ad72a123
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "104472275"
---
# <a name="authentication-adsi"></a><span data-ttu-id="3b4d1-105">Autenticazione (ADSI)</span><span class="sxs-lookup"><span data-stu-id="3b4d1-105">Authentication (ADSI)</span></span>

<span data-ttu-id="3b4d1-106">In ADSI le credenziali che sono costituite da un nome utente e una password vengono utilizzate per fornire o limitare l'accesso agli oggetti nel servizio directory.</span><span class="sxs-lookup"><span data-stu-id="3b4d1-106">In ADSI, credentials that consist of a user name and password are used to provide or restrict access to objects in the directory service.</span></span> <span data-ttu-id="3b4d1-107">La funzione [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) usa le credenziali del thread chiamante per l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="3b4d1-107">The [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) function uses the credentials of the calling thread for authentication.</span></span> <span data-ttu-id="3b4d1-108">È possibile usare la funzione [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) e il metodo [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) per specificare credenziali diverse da quelle del thread chiamante.</span><span class="sxs-lookup"><span data-stu-id="3b4d1-108">The [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) function and [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) method can be used to specify credentials other than those of the calling thread.</span></span> <span data-ttu-id="3b4d1-109">Quando un oggetto è associato a un utente autenticato, l'utente può accedere all'oggetto come supportato dai requisiti di sicurezza del servizio directory sottostante.</span><span class="sxs-lookup"><span data-stu-id="3b4d1-109">When an object is bound to with an authenticated user, the user is allowed access to the object as supported by the underlying directory service security requirements.</span></span>

> [!Note]  
> <span data-ttu-id="3b4d1-110">La funzione [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) e il metodo [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) non devono essere usati per convalidare le credenziali utente.</span><span class="sxs-lookup"><span data-stu-id="3b4d1-110">The [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) function and [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) method should not be used to validate user credentials.</span></span> <span data-ttu-id="3b4d1-111">Per ulteriori informazioni sulla convalida delle credenziali utente, vedere l'articolo 180548 della Microsoft Knowledge base [: convalidare le credenziali utente nei sistemi operativi Microsoft](https://support.microsoft.com/kb/180548).</span><span class="sxs-lookup"><span data-stu-id="3b4d1-111">For more information about validating user credentials, see Microsoft Knowledge Base article 180548 [HOWTO: Validate User Credentials on Microsoft Operating Systems](https://support.microsoft.com/kb/180548).</span></span>

 

<span data-ttu-id="3b4d1-112">Nell'esempio di codice seguente viene illustrato come utilizzare il metodo [**OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) per autenticare un utente.</span><span class="sxs-lookup"><span data-stu-id="3b4d1-112">The following code example shows how to use the [**OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) method to authenticate a user.</span></span>


```VB
Dim MyNamespace As IADsOpenDSObject
Dim X
oUsername="MyUserName"
oPassword="MyPassword"

OnError GoTo CleanuUp
 
Set MyNamespace = GetObject("LDAP:")

' For authentication, pass a variable for the user name and password to be used for 
' authentication. For security reasons, it is recommended that you use the ADS_SECURE_AUTHENTICATION flag.
' 
Set X = MyNamespace.OpenDSObject(DN, oUserName, oPassword, ADS_SECURE_AUTHENTICATION)     

CleanUp:
    MsgBox ("An error has occurred.")
    Set MyNamespace = Nothing
    Set X = Nothing
```



 

 




