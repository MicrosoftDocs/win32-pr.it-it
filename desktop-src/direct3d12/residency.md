---
title: Residenza
description: Un oggetto viene considerato residente quando è accessibile dalla GPU.
ms.assetid: 956F80D7-EEC8-4D88-B251-EE325614F31E
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b842ce5b3e89c3877f50036e747a90f14104bce
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548858"
---
# <a name="residency"></a>Residenza

Un oggetto viene considerato *residente* quando è accessibile dalla GPU.

-   [Budget residenza](#residency-budget)
-   [Risorse heap](#heap-resources)
-   [Priorità di residenza](#residency-priorities)
    -   [Algoritmo di priorità predefinito](#default-priority-algorithm)
-   [Programmazione della gestione delle residenze](#programming-residency-management)
-   [Argomenti correlati](#related-topics)

## <a name="residency-budget"></a>Budget residenza

Le GPU non supportano ancora l'errore di pagina, quindi le applicazioni devono eseguire il commit dei dati nella memoria fisica mentre la GPU può accedervi. Questo processo è noto come "creazione di un elemento residente" e deve essere eseguito sia per la memoria di sistema fisica che per la memoria del video discreta fisica. In D3D12 la maggior parte degli oggetti API incapsula una certa quantità di memoria accessibile dalla GPU. Tale memoria accessibile dalla GPU viene resa residente durante la creazione dell'oggetto API ed eliminata durante la distruzione dell'oggetto API.

La quantità di memoria fisica disponibile per il processo è nota come budget di memoria video. Il budget può variare in modo evidente dal momento che i processi in background riattivano e dormono; e variano notevolmente quando l'utente passa a un'altra applicazione. L'applicazione può ricevere una notifica quando il budget viene modificato e viene eseguito il polling del budget corrente e della quantità di memoria attualmente utilizzata. Se un'applicazione non rimane entro il suo budget, il processo verrà bloccato in modo intermittente per consentire l'esecuzione di altre applicazioni e/o le API di creazione restituiranno un errore. L'interfaccia [**IDXGIAdapter3**](/windows/desktop/api/dxgi1_4/nn-dxgi1_4-idxgiadapter3) fornisce i metodi relativi a questa funzionalità, in particolare [**QueryVideoMemoryInfo**](/windows/desktop/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-queryvideomemoryinfo) e [**RegisterVideoMemoryBudgetChangeNotificationEvent**](/windows/desktop/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-registervideomemorybudgetchangenotificationevent).

Le applicazioni sono incoraggiate a usare una prenotazione per indicare la quantità di memoria di cui non è possibile accedere. Idealmente, le impostazioni grafiche "low" specificate dall'utente o qualcosa di più basso è il valore corretto per tale prenotazione. L'impostazione di una prenotazione non consentirà a un'applicazione di ottenere un budget superiore rispetto a quello normalmente ricevuto. Al contrario, le informazioni sulla prenotazione consentono al kernel del sistema operativo di ridurre rapidamente l'effetto delle situazioni di utilizzo elevato della memoria. Anche se l'applicazione non è un'applicazione in primo piano, non è garantita la disponibilità della prenotazione.

## <a name="heap-resources"></a>Risorse heap

Sebbene molti oggetti API incapsulano alcune risorse di memoria accessibili per la GPU, è previsto che gli heap & risorse siano il modo più significativo per utilizzare e gestire la memoria fisica da parte delle applicazioni. Un heap è l'unità di livello più basso per la gestione della memoria fisica, quindi è opportuno avere familiarità con le proprietà di residenza.

-   Gli heap non possono essere resi parzialmente residenti, ma esistono soluzioni alternative con risorse riservate.
-   Gli heap devono essere inclusi in un budget come parte di un pool specifico. Gli adapter UMA hanno un pool, mentre gli adattatori discreti hanno due pool. Sebbene sia vero, il kernel può spostare alcuni heap sugli adattatori discreti dalla memoria video alla memoria di sistema, ma solo come ultima risorsa. Le applicazioni non devono basarsi sul comportamento di budget eccessivo del kernel e dovrebbero concentrarsi sulla gestione del budget.
-   Gli heap possono essere rimossi dalla residenza, che consente il paging del contenuto sul disco. Tuttavia, la distruzione degli heap è una tecnica più affidabile per liberare la residenza in tutte le architetture degli adapter. Nelle schede in cui il campo *theMaxGPUVirtualAddressBitsPerProcess* del supporto per gli [**\_ \_ \_ \_ \_ indirizzi \_ virtuali della GPU dei dati della funzionalità D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_gpu_virtual_address_support) è vicino alle dimensioni del budget, [**Rimuovi**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-evict) non recupererà in modo affidabile la residenza.
-   La creazione dell'heap può essere lenta; ma è ottimizzato per l'elaborazione dei thread in background. È consigliabile creare heap sui thread in background per evitare la glitching del thread di rendering. In D3D12, più thread possono chiamare in modo sicuro le routine create simultaneamente.

D3D12 introduce una maggiore flessibilità e ortogonalità nel modello di risorse, in modo da consentire più opzioni per le applicazioni. Sono disponibili tre tipi di risorse di alto livello in D3D12: commit, inserito e riservato.

-   Le risorse di cui è stato eseguito il commit creano una risorsa e un heap nello stesso momento. L'heap è implicito e non è possibile accedervi direttamente. L'heap è dimensionato in modo appropriato per individuare l'intera risorsa all'interno dell'heap.
-   Le risorse posizionate consentono il posizionamento di una risorsa con un offset diverso da zero all'interno di un heap. Gli offset devono in genere essere allineati a 64KB; Tuttavia, alcune eccezioni sono presenti in entrambe le direzioni. Le risorse MSAA richiedono l'allineamento di offset 4 MB e l'allineamento dell'offset 4KB è disponibile per le trame di piccole dimensioni. Le risorse posizionate non possono essere rilocate o rimappate direttamente a un altro heap; ma consentono una rilocazione semplice dei dati delle risorse tra gli heap. Dopo la creazione di una nuova risorsa posizionata in un heap diverso e la copia dei dati della risorsa, sarà necessario usare nuovi descrittori di risorse per la nuova posizione dei dati della risorsa.
-   Le risorse riservate sono disponibili solo se l'adapter supporta il livello 1 o superiore delle risorse affiancate. Quando disponibili, offrono le tecniche di gestione della residenza più avanzate disponibili; ma non tutti gli adapter li supportano attualmente. Consentono di ricreare il mapping di una risorsa senza richiedere la rigenerazione di descrittori di risorse, residenza del livello MIP parziale e scenari di trama sparse e così via. Non tutti i tipi di risorse sono supportati anche quando sono disponibili risorse riservate, quindi non è ancora possibile un gestore di residenza completo basato su pagine.

## <a name="residency-priorities"></a>Priorità di residenza

Windows 10 Creators Update consente agli sviluppatori di influenzare gli heap e le risorse che preferiscono rimanere residenti quando la pressione della memoria richiede l'abbassamento di grado di alcune risorse. Questo consente agli sviluppatori di creare applicazioni con prestazioni migliori sfruttando la conoscenza che il runtime non può dedurre dall'utilizzo dell'API. Si prevede che gli sviluppatori diventeranno più comodi e possano specificare le priorità durante la transizione dall'uso di risorse sottoposti a commit a riservato e alle risorse affiancate.

L'applicazione di queste priorità deve essere più semplice rispetto alla gestione di due budget di memoria dinamici, abbassamento manualmente e innalzamento di grado delle risorse bettween, dal momento che le applicazioni possono già farlo. Per questo motivo, la progettazione dell'API della priorità di residenza è naturalmente con granularità ragionevole assegnata a ogni heap o risorsa come creata. Per ulteriori informazioni, vedere [**ID3D12Device1:: SetResidencyPriority**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device1-setresidencypriority) e l'enumerazione di [**\_ \_ priorità di residenza D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_residency_priority) .

Con le priorità, gli sviluppatori dovrebbero:

-   Aumentare la priorità di alcuni heap eccezionali per attenuare al meglio l'effetto sulle prestazioni di questi heap abbassati prima o con maggiore frequenza rispetto ai modelli di accesso naturale richiesti. Questo approccio dovrebbe essere usato dalle applicazioni portate da API grafiche, ad esempio Direct3D 11 o OpenGL, il modello di gestione delle risorse è significativamente diverso rispetto a quello di Direct3D 12.
-   Eseguire l'override di quasi tutte le priorità dell'heap con lo schema di bucket personalizzato dell'applicazione, sia fisso, in base alla conoscenza della frequenza di accesso del programmatore, sia dinamica; uno schema fisso è più semplice da gestire rispetto a uno dinamico, ma può essere meno efficace e richiedere al programmatore intervento di modificare i modelli di utilizzo nel corso dello sviluppo. Questo approccio dovrebbe essere usato dalle applicazioni compilate con la gestione delle risorse di tipo Direct3D 12, ad esempio quelle che usano la libreria di residenza (in particolare gli schemi dinamici).

### <a name="default-priority-algorithm"></a>Algoritmo di priorità predefinito

Un'applicazione non può specificare le priorità utili per tutti gli heap che tenta di gestire senza prima sottostanare l'algoritmo di priorità predefinito. Ciò è dovuto al fatto che il valore di assegnazione di una particolare priorità a un heap deriva dalla relativa priorità ad altri heap con priorità che competono per la stessa memoria.

La strategia scelta per la generazione delle priorità predefinite consiste nel categorizzare gli heap in due bucket, privilegiando gli heap (assegnando una priorità più elevata) che si presume vengano scritti frequentemente dalla GPU sugli heap che non lo sono.

Il bucket ad alta priorità contiene heap e risorse creati con flag che li identificano come destinazioni di rendering, buffer di stencil Depth o viste di accesso non ordinate (UAV). A questi vengono assegnati valori di priorità nell'intervallo a partire da **D3D12 \_ Residency \_ Priority \_ High**. per definire ulteriormente le priorità tra questi heap e risorse, i 16 bit più bassi della priorità vengono impostati sulla dimensione dell'heap o della risorsa divisa da 10 MB (saturazione a 0xFFFF per heap estremamente grandi). Questa impostazione di priorità aggiuntiva favorisce heap e risorse più grandi.

Il bucket con priorità bassa contiene tutti gli altri heap e risorse a cui viene assegnato un valore di priorità di **D3D12 \_ Residency \_ Priority \_ Normal**. Non è stata tentata alcuna ulteriore assegnazione di priorità tra questi heap e risorse.

## <a name="programming-residency-management"></a>Programmazione della gestione delle residenze

Le applicazioni semplici potrebbero essere in grado di ottenere semplicemente creando risorse di cui è stato eseguito il commit finché non si verificano errori di memoria insufficiente. In caso di errore, l'applicazione può eliminare altre risorse o oggetti API di cui è stato eseguito il commit per consentire la riuscita di altre creazioni di risorse. Tuttavia, anche le applicazioni semplici sono fortemente consigliate per tenere sotto controllo le modifiche di budget negative ed eliminare gli oggetti API inutilizzati approssimativamente una volta al frame.

La complessità di un progetto di gestione della residenza si verifica quando si tenta di ottimizzare le architetture degli adattatori o di incorporare le priorità di residenza. Il budget e la gestione discreta di due pool di memoria discreta saranno più complessi rispetto alla gestione di un solo e l'assegnazione di priorità fisse su larga scala può diventare un carico di manutenzione se i modelli di utilizzo cambiano. L'overflow delle trame nella memoria di sistema aggiunge una maggiore complessità, perché la risorsa sbagliata nella memoria del sistema può influire gravemente sulla frequenza dei fotogrammi. Non sono disponibili funzionalità semplici che consentono di identificare le risorse che trarrebbero vantaggio da una maggiore larghezza di banda GPU o tollerano una larghezza di banda GPU inferiore.

Le progettazioni ancora più complesse eseguiranno una query per le funzionalità dell'adapter corrente. Queste informazioni sono disponibili nel [**supporto per gli \_ \_ \_ \_ \_ indirizzi \_ virtuali della GPU dati delle funzionalità di D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_gpu_virtual_address_support), nell' [**\_ \_ \_ architettura dei dati della funzionalità D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_architecture), nel [**\_ \_ \_ livello di risorse affiancato D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_tiled_resources_tier)e nel [**\_ \_ \_ livello heap risorse D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_heap_tier).

È probabile che più parti di un'applicazione si ritrovino utilizzando tecniche diverse. Ad esempio, alcune trame di grandi dimensioni e percorsi di codice utilizzati raramente possono utilizzare risorse di cui è stato eseguito il commit, mentre molte trame possono essere designate con una proprietà di flusso e utilizzare una tecnica di risorse poste generali.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**ID3D12Heap**](/windows/desktop/api/d3d12/nn-d3d12-id3d12heap)
</dt> <dt>

[Gestione della memoria](memory-management.md)
</dt> </dl>

 

 