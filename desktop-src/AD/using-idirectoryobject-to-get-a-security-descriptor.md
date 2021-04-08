---
title: Uso di IDirectoryObject per ottenere un descrittore di sicurezza
description: Questo argomento include un esempio di codice usato per ottenere un descrittore di sicurezza.
ms.assetid: 989abd3f-9043-4c3f-a99a-63fa95daf203
ms.tgt_platform: multiple
keywords:
- Esempi di Active Directory Active Directory, uso di IDirectoryObject per ottenere un descrittore di sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 562438d37d6bfadadfee95d13f80cb4c4728e0f2
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724391"
---
# <a name="using-idirectoryobject-to-get-a-security-descriptor"></a>Uso di IDirectoryObject per ottenere un descrittore di sicurezza

Questo argomento include un esempio di codice usato per ottenere un descrittore di sicurezza.

Nell'esempio di codice C++ riportato di seguito:

-   Crea un buffer.
-   Usa l'interfaccia [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) per ottenere il descrittore di sicurezza dell'oggetto specificato.
-   Copia il descrittore di sicurezza nel buffer.
-   Restituisce un puntatore a una struttura di [**\_ descrittore di sicurezza**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) che contiene i dati del descrittore di sicurezza.


```C++
HRESULT GetSDFromIDirectoryObject(
    IDirectoryObject *pObject,
    PSECURITY_DESCRIPTOR *pSecurityDescriptor)
{
    HRESULT hr = E_FAIL;
    PADS_ATTR_INFO pAttrInfo;
    DWORD dwReturn= 0;
    LPWSTR pAttrName= L"nTSecurityDescriptor";
    PSECURITY_DESCRIPTOR pSD = NULL;

    if(!pObject || !pSecurityDescriptor)
    {
        return E_INVALIDARG;
    }
 
    // Get the nTSecurityDescriptor.
    hr = pObject->GetObjectAttributes( &pAttrName, 
                                       1, 
                                       &pAttrInfo, 
                                       &dwReturn );
    if((FAILED(hr)) || (dwReturn != 1)) 
    {
        wprintf(L" failed: 0x%x\n", hr);
        return hr;
    }
 
    // Check the attribute name and type.
    if((_wcsicmp(pAttrInfo->pszAttrName,L"nTSecurityDescriptor") == 0) &&
     (pAttrInfo->dwADsType==ADSTYPE_NT_SECURITY_DESCRIPTOR))
    {
        // Get a pointer to the security descriptor.
        pSD = (PSECURITY_DESCRIPTOR)(pAttrInfo->pADsValues->SecurityDescriptor.lpValue);
               
        DWORD SDSize = pAttrInfo->pADsValues->SecurityDescriptor.dwLength;
               
        // Allocate memory for the buffer and copy the security descriptor to the buffer.
        *pSecurityDescriptor = (PSECURITY_DESCRIPTOR)CoTaskMemAlloc(SDSize);
        if (*pSecurityDescriptor)
        {
            CopyMemory((PVOID)*pSecurityDescriptor, (PVOID)pSD, SDSize);
        }
        else
        {
            hr = E_FAIL;
        }

        // Caller must free the memory for pSecurityDescriptor using CoTaskMemFree.
    }
 
    // Free memory used for the attributes retrieved.
    FreeADsMem(pAttrInfo); 
 
    return hr;
}
```



 

 