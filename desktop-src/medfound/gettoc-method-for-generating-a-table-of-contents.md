---
description: Funzione GetToc per la generazione di un sommario
ms.assetid: f2f312ff-3519-4269-8252-eb52d2bc2e56
title: Funzione GetToc per la generazione di un sommario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b24da42f39ba5a499492bac8a166ffcfa883aab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127875"
---
# <a name="gettoc-function-for-generating-a-table-of-contents"></a><span data-ttu-id="8fbcb-103">Funzione GetToc per la generazione di un sommario</span><span class="sxs-lookup"><span data-stu-id="8fbcb-103">GetToc Function for Generating a Table of Contents</span></span>

<span data-ttu-id="8fbcb-104">La funzione seguente è una funzione helper in un programma di esempio descritto in [generazione automatica di un sommario](generating-a-table-of-contents-automatically.md).</span><span class="sxs-lookup"><span data-stu-id="8fbcb-104">The following function is a helper function in an example program that is discussed in [Generating a Table of Contents Automatically](generating-a-table-of-contents-automatically.md).</span></span>


```C++
HRESULT GetToc(IDMOWrapperFilter* pWrap, IToc** ppToc)
{
   IPropertyStore* pStore = NULL;
   HRESULT  hr = pWrap->QueryInterface(IID_IPropertyStore, (VOID**)&pStore);

   if(SUCCEEDED(hr))
   {
      PROPVARIANT pv;
      PropVariantInit(&pv);

      pv.vt = VT_BOOL;
      pv.bVal = VARIANT_TRUE;                                                     
      hr = pStore->SetValue(MFPKEY_TOCGENERATOR_ENDSIGNAL, pv);

      if(SUCCEEDED(hr))
      {
         for(LONG j = 0; j < 10; ++j)
         {
            PropVariantClear(&pv);
            pv.vt = VT_BOOL;
            hr = pStore->GetValue(MFPKEY_TOCGENERATOR_TOCREADY, &pv);

            if(SUCCEEDED(hr) && 1 == pv.bVal)  // Note: 1 is not equal to VARIANT_TRUE.
            {
               PropVariantClear(&pv);
               pv.vt = VT_UNKNOWN;
               hr = pStore->GetValue(MFPKEY_TOCGENERATOR_TOCOBJECT, &pv);

               if(SUCCEEDED(hr))
               {
                  *ppToc = (IToc*)pv.punkVal;
               }

               break;
            }

            Sleep(200);
            hr = ERROR_TIMEOUT;       
         }
      }

      pStore->Release();
      pStore = NULL;
   }
   
   return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="8fbcb-105">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8fbcb-105">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8fbcb-106">Generazione automatica di un sommario</span><span class="sxs-lookup"><span data-stu-id="8fbcb-106">Generating a Table of Contents Automatically</span></span>](generating-a-table-of-contents-automatically.md)
</dt> </dl>

 

 



