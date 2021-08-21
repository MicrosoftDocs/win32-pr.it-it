---
title: Residency
description: Un oggetto viene considerato residente quando è accessibile dalla GPU.
ms.assetid: 956F80D7-EEC8-4D88-B251-EE325614F31E
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 257af2526120df5509a38fcc0c81984aa53a954f8eed6a8ce9194fa2aadb020a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989456"
---
# <a name="residency"></a>Residency

Un oggetto viene considerato *residente* quando è accessibile dalla GPU.

-   [Budget di residenza](#residency-budget)
-   [Risorse heap](#heap-resources)
-   [Priorità di residenza](#residency-priorities)
    -   [Algoritmo di priorità predefinito](#default-priority-algorithm)
-   [Programmazione della gestione della residenza](#programming-residency-management)
-   [Argomenti correlati](#related-topics)

## <a name="residency-budget"></a>Budget di residenza

Le GPU non supportano ancora l'errore di pagina, pertanto le applicazioni devono eseguire il commit dei dati nella memoria fisica mentre la GPU può accedervi. Questo processo è noto come "creazione di qualcosa di residente" e deve essere eseguito sia per la memoria di sistema fisica che per la memoria video discreta fisica. In D3D12 la maggior parte degli oggetti API incapsula una quantità di memoria accessibile tramite GPU. Tale memoria accessibile tramite GPU viene resa residente durante la creazione dell'oggetto API ed espulsa in caso di distruzione di oggetti API.

La quantità di memoria fisica disponibile per il processo è nota come budget di memoria video. Il budget può variare in modo notevolmente durante la riattivazione e la sospensione dei processi in background. e fluttuano notevolmente quando l'utente passa a un'altra applicazione. L'applicazione può ricevere una notifica quando il budget cambia ed esegue il polling sia del budget corrente che della quantità di memoria attualmente utilizzata. Se un'applicazione non rientra nel budget, il processo verrà bloccato in modo intermittente per consentire l'esecuzione di altre applicazioni e/o le API di creazione restituiranno un errore. [**L'interfaccia IDXGIAdapter3**](/windows/desktop/api/dxgi1_4/nn-dxgi1_4-idxgiadapter3) fornisce i metodi relativi a questa funzionalità, in particolare [**QueryVideoMemoryInfo**](/windows/desktop/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-queryvideomemoryinfo) e [**RegisterVideoMemoryBudgetChangeNotificationEvent**](/windows/desktop/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-registervideomemorybudgetchangenotificationevent).

Le applicazioni sono invitate a usare una prenotazione per indicare la quantità di memoria di cui non possono fare a meno. Idealmente, le impostazioni grafiche "basse" specificate dall'utente, o qualcosa di ancora più basso, sono il valore giusto per una prenotazione di questo tipo. L'impostazione di una prenotazione non offrirà mai a un'applicazione un budget superiore a quello normalmente ricevuto. Al contrario, le informazioni sulla prenotazione consentono al kernel del sistema operativo di ridurre rapidamente l'impatto di situazioni di utilizzo elevato della memoria. Anche la prenotazione non è garantita per essere disponibile per l'applicazione quando l'applicazione non è l'applicazione in primo piano.

## <a name="heap-resources"></a>Risorse heap

Sebbene molti oggetti API incapsulano una memoria accessibile tramite GPU, è previsto che gli heap & risorse siano il modo più significativo in cui le applicazioni utilizzano e gestiscono la memoria fisica. Un heap è l'unità di livello più basso per gestire la memoria fisica, quindi è bene avere familiarità con le relative proprietà di residenza.

-   Gli heap non possono essere resi parzialmente residenti, ma esistono soluzioni alternative con risorse riservate.
-   Gli heap devono essere a budget come parte di un pool specifico. Le schede UMA hanno un pool, mentre le schede discrete hanno due pool. Anche se è vero che il kernel può spostare alcuni heap sulle schede discrete dalla memoria video alla memoria di sistema, lo fa solo come ultima risorsa estrema. Le applicazioni non devono basarsi sul comportamento over-budget del kernel e devono concentrarsi su una buona gestione del budget.
-   Gli heap possono essere sfrattati dalla residenza, che consente di eseguire il paged del contenuto su disco. Tuttavia, la distruzione degli heap è una tecnica più affidabile per liberare la residenza in tutte le architetture dell'adapter. Nelle schede in cui il campo *MaxGPUVirtualAddressBitsPerProcess* di [**D3D12 \_ FEATURE DATA \_ \_ GPU VIRTUAL ADDRESS \_ \_ \_ SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_gpu_virtual_address_support) è prossimo alle dimensioni del budget, [**Evict**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-evict) non recupera in modo affidabile la residenza.
-   La creazione dell'heap può essere lenta. ma è ottimizzato per l'elaborazione dei thread in background. È consigliabile creare heap nei thread in background per evitare problemi nel thread di rendering. In D3D12 più thread possono chiamare in modo sicuro le routine create contemporaneamente.

D3D12 introduce maggiore flessibilità e ortogonalità nel modello di risorse per abilitare più opzioni per le applicazioni. In D3D12 sono disponibili tre tipi di risorse di alto livello: commit, posizione e riservato.

-   Le risorse di cui è stato eseguito il commit creano contemporaneamente una risorsa e un heap. L'heap è implicito e non è accessibile direttamente. L'heap viene ridimensionato in modo appropriato per individuare l'intera risorsa all'interno dell'heap.
-   Le risorse posizionate consentono il posizionamento di una risorsa in corrispondenza di un offset diverso da zero all'interno di un heap. Gli offset devono in genere essere allineati a 64 KB. ma esistono alcune eccezioni in entrambe le direzioni. Le risorse MSAA richiedono l'allineamento dell'offset di 4 MB e l'allineamento dell'offset di 4 KB è disponibile per trame di piccole dimensioni. Le risorse posizionate non possono essere rilocate o mappate direttamente in un altro heap. ma consentono una semplice rilocazione dei dati delle risorse tra heap. Dopo aver creato una nuova risorsa inserita in un heap diverso e aver copiato i dati della risorsa, sarà necessario usare nuovi descrittori di risorsa per il nuovo percorso dei dati delle risorse.
-   Le risorse riservate sono disponibili solo quando l'adapter supporta le risorse affiancate di livello 1 o superiore. Se disponibili, offrono le tecniche di gestione della residenza più avanzate disponibili; ma non tutti gli adattatori li supportano attualmente. Consentono di modificare il mapping di una risorsa senza richiedere la rigenerazione dei descrittori di risorse, la residenza parziale a livello mip e gli scenari di trama di tipo sparse e così via. Non tutti i tipi di risorse sono supportati anche quando sono disponibili risorse riservate, quindi un gestore di residenza basato su pagine completamente generale non è ancora fattibile.

## <a name="residency-priorities"></a>Priorità di residenza

Il Windows 10 Creators Update consente agli sviluppatori di influire su quali heap e risorse sarà preferibile rimanere residenti quando la pressione della memoria richiede l'abbassamento di livello di alcune delle risorse. Ciò consente agli sviluppatori di creare applicazioni con prestazioni migliori sfruttando la conoscenza che il runtime non può dedurre dall'utilizzo delle API. Si prevede che gli sviluppatori diventeranno più confortevoli e in grado di specificare le priorità durante la transizione dall'uso delle risorse di cui è stato eseguito il commit alle risorse reinviate e affiancate.

L'applicazione di queste priorità deve essere più semplice della gestione di due budget di memoria dinamica, dell'abbassamento di livello e dell'innalzamento di livello manuale delle risorse, perché le applicazioni possono già farlo. Di conseguenza, la progettazione dell'API di priorità di residenza è naturalmente con granularità con priorità predefinite ragionevoli assegnate a ogni heap o risorsa durante la creazione. Per altre informazioni, vedere [**ID3D12Device1::SetResidencyPriority**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device1-setresidencypriority) e [**l'enumerazione D3D12 \_ RESIDENCY \_ PRIORITY.**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_residency_priority)

Con le priorità, è previsto che gli sviluppatori:

-   Aumentare la priorità di alcuni heap eccezionali per attenuare meglio l'impatto sulle prestazioni di questi heap abbassati di livello prima o più frequentemente rispetto ai modelli di accesso naturali richiesti. Si prevede che questo approccio verrà sfruttato dalle applicazioni portate dalle API grafiche, ad esempio Direct3D 11 o OpenGL, che il modello di gestione delle risorse è significativamente diverso da quello di Direct3D 12.
-   Eseguire l'override di quasi tutte le priorità dell'heap con lo schema di bucketizzazione dell'applicazione, fisso, in base alla conoscenza della frequenza di accesso del programmatore o dinamico; uno schema fisso è più semplice da gestire rispetto a uno dinamico, ma può essere meno efficace e richiedere l'intevention del programmatore in quanto i modelli di utilizzo cambiano nel corso dello sviluppo. Questo approccio dovrebbe essere sfruttato dalle applicazioni compilate con la gestione delle risorse in stile Direct3D 12, ad esempio quelle che usano la libreria di residenza (in particolare gli schemi dinamici).

### <a name="default-priority-algorithm"></a>Algoritmo di priorità predefinito

Un'applicazione non può specificare priorità utili per qualsiasi heap che tenta di gestire senza prima sottostanare l'algoritmo di priorità predefinito. Ciò è dovuto al fatto che il valore dell'assegnazione di una particolare priorità a un heap è derivato dalla priorità relativa ad altri heap con priorità che competono per la stessa memoria.

La strategia scelta per la generazione di priorità predefinite consiste nel suddividere gli heap in due bucket, favorendo (assegnando priorità più elevata) agli heap che si presuppone siano scritti frequentemente dalla GPU rispetto agli heap che non lo sono.

Il bucket con priorità alta contiene heap e risorse creati con flag che li identificano come destinazioni di rendering, buffer depth-stencil o viste di accesso non ordinate. A questi valori di priorità vengono assegnati valori di priorità nell'intervallo a partire da **D3D12 \_ RESIDENCY \_ PRIORITY \_ HIGH.** Per definire ulteriormente la priorità tra questi heap e risorse, i 16 bit più bassi della priorità vengono impostati sulle dimensioni dell'heap o della risorsa suddivise per 10 MB (saturazione di 0xFFFF per heap estremamente grandi). Questa priorità aggiuntiva favorisce heap e risorse più grandi.

Il bucket con priorità bassa contiene tutti gli altri heap e risorse a cui viene assegnato un valore di priorità **D3D12 \_ RESIDENCY \_ PRIORITY \_ NORMAL.** Non viene tentata un'ulteriore assegnazione di priorità tra questi heap e risorse.

## <a name="programming-residency-management"></a>Programmazione della gestione della residenza

Le applicazioni semplici possono essere in grado di ottenere semplicemente creando risorse di cui è stato eseguito il commit fino a quando non si verificano errori di memoria insufficiente. In caso di errore, l'applicazione può eliminare altre risorse o oggetti API di cui è stato eseguito il commit per consentire l'esito positivo di altre creazioni di risorse. Tuttavia, anche le applicazioni semplici sono fortemente consigliate per controllare le modifiche negative del budget ed eliminare gli oggetti API inutilizzati approssimativamente una volta un frame.

La complessità di una progettazione di gestione della residenza si farà più complessa quando si tenta di ottimizzare le architetture degli adapter o di incorporare le priorità di residenza. L'assegnazione discreta del budget e la gestione di due pool di memoria discreta saranno più complesse rispetto alla gestione di una sola e l'assegnazione di priorità fisse su larga scala può diventare un onere di manutenzione se i modelli di utilizzo si evolvono. L'overflow delle trame nella memoria di sistema aumenta la complessità, in quanto la risorsa errata nella memoria di sistema può influire negativamente sulla frequenza dei fotogrammi. Inoltre, non è disponibile alcuna funzionalità semplice per identificare le risorse che potrebbero trarre vantaggio da una maggiore larghezza di banda GPU o tollerare una larghezza di banda GPU inferiore.

Progettazioni ancora più complesse esegue una query per le funzionalità dell'adapter corrente. Queste informazioni sono disponibili in [**D3D12 \_ FEATURE \_ DATA \_ GPU VIRTUAL ADDRESS \_ \_ \_ SUPPORT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_gpu_virtual_address_support), [**D3D12 \_ FEATURE DATA \_ \_ ARCHITECTURE,**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_architecture) [**D3D12 \_ TILED RESOURCES \_ \_ TIER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier)e [**D3D12 \_ RESOURCE HEAP \_ \_ TIER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_heap_tier).

È probabile che più parti di un'applicazione si consee ranno usando tecniche diverse. Ad esempio, alcune trame di grandi dimensioni e percorsi di codice raramente esemplati possono usare risorse di cui è stato eseguito il commit, mentre molte trame possono essere designate con una proprietà di streaming e usare una tecnica generale di risorse posizionate.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**ID3D12Heap**](/windows/desktop/api/d3d12/nn-d3d12-id3d12heap)
</dt> <dt>

[Gestione della memoria](memory-management.md)
</dt> </dl>

 

 