---
title: Glossario Direct3D 12
description: Questi termini sono distintivi di Direct3D 12.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 46B0F055-7E4F-4F8D-9915-3D195FD695B7
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4a7ad8d9c925d4bd3b82a3c7dd177a58afd7f50fb82836bed56fac6a20c8f6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119496881"
---
# <a name="direct3d-12-glossary"></a>Glossario Direct3D 12

Questi termini sono distintivi di Direct3D 12.

<dl> <dt>

<span id="direct3d12.directx_12_glossary_binding"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_BINDING"></span>**Associazione**
</dt> <dd>

Processo di collegamento della memoria alla pipeline grafica. L'associazione di risorse, ad esempio, comporta l'associazione di una risorsa, ad esempio una trama alla pipeline, da usare nel rendering di un oggetto .

</dd> <dt>

<span id="direct3d12.directx_12_glossary_buffer"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_BUFFER"></span>**Buffer**
</dt> <dd>

Tipo di risorsa D3D sinonimo di un'allocazione di memoria contigua.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_bundle"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_BUNDLE"></span>**Bundle**
</dt> <dd>

Buffer dei comandi che l'unità di elaborazione grafica (GPU) può eseguire solo direttamente tramite un *elenco di comandi diretto.* Un bundle eredita tutto lo stato della GPU (ad eccezione dell'oggetto stato *della pipeline* attualmente impostato e della topologia primitiva).

</dd> <dt>

<span id="direct3d12.directx_12_glossary_command_allocator"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_COMMAND_ALLOCATOR"></span>**allocatore di comandi**
</dt> <dd>

Allocazioni di memoria sottostanti in cui vengono archiviati i comandi GPU. L'oggetto allocatore di comandi si applica *sia agli elenchi di comandi* diretti che ai *bundle*.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_command_list"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_COMMAND_LIST"></span>**elenco di comandi**
</dt> <dd>

Un elenco di comandi corrisponde a un set di comandi eseguiti dalla GPU. Questi includono comandi come per impostare lo stato, disegnare, cancellare e copiare. L'interfaccia dell'elenco di comandi D3D12 è significativamente diversa dall'interfaccia dell'elenco di comandi D3D11. L'interfaccia dell'elenco di comandi D3D12 contiene API simili alle API di rendering del contesto di dispositivo D3D11.

Un elenco di comandi D3D12 non esegue il mapping o l'annullamento del mapping delle risorse, modifica i mapping dei riquadri, ridimensiona i pool di riquadri, ottiene i dati di query e non invia mai in modo implicito comandi alla GPU per l'esecuzione.

A differenza dei contesti posticipati D3D11, gli elenchi di comandi D3D12 supportano solo due livelli di riferimento indiretto. Un *elenco di comandi diretto* corrisponde a un buffer dei comandi che la GPU può eseguire. Un *bundle* può essere eseguito solo direttamente tramite un elenco di comandi diretto.

