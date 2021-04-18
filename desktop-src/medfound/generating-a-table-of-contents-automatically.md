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
# <a name="generating-a-table-of-contents-automatically"></a>Generazione automatica di un sommario

In questo argomento viene illustrato come utilizzare il componente [**Table of Contents Generator**](/previous-versions/ee264297(v=vs.85)) (Generatore Sommario) per generare automaticamente un sommario per un file video.

Il generatore di sommario è un oggetto DMO (DirectX Media Object). Per usare il generatore di sommario DMO, compilare un grafico di filtro DirectX con un file video come origine. Inserire il generatore di sommario DMO nel grafico del filtro ed eseguire il grafo. È quindi possibile ottenere il sommario generato automaticamente dal generatore di sommario DMO.

La procedura seguente illustra in modo più dettagliato i passaggi.

1.  Chiamare [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per creare un oggetto grafico di filtro (**CLSID \_ filtergraph**) e ottenere un'interfaccia [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) .
2.  Chiamare [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per creare un oggetto filtro wrapper DMO (**CLSID \_ DMOWrapperFilter**) e ottenere un'interfaccia [**IDMOWrapperFilter**](/previous-versions/windows/desktop/api/dmodshow/nn-dmodshow-idmowrapperfilter) .
3.  Passare **CLSID \_ CTocGeneratorDmo** al metodo [**init**](/previous-versions/windows/desktop/api/dmodshow/nf-dmodshow-idmowrapperfilter-init) del filtro del wrapper DMO. Viene creato un generatore di sommario DMO e ne viene eseguito il wrapping nel filtro del wrapper DMO.
4.  Chiamare il metodo [**addFilter**](/windows/win32/api/strmif/nf-strmif-ifiltergraph-addfilter) dell'interfaccia [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) per aggiungere il generatore di sommario con wrapper DMO al grafo del filtro.
    > [!Note]  
    > [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) eredita da [**IFilterGraph**](/windows/win32/api/strmif/nn-strmif-ifiltergraph).

     

5.  Chiamare il metodo [**AddSourceFilter**](/windows/win32/api/strmif/nf-strmif-igraphbuilder-addsourcefilter) dell'interfaccia [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) per creare un filtro origine e aggiungerlo al grafico.
6.  Enumerare i pin sul filtro del wrapper DMO e sul filtro di origine. Ciò implica l'ottenimento delle interfacce [**IEnumPins**](/windows/win32/api/strmif/nn-strmif-ienumpins) e delle interfacce [**Ipin**](/windows/win32/api/strmif/nn-strmif-ipin) .
7.  Connettere il filtro di origine e il filtro wrapper chiamando il metodo [**Connect**](/windows/win32/api/strmif/nf-strmif-igraphbuilder-connect) dell'interfaccia [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) .
8.  Completare il grafo chiamando il metodo [**Render**](/windows/win32/api/strmif/nf-strmif-igraphbuilder-render) dell'interfaccia [**IGraphBuilder**](/windows/win32/api/strmif/nn-strmif-igraphbuilder) .
9.  Eseguire il grafo ([**IMediaControl:: Run**](/windows/win32/api/control/nf-control-imediacontrol-run)) e attenderne il completamento ([**IMediaEvent:: WaitForCompletion**](/windows/win32/api/control/nf-control-imediaevent-waitforcompletion)).
10. Ottenere un'interfaccia [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) sul wrapper del filtro DMO e ottenere il valore della proprietà [**MFPKEY \_ TOCGENERATOR \_ TOCREADY**](/previous-versions/ee264297(v=vs.85)) . Ripetere se necessario finché il sommario non è pronto.
11. Usare l'interfaccia [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) per ottenere il valore della proprietà [**MFPKEY \_ TOCGENERATOR \_ tocobject**](/previous-versions/ee264297(v=vs.85)) . Questa proprietà è un'interfaccia [**IToc**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc) che rappresenta il sommario generato automaticamente.

Nel codice seguente viene illustrata la procedura per la generazione automatica di un sommario. Il codice usa tre funzioni helper ([**BuildGraph**](buildgraph-method-for-generating-a-table-of-contents.md), [**RunGraphAndWait**](rungraphandwait-method-for-generating-a-table-of-contents.md)e [**GetToc**](gettoc-method-for-generating-a-table-of-contents.md)) visualizzate in altre pagine di questa documentazione.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Funzione BuildGraph per la generazione di un sommario](buildgraph-method-for-generating-a-table-of-contents.md)
</dt> <dt>

[Funzione GetToc per la generazione di un sommario](gettoc-method-for-generating-a-table-of-contents.md)
</dt> <dt>

[Funzione RunGraphAndWait per la generazione di un sommario](rungraphandwait-method-for-generating-a-table-of-contents.md)
</dt> <dt>

[Guida per programmatori del parser Sommario](toc-parser-programming-guide.md)
</dt> </dl>

 

 
