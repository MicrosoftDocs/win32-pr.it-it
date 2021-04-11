---
description: Incorporamento di un sommario in un file video
ms.assetid: 1546388a-7868-4411-be20-34d28becbe76
title: Incorporamento di un sommario in un file video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a8303082e454dde181de336ee0f64ff9d583312
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127895"
---
# <a name="embedding-a-table-of-contents-in-a-video-file"></a>Incorporamento di un sommario in un file video

In questo argomento viene illustrato come creare un sommario e incorporarlo in un file video. Per rendere il codice di esempio breve, il sommario è molto semplice; contiene una sola voce e la voce viene popolata con un minimo di informazioni.

Per creare un sommario e incorporarlo in un file, è necessario creare i quattro oggetti seguenti chiamando **CoCreateInstance**.

-   Voce Sommario
-   Elenco voci Sommario
-   Sommario
-   Parser Sommario

Gli identificatori di classe per gli oggetti vengono specificati negli [identificatori di classe per il parser di sommario](class-identifiers-for-toc-parser.md).

Per prima cosa popolare la voce TOC con le informazioni che descrivono una parte del file video. Aggiungere la voce TOC all'elenco di voci del sommario, quindi aggiungere l'elenco di voci di sommario al sommario. Infine, aggiungere il sommario al parser TOC, che fornisce la funzionalità per incorporare il sommario nel file video. L'elenco seguente illustra i passaggi in modo più dettagliato.

1.  Creare un oggetto voce del sommario e ottenere un'interfaccia [**ITocEntry**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry) .
2.  Popolare una struttura del [**\_ \_ descrittore di voci di sommario**](/windows/desktop/api/wmcodecdsp/ns-wmcodecdsp-toc_entry_descriptor) e passarla a [**ITocEntry:: descrittore**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentry-setdescriptor).
3.  Creare un oggetto elenco di voci di sommario e ottenere un'interfaccia [**ITocEntryList**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentrylist) .
4.  Aggiungere l'oggetto voce del sommario creato nel passaggio 1 all'oggetto elenco di voci di sommario chiamando [**ITocEntryList:: AddEntryByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentrylist-addentrybyindex).
5.  Creare un oggetto TOC e ottenere un'interfaccia [**IToc**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc) .
6.  Aggiungere l'oggetto elenco di voci di sommario creato nel passaggio 3 all'oggetto TOC chiamando [**IToc:: AddEntryListByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itoc-addentrylistbyindex).
7.  Creare un oggetto parser TOC e ottenere un'interfaccia [**ITocParser**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) .
8.  Chiamare [**ITocParser:: init**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-init) per inizializzare l'oggetto parser TOC e associarlo a un file video.
9.  Aggiungere l'oggetto TOC creato nel passaggio 5 all'oggetto parser TOC chiamando [**ITocParser:: AddToc**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-addtoc).
10. Incorporare il sommario nel file video chiamando [**ITocParser:: commit**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-commit).

Nel codice riportato di seguito vengono illustrati i passaggi indicati nell'elenco precedente.


```C++
#include <wmcodecdsp.h>
HRESULT InitTocParserAndCommit(IToc* pToc);

void main()
{
   HRESULT hr = CoInitialize(NULL);
   
   if(SUCCEEDED(hr))
   {    
      ITocEntry* pEntry = NULL;
      hr = CoCreateInstance(CLSID_CTocEntry, NULL, 
         CLSCTX_INPROC_SERVER, IID_ITocEntry, (VOID**)&pEntry); 

      if(SUCCEEDED(hr))
      {
         TOC_ENTRY_DESCRIPTOR tocDesc = {0};
         tocDesc.qwStartTime = 4; 
         tocDesc.qwEndTime = 8;
         pEntry->SetDescriptor(&tocDesc); // HRESULT ignored for simplicity.    
    
         ITocEntryList* pEntryList = NULL;
         hr = CoCreateInstance(CLSID_CTocEntryList, NULL, 
            CLSCTX_INPROC_SERVER, IID_ITocEntryList, (VOID**)&pEntryList);

         if(SUCCEEDED(hr))
         {
            pEntryList->AddEntryByIndex(0, pEntry); // HRESULT ignored.
      
            IToc* pToc = NULL;
            hr = CoCreateInstance(CLSID_CToc, NULL, 
               CLSCTX_INPROC_SERVER, IID_IToc, (VOID**)&pToc);

            if(SUCCEEDED(hr))
            {
               pToc->AddEntryListByIndex(0, pEntryList); // HRESULT ignored.
               hr = InitTocParserAndCommit(pToc);
            }
         }
      }
     
      CoUninitialize();
   }
}

HRESULT InitTocParserAndCommit(IToc* pToc)
{
   ITocParser* pTocParser = NULL;
   HRESULT hr = CoCreateInstance(CLSID_CTocParser, NULL, 
      CLSCTX_INPROC_SERVER, IID_ITocParser, (VOID**)&pTocParser);

   if(SUCCEEDED(hr))
   {
      hr = pTocParser->Init(L"\\\\?\\c:\\experiment\\seattle.wmv");

      if(SUCCEEDED(hr))
      {
         DWORD tocIndex = 0;
         hr = pTocParser->AddToc(TOC_POS_TOPLEVELOBJECT, pToc, &tocIndex);

         if(SUCCEEDED(hr))
         {
            hr = pTocParser->Commit();
         }
      }

      pTocParser->Release();
      pTocParser = NULL;
   }

   return hr;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Lettura di un sommario da un file video](reading-a-table-of-contents-from-a-video-file.md)
</dt> <dt>

[Oggetti parser del sommario](toc-parser-objects.md)
</dt> <dt>

[Guida per programmatori del parser Sommario](toc-parser-programming-guide.md)
</dt> </dl>

 

 



