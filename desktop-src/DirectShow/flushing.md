---
description: Flushing
ms.assetid: 868218c4-3e1a-4da0-89fa-30a9848da0e8
title: Flushing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 575f311020c2c7a567e544b80ba323a29051cc38
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522401"
---
# <a name="flushing"></a>Flushing

Mentre il grafico del filtro è in esecuzione, è possibile spostarsi tra le quantità arbitrarie di dati nel grafico. Alcune di esse potrebbero trovarsi in code, in attesa di essere recapitate. In alcuni casi il grafo del filtro deve rimuovere questi dati in sospeso il più rapidamente possibile e sostituirli con nuovi dati. Dopo un comando seek, ad esempio, il filtro di origine genera esempi da una nuova posizione nell'origine. Per ridurre al minimo la latenza, è necessario che i filtri downstream eliminino tutti gli esempi creati prima del comando seek. Il processo di eliminazione degli esempi è denominato *svuotamento*. Consente al grafico di essere più reattivo quando gli eventi modificano il flusso di dati normale.

Lo svuotamento viene gestito in modo leggermente diverso dal modello pull rispetto al modello push. Questo articolo inizia con la descrizione del modello push; descrive quindi le differenze nel modello pull.

Lo svuotamento avviene in due fasi.

-   In primo luogo, il filtro di origine chiama [**Ipin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) sul pin di input del filtro downstream. Il filtro downstream inizia a rifiutare gli esempi da upstream. Elimina anche tutti gli esempi che contiene e Invia la chiamata **BeginFlush** downstream al filtro successivo.
-   Quando il filtro di origine è pronto per l'invio di nuovi dati, viene chiamato [**Ipin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) sul pin di input. Viene segnalato il filtro downstream che può ricevere nuovi esempi. Il filtro downstream Invia la chiamata **EndFlush** al filtro successivo.

Nel metodo **BeginFlush** , il pin di input esegue le operazioni seguenti:

1.  Chiama **BeginFlush** nei pin di input downstream.
2.  Rifiuta qualsiasi altra chiamata che esegue il flusso dei dati, inclusi **Receive** e **EndOfStream**.
3.  Sblocca tutti i filtri upstream che sono bloccati in attesa di un campione dall'allocatore del filtro. Alcuni filtri decommitno gli allocatori a questo scopo.
4.  Esce dalle attese che bloccano il flusso. Ad esempio, i filtri renderer vengono bloccati quando vengono sospesi. Si bloccano anche quando sono in attesa di eseguire il rendering di un campione nel momento in cui il flusso è corretto. Il filtro deve essere sbloccato, in modo che gli esempi in coda upstream possano essere recapitati e rifiutati. Questo passaggio garantisce che tutti i filtri upstream si blocchino.

Nel metodo **EndFlush** , il pin di input esegue le operazioni seguenti:

1.  Attende che tutti gli esempi in coda vengano rimossi.
2.  Libera tutti i dati memorizzati nel buffer. Questo passaggio può essere eseguito a volte nel metodo **BeginFlush** . Tuttavia, **BeginFlush** non è sincronizzato con il thread di streaming. Il filtro non deve elaborare o memorizzare nel buffer più dati tra la chiamata a **BeginFlush** e la chiamata a **EndFlush**.
3.  Cancella le notifiche complete di EC in sospeso \_ .
4.  Chiama **EndFlush** downstream.

A questo punto, il filtro può accettare nuovamente i campioni. Tutti gli esempi sono sicuramente più recenti dello scaricamento.

Nel modello pull il filtro del parser avvia lo scaricamento, anziché il filtro di origine. Non solo chiama **Ipin:: BeginFlush** e **Ipin:: EndFlush** sul filtro downstream, chiama anche [**IAsyncReader:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-beginflush) e [**IAsyncReader:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-endflush) sul pin di *output* del filtro di origine. Se il filtro di origine ha richieste di lettura in sospeso, le ignorerà.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Scaricamento dei dati](flushing-data.md)
</dt> </dl>

 

 



