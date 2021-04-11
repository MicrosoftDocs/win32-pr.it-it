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
# <a name="embedding-a-table-of-contents-in-a-video-file"></a><span data-ttu-id="0d525-103">Incorporamento di un sommario in un file video</span><span class="sxs-lookup"><span data-stu-id="0d525-103">Embedding a Table of Contents in a Video File</span></span>

<span data-ttu-id="0d525-104">In questo argomento viene illustrato come creare un sommario e incorporarlo in un file video.</span><span class="sxs-lookup"><span data-stu-id="0d525-104">This topic demonstrates how to create a table of contents (TOC) and embed it in a video file.</span></span> <span data-ttu-id="0d525-105">Per rendere il codice di esempio breve, il sommario è molto semplice; contiene una sola voce e la voce viene popolata con un minimo di informazioni.</span><span class="sxs-lookup"><span data-stu-id="0d525-105">To keep the example code short, the table of contents is very simple; it contains only one entry, and the entry is populated with a minimum of information.</span></span>

<span data-ttu-id="0d525-106">Per creare un sommario e incorporarlo in un file, è necessario creare i quattro oggetti seguenti chiamando **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="0d525-106">To create a table of contents and embed it in a file, you must create the following four objects by calling **CoCreateInstance**.</span></span>

-   <span data-ttu-id="0d525-107">Voce Sommario</span><span class="sxs-lookup"><span data-stu-id="0d525-107">TOC Entry</span></span>
-   <span data-ttu-id="0d525-108">Elenco voci Sommario</span><span class="sxs-lookup"><span data-stu-id="0d525-108">TOC Entry List</span></span>
-   <span data-ttu-id="0d525-109">Sommario</span><span class="sxs-lookup"><span data-stu-id="0d525-109">TOC</span></span>
-   <span data-ttu-id="0d525-110">Parser Sommario</span><span class="sxs-lookup"><span data-stu-id="0d525-110">TOC Parser</span></span>

<span data-ttu-id="0d525-111">Gli identificatori di classe per gli oggetti vengono specificati negli [identificatori di classe per il parser di sommario](class-identifiers-for-toc-parser.md).</span><span class="sxs-lookup"><span data-stu-id="0d525-111">Class identifiers for the objects are given in [Class Identifiers for Table of Contents Parser](class-identifiers-for-toc-parser.md).</span></span>

<span data-ttu-id="0d525-112">Per prima cosa popolare la voce TOC con le informazioni che descrivono una parte del file video.</span><span class="sxs-lookup"><span data-stu-id="0d525-112">First populate the TOC entry with information that describes one portion of the video file.</span></span> <span data-ttu-id="0d525-113">Aggiungere la voce TOC all'elenco di voci del sommario, quindi aggiungere l'elenco di voci di sommario al sommario.</span><span class="sxs-lookup"><span data-stu-id="0d525-113">Add the TOC entry to the TOC entry list, and then add the TOC entry list to the TOC.</span></span> <span data-ttu-id="0d525-114">Infine, aggiungere il sommario al parser TOC, che fornisce la funzionalità per incorporare il sommario nel file video.</span><span class="sxs-lookup"><span data-stu-id="0d525-114">Finally, add the TOC to the TOC parser, which provides the functionality for embedding the TOC in the video file.</span></span> <span data-ttu-id="0d525-115">L'elenco seguente illustra i passaggi in modo più dettagliato.</span><span class="sxs-lookup"><span data-stu-id="0d525-115">The following list gives the steps in more detail.</span></span>

