---
title: Panoramica dell'associazione di risorse
description: La chiave per l'associazione di risorse in DirectX 12 è costituita dai concetti di un descrittore, tabelle di descrittore, heap di descrittori e una firma radice.
ms.assetid: 92E100CA-822D-46B1-BD37-FF57C3FB703D
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bc7e78255c123777716eddb43d9443e19113b34
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104647"
---
# <a name="resource-binding-overview"></a>Panoramica dell'associazione di risorse

La chiave per l'associazione di risorse in DirectX 12 è costituita dai concetti di un *descrittore*, *tabelle di descrittore*, *heap di descrittori* e una *firma radice*.

-   [Risorse e pipeline grafica](#resources-and-the-graphics-pipeline)
-   [Tipi di risorse e viste](#resource-types-and-views)
-   [Flusso di associazione di risorse del controllo](#resource-binding-overview)
-   [Sottoallocazione](#suballocation)
-   [Liberare risorse](#freeing-resources)
-   [Argomenti correlati](#related-topics)

## <a name="resources-and-the-graphics-pipeline"></a>Risorse e pipeline grafica

Le risorse dello shader, ad esempio le trame, le tabelle costanti, le immagini, i buffer e così via, non sono associate direttamente alla pipeline dello shader. al contrario, viene fatto riferimento tramite un *descrittore*. Un descrittore è un piccolo oggetto che contiene informazioni su una risorsa.

I descrittori sono raggruppati in *tabelle di descrittori* di form. Ogni tabella descrittore archivia informazioni su un intervallo di tipi di risorse. Sono disponibili molti tipi diversi di risorse. Le risorse più comuni sono:

-   Viste del buffer costante (CBVs)
-   Viste di accesso non ordinate (UAV)
-   Viste risorse shader (SRVs)
-   Campionatori

I descrittori SRV, UAV e CBVs possono essere combinati nella stessa tabella descrittore.

Le pipeline di calcolo e di grafica ottengono l'accesso alle risorse facendo riferimento alle tabelle del descrittore in base all'indice.

Le tabelle descrittore vengono archiviate in un *heap del descrittore*. Gli heap descrittore conterranno idealmente tutti i descrittori (nelle tabelle dei descrittori) per uno o più frame di cui eseguire il rendering. Tutte le risorse verranno archiviate in heap in modalità utente.

Un altro concetto è quello di una *firma radice*. La firma radice è una convenzione di associazione, definita dall'applicazione, che viene utilizzata dagli shader per individuare le risorse a cui è necessario accedere. La firma radice può archiviare:

-   Indici per le tabelle dei descrittori in un heap del descrittore, in cui il layout della tabella descrittore è già stato definito.
-   Le costanti, in modo che le app possano associare le costanti definite dall'utente (note come *costanti radice*) direttamente agli shader senza dover passare attraverso i descrittori e le tabelle dei descrittori.
-   Numero molto ridotto di descrittori direttamente all'interno della firma radice, ad esempio una visualizzazione del buffer costante (CBV) che cambia per ogni estrazione, evitando così che l'applicazione debba inserire i descrittori in un heap dei descrittori.

In altre parole, la firma radice fornisce le ottimizzazioni delle prestazioni appropriate per piccole quantità di dati che cambiano per ogni progetto.

Il progetto Direct3D 12 per l'associazione lo separa da altre attività, ad esempio la gestione della memoria, la gestione della durata degli oggetti, il rilevamento dello stato e la sincronizzazione della memoria (vedere [le differenze nel modello di associazione da Direct3D 11](binding-model.md)). Il binding Direct3D 12 è progettato per un sovraccarico ridotto e ottimizzato per le chiamate API eseguite con maggiore frequenza. Inoltre, è scalabile per l'hardware di fascia bassa fino a un livello superiore e scalabile dalle versioni precedenti (la pipeline Direct3D 11 più lineare) agli approcci più recenti (più paralleli) alla programmazione del motore di grafica.

## <a name="resource-types-and-views"></a>Tipi di risorse e viste

I tipi di risorsa corrispondono a Direct3D 11, ovvero:

-   Texture1D e Texture1DArray
-   Texture2D, Texture2DArray, Texture2DMS, Texture2DMSArray
-   Texture3D
-   Buffer (tipizzati, strutturati e non elaborati)

Le visualizzazioni delle risorse sono simili, ma leggermente diverse dalle visualizzazioni Direct3D 11, vertex e index buffer sono state aggiunte.

-   Constant Buffer View (CBV)
-   Visualizzazione accessi non ordinati (UAV)
-   Visualizzazione risorse shader (SRV)
-   Campionatori
-   Visualizzazione destinazione rendering (RTV)
-   Visualizzazione stencil profondità (DSV)
-   Visualizzazione buffer indice (IBV)
-   Visualizzazione buffer dei vertici (VBV)
-   Visualizzazione output flusso (SOV)

Solo le prime quattro visualizzazioni sono effettivamente visibili agli shader, fanno riferimento a heap del [descrittore visibile dello shader](shader-visible-descriptor-heaps.md) e [heap dei descrittori non shader visibili](non-shader-visible-descriptor-heaps.md).

## <a name="resource-binding-flow-of-control"></a>Flusso di associazione di risorse del controllo

Concentrandosi solo sulle firme radice, i descrittori radice, le costanti radice, le tabelle dei descrittori e gli heap dei descrittori, il flusso della logica di rendering per un'app dovrebbe essere simile al seguente:

-   Creare uno o più oggetti firma radice, uno per ogni diversa configurazione di binding necessaria per un'applicazione.
-   Creare shader e lo stato della pipeline con gli oggetti firma radice con cui verranno utilizzati.
-   Crearne uno (o, se necessario, più) heap dei descrittori che conterranno tutti i descrittori SRV, UAV e CBV per ogni frame di rendering.
-   Inizializzare gli heap dei descrittori con i descrittori laddove possibile per i set di descrittori che verranno riutilizzati in molti frame.
-   Per ogni fotogramma di cui eseguire il rendering:
    -   Per ogni elenco di comandi:
        -   Impostare la firma radice corrente da usare e modificare se necessario durante il rendering, che è raramente necessario.
        -   Aggiornare le costanti della firma radice e/o i descrittori di firma radice per la nuova vista, ad esempio le proiezioni del mondo/visualizzazione.
        -   Per ogni elemento da creare:
            -   Definire tutti i nuovi descrittori negli heap del descrittore in base alle esigenze per il rendering per oggetto. Per gli heap dei descrittori visibili allo shader, l'app deve assicurarsi di usare lo spazio dell'heap dei descrittori a cui non è già stato fatto riferimento mediante il rendering che potrebbe essere in corso, ad esempio l'allocazione lineare dello spazio attraverso l'heap del descrittore durante il rendering.
            -   Aggiornare la firma radice con i puntatori alle aree richieste degli heap del descrittore. Una tabella dei descrittori, ad esempio, può puntare ad alcuni descrittori statici (non modificabili) inizializzati in precedenza, mentre un'altra tabella descrittore può puntare ad alcuni descrittori dinamici configurati per il rendering corrente.
            -   Aggiornare alcune costanti della firma radice e/o descrittori di firma radice per il rendering per singolo elemento.
            -   Impostare lo stato della pipeline per l'elemento da creare (solo se è necessario modificare), compatibile con la firma radice attualmente associata.
            -   Disegna
        -   Repeat (elemento successivo)
    -   Repeat (elenco dei comandi successivi)
    -   In modo rigoroso al termine della GPU con la memoria che non verrà più usata, è possibile rilasciarla. I riferimenti ai descrittori non devono essere eliminati se il rendering aggiuntivo che usa tali descrittori non viene inviato. Il rendering successivo può quindi puntare ad altre aree negli heap del descrittore oppure è possibile sovrascrivere i descrittori non aggiornati con descrittori validi per riutilizzare lo spazio dell'heap del descrittore.
-   Ripeti (fotogramma successivo)

Si noti che altri tipi di descrittori, visualizzazioni di destinazione di rendering (RTVs), viste depth stencil (DSV), viste buffer index (IBVs), viste buffer vertex (VBVs) e visualizzazioni di oggetti shader (SOV) vengono gestiti in modo diverso. Il driver gestisce il controllo delle versioni del set di descrittori associato per ogni progetto durante la registrazione dell'elenco dei comandi (in modo analogo a come le associazioni della firma radice vengono sottoposte a controllo delle versioni dal driver o dall'hardware). Questa operazione è diversa dal contenuto degli heap dei descrittori visibili dello shader, per i quali l'applicazione deve essere allocata manualmente attraverso l'heap, perché fa riferimento a descrittori diversi tra le estrazioni. Il controllo delle versioni del contenuto dell'heap che è visibile allo shader viene lasciato all'applicazione perché consente alle applicazioni di eseguire operazioni come il riutilizzo dei descrittori che non cambiano. in alternativa, usare set statici di grandi dimensioni di descrittori e usare l'indicizzazione dello shader, ad esempio l'ID del materiale, per selezionare i descrittori da usare dall'heap del descrittore o usare combinazioni di tecniche per diversi set di descrittori. L'hardware non è equipaggiato per gestire questo tipo di flessibilità per gli altri tipi di descrittori (RTV, DSV, IBV, VBV, SOV).

## <a name="suballocation"></a>Sottoallocazione

In Direct3D 12, l'app dispone di un controllo di basso livello sulla gestione della memoria. Nelle versioni precedenti di Direct3D, incluso Direct3D 11, esiste un'allocazione per ogni risorsa. In Direct3D 12, l'app può usare l'API per allocare un blocco di memoria di grandi dimensioni, più grande di qualsiasi singolo oggetto necessario. Al termine dell'operazione, l'app può creare descrittori per puntare a sezioni del blocco di memoria di grandi dimensioni. Questo processo di decidere cosa inserire dove (blocchi più piccoli all'interno del blocco di grandi dimensioni) è noto come *allocazione*. Per consentire all'app di eseguire questa operazione, è possibile ottenere miglioramenti in termini di utilizzo efficiente di calcolo e memoria. Ad esempio, la ridenominazione delle risorse viene resa obsoleta. Al posto di questo, le app possono usare le recinzioni per determinare quando viene usata una determinata risorsa e quando non si esegue la schermatura nelle esecuzioni dell'elenco di comandi in cui l'elenco dei comandi richiede l'uso di quella particolare risorsa.

## <a name="freeing-resources"></a>Liberare risorse

Prima di poter liberare la memoria associata alla pipeline, è necessario che la GPU sia terminata.

L'attesa del rendering del frame è probabilmente il modo più grossolano per assicurarsi che la GPU sia stata completata. A un livello più preciso, è possibile usare di nuovo le schermate, quando un comando viene registrato in un elenco di comandi di cui si vuole tenere traccia del completamento, inserire un limite immediatamente dopo. Quindi, è possibile eseguire diverse operazioni di sincronizzazione con la barriera. Si invia un nuovo lavoro (elenchi di comandi) che attende fino a quando non viene passato un limite specificato sulla GPU, che indica il completamento di tutti gli elementi prima che siano completati, oppure è possibile richiedere che venga generato un evento della CPU quando il limite viene superato (che l'app può attendere con un thread in sospensione). In Direct3D 11, era `EnqueueSetEvent` ().

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Associazione di risorse](resource-binding.md)
</dt> </dl>

 

 




