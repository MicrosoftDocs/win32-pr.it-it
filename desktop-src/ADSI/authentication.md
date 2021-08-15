---
title: Autenticazione (ADSI)
description: In ADSI le credenziali costituite da un nome utente e una password vengono usate per fornire o limitare l'accesso agli oggetti nel servizio directory.
ms.assetid: eef6451d-ebb8-4e22-84f4-61b8be73068a
ms.tgt_platform: multiple
keywords:
- Autenticazione ADSI
- ADSI, uso, autenticazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19177153d8d66f3c27db5c0c2027faa2e02b213305d760d070f5af90b6ba1058
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117840558"
---
# <a name="authentication-adsi"></a>Autenticazione (ADSI)

In ADSI le credenziali costituite da un nome utente e una password vengono usate per fornire o limitare l'accesso agli oggetti nel servizio directory. La [**funzione ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) usa le credenziali del thread chiamante per l'autenticazione. La [**funzione ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) e il metodo [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) possono essere usati per specificare credenziali diverse da quelle del thread chiamante. Quando un oggetto è associato a con un utente autenticato, l'utente può accedere all'oggetto come supportato dai requisiti di sicurezza del servizio directory sottostanti.

> [!Note]  
> La [**funzione ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) e [**il metodo IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) non devono essere usati per convalidare le credenziali utente. Per altre informazioni sulla convalida delle credenziali utente, vedere Microsoft Knowledge Base articolo 180548 [HOWTO: Convalidare le credenziali utente nei sistemi operativi Microsoft](https://support.microsoft.com/kb/180548).

 

Nell'esempio di codice seguente viene illustrato come usare il [**metodo OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) per autenticare un utente.


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



 

 




