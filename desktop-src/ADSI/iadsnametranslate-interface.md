---
title: Interfaccia IADsNameTranslate
description: L'interfaccia IADsNameTranslate viene utilizzata per tradurre i nomi distinti tra i vari formati. Le conversioni dei nomi vengono eseguite nel server di directory e questa interfaccia è attualmente disponibile solo per gli oggetti in Active Directory.
ms.assetid: c5c6e821-f19b-4269-81de-34c79dd2731f
ms.tgt_platform: multiple
keywords:
- Interfaccia IADsNameTranslate ADSI
- IADsTranslate ADSI, utilizzo
- ADSI ADSI, codice di esempio C/C++, uso di IADsTranslate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7ff5b44288289f118c41463a22e619aa815ecb2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855297"
---
# <a name="iadsnametranslate-interface"></a>Interfaccia IADsNameTranslate

L'interfaccia [**IADsNameTranslate**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate) viene utilizzata per tradurre i nomi distinti tra i vari formati. Le conversioni dei nomi vengono eseguite nel server di directory e questa interfaccia è attualmente disponibile solo per gli oggetti in Active Directory.

Nell'esempio di codice seguente un nome di account viene convertito dal formato Windows al formato LDAP.


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



 

 




