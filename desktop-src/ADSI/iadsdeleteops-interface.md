---
title: Interfaccia IADsDeleteOps
description: L'interfaccia IADsDeleteOps viene usata nelle routine di supervisione e manutenzione per l'archivio directory sottostante. Può eliminare gli oggetti foglia e interi sottoalberi in una singola operazione.
ms.assetid: 821b71c2-e9f5-4ca8-9366-e8a3f1907670
ms.tgt_platform: multiple
keywords:
- Interfaccia IADsDeleteOps ADSI
- IADsDeleteOps ADSI , con
- ADSI ADSI , codice di esempio C/C++, uso di IADsDeleteOps per eliminare interi gruppi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 192411e53f54de2a5f73cc043f35cea6787f4b879972b6a69ada4760c175292a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117839944"
---
# <a name="iadsdeleteops-interface"></a>Interfaccia IADsDeleteOps

[**L'interfaccia IADsDeleteOps**](/windows/desktop/api/Iads/nn-iads-iadsdeleteops) viene usata nelle routine di supervisione e manutenzione per l'archivio directory sottostante. Può eliminare gli oggetti foglia e interi sottoalberi in una singola operazione.

Se questa interfaccia non fosse supportata, l'eliminazione di un oggetto da Active Directory richiederebbe che ogni oggetto contenuto sia enumerato ed eliminato in modo ricorsivo. Con questa interfaccia, qualsiasi oggetto contenitore, con tutti i relativi oggetti e sottooggetti contenuti, può essere eliminato con una singola operazione.

L'esempio di codice seguente elimina il contenitore "Eng" e tutti gli oggetti figlio.


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



L'esempio di codice seguente elimina il contenitore "Eng" e tutti gli oggetti figlio.


```VB
Dim DeleteOps As IADsDeleteOps

' Bind to the LDAP provider.
Set DeleteOps = GetObject("LDAP://CN=Eng,CN=Users,DC=Fabrikam,DC=Com")

' Delete the container and all child objects.
DeleteOps.DeleteObject (0)
```



 

 




