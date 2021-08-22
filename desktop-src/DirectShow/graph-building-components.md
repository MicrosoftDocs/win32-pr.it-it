---
description: Graph-Building componenti
ms.assetid: d803c56c-6fb1-4937-92e7-9ed2db2afc46
title: Graph-Building componenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14aabcf31f55d0d42117e39cb22fa286b383641c94fe21f386345fd8db1cc890
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119564641"
---
# <a name="graph-building-components"></a>Graph-Building componenti

DirectShow fornisce diversi componenti che possono essere usati per creare grafici di filtro. tra cui:

-   [Filtrare Graph Manager](filter-graph-manager.md). Questo oggetto controlla il grafico dei filtri. Supporta le [**interfacce IGraphBuilder,**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol)e [**IMediaEventEx,**](/windows/desktop/api/Control/nn-control-imediaeventex) tra le altre. Tutte DirectShow applicazioni usano questo oggetto a un certo punto, anche se in alcuni casi un altro oggetto crea Filter Graph Manager per l'applicazione.
-   [Acquisisci Graph Builder](capture-graph-builder.md). Questo oggetto fornisce metodi aggiuntivi per la creazione di grafi di filtro. Originariamente è stato progettato per la creazione di grafici che eseguono l'acquisizione video (da qui il nome), ma è utile per molti altri tipi di grafico di filtro personalizzato. Supporta [**l'interfaccia ICaptureGraphBuilder2.**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2)
-   [Filter Mapper](filter-mapper.md) e [System Device Enumerator](system-device-enumerator.md). Questi oggetti individuano i filtri registrati nel sistema dell'utente o che rappresentano i dispositivi hardware.
-   [DVD Graph Builder](dvd-graph-builder.md). Questo oggetto crea grafici di filtro per la riproduzione e la navigazione dei DVD. Supporta [**l'interfaccia IDvdGraphBuilder.**](/windows/desktop/api/Strmif/nn-strmif-idvdgraphbuilder)

### <a name="intelligent-connect"></a>Gestione Connessione

Il termine "Intelligent Connessione" copre un set di algoritmi che Filter Graph Manager usa per compilare tutto o parte di un grafico filtri. Ogni volta che gestione Graph filtro richiede filtri aggiuntivi per completare il grafico, esegue approssimativamente le operazioni seguenti:

1.  Se nel grafico è attualmente presente un filtro con almeno un pin di input Graph non associato, Gestione filtri tenta di usare tale filtro.
2.  In caso contrario, Filter Graph Manager cerca nel Registro di sistema i filtri che possono accettare il tipo di supporto corretto per la connessione. Ogni filtro ha un valore del Registro di sistema denominato "Merito", che indica approssimativamente la probabilità che il filtro sia utile per completare il grafico. Gestione filtri Graph filtri tenta i filtri in ordine di valore di merito. Per ogni tipo di flusso (ad esempio audio, video o MIDI), il renderer predefinito ha un merito elevato. Anche i decodificatori hanno un merito elevato. I filtri per utilizzo speciale hanno un merito basso.

Se Gestione filtri Graph si blocca, verrà visualizzato di nuovo e verrà tentata una combinazione diversa di filtri. È possibile trovare i dettagli esatti nell'argomento [Intelligent Connessione](intelligent-connect.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Compilazione del filtro Graph](building-the-filter-graph.md)
</dt> </dl>

 

 



