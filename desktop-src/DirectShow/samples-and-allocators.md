---
description: Esempi e allocatori
ms.assetid: 1fbea741-f29a-4815-9885-94ca9cf4bb95
title: Esempi e allocatori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f9132ff2c70b5ade63f8853b5c03bacb7a25371
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104555751"
---
# <a name="samples-and-allocators"></a>Esempi e allocatori

Quando un pin recapita i dati multimediali a un altro pin, non passa un puntatore diretto al buffer di memoria. Fornisce invece un puntatore a un oggetto COM che gestisce la memoria. Questo oggetto, denominato *esempio multimediale*, espone l'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) . Il pin di ricezione accede al buffer di memoria chiamando i metodi **IMediaSample** , ad esempio [**IMediaSample:: getpointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer), [**IMediaSample:: GetSize**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getsize)e [**IMediaSample:: GetActualDataLength**](/windows/win32/api/strmif/nf-strmif-imediasample-getactualdatalength).

Gli esempi viaggiano sempre a valle, dal pin di output al pin di input. Nel modello push il pin di output recapita un esempio chiamando [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) sul pin di input. Il pin di input elabora i dati in modo sincrono (ovvero completamente all'interno del metodo **Receive** ) o li elabora in modo asincrono in un thread di lavoro. Il pin di input può essere bloccato all'interno del metodo **Receive** , se è necessario attendere le risorse.

Un altro oggetto COM, denominato *allocatore*, è responsabile della creazione e della gestione degli esempi di supporti. Gli allocatori espongono l'interfaccia [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) . Ogni volta che un filtro necessita di un campione multimediale con un buffer vuoto, chiama il metodo [**IMemAllocator:: GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) , che restituisce un puntatore all'esempio. Ogni connessione pin condivide un allocatore. Quando due pin si connettono, decidono quale filtro fornirà l'allocatore. I pin impostano inoltre le proprietà nell'allocatore, ad esempio il numero di buffer e le dimensioni di ogni buffer. Per informazioni dettagliate, vedere [How filters Connect](how-filters-connect.md) and [negotiating allocator](negotiating-allocators.md).

Nella figura seguente sono illustrate le relazioni tra l'allocatore, gli esempi di supporti e il filtro.

![esempi di supporti e allocatori](images/mediasamples.png)

**Conteggio riferimenti di esempio multimediale**

Un allocatore crea un pool finito di esempi. In qualsiasi momento, è possibile che alcuni esempi siano in uso, mentre altri sono disponibili per le chiamate a **GetBuffer** . L'allocatore usa il conteggio dei riferimenti per tenere traccia degli esempi. Il metodo **GetBuffer** restituisce un campione con un conteggio dei riferimenti pari a 1. Se il conteggio dei riferimenti va a zero, l'esempio torna al pool dell'allocatore, dove può essere usato nella chiamata a **GetBuffer** successiva. Fino a quando il conteggio dei riferimenti rimane superiore a zero, l'esempio non è disponibile per **GetBuffer**. Se ogni esempio appartenente all'allocatore è in uso, il metodo **GetBuffer** si blocca fino a quando non viene reso disponibile un campione.

Si supponga, ad esempio, che un pin di input riceva un campione. Se l'esempio viene elaborato in modo sincrono, all'interno del metodo **Receive** , il conteggio dei riferimenti non viene incrementato. Dopo la restituzione di **Receive** , il pin di output rilascia l'esempio, il conteggio dei riferimenti va a zero e l'esempio ritorna al pool dell'allocatore. D'altra parte, se il pin di input elabora l'esempio in un thread di lavoro, incrementa il conteggio dei riferimenti prima di lasciare il metodo **Receive** . Il conteggio dei riferimenti è ora 2. Quando il pin di output rilascia l'esempio, il conteggio va a 1. Nell'esempio non viene ancora restituito al pool. Al termine dell'esempio, il thread di lavoro chiama **Release** per liberare l'esempio. A questo punto, l'esempio ritorna al pool.

Quando un pin riceve un campione, può copiare i dati in un altro esempio oppure può modificare l'esempio originale e recapitarlo al filtro successivo. Potenzialmente, un campione può attraversare l'intera lunghezza del grafo, ogni filtro che chiama **AddRef** e **Release** a sua volta. Il pin di output, quindi, non deve mai riutilizzare un campione dopo la chiamata di **Receive**, perché un filtro downstream può utilizzare l'esempio. Il pin di output deve sempre chiamare **GetBuffer** per ottenere un nuovo campione.

Questo meccanismo riduce la quantità di allocazione di memoria, perché i filtri riutilizzano gli stessi buffer. Impedisce inoltre ai filtri di scrivere accidentalmente sui dati che non sono stati elaborati, poiché l'allocatore gestisce un elenco di esempi disponibili.

Un filtro può utilizzare allocatori distinti per l'input e l'output. Questa operazione può essere eseguita se espande i dati di input (ad esempio, decomprimendo). Se l'output non è maggiore dell'input, un filtro potrebbe elaborare i dati sul posto, senza copiarli in un nuovo esempio. In tal caso, due o più connessioni pin possono condividere un allocatore.

**Commit e decommit di allocatori**

Quando un filtro crea prima un allocatore, l'allocatore non ha riservato alcun buffer di memoria. A questo punto, tutte le chiamate al metodo **GetBuffer** avranno esito negativo. Quando viene avviato il flusso, il pin di output chiama [**IMemAllocator:: commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit), che esegue il commit dell'allocatore, causando l'allocazione della memoria. I pin ora possono chiamare **GetBuffer**.

Quando il flusso viene interrotto, il pin chiama [**IMemAllocator::D ecommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit), che esegue il commit dell'allocatore. Tutte le chiamate successive a **GetBuffer** hanno esito negativo fino a quando non viene eseguito il commit dell'allocatore Se, inoltre, le chiamate a **GetBuffer** sono attualmente bloccate in attesa di un campione, restituiscono immediatamente un codice di errore. Il metodo di **decommit** può o non liberare la memoria, a seconda dell'implementazione. La classe [**CMemAllocator**](cmemallocator.md) , ad esempio, attende fino a quando il metodo del distruttore non libera la memoria.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Flusso di dati nel grafico del filtro](data-flow-in-the-filter-graph.md)
</dt> </dl>

 

 
