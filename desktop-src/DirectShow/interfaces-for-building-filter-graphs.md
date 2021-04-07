---
description: Interfacce per la compilazione di grafici di filtro
ms.assetid: 18d5217a-7f4e-49e9-ac14-2f4ba229e065
title: Interfacce per la compilazione di grafici di filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 862d581f44a711cc6f2aa094210571995b15005b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746010"
---
# <a name="interfaces-for-building-filter-graphs"></a>Interfacce per la compilazione di grafici di filtro

Le applicazioni utilizzano queste interfacce per creare vari tipi di grafici dei filtri.



| Interfaccia                                                  | Descrizione                                                 |
|------------------------------------------------------------|-------------------------------------------------------------|
| [**IAMFilterGraphCallback**](/windows/desktop/api/Strmif/nn-strmif-iamfiltergraphcallback)   | Ricevere notifiche di callback se non è possibile eseguire il rendering di un PIN. |
| [**IAMGraphBuilderCallback**](/windows/desktop/api/Strmif/nn-strmif-iamgraphbuildercallback) | Fornisce un meccanismo di callback durante la compilazione del grafo.        |
| [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2)     | Grafici filtro compilazione per acquisizione video.                      |
| [**ICreateDevEnum**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum)                   | Enumerare i dispositivi di sistema, ad esempio i dispositivi di acquisizione.          |
| [**IDvdGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-idvdgraphbuilder)               | Crea grafici filtro per la navigazione e la riproduzione di DVD.        |
| [**IEnumFilters**](/windows/desktop/api/Strmif/nn-strmif-ienumfilters)                       | Enumerare i filtri nel grafico.                         |
| [**IFilterGraph2**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph2)                     | Aggiunta, rimozione o connessione dei filtri.                            |
| [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2)                   | Enumerare i filtri registrati nel sistema dell'utente.      |
| [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder)                     | Crea grafici filtro per la riproduzione di file o per usi personalizzati.   |
| [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig)                       | Riconfigurare dinamicamente un grafico di filtro.                     |
| [**IGraphVersion**](/windows/desktop/api/Strmif/nn-strmif-igraphversion)                     | Determinare quando il grafico viene modificato.                           |



 

 

 



