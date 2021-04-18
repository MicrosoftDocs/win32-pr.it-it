---
description: Lettura di un sommario da un file video
ms.assetid: 10c4f4ca-cb30-453c-b18d-0470bfecc14e
title: Lettura di un sommario da un file video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94d75d1101b2ad0a2ecd57dcf53acbe6a6e7d435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309021"
---
# <a name="reading-a-table-of-contents-from-a-video-file"></a>Lettura di un sommario da un file video

In questo argomento viene illustrato come leggere un sommario che è già stato incorporato in un file video.

Per iniziare, chiamare [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per creare un oggetto parser TOC e ottenere un'interfaccia [**ITocParser**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) . Ottenere quindi le interfacce seguenti chiamando i metodi.

-   [**IToc**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc)
-   [**ITocEntryList**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentrylist)
-   [**ITocEntry**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry)

Usare i metodi di [**ITocEntry**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry) per esaminare una singola voce nel sommario. Ad esempio, è possibile controllare il titolo, l'ora di inizio e l'ora di fine della voce.

L'elenco seguente illustra i passaggi in modo più dettagliato.

1.  Chiamare [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per creare un oggetto parser TOC e ottenere un'interfaccia [**ITocParser**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) .
2.  Chiamare [**ITocParser:: init**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-init) per inizializzare il parser TOC e associarlo a un file video.
3.  Ottenere un'interfaccia [**IToc**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc) chiamando [**ITocParser:: GetTocByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-gettocbyindex).
4.  Ottenere un'interfaccia [**ITocEntryList**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentrylist) chiamando [**IToc:: GetEntryListByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itoc-getentrylistbyindex).
5.  Ottenere un'interfaccia [**ITocEntry**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry) chiamando [**ITocEntryList:: GetEntryByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentrylist-getentrybyindex).
6.  Alloca una struttura del [**\_ \_ descrittore di voci di sommario**](/windows/desktop/api/wmcodecdsp/ns-wmcodecdsp-toc_entry_descriptor) .
7.  Popolare la struttura del [**\_ \_ descrittore di voce del sommario**](/windows/desktop/api/wmcodecdsp/ns-wmcodecdsp-toc_entry_descriptor) chiamando [**ITocEntry:: GetDescriptor**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentry-getdescriptor).

Nel codice riportato di seguito vengono illustrati i passaggi nell'elenco precedente.


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

[Guida per programmatori del parser Sommario](toc-parser-programming-guide.md)
</dt> </dl>

 

 
