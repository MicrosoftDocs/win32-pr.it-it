---
description: Flushing
ms.assetid: 868218c4-3e1a-4da0-89fa-30a9848da0e8
title: Flushing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e70f610a68b2ca81afff736b3e7402d80e5d5675e429d1715ebebf5b640a362
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118401745"
---
# <a name="flushing"></a>Flushing

Durante l'esecuzione del grafico dei filtri, è possibile che quantità arbitrarie di dati si svolsino attraverso il grafico. Alcune potrebbero essere in coda, in attesa di essere recapitate. In alcuni casi il grafico dei filtri deve rimuovere i dati in sospeso il più rapidamente possibile e sostituirli con nuovi dati. Dopo un comando di ricerca, ad esempio, il filtro di origine genera campioni da una nuova posizione nell'origine. Per ridurre al minimo la latenza, i filtri downstream devono eliminare tutti i campioni creati prima del comando seek. Il processo di rimozione dei campioni è detto *scaricamento di*. Consente al grafo di essere più reattivo quando gli eventi modificano il flusso di dati normale.

Lo scaricamento viene gestito in modo leggermente diverso dal modello pull rispetto al modello push. Questo articolo inizia descrivendo il modello push. vengono quindi descritte le differenze nel modello pull.

Lo scaricamento avviene in due fasi.

-   In primo luogo, il filtro di [**origine chiama IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) sul pin di input del filtro downstream. Il filtro downstream inizia a rifiutare gli esempi dall'upstream. Rimuove anche tutti i campioni in esso presenti e invia la **chiamata BeginFlush** a valle al filtro successivo.
-   Quando il filtro di origine è pronto per l'invio di nuovi dati, chiama [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) sul pin di input. Questo segnala al filtro downstream che può ricevere nuovi esempi. Il filtro downstream invia la **chiamata EndFlush** al filtro successivo.

Nel metodo **BeginFlush** il pin di input esegue le operazioni seguenti:

1.  Chiama **BeginFlush sui** pin di input downstream.
2.  Rifiuta eventuali altre chiamate che tras streaming di dati, tra **cui Receive** **ed EndOfStream.**
3.  Sblocca tutti i filtri upstream bloccati in attesa di un campione dall'allocatore del filtro. Alcuni filtri esecuno il decommit dei relativi allocatori a questo scopo.
4.  Esce da eventuali attese che bloccano lo streaming. Ad esempio, i filtri del renderer si bloccano quando vengono sospesi. Si bloccano anche quando sono in attesa di eseguire il rendering di un campione al momento del flusso corretto. Il filtro deve essere sbloccato, in modo che i campioni accodati a monte possano essere recapitati e rifiutati. Questo passaggio assicura che tutti i filtri upstream alla fine si sblocchino.

Nel metodo **EndFlush** il pin di input esegue le operazioni seguenti:

1.  Attende che tutti gli esempi in coda siano eliminati.
2.  Libera tutti i dati memorizzati nel buffer. Questo passaggio può talvolta essere eseguito nel **metodo BeginFlush.** **BeginFlush non** è tuttavia sincronizzato con il thread di streaming. Il filtro non deve elaborare o bufferare altri dati tra la chiamata a **BeginFlush** e la chiamata a **EndFlush.**
3.  Cancella tutte le notifiche EC \_ COMPLETE in sospeso.
4.  Chiama **EndFlush** downstream.

A questo punto, il filtro può accettare nuovamente gli esempi. È garantito che tutti i campioni siano più recenti dello scaricamento.

Nel modello pull il filtro del parser avvia lo scaricamento, anziché il filtro di origine. Non solo chiama **IPin::BeginFlush** e **IPin::EndFlush** sul filtro downstream, ma chiama anche [**IAsyncReader::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-beginflush) e [**IAsyncReader::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-endflush) sul pin di *output* del filtro di origine. Se il filtro di origine ha richieste di lettura in sospeso, le rimuoverà.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Scaricamento dei dati](flushing-data.md)
</dt> </dl>

 

 



