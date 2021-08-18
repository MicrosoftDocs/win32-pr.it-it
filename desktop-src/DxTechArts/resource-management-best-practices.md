---
title: Procedure consigliate per la gestione delle risorse
description: Questo articolo illustra le procedure consigliate per gestire le risorse in generale, il comportamento delle risorse gestite e non gestite e fornisce alcuni dettagli sul modo in cui le risorse vengono in genere gestite dal runtime e dai driver.
ms.assetid: 265ae0b2-f268-a4a4-551e-9d3dae886517
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bacf57c33ef765596ffa660ba884708ee000dd370c90edd3fcd158a9c526a7ac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119213243"
---
# <a name="resource-management-best-practices"></a>Procedure consigliate per la gestione delle risorse

Le trame gestite, note anche come gestione automatica delle trame, sono disponibili in DirectX a partire dalla versione 6, con diverse revisioni e miglioramenti apportati nelle versioni successive. Al rilascio dell'API Direct3D 9, la gestione automatica delle risorse include il supporto per trame, buffer dei vertici e buffer di indice, il tutto con un'interfaccia condivisa coerente. Usando Direct3D Resource Manager, le applicazioni possono semplificare notevolmente la gestione delle situazioni di perdita dei dispositivi e possono basarsi sul sistema per gestire una quantità ragionevole di risorse di memoria video troppo grandi.

A volte gli sviluppatori hanno difficoltà a usare le risorse gestite, in parte a causa della natura astratta del sistema. Sebbene molti scenari comuni per le risorse siano adatti per le risorse gestite, in alcuni casi le prestazioni sono migliori quando si usano risorse non gestite. Questo articolo illustra le procedure consigliate per gestire le risorse in generale, il comportamento delle risorse gestite e non gestite e fornisce alcuni dettagli sul modo in cui le risorse vengono in genere gestite dal runtime e dai driver.

Questo articolo illustra questi concetti:

