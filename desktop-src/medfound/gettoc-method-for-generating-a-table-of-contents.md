---
description: Funzione GetToc per la generazione di un sommario
ms.assetid: f2f312ff-3519-4269-8252-eb52d2bc2e56
title: Funzione GetToc per la generazione di un sommario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f1d70317c77bf73df12983946abafc10675b6f63f62759335604871df3633d1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061577"
---
# <a name="gettoc-function-for-generating-a-table-of-contents"></a>Funzione GetToc per la generazione di un sommario

La funzione seguente è una funzione helper in un programma di esempio descritto in Generazione automatica di un [sommario.](generating-a-table-of-contents-automatically.md)


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Generazione automatica di un sommario](generating-a-table-of-contents-automatically.md)
</dt> </dl>

 

 



