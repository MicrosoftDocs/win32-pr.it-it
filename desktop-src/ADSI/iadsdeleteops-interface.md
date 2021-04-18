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
# <a name="iadsdeleteops-interface"></a><span data-ttu-id="d55a3-107">Interfaccia IADsDeleteOps</span><span class="sxs-lookup"><span data-stu-id="d55a3-107">IADsDeleteOps Interface</span></span>

<span data-ttu-id="d55a3-108">L'interfaccia [**IADsDeleteOps**](/windows/desktop/api/Iads/nn-iads-iadsdeleteops) viene utilizzata nelle routine di supervisione e manutenzione per l'archivio directory sottostante.</span><span class="sxs-lookup"><span data-stu-id="d55a3-108">The [**IADsDeleteOps**](/windows/desktop/api/Iads/nn-iads-iadsdeleteops) interface is used in supervisory and maintenance routines for the underlying directory store.</span></span> <span data-ttu-id="d55a3-109">Può eliminare oggetti foglia e sottoalberi interi in un'unica operazione.</span><span class="sxs-lookup"><span data-stu-id="d55a3-109">It can delete leaf objects and entire subtrees in a single operation.</span></span>

<span data-ttu-id="d55a3-110">Se questa interfaccia non è supportata, l'eliminazione di un oggetto da Active Directory richiede che ogni oggetto contenuto venga enumerato ed eliminato in modo ricorsivo.</span><span class="sxs-lookup"><span data-stu-id="d55a3-110">If this interface were not supported, deleting an object from Active Directory would require that each contained object be recursively enumerated and deleted.</span></span> <span data-ttu-id="d55a3-111">Con questa interfaccia, qualsiasi oggetto contenitore, con tutti i relativi oggetti contenuti e i relativi oggetti, può essere eliminato con una singola operazione.</span><span class="sxs-lookup"><span data-stu-id="d55a3-111">With this interface, any container object, with all its contained objects and subobjects, can be deleted with a single operation.</span></span>

<span data-ttu-id="d55a3-112">Nell'esempio di codice seguente vengono eliminati il contenitore "ENG" e tutti gli oggetti figlio.</span><span class="sxs-lookup"><span data-stu-id="d55a3-112">The following code example deletes the "Eng" container and all child objects.</span></span>


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



<span data-ttu-id="d55a3-113">Nell'esempio di codice seguente vengono eliminati il contenitore "ENG" e tutti gli oggetti figlio.</span><span class="sxs-lookup"><span data-stu-id="d55a3-113">The following code example deletes the "Eng" container and all child objects.</span></span>


```VB
Dim DeleteOps As IADsDeleteOps

' Bind to the LDAP provider.
Set DeleteOps = GetObject("LDAP://CN=Eng,CN=Users,DC=Fabrikam,DC=Com")

' Delete the container and all child objects.
DeleteOps.DeleteObject (0)
```



 

 




