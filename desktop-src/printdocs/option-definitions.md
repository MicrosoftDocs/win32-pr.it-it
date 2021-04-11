---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: e81068db-ab8e-420c-a0be-93bc92f3df6f
title: Definizioni delle opzioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10016b295cc2da7ede4e6a4f8944f279a25f6f9b
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104234585"
---
# <a name="option-definitions"></a>Definizioni delle opzioni

Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

La considerazione fondamentale quando si definisce un'opzione consiste nell'eseguire questa operazione in modo che possa essere significativa rispetto ad altre istanze di opzioni contenute nella stessa funzionalità. Il confronto deve essere significativo perché l'istanza dell'opzione viene usata per definire la configurazione non solo del dispositivo, ma del processo, indipendentemente dal dispositivo o da PrintCapabilities usati per creare la configurazione. Le altre istanze di opzioni nella funzionalità possono essere visualizzate nello stesso documento PrintCapabilities o in un altro documento PrintCapabilities che rappresenta un dispositivo diverso, un documento PrintCapabilities definito da un'altra parte che opera in modo indipendente. Dopo che un client ha selezionato la configurazione del dispositivo da usare per il rendering di un processo o di un documento, tale configurazione viene in genere salvata, insieme al processo o al documento, sotto forma di un oggetto PrintTicket. L'oggetto PrintTicket contiene un set di istanze di opzioni, in genere una per ogni funzionalità definita nel documento PrintCapabilities. Le istanze delle opzioni devono essere portabili e devono mantenere la finalità di stampa, in modo che lo scopo possa essere comunicato quando questo PrintTicket viene assegnato a un dispositivo diverso, anche uno con un documento PrintCapabilities diverso scritto da un autore diverso. Il vantaggio principale di questa portabilità è che se un dispositivo diverso non supporta specificamente un'opzione contenuta nel PrintTicket, il driver di dispositivo o il sottosistema è in grado di identificare e selezionare l'opzione più vicina alle funzionalità.

Una delle principali funzioni PrintTicket del driver consiste nell'identificare l'opzione del dispositivo nel documento PrintCapabilities che corrisponde maggiormente a una particolare opzione elencata nell'oggetto PrintTicket. Durante questo processo di assegnazione dei punteggi definito da driver di dispositivo o di dispositivo, l'opzione nel PrintTicket viene definita opzione di *riferimento* , mentre l'opzione nel documento PrintCapabilities viene definita opzione *candidata* . La metrica di corrispondenza generale è il numero di istanze di ScoredProperty corrispondenti nelle istanze delle opzioni candidate e di riferimento; un numero maggiore di corrisponde in genere indica una migliore conservazione della finalità di stampa. Nel processo di assegnazione dei punteggi è possibile scegliere di attribuire un peso maggiore ad alcuni elementi ScoredProperty rispetto ad altri.

È possibile rendere portabili le istanze delle opzioni assicurando che tutte le istanze di opzioni che appartengono alla stessa funzionalità dispongano di uno o più *elementi ScoredProperty in comune*. Ciò significa che è presente un set di elementi ScoredProperty che viene visualizzato in ogni istanza di opzione (appartenente alla stessa funzionalità). Ad esempio, le istanze di opzioni per la funzionalità PageMediaSize possono essere portabili se ogni istanza di opzione contiene elementi ScoredProperty che definiscono le proprietà PageMediaSize intrinseche: MediaSizeWidth e MediaSizeHeight. Il codice del driver del dispositivo o del sottosistema può quindi determinare il modo in cui due istanze di opzioni accettano il confronto delle differenze in questi valori ScoredProperty. Se nel documento PrintCapabilities non è presente alcuna opzione che corrisponda esattamente a quella dell'oggetto PrintTicket, il driver di dispositivo può facilmente determinare e selezionare l'opzione con le dimensioni dei supporti corrispondenti più vicine.

Due oggetti (istanze di opzioni in questo caso) hanno *elementi in comune*, o equivalenti, hanno *elementi corrispondenti*, se le tre condizioni seguenti sono soddisfatte.

1.  I due elementi sono dello stesso tipo di elemento.

2.  Gli attributi del nome dei due elementi sono identici (o nessun elemento contiene un attributo Name).

3.  La catena di elementi padre degli elementi confrontati, fino ai due oggetti in considerazione, deve soddisfare le condizioni 1 e 2.

Si consideri, ad esempio, una situazione in cui sono presenti due istanze di opzioni, ciascuna delle quali contiene un'istanza di ScoredProperty, e ognuna di queste istanze di ScoredProperty contiene un'istanza della proprietà. Ovviamente, la prima condizione viene soddisfatta (le due istanze di proprietà sono dello stesso tipo) e viene soddisfatta una parte della terza condizione (gli elementi padre delle istanze di proprietà sono dello stesso tipo, ScoredProperty, e gli elementi padre di tali elementi sono le istanze di opzioni, che sono anche dello stesso tipo). Se gli attributi Name di, rispettivamente, le istanze di proprietà, le istanze ScoredProperty e le istanze dell'opzione sono identici o non vengono specificati, le due istanze delle opzioni hanno elementi in comune.

