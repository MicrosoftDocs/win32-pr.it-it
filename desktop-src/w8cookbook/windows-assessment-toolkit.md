---
title: Windows Assessment Toolkit
description: Windows Assessment Toolkit
ms.assetid: 9D0A4F42-F027-4032-8297-045937BD2B6E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d6eff172a59a7f0ee00f85a0cd8f237387aaa78
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482677"
---
# <a name="windows-assessment-toolkit"></a>Windows Assessment Toolkit

## <a name="platforms"></a>Piattaforme

**Client** - Windows 7 \| Windows 8  

## <a name="description"></a>Descrizione

Il Windows Assessment Toolkit e Windows Performance Toolkit costituiscono Windows Assessment and Deployment Kit (ADK). Insieme offrono una soluzione completa per valutare le prestazioni complessive del computer e automatizzare la distribuzione del Windows sistema operativo in nuovi computer.

Questo argomento è in particolare in **Toolkit**. I risultati della valutazione vengono usati per diagnosticare potenziali problemi, in modo che l'hardware e il software sviluppato siano reattivi e hanno un impatto minimo sulla durata della batteria, sulle prestazioni di avvio e sul tempo di arresto. Le stesse valutazioni sono disponibili per partner OEM, partner ISV/IHV, appassionati e altri membri della community, per stabilire un framework comune per misurare, confrontare e rivedere gli aspetti di qualità.

Usando gli strumenti di valutazione Windows, è possibile misurare diversi aspetti delle prestazioni in diversi scenari, dal tempo di avvio alle prestazioni di durata della batteria allo streaming video ad alta definizione. Le valutazioni possono identificare potenziali problemi, comportamenti incoerenti ed evidenziare le aree da analizzare.

Nelle versioni Windows precedenti erano disponibili più strumenti per misurare la qualità, tra cui Velocità Test Suite (VTS/VOS), Fundamental Quality Tools Suite (FQTS) e System Power and Performance Tools Suite (SPPTS). L'Toolkit di valutazione combina le funzionalità di questi strumenti di diagnostica delle prestazioni in un set integrato di strumenti più facile da usare e offre risultati più ampi e significativi.

Il Windows Assessment Toolkit ottimizza la soddisfazione dei consumatori tramite:

-   Aiutare a valutare l'esperienza complessiva di Windows, software e driver a valore aggiunto e configurazioni hardware
-   Fornire dati di sistema dettagliati che consentono di identificare le cause principali dei problemi di qualità
-   Riduzione dei costi rivelando i problemi durante lo sviluppo
-   Generazione di confronti di risultati da computer diversi o dallo stesso set di computer nel tempo creando grafici di confronto da più set di risultati
-   Generazione di commenti e suggerimenti in un formato standardizzato che è possibile usare per migliorare la qualità dei prodotti

È possibile raggiungere obiettivi aziendali importanti usando le Toolkit:

-   **Confronto &** dati: è possibile usare i dati per confrontare i componenti (software, driver o entrambi) con altri componenti simili per facilitare il processo decisionale, le raccomandazioni e il contrassegno del banco competitivo
-   **Migliorare la** qualità: è possibile lavorare in modo indipendente o con i partner coinvolti per creare un componente (software, driver o entrambi) in base a criteri di qualità predefiniti
-   **Tenere traccia della qualità**   È possibile creare un processo per tenere traccia in modo efficiente della qualità delle versioni dei componenti e rilevare le regressioni dopo ogni iterazione

## <a name="usage-and-best-practices"></a>Utilizzo e procedure consigliate

Le valutazioni sono una combinazione di file XML e binari che provocano un set specifico di stati in un computer, misurano e registrano l'attività e mantengono i risultati registrati. Un processo è una raccolta di una o più valutazioni e delle relative impostazioni, eseguite contemporaneamente in un computer. La piattaforma di valutazione fornisce l'infrastruttura per l'esecuzione e la visualizzazione coerente di processi, valutazioni e risultati. I risultati includono spesso informazioni di diagnostica e correzione che consentono di determinare le aree che necessitano di ulteriori indagini e azioni correttive. È possibile:

-   Eseguire valutazioni in un singolo computer o in una piccola raccolta di computer con Windows **Assessment Console** (Windows AC) <dl> Questo scenario è per gli utenti che vogliono visualizzare le caratteristiche delle prestazioni in una o più configurazioni di computer diverse. Windows Ac è un'interfaccia utente grafica (GUI) usata per raggruppare le valutazioni, creare un processo, creare un pacchetto di un processo, eseguirne il processo e gestirne i risultati. I risultati includono spesso le azioni consigliate.  
    </dl>
-   Run assessments against multiple computers in a lab environment with **Windows Assessment Services** (Windows AS) <dl> Questo scenario è destinato principalmente agli utenti che vogliono eseguire una suite di valutazioni qualitative su una linea completa di computer desktop, portatili o tablet in un ambiente di sviluppo.  
    </dl>

L'Toolkit assessment offre queste funzionalità:

