---
description: Funzione BuildGraph per la generazione di un sommario
ms.assetid: f70740ef-4c58-4944-9be6-dd056e12ad93
title: Funzione BuildGraph per la generazione di un sommario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f53f1f175095573a5f0f53a5274d997d85db7b74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342566"
---
# <a name="buildgraph-function-for-generating-a-table-of-contents"></a>Funzione BuildGraph per la generazione di un sommario

La funzione seguente è una funzione helper in un programma di esempio descritto in [generazione automatica di un sommario](generating-a-table-of-contents-automatically.md).


```C++
HRESULT BuildGraph(IGraphBuilder* pGraph, IDMOWrapperFilter* pWrap)
{
   IBaseFilter* pTocGeneratorBase = NULL;
   HRESULT hr = pWrap->QueryInterface(IID_IBaseFilter, (VOID**)&pTocGeneratorBase);

   if(SUCCEEDED(hr))
   {
      hr = pGraph->AddFilter(pTocGeneratorBase, L"TOC Generator");

      if(SUCCEEDED(hr))
      {
         IBaseFilter* pSourceBase = NULL;
         hr = pGraph->AddSourceFilter(g_sourceFile, L"Source", &pSourceBase);

         if(SUCCEEDED(hr))
         { 
            IEnumPins* pTocGenPins = NULL;
            hr = pTocGeneratorBase->EnumPins(&pTocGenPins);

            if(SUCCEEDED(hr))
            {                            
               ULONG numPins = 0;
               IPin* pTocGenInput = NULL;  // 1st pin is input.
               hr = pTocGenPins->Next(1, &pTocGenInput, &numPins);

               if(SUCCEEDED(hr))
               {                           
                  numPins = 0;
                  IPin* pTocGenOutput = NULL;  // 2nd pin is output.
                  hr = pTocGenPins->Next(1, &pTocGenOutput, &numPins);

                  if(SUCCEEDED(hr))
                  {
                     IEnumPins* pSourcePins = NULL;
                     hr = pSourceBase->EnumPins(&pSourcePins);

                     if(SUCCEEDED(hr))
                     {
                        numPins = 0;
                        IPin* pSourceInput = NULL;
                        hr = pSourcePins->Next(1, &pSourceInput, &numPins);
                      
                        // We don't need the first pin, so discard it.
                        if(NULL != pSourceInput)
                        {
                           pSourceInput->Release();
                           pSourceInput = NULL;
                        }

                        IPin* pSourceOutput = NULL;  // 2nd pin is output.
                        hr = pSourcePins->Next(1, &pSourceOutput, &numPins);

                        if(SUCCEEDED(hr))
                        { 
                           hr = pGraph->Connect(pSourceOutput, pTocGenInput);

                           if(SUCCEEDED(hr))
                           {
                              hr = pGraph->Render(pTocGenOutput);
                           }

                           pSourceOutput->Release();
                           pSourceOutput = NULL;
                        }

                        pSourcePins->Release();
                        pSourcePins = NULL;
                     }

                     pTocGenOutput->Release();
                     pTocGenOutput = NULL;
                  }

                  pTocGenInput->Release();
                  pTocGenInput = NULL;
               }

               pTocGenPins->Release();
               pTocGenPins = NULL;
            }
                                               
            pSourceBase->Release();
            pSourceBase = NULL;
         }
      }

      pTocGeneratorBase->Release();
      pTocGeneratorBase = NULL;
   }

   return hr;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Generazione automatica di un sommario](generating-a-table-of-contents-automatically.md)
</dt> </dl>

 

 



