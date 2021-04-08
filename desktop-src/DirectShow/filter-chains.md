---
description: Catene di filtri
ms.assetid: c17b3b58-65ab-4e83-91f2-54a995f22ddf
title: Catene di filtri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d46e374aca71b024773e4177d09e67c7ee6034ac
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876826"
---
# <a name="filter-chains"></a>Catene di filtri

Una *catena* di filtri è una sequenza di filtri che soddisfa le condizioni seguenti:

-   Ogni filtro della catena ha al massimo un pin di input connesso e un pin di output connesso.
-   È possibile attraversare tutti i filtri della catena senza attraversare i filtri all'esterno della catena.

Nel diagramma seguente, ad esempio, i filtri A-B, C-D e F – G – H sono catene di filtri. Ogni sottocatena in F – G – H (F – G e G – H) è anche una catena di filtri. Una catena di filtri può essere costituita da un singolo filtro, quindi i filtri A, B, C, D, F, G e H sono anche catene di filtri distinti. Filter E include due connessioni di input, pertanto qualsiasi sequenza di filtri che includa Filter E non è una catena di filtri.

![catena di filtri (esempio 1)](images/filter-chain1.png)

L'interfaccia [**IFilterChain**](/windows/desktop/api/Strmif/nn-strmif-ifilterchain) fornisce i metodi seguenti per controllare le catene di filtri:



|                                                               |                                 |
|---------------------------------------------------------------|---------------------------------|
| [**IFilterChain::StartChain**](/windows/desktop/api/Strmif/nf-strmif-ifilterchain-startchain)   | Avvia una catena.                 |
| [**IFilterChain::StopChain**](/windows/desktop/api/Strmif/nf-strmif-ifilterchain-stopchain)     | Arresta una catena.                  |
| [**IFilterChain::P auseChain**](/windows/desktop/api/Strmif/nf-strmif-ifilterchain-pausechain)   | Sospende una catena.                 |
| [**IFilterChain::RemoveChain**](/windows/desktop/api/Strmif/nf-strmif-ifilterchain-removechain) | Rimuove una catena dal grafico. |



 

Non esiste alcun metodo specifico per l'aggiunta di una catena. Per aggiungere una catena, inserire i nuovi filtri usando il metodo [**IFilterGraph:: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) . Connettere quindi i filtri chiamando [**IGraphBuilder:: Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect), [**IGraphBuilder:: Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render)o metodi simili.

Quando il grafico è in esecuzione, una catena di filtri può spostarsi tra l'esecuzione e l'arresto. Quando il grafico è sospeso, può passare da una pausa all'altra e viceversa. Queste sono le uniche transizioni di stato possibili con le catene di filtri.

## <a name="filter-chain-guidelines"></a>Linee guida per la catena di filtri

Quando si usano i metodi **IFilterChain** , è importante assicurarsi che i filtri nel grafico possano supportare le operazioni di concatenamento dei filtri. In caso contrario, è possibile che si verifichino deadlock o errori del grafo. I filtri connessi alla catena devono funzionare correttamente dopo che lo stato della catena è stato modificato.

Il modo migliore per usare **IFilterChain** è costituito da un set di filtri progettati in modo specifico per il concatenamento. Usare le linee guida seguenti per assicurarsi che i filtri siano sicuri per le operazioni a catena di filtri. Questi punti fanno riferimento al diagramma seguente.

![catena di filtri (esempio 2)](images/filter-chain2.png)

-   Prima che lo stato della catena di filtri venga modificato, è necessario completare tutte le chiamate di elaborazione dati al limite della catena di filtri. Questa regola si applica ai metodi [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive), [**Ipin:: NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment)e [**Ipin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream). I filtri nella catena devono restituire dalle chiamate a questi metodi creati da filtri all'esterno della catena; i filtri e all'esterno della catena devono restituire dalle chiamate effettuate da filtri all'interno della catena.

Nel diagramma precedente, ad esempio, il filtro B deve completare qualsiasi chiamata di elaborazione dati dal filtro A e il filtro E deve terminare tutte le chiamate dal filtro D. Se i pin espongono le interfacce [**IPinFlowControl**](/windows/desktop/api/Strmif/nn-strmif-ipinflowcontrol) e [**IPinConnection**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection) , è possibile eseguire il push dei dati tramite il grafo chiamando il metodo [**IPinFlowControl:: Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) e [**IGraphConfig::P Ushthroughdata**](/windows/desktop/api/Strmif/nf-strmif-igraphconfig-pushthroughdata) , come descritto in [riconnessione dinamica](dynamic-reconnection.md). I filtri possono inoltre supportare metodi privati per eseguire il push dei dati.

-   I filtri upstream devono prevedere che lo stato della catena venga modificato. Nel diagramma precedente, ad esempio, si supponga che la catena venga arrestata, ma che il filtro A chiami **IMemInputPin:: Receive**. La chiamata ha esito negativo e la risposta del filtro A consiste nell'arrestare lo streaming. Quando l'applicazione riavvia la catena, non ha alcun effetto perché il filtro A non è più in streaming dei dati.
-   Anche i filtri downstream devono prevedere che lo stato della catena venga modificato. In caso contrario, il filtro downstream potrebbe bloccarsi durante l'attesa di campioni che non arrivano mai. I filtri multiplexer (MUX), ad esempio, richiedono spesso i dati di tutti i pin di input. L'arresto del flusso di dati da un pin di input potrebbe impedire l'elaborazione degli altri flussi. Questo può causare il deadlock del grafico.
-   Ogni connessione pin da un filtro all'esterno della catena a un filtro all'interno della catena deve avere un proprio allocatore, che non è condiviso da altre connessioni. Quando la catena cambia stato o viene rimossa dal grafico, è possibile che venga eseguito il commit dell'allocatore. Se altre connessioni utilizzano lo stesso allocatore, non possono più elaborare gli esempi.
-   Non rimuovere una catena, a meno che i filtri connessi alla catena non supportino la disconnessione dinamica. In genere, i filtri connessi supporteranno l'interfaccia **IPinConnection** o **IPinFlowControl** , ma potrebbero supportare invece le interfacce private.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di grafici dinamici](dynamic-graph-building.md)
</dt> </dl>

 

 



