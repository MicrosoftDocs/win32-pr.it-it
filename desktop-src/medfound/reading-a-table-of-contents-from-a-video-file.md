---
description: Lettura di un sommario da un file video
ms.assetid: 10c4f4ca-cb30-453c-b18d-0470bfecc14e
title: Lettura di un sommario da un file video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bee379b0c50263463b0aa56e7ebb86bba447e70ef94ff82a6ba89e025d450bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034939"
---
# <a name="reading-a-table-of-contents-from-a-video-file"></a>Lettura di un sommario da un file video

Questo argomento illustra come leggere un sommario già incorporato in un file video.

Iniziare chiamando [**CoCreateInstance per**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) creare un oggetto parser del sommario e ottenere [**un'interfaccia ITocParser.**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) Ottenere quindi le interfacce seguenti chiamando i metodi .

-   [**IToc**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc)
-   [**ITocEntryList**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentrylist)
-   [**ITocEntry**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry)

Usare i metodi di [**ITocEntry**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry) per esaminare una singola voce nel sommario. Ad esempio, è possibile esaminare il titolo, l'ora di inizio e l'ora di fine della voce.

L'elenco seguente fornisce i passaggi in modo più dettagliato.

1.  Chiamare [**CoCreateInstance per**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) creare un oggetto parser del sommario e ottenere [**un'interfaccia ITocParser**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) su di esso.
2.  Chiamare [**ITocParser::Init**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-init) per inizializzare il parser del sommario e associarlo a un file video.
3.  Ottenere [**un'interfaccia IToc**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc) chiamando [**ITocParser::GetTocByIndex.**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-gettocbyindex)
4.  Ottenere [**un'interfaccia ITocEntryList**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentrylist) chiamando [**IToc::GetEntryListByIndex.**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itoc-getentrylistbyindex)
5.  Ottenere [**un'interfaccia ITocEntry**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry) chiamando [**ITocEntryList::GetEntryByIndex.**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentrylist-getentrybyindex)
6.  Allocare una [**struttura \_ \_ DESCRIPTOR TOC ENTRY.**](/windows/desktop/api/wmcodecdsp/ns-wmcodecdsp-toc_entry_descriptor)
7.  Popolare la struttura [**\_ \_ DESCRIPTOR TOC ENTRY**](/windows/desktop/api/wmcodecdsp/ns-wmcodecdsp-toc_entry_descriptor) chiamando [**ITocEntry::GetDescriptor**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentry-getdescriptor).

Il codice seguente illustra i passaggi nell'elenco precedente.


```C++
#include <stdio.h>
#include <wmcodecdsp.h>

HRESULT ShowEntryInfo(ITocEntry* pEntry);

void main()
{
   HRESULT hr = CoInitialize(NULL);
   
   if(SUCCEEDED(hr))
   {    
      ITocParser* pTocParser = NULL;

      hr = CoCreateInstance(CLSID_CTocParser, NULL, CLSCTX_INPROC_SERVER, 
         IID_ITocParser, (VOID**)&pTocParser);  
      
      if(SUCCEEDED(hr))
      {  
         hr = pTocParser->Init(L"\\\\?\\c:\\experiment\\seattle.wmv");

         if(SUCCEEDED(hr))
         {
            IToc* pToc = NULL;
            hr = pTocParser->GetTocByIndex(TOC_POS_TOPLEVELOBJECT, 0, &pToc);

            if(SUCCEEDED(hr))
            {
               ITocEntryList* pEntryList = NULL;
               hr = pToc->GetEntryListByIndex(0, &pEntryList);

               if(SUCCEEDED(hr))
               {
                  ITocEntry* pEntry = NULL;
                  hr = pEntryList->GetEntryByIndex(0, &pEntry);

                  if(SUCCEEDED(hr))
                  {
                     hr = ShowEntryInfo(pEntry);
                     pEntry->Release();
                     pEntry = NULL;
                  }

                  pEntryList->Release();
                  pEntryList = NULL;
               }

               pToc->Release();
               pToc = NULL;
            }
         }

         pTocParser->Release();
         pTocParser = NULL;  
      }
                   
      CoUninitialize();
   }
}

HRESULT ShowEntryInfo(ITocEntry* pEntry)
{
   HRESULT hr = E_FAIL;

   TOC_ENTRY_DESCRIPTOR entryDesc = {0};
   hr = pEntry->GetDescriptor(&entryDesc);

   if(SUCCEEDED(hr))
   {
      printf_s("qwStartTime: %x\n", entryDesc.qwStartTime);
      printf_s("qwEndTime: %x\n", entryDesc.qwEndTime);
      printf_s("qwStartStartPacketOffset: %x\n", entryDesc.qwStartPacketOffset);
      printf_s("qwEndPacketOffset: %x\n", entryDesc.qwEndPacketOffset);
      printf_s("qwRepresentativeFrameTime: %x\n", entryDesc.qwRepresentativeFrameTime);
   }

   return hr;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Incorporamento di un sommario in un file video](embedding-a-table-of-contents-in-a-video-file.md)
</dt> <dt>

[Oggetti parser del sommario](toc-parser-objects.md)
</dt> <dt>

[Guida per programmatori del parser sommario](toc-parser-programming-guide.md)
</dt> </dl>

 

 
