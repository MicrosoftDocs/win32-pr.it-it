---
title: Codice di esempio per l'associazione al contenitore dell'utente
description: Questo argomento include un esempio di codice che verrà associato al contenitore Users nel dominio corrente e restituirà l'interfaccia IADsContainer per il contenitore.
ms.assetid: 78524b05-f57a-4816-92eb-e37be74dd245
ms.tgt_platform: multiple
keywords:
- Esempi di Active Directory Active Directory, associazione al contenitore dell'utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8db1ccb3d2331c4ccef5bbf28f58fa5c046337c7
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104046513"
---
# <a name="example-code-for-binding-to-the-users-container"></a>Codice di esempio per l'associazione al contenitore dell'utente

Nell'esempio di codice C++ riportato di seguito viene associato al contenitore Users nel dominio corrente e viene restituita l'interfaccia [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) per il contenitore. Per altre informazioni sull'associazione a oggetti noti, vedere [associazione a oggetti di Well-Known con WKGUID](binding-to-well-known-objects-using-wkguid.md).


```C++
//**********************************************************
//
//  GetUsersContainer()
//
//  Binds to the well-known Users container in the current domain 
//  with the current user credentials. GUID_USERS_CONTAINER_W is 
//  defined in NTDSAPI.H.
//
//*******************************************************************

HRESULT GetUsersContainer(IADsContainer **ppContainer)
{
    if(NULL == ppContainer)
    {
        return E_INVALIDARG;
    }

    HRESULT hr;
    IADs *pRoot;

    *ppContainer = NULL;

    // Bind to the rootDSE object.
    hr = ADsOpenObject(L"LDAP://rootDSE",
                    NULL,
                    NULL,
                    ADS_SECURE_AUTHENTICATION,
                    IID_IADs,
                    (LPVOID*)&pRoot);
    if(SUCCEEDED(hr))
    {
        VARIANT var;
        
        VariantInit(&var);

        // Get the current domain DN.
        hr = pRoot->Get(CComBSTR("defaultNamingContext"), &var);
        if(SUCCEEDED(hr))
        {
            // Build the binding string.
            LPWSTR pwszFormat = L"LDAP://<WKGUID=%s,%s>";
            LPWSTR pwszPath;

            pwszPath = new WCHAR[wcslen(pwszFormat) + 
                           wcslen(GUID_USERS_CONTAINER_W) + 
                           wcslen(var.bstrVal)];
            if(NULL != pwszPath)
            {
                swprintf_s(pwszPath, 
                         pwszFormat, 
                         GUID_USERS_CONTAINER_W,
                         var.bstrVal);

                // Bind to the object.
                hr = ADsOpenObject(pwszPath,
                                NULL,
                                NULL,
                                ADS_SECURE_AUTHENTICATION,
                                IID_IADsContainer,
                                (LPVOID*)ppContainer);

                delete pwszPath;
            }
            else
            {
                hr = E_OUTOFMEMORY;
            }

            VariantClear(&var);        
        }

        pRoot->Release(); 
    }

    return hr;
}
```



 

 