Un elenco di comandi diretti non eredita alcuno stato GPU. Un bundle eredita tutto lo stato della GPU (ad eccezione dell'oggetto stato della pipeline attualmente impostato e della topologia primitiva).

La memoria per un elenco di comandi viene impostata *dall'allocatore di comandi*. Lo scopo degli elenchi di comandi è che possono essere inviati a una GPU come singola richiesta di rendering.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_command_queue"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_COMMAND_QUEUE"></span>**coda di comandi**
</dt> <dd>

Coda di *elenchi di comandi* che la GPU esegue in successione. Le applicazioni devono inviare in *modo esplicito gli elenchi di* comandi a una coda di comandi per l'esecuzione. In genere sono presenti tre code di comandi: grafica 3D, calcolo e copia, corrispondente alla pipeline grafica 3D, al motore di calcolo e a uno o più motori di copia, nella GPU.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_conservative_rasterization"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_CONSERVATIVE_RASTERIZATION"></span>**rasterizzazione conservativa**
</dt> <dd>

La rasterizzazione conservativa è una modalità di funzionamento per la fase di rasterizzazione della pipeline grafica Direct3D. Disabilita la rasterizzazione standard basata su campioni e rasterizza invece un pixel coperto da qualsiasi quantità da una primitiva. Una distinzione importante è che, mentre qualsiasi copertura produce un pixel rasterizzato, tale copertura non può essere caratterizzata dall'hardware, quindi la copertura appare sempre binaria per un pixel shader: completamente coperto o non coperto. Viene lasciato al codice pixel shader per determinare in modo analitico il code coverage effettivo.

La rasterizzazione conservativa può essere utile per risolvere problemi quali rilevamento di collisioni e hit, binning e occlusione, in cui il colore di un pixel è più certo e i casi di bordo possono essere eliminati. Vedere [Rasterizzazione conservativa.](conservative-rasterization.md)

</dd> <dt>

<span id="direct3d12.directx_12_glossary_cbv"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_CBV"></span>**Constant Buffer View (CBV)**
</dt> <dd>

I buffer costanti contengono dati costanti dello shader, ad esempio una visualizzazione della fotocamera, matrici di proiezione e matrici del mondo. Una "visualizzazione del buffer costante" è la visualizzazione specifica del formato del buffer, come illustrato dalla pipeline di grafica.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_default_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DEFAULT_HEAP"></span>**heap predefinito**
</dt> <dd>

Heap in modalità utente incentrato sul supporto di tipi di risorse GPU persistenti, incluse le risorse scritte in GPU.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_descriptor"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DESCRIPTOR"></span>**Descrittore**
</dt> <dd>

I descrittori sono l'unità primaria di associazione per una singola risorsa in D3D12. Un descrittore è un blocco relativamente piccolo di dati che descrive completamente un oggetto per la GPU, in un formato specifico della GPU. Esistono molti tipi diversi di descrittori: viste di risorse shader (SPV), viste di accesso non ordinate (UAV), visualizzazioni di buffer costanti (CPV) e campionatori sono alcuni esempi.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_descriptor_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DESCRIPTOR_HEAP"></span>**heap dei descrittori**
</dt> <dd>

Un heap dei descrittori è una raccolta di allocazioni contigue di descrittori, un'allocazione per ogni descrittore. Il punto principale di un heap del descrittore è includere la maggior parte dell'allocazione di memoria necessaria per archiviare le specifiche del descrittore dei tipi di oggetto a cui fanno riferimento gli shader per il maggior numero possibile di finestre di rendering (idealmente un intero frame di rendering o più).

</dd> <dt>

<span id="direct3d12.directx_12_glossary_descriptor_table"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DESCRIPTOR_TABLE"></span>**tabella dei descrittori**
</dt> <dd>

Una tabella dei descrittori è logicamente una matrice di descrittori. Ogni tabella dei descrittori archivia i descrittori di uno o più tipi, tra cui SRV, UAVe, CBV e Sampler. Una tabella del descrittore non è un'allocazione di memoria, ma semplicemente un offset e una lunghezza in un heap dei descrittori.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_direct_command_list"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DIRECT_COMMAND_LIST"></span>**elenco di comandi diretti**
</dt> <dd>

Buffer dei comandi che può essere eseguito dalla GPU. Un elenco di comandi diretti non eredita lo stato della GPU.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_fence"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_FENCE"></span>**Recinzione**
</dt> <dd>

Meccanismo per sincronizzare la GPU e la CPU. Sia la GPU che la CPU possono essere incaricate di attendere un limite, in attesa che l'altro processore recchi. Vedere [Sincronizzazione di più motori.](./user-mode-heap-synchronization.md)

</dd> <dt>

<span id="direct3d12.directx_12_glossary_hazard"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_HAZARD"></span>**hazard, hazard tracking**
</dt> <dd>

Un rischio si verifica quando una risorsa è stata usata per uno scopo e l'app intende riutilizzarla per un altro scopo. Per usare di nuovo la risorsa, sarà necessario scaricare o invalidare le cache intermedie, i requisiti di compressione dovranno essere coerenti con il secondo utilizzo e la risorsa deve essere nello stato richiesto per evitare di leggere la risorsa dopo che è stata scritta e invalidata per lo scopo previsto.

Il processo di gestione delle risorse ed evitare questi problemi di sincronizzazione è noto come rilevamento dei rischi. Se il driver non ha alcun rilevamento dei rischi, l'app ne è responsabile. Nella maggior parte delle versioni precedenti di DirectX il rilevamento dei rischi è stato gestito dal driver. Per migliorare le prestazioni, i metodi senza rilevamento dei rischi sono disponibili in DirectX 12.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_hlsl"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_HLSL"></span>**Linguaggio shader di alto livello (HLSL)**
</dt> <dd>

Linguaggio computer, simile ma distinto per molti aspetti da C, usato per scrivere codice shader. Vertex, pixel, geometry, compute, domain e hull shader vengono tutti scritti usando HLSL. Un compilatore converte l'origine HLSL in un formato binario per l'utilizzo da parte della GPU.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_multiengine"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_MULTIENGINE"></span>**multiengine**
</dt> <dd>

Le diverse istanze e tipi di motori in una singola GPU. I tipi di motori includono: grafica, calcolo e copia.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_multigpu"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_MULTIGPU"></span>**MultiGPU**
</dt> <dd>

Configurazione hardware in cui sono presenti più schede grafiche. Gli adattatori separati vengono talvolta definiti nodi. La presenza di più GPU può rendere l'attività di sincronizzazione con la CPU e tra loro molto più complessa rispetto a una singola GPU.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_pipeline_state_object"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_PIPELINE_STATE_OBJECT"></span>**Oggetto Stato pipeline (PSO)**
</dt> <dd>

Parte significativa dello stato della GPU. Questo stato include tutti gli shader attualmente impostati e alcuni oggetti di stato a funzione fissa. L'unico modo per modificare gli stati contenuti nell'oggetto pipeline è modificare l'oggetto pipeline attualmente associato.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_predication"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_PREDICATION"></span>**predicazione**
</dt> <dd>

La predicazione è una funzionalità che consente alla GPU anziché alla CPU di determinare di non disegnare, copiare o inviare un oggetto. Ad esempio, se un rettangolo di selezione di un oggetto è completamente occluso da un altro oggetto o prospettiva ha ridotto l'oggetto a dimensioni inferiori alle dimensioni di un pixel, potrebbe non essere necessario tentare di disegnare l'oggetto nascosto. Vedere [Predicazione](predication.md).

</dd> <dt>

<span id="direct3d12.directx_12_glossary_rov"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_ROV"></span>**Visualizzazione ordine rasterizzatore (ROV)**
</dt> <dd>

Le pipeline di grafica standard possono avere problemi a comporre correttamente più trame contenenti trasparenza. Per ottenere l'effetto desiderato, gli oggetti come recinti, fumi, fuoco, fiori e vetri colorati usano la trasparenza. I problemi si verificano quando più trame che contengono trasparenza sono in linea tra loro (fuma davanti a un recinto davanti a un edificio in vetro contenente piante di piante, ad esempio). Le viste ordinate del rasterizzatore consentono agli algoritmi OIT (Order Independent Transparency) sottostanti di usare le funzionalità dell'hardware per tentare di risolvere correttamente l'ordine di trasparenza. La trasparenza viene gestita dal pixel shader.

Le viste ordinate del rasterizzatore consentono al codice pixel shader di contrassegnare le associazioni Unordered Access View (UAV) con una dichiarazione che modifica i normali requisiti per l'ordine dei risultati della pipeline grafica per gli UAV.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_readback_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_READBACK_HEAP"></span>**heap di readback**
</dt> <dd>

Heap in modalità utente incentrato sul trasferimento dei dati dalla GPU alla CPU.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_resource"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE"></span>**Risorsa**
</dt> <dd>

Entità che fornisce dati alla pipeline e definisce gli elementi di cui viene eseguito il rendering durante la scena. Le risorse possono essere caricate dal supporto di gioco o create dinamicamente in fase di esecuzione. In genere, le risorse includono i dati di trama, i dati dei vertici e i dati dello shader. La maggior parte delle applicazioni Direct3D crea ed elimina le risorse in modo esteso per tutta la durata.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_resource_barrier"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE_BARRIER"></span>**barriera delle risorse**
</dt> <dd>

Una barriera di risorse notifica al driver che potrebbe essere necessaria la sincronizzazione di più accessi a una singola risorsa, ad esempio la lettura e la scrittura nella stessa trama.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_resource_binding"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE_BINDING"></span>**associazione di risorse**
</dt> <dd>

L'associazione di risorse è il processo di collegamento delle risorse (trame, buffer dei vertici, buffer di indice e così via) alla pipeline grafica, consentendo agli shader della pipeline di elaborare la risorsa corretta.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_resource_heaps"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE_HEAPS"></span>**heap delle risorse**
</dt> <dd>

Heap delle risorse è un termine generico per gli heap che sono buffer di memoria da riservare per contenere le risorse durante il trasferimento da e verso la GPU. Un trasferimento alla GPU richiede un heap Upload, dalla GPU alla CPU richiede un heap readback e un heap persistente per la GPU per la manutenzione su più fotogrammi di rendering è denominato heap predefinito.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_root_signature"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_ROOT_SIGNATURE"></span>**firma radice**
</dt> <dd>

Le firme radice definiscono tutte le risorse che devono essere associate alle pipeline grafiche o di calcolo. Una firma radice viene configurata dall'app e collega gli elenchi di comandi alle risorse richieste dagli shader. In genere, sono presenti una grafica e una firma radice di calcolo per ogni app.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_sampler"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SAMPLER"></span>**Campionatore**
</dt> <dd>

Un campionatore è il codice che legge da una trama.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_srv"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SRV"></span>**Shader Resource View (SRV)**
</dt> <dd>

Un modo specifico del formato per esaminare i dati in una risorsa shader, ad esempio una trama.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_static_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_STATIC_HEAP"></span>**heap statico**
</dt> <dd>

Heap in modalità utente incentrato su più risorse di sola lettura della GPU che vengono in genere usate contemporaneamente e non vengono modificate di frequente.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_swap_chain"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SWAP_CHAIN"></span>**catena di scambio**
</dt> <dd>

Le catene di scambio controllano la rotazione del buffer nascosto, formando la base dell'animazione grafica. Le catene di scambio vengono gestite dal set di API di basso livello DXGI (vedere [Panoramica di DXGI).](../direct3ddxgi/d3d10-graphics-programming-guide-dxgi.md)

</dd> <dt>

<span id="direct3d12.directx_12_glossary_swizzle"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SWIZZLE"></span>**Swizzle**
</dt> <dd>

Tecnica di individuazione dei dati multidimensionali in memoria in modo che i dati di dimensionalità nelle vicinanze tendono ad avere indirizzi vicini. In particolare, tutti i dati per una riga non si trovano in modo contiguo prima dei dati per la riga successiva. Un "swizzle con parametri" descrive un modo standardizzato per descrivere i modelli di swizzle.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_static_texture"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_STATIC_TEXTURE"></span>**Texture**
</dt> <dd>

Tipo di risorsa D3D multidimensionale con layout di memoria ottimizzato per l'accesso multidimensionale dalla GPU. Le trame contengono spesso l'immagine non elaborata necessaria per il rendering su una superficie, prima dell'esecuzione dell'illuminazione e della fusione, ma possono contenere altre forme di dati, ad esempio sfumature di colore e colori di riferimento. Direct3D 12 supporta trame una, due e tridimensionali.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_tile"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_TILE"></span>**Piastrelle**
</dt> <dd>

Una pagina di memoria video, simile a una pagina di memoria cpu/sistema. La notazione del riquadro consente di distinguere il sottosistema di memoria virtuale GPU dal sottosistema di memoria virtuale della CPU. Le GPU offrono funzionalità di memoria virtuale simili a quelle della memoria virtuale di sistema. Alcune GPU hanno funzionalità di memoria virtuale condivise, che consentono la condivisione di alcune pagine del sottosistema di memoria virtuale con CPU e GPU.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_tiled_resources"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_TILED_RESOURCES"></span>**risorse affiancate**
</dt> <dd>

Le risorse affiancate sono necessarie in modo da sprecare meno memoria GPU archiviando aree di superfici che l'applicazione sa non sarà accessibile e l'hardware è in grado di comprendere come filtrare tra riquadri adiacenti. Le risorse affiancate sono risorse logiche di grandi dimensioni, ma richiedono piccole quantità di memoria fisica.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_uav"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_UAV"></span>**Unordered Access View (UAV)**
</dt> <dd>

Una visualizzazione di accesso non ordinato in una risorsa (che include buffer, trame e matrici di trame, senza campionamento multiplo), consente l'accesso in lettura/scrittura non ordinato a livello temporale da più thread. Ciò significa che questo tipo di risorsa può essere letto/scritto contemporaneamente da più thread senza generare conflitti di memoria.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_upload_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_UPLOAD_HEAP"></span>**caricare l'heap**
</dt> <dd>

Heap in modalità utente incentrato sul trasferimento dei dati dalla CPU alla GPU.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_user_mode_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_USER_MODE_HEAP"></span>**heap in modalità utente**
</dt> <dd>

Raccolta di allocazioni di memoria contigue di grandi dimensioni che vengono riciclate senza la consapevolezza di alcun componente del kernel: i metodi di allocazione e distruzione non chiamano metodi di allocazione e distruzione del kernel durante lo stato stabile. Upload, Readback e Heap predefiniti sono varianti degli heap in modalità utente.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_volume_tiled_resources"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_VOLUME_TILED_RESOURCES"></span>**risorse affiancate del volume**
</dt> <dd>

Risorse [affiancate tridimensionali.](/windows)

</dd> </dl>

 

 