-   Interfaccia utente grafica semplice e valutazioni che possono essere usate per valutare un computer senza conoscenze tecniche approfondite del sistema
-   Risultati della valutazione, visualizzati nella console o nell'interfaccia utente, che spesso includono raccomandazioni per migliorare il sistema
-   Possibilità di eseguire un processo preconfigurato con un solo clic
-   Impostazioni di valutazione predefinite in ogni valutazione del processo preconfigurata in modo da poter eseguire un processo in più computer e avere la certezza che i risultati siano confrontabili
-   Processi che possono essere personalizzati per includere le valutazioni da usare e le impostazioni da usare
-   Sintassi della riga di comando di Assessment Platform per la creazione di script e l'automazione dei processi
-   Possibilità di eseguire un processo, visualizzare i risultati, eseguire passaggi di correzione per migliorare il sistema, quindi eseguire di nuovo il processo e confrontare i nuovi risultati side-by-side con i risultati precedenti per vedere come il sistema è migliorato

L'Toolkit valutazione viene in genere usata in questi scenari:




| Scenario | Descrizione | 
|----------|-------------|
| "Black box" | Eseguire un processo predefinito ed esaminare i risultati per eventuali valori insoliti o indicazioni di problemi relativi ai driver, all'utilizzo della memoria o ad altre aree che le valutazioni affrontano. | 
| Confronto dei risultati | <ol><li>Eseguire una singola valutazione usando le impostazioni consigliate in qualsiasi computer che esegue un sistema operativo supportato.</li><li>Usare il Windows per creare un pacchetto del processo da eseguire in un altro computer.</li><li>Salvare i risultati in una condivisione in modo da poter confrontare i risultati.</li><li>Confrontare i risultati di qualsiasi Windows computer con quelli di qualsiasi altro sistema operativo supportato per identificare le differenze.</li></ol><br /> | 
| Pulire il computer | Eseguire valutazioni in un computer pulito che include solo il sistema operativo per stabilire i risultati del sistema di base. | 
| Computer con componenti hardware o software aggiunti | Aggiungere nuovo hardware o software al sistema di computer pulito e quindi eseguire nuovamente le valutazioni per confrontare i risultati con i risultati del computer pulito. | 
| Creazione di valutazioni | Usare le API pubbliche per sviluppare o estendere una valutazione o integrare le valutazioni con gli strumenti e l'infrastruttura. | 




 

È possibile usare queste valutazioni:



