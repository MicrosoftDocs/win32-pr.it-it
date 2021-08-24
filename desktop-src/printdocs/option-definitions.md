---
description: Informazioni sulle definizioni delle opzioni nello schema PrintCapabilities. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: e81068db-ab8e-420c-a0be-93bc92f3df6f
title: Definizioni delle opzioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f71f4201bb9bd38860a79fead7fd3e8738429fc34b729981af68c0d2d1f38d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119098955"
---
# <a name="option-definitions"></a>Definizioni delle opzioni

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

La considerazione principale quando si definisce un'opzione è di eseguire questa operazione in modo che possa essere confrontata in modo significativo con altre istanze option contenute nella stessa funzionalità. Il confronto deve essere significativo perché l'istanza Option viene usata per definire la configurazione non solo del dispositivo, ma del processo, indipendentemente dal dispositivo o printCapabilities usato per creare la configurazione. Le altre istanze Option nella funzionalità possono essere visualizzate nello stesso documento PrintCapabilities o in un altro documento PrintCapabilities che rappresenta un dispositivo diverso, un documento PrintCapabilities definito da un'altra parte che funziona in modo indipendente. Dopo che un client ha selezionato la configurazione del dispositivo da usare per il rendering di un processo o di un documento, tale configurazione viene in genere salvata, insieme al processo o al documento, sotto forma di PrintTicket. PrintTicket contiene un set di istanze Option, in genere una per ogni funzionalità definita nel documento PrintCapabilities. Le istanze dell'opzione devono essere portabili e devono mantenere la finalità di stampa, in modo che la finalità possa essere comunicata quando questo PrintTicket viene assegnato a un dispositivo diverso, anche con un documento PrintCapabilities diverso scritto da un altro autore. Il vantaggio principale di questa portabilità è che se un dispositivo diverso non supporta in modo specifico un'opzione contenuta in PrintTicket, il driver di dispositivo o il sottosistema è in grado di identificare e selezionare l'opzione più vicina nella funzionalità.

Una delle principali funzioni PrintTicket del driver è identificare l'opzione del dispositivo nel documento PrintCapabilities che corrisponde maggiormente a una determinata opzione elencata in PrintTicket. Durante questo processo di assegnazione dei punteggi corrispondente o definito dal driver di  dispositivo, l'opzione in PrintTicket viene definita opzione di riferimento, mentre l'opzione nel documento PrintCapabilities viene definita opzione *candidata.* La metrica di corrispondenza generale è il numero di istanze ScoredProperty corrispondenti nelle istanze option candidate e di riferimento. un numero maggiore di corrispondenze indica in genere una migliore conservazione della finalità di stampa. Nel processo di assegnazione dei punteggi è possibile scegliere di assegnare un peso maggiore ad alcuni elementi ScoredProperty rispetto ad altri.

È possibile rendere portabili le istanze Option assicurando che tutte le istanze Option che appartengono alla stessa funzionalità presentino uno o più elementi ScoredProperty *in comune.* Ciò significa che è presente un set di elementi ScoredProperty che viene visualizzato in ogni istanza di Option (appartenente alla stessa funzionalità). Ad esempio, le istanze Option per la funzionalità PageMediaSize possono essere portabili se ogni istanza Option contiene elementi ScoredProperty che definiscono le proprietà PageMediaSize intrinseche: MediaSizeWidth e MediaSizeHeight. Il codice del driver di dispositivo o del sottosistema può quindi determinare il grado di accordo tra due istanze option confrontando le differenze in questi valori ScoredProperty. Se nel documento PrintCapabilities non è presente alcuna opzione che corrisponda esattamente a quella in PrintTicket, il driver di dispositivo può determinare e selezionare facilmente l'opzione con le dimensioni dei supporti corrispondenti più vicine.

Due oggetti (istanze option in questo caso) hanno elementi *in comune* o, in modo equivalente, hanno elementi corrispondenti, se vengono soddisfatte le tre condizioni seguenti. 

1.  I due elementi sono dello stesso tipo di elemento.

2.  Gli attributi del nome dei due elementi sono identici o nessuno dei due elementi contiene un attributo name.

3.  La catena di elementi padre degli elementi confrontati, fino ai due oggetti considerati, deve soddisfare le condizioni 1 e 2.

Si consideri ad esempio una situazione in cui sono presenti due istanze Option, in cui ognuna contiene un'istanza ScoredProperty e ognuna di queste istanze scoredProperty contiene un'istanza Property. Chiaramente, la prima condizione viene soddisfatta (le due istanze Property sono dello stesso tipo) e parte della terza condizione viene soddisfatta (gli elementi padre delle istanze Property sono dello stesso tipo, ScoredProperty, e gli elementi padre di tali elementi sono le istanze Option, che sono dello stesso tipo). Se gli attributi del nome delle istanze Property, ScoredProperty e Option sono identici o non vengono forniti, le due istanze Option hanno elementi in comune.

