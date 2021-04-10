---
description: Componenti Graph-Building
ms.assetid: d803c56c-6fb1-4937-92e7-9ed2db2afc46
title: Componenti Graph-Building
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea3ba346356109d8080d887a510cfcb85b6a6c80
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125586"
---
# <a name="graph-building-components"></a>Componenti Graph-Building

DirectShow fornisce diversi componenti che possono essere usati per compilare i grafici dei filtri. tra cui:

-   [Gestione grafico filtro](filter-graph-manager.md). Questo oggetto controlla il grafico del filtro. Supporta le interfacce [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder), [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol)e [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) , tra le altre. Tutte le applicazioni DirectShow utilizzano questo oggetto a un certo punto, sebbene in alcuni casi un altro oggetto crei la gestione del grafico del filtro per l'applicazione.
-   [Acquisisci il generatore Graph](capture-graph-builder.md). Questo oggetto fornisce metodi aggiuntivi per la compilazione di grafici di filtro. È stata originariamente progettata per la creazione di grafici che eseguono l'acquisizione video, di conseguenza il nome, ma è utile per molti altri tipi di grafico filtro personalizzato. Supporta l'interfaccia [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) .
-   [Mapper di filtri](filter-mapper.md) e [enumeratori di dispositivi di sistema](system-device-enumerator.md). Questi oggetti individuano i filtri registrati nel sistema dell'utente o che rappresentano i dispositivi hardware.
-   [Generatore di grafici DVD](dvd-graph-builder.md). Questo oggetto compila i grafici filtro per la riproduzione e la navigazione in DVD. Supporta l'interfaccia [**IDvdGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-idvdgraphbuilder) .

### <a name="intelligent-connect"></a>Connessione intelligente

Il termine "connessione intelligente" riguarda un set di algoritmi utilizzati dal gestore del grafo del filtro per compilare tutto o parte di un grafico di filtro. Ogni volta che il gestore del grafico dei filtri richiede filtri aggiuntivi per completare il grafo, esegue approssimativamente le operazioni seguenti:

1.  Se è presente un filtro attualmente nel grafico, con almeno un pin di input non connesso, il gestore del grafico del filtro tenta di utilizzare tale filtro.
2.  In caso contrario, il gestore del grafico dei filtri Cerca nel registro di sistema i filtri che possono accettare il tipo di supporto corretto per la connessione. Ogni filtro ha un valore del registro di sistema denominato "Merit", che indica approssimativamente la probabilità che il filtro sia utile per il completamento del grafo. Il gestore del grafico del filtro tenta i filtri in ordine di valore Merit. Per ogni tipo di flusso (ad esempio audio, video o MIDI), il renderer predefinito ha un valore elevato. I decodificatori hanno anche un valore elevato. I filtri per scopi specifici hanno un merito basso.

Se il gestore del grafico dei filtri si blocca, verrà eseguito il backup e si tenterà di usare una combinazione di filtri diversa. È possibile trovare i dettagli esatti nell'argomento [connessione intelligente](intelligent-connect.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione del grafico di filtro](building-the-filter-graph.md)
</dt> </dl>

 

 