| Valutazione                                   | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Pre-convalida della certificazione driver          | La **valutazione della pre-convalida** della certificazione driver verifica che i driver in un sistema operativo Windows in esecuzione si qualificano per il programma Windows certificazione. I risultati includono raccomandazioni che consentono di risolvere i problemi rilevati dalla valutazione, ad esempio driver non firmati o firme scadute.                                                                                                                                                                                                                                                            |
| Verifica del driver                          | La **valutazione verifica** driver verifica che un'immagine Windows offline o un sistema operativo Windows in esecuzione contenga il set corretto di driver. I risultati includono raccomandazioni che consentono di risolvere eventuali problemi rilevati dalla valutazione. Questi problemi possono includere driver mancanti, duplicati, meno recenti o non necessari.                                                                                                                                                                                                                                         |
| Gestione di file                                | La **valutazione Gestione file** offre un modo automatizzato per eseguire operazioni di file comuni e acquisire metriche. Le metriche misurano le durate e la velocità effettiva per comprendere le prestazioni di un computer negli scenari di gestione dei file degli utenti finali. La valutazione Gestione file usa un set di carichi di lavoro per simulare un utente che copia, sposta, comprime, decomprime ed elimina file e cartelle nei sistemi client.                                                                                                                                       |
| Gestione delle foto                               | La **valutazione Gestione foto misura** le prestazioni del computer e la durata della batteria simulando un utente finale che visualizza e modifica le foto.                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Internet Explorer avvio/creazione di schede          | La **Internet Explorer delle prestazioni di** avvio consente di identificare i componenti che possono influire sul tempo necessario per Internet Explorer. La valutazione misura il tempo necessario per eseguire il rendering completo di una pagina vuota, incluso il tempo di caricamento del processo di IExplore.exe e gli intervalli di creazione di frame e creazione di schede. Misura anche l'effetto di tutte le estensioni, i componenti aggiuntivi e le barre degli strumenti installate nel sistema. Non misura le prestazioni di rete o di esplorazione.                                                                                         |
| Attivato/Disattivato                                       | La **valutazione della transizione on/off** misura le prestazioni di Windows 8 di prestazioni di avvio, standby e ibernazione.                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Internet Explorer prestazioni di esplorazione       | La **Internet Explorer delle** prestazioni di esplorazione misura la qualità dell'esperienza di esplorazione in Internet Explorer e valuta le funzionalità hardware di CPU e grafica. Vengono forniti tre carichi di lavoro di esplorazione separati per stressare il computer in vari modi.                                                                                                                                                                                                                                                                                                  |
| Prestazioni di transcoding multimediale                | La **valutazione Transcode Video** misura il processo di modifica di un file video in un formato o in una velocità in bit diversa. Questa valutazione esegue una serie di operazioni di transcodifica con formati e risoluzioni di file di input e output comuni                                                                                                                                                                                                                                                                                                                                           |
| Windows Prestazioni dell'interfaccia utente                       | La **Windows delle prestazioni dell'interfaccia** utente valuta le prestazioni di alcune esperienze di base all'interno dell Windows'interfaccia utente. La valutazione misura la velocità di risposta e la qualità del rendering mentre la valutazione esercita i carichi di lavoro che simulano le attività degli utenti, ad esempio l'uso della ricerca e la transizione dall'ambiente dell'app di Windows Store al desktop. I risultati della velocità di risposta vengono misurati in millisecondi. I numeri bassi significano che il computer è più veloce e reattivo. Per il rendering, i risultati mostrano la frequenza dei fotogrammi e il numero di errori che si verificano. |
| Footprint di memoria                             | È possibile usare la valutazione **del footprint di** memoria per confrontare quantitativamente un'immagine del sistema operativo di base con un'altra immagine del sistema operativo. È quindi possibile identificare i componenti specifici che influiscono sul footprint di memoria del sistema fisico. Questi componenti possono includere driver, app per componenti aggiuntivi, pacchetti software precaricati e programmi antivirus.                                                                                                                                                                                                           |
| Prestazioni del primo avvio                       | La **valutazione delle prestazioni primo** avvio identifica i problemi che influiscono sul tempo necessario Windows avvio e visualizzano il schermata Start al primo avvio del computer. I risultati consentono agli OEM di diagnosticare cosa causa ritardi e forniscono raccomandazioni per migliorare l'esperienza.                                                                                                                                                                                                                                                                                      |
| Streaming multimediale                              | La **valutazione delle prestazioni dei supporti** di streaming consente di valutare le prestazioni di una configurazione del computer quando si esegue lo streaming dei supporti Internet Explorer. È possibile usare i risultati della valutazione per comprendere, confrontare e migliorare l'esperienza dei supporti di streaming.                                                                                                                                                                                                                                                                                                                 |
| WinSAT completo                         | Il **Windows System Assessment (WinSAT)** viene usato per valutare e migliorare le prestazioni di un computer in diversi componenti di sistema, tra cui CPU, memoria, disco e grafica. I risultati della valutazione completa di WinSAT esprimono la funzionalità della configurazione hardware di un computer in numeri. I punteggi più elevati in genere significano che il computer valutato offre prestazioni migliori e più veloci rispetto a un computer con un punteggio inferiore.                                                                                                                                                        |
| Efficienza energetica                            | Il **processo efficienza** energetica offre un modo automatizzato per valutare la durata della batteria di un computer. Usando i carichi di lavoro, il processo efficienza energetica esegue anche la diagnostica che valuta se i componenti di sistema usano alimentazione quando devono essere inattivi.                                                                                                                                                                                                                                                                                                               |
| Diagnostica MiniFilter Impostazioni               | **L'opzione MiniFilter Diagnostic** viene eseguita all'interno Internet Explorer valutazione delle prestazioni di avvio, della valutazione gestione file e della valutazione delle prestazioni di avvio (Windows 8). La selezione di questa opzione nelle valutazioni che offrono l'opzione di diagnostica MiniFilter produce metriche che consentono di valutare l'impatto delle operazioni MiniFilter in vari scenari di valutazione.                                                                                                                                                                                  |
| Windows Media Player Prestazioni e qualità | La **valutazione Windows Media Player** prestazioni e qualità avvia WMP e riproduce più clip multimediali una dopo l'altra per acquisire metriche di prestazioni e qualità correlate alla riproduzione multimediale.                                                                                                                                                                                                                                                                                                                                                                          |



 

Altri strumenti, ad esempio Windows prestazioni Toolkit, sono inclusi in ADK. Questi strumenti forniscono informazioni approfondite che consentono di analizzare e tracciare le prestazioni del sistema e delle app. Per altre informazioni, vedere la sezione Risorse riportata di seguito.

## <a name="resources"></a>Risorse

**Dei video:**

-   [Video di Channel9 BUILD ADK](https://channel9.msdn.com/Events/BUILD/BUILD2011?sort=status&direction=asc&term=&t=assessment+and+deployment+kit)

  
**Documentazione:**

-   [Windows Assessment and Deployment Kit](/previous-versions/windows/hh825420(v=win.10))
-   [Windows Riferimento tecnico Toolkit valutazione](/previous-versions/windows/it-pro/windows-8.1-and-8/hh825508(v=win.10))
-   [Motore esecuzione valutazioni](/previous-versions/windows/desktop/axe/axe-access-portal)
-   [Windows Analisi delle prestazioni](https://msdn.microsoft.com/performance/default.aspx)

  


 

