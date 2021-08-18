---
description: Gestione Graph filtri
ms.assetid: b1a53193-27c6-4e86-a5b9-f3c1e4401690
title: Gestione Graph filtri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 793a261f0d7bd12058aa0dc22a448f567fea6847dca6062494f0943eee03a9b3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756721"
---
# <a name="filter-graph-manager"></a>Gestione Graph filtri

Il filtro Graph Manager compila e controlla i grafici dei filtri. Questo oggetto è il componente centrale in DirectShow. Le applicazioni lo usano per compilare e controllare i grafici dei filtri. Filter Graph Manager gestisce anche la sincronizzazione, la notifica degli eventi e altri aspetti del controllo del grafico dei filtri. Creare questo oggetto chiamando **CoCreateInstance.**

### <a name="clsid"></a>CLSID

Sono disponibili due CLSID per la creazione di Filter Graph Manager:



| CLSID                      | Descrizione                                                 |
|----------------------------|-------------------------------------------------------------|
| CLSID \_ FilterGraph         | Crea l'oggetto Filter Graph Manager in un thread di lavoro condiviso. |
| CLSID \_ FilterGraphNoThread | Crea la gestione Graph filtro nel thread dell'applicazione. |



 

In genere, le applicazioni devono usare clsID \_ FilterGraph. Entrambi i CLSID creano lo stesso oggetto, ma usano modelli di threading diversi:

-   ClSID FilterGraph crea filter Graph Manager in un thread di lavoro, condiviso da tutte le istanze filterGraph del CLSID all'interno \_ \_ dello stesso processo. Il thread invia i messaggi inviati dai filtri e controlla la durata di tutte le finestre create dai filtri.
-   ClSID \_ FilterGraphNoThread crea la gestione Graph filtro nel thread dell'applicazione. Se si usa questo CLSID, il thread che chiama **CoCreateInstance** deve avere un ciclo di messaggi che invia messaggi. In caso contrario, possono verificarsi deadlock. Inoltre, prima che il thread dell'applicazione venga chiuso, deve rilasciare Filter Graph Manager e tutti gli oggetti grafico( ad esempio filtri, segnaposto, orologi di riferimento e così via).

### <a name="interfaces"></a>Interfacce

Gestione filtri Graph espone le interfacce seguenti:

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
-   [**Filtro IMediaFilter**](/windows/desktop/api/Strmif/nn-strmif-imediafilter)
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

[DirectShow Oggetti](directshow-objects.md)
</dt> </dl>

 

 



