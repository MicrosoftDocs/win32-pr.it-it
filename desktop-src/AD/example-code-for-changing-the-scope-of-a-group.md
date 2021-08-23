---
title: Codice di esempio per la modifica dell'ambito di un gruppo
description: Questo argomento contiene codice di esempio per la modifica dell'ambito di un gruppo.
ms.assetid: 4ae61101-f123-44bd-8bec-bade51d22217
ms.tgt_platform: multiple
keywords:
- Esempi di Active Directory Active Directory, modifica dell'ambito di un gruppo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edbcbfb7e665b4f569fdef6d623bd7bfb947f94ece1de26ee062a70b07757300
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118694544"
---
# <a name="example-code-for-changing-the-scope-of-a-group"></a>Codice di esempio per la modifica dell'ambito di un gruppo

L'esempio di codice C++ seguente modifica l'ambito di un gruppo.


```C++

    WCHAR *pwszLDAPPath = 
        L"LDAP://CN=mygroup,OU=myou,DC=Fabrikam,DC=com";
 
    HRESULT hr;
    IADsGroup * pGroup = NULL;
 
    // Initialize COM.
    CoInitialize(0);
 
    // Bind to the passed container. 
    hr = ADsGetObject( pwszLDAPPath, IID_IADsGroup,(void **)&pGroup);
 
    if (SUCCEEDED(hr))
    {
        VARIANT vValue;
        BSTR    bsValue = SysAllocString(L"groupType");
        VariantInit(&vValue);
    // Set a new GroupType Value.
        vValue.vt = VT_I4;
        vValue.lVal = ADS_GROUP_TYPE_GLOBAL_GROUP ;
 
        hr = pGroup->Put(bsValue,vValue);
        hr = pGroup->SetInfo();
        pGroup->Release();
        pGroup= NULL;
        SysFreeString(bsValue);
    }
 
    CoUninitialize();
```



Nell'esempio Visual Basic di codice seguente viene modificato l'ambito di un gruppo.


```VB
Dim x as IADs
On Error GoTo CleanUp
Set x = GetObject("LDAP://CN=mygroup,OU=myou,DC=Fabrikam,DC=com")
x.Put "groupType", 
    ADS_GROUP_TYPE_UNIVERSAL_GROUP|ADS_GROUP_TYPE_SECURITY_ENABLED
Exit Sub

CleanUp:
    MsgBox("An error has occurred.")
    x = Nothing
```



 

 




