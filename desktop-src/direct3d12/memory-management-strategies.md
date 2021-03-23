---
title: Strategie di gestione della memoria
description: Un gestore della memoria per Direct3D 12 potrebbe essere molto complicato rapidamente con tutti i diversi livelli di supporto, per gli adapter UMA o discreti (non-UMA) e con una vasta gamma di differenze di architettura tra gli adattatori GPU. La strategia consigliata per la gestione della memoria di Direct3D 12, descritta in questa sezione, è \ 0034; classifica, budget e Stream \ 0034;.
ms.assetid: BC9894F7-D496-46F2-A5C3-C7CA31FD4BA8
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dad04055a5acdeeeaead3a56f0bd04e64aa90fe0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548837"
---
# <a name="memory-management-strategies"></a>Strategie di gestione della memoria

Un gestore della memoria per Direct3D 12 potrebbe essere molto complicato rapidamente con tutti i diversi livelli di supporto, per gli adapter UMA o discreti (non-UMA) e con una vasta gamma di differenze di architettura tra gli adattatori GPU.

La strategia consigliata per la gestione della memoria di Direct3D 12, descritta in questa sezione, è "classificazione, budget e flusso".

-   [Tipi di risorsa](#resource-types)
-   [Budget per la memoria](#memory-budget)
-   [Strategia di classificazione](#classification-strategy)
-   [Argomenti correlati](#related-topics)

## <a name="resource-types"></a>Tipi di risorsa

Il concetto di base di una "risorsa di cui è stato eseguito il commit", ovvero la creazione di spazi di indirizzi virtuali e fisici inizializzati nella memoria fisica gestita, è stato girato da Direct3D 9, anche se l'indirizzamento virtuale (VA) e l'indirizzamento fisico possono essere presi in esame in Direct3D 12 per consentire all'app di gestire con attenzione la memoria fisica.

Oltre alle risorse di cui è stato eseguito il commit, il costrutto di heap di Direct3D 12 Abilita altri due tipi di risorsa: "posizione" e "riservata". In Direct3D 11 una risorsa "riservata" era nota come "risorsa affiancata".

Le risorse riservate sono diverse dalle risorse posizionate in quanto le risorse riservate hanno lo spazio degli indirizzi virtuali GPU univoco. Ciò consente un'allocazione di grandi dimensioni dello spazio VA all'inizio, quindi Abilita il mapping delle pagine VA a determinate sezioni dell'heap in un secondo momento e l'applicazione riconfigura la disposizione in tempo reale. Lo spazio VA è contiguo e può essere mappato in modo sporadico a.

La risorsa riservata può essere creata per fare riferimento alle aree nell'heap con chiamate API, ad esempio [**UpdateTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings) , e può essere resa residente dall'app aggiornando le tabelle di pagine in tempo reale. Quando viene eseguito il mapping di un intervallo VA a un heap NULL o non residente, tale parte della risorsa viene considerata non residente. Quando viene eseguito il mapping di un intervallo VA a un heap residente, tale parte della risorsa viene considerata residente. Gli heap sono residenti al momento della creazione.

Le risorse posizionate sono una progettazione molto più semplice, essendo semplicemente un puntatore a una determinata area di un heap, ad esempio un'area di 1 MB per una trama in un heap di 5 MB. Le barriere di aliasing consentono l'uso di risorse posizionate sovrapposte (vedere [**CreatePlacedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createplacedresource) e [**ResourceBarrier**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)).

Le risorse riservate non sono disponibili in tutti i componenti hardware Direct3D 12 e le risorse posizionate sono un fallback ragionevole, sebbene le risorse posizionate debbano essere contigue e non possano essere parzialmente residenti.

## <a name="memory-budget"></a>Budget per la memoria

In Direct3D 12 quando si alloca un heap si crea l'aspetto della memoria fisica di una risorsa di cui è stato eseguito il commit. La scelta di un segmento di memoria più esplicito è disponibile in Direct3D 12 (scegliendo tra video e memoria di sistema). Gli adapter UMA hanno solo un singolo segmento di memoria, memoria di sistema.

Le GPU non supportano gli errori di pagina, quindi gli sviluppatori devono essere consapevoli che non si impegnano sul commit, soprattutto nei sistemi, ad indicare solo 1 GB di memoria di sistema. Se un'app esegue il commit, il sistema operativo usa la pianificazione dei processi con granularità grossolana in base alla domanda sulla memoria fisica. L'utilità di pianificazione blocca i processi in primo piano e ne esegue sostanzialmente il paging in un processo in background che vuole eseguire. La memoria fisica disponibile può variare notevolmente a seconda delle operazioni eseguite dall'utente in background, ad esempio l'esecuzione di un browser o l'osservazione di un video.

Il budget per l'API per la memoria è [**QueryVideoMemoryInfo**](/windows/desktop/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-queryvideomemoryinfo). Per gli adattatori discreti "local" si tratta di memoria video "non locale" è memoria di sistema. Per gli adapter UMA non locale è sempre zero. Una domanda di progettazione è se il motore gestisce sia i budget sia solo il budget locale. La gestione solo del budget locale è più semplice, ma presenta alcune avvertenze; ad esempio, è disponibile un budget locale massimo di 1 GB, quindi tutti gli heap derivano da tale 1 GB in un sistema UMA e non è presente alcun overflow per la memoria di sistema (ovviamente, perché non ne esiste nessuno).

Poiché Direct3D11 managed memory per le applicazioni, le risorse inutilizzate verrebbero essenzialmente sottopaginate.

Scegliere le dimensioni più appropriate per le risorse. Valutare se le dimensioni di una risorsa sono appropriate per la situazione in cui l'applicazione è effettivamente in esecuzione. Alcuni utenti possono eseguire l'applicazione in una finestra o con una risoluzione dello schermo di 800x600.

## <a name="classification-strategy"></a>Strategia di classificazione

Per gestire le risorse in modo efficace negli scenari associati alla memoria, valutare la possibilità di classificare le risorse nei seguenti elementi:



| Classificazione      | Esempio                                                                                         | Oggetti e funzionalità API                                                                                           | Note sulla gestione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Critico            | Interfaccia utente del gioco                                                                                          | Allocatore di comandi, code di comandi, heap di query, risorse e heap di risorse.                                      | Questi elementi devono essere inseriti in memoria non paginabile/sempre vincolata.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Ridimensionato/facoltativo    | Modelli e trame specifici del livello, catene di scambio, caselle Sky, modelli di caratteri per i giocatori per la prima persona | Risorse e heap. Le risorse di cui è stato eseguito il commit, ma anche le risorse riservate possono funzionare correttamente.          | Integrare il budget della residenza di memoria negli algoritmi di rendering. Scegliere il livello di dettaglio disponibile appropriato e rivalutare meno di una volta per fotogramma. Le tecniche includono l'uso di risorse a dimensione variabile e la scalabilità della catena di scambio.<br/>                                                                                                                                                                                                                                                                                                                                                 |
| Risorse riutilizzate   | Buffer Shadow, risorse di rendering posticipate, risorse di post-elaborazione, cache di dati di illuminazione    | Risorse e heap. Risorse posizionate sovrapposte su heap e barriere di aliasing.                                  | Riutilizzare risorse di grandi dimensioni o aree heap all'interno di un frame per ridurre i requisiti per l'intero frame. Usare la tecnica di riutilizzo della memoria intra-frame. In Direct3D 11, le applicazioni potevano riutilizzare solo le risorse con lo stesso tipo e dimensioni potenzialmente sufficientemente grandi. Gli heap Direct3D 12 consentono di usare risorse sovrapposte per un riutilizzo molto più semplice e maggiore.<br/>                                                                                                                                                                                                                              |
| Risorse di streaming | Terreno, trame e geometria Open-World                                                        | Risorse e heap. Creazione a thread libero, thread della CPU in background e code ed elenchi di comandi per la copia in background. | La residenza parziale, in genere basata sulla visibilità (usando la valutazione di View-tronco o distance) e la rivalutazione della residenza necessita di ogni fotogramma.<br/> Quando l'adapter GPU supporta risorse riservate all'interno di heap, è disponibile la tecnica di utilizzo di una gestione di residenza parziale per riquadro e di riutilizzo tra frame.<br/> Usando la tecnica di riutilizzo della memoria tra frame, è possibile eseguire la residenza parziale di risorse parziali, ma è meno ottimale. Le risorse posizionate con gli heap devono consentire un riciclo più veloce, ma è possibile usare le risorse con commit come fallback.<br/> |



 

Maggiore è il numero di applicazioni che gravitano sulle risorse di streaming per la maggior parte del lavoro, maggiore sarà la possibilità di sfruttare le risorse posizionate e riservate, in modo da massimizzare il riutilizzo della memoria tra queste quattro classificazioni. Maggiore è il flusso di applicazioni, maggiore è il budget e assegnano priorità alla larghezza di banda.

In genere, con i motori grafici Direct3D 12 è necessario rispettare un budget più vario e dinamico ed eseguire questa operazione in modo più rigoroso rispetto al passato. Le applicazioni migliori troveranno tutte e quattro le categorie nel budget assegnato al processo, ridimensionando la riproduzione del gioco dall'app per dispositivi mobili in background ai budget discreti a schermo intero. Tuttavia, molte applicazioni probabilmente lotteranno iniziando con un numero eccessivo di tipi di risorse critiche. Direct3D 11 consente di creare anonimamente risorse abilitate e occupare lo stato critico senza influisca sulle prestazioni. Tuttavia, per Direct3D 12, gli sviluppatori devono cercare diligentemente le risorse create in modo casuale in tutto il motore e il middleware e assegnarle nuovamente a una delle altre categorie.

Altre aree problematiche sono componenti middleware, controlli utente e flussi intra-frame. I componenti del middleware potrebbero non essere esposti a un budget, né devono funzionare strettamente insieme. È probabile che i componenti middleware espongano le funzionalità come tecniche di rendering; e l'applicazione può basarsi sull'esposizione delle impostazioni del middleware e del motore. Gli sviluppatori possono affidarsi a Direct3D 11 per eseguire il paging e ottenere la frequenza dei fotogrammi corretta. In alcuni casi, è possibile che le applicazioni Direct3D 11 abbiano effettuato il paging del contenuto delle risorse in ogni frame. e hanno generato una frequenza di fotogrammi accettabile per l'utente. La maggior parte dei motori trasmette solo i dati delle risorse come attività in background, in cui non è disponibile un fallback normale a flussi intra-frame con priorità alta. Chiedere ai motori di implementare in modo da erodere alcuni dei miglioramenti di overhead della CPU cercati passando a Direct3D 12. Gli sviluppatori del motore potevano prendere in considerazione la possibilità di prendere in esame i frame in fasi per offrire maggiori opportunità di risorse riutilizzabili; e probabilmente funzionano con i fornitori di middleware per supportare risorse e heap posizionati per il riutilizzo della memoria intra-frame.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**CreateCommittedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource)
</dt> <dt>

[**CreateReservedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createreservedresource)
</dt> <dt>

[Guida per programmatori Direct3D 12](directx-12-programming-guide.md)
</dt> <dt>

[Gestione della memoria](memory-management.md)
</dt> <dt>

[Associazione di risorse](resource-binding.md)
</dt> </dl>

 

