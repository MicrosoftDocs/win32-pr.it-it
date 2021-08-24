---
title: Strategie di gestione della memoria
description: Un gestore di memoria per Direct3D 12 può essere molto complicato rapidamente con tutti i diversi livelli di supporto, per schede UMA o discrete (non UMA) e con una notevole gamma di differenze di architettura tra le schede GPU. La strategia consigliata per la gestione della memoria Direct3D 12, descritta in questa sezione, è \ 0034;classificazione, budget e flusso \ 0034;.
ms.assetid: BC9894F7-D496-46F2-A5C3-C7CA31FD4BA8
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7797b933a759afd0ccfb959672e5c595cefa21712f3488e61b4f99b8a57b0893
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123803"
---
# <a name="memory-management-strategies"></a>Strategie di gestione della memoria

Un gestore di memoria per Direct3D 12 può essere molto complicato rapidamente con tutti i diversi livelli di supporto, per schede UMA o discrete (non UMA) e con una notevole gamma di differenze di architettura tra le schede GPU.

La strategia consigliata per la gestione della memoria Direct3D 12, descritta in questa sezione, è "classificazione, budget e flusso".

-   [Tipi di risorsa](#resource-types)
-   [Budget di memoria](#memory-budget)
-   [Strategia di classificazione](#classification-strategy)
-   [Argomenti correlati](#related-topics)

## <a name="resource-types"></a>Tipi di risorsa

Il concetto di base di una "risorsa di cui è stato eseguito il commit" (la creazione di spazi di indirizzi virtuali e fisici inizializzati nella memoria fisica gestita) è stato definito a partire da Direct3D 9, anche se l'indirizzamento virtuale (VA) e l'indirizzamento fisico possono essere separati in Direct3D 12 per consentire all'app di gestire con attenzione la memoria fisica.

Oltre alle risorse di cui è stato eseguito il commit, il costrutto heap di Direct3D 12 abilita altri due tipi di risorsa: "placed" e "reserved". In Direct3D 11 una risorsa "riservata" era nota come "risorsa affiancata".

Le risorse riservate differiscono dalle risorse inserite in cui le risorse riservate hanno un proprio spazio di indirizzi virtuali GPU univoco. Ciò consente una grande allocazione di spazio va in anticipo e quindi consente il mapping delle pagine va va a determinate sezioni dell'heap in un secondo momento e l'applicazione riconfigura la disposizione in tempo reale. Lo spazio va è contiguo e può essere mappato a livello di dati.

La risorsa riservata può essere resa disponibile per fare riferimento alle aree nell'heap con chiamate API come [**UpdateTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings) e può essere resa residente dall'app aggiornando le tabelle di pagina in tempo reale. Quando un intervallo va viene mappato a NULL o a un heap non residente, tale parte della risorsa viene considerata non residente. Quando un intervallo va viene mappato a un heap residente, tale parte della risorsa viene considerata residente. Gli heap sono residenti al momento della creazione.

Le risorse posizionate sono una progettazione molto più semplice, essendo semplicemente un puntatore a una determinata area di un heap (ad esempio, un'area di 1 Mb per una trama in un heap da 5 Mb). Le barriere di aliasing consentono l'uso di risorse sovrapposte posizionate (vedere [**CreatePlacedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createplacedresource) e [**ResourceBarrier).**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)

Le risorse riservate non sono disponibili in tutto l'hardware Direct3D 12 e le risorse inserite sono un fallback ragionevole, anche se le risorse inserite devono essere contigue e non possono essere parzialmente residenti.

## <a name="memory-budget"></a>Budget di memoria

In Direct3D 12 quando si alloca un heap si crea l'aspetto della memoria fisica di una risorsa di cui è stato eseguito il commit. La scelta più esplicita del segmento di memoria è disponibile in Direct3D 12 (scegliendo tra video e memoria di sistema). Le schede UMA hanno un solo segmento di memoria, la memoria di sistema.

Le GPU non supportano l'errore di pagina, quindi gli sviluppatori devono essere consapevoli che non esercitino il commit, in particolare per i sistemi, ad esempio con solo 1 Gb di memoria di sistema. Se un'app esegue un over commit, il sistema operativo usa la pianificazione grosso modo granulare dei processi in base alla richiesta di memoria fisica. L'utilità di pianificazione blocca i processi in primo piano e ne esegue essenzialmente il page out, per eseguire il page-in un processo in background che vuole essere eseguito. La memoria fisica disponibile può variare notevolmente a seconda delle attività eseguite dall'utente in background, ad esempio l'esecuzione di un browser o la visione di un video.

L'API per il budget di memoria [**è QueryVideoMemoryInfo**](/windows/desktop/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-queryvideomemoryinfo). Per le schede discrete "local" è la memoria video, "non locale" è la memoria di sistema. Per le schede UMA non locali è sempre zero. Una domanda di progettazione è se il motore gestirà entrambi i budget o solo il budget locale. La gestione solo del budget locale è più semplice, ma presenta alcune avvertenze; Ad esempio, si supponga che sia presente un budget locale massimo di 1 Gb, quindi tutti gli heap provengono da tale 1 Gb in un sistema UMA e non si verifica alcun overflow nella memoria di sistema (ovviamente, perché non ne esiste nessuno).

Dal momento che Direct3D11 managed memory per le applicazioni, le risorse inutilizzate verrebbero essenzialmente impasse.

Scegliere le dimensioni delle risorse più appropriate. Valutare se le dimensioni di una risorsa sono appropriate per la situazione in cui l'applicazione è effettivamente in esecuzione. Alcuni utenti possono eseguire l'applicazione in una finestra o con una risoluzione dello schermo di 800x600.

## <a name="classification-strategy"></a>Strategia di classificazione

Per gestire le risorse in modo efficace negli scenari associati alla memoria, è consigliabile classificare le risorse negli elementi seguenti:



| Classificazione      | Esempio                                                                                         | Oggetti e funzionalità api                                                                                           | Note sulla gestione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Critico            | Interfaccia utente del gioco                                                                                          | Allocatore di comandi, code di comandi, heap delle query, risorse e heap delle risorse.                                      | Questi elementi devono essere in memoria non di cui è possibile eseguire il pageable/always committed.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Ridimensionato/Facoltativo    | Modelli e trame specifici del livello, catene di scambio, sky box, modelli di caratteri del giocatore in prima persona | Risorse e heap. Anche le risorse di cui è stato eseguito il commit, ma anche le risorse inserite e riservate, potrebbero funzionare correttamente.          | Integrare il budget di residenza della memoria negli algoritmi di rendering. Scegliere il livello di dettaglio disponibile appropriato e valutare di nuovo meno di una volta per frame. Le tecniche includono l'uso di risorse di dimensioni variabili e il ridimensionamento della catena di scambio.<br/>                                                                                                                                                                                                                                                                                                                                                 |
| Risorse usate di nuovo   | Buffer shadow, risorse di rendering posticipate, risorse di post-elaborazione, cache dei dati di illuminazione    | Risorse e heap. Sovrapposizione delle risorse posizionate su heap e barriere di aliasing.                                  | Riutilizzare risorse di grandi dimensioni o aree heap all'interno di un frame per ridurre i requisiti per l'intero frame. Usare la tecnica del riutilizzo della memoria all'interno dei frame. In Direct3D 11 le applicazioni potevano riutilizzare solo le risorse con lo stesso tipo e dimensioni potenzialmente sufficientemente grandi. Gli heap Direct3D 12 consentono di sovrapporre le risorse per un riutilizzo molto più semplice e maggiore.<br/>                                                                                                                                                                                                                              |
| Risorse di streaming | Terreno, trame e geometrie open world                                                        | Risorse e heap. Creazione a thread libero, thread della CPU in background ed elenchi di comandi di copia in background. | La residenza parziale, comunemente basata sulla visibilità (usando la valutazione view-frustum o basata sulla distanza) e la valutazione della residenza richiede ogni frame.<br/> La tecnica di uso di una gestione della residenza parziale per riquadro e del riutilizzo tra frame è disponibile quando l'adapter GPU supporta le risorse riservate all'interno degli heap.<br/> Usando la tecnica del re-uso della memoria tra frame, è possibile ottenere la residenza parziale delle sottorisorse, ma è meno ottimale. Le risorse inserite con heap devono consentire un riciclo più rapido, ma le risorse di cui è stato eseguito il commit possono essere usate come fallback.<br/> |



 

Più applicazioni gravitano alle risorse di streaming per la maggior parte del lavoro, più sfruttano le risorse posizionate e riservate, che massimizzano il ri-uso della memoria tra queste quattro classificazioni. Maggiore è il flusso delle applicazioni, maggiore è il budget e la priorità della larghezza di banda.

In genere con i motori di grafica Direct3D 12 è necessario rispettare un budget più diversificato e dinamico e farlo in modo più rigoroso rispetto al passato. Le applicazioni migliori individuano tutte e quattro le categorie nel budget assegnato al processo, ridimensionando il gioco dall'app per dispositivi mobili in background ai budget discreti a schermo intero. Molte applicazioni, tuttavia, probabilmente faticano iniziando con troppi tipi di categorie critiche di risorse. Direct3D 11 ha abilitato la creazione anonima delle risorse e occupa lo stato critico senza influire sulle prestazioni. Tuttavia, per Direct3D 12, gli sviluppatori devono cercare diligentemente le risorse create in modo casuale nel motore e nel middleware e rias assegnarle a una delle altre categorie.

Altre aree problematice sono i componenti middleware, i controlli utente e lo streaming all'interno dei frame. I componenti middleware non possono essere esposti a un budget né devono funzionare strettamente insieme. I componenti middleware potrebbero probabilmente esporre le funzionalità come tecniche di rendering; e l'applicazione può basarsi sull'esposizione di middleware e impostazioni del motore. Gli sviluppatori possono affidarsi a Direct3D 11 per eseguire il paging e ottenere la frequenza dei fotogrammi giusta. In alcuni casi, le applicazioni Direct3D 11 potrebbero avere paging del contenuto delle risorse in ogni frame; e ha comportato frequenze di fotogrammi accettabili per l'utente. La maggior parte dei motori consente di trasmettere solo i dati delle risorse come attività in background, in cui non ha alcun fallback normale al flusso intra-frame ad alta priorità. Chiedere ai motori di implementare che erose alcuni dei vantaggi di sovraccarico della CPU che stanno cercando passando a Direct3D 12. Gli sviluppatori di motori possono prendere in considerazione la possibilità di prendere in considerazione i frame in fasi per offrire più opportunità di riutilizzo delle risorse. e probabilmente collaborare con i fornitori di middleware per supportare le risorse e gli heap posizionati per il ri-uso della memoria all'interno dei frame.

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

 

