---
title: Procedure consigliate per la gestione delle risorse
description: Questo articolo illustra le procedure consigliate per la gestione delle risorse in genere, il comportamento delle risorse gestite e non gestite e fornisce alcuni dettagli sul modo in cui le risorse vengono in genere gestite dal runtime e dai driver.
ms.assetid: 265ae0b2-f268-a4a4-551e-9d3dae886517
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27cdadb8cee3cb57f4208657054784937ecd1ea2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338438"
---
# <a name="resource-management-best-practices"></a>Procedure consigliate per la gestione delle risorse

Le trame gestite, note anche come gestione automatica delle trame, sono state rese disponibili in DirectX dalla versione 6, con diverse revisioni e miglioramenti apportati nelle versioni successive. A partire dalla versione dell'API Direct3D 9, la gestione automatica delle risorse include il supporto per le trame, i buffer dei vertici e i buffer di indice, il tutto con un'interfaccia condivisa coerente. Grazie a Direct3D Resource Manager, le applicazioni possono semplificare notevolmente la gestione delle situazioni di dispositivo smarrito e possono fare affidamento sul sistema per gestire una quantità ragionevole di risorse di memoria video.

Gli sviluppatori talvolta presentano difficoltà nell'utilizzo di risorse gestite, in parte grazie alla natura astratta del sistema. Sebbene molti scenari comuni per le risorse siano una scelta ottimale per le risorse gestite, alcuni casi offrono prestazioni migliori quando si utilizzano risorse non gestite. Questo articolo illustra le procedure consigliate per la gestione delle risorse in genere, il comportamento delle risorse gestite e non gestite e fornisce alcuni dettagli sul modo in cui le risorse vengono in genere gestite dal runtime e dai driver.

Questo articolo illustra i concetti seguenti:

