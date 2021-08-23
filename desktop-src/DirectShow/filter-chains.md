---
description: Catene di filtri
ms.assetid: c17b3b58-65ab-4e83-91f2-54a995f22ddf
title: Catene di filtri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4650c49dd796ff3aa7ddecbd21076a4e217def9bfb6504149fdb740c2810b48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119685483"
---
# <a name="filter-chains"></a>Catene di filtri

Una *catena di* filtri è una sequenza di filtri che soddisfa le condizioni seguenti:

-   Ogni filtro nella catena ha al massimo un pin di input connesso e un pin di output connesso.
-   È possibile attraversare ogni filtro nella catena senza attraversare i filtri all'esterno della catena.

Nel diagramma seguente, ad esempio, i filtri A-B, C-D e F-G-H sono catene di filtri. Ogni subchain in F-G-H (F-G e G-H) è anche una catena di filtri. Una catena di filtri può essere costituita da un singolo filtro, quindi anche i filtri A, B, C, D, F, G e H sono catene di filtri distinte. Il filtro E ha due connessioni di input, quindi qualsiasi sequenza di filtri che include il filtro E non è una catena di filtri.

![catena di filtri (esempio 1)](images/filter-chain1.png)

[**L'interfaccia IFilterChain**](/windows/desktop/api/Strmif/nn-strmif-ifilterchain) fornisce i metodi seguenti per controllare le catene di filtri:



| Etichetta | Valore |
|---------------------------------------------------------------|---------------------------------|
| [**IFilterChain::StartChain**](/windows/desktop/api/Strmif/nf-strmif-ifilterchain-startchain)   | Avvia una catena.                 |
| [**IFilterChain::StopChain**](/windows/desktop/api/Strmif/nf-strmif-ifilterchain-stopchain)     | Arresta una catena.                  |
| [**IFilterChain::P auseChain**](/windows/desktop/api/Strmif/nf-strmif-ifilterchain-pausechain)   | Sospende una catena.                 |
| [**IFilterChain::RemoveChain**](/windows/desktop/api/Strmif/nf-strmif-ifilterchain-removechain) | Rimuove una catena dal grafico. |



 

Non esiste alcun metodo specifico per l'aggiunta di una catena. Per aggiungere una catena, inserire i nuovi filtri usando il [**metodo IFilterGraph::AddFilter.**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) Connettere quindi i filtri chiamando [**IGraphBuilder::Connessione**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect), [**IGraphBuilder::Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render)o metodi simili.

Quando il grafico è in esecuzione, una catena di filtri può passare dall'esecuzione all'arresto. Quando il grafico viene sospeso, può passare da sospeso a arrestato. Queste sono le uniche transizioni di stato possibili con le catene di filtri.

## <a name="filter-chain-guidelines"></a>Linee guida per la catena di filtri

Quando si usano **i metodi IFilterChain,** è importante assicurarsi che i filtri nel grafo supportino le operazioni di concatenamento dei filtri. In caso contrario, potrebbero verificarsi deadlock o errori del grafo. I filtri connessi alla catena devono funzionare correttamente dopo che lo stato della catena cambia.

Il modo migliore per usare **IFilterChain** è con un set di filtri progettato appositamente per il concatenamento. Usare le linee guida seguenti per assicurarsi che i filtri siano sicuri per le operazioni della catena di filtri. Questi punti fanno riferimento al diagramma seguente.

![catena di filtri (esempio 2)](images/filter-chain2.png)

-   Prima che lo stato della catena di filtri cambi, tutte le chiamate di elaborazione dati al limite della catena di filtri devono essere completate. Questa regola si applica ai [**metodi IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive), [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment)e [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream). I filtri nella catena devono restituire le chiamate a questi metodi effettuati da filtri all'esterno della catena; e i filtri all'esterno della catena devono restituire le chiamate effettuate dai filtri all'interno della catena.

Nel diagramma precedente, ad esempio, il filtro B deve completare tutte le chiamate di elaborazione dati dal filtro A e il filtro E deve completare tutte le chiamate dal filtro D. Se i pin espongono le interfacce [**IPinFlowControl**](/windows/desktop/api/Strmif/nn-strmif-ipinflowcontrol) e [**IPinConnection,**](/windows/desktop/api/Strmif/nn-strmif-ipinconnection) è possibile eseguire il push dei dati tramite il grafo chiamando i metodi [**IPinFlowControl::Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) e [**IGraphConfig::P ushThroughData,**](/windows/desktop/api/Strmif/nf-strmif-igraphconfig-pushthroughdata) come descritto in Riconnessione [dinamica.](dynamic-reconnection.md) I filtri possono anche supportare metodi privati per il push dei dati.

-   I filtri upstream devono prevedere la modifica dello stato della catena. Ad esempio, nel diagramma precedente si supponga che la catena sia arrestata ma che il filtro A **chiami IMemInputPin::Receive**. La chiamata non riesce e la risposta del filtro A è arrestare lo streaming. Quando l'applicazione riavvia la catena, non ha alcun effetto perché il filtro A non esegue più lo streaming dei dati.
-   Anche i filtri downstream devono prevedere la modifica dello stato della catena. In caso contrario, il filtro downstream potrebbe bloccarsi durante l'attesa di campioni che non arrivano mai. Ad esempio, i filtri multiplexer (MUX) spesso richiedono dati da tutti i pin di input. L'interruzione del flusso di dati da un pin di input potrebbe impedire l'elaborazione degli altri flussi. Ciò può causare un deadlock del grafo.
-   Ogni connessione pin da un filtro esterno alla catena a un filtro all'interno della catena deve avere un proprio allocatore, che non è condiviso da altre connessioni. Quando lo stato della catena cambia o viene rimosso dal grafico, l'allocatore potrebbe essere decommesso. Se altre connessioni usano lo stesso allocatore, non possono più elaborare esempi.
-   Non rimuovere una catena a meno che i filtri connessi alla catena non supportino la disconnessione dinamica. In genere, i filtri connessi supportano **l'interfaccia IPinConnection** o **IPinFlowControl,** ma potrebbero invece supportare interfacce private.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Compilazione Graph dinamica](dynamic-graph-building.md)
</dt> </dl>

 

 



