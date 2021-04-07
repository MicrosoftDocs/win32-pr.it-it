---
description: Gestione grafico filtro
ms.assetid: b1a53193-27c6-4e86-a5b9-f3c1e4401690
title: Gestione grafico filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7161f15ea04e1404425d4671ca7991420e0aa993
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876018"
---
# <a name="filter-graph-manager"></a>Gestione grafico filtro

Filter Graph Manager compila e controlla i grafici dei filtri. Questo oggetto è il componente centrale in DirectShow. Le applicazioni lo usano per compilare e controllare i grafici di filtro. Filter Graph Manager gestisce anche la sincronizzazione, la notifica degli eventi e altri aspetti del controllo del grafico del filtro. Creare questo oggetto chiamando **CoCreateInstance**.

### <a name="clsid"></a>CLSID

Sono disponibili due CLSID per la creazione del gestore del grafico dei filtri:



| CLSID                      | Descrizione                                                 |
|----------------------------|-------------------------------------------------------------|
| \_FILTERGRAPH CLSID         | Crea il gestore del grafico di filtro in un thread di lavoro condiviso. |
| \_FILTERGRAPHNOTHREAD CLSID | Crea il gestore del grafico del filtro nel thread dell'applicazione. |



 

In genere, le applicazioni devono usare CLSID \_ filtergraph. Entrambi i CLSID creano lo stesso oggetto, ma utilizzano modelli di threading diversi:

-   CLSID \_ filtergraph crea Filter Graph Manager in un thread di lavoro, che è condiviso da tutte \_ le istanze di filtergraph CLSID nello stesso processo. Il thread invia i messaggi inviati dai filtri e controlla la durata di tutte le finestre create dai filtri.
-   CLSID \_ FilterGraphNoThread crea il gestore del grafo del filtro nel thread dell'applicazione. Se si utilizza questo CLSID, il thread che chiama **CoCreateInstance** deve disporre di un ciclo di messaggi che invia i messaggi; in caso contrario, possono verificarsi deadlock. Inoltre, prima che il thread dell'applicazione venga chiuso, deve rilasciare Filter Graph Manager e tutti gli oggetti Graph, ad esempio filtri, pin, orologi di riferimento e così via.

### <a name="interfaces"></a>Interfacce

Il gestore del grafo del filtro espone le interfacce seguenti:

-   [**IAMGraphStreams**](/windows/desktop/api/Strmif/nn-strmif-iamgraphstreams)
-   [**IAMStats**](/windows/desktop/api/Control/nn-control-iamstats)
-   [**IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio)
-   [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo)
-   [**IBasicVideo2**](/windows/desktop/api/Control/nn-control-ibasicvideo2)
-   [**IFilterChain**](/windows/desktop/api/Strmif/nn-strmif-ifilterchain)
-   [**IFilterGraph**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph)
-   [**IFilterGraph2**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph2)
-   [**IFilterGraph3**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph3)
-   [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2)
-   [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder)
-   [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig)
-   [**IGraphVersion**](/windows/desktop/api/Strmif/nn-strmif-igraphversion)
-   [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol)
-   [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent)
-   [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex)
-   [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink)
-   [**IMediaFilter**](/windows/desktop/api/Strmif/nn-strmif-imediafilter)
-   [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition)
-   [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)
-   [**IQueueCommand**](/windows/desktop/api/Control/nn-control-iqueuecommand)
-   [**IRegisterServiceProvider**](/windows/desktop/api/Strmif/nn-strmif-iregisterserviceprovider)
-   [**IResourceManager**](/windows/desktop/api/Strmif/nn-strmif-iresourcemanager)
-   **IServiceProvider**
-   [**IVideoFrameStep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep)
-   [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Oggetti DirectShow](directshow-objects.md)
</dt> </dl>

 

 