-   [Memoria video](#video-memory)
-   [Risorse gestite](#managed-resources)
-   [Risorse gestite dal driver](#driver-managed-resources)
-   [Risorse predefinite](#default-resources)
    -   [Uso di risorse gestite e predefinite](#using-both-managed-and-default-resources)
    -   [Risorse predefinite dinamiche](#dynamic-default-resources)
-   [Risorse di memoria di sistema](#system-memory-resources)
-   [Raccomandazioni generali](#general-recommendations)
-   [Argomenti correlati](#related-topics)

## <a name="video-memory"></a>Memoria video

Per fare in modo che il sistema video usi una risorsa, deve trovarsi in memoria accessibile alla GPU. La memoria video locale offre le migliori prestazioni per la GPU e alcune risorse, ad esempio le destinazioni di rendering e i buffer di profondità/stencil, devono trovarsi nella memoria video locale. Con l'avvento di AGP, la GPU può anche accedere direttamente a una parte della memoria di sistema. Questa area di memoria, nota come apertura AGP, viene definita memoria video non locale e non è disponibile per altri scopi. La memoria del video non locale può essere letta e scritta dalla CPU, che in genere non ha accesso a prestazioni elevate alla memoria video locale ed è quindi ideale per l'uso come risorsa di memoria condivisa. Un aspetto fondamentale da tenere presente sulla memoria AGP è che l'it, ad esempio la memoria del video locale, viene invalidato in situazioni di dispositivo smarrito ed è necessario ripristinare gli asset permanenti.

**Figura 1. Relazione tra GPU, CPU, RAM video e RAM di sistema**

![relazione tra GPU, CPU, RAM video e RAM di sistema](images/managingresources1.gif)

Alcune soluzioni video integrate si avvaleno di un'architettura di memoria unificata (UMA), in cui la memoria principale è indirizzabile da tutti i componenti dei sistemi. Direct3D supporta UMA senza richiedere alcuna modifica all'applicazione, usando gli stessi hint delle configurazioni di memoria video locale. Per tali sistemi, le risorse sono sempre situate nella memoria di sistema e il driver è responsabile di garantire che le risorse funzionino in modo analogo a quanto avviene in un'architettura più tradizionale, sfruttando al contempo le proprietà di UMA e qualsiasi comportamento specifico dell'implementazione dell'hardware.

**Figura 2. GPU e CPU hanno accesso uguale alla RAM di sistema in un'architettura di memoria unificata**

![GPU e CPU hanno accesso uguale alla RAM di sistema in un'architettura di memoria unificata](images/managingresources2.gif)

## <a name="managed-resources"></a>Risorse gestite

La maggior parte delle risorse deve essere creata come risorse gestite nel POOL \_ gestito. Tutte le risorse verranno create nella memoria di sistema e quindi copiate in base alle esigenze nella memoria video. Le situazioni di dispositivo perso verranno gestite automaticamente dalla copia di memoria di sistema. Poiché non tutte le risorse gestite sono necessarie per rientrare nella memoria video in una sola volta, è possibile eseguire il commit della memoria in cui una memoria video più piccola working set di risorse è sufficiente per il rendering in un frame specifico. Si noti che è probabile che la maggior parte della memoria del sistema di archiviazione di backup venga rilasciata su disco nel tempo, motivo per cui l'operazione di reimpostazione può essere lenta a causa della necessità di riportare i dati in modo da ripristinare la memoria video persa.

Il runtime mantiene un timestamp per l'ultima volta che viene usata una risorsa e quando un'allocazione di memoria video non riesce a caricare una risorsa gestita necessaria, rilascia le risorse basate su questo timestamp in modo LRU. L'utilizzo di [**Sepriority**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3dresource9-setpriority) ha la precedenza sul timestamp, quindi le risorse più comunemente utilizzate devono essere impostate su un valore di priorità più alto. Direct3D 9,0 contiene informazioni limitate sulla memoria video gestita dal driver, quindi è possibile che il runtime debba rimuovere diverse risorse per creare un'area sufficientemente grande affinché l'allocazione riesca. Le priorità appropriate consentono di eliminare le situazioni in cui un elemento viene eliminato e quindi viene richiesto di nuovo poco dopo. L'applicazione può anche chiamare [**EvictManagedResources**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-evictmanagedresources) per forzare la rimozione di tutte le risorse gestite. Anche in questo caso, può trattarsi di un'operazione che richiede molto tempo per ricaricare tutte le risorse necessarie per il frame successivo, ma è molto utile per le transizioni di livello in cui il working set cambia significativamente e per la rimozione della frammentazione della memoria del video.

Viene anche mantenuto un conteggio dei frame per consentire al runtime di rilevare se la risorsa che ha appena scelto di rimuovere è stata usata prima del frame corrente, il che implica una situazione di thrashing in cui sono in uso più risorse in un singolo frame che rientrerà nella memoria video. In questo modo i criteri di sostituzione vengono attivati per passare a un tipo di file obsoleto anziché a LRU per il resto del frame, in quanto tende a offrire prestazioni leggermente migliori in tali condizioni. Questo comportamento di thrashing influirà in modo significativo sulle prestazioni di rendering. Si noti che la nozione di frame corrente è associata a [**EndScene**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-endscene), pertanto tutte le applicazioni che usano le risorse gestite devono effettuare chiamate normali a questo metodo.

Gli sviluppatori che desiderano trovare ulteriori informazioni sul comportamento delle risorse gestite nell'applicazione possono utilizzare la query di eventi RESOURCEMANAGER tramite l'interfaccia [**IDirect3DQuery9**](/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dquery9) . Questa operazione funziona solo quando si usano i runtime di debug, pertanto queste informazioni non possono dipendere dall'applicazione, ma forniscono informazioni approfondite sulle risorse gestite dal runtime.

Per comprendere il funzionamento di gestione risorse può essere utile quando si esegue l'ottimizzazione e il debug delle applicazioni, è importante non collegare eccessivamente l'applicazione ai dettagli di implementazione del runtime o dei driver correnti. Le revisioni del driver o delle modifiche apportate all'hardware possono modificare significativamente il comportamento e le versioni future di Direct3D avranno una gestione delle risorse notevolmente migliorata e sofisticata.

## <a name="driver-managed-resources"></a>Risorse Driver-Managed

I driver Direct3D sono liberi di implementare la funzionalità di trame gestite dal driver, indicata da D3DCAPS2 \_ CANMANAGERESOURCE, che consente al driver di gestire la gestione delle risorse anziché il Runtime. Per il driver (rare) che implementa questa funzionalità, il comportamento esatto del gestore di risorse del driver può variare notevolmente ed è necessario contattare il fornitore del driver per informazioni dettagliate su come funziona per la loro implementazione. In alternativa, è possibile assicurarsi che gestione runtime venga sempre utilizzato specificando D3DCREATE \_ Disabilita \_ \_ Gestione driver durante la creazione del dispositivo.

## <a name="default-resources"></a>Risorse predefinite

Sebbene le risorse gestite siano semplici, efficienti e facili da usare, in alcuni casi è preferibile usare la memoria video direttamente o anche obbligatoria. Tali risorse vengono create nella \_ categoria predefinita del pool. L'uso di tali risorse comporta ulteriori complicazioni per l'applicazione. Il codice è necessario per gestire la situazione dei dispositivi perduti per tutte le \_ risorse predefinite del pool e tenere conto delle considerazioni sulle prestazioni durante la copia dei dati. La mancata specifica dell'utilizzo \_ WRITEONLY o la creazione di una destinazione di rendering bloccabile può comportare anche gravi sanzioni in merito alle prestazioni.

La chiamata di **blocco** su una \_ risorsa predefinita del pool è più probabile che la GPU si blocchi rispetto all'utilizzo di una \_ risorsa gestita del pool, a meno che non si utilizzino determinati flag di hint. A seconda della posizione della risorsa, il puntatore restituito può essere un buffer di memoria di sistema temporaneo o un puntatore direttamente nella memoria AGP. Se si tratta di un buffer di memoria di sistema temporaneo, sarà necessario trasferire i dati alla memoria video dopo la chiamata di **sblocco** . Se la risorsa video non è di sola scrittura, i dati dovranno essere trasferiti nel buffer temporaneo durante il **blocco**. Se si tratta di un'area di memoria AGP, le copie temporanee vengono evitate, ma il comportamento della cache necessario può causare un rallentamento delle prestazioni.

È necessario prestare attenzione a scrivere una riga di dati completa della cache in qualsiasi puntatore alla memoria di apertura AGP per evitare la rigore della pettinatura di scrittura, che provoca un ciclo di lettura/scrittura e l'accesso sequenziale dell'area di memoria. Se l'applicazione deve eseguire l'accesso casuale ai dati durante la creazione e non si desidera utilizzare una risorsa gestita per il buffer, è consigliabile utilizzare una copia di memoria di sistema. Una volta creati i dati, è possibile trasmettere il risultato nella memoria della risorsa bloccata per evitare di pagare una penalità elevata per l'operazione di combinazione di scrittura nella cache.

Il \_ flag Lock overwrite può essere usato per accodare i dati in modo efficiente per alcune risorse, ma idealmente è possibile evitare più chiamate di **blocco** e **sblocco** alla stessa risorsa. L'uso corretto dei diversi flag di blocco è importante per ottenere prestazioni ottimali, in quanto usa un modello descrittivo per la cache di accesso ai dati durante il riempimento della memoria bloccata.

### <a name="using-both-managed-and-default-resources"></a>Uso di risorse gestite e predefinite

La combinazione di allocazioni di risorse predefinite gestite e di POOL \_ può causare la frammentazione della memoria video e confondere la visualizzazione del runtime della memoria video disponibile per le risorse gestite. Idealmente, è consigliabile creare tutte le \_ risorse predefinite del pool prima di utilizzare \_ le risorse gestite del pool o utilizzare la chiamata [**EvictManagedResources**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-evictmanagedresources) prima di allocare le risorse non gestite. Tenere presente che tutte le allocazioni effettuate dall' \_ impostazione predefinita del pool che si trovano nella memoria video rilegano memoria per la durata della risorsa che non è disponibile per l'uso da parte di Resource Manager o per altri scopi.

Si noti che, a differenza delle versioni precedenti di Direct3D, il runtime della versione 9 Elimina automaticamente alcune risorse gestite prima di rinunciare a un'allocazione di risorse non gestite non riuscita per la mancanza di memoria video, ma ciò può potenzialmente creare una frammentazione aggiuntiva e anche forzare una risorsa in una posizione non ottimale, ad esempio con una trama statica nella memoria video non locale. Anche in questo caso, è preferibile allocare tutte le risorse non gestite richieste prima e prima di usare le risorse gestite.

### <a name="dynamic-default-resources"></a>Risorse predefinite dinamiche

I dati generati e aggiornati con una frequenza elevata non hanno bisogno dell'archivio di backup perché tutte le informazioni verranno ricreate durante il ripristino del dispositivo. Questi dati vengono in genere creati in modo ottimale nell' \_ impostazione predefinita del pool, specificando l' \_ hint Dynamic Usage, in modo che il driver possa prendere decisioni di ottimizzazione quando si posiziona la risorsa, sapendo che verrà aggiornata spesso. Ciò significa in genere che la risorsa viene posizionata nella memoria video non locale e, di conseguenza, è in genere molto più lenta per poter accedere alla GPU rispetto alla memoria video locale. Per le architetture UMA, il driver potrebbe scegliere una posizione specifica per le risorse dinamiche da ottimizzare per l'accesso in scrittura alla CPU.

Questo utilizzo è tipico per le soluzioni di skinning software e i sistemi particellari basati su CPU che compilano i buffer di vertex/index e il flag di scarto del blocco garantirà \_ che i blocchi non vengano creati nei casi in cui la risorsa è ancora in uso dal frame precedente. In questo caso, l'utilizzo di una risorsa gestita aggiorna un buffer di memoria di sistema, che viene quindi copiato nella memoria video e quindi utilizzato solo per un frame o due prima di essere sostituito. Per i sistemi con memoria video non locale, la copia aggiuntiva viene eliminata con l'uso corretto di questo modello dinamico.

Le trame standard non possono essere bloccate e possono essere aggiornate solo tramite [**UpdateSurface**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-updatesurface) o [**UpdateTexture**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-updatetexture). Alcuni sistemi supportano le trame dinamiche, che possono essere bloccate e usano il \_ modello di scarto del blocco, ma è necessario verificare un bit delle funzionalità (D3DCAPS2 \_ DYNAMICTEXTURES) prima di usare tali risorse. Per le trame altamente dinamiche (video o procedurale), l'applicazione può creare \_ risorse di pool SYSTEMMEM predefinite e pool corrispondenti \_ e gestire gli aggiornamenti della memoria video usando **UpdateTexture**. Per gli aggiornamenti estremamente frequenti e parziali, il paradigma **UpdateTexture** è probabilmente la scelta migliore.

Per quanto possibile, è opportuno prestare attenzione quando si progettano sistemi che si basano molto sull'invio dinamico. Le risorse statiche devono essere inserite in un POOL \_ gestito per garantire un utilizzo ottimale della memoria video locale e per sfruttare in modo più efficiente il bus limitato e la larghezza di banda della memoria principale. Per le risorse semi-statiche, è possibile che il costo di un caricamento occasionale nella memoria del video locale sia molto inferiore rispetto al traffico del bus costante generato rendendoli dinamici.

## <a name="system-memory-resources"></a>Risorse di memoria di sistema

È anche possibile creare risorse nel POOL \_ SYSTEMMEM. Sebbene non possano essere usati dalla pipeline grafica, possono essere usati come origini per l'aggiornamento \_ delle risorse predefinite del pool tramite [**UpdateSurface**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-updatesurface) o [**UpdateTexture**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-updatetexture). Il comportamento di blocco è semplice, sebbene i blocchi possano verificarsi se sono utilizzati da uno dei metodi citati in precedenza.

Sebbene si trovino nella memoria di sistema, le \_ risorse SYSTEMMEM del pool sono limitate agli stessi formati e funzionalità, ad esempio le dimensioni massime, supportate dal driver di dispositivo. Il \_ tipo di risorsa Scratch del pool è un altro tipo di risorsa di memoria di sistema che può utilizzare tutti i formati e le funzionalità supportati dal runtime, ma non è possibile accedervi dal dispositivo. Le risorse Scratch sono destinate principalmente all'uso da strumenti di contenuto.

**Figura 3. Risorse di memoria in RAM video, aperture AGP e RAM di sistema**

![risorse di memoria in RAM video, aperture AGP e RAM di sistema](images/managingresources3.gif)

## <a name="general-recommendations"></a>Suggerimenti generali

Ottenere i dettagli di implementazione tecnica della gestione delle risorse corretta è molto lungo per raggiungere gli obiettivi di prestazioni per l'applicazione. Pianificare il modo in cui le risorse vengono presentate a Direct3D e la progettazione dell'architettura per ottenere i dati caricati in modo tempestivo è un'attività più complicata. Quando si prendono le decisioni seguenti per l'applicazione, è consigliabile scegliere una serie di procedure consigliate:

-   Pre-elaborare tutte le risorse. L'uso di una conversione costosa e l'ottimizzazione del tempo di caricamento per le risorse risultano utili durante lo sviluppo, ma ciò comporta un notevole carico di prestazioni nei computer degli utenti. Le risorse pre-elaborate sono più veloci da caricare, più velocemente da usare e offrono la possibilità di eseguire attività non in linea sofisticate.
-   Evitare di creare molte risorse per fotogramma. Le interazioni dei driver necessarie possono serializzare la CPU e la GPU e le operazioni implicate sono pesanti, perché spesso richiedono transizioni del kernel. Distribuire la creazione in diversi frame o riutilizzare le risorse senza crearle/rilasciarle. Idealmente, è consigliabile attendere diversi frame prima di bloccare o rilasciare le risorse usate di recente per il rendering.
-   Alla fine del frame, assicurarsi di annullare l'associazione di tutti i canali di risorse (ovvero origini di flusso, fasi della trama e indici correnti). In questo modo si garantisce la rimozione dei riferimenti in sospeso alle risorse prima che il gestore di risorse mantenga le risorse che non sono più in uso.
-   Per le trame, usare formati compressi (ad esempio, DXTn) con MIP-Maps e prendere in considerazione l'uso di un Atlante delle trame. Questi riducono notevolmente i requisiti di larghezza di banda e possono ridurre le dimensioni complessive delle risorse, rendendole così più efficienti.
-   Per la geometria, usare la geometria indicizzata, in quanto consente di comprimere le risorse del buffer dei vertici e l'hardware video moderno è altamente ottimizzato per quanto riguarda il riutilizzo dei vertici. Usando i vertex shader programmabili, è possibile comprimere le informazioni sui vertici ed espanderle durante l'elaborazione del vertice. Anche in questo caso, è possibile ridurre i requisiti di larghezza di banda e rendere più efficienti le risorse del buffer
-   Evitare di ottimizzare la gestione delle risorse. Le revisioni future di driver, hardware e il sistema operativo possono causare problemi di compatibilità se l'applicazione viene ottimizzata troppo spesso in una combinazione particolare. Poiché la maggior parte delle applicazioni è associata alla CPU, una gestione costosa basata sulla CPU causa in genere più problemi di prestazioni rispetto a quanto si risolve.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione delle risorse](/windows/desktop/direct3d9/managing-resources)
</dt> <dt>

[Dispositivi persi](/windows/desktop/direct3d9/lost-devices)
</dt> <dt>

[Ottimizzazioni delle prestazioni](/windows/desktop/direct3d9/performance-optimizations)
</dt> <dt>

[Risorse di trama compresse](/windows/desktop/direct3d9/compressed-texture-resources)
</dt> <dt>

[Query](/windows/desktop/direct3d9/queries)
</dt> <dt>

[**D3DUSAGE**](/windows/desktop/direct3d9/d3dusage)
</dt> <dt>

[**D3DPOOL**](/windows/desktop/direct3d9/d3dpool)
</dt> <dt>

[D3DCREATE](/windows/desktop/direct3d9/d3dcreate)
</dt> </dl>

 

 