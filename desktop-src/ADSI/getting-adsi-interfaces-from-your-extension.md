---
title: Recupero di interfacce ADSI dall'estensione
description: Un'estensione deve spesso ottenere dati dall'oggetto directory a cui esegue l'associazione.
ms.assetid: 2d2e6dc6-1eed-491b-9d6a-7f35c24a7ba8
ms.tgt_platform: multiple
keywords:
- estensioni ADSI, recupero di interfacce ADSI dall'estensione
- ADSI ADSI , codice di esempio C/C++ , recupero di interfacce ADSI dall'estensione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41df2498bd0c25996cfd0941f823e414289c0a9fbe006df846960c6f455e4301
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118179731"
---
# <a name="getting-adsi-interfaces-from-your-extension"></a>Recupero di interfacce ADSI dall'estensione

Un'estensione deve spesso ottenere dati dall'oggetto directory a cui esegue l'associazione. Ad esempio, un'estensione per un **oggetto computer** potrebbe voler ottenere **il dnsHostName** dell'oggetto corrente dalla directory. A tale scopo, è possibile eseguire facilmente una **chiamata QueryInterface** sull'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) per l'aggregatore.


```C++
HRESULT hr;
IADs *pADs; ' ADSI Interface to get/set attributes.
 
hr = m_pOuterUnk->QueryInterface(IID_IADs,(void**)&pADs);
 
if ( SUCCEEDED(hr) )
{
    VARIANT var;
    VariantInit(&var);
    hr  = pADs ->Get(_bstr_t("dnsHostName"), &var);
    if ( SUCCEEDED(hr) )
    { 
        printf("%S\n", V_BSTR(&var));
    }
    VariantClear(&var);
    pADs->Release();
}
```



È consigliabile rilasciare l'interfaccia immediatamente dopo l'uso. Se l'estensione ha un riferimento aperto all'aggregatore, è stato creato un riferimento circolare e l'aggregatore non può rilasciare l'estensione. Pertanto, l'aggregatore non può essere rilasciato e il risultato è una perdita di memoria nell'applicazione.

 

 