1.  <span data-ttu-id="0d525-116">Creare un oggetto voce del sommario e ottenere un'interfaccia [**ITocEntry**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry) .</span><span class="sxs-lookup"><span data-stu-id="0d525-116">Create a TOC Entry object and obtain an [**ITocEntry**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry) interface on it.</span></span>
2.  <span data-ttu-id="0d525-117">Popolare una struttura del [**\_ \_ descrittore di voci di sommario**](/windows/desktop/api/wmcodecdsp/ns-wmcodecdsp-toc_entry_descriptor) e passarla a [**ITocEntry:: descrittore**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentry-setdescriptor).</span><span class="sxs-lookup"><span data-stu-id="0d525-117">Populate a [**TOC\_ENTRY\_DESCRIPTOR**](/windows/desktop/api/wmcodecdsp/ns-wmcodecdsp-toc_entry_descriptor) structure and pass it to [**ITocEntry::SetDescriptor**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentry-setdescriptor).</span></span>
3.  <span data-ttu-id="0d525-118">Creare un oggetto elenco di voci di sommario e ottenere un'interfaccia [**ITocEntryList**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentrylist) .</span><span class="sxs-lookup"><span data-stu-id="0d525-118">Create a TOC Entry List object and obtain an [**ITocEntryList**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentrylist) interface on it.</span></span>
4.  <span data-ttu-id="0d525-119">Aggiungere l'oggetto voce del sommario creato nel passaggio 1 all'oggetto elenco di voci di sommario chiamando [**ITocEntryList:: AddEntryByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentrylist-addentrybyindex).</span><span class="sxs-lookup"><span data-stu-id="0d525-119">Add the TOC Entry object you created in step 1 to the TOC Entry List object by calling [**ITocEntryList::AddEntryByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentrylist-addentrybyindex).</span></span>
5.  <span data-ttu-id="0d525-120">Creare un oggetto TOC e ottenere un'interfaccia [**IToc**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc) .</span><span class="sxs-lookup"><span data-stu-id="0d525-120">Create a TOC object and obtain an [**IToc**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc) interface on it.</span></span>
6.  <span data-ttu-id="0d525-121">Aggiungere l'oggetto elenco di voci di sommario creato nel passaggio 3 all'oggetto TOC chiamando [**IToc:: AddEntryListByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itoc-addentrylistbyindex).</span><span class="sxs-lookup"><span data-stu-id="0d525-121">Add the TOC Entry List object you created in step 3 to the TOC object by calling [**IToc::AddEntryListByIndex**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itoc-addentrylistbyindex).</span></span>
7.  <span data-ttu-id="0d525-122">Creare un oggetto parser TOC e ottenere un'interfaccia [**ITocParser**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) .</span><span class="sxs-lookup"><span data-stu-id="0d525-122">Create a TOC Parser object and obtain an [**ITocParser**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) interface on it.</span></span>
8.  <span data-ttu-id="0d525-123">Chiamare [**ITocParser:: init**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-init) per inizializzare l'oggetto parser TOC e associarlo a un file video.</span><span class="sxs-lookup"><span data-stu-id="0d525-123">Call [**ITocParser::Init**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-init) to initialize the TOC Parser object and associate it with a video file.</span></span>
9.  <span data-ttu-id="0d525-124">Aggiungere l'oggetto TOC creato nel passaggio 5 all'oggetto parser TOC chiamando [**ITocParser:: AddToc**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-addtoc).</span><span class="sxs-lookup"><span data-stu-id="0d525-124">Add the TOC object you created in step 5 to the TOC Parser object by calling [**ITocParser::AddToc**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-addtoc).</span></span>
10. <span data-ttu-id="0d525-125">Incorporare il sommario nel file video chiamando [**ITocParser:: commit**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-commit).</span><span class="sxs-lookup"><span data-stu-id="0d525-125">Embed the table of contents in the video file by calling [**ITocParser::Commit**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-commit).</span></span>

<span data-ttu-id="0d525-126">Nel codice riportato di seguito vengono illustrati i passaggi indicati nell'elenco precedente.</span><span class="sxs-lookup"><span data-stu-id="0d525-126">The following code demonstrates the steps given in the preceding list.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="0d525-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0d525-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d525-128">Lettura di un sommario da un file video</span><span class="sxs-lookup"><span data-stu-id="0d525-128">Reading a Table of Contents From a Video File</span></span>](reading-a-table-of-contents-from-a-video-file.md)
</dt> <dt>

[<span data-ttu-id="0d525-129">Oggetti parser del sommario</span><span class="sxs-lookup"><span data-stu-id="0d525-129">Table of Contents Parser Objects</span></span>](toc-parser-objects.md)
</dt> <dt>

[<span data-ttu-id="0d525-130">Guida per programmatori del parser Sommario</span><span class="sxs-lookup"><span data-stu-id="0d525-130">Table of Contents Parser Programming Guide</span></span>](toc-parser-programming-guide.md)
</dt> </dl>

 

 



