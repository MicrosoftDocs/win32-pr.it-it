---
title: Glossario di Direct3D 12
description: Questi termini sono specifici di Direct3D 12.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 46B0F055-7E4F-4F8D-9915-3D195FD695B7
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a84b4b2e5a993b33b4c322b91682c8f9b5499bc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548879"
---
# <a name="direct3d-12-glossary"></a>Glossario di Direct3D 12

Questi termini sono specifici di Direct3D 12.

<dl> <dt>

<span id="direct3d12.directx_12_glossary_binding"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_BINDING"></span>**associazione**
</dt> <dd>

Processo di connessione della memoria alla pipeline grafica. L'associazione di risorse, ad esempio, implica l'associazione di una risorsa, ad esempio una trama alla pipeline, da usare per il rendering di un oggetto.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_buffer"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_BUFFER"></span>**buffer**
</dt> <dd>

Tipo di risorsa D3D che è sinonimo di un'allocazione di memoria contigua.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_bundle"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_BUNDLE"></span>**Bundle**
</dt> <dd>

Un buffer dei comandi che l'unità di elaborazione grafica (GPU) può eseguire solo direttamente tramite un *elenco di comandi diretto*. Un bundle eredita lo stato della GPU (ad eccezione dell' *oggetto stato della pipeline* attualmente impostato e della topologia primitiva).

</dd> <dt>

<span id="direct3d12.directx_12_glossary_command_allocator"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_COMMAND_ALLOCATOR"></span>**allocatore di comandi**
</dt> <dd>

Allocazioni di memoria sottostanti in cui sono archiviati i comandi della GPU. L'oggetto allocatore di comandi si applica sia agli *elenchi di comandi diretti* che ai *bundle*.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_command_list"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_COMMAND_LIST"></span>**Elenco comandi**
</dt> <dd>

Un elenco di comandi corrisponde a un set di comandi eseguiti dalla GPU. Questi includono comandi come per impostare lo stato, il progetto, la cancellazione e la copia. L'interfaccia dell'elenco di comandi D3D12 è significativamente diversa dall'interfaccia dell'elenco di comandi di D3D11. L'interfaccia dell'elenco di comandi D3D12 contiene API simili alle API per il rendering del contesto del dispositivo D3D11.

Un elenco di comandi di D3D12 non esegue il mapping delle risorse o annullare, modifica i mapping dei riquadri, ridimensiona i pool di sezioni, ottiene i dati della query e non invia mai in modo implicito comandi alla GPU per l'esecuzione.

A differenza dei contesti posticipati di D3D11, gli elenchi di comandi D3D12 supportano solo due livelli di riferimento indiretto. Un *elenco di comandi diretto* corrisponde a un buffer dei comandi che può essere eseguito dalla GPU. Un *bundle* può essere eseguito solo direttamente tramite un elenco di comandi diretto.

