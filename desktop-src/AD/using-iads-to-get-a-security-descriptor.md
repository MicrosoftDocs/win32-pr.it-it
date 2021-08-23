---
title: Uso di IAD per ottenere un descrittore di sicurezza
description: Negli esempi di codice seguenti viene utilizzato il metodo Get IADs per recuperare un puntatore IADsSecurityDescriptor alla proprietà nTSecurityDescriptor di un oggetto in Active Directory Domain Services.
ms.assetid: ce8948ac-0644-42a0-8b77-5a06d3fcf042
ms.tgt_platform: multiple
keywords:
- Esempi di Active Directory Active Directory, uso di IAD per ottenere un descrittore di sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24ecf0d8921e797a4d226d472f34b3172a01d9fb67d96ca61e9f0b491a7f7851
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024519"
---
# <a name="using-iads-to-get-a-security-descriptor"></a>Uso di IAD per ottenere un descrittore di sicurezza

Negli esempi di codice seguenti viene utilizzato il metodo [**IADs::Get**](/windows/desktop/api/iads/nf-iads-iads-get) per recuperare un puntatore [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) alla proprietà **nTSecurityDescriptor** di un oggetto in Active Directory Domain Services.


```VB
Dim rootDSE As IADs
Dim ADUser As IADs
Dim sd As IADsSecurityDescriptor

On Error GoTo Cleanup
 
' Bind to the Users container in the local domain.
Set rootDSE = GetObject("LDAP://rootDSE")
Set ADUser = GetObject("LDAP://cn=users," & rootDSE.Get("defaultNamingContext"))
 
' Get the security descriptor on the Users container.
Set sd = ADUser.Get("ntSecurityDescriptor")
Debug.Print sd.Control
Debug.Print sd.Group
Debug.Print sd.Owner
Debug.Print sd.Revision

Exit Sub

Cleanup:
    Set rootDSE = Nothing
    Set ADUser = Nothing
    Set sd = Nothing
```




```C++
HRESULT GetSDFromIADs(
                IADs *pObject,
                IADsSecurityDescriptor **ppSD )
{
    VARIANT var;
    HRESULT hr;

    if(!pObject || !ppSD)
    {
        return E_INVALIDARG;
    }
 
    // Set *ppSD to NULL.
    *ppSD = NULL;
    
    VariantInit(&var);
 
    // Get the nTSecurityDescriptor.
    hr = pObject->Get(CComBSTR("nTSecurityDescriptor"), &var);
    if (SUCCEEDED(hr))
    {
        // Type should be VT_DISPATCH - an IDispatch pointer to the security descriptor object.
        if (var.vt == VT_DISPATCH)
        { 
            // Use V_DISPATCH macro to get the IDispatch pointer from the 
            // VARIANT structure and QueryInterface for the IADsSecurityDescriptor pointer.
            hr = V_DISPATCH(&var)->QueryInterface(IID_IADsSecurityDescriptor, (void**)ppSD);
        }
        else
        {
            hr = E_FAIL;
        }
    }

    VariantClear(&var);
    return hr;
}
```



 

 