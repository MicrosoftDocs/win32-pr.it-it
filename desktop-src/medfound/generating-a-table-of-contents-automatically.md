---
description: Generazione automatica di un sommario
ms.assetid: 3acb9c12-0158-4b89-87c4-4abd35ae8c2f
title: Generazione automatica di un sommario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22adc4d48ad7f4b1d89a446eb28c25d6011804a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305378"
---
# <a name="generating-a-table-of-contents-automatically"></a><span data-ttu-id="cbcbd-103">Generazione automatica di un sommario</span><span class="sxs-lookup"><span data-stu-id="cbcbd-103">Generating a Table of Contents Automatically</span></span>

<span data-ttu-id="cbcbd-104">In questo argomento viene illustrato come utilizzare il componente [**Table of Contents Generator**](/previous-versions/ee264297(v=vs.85)) (Generatore Sommario) per generare automaticamente un sommario per un file video.</span><span class="sxs-lookup"><span data-stu-id="cbcbd-104">This topic demonstrates how to use [**Table of Contents Generator**](/previous-versions/ee264297(v=vs.85)) (TOC Generator) component to automatically generate a table of contents for a video file.</span></span>

<span data-ttu-id="cbcbd-105">Il generatore di sommario è un oggetto DMO (DirectX Media Object).</span><span class="sxs-lookup"><span data-stu-id="cbcbd-105">TOC Generator is a DirectX Media Object (DMO).</span></span> <span data-ttu-id="cbcbd-106">Per usare il generatore di sommario DMO, compilare un grafico di filtro DirectX con un file video come origine.</span><span class="sxs-lookup"><span data-stu-id="cbcbd-106">To use the TOC Generator DMO, build a DirectX filter graph that has a video file as its source.</span></span> <span data-ttu-id="cbcbd-107">Inserire il generatore di sommario DMO nel grafico del filtro ed eseguire il grafo.</span><span class="sxs-lookup"><span data-stu-id="cbcbd-107">Insert the TOC Generator DMO into the filter graph, and run the graph.</span></span> <span data-ttu-id="cbcbd-108">È quindi possibile ottenere il sommario generato automaticamente dal generatore di sommario DMO.</span><span class="sxs-lookup"><span data-stu-id="cbcbd-108">You can then obtain the automatically generated table of contents from the TOC Generator DMO.</span></span>

<span data-ttu-id="cbcbd-109">La procedura seguente illustra in modo più dettagliato i passaggi.</span><span class="sxs-lookup"><span data-stu-id="cbcbd-109">The following procedure gives the steps in more detail.</span></span>

1.  <span data-ttu-id="cbcbd-110">Chiamare [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per creare un oggetto grafico di filtro (**CLSID \_ filtergraph**) e ottenere un'interfaccia [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) .</span><span class="sxs-lookup"><span data-stu-id="cbcbd-110">Call [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to create a Filter Graph object (**CLSID\_FilterGraph**) and obtain an [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) interface.</span></span>
2.  <span data-ttu-id="cbcbd-111">Chiamare [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per creare un oggetto filtro wrapper DMO (**CLSID \_ DMOWrapperFilter**) e ottenere un'interfaccia [**IDMOWrapperFilter**](/previous-versions/windows/desktop/api/dmodshow/nn-dmodshow-idmowrapperfilter) .</span><span class="sxs-lookup"><span data-stu-id="cbcbd-111">Call [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to create a DMO Wrapper Filter object (**CLSID\_DMOWrapperFilter**) and obtain an [**IDMOWrapperFilter**](/previous-versions/windows/desktop/api/dmodshow/nn-dmodshow-idmowrapperfilter) interface.</span></span>
3.  <span data-ttu-id="cbcbd-112">Passare **CLSID \_ CTocGeneratorDmo** al metodo [**init**](/previous-versions/windows/desktop/api/dmodshow/nf-dmodshow-idmowrapperfilter-init) del filtro del wrapper DMO.</span><span class="sxs-lookup"><span data-stu-id="cbcbd-112">Pass **CLSID\_CTocGeneratorDmo** to the [**Init**](/previous-versions/windows/desktop/api/dmodshow/nf-dmodshow-idmowrapperfilter-init) method of your DMO wrapper filter.</span></span> <span data-ttu-id="cbcbd-113">Viene creato un generatore di sommario DMO e ne viene eseguito il wrapping nel filtro del wrapper DMO.</span><span class="sxs-lookup"><span data-stu-id="cbcbd-113">This creates a TOC Generator DMO and wraps it in your DMO wrapper filter.</span></span>
4.  <span data-ttu-id="cbcbd-114">Chiamare il metodo [**addFilter**](/windows/win32/api/strmif/nf-strmif-ifiltergraph-addfilter) dell'interfaccia [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) per aggiungere il generatore di sommario con wrapper DMO al grafo del filtro.</span><span class="sxs-lookup"><span data-stu-id="cbcbd-114">Call the [**AddFilter**](/windows/win32/api/strmif/nf-strmif-ifiltergraph-addfilter) method of your [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) interface to add the wrapped TOC Generator DMO to the filter graph.</span></span>
    > [!Note]  
    > <span data-ttu-id="cbcbd-115">[**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) eredita da [**IFilterGraph**](/windows/win32/api/strmif/nn-strmif-ifiltergraph).</span><span class="sxs-lookup"><span data-stu-id="cbcbd-115">[**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) inherits from [**IFilterGraph**](/windows/win32/api/strmif/nn-strmif-ifiltergraph).</span></span>

     

5.  <span data-ttu-id="cbcbd-116">Chiamare il metodo [**AddSourceFilter**](/windows/win32/api/strmif/nf-strmif-igraphbuilder-addsourcefilter) dell'interfaccia [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) per creare un filtro origine e aggiungerlo al grafico.</span><span class="sxs-lookup"><span data-stu-id="cbcbd-116">Call the [**AddSourceFilter**](/windows/win32/api/strmif/nf-strmif-igraphbuilder-addsourcefilter) method of your [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) interface to create a souce filter and add it to the graph.</span></span>
6.  <span data-ttu-id="cbcbd-117">Enumerare i pin sul filtro del wrapper DMO e sul filtro di origine.</span><span class="sxs-lookup"><span data-stu-id="cbcbd-117">Enumerate pins on the DMO wrapper filter and the source filter.</span></span> <span data-ttu-id="cbcbd-118">Ciò implica l'ottenimento delle interfacce [**IEnumPins**](/windows/win32/api/strmif/nn-strmif-ienumpins) e delle interfacce [**Ipin**](/windows/win32/api/strmif/nn-strmif-ipin) .</span><span class="sxs-lookup"><span data-stu-id="cbcbd-118">This involves obtaining [**IEnumPins**](/windows/win32/api/strmif/nn-strmif-ienumpins) interfaces and [**IPin**](/windows/win32/api/strmif/nn-strmif-ipin) interfaces.</span></span>
7.  <span data-ttu-id="cbcbd-119">Connettere il filtro di origine e il filtro wrapper chiamando il metodo [**Connect**](/windows/win32/api/strmif/nf-strmif-igraphbuilder-connect) dell'interfaccia [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) .</span><span class="sxs-lookup"><span data-stu-id="cbcbd-119">Connect the source filter and the wrapper filter by calling the [**Connect**](/windows/win32/api/strmif/nf-strmif-igraphbuilder-connect) method of your [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) interface.</span></span>
8.  <span data-ttu-id="cbcbd-120">Completare il grafo chiamando il metodo [**Render**](/windows/win32/api/strmif/nf-strmif-igraphbuilder-render) dell'interfaccia [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) .</span><span class="sxs-lookup"><span data-stu-id="cbcbd-120">Complete the graph by calling the [**Render**](/windows/win32/api/strmif/nf-strmif-igraphbuilder-render) method of your [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) interface.</span></span>
9.  <span data-ttu-id="cbcbd-121">Eseguire il grafo ([**IMediaControl:: Run**](/windows/win32/api/control/nf-control-imediacontrol-run)) e attenderne il completamento ([**IMediaEvent:: WaitForCompletion**](/windows/win32/api/control/nf-control-imediaevent-waitforcompletion)).</span><span class="sxs-lookup"><span data-stu-id="cbcbd-121">Run the graph ([**IMediaControl::Run**](/windows/win32/api/control/nf-control-imediacontrol-run)), and wait for it to complete ([**IMediaEvent::WaitForCompletion**](/windows/win32/api/control/nf-control-imediaevent-waitforcompletion)).</span></span>
10. <span data-ttu-id="cbcbd-122">Ottenere un'interfaccia [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) sul wrapper del filtro DMO e ottenere il valore della proprietà [**MFPKEY \_ TOCGENERATOR \_ TOCREADY**](/previous-versions/ee264297(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="cbcbd-122">Obtain an [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface on your DMO filter wrapper, and get the value of the [**MFPKEY\_TOCGENERATOR\_TOCREADY**](/previous-versions/ee264297(v=vs.85)) property.</span></span> <span data-ttu-id="cbcbd-123">Ripetere se necessario finché il sommario non è pronto.</span><span class="sxs-lookup"><span data-stu-id="cbcbd-123">Repeat if necessary until the table of contents is ready.</span></span>
11. <span data-ttu-id="cbcbd-124">Usare l'interfaccia [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) per ottenere il valore della proprietà [**MFPKEY \_ TOCGENERATOR \_ tocobject**](/previous-versions/ee264297(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="cbcbd-124">Use your [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface to get the value of the [**MFPKEY\_TOCGENERATOR\_TOCOBJECT**](/previous-versions/ee264297(v=vs.85)) property.</span></span> <span data-ttu-id="cbcbd-125">Questa proprietà è un'interfaccia [**IToc**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc) che rappresenta il sommario generato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="cbcbd-125">This property is an [**IToc**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc) interface that represents the automatically generated table of contents.</span></span>

<span data-ttu-id="cbcbd-126">Nel codice seguente viene illustrata la procedura per la generazione automatica di un sommario.</span><span class="sxs-lookup"><span data-stu-id="cbcbd-126">The following code demonstrates the procedure for generating a table of contents automatically.</span></span> <span data-ttu-id="cbcbd-127">Il codice usa tre funzioni helper ([**BuildGraph**](buildgraph-method-for-generating-a-table-of-contents.md), [**RunGraphAndWait**](rungraphandwait-method-for-generating-a-table-of-contents.md)e [**GetToc**](gettoc-method-for-generating-a-table-of-contents.md)) visualizzate in altre pagine di questa documentazione.</span><span class="sxs-lookup"><span data-stu-id="cbcbd-127">The code uses three helper functions ([**BuildGraph**](buildgraph-method-for-generating-a-table-of-contents.md), [**RunGraphAndWait**](rungraphandwait-method-for-generating-a-table-of-contents.md), and [**GetToc**](gettoc-method-for-generating-a-table-of-contents.md)) that are shown on other pages of this documentation.</span></span>


```C++
#include <dshow.h>
#include <dmodshow.h>
#include <wmcodecdsp.h>
#include <dmoreg.h>
#include <propsys.h>
#include <propidl.h>
#include <initguid.h>

HRESULT GetToc(IDMOWrapperFilter* pWrap, IToc** ppToc);
HRESULT RunGraphAndWait(IGraphBuilder* pGraph);
HRESULT BuildGraph(IGraphBuilder* pGraph, IDMOWrapperFilter* pWrap);

WCHAR g_sourceFile[] = L"c:\\experiment\\Seattle.wmv";

void main()
{
   HRESULT hr = E_FAIL;
   hr = CoInitialize(NULL);

   if(SUCCEEDED(hr))
   {
      IGraphBuilder* pBuilder = NULL;
      hr = CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC_SERVER, 
         IID_IGraphBuilder, (VOID**)&pBuilder);

      if(SUCCEEDED(hr))
      {
         IDMOWrapperFilter* pWrap = NULL;
         hr = CoCreateInstance(CLSID_DMOWrapperFilter, NULL, CLSCTX_INPROC, 
            IID_IDMOWrapperFilter, (VOID**)&pWrap);

         if(SUCCEEDED(hr))
         {
            hr = pWrap->Init(CLSID_CTocGeneratorDmo, DMOCATEGORY_VIDEO_EFFECT); 

            if(SUCCEEDED(hr))
            {
               hr = BuildGraph(pBuilder, pWrap);

               if(SUCCEEDED(hr))
               {
                  hr = RunGraphAndWait(pBuilder);

                  if(SUCCEEDED(hr))
                  {
                     IToc* pToc = NULL;
                     hr = GetToc(pWrap, &pToc);

                     if(SUCCEEDED(hr))
                     {
                        // Inspect the table of contents by calling IToc methods.

                        pToc->Release();
                        pToc = NULL;
                     }
                  }
               }
            }

            pWrap->Release();
            pWrap = NULL;
         }

         pBuilder->Release();
         pBuilder = NULL;
      }

      CoUninitialize();
   }
}
```



## <a name="related-topics"></a><span data-ttu-id="cbcbd-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cbcbd-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cbcbd-129">Funzione BuildGraph per la generazione di un sommario</span><span class="sxs-lookup"><span data-stu-id="cbcbd-129">BuildGraph Function for Generating a Table of Contents</span></span>](buildgraph-method-for-generating-a-table-of-contents.md)
</dt> <dt>

[<span data-ttu-id="cbcbd-130">Funzione GetToc per la generazione di un sommario</span><span class="sxs-lookup"><span data-stu-id="cbcbd-130">GetToc Function for Generating a Table of Contents</span></span>](gettoc-method-for-generating-a-table-of-contents.md)
</dt> <dt>

[<span data-ttu-id="cbcbd-131">Funzione RunGraphAndWait per la generazione di un sommario</span><span class="sxs-lookup"><span data-stu-id="cbcbd-131">RunGraphAndWait Function for Generating a Table of Contents</span></span>](rungraphandwait-method-for-generating-a-table-of-contents.md)
</dt> <dt>

[<span data-ttu-id="cbcbd-132">Guida per programmatori del parser Sommario</span><span class="sxs-lookup"><span data-stu-id="cbcbd-132">Table of Contents Parser Programming Guide</span></span>](toc-parser-programming-guide.md)
</dt> </dl>

 

 
