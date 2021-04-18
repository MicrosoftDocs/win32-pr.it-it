---
title: Recupero di interfacce ADSI dall'estensione
description: Un'estensione deve spesso recuperare i dati dall'oggetto directory al quale è associato.
ms.assetid: 2d2e6dc6-1eed-491b-9d6a-7f35c24a7ba8
ms.tgt_platform: multiple
keywords:
- estensioni ADSI, recupero di interfacce ADSI dall'estensione
- ADSI ADSI, esempio di codice C/C++, recupero di interfacce ADSI dall'estensione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a1eeff55f2e382ce2816f59ee53dbd78033b79c
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "106300456"
---
# <a name="getting-adsi-interfaces-from-your-extension"></a><span data-ttu-id="9f89d-105">Recupero di interfacce ADSI dall'estensione</span><span class="sxs-lookup"><span data-stu-id="9f89d-105">Getting ADSI Interfaces From Your Extension</span></span>

<span data-ttu-id="9f89d-106">Un'estensione deve spesso recuperare i dati dall'oggetto directory al quale è associato.</span><span class="sxs-lookup"><span data-stu-id="9f89d-106">An extension often needs to get data from the directory object it binds to.</span></span> <span data-ttu-id="9f89d-107">Ad esempio, un'estensione per un oggetto **computer** può voler ottenere il **dNSHostName** dell'oggetto corrente dalla directory.</span><span class="sxs-lookup"><span data-stu-id="9f89d-107">For example, an extension for a **computer** object may want to get the **dnsHostName** of the current object from the directory.</span></span> <span data-ttu-id="9f89d-108">Questa operazione può essere eseguita facilmente eseguendo una chiamata **QueryInterface** sull'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) per l'aggregatore.</span><span class="sxs-lookup"><span data-stu-id="9f89d-108">This can be easily achieved by issuing a **QueryInterface** call on the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface for the aggregator.</span></span>


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



<span data-ttu-id="9f89d-109">È consigliabile rilasciare l'interfaccia immediatamente dopo averla usata.</span><span class="sxs-lookup"><span data-stu-id="9f89d-109">You should release the interface immediately after using it.</span></span> <span data-ttu-id="9f89d-110">Se l'estensione dispone di un riferimento aperto a aggregator, è stato creato un riferimento circolare e l'aggregatore non può rilasciare l'estensione.</span><span class="sxs-lookup"><span data-stu-id="9f89d-110">If the extension has an open reference to the aggregator, you have created a circular reference and the aggregator cannot release the extension.</span></span> <span data-ttu-id="9f89d-111">Non è quindi possibile rilasciare l'aggregatore e il risultato è una perdita di memoria nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9f89d-111">Therefore, the aggregator cannot be released and the result is memory leaks in your application.</span></span>

 

 