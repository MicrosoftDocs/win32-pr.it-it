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
# <a name="authentication-adsi"></a>Autenticazione (ADSI)

In ADSI le credenziali che sono costituite da un nome utente e una password vengono utilizzate per fornire o limitare l'accesso agli oggetti nel servizio directory. La funzione [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) usa le credenziali del thread chiamante per l'autenticazione. È possibile usare la funzione [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) e il metodo [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) per specificare credenziali diverse da quelle del thread chiamante. Quando un oggetto è associato a un utente autenticato, l'utente può accedere all'oggetto come supportato dai requisiti di sicurezza del servizio directory sottostante.

> [!Note]  
> La funzione [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) e il metodo [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) non devono essere usati per convalidare le credenziali utente. Per ulteriori informazioni sulla convalida delle credenziali utente, vedere l'articolo 180548 della Microsoft Knowledge base [: convalidare le credenziali utente nei sistemi operativi Microsoft](https://support.microsoft.com/kb/180548).

 

Nell'esempio di codice seguente viene illustrato come utilizzare il metodo [**OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) per autenticare un utente.


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



 

 




