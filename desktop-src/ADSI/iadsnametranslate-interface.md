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
# <a name="iadsnametranslate-interface"></a><span data-ttu-id="55d46-107">Interfaccia IADsNameTranslate</span><span class="sxs-lookup"><span data-stu-id="55d46-107">IADsNameTranslate Interface</span></span>

<span data-ttu-id="55d46-108">L'interfaccia [**IADsNameTranslate**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate) viene utilizzata per tradurre i nomi distinti tra i vari formati.</span><span class="sxs-lookup"><span data-stu-id="55d46-108">The [**IADsNameTranslate**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate) interface is used to translate distinguished names between various formats.</span></span> <span data-ttu-id="55d46-109">Le conversioni dei nomi vengono eseguite nel server di directory e questa interfaccia è attualmente disponibile solo per gli oggetti in Active Directory.</span><span class="sxs-lookup"><span data-stu-id="55d46-109">Name translations are performed on the directory server, and this interface is currently available only to objects in Active Directory.</span></span>

<span data-ttu-id="55d46-110">Nell'esempio di codice seguente un nome di account viene convertito dal formato Windows al formato LDAP.</span><span class="sxs-lookup"><span data-stu-id="55d46-110">The following code example converts an account name from Windows format into LDAP format.</span></span>


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



 

 