Il primo passaggio nella creazione di istanze Option consiste nel definire un set di elementi ScoredProperty presenti nella maggior parte o in tutte le istanze di Option. Se l'attributo di configurazione del dispositivo può essere rappresentato da una funzionalità standard (elencata nelle parole chiave dello schema di stampa), prendere nota degli elementi ScoredProperty in comune nelle istanze Option standard. È necessario assicurarsi che tutte le nuove istanze option introdotte contengano anche questi elementi ScoredProperty. È sempre possibile aggiungere altri elementi ScoredProperty in base alle esigenze per differenziare le istanze option dalle istanze Option standard. È anche possibile eliminare uno o più elementi ScoredProperty in comune se esiste un buon motivo, anche se ciò riduce la portabilità di tale opzione. Naturalmente, le considerazioni sulla portabilità suggeriscono di usare le istanze Option standard non modificati, a meno che non vi sia una differenza intrinseca tra l'opzione e l'istanza di Opzione standard che deve essere riflessa nella nuova istanza di Option.

L'esempio seguente illustra una situazione per cui è possibile aggiungere un elemento ScoredProperty a un'istanza option. Tutte le istanze Option standard per la funzionalità PageMediaSize hanno in comune gli elementi MediaSizeWidth e MediaSizeHeight ScoredProperty. Si supponga che il dispositivo sia in grado di supportare uno dei formati di supporti Letter standard alimentando la carta in modo trasversale (LongEdgeFirst) o longitudinally (ShortEdgeFirst). Supponendo che non si voglia introdurre una nuova funzionalità di direzione del feed per esporre questo grado di libertà, è invece possibile modificare le due istanze dell'opzione PageMediaSize per Letter in modo da incorporare l'orientamento del feed carta. Per queste due istanze dell'opzione Letter, iniziare con l'istanza dell'opzione PageMediaSize standard e aggiungere un nuovo elemento ScoredProperty per rappresentare FeedDirection. In un'istanza Option impostare FeedDirection ScoredProperty su LongEdgeFirst. nell'altra istanza option impostare FeedDirection su ShortEdgeFirst. Si noti che queste nuove istanze option mantengono la portabilità. Se l'opzione che rappresenta Letter, ShortEdgeFirst viene salvata in un PrintTicket e un dispositivo diverso che supporta solo l'opzione standard Letter è selezionato per eseguire il rendering del processo, il codice di corrispondenza delle opzioni può determinare rapidamente che la lettera di opzione standard è la migliore corrispondenza alla lettera di opzione, ShortEdgeFirst. Il motivo per cui questa è la corrispondenza migliore è che tutte le istanze scoredProperty sono d'accordo, ad eccezione di FeedDirection ScoredProperty, che non esiste nell'opzione standard Letter.

È anche possibile che si verifichino casi in cui le modifiche all'opzione modificano effettivamente il significato in modo tale che l'opzione modificata non può più essere considerata un caso specializzato dell'originale. In questi casi, è necessario modificare il nome dell'opzione per riflettere la differenza tra l'istanza dell'opzione modificata e quella non modificata. Solo l'autore del documento PrintCapabilities per un determinato dispositivo può decidere se l'opzione offerta dal dispositivo è sufficientemente diversa da un'istanza Option standard per giustificare una definizione incompatibile.

Si consideri ora il caso in cui il dispositivo abbia un attributo di configurazione del dispositivo che non corrisponde a nessuna delle istanze di funzionalità standard. In questo caso non è possibile fare affidamento sulle istanze Option standard per fornire l'elenco di elementi ScoredProperty in comune. Quando si crea un'istanza scoredProperty, l'obiettivo principale è distinguere ogni opzione dalle altre nella funzionalità e descrivere il motivo per cui un utente seleziona un'opzione rispetto a un'altra. La linea di base è quella di caratterizzare ogni opzione con un attributo di nome univoco e scoredProperty che contiene l'attributo name diventa quello usato per determinare gli elementi in comune.

Dopo aver stabilito un set di elementi ScoredProperty in comune, è semplice assegnare valori appropriati a ogni ScoredProperty per creare ogni opzione. Come nell'esempio precedente, per alcune istanze option potrebbe essere necessario aggiungere altre istanze scoredProperty o eliminare alcuni degli elementi in comune per creare un'istanza Option appropriata.

Si noti che lo schema di stampa richiede che il set di istanze ScoredProperty, le relative posizioni e i valori assegnati a ogni ScoredProperty in un'opzione rimangano costanti, indipendentemente dalla configurazione. L'intero concetto dello schema di stampa si basa sulle istanze Option con istanze di Proprietà fisse e identificabili e ScoredProperty condivise tra più dispositivi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



