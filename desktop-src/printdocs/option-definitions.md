---
description: Informazioni sulle definizioni delle opzioni nello schema PrintCapabilities. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print Schema Specification( Specifica dello schema di stampa).
ms.assetid: e81068db-ab8e-420c-a0be-93bc92f3df6f
title: Definizioni di opzioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdc7dddb4840de8bc91c7f9ab127fd31319e5399
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549369"
---
# <a name="option-definitions"></a>Definizioni di opzioni

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Print [Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

La considerazione principale quando si definisce un'opzione è di farlo in modo che possa essere confrontata in modo significativo con altre istanze di Option contenute nella stessa funzionalità. Il confronto deve essere significativo perché l'istanza Option viene usata per definire la configurazione non solo del dispositivo, ma del processo, indipendentemente dal dispositivo o da PrintCapabilities usati per creare la configurazione. Le altre istanze di Option in Feature possono essere visualizzate nello stesso documento PrintCapabilities o in un altro documento PrintCapabilities che rappresenta un dispositivo diverso, un documento PrintCapabilities definito da un'altra parte che opera in modo indipendente. Dopo che un client ha selezionato la configurazione del dispositivo da usare per eseguire il rendering di un processo o di un documento, tale configurazione viene in genere salvata, insieme al processo o al documento, sotto forma di PrintTicket. PrintTicket contiene un set di istanze option, in genere una per ogni funzionalità definita nel documento PrintCapabilities. Le istanze delle opzioni devono essere portabili e devono mantenere la finalità di stampa, in modo che la finalità possa essere comunicata quando questo PrintTicket viene assegnato a un dispositivo diverso, anche con un documento PrintCapabilities diverso scritto da un altro autore. Il vantaggio principale di questa portabilità è che se un dispositivo diverso non supporta in modo specifico un'opzione contenuta in PrintTicket, il driver di dispositivo o il sottosistema è in grado di identificare e selezionare l'opzione più vicina nella funzionalità.

Una delle funzioni printTicket principali del driver è identificare l'opzione del dispositivo nel documento PrintCapabilities che corrisponde maggiormente a una determinata opzione elencata in PrintTicket. Durante questo processo di assegnazione dei punteggi corrispondente o definito dal driver di  dispositivo, l'opzione in PrintTicket viene definita opzione di riferimento, mentre l'opzione nel documento PrintCapabilities viene definita opzione *candidata.* La metrica di corrispondenza generale è il numero di istanze ScoredProperty corrispondenti nelle istanze Option candidate e reference; Un numero maggiore di corrispondenze indica in genere una migliore conservazione della finalità di stampa. Nel processo di assegnazione dei punteggi è possibile scegliere di assegnare un peso maggiore ad alcuni elementi ScoredProperty rispetto ad altri.

È possibile rendere portabili le istanze option assicurandosi che tutte le istanze option che appartengono alla stessa funzionalità presentino uno o più elementi ScoredProperty *in comune.* Ciò significa che è presente un set di elementi ScoredProperty che viene visualizzato in ogni istanza di Option (appartenente alla stessa funzionalità). Ad esempio, le istanze Option per la funzionalità PageMediaSize possono essere portabili se ogni istanza Option contiene elementi ScoredProperty che definiscono le proprietà intrinseche PageMediaSize: MediaSizeWidth e MediaSizeHeight. Il codice del driver di dispositivo o del sottosistema può quindi determinare quanto sono concordate due istanze option confrontando le differenze in questi valori ScoredProperty. Se nel documento PrintCapabilities non è presente un'opzione che corrisponda esattamente a quella di PrintTicket, il driver di dispositivo può determinare e selezionare facilmente l'opzione con le dimensioni del supporto corrispondenti più vicine.

Due oggetti (istanze option in questo caso) hanno elementi *in comune* o, in modo equivalente, hanno elementi corrispondenti, se vengono soddisfatte le tre condizioni seguenti. 

1.  I due elementi sono dello stesso tipo di elemento.

2.  Gli attributi del nome dei due elementi sono identici (o nessuno dei due elementi contiene un attributo name).

3.  La catena di elementi padre degli elementi confrontati, fino ai due oggetti considerati, deve soddisfare le condizioni 1 e 2.

Si consideri, ad esempio, una situazione in cui sono presenti due istanze option, ognuna delle quali contiene un'istanza ScoredProperty e ognuna di queste istanze scoredProperty contiene un'istanza Property. Ovviamente, viene soddisfatta la prima condizione (le due istanze Property sono dello stesso tipo) e viene soddisfatta parte della terza condizione (gli elementi padre delle istanze Property sono dello stesso tipo, ScoredProperty, e gli elementi padre di tali elementi sono le istanze Option, che sono anche dello stesso tipo). Se gli attributi name rispettivamente delle istanze Property, ScoredProperty e Option sono identici o non sono specificati, le due istanze Option hanno elementi in comune.

Dal precedente, il primo passaggio per la creazione di istanze option consiste nel definire un set di elementi ScoredProperty presenti nella maggior parte o in tutte le istanze option. Se l'attributo di configurazione del dispositivo può essere rappresentato da una funzionalità standard (elencata nelle parole chiave dello schema di stampa), prendere nota degli elementi ScoredProperty in comune nelle istanze Option standard. È necessario assicurarsi che tutte le nuove istanze option introdotte contengano anche questi elementi ScoredProperty. È sempre possibile aggiungere altri elementi ScoredProperty in base alle esigenze per differenziare le istanze Option dalle istanze Option standard. È anche possibile eliminare uno o più elementi ScoredProperty in comune se esiste un motivo valido, anche se ciò riduce la portabilità di tale opzione. Naturalmente, le considerazioni sulla portabilità suggeriscono l'uso delle istanze Option standard non modificati, a meno che non vi sia una differenza intrinseca tra l'opzione e l'istanza standard di Option che deve essere riflessa nella nuova istanza di Option.

L'esempio seguente illustra una situazione per cui è possibile aggiungere un elemento ScoredProperty a un'istanza Option. Tutte le istanze Option standard per la funzionalità PageMediaSize hanno in comune gli elementi MediaSizeWidth e MediaSizeHeight ScoredProperty. Si supponga che il dispositivo sia in grado di supportare uno dei formati di supporti Letter standard, invicendo la carta in modo inverso (LongEdgeFirst) o longitudinamente (ShortEdgeFirst). Supponendo di non voler introdurre una nuova funzionalità di direzione del feed per esporre questo grado di libertà, è invece possibile modificare le due istanze dell'opzione PageMediaSize per Letter per incorporare l'orientamento dell'alimentazione della carta. Per queste due istanze di Letter Option, iniziare con l'istanza standard pageMediaSize Option e aggiungere un nuovo elemento ScoredProperty per rappresentare FeedDirection. In un'istanza Option impostare FeedDirection ScoredProperty su LongEdgeFirst; Nell'altra istanza di Option impostare FeedDirection su ShortEdgeFirst. Si noti che queste nuove istanze option mantengono la portabilità. Se l'opzione che rappresenta Letter, ShortEdgeFirst viene salvata in un PrintTicket ed è selezionato un altro dispositivo che supporta solo l'opzione standard Letter per il rendering del processo, il codice di corrispondenza delle opzioni può determinare rapidamente che la lettera di opzione standard è la corrispondenza migliore con la lettera di opzione ShortEdgeFirst. Il motivo per cui questa è la corrispondenza migliore è che tutte le istanze scoredProperty sono d'accordo, ad eccezione di FeedDirection ScoredProperty, che non esiste nell'opzione standard Letter.

È anche possibile riscontrare casi in cui le modifiche apportate all'opzione modificano effettivamente il significato a tal punto che l'opzione modificata non può più essere considerata un caso specializzato dell'originale. In questi casi, è necessario modificare il nome dell'opzione in modo da riflettere la differenza tra l'istanza dell'opzione modificata e quella non modificata. Solo l'autore del documento PrintCapabilities per un determinato dispositivo può decidere se l'opzione offerta dal dispositivo è sufficientemente diversa da un'istanza Option standard per garantire una definizione incompatibile.

Si consideri ora il caso in cui il dispositivo abbia un attributo di configurazione del dispositivo che non corrisponde ad alcuna delle istanze di funzionalità standard. In questo caso non è possibile basarsi sulle istanze option standard per fornire l'elenco di elementi ScoredProperty in comune. Quando si crea un'istanza scoredProperty, l'obiettivo principale è distinguere ogni opzione dalle altre nella funzionalità e descrivere il motivo per cui un utente seleziona un'opzione rispetto a un'altra. La linea di base è quella di caratterizzare ogni opzione con un attributo nome univoco e scoredProperty che contiene l'attributo name diventa quello usato per determinare gli elementi in comune.

Dopo aver stabilito un set di elementi ScoredProperty in comune, è semplice assegnare i valori appropriati a ogni ScoredProperty per creare ogni opzione. Come nell'esempio precedente, per alcune istanze option potrebbe essere necessario aggiungere altre istanze scoredProperty o eliminare alcuni elementi in comune per creare un'istanza Option appropriata.

Si noti che lo schema di stampa richiede che il set di istanze ScoredProperty, le relative posizioni e i valori assegnati a ogni ScoredProperty in un'opzione rimangano costanti, indipendentemente dalla configurazione. L'intero concetto dello schema di stampa si basa sulle istanze option con istanze property fisse e identificabili e scoredProperty condivise tra più dispositivi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