Dal precedente, il primo passaggio nella creazione delle istanze delle opzioni consiste nel definire un set di elementi ScoredProperty presenti nella maggior parte o in tutte le istanze di opzioni. Se l'attributo di configurazione del dispositivo può essere rappresentato da una funzionalità standard (una elencata nelle parole chiave Print Schema), prendere nota degli elementi ScoredProperty in comune nelle istanze dell'opzione standard. È necessario assicurarsi che tutte le nuove istanze di opzioni introdotte includano anche questi elementi ScoredProperty. È sempre possibile aggiungere altri elementi ScoredProperty in base alle esigenze per distinguere le istanze delle opzioni dalle istanze di opzioni standard. È anche possibile eliminare uno o più elementi ScoredProperty in comune se c'è un buon motivo, anche se questo riduce la portabilità di tale opzione. Naturalmente, le considerazioni sulla portabilità suggeriscono l'uso delle istanze di opzioni standard non modificate a meno che non esista una differenza intrinseca tra l'opzione e l'istanza dell'opzione standard che deve essere riflessa nella nuova istanza dell'opzione.

Nell'esempio seguente viene illustrata una situazione per la quale si desidera aggiungere un elemento ScoredProperty a un'istanza di Option. Tutte le istanze di opzioni standard per la funzionalità PageMediaSize presentano gli elementi ScoredProperty MediaSizeWidth e MediaSizeHeight in comune. Si supponga che il dispositivo sia in grado di supportare una delle dimensioni dei supporti letterali standard alimentando il foglio (LongEdgeFirst) o longitudinalmente (ShortEdgeFirst). Supponendo che non si voglia introdurre una nuova funzionalità di direzione del feed per esporre questo grado di libertà, è possibile modificare le due istanze dell'opzione PageMediaSize per la lettera per incorporare l'orientamento del feed di carta. Per queste istanze di opzioni di due lettere, iniziare con l'istanza di opzione PageMediaSize standard e aggiungere un nuovo elemento ScoredProperty per rappresentare il FeedDirection. In un'istanza di opzione impostare FeedDirection ScoredProperty su LongEdgeFirst; nell'altra istanza di opzione impostare FeedDirection su ShortEdgeFirst. Si noti che queste nuove istanze di opzioni mantengono la portabilità. Se l'opzione che rappresenta la lettera, ShortEdgeFirst viene salvata in un oggetto PrintTicket e un dispositivo diverso che supporta solo l'opzione Letter standard è selezionato per eseguire il rendering del processo, il codice corrispondente all'opzione può determinare rapidamente che la lettera di opzione standard è la migliore corrispondenza con la lettera di opzione, ShortEdgeFirst. Il motivo per cui si tratta della corrispondenza migliore è che tutte le istanze di ScoredProperty accettano, ad eccezione di FeedDirection ScoredProperty, che non esiste nell'opzione Letter standard.

È anche possibile che si verifichino casi in cui le modifiche apportate all'opzione modificano il significato in modo tale che l'opzione modificata non possa più essere considerata un caso specializzato del originale. In questi casi, è necessario modificare il nome dell'opzione in modo da riflettere la differenza tra l'istanza di opzione modificata e quella non modificata. Solo l'autore del documento PrintCapabilities per un determinato dispositivo può decidere se l'opzione offerta dal dispositivo è sufficientemente diversa da un'istanza di opzione standard per garantire una definizione incompatibile.

A questo punto, si consideri il caso in cui il dispositivo ha un attributo di configurazione del dispositivo che non corrisponde ad alcuna istanza di funzionalità standard. In questo caso non è possibile basarsi sulle istanze di opzioni standard per fornire l'elenco di elementi ScoredProperty in comune. Quando si crea un'istanza di ScoredProperty, l'obiettivo principale è distinguere ogni opzione dagli altri nella funzionalità e descrivere il motivo per cui un utente seleziona un'opzione rispetto a un'altra. La linea di base consiste nel caratterizzare ogni opzione con un attributo nome univoco e il ScoredProperty che include l'attributo Name diventa quello utilizzato per determinare gli elementi in comune.

Dopo aver stabilito un set di elementi ScoredProperty in comune, è semplice assegnare i valori appropriati a ogni ScoredProperty per creare ogni opzione. Come nell'esempio precedente, per alcune istanze di opzioni, potrebbe essere necessario aggiungere altre istanze di ScoredProperty o eliminare alcuni degli elementi in comune per creare un'istanza di opzione appropriata.

Si noti che lo schema di stampa richiede che il set di istanze di ScoredProperty, le rispettive posizioni e i valori assegnati a ogni ScoredProperty in un'opzione debbano rimanere costanti, indipendentemente dalla configurazione. L'intero concetto di Print Schema si basa sulle istanze delle opzioni con proprietà fisse e identificabili e istanze di ScoredProperty condivise tra molti dispositivi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



