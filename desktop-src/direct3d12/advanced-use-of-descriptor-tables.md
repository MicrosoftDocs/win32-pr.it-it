---
title: Uso avanzato di tabelle di descrittori
description: Nelle sezioni seguenti vengono fornite informazioni sull'utilizzo avanzato delle tabelle dei descrittori.
ms.assetid: BB0CA29C-65CB-48B1-8351-EE13CC470B54
ms.date: 05/31/2018
ms.localizationpriority: high
ms.topic: article
ms.openlocfilehash: 79dad6914cff07726c2d40ed2ee27cccb6a0cf1e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104925"
---
# <a name="advanced-use-of-descriptor-tables"></a>Uso avanzato di tabelle di descrittori

Nelle sezioni seguenti vengono fornite informazioni sull'utilizzo avanzato delle tabelle dei descrittori.

-   [Modifica delle voci della tabella descrittore tra chiamate di rendering](#changing-descriptor-table-entries-between-rendering-calls)
-   [Indicizzazione fuori limite](#out-of-bounds-indexing)
-   [Derivati dello shader e indicizzazione divergente](#shader-derivatives-and-divergent-indexing)
-   [Argomenti correlati](#related-topics)

## <a name="changing-descriptor-table-entries-between-rendering-calls"></a>Modifica delle voci della tabella descrittore tra chiamate di rendering

Dopo che gli elenchi di comandi che consentono di impostare le tabelle dei descrittori sono stati inviati a una coda per l'esecuzione, l'applicazione non deve modificare dalla CPU le parti degli heap del descrittore a cui può fare riferimento la GPU fino a quando l'applicazione non è in grado di utilizzare i riferimenti.

Il completamento del lavoro può essere determinato a una stretta associazione usando le schermate dell'API per tenere traccia dello stato di avanzamento della GPU o meccanismi più grossolani, ad esempio in attesa di osservare che il rendering è stato inviato a display, a prescindere dall'applicazione. Se un'applicazione sa che verrà eseguito l'accesso solo a un subset dell'area a cui punta una tabella del descrittore (ad indicare che il controllo di flusso è nello shader), gli altri descrittori privi di riferimenti possono comunque essere modificati. Se un'applicazione deve passare tra diverse tabelle dei descrittori tra le chiamate di rendering, è possibile scegliere tra alcuni approcci:

-   Controllo delle versioni delle tabelle dei descrittori: creare o riutilizzare una tabella descrittore separata per ogni raccolta univoca di descrittori a cui fa riferimento un elenco di comandi. Quando si modificano e si riutilizzano aree popolate in precedenza negli heap dei descrittori, le applicazioni devono innanzitutto assicurarsi che la GPU abbia terminato di utilizzare una parte di un heap dei descrittori che verrà riciclata.
-   Indicizzazione dinamica: le applicazioni possono disporre gli oggetti che variano in base a un oggetto di estrazione (o addirittura variare all'interno di un progetto) in un intervallo di un heap dei descrittori, definire una tabella dei descrittori che si estende a tutti gli oggetti e dallo shader, usare l'indicizzazione dinamica della tabella durante l'esecuzione dello shader per selezionare l'oggetto da usare.
-   Inserimento diretto dei descrittori nella firma radice. In questo modo è possibile gestire solo un numero molto ridotto di descrittori perché lo spazio della firma radice è limitato.

L'implicazione dell'uso del controllo delle versioni della tabella descrittore è che la memoria del descrittore fuori da un heap dei descrittori deve essere bruciata per ogni set univoco di descrittori a cui fa riferimento la pipeline grafica per ogni elenco di comandi che potrebbe essere in esecuzione, accodato per l'esecuzione o registrato in un determinato momento.

D3D12 lascia la responsabilità di gestire il controllo delle versioni all'applicazione per i tipi di oggetto gestiti tramite gli heap dei descrittori e le tabelle descrittore. Un vantaggio è che le applicazioni possono scegliere di riutilizzare il contenuto della tabella descrittore quanto più possibile anziché definire sempre una nuova versione della tabella dei descrittori per ogni invio dell'elenco dei comandi. La firma radice è uno spazio in cui il driver D3D12 è automaticamente in versione.

La possibilità di associare più tabelle dei descrittori alla firma radice (e quindi alla pipeline) per volta consente alle applicazioni di raggruppare e comportare set di riferimenti a descrittori a frequenze diverse, se lo si desidera. Ad esempio, un'applicazione può usare un numero ridotto (forse solo uno) di tabelle descrittori statiche di grandi dimensioni che cambiano raramente o in quali aree della memoria heap del descrittore sottostante vengono popolate in base alle esigenze, con l'uso dell'indicizzazione dinamica dello shader per selezionare le trame. Allo stesso tempo, l'applicazione potrebbe mantenere un'altra classe di risorse in cui il set a cui viene fatto riferimento da ogni chiamata di progetto viene passato dalla CPU utilizzando la tecnica di controllo delle versioni delle tabelle dei descrittori.

## <a name="out-of-bounds-indexing"></a>Indicizzazione fuori limite

L'indicizzazione fuori limite di qualsiasi tabella dei descrittori dello shader produce un accesso di memoria non definito in gran parte, inclusa la possibilità di leggere una memoria arbitraria in-process come se si trattasse di un descrittore di stato hardware e di vivere con la conseguenza dell'operazione eseguita dall'hardware. Questo potrebbe produrre una reimpostazione del dispositivo, ma non arresterà l'arresto anomalo di Windows.

## <a name="shader-derivatives-and-divergent-indexing"></a>Derivati dello shader e indicizzazione divergente

Se pixel shader chiamate che sono in esecuzione in un timbro 2x2 (per supportare calcoli derivati), scegliere diversi indici di trama da campionare da una tabella descrittore, se la configurazione e la trama del campionatore selezionato per un determinato pixel richiedono un calcolo LOD da derivati da coordinate di trama, il calcolo del LOD e il processo di campionamento della trama vengono eseguiti dall'hardware indipendentemente per ogni ricerca di trama nell'indicatore 2x2 , che avrà un effetto sulle prestazioni.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tabelle descrittore](descriptor-tables.md)
</dt> </dl>

 

 