-   [Memoria video](#video-memory)
-   [Risorse gestite](#managed-resources)
-   [Risorse gestite dal driver](#driver-managed-resources)
-   [Risorse predefinite](#default-resources)
    -   [Uso di risorse gestite e predefinite](#using-both-managed-and-default-resources)
    -   [Risorse predefinite dinamiche](#dynamic-default-resources)
-   [Risorse di memoria di sistema](#system-memory-resources)
-   [Informazioni Consigli](#general-recommendations)
-   [Argomenti correlati](#related-topics)

## <a name="video-memory"></a>Memoria video

Perché il sistema video usi una risorsa, deve trovarsi in memoria accessibile alla GPU. La memoria video locale offre le migliori prestazioni per la GPU e alcune risorse, ad esempio destinazioni di rendering e buffer di profondità/stencil, devono trovarsi nella memoria video locale. Con l'avvento di AGP, la GPU può anche accedere direttamente a una parte della memoria di sistema. Quest'area di memoria, nota come aperture AGP, viene definita memoria video non locale e non è disponibile per altri scopi. La memoria video non locale può essere letta e scritta dalla CPU, che in genere non ha accesso ad alte prestazioni alla memoria video locale ed è quindi ideale per l'uso come risorsa di memoria condivisa. Un aspetto importante da ricordare sulla memoria AGP è che, come la memoria video locale, viene invalidata in situazioni di dispositivo perso e gli asset persistenti presenti in tale posizione devono essere ripristinati.

**Figura 1. Relazione tra GPU, CPU, RAM video e RAM di sistema**

![relazione tra GPU, CPU, RAM video e RAM di sistema](images/managingresources1.gif)

Alcune soluzioni video integrate usano un'architettura UMA (Unified Memory Architecture), in cui la memoria principale è indirizzabile da tutti i componenti dei sistemi. Direct3D supporta UMA senza richiedere alcuna modifica all'applicazione, utilizzando gli stessi suggerimenti delle configurazioni della memoria video locale. Per questi sistemi, le risorse si trovano sempre nella memoria di sistema e il driver è responsabile di garantire che le risorse funzionino in modo molto simile a un'architettura più tradizionale sfruttando al tempo stesso le proprietà di UMA e qualsiasi comportamento specifico dell'implementazione hardware.

**Figura 2. GPU e CPU hanno lo stesso accesso alla RAM di sistema in un'architettura di memoria unificata**

![Gpu e CPU hanno lo stesso accesso alla RAM di sistema in un'architettura di memoria unificata](images/managingresources2.gif)

## <a name="managed-resources"></a>Risorse gestite

La maggior parte delle risorse deve essere creata come risorse gestite in POOL \_ MANAGED. Tutte le risorse verranno create nella memoria di sistema e quindi copiate in base alle esigenze nella memoria video. Le situazioni di dispositivo perso verranno gestite automaticamente dalla copia della memoria di sistema. Poiché non tutte le risorse gestite sono necessarie per la memoria video in una sola volta, è possibile eseguire un over-commit della memoria in cui un working set di risorse di memoria video più piccolo è tutto ciò che è necessario per eseguire il rendering in qualsiasi fotogramma specifico. Si noti che è probabile che la maggior parte di questa memoria di sistema dell'archivio di backup verrà paginata su disco nel corso del tempo, motivo per cui l'operazione di reimpostazione può essere lenta a causa della necessità di reinserire i dati in pagine per ripristinare la memoria video persa.

Il runtime mantiene un timestamp per l'ultima volta che viene usata una risorsa e, quando un'allocazione di memoria video non riesce per il caricamento di una risorsa gestita necessaria, rilascerà le risorse in base a questo timestamp in modalità LRU. [**L'utilizzo di SetPriority**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3dresource9-setpriority) ha la precedenza sul timestamp, quindi le risorse usate più di frequente devono essere impostate su un valore di priorità più alto. Direct3D 9.0 dispone di informazioni limitate sulla memoria video gestita dal driver, quindi il runtime potrebbe dover eviti diverse risorse per creare un'area sufficientemente grande perché l'allocazione abbia esito positivo. Le priorità appropriate possono aiutare a eliminare le situazioni in cui un elemento viene eliminato e quindi richiesto di nuovo poco dopo. L'applicazione può anche [**chiamare EvictManagedResources**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-evictmanagedresources) per forzare la rimozione di tutte le risorse gestite. Anche in questo caso, questa operazione può richiedere molto tempo per ricaricare tutte le risorse necessarie per il fotogramma successivo, ma è molto utile per le transizioni di livello in cui il working set cambia in modo significativo e per rimuovere la frammentazione della memoria video.

Viene inoltre mantenuto un conteggio dei fotogrammi per consentire al runtime di rilevare se la risorsa che si è appena scelta è stata usata all'inizio del fotogramma corrente, il che implica una situazione di thrashing in cui sono in uso più risorse in un singolo fotogramma di quelle che rientrano nella memoria video. In questo modo vengono attivati i criteri di sostituzione per passare a una modalità MRU anziché all'LRU per il resto del frame, in quanto in queste condizioni le prestazioni tendono a essere leggermente migliori. Questo comportamento di thrashing incide in modo significativo sulle prestazioni di rendering. Si noti che la nozione di frame corrente è associata a [**EndScene,**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-endscene)quindi qualsiasi applicazione che usa risorse gestite deve effettuare chiamate regolari a questo metodo.

Gli sviluppatori che desiderano trovare altre informazioni sul comportamento delle risorse gestite nell'applicazione possono usare la query di eventi RESOURCEMANAGER tramite [**l'interfaccia IDirect3DQuery9.**](/windows/desktop/api/d3d9helper/nn-d3d9helper-idirect3dquery9) Questa operazione funziona solo quando si usano i runtime di debug, quindi queste informazioni non possono dipendere dall'applicazione, ma forniscono dettagli approfonditi sulle risorse gestite dal runtime.

Anche se la comprensione del funzionamento di Resource Manager può essere utile durante l'ottimizzazione e il debug delle applicazioni, è importante non associare l'applicazione troppo strettamente ai dettagli di implementazione del runtime o dei driver correnti. Le revisioni del driver o le modifiche apportate all'hardware possono modificare significativamente il comportamento e le versioni future di Direct3D avranno una gestione delle risorse significativamente migliorata e sofisticata.

## <a name="driver-managed-resources"></a>Driver-Managed risorse

I driver Direct3D sono liberi di implementare la funzionalità di trame gestite dal driver, indicata da D3DCAPS2 CANMANAGERESOURCE, che consente al driver di gestire la gestione delle risorse anziché il \_ runtime. Per il driver (raro) che implementa questa funzionalità, il comportamento esatto del gestore di risorse del driver può variare notevolmente ed è necessario contattare il fornitore del driver per informazioni dettagliate sul funzionamento per la loro implementazione. In alternativa, è possibile assicurarsi che il gestore di runtime sia sempre usato specificando D3DCREATE DISABLE DRIVER MANAGEMENT durante \_ \_ la creazione del \_ dispositivo.

## <a name="default-resources"></a>Risorse predefinite

Anche se le risorse gestite sono semplici, efficienti e facili da usare, in alcuni casi è preferibile o addirittura necessario usare direttamente la memoria video. Tali risorse vengono create nella categoria POOL \_ DEFAULT. L'uso di tali risorse causa complicazioni aggiuntive per l'applicazione. Il codice è necessario per gestire la situazione di dispositivo perso per tutte le risorse POOL DEFAULT ed è necessario tenere conto delle considerazioni sulle prestazioni quando si copiano \_ i dati in esse. Se non si specifica USAGE WRITEONLY o si rende bloccabile una destinazione di rendering, è anche possibile che si imponga una \_ grave penalità per le prestazioni.

Se **si chiama Lock** su una risorsa POOL DEFAULT, è più probabile che la GPU si blocchi rispetto all'uso di una risorsa POOL MANAGED, a meno che non si utilizzino determinati flag di \_ \_ hint. A seconda della posizione della risorsa, il puntatore restituito potrebbe essere a un buffer di memoria di sistema temporaneo oppure può essere un puntatore direttamente alla memoria AGP. Se si tratta di un buffer di memoria di sistema temporaneo, i dati dovranno essere trasferiti nella memoria video dopo la **chiamata di** sblocco. Se la risorsa video non è di sola scrittura, sarà necessario trasferire i dati nel buffer temporaneo durante il **blocco**. Se si tratta di un'area di memoria AGP, le copie temporanee vengono evitate, ma il comportamento della cache richiesto può comportare un rallentamento delle prestazioni.

È necessario fare attenzione a scrivere una riga di dati della cache completa in qualsiasi puntatore alla memoria di apertura AGP per evitare la penalità della combinazione di scrittura, che provoca un ciclo di lettura/scrittura, ed è preferibile l'accesso sequenziale all'area di memoria. Se l'applicazione deve eseguire l'accesso casuale ai dati durante la creazione e non si vuole usare una risorsa gestita per il buffer, è invece consigliabile usare una copia della memoria di sistema. Dopo aver creato i dati, è possibile trasmettere il risultato nella memoria della risorsa bloccata per evitare di pagare una penalità elevata per l'operazione di combinazione della scrittura nella cache.

Il flag LOCK NOOVERWRITE può essere usato per accodare i dati in modo efficiente per alcune risorse, ma idealmente è possibile evitare più chiamate Lock e Unlock alla \_ stessa risorsa.   L'uso corretto dei vari flag di blocco è importante per ottenere prestazioni ottimali, così come l'uso di un modello di accesso ai dati facile da memorizzare nella cache quando si riempie la memoria bloccata.

### <a name="using-both-managed-and-default-resources"></a>Uso di risorse gestite e predefinite

La combinazione di allocazioni di risorse gestite e POOL DEFAULT può causare la frammentazione della memoria video e confondere la visualizzazione del runtime della \_ memoria video disponibile per le risorse gestite. Idealmente, è consigliabile creare tutte le risorse POOL DEFAULT prima di usare le risorse GESTITE da POOL o usare la \_ \_ chiamata [**EvictManagedResources**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-evictmanagedresources) prima di allocare le risorse non gestite. Tenere presente che tutte le allocazioni effettuate da POOL DEFAULT che risiedono nella memoria video collegano la memoria per tutta la durata di quella risorsa che non è disponibile per l'uso da parte del gestore di risorse o per \_ qualsiasi altro scopo.

Si noti che a differenza delle versioni precedenti di Direct3D, il runtime della versione 9 esita automaticamente alcune risorse gestite prima di rinunciare a un'allocazione di risorse non gestite non riuscita per mancanza di memoria video, ma questo può potenzialmente creare frammentazione aggiuntiva e persino forzare una risorsa in una posizione non ottimale(ad esempio, con una trama statica nella memoria video non locale). Anche in questo caso, è meglio allocare tutte le risorse non gestite necessarie in anticipo e prima di usare qualsiasi risorsa gestita.

### <a name="dynamic-default-resources"></a>Risorse predefinite dinamiche

I dati generati e aggiornati a una frequenza elevata non necessitano dell'archivio di backup perché tutte le informazioni verranno ri create di nuovo durante il ripristino del dispositivo. Questi dati vengono in genere creati meglio in POOL DEFAULT, specificando l'hint USAGE DYNAMIC, in modo che il driver possa prendere decisioni di ottimizzazione quando inserisce la risorsa, sapendo che verrà \_ \_ aggiornata spesso. Ciò significa in genere inserire la risorsa nella memoria video non locale e quindi l'accesso alla GPU è in genere molto più lento rispetto alla memoria video locale. Per le architetture UMA, il driver potrebbe scegliere un particolare posizionamento per le risorse dinamiche da ottimizzare per l'accesso in scrittura della CPU.

Questo utilizzo è tipico per le soluzioni di interfaccia software e i sistemi di particelle basate su CPU che compilano buffer di vertici/indici e il flag LOCK DISCARD garantisce che non si creino blocchi nei casi in cui la risorsa è ancora in uso dal \_ frame precedente. L'uso di una risorsa gestita in questo caso aggiornerebbe un buffer di memoria di sistema, che verrebbe quindi copiato nella memoria video e quindi usato solo per uno o due fotogrammi prima di essere sostituito. Per i sistemi con memoria video non locale, la copia aggiuntiva viene eliminata usando correttamente questo modello dinamico.

Le trame standard non possono essere bloccate e possono essere aggiornate solo tramite [**UpdateSurface**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-updatesurface) [**o UpdateTexture.**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-updatetexture) Alcuni sistemi supportano trame dinamiche, che possono essere bloccate, e usano il modello LOCK DISCARD, ma è necessario controllare un bit di funzionalità \_ (D3DCAPS2 DYNAMICTEXTURES) prima di usare tali \_ risorse. Per trame altamente dinamiche (video o procedurali), l'applicazione può creare risorse POOL DEFAULT e POOL SYSTEMMEM corrispondenti e gestire gli aggiornamenti della memoria \_ \_ video usando **UpdateTexture.** Per gli aggiornamenti molto frequenti e parziali, **il paradigma UpdateTexture** è probabilmente la scelta migliore.

Per quanto sia utile quanto le risorse dinamiche, prestare attenzione quando si progettano sistemi che si basano molto sull'invio dinamico. Le risorse statiche devono essere inserite in POOL MANAGED per garantire un buon utilizzo della memoria video locale e per un uso più efficiente della larghezza di banda limitata del bus e della \_ memoria principale. Per le risorse semi statiche, è possibile che il costo di un caricamento occasionale nella memoria video locale sia molto inferiore al traffico bus costante generato rendendole dinamiche.

## <a name="system-memory-resources"></a>Risorse di memoria di sistema

Le risorse possono essere create anche in \_ POOL SYSTEMMEM. Sebbene non possano essere usati dalla pipeline grafica, possono essere usati come origini per l'aggiornamento delle risorse POOL \_ DEFAULT usando [**UpdateSurface**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-updatesurface) [**o UpdateTexture.**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-updatetexture) Il comportamento di blocco è semplice, anche se possono verificarsi blocchi se sono in uso da uno dei metodi indicati in precedenza.

Anche se si trovano nella memoria di sistema, le risorse POOL SYSTEMMEM sono limitate agli stessi formati e funzionalità (ad esempio le dimensioni \_ massime) supportati dal driver di dispositivo. Il tipo di risorsa POOL SCRATCH è un'altra forma di risorsa di memoria di sistema che può usare tutti i formati e le funzionalità supportati dal runtime, ma non è accessibile \_ dal dispositivo. Le risorse Scratch sono destinate principalmente all'uso da parte degli strumenti di contenuto.

**Figura 3. Risorse di memoria nella RAM video, nell'apertura AGP e nella RAM di sistema**

![risorse di memoria nella ram video, nell'apertura agp e nella ram di sistema](images/managingresources3.gif)

## <a name="general-recommendations"></a>Suggerimenti generali

Ottenere i dettagli di implementazione tecnica della gestione delle risorse corretti farà molto per raggiungere gli obiettivi di prestazioni per l'applicazione. La pianificazione del modo in cui le risorse vengono presentate a Direct3D e la progettazione dell'architettura relativa al caricamento dei dati in modo orario è un'attività più complessa. Quando si prendono queste decisioni per l'applicazione, è consigliabile usare una serie di procedure consigliate:

-   Pre-elaborare tutte le risorse. Affidarsi a costose conversioni e ottimizzazioni in fase di caricamento per le risorse è utile durante lo sviluppo, ma in questo modo si verifica un grande carico di prestazioni per i computer degli utenti. Le risorse pre-elaborate sono più veloci da caricare, più veloci da usare e offrono la possibilità di eseguire attività off-line sofisticate.
-   Evitare di creare molte risorse per frame. Le interazioni del driver necessarie possono serializzare la CPU e la GPU e le operazioni coinvolte sono di peso elevato, in quanto spesso richiedono transizioni del kernel. Distribuire la creazione su più frame o riutilizzare le risorse senza crearle/rilasciarle. Idealmente, è consigliabile attendere diversi fotogrammi prima di bloccare o rilasciare le risorse usate di recente per il rendering.
-   Alla fine del frame, assicurarsi di annullare l'associazione di tutti i canali di risorse, ovvero le origini di flusso, le fasi di trama e gli indici correnti. In questo modo si garantisce che i riferimenti pentolati alle risorse siano rimossi prima che facciano sì che il gestore delle risorse mantenda le risorse residenti che non sono effettivamente più in uso.
-   Per le trame, usare formati compressi (ad esempio, DXTn) con mappe mip e prendere in considerazione l'uso di un at atlas di trame. Questi riducono notevolmente i requisiti di larghezza di banda e possono ridurre le dimensioni complessive delle risorse, rendendole quindi più efficienti.
-   Per la geometria, usare la geometria indicizzata perché consente di comprimere le risorse del buffer dei vertici e l'hardware video moderno è fortemente ottimizzato per il riutilizzo dei vertici. Usando vertex shader programmabili, è possibile comprimere le informazioni sui vertici ed espanderlo durante l'elaborazione dei vertici. Anche in questo caso, ciò consente di ridurre i requisiti di larghezza di banda e di rendere più efficienti le risorse del vertex buffer.
-   Evitare di ottimizzare la gestione delle risorse. Le future revisioni di driver, hardware e sistema operativo possono causare problemi di compatibilità se l'applicazione viene ottimizzata troppo per una combinazione particolare. Poiché la maggior parte delle applicazioni è associata alla CPU, una gestione costosa basata sulla CPU causa in genere più problemi di prestazioni di quanto non risolva.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione delle risorse](/windows/desktop/direct3d9/managing-resources)
</dt> <dt>

[Dispositivi persi](/windows/desktop/direct3d9/lost-devices)
</dt> <dt>

[Ottimizzazioni delle prestazioni](/windows/desktop/direct3d9/performance-optimizations)
</dt> <dt>

[Risorse trame compresse](/windows/desktop/direct3d9/compressed-texture-resources)
</dt> <dt>

[Query](/windows/desktop/direct3d9/queries)
</dt> <dt>

[**D3DUSAGE**](/windows/desktop/direct3d9/d3dusage)
</dt> <dt>

[**D3DPOOL**](/windows/desktop/direct3d9/d3dpool)
</dt> <dt>

[D3DCREATE](/windows/desktop/direct3d9/d3dcreate)
</dt> </dl>

 

 