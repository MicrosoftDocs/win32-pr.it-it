---
title: Interfaccia IADsDeleteOps
description: L'interfaccia IADsDeleteOps viene utilizzata nelle routine di supervisione e manutenzione per l'archivio directory sottostante. Può eliminare oggetti foglia e sottoalberi interi in un'unica operazione.
ms.assetid: 821b71c2-e9f5-4ca8-9366-e8a3f1907670
ms.tgt_platform: multiple
keywords:
- Interfaccia IADsDeleteOps ADSI
- IADsDeleteOps ADSI, utilizzo
- ADSI ADSI, esempio di codice C/C++, uso di IADsDeleteOps per eliminare interi gruppi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6332dd28e903996e8688d6c6fc672df080822595
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297677"
---
# <a name="iadsdeleteops-interface"></a>Interfaccia IADsDeleteOps

L'interfaccia [**IADsDeleteOps**](/windows/desktop/api/Iads/nn-iads-iadsdeleteops) viene utilizzata nelle routine di supervisione e manutenzione per l'archivio directory sottostante. Può eliminare oggetti foglia e sottoalberi interi in un'unica operazione.

Se questa interfaccia non è supportata, l'eliminazione di un oggetto da Active Directory richiede che ogni oggetto contenuto venga enumerato ed eliminato in modo ricorsivo. Con questa interfaccia, qualsiasi oggetto contenitore, con tutti i relativi oggetti contenuti e i relativi oggetti, può essere eliminato con una singola operazione.

Nell'esempio di codice seguente vengono eliminati il contenitore "ENG" e tutti gli oggetti figlio.


```C++
HRESULT hr;
IADsDeleteOps *pDeleteOps;
LPWSTR pwszUsername = NULL;
LPWSTR pwszPassword = NULL;

// Insert code to securely retrieve the pwszUsername and pwszPassword
// or leave as NULL to use the default security context of the 
// calling application.
 
// Bind to the LDAP provider.
hr = ADsOpenObject(L"LDAP://CN=Eng,CN=Users,DC=Fabrikam,DC=Com", 
    pwszUsername,
    pwszPassword,
    0,
    ADS_SECURE_AUTHENTICATION,
    IID_IADsDeleteOps, 
    (void**)&pDeleteOps);
if(S_OK == hr)
{
    // Delete the container and all child objects.
    pDeleteOps->DeleteObject(0);

    // Release the interface.
    pDeleteOps->Release();
}

if(pwszUsername)
{
    SecureZeroMemory(pwszUsername, lstrlen(pwszUsername) * sizeof(TCHAR));
}
if(pwszPassword)
{
    SecureZeroMemory(pwszPassword, lstrlen(pwszPassword) * sizeof(TCHAR));
}
```



Nell'esempio di codice seguente vengono eliminati il contenitore "ENG" e tutti gli oggetti figlio.


```VB
Dim DeleteOps As IADsDeleteOps

' Bind to the LDAP provider.
Set DeleteOps = GetObject("LDAP://CN=Eng,CN=Users,DC=Fabrikam,DC=Com")

' Delete the container and all child objects.
DeleteOps.DeleteObject (0)
```



 

 




