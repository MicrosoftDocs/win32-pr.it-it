---
title: Interfaccia IADsNameTranslate
description: L'interfaccia IADsNameTranslate viene usata per convertire nomi distinti tra vari formati. Le traduzioni dei nomi vengono eseguite nel server di directory e questa interfaccia è attualmente disponibile solo per gli oggetti in Active Directory.
ms.assetid: c5c6e821-f19b-4269-81de-34c79dd2731f
ms.tgt_platform: multiple
keywords:
- Interfaccia IADsNameTranslate ADSI
- IADsTranslate ADSI , con
- ADSI ADSI , codice di esempio C/C++, con IADsTranslate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60e167363e3c35337e74851dc43126593772aac56236f27e10a98a81b533159e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023449"
---
# <a name="iadsnametranslate-interface"></a>Interfaccia IADsNameTranslate

[**L'interfaccia IADsNameTranslate**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate) viene usata per convertire nomi distinti tra vari formati. Le traduzioni dei nomi vengono eseguite nel server di directory e questa interfaccia è attualmente disponibile solo per gli oggetti in Active Directory.

L'esempio di codice seguente converte un nome di account Windows formato LDAP.


```C++
HRESULT TranslateNTNameToLDAPName( BSTR * pNTName, BSTR * pLDAPName )
{
    IADsNameTranslate *pTrans;
    HRESULT hr = S_OK;
 
    hr = CoCreateInstance(CLSID_NameTranslate, 
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IADsNameTranslate,
                          (void**) &pTrans );
    if (FAILED(hr)) { return hr; }

    hr = pTrans->Init(ADS_NAME_INITTYPE_DOMAIN, 
                      CComBSTR("Fabrikam.com"));
    if (FAILED(hr)) { return hr; }

    hr = pTrans->Set(ADS_NAME_TYPE_NT4, *pNTName);
    if (FAILED(hr)) { return hr; }

    hr = pTrans->Get(ADS_NAME_TYPE_1779, pLDAPName);
    pTrans->Release();
    return hr;
}
```



 

 




