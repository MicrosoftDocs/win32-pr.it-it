---
title: Uso avanzato delle tabelle di descrizione
description: Le sezioni seguenti forniscono informazioni sull'uso avanzato delle tabelle dei descrittori.
ms.assetid: BB0CA29C-65CB-48B1-8351-EE13CC470B54
ms.date: 05/31/2018
ms.localizationpriority: high
ms.topic: article
ms.openlocfilehash: 044c02b87591f7ad53212ce37d7549ade68308a648092a260a67c97395959c98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119632591"
---
# <a name="advanced-use-of-descriptor-tables"></a>Uso avanzato delle tabelle di descrizione

Le sezioni seguenti forniscono informazioni sull'uso avanzato delle tabelle dei descrittori.

-   [Modifica delle voci della tabella dei descrittori tra chiamate di rendering](#changing-descriptor-table-entries-between-rendering-calls)
-   [Indicizzazione fuori limiti](#out-of-bounds-indexing)
-   [Derivati dello shader e indicizzazione divergente](#shader-derivatives-and-divergent-indexing)
-   [Argomenti correlati](#related-topics)

## <a name="changing-descriptor-table-entries-between-rendering-calls"></a>Modifica delle voci della tabella dei descrittori tra chiamate di rendering

Dopo che gli elenchi di comandi che impostano tabelle di descrittori sono stati inviati a una coda per l'esecuzione, l'applicazione non deve modificare dalla CPU le parti di heap dei descrittori a cui la GPU potrebbe fare riferimento fino a quando l'applicazione non sa che la GPU ha terminato di usare i riferimenti.

Il completamento del lavoro può essere determinato a un limite ristretto usando i limiti api per tenere traccia dello stato della GPU o meccanismi più grossosi, ad esempio l'attesa di vedere che il rendering è stato inviato per la visualizzazione, in base alle esigenze dell'applicazione. Se un'applicazione sa che è possibile accedere solo a un subset dell'area a cui punta una tabella di descrittori (ad esempio a causa del controllo di flusso nello shader), gli altri descrittori senza riferimenti sono ancora liberi di essere modificati. Se un'applicazione deve passare da una tabella di descrizione all'altra tra le chiamate di rendering, esistono alcuni approcci tra cui l'applicazione può scegliere:

-   Controllo delle versioni della tabella dei descrittori: creare (o riutilizzare) una tabella di descrittori separata per ogni raccolta univoca di descrittori a cui deve fare riferimento un elenco di comandi. Quando si modificano e si riutilizzano aree popolate in precedenza negli heap dei descrittori, le applicazioni devono prima assicurarsi che la GPU abbia terminato l'uso di qualsiasi parte di un heap descrittore che verrà riciclata.
-   Indicizzazione dinamica: le applicazioni possono disporre gli oggetti che variano tra le operazioni di disegno/invio (o anche all'interno di un disegno) in un intervallo di un heap descrittore, definire una tabella di descrittori che si estende su tutti gli oggetti e, a partire dallo shader, usare l'indicizzazione dinamica della tabella durante l'esecuzione dello shader per selezionare l'oggetto da usare.
-   Inserimento diretto dei descrittori nella firma radice. In questo modo è possibile gestire solo un numero molto ridotto di descrittori perché lo spazio della firma radice è limitato.

L'implicazione dell'uso del controllo delle versioni della tabella dei descrittori è che la memoria dei descrittori all'uscita da un heap dei descrittori deve essere corretta per ogni set univoco di descrittori a cui fa riferimento la pipeline grafica per ogni elenco di comandi che può essere in esecuzione, accodato per l'esecuzione o registrato in un determinato momento.

D3D12 lascia all'applicazione la responsabilità di gestire il controllo delle versioni per i tipi di oggetto gestiti tramite gli heap dei descrittori e le tabelle dei descrittori. Uno dei vantaggi è che le applicazioni possono scegliere di riutilizzare il più possibile il contenuto della tabella dei descrittori anziché definire sempre una nuova versione della tabella dei descrittori per ogni invio dell'elenco di comandi. La firma radice è uno spazio che il driver D3D12 versioni automaticamente.

La possibilità di associare più tabelle di descrittori alla firma radice (e quindi alla pipeline) alla volta consente alle applicazioni di raggruppare e cambiare set di riferimenti ai descrittori a frequenze diverse, se necessario. Ad esempio, un'applicazione potrebbe usare un numero ridotto (forse solo uno) di tabelle di descrittori statici di grandi dimensioni che cambiano raramente o in cui le aree nella memoria heap del descrittore sottostante vengono popolate in base alle esigenze, con l'uso dell'indicizzazione dinamica dallo shader per selezionare le trame. Allo stesso tempo, l'applicazione potrebbe mantenere un'altra classe di risorse in cui il set a cui fa riferimento ogni chiamata di disegno viene commutato dalla CPU usando la tecnica di controllo delle versioni della tabella dei descrittori.

## <a name="out-of-bounds-indexing"></a>Indicizzazione fuori limiti

L'indicizzazione fuori dai limiti di qualsiasi tabella di descrittori dello shader comporta un accesso alla memoria in gran parte indefinito, inclusa la possibilità di leggere la memoria arbitraria in-process come se fosse un descrittore di stato hardware e di conviversi con la conseguenza di ciò che fa l'hardware. Questo potrebbe produrre una reimpostazione del dispositivo, ma non si arresterà in modo anomalo Windows.

## <a name="shader-derivatives-and-divergent-indexing"></a>Derivati dello shader e indicizzazione divergente

Se le chiamate pixel shader in esecuzione in uno stamp 2x2 (per supportare i calcoli derivati) scelgono indici di trama diversi da campionare da una tabella di descrittori e se la configurazione e la trama del campionatore selezionate per un determinato pixel richiedono un calcolo LOD dai derivati delle coordinate di trama, il processo di calcolo e campionamento delle trame loD viene eseguito dall'hardware in modo indipendente per ogni ricerca di trama nello stamp 2x2,  che inciderà sulle prestazioni.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tabelle dei descrittori](descriptor-tables.md)
</dt> </dl>

 

 