Un elenco di comandi diretto non eredita alcuno stato GPU. Un bundle eredita lo stato della GPU (ad eccezione dell'oggetto stato della pipeline attualmente impostato e della topologia primitiva).

La memoria per un elenco di comandi viene impostata dall' *allocatore di comandi*. Lo scopo degli elenchi di comandi è che possono essere inviati a una GPU come una singola richiesta di rendering.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_command_queue"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_COMMAND_QUEUE"></span>**coda comandi**
</dt> <dd>

Coda degli *elenchi di comandi* eseguiti dalla GPU in successione. Le applicazioni devono inviare in modo esplicito *elenchi di comandi* a una coda di comandi per l'esecuzione. Sono in genere disponibili tre code di comando: grafica 3D, calcolo e copia, corrispondenti alla pipeline grafica 3D, al motore di calcolo e a uno o più motori di copia nella GPU.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_conservative_rasterization"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_CONSERVATIVE_RASTERIZATION"></span>**rasterizzazione conservativa**
</dt> <dd>

La rasterizzazione conservativa è una modalità di funzionamento per la fase di rasterizzazione della pipeline grafica Direct3D. Consente di disabilitare la rasterizzazione basata su campione standard e di rasterizzare invece un pixel coperto da qualsiasi quantità da una primitiva. Una differenza importante è che, sebbene qualsiasi copertura produca un pixel rasterizzato, il code coverage non può essere caratterizzato dall'hardware, quindi il code coverage viene sempre visualizzato come binario per un pixel shader, ovvero completamente coperto o non coperto. Viene lasciata al codice pixel shader per determinare in modo analitico il coverage effettivo.

La rasterizzazione conservativa può essere utile per risolvere problemi di questo tipo, ad esempio collisioni e rilevamento di colpi, contenitori e abbattimento dell'occlusione, in cui il colore di un pixel è più determinato e i casi limite possono essere eliminati. Vedere [rasterizzazione conservativa](conservative-rasterization.md).

</dd> <dt>

<span id="direct3d12.directx_12_glossary_cbv"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_CBV"></span>**Constant Buffer View (CBV)**
</dt> <dd>

I buffer costanti contengono dati costanti dello shader, ad esempio una visualizzazione della fotocamera, matrici di proiezione e matrici internazionali. Una "visualizzazione buffer costante" è la visualizzazione specifica del formato del buffer, come illustrato dalla pipeline grafica.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_default_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DEFAULT_HEAP"></span>**heap predefinito**
</dt> <dd>

Heap in modalità utente che è incentrato sul supporto di tipi di risorse GPU persistenti, incluse le risorse scritte da GPU.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_descriptor"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DESCRIPTOR"></span>**descrittore**
</dt> <dd>

I descrittori sono l'unità primaria di binding per una singola risorsa in D3D12. Un descrittore è un blocco di dati relativamente piccolo che descrive completamente un oggetto alla GPU, in un formato specifico della GPU. Esistono molti tipi diversi di descrittori: le viste delle risorse dello shader (SRVs), le viste di accesso non ordinate (UAV), le viste del buffer costante (CBVs) e i Samplers sono alcuni esempi.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_descriptor_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DESCRIPTOR_HEAP"></span>**heap descrittore**
</dt> <dd>

Un heap del descrittore è una raccolta di allocazioni contigue di descrittori, un'allocazione per ogni descrittore. Il punto principale di un heap del descrittore consiste nell'includere la maggior parte dell'allocazione di memoria necessaria per archiviare le specifiche del descrittore dei tipi di oggetto a cui gli shader fanno riferimento per il maggior numero possibile di una finestra di rendering (idealmente un intero frame di rendering o più).

</dd> <dt>

<span id="direct3d12.directx_12_glossary_descriptor_table"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DESCRIPTOR_TABLE"></span>**tabella descrittori**
</dt> <dd>

Una tabella descrittore è logicamente una matrice di descrittori. Ogni tabella dei descrittori archivia i descrittori di uno o più tipi, tra cui SRVs, UAVe, CBVs e Samplers. Una tabella dei descrittori non è un'allocazione di memoria, ma è semplicemente un offset e una lunghezza in un heap descrittore.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_direct_command_list"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_DIRECT_COMMAND_LIST"></span>**Elenco comandi diretti**
</dt> <dd>

Buffer dei comandi che può essere eseguito dalla GPU. Un elenco di comandi diretto non eredita alcuno stato della GPU.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_fence"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_FENCE"></span>**limite**
</dt> <dd>

Meccanismo per sincronizzare la GPU e la CPU. Sia la GPU che la CPU possono essere istruite ad attendere una recinzione, in attesa che l'altro processore si aggiorni. Vedere [sincronizzazione multimotore](./user-mode-heap-synchronization.md).

</dd> <dt>

<span id="direct3d12.directx_12_glossary_hazard"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_HAZARD"></span>**rischio, rilevamento dei rischi**
</dt> <dd>

Un rischio si verifica quando una risorsa è stata usata per uno scopo e l'app intende riutilizzarla per un altro scopo. Per usare di nuovo la risorsa, le cache intermedie dovranno essere scaricate o invalidate, i requisiti di compressione dovranno essere coerenti con il secondo utilizzo e la risorsa deve essere nello stato richiesto per evitare la lettura della risorsa dopo che è stata scritta e invalidata per lo scopo designato.

Il processo di gestione delle risorse e di evitare questi problemi di sincronizzazione è noto come rilevamento dei rischi. Se non si verifica alcun rischio da parte del driver, l'app è responsabile di questa operazione. Nella maggior parte delle versioni precedenti di DirectX, il rilevamento dei rischi è stato gestito dal driver. Per migliorare le prestazioni, i metodi senza rilevamento dei rischi sono disponibili in DirectX 12.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_hlsl"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_HLSL"></span>**High-Level Shader Language (HLSL)**
</dt> <dd>

Linguaggio del computer, simile ma distinto in molti modi da C, usato per scrivere il codice dello shader. Gli shader vertex, pixel, Geometry, COMPUTE, Domain e Hull vengono scritti con HLSL. Un compilatore converte l'origine HLSL in un formato binario per l'utilizzo della GPU.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_multiengine"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_MULTIENGINE"></span>**multimotore**
</dt> <dd>

Istanze e tipi diversi di motori in una singola GPU. I tipi di motori includono: graphics, COMPUTE e Copy.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_multigpu"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_MULTIGPU"></span>**MultiGPU**
</dt> <dd>

Una configurazione hardware in cui è presente più di una scheda grafica. Gli adapter separati sono talvolta denominati nodi. La presenza di più GPU consente di eseguire l'operazione di sincronizzazione con la CPU e, tra loro, in modo molto più complesso rispetto a una singola GPU.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_pipeline_state_object"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_PIPELINE_STATE_OBJECT"></span>**Oggetto di stato della pipeline (PSO)**
</dt> <dd>

Parte significativa dello stato della GPU. Questo stato include tutti gli shader attualmente impostati e alcuni oggetti di stato a funzione fissa. L'unico modo per modificare gli stati contenuti nell'oggetto pipeline consiste nel modificare l'oggetto pipeline attualmente associato.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_predication"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_PREDICATION"></span>**predicazione**
</dt> <dd>

Predicazione è una funzionalità che consente alla GPU anziché alla CPU di determinare di non creare, copiare o inviare un oggetto. Se, ad esempio, un rettangolo di delimitazione di un oggetto è completamente nascosto da un altro oggetto o una prospettiva ha ridotto l'oggetto a un valore inferiore a quello di un pixel, potrebbe non essere necessario tentare di creare l'oggetto nascosto. Vedere [predicazione](predication.md).

</dd> <dt>

<span id="direct3d12.directx_12_glossary_rov"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_ROV"></span>**Visualizzazione ordine rasterizzatore (ROV)**
</dt> <dd>

Le pipeline di grafica standard possono avere problemi a comporre correttamente più trame che contengono la trasparenza. Oggetti quali recinzioni di trasmissione, fumo, incendi, vegetazione e vetro colorato usano la trasparenza per ottenere l'effetto desiderato. Si verificano problemi quando più trame che contengono la trasparenza sono allineate l'una all'altra (fumo davanti a una recinzione davanti a una costruzione di vetro che contiene la vegetazione, come esempio). Le visualizzazioni ordinate del rasterizzatore (ROV) consentono agli algoritmi OIT (Order Independent Transparency) sottostanti di usare le funzionalità dell'hardware per tentare di risolvere correttamente l'ordine di trasparenza. La trasparenza viene gestita dal pixel shader.

Le visualizzazioni ordinate del rasterizzatore (ROV) consentono pixel shader codice di contrassegnare Unordered Access View (UAV) binding con una dichiarazione che modifica i requisiti normali per l'ordine dei risultati della pipeline grafica per UAV.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_readback_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_READBACK_HEAP"></span>**heap readback**
</dt> <dd>

Heap in modalità utente focalizzato sul trasferimento dei dati dalla GPU alla CPU.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_resource"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE"></span>**risorse**
</dt> <dd>

Entità che fornisce i dati alla pipeline e definisce gli elementi di cui viene eseguito il rendering durante la scena. Le risorse possono essere caricate dal supporto del gioco o create dinamicamente in fase di esecuzione. In genere, le risorse includono i dati di trama, i dati dei vertici e gli shader. La maggior parte delle applicazioni Direct3D crea ed Elimina in modo estensivo le risorse per tutta la loro durata.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_resource_barrier"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE_BARRIER"></span>**barriera delle risorse**
</dt> <dd>

Una barriera delle risorse notifica al driver che la sincronizzazione di più accessi a una singola risorsa potrebbe essere obbligatoria, ad esempio la lettura e la scrittura nella stessa trama.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_resource_binding"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE_BINDING"></span>**associazione di risorse**
</dt> <dd>

L'associazione di risorse è il processo di collegamento delle risorse (trame, buffer dei vertici, buffer di indice e così via) alla pipeline grafica, consentendo agli shader della pipeline di elaborare la risorsa corretta.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_resource_heaps"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_RESOURCE_HEAPS"></span>**heap delle risorse**
</dt> <dd>

Heap risorse è un termine generico per gli heap che sono buffer di memoria accantonati per mantenere le risorse non appena vengono trasferiti da e verso la GPU. Un trasferimento alla GPU richiede un heap di caricamento, dalla GPU alla CPU richiede un heap readback e un heap permanente per la GPU per la manutenzione di più frame di rendering viene definito heap predefinito.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_root_signature"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_ROOT_SIGNATURE"></span>**firma radice**
</dt> <dd>

Le firme radice definiscono tutte le risorse che devono essere associate alle pipeline di calcolo o di grafica. Una firma radice viene configurata tramite l'app e collega gli elenchi di comandi alle risorse richieste dagli shader in genere, sono presenti una grafica e una firma radice di calcolo per ogni app.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_sampler"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SAMPLER"></span>**campionatore**
</dt> <dd>

Un campionatore è un codice che legge da una trama.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_srv"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SRV"></span>**Shader Resource View (SRV)**
</dt> <dd>

Modo specifico del formato per esaminare i dati in una risorsa shader, ad esempio una trama.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_static_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_STATIC_HEAP"></span>**heap statico**
</dt> <dd>

Heap in modalità utente incentrato su più risorse di sola lettura GPU che in genere vengono utilizzate contemporaneamente e non vengono modificate di frequente.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_swap_chain"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SWAP_CHAIN"></span>**Scambia catena**
</dt> <dd>

Le catene di scambio controllano la rotazione del buffer indietro, formando la base dell'animazione grafica. Le catene di scambio vengono gestite dal set di API di basso livello DXGI (vedere [Panoramica di DXGI](../direct3ddxgi/d3d10-graphics-programming-guide-dxgi.md)).

</dd> <dt>

<span id="direct3d12.directx_12_glossary_swizzle"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_SWIZZLE"></span>**swizzle**
</dt> <dd>

Una tecnica per l'individuazione dei dati multidimensionali in memoria, in modo che i dati di dimensionalità vicina tendano a disporre di indirizzi vicini. In particolare, tutti i dati di una riga non si trovano in modo contiguo prima dei dati della riga successiva. Un "swizzle con parametri" descrive un modo standardizzato per descrivere i modelli di Swizzle.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_static_texture"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_STATIC_TEXTURE"></span>**trama**
</dt> <dd>

Tipo di risorsa D3D che è multidimensionale e ha un layout di memoria ottimizzato per l'accesso multidimensionale dalla GPU. Le trame contengono spesso l'immagine non elaborata necessaria per il rendering su una superficie, prima che l'illuminazione e la fusione avvengano, ma possono contenere altre forme di dati, ad esempio sfumature di colore e colori di riferimento. Direct3D 12 supporta una, due e tre trame dimensionali.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_tile"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_TILE"></span>**piastrelle**
</dt> <dd>

Una pagina di memoria video, simile a una pagina CPU/sistema di memoria. La notazione dei riquadri consente di distinguere il sottosistema di memoria virtuale GPU dal sottosistema di memoria virtuale della CPU. Le GPU forniscono funzionalità di memoria virtuale analoghe alla memoria virtuale di sistema. Alcune GPU hanno funzionalità di memoria virtuale condivise, che consentono la condivisione di alcune pagine del sottosistema di memoria virtuale con CPU e GPU.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_tiled_resources"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_TILED_RESOURCES"></span>**risorse affiancate**
</dt> <dd>

Le risorse affiancate sono necessarie, in modo che meno memoria GPU venga sprecata per archiviare le aree di superficie che l'applicazione sa non sarà accessibile e l'hardware possa comprendere come filtrare tra i riquadri adiacenti. Le risorse affiancate sono risorse logiche di grandi dimensioni, ma richiedono piccole quantità di memoria fisica.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_uav"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_UAV"></span>**Unordered Access View (UAV)**
</dt> <dd>

Una visualizzazione di accesso non ordinato in una risorsa (che include buffer, trame e matrici di trame senza campionamento multiplo) consente l'accesso in lettura/scrittura non ordinato da più thread. Questo significa che questo tipo di risorsa può essere letto/scritto simultaneamente da più thread senza generare conflitti di memoria.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_upload_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_UPLOAD_HEAP"></span>**carica heap**
</dt> <dd>

Heap in modalità utente incentrato sul trasferimento dei dati dalla CPU alla GPU.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_user_mode_heap"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_USER_MODE_HEAP"></span>**heap in modalità utente**
</dt> <dd>

Raccolta di allocazioni di memoria grandi e contigue riciclate senza la consapevolezza di alcun componente kernel: i metodi di allocazione e distruzione non chiamano i metodi di allocazione e distruzione del kernel durante lo stato stazionario. Gli heap upload, readback e default sono varianti degli heap in modalità utente.

</dd> <dt>

<span id="direct3d12.directx_12_glossary_volume_tiled_resources"></span><span id="DIRECT3D12.DIRECTX_12_GLOSSARY_VOLUME_TILED_RESOURCES"></span>**risorse affiancate al volume**
</dt> <dd>

[Risorse affiancate](/windows)tridimensionali.

</dd> </dl>

 

 