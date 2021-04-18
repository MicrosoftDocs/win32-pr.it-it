---
title: Windows Assessment Toolkit
description: Windows Assessment Toolkit
ms.assetid: 9D0A4F42-F027-4032-8297-045937BD2B6E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38d75aa02757acb54083e005d67a10e0fa42efec
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/20/2020
ms.locfileid: "106300667"
---
# <a name="windows-assessment-toolkit"></a>Windows Assessment Toolkit

## <a name="platforms"></a>Piattaforme

**Client** -Windows 7 \| Windows 8  

## <a name="description"></a>Descrizione

Windows Assessment Toolkit e Windows Performance Toolkit costituiscono Windows Assessment and Deployment Kit (ADK). Insieme forniscono una soluzione completa per la valutazione delle prestazioni complessive del computer e l'automazione della distribuzione del sistema operativo Windows nei nuovi computer.

Questo argomento è incentrato su **Assessment Toolkit**. I risultati della valutazione vengono usati per diagnosticare potenziali problemi, in modo che l'hardware e il software sviluppato siano entrambi reattivi e abbiano un impatto minimo sulla durata della batteria, sulle prestazioni di avvio e sull'ora di arresto. Sono disponibili le stesse valutazioni per partner OEM, partner ISV/IHV, appassionati e altri membri della community, per definire un Framework comune per misurare, confrontare ed esaminare gli aspetti della qualità.

Utilizzando gli strumenti di valutazione di Windows, è possibile misurare diversi aspetti delle prestazioni in un'ampia gamma di scenari, dal tempo di avvio alle prestazioni della batteria allo streaming video ad alta definizione. Le valutazioni possono identificare i potenziali problemi, il comportamento incoerente e evidenziare le aree da analizzare.

Nelle versioni precedenti di Windows erano disponibili più strumenti per misurare la qualità, tra cui Velocity test suite (VTS/VOS), base Quality Tools Suite (FQTS) e System Power and Performance Tools Suite (SPPTS). Assessment Toolkit combina le funzionalità di questi strumenti di diagnostica delle prestazioni in un set integrato di strumenti più facili da utilizzare e fornisce risultati più ampi e significativi.

Windows Assessment Toolkit ottimizza la soddisfazione dei clienti in base a quanto segue:

-   Che consente di valutare l'esperienza complessiva di Windows, il software e i driver aggiunti a livello di valore e le configurazioni hardware
-   Fornire dati di sistema dettagliati che consentono di identificare le cause principali dei problemi di qualità
-   Riduzione dei costi rivelando problemi durante lo sviluppo
-   Generazione di confronti di risultati da computer diversi o dallo stesso set di computer nel tempo mediante la creazione di grafici di confronto da più set di risultati
-   Generazione di commenti e suggerimenti in un formato standardizzato che è possibile usare per migliorare la qualità dei prodotti

È possibile raggiungere obiettivi aziendali importanti tramite il Toolkit Assessments:

-   **Misura & confrontare** : è possibile usare i dati per confrontare i componenti (software, driver o entrambi) con altri componenti simili per facilitare il processo decisionale, le raccomandazioni e il contrassegno del banco competitivo
-   **Migliorare la qualità** : è possibile lavorare in modo indipendente o con i partner partecipanti per compilare un componente (software, driver o entrambi) in base ai criteri di qualità predefiniti
-   **Rileva qualità**   È possibile creare un processo per tenere traccia in modo efficiente della qualità delle versioni dei componenti e rilevare regressioni dopo ogni iterazione

## <a name="usage-and-best-practices"></a>Utilizzo e procedure consigliate

Le valutazioni sono una combinazione di file XML e binari che inducono un set specifico di stati in un computer, misurano e registrano l'attività e conservano i risultati registrati. Un processo è una raccolta di una o più valutazioni e delle relative impostazioni, eseguite in una sola volta in un computer. La piattaforma di valutazione fornisce l'infrastruttura per l'esecuzione coerente e la visualizzazione di processi, valutazioni e risultati. I risultati includono spesso informazioni di diagnostica e correzione che consentono di determinare le aree che richiedono un'ulteriore analisi e un'azione correttiva. È possibile:

-   Eseguire valutazioni in un singolo computer o in una piccola raccolta di computer con **Windows Assessment console** (Windows AC) <dl> Questo scenario si riferisce agli utenti che desiderano visualizzare le caratteristiche delle prestazioni in una o più configurazioni di computer differenti. Windows AC è un'interfaccia utente grafica (GUI) utilizzata per raggruppare le valutazioni, creare un processo, creare un pacchetto di un processo, eseguire il processo e gestire i risultati del processo. I risultati includono spesso le azioni consigliate.  
    </dl>
-   Run assessments against multiple computers in a lab environment with **Windows Assessment Services** (Windows AS) <dl> Questo scenario è destinato principalmente agli utenti che desiderano eseguire una suite di valutazioni qualitative su una linea completa di computer desktop, portatili o tablet in un ambiente di sviluppo.  
    </dl>

Assessment Toolkit offre le funzionalità seguenti:

-   Una semplice interfaccia utente grafica (GUI) e valutazioni che possono essere usate per valutare un computer senza alcuna conoscenza tecnica approfondita del sistema
-   Risultati della valutazione, visualizzati nella console o nell'interfaccia utente, che spesso includono suggerimenti per migliorare il sistema
-   Possibilità di eseguire un processo preconfigurato con un solo clic
-   Impostazioni di valutazione predefinite in ogni valutazione del processo preconfigurato, in modo che sia possibile eseguire un processo su più computer e avere la certezza che i risultati siano confrontabili
-   Processi che possono essere personalizzati per includere le valutazioni da usare e le impostazioni che si vuole usare
-   Sintassi della riga di comando della piattaforma di valutazione per la creazione di script e l'automazione di processi
-   La possibilità di eseguire un processo, visualizzare i risultati, eseguire operazioni correttive per migliorare il sistema, quindi eseguire di nuovo il processo e confrontare i nuovi risultati affiancati con i risultati precedenti per vedere il modo in cui il sistema è migliorato

Assessment Toolkit viene in genere usato in questi scenari:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Scenario</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>&quot;Casella nera&quot;</td>
<td>Eseguire un processo predefinito ed esaminare i risultati per eventuali valori insoliti o indicazioni di problemi relativi a driver, utilizzo della memoria o altre aree a cui si rivolgono le valutazioni.</td>
</tr>
<tr class="even">
<td>Confronto dei risultati</td>
<td><ol>
<li>Eseguire una singola valutazione usando le impostazioni consigliate in qualsiasi computer in cui è in esecuzione un sistema operativo supportato.</li>
<li>Utilizzare Windows AC per creare il pacchetto del processo da eseguire in un altro computer.</li>
<li>Salvare i risultati in una condivisione in modo da poter confrontare i risultati.</li>
<li>Confrontare i risultati di qualsiasi computer Windows con quelli di qualsiasi altro sistema operativo supportato per identificare le differenze.</li>
</ol>
<br/></td>
</tr>
<tr class="odd">
<td>Pulisci computer</td>
<td>Eseguire valutazioni in un computer pulito che includa solo il sistema operativo per stabilire i risultati del sistema di base.</td>
</tr>
<tr class="even">
<td>Computer con componenti hardware o software aggiunti</td>
<td>Aggiungere nuovo hardware o software al computer pulito e quindi eseguire di nuovo le valutazioni per confrontare i risultati con i risultati puliti del computer.</td>
</tr>
<tr class="odd">
<td>Creazione di valutazioni</td>
<td>Usa le API pubbliche per sviluppare o estendere una valutazione o integrare valutazioni con gli strumenti e l'infrastruttura.</td>
</tr>
</tbody>
</table>



 

È possibile usare queste valutazioni:



| Valutazione                                   | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Pre-convalida della certificazione driver          | La valutazione della **pre-convalida della certificazione dei driver** verifica che i driver in un sistema operativo Windows in esecuzione siano idonei per il programma di certificazione Windows. I risultati includono consigli che consentono di risolvere i problemi rilevati dalla valutazione, ad esempio driver non firmati o firme scadute.                                                                                                                                                                                                                                                            |
| Verifica driver                          | La valutazione della **Verifica del driver** verifica che un'immagine Windows offline o un sistema operativo Windows in esecuzione contenga il set corretto di driver. I risultati includono suggerimenti che consentono di risolvere eventuali problemi rilevati dalla valutazione. Questi problemi possono includere driver mancanti, duplicati, obsoleti o non necessari.                                                                                                                                                                                                                                         |
| Gestione di file                                | La valutazione della **gestione dei file** fornisce un modo automatico per eseguire operazioni comuni sui file e acquisire le metriche. Le metriche misurano le durate e la velocità effettiva per facilitare la comprensione dell'esecuzione di un computer negli scenari di gestione dei file degli utenti finali. La valutazione della gestione dei file usa un set di carichi di lavoro per simulare un utente che copia, trasferisce, comprime, decomprime ed Elimina file e cartelle nei sistemi client.                                                                                                                                       |
| Gestione foto                               | La valutazione della **gestione delle foto** consente di misurare le prestazioni del computer e la durata della batteria simulando un utente finale che Visualizza e manipola le foto.                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Creazione di una scheda/avvio di Internet Explorer          | La valutazione **delle prestazioni di avvio di Internet Explorer** consente di identificare i componenti che possono influire sul tempo necessario per avviare Internet Explorer. La valutazione misura il tempo necessario per eseguire il rendering completo di una pagina vuota, incluso il tempo di caricamento del processo di IExplore.exe e gli intervalli di creazione di fotogrammi e di creazione di tabulazioni. Viene inoltre misurato l'effetto di tutte le estensioni, i componenti aggiuntivi e le barre degli strumenti installati nel sistema. Non misura le prestazioni di rete o di esplorazione.                                                                                         |
| Attivato/Disattivato                                       | La valutazione della **transizione on/off** misura le prestazioni degli scenari di prestazioni di avvio, standby e ibernazione di Windows 8.                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Prestazioni di esplorazione di Internet Explorer       | **Internet Explorer browsing performance** Assessment misura la qualità dell'esperienza di esplorazione in Internet Explorer e valuta le funzionalità hardware di CPU e grafica. Sono disponibili tre carichi di lavoro di esplorazione distinti per sottolineare il computer in diversi modi.                                                                                                                                                                                                                                                                                                  |
| Prestazioni di transcodifica dei supporti                | La valutazione **transcodifica video** consente di misurare il processo di modifica di un file video in un formato o Bitrate diverso. Questa valutazione esegue una serie di operazioni transcodificate con formati di file di input e di output comuni e risoluzioni                                                                                                                                                                                                                                                                                                                                           |
| Prestazioni dell'interfaccia utente di Windows                       | La valutazione delle **prestazioni dell'interfaccia** utente di Windows valuta le prestazioni di alcune esperienze di base all'interno dell'interfaccia utente di Windows. La valutazione misura la velocità di risposta e la qualità di rendering mentre la valutazione esercita i carichi di lavoro che simulano le attività dell'utente, ad esempio l'uso della ricerca e della transizione dall'ambiente delle app di Windows Store al desktop. I risultati della velocità di risposta sono misurati in millisecondi. I numeri bassi indicano che il computer è più veloce e più reattivo. Per il rendering, i risultati mostrano la frequenza dei fotogrammi e il numero di problemi che si verificano. |
| Footprint di memoria                             | È possibile usare la valutazione del **footprint di memoria** per confrontare quantitativamente un'immagine del sistema operativo di base rispetto a un'altra immagine del sistema operativo. È quindi possibile identificare i componenti specifici che influiscono sul footprint di memoria del sistema fisico. Questi componenti possono includere driver, app per componenti aggiuntivi, pacchetti software precaricati e programmi antivirus.                                                                                                                                                                                                           |
| Prime prestazioni di avvio                       | La **prima valutazione delle prestazioni di avvio** identifica i problemi che influiscono sul tempo necessario per l'avvio di Windows e la visualizzazione della schermata Start la prima volta che il computer viene avviato. I risultati consentono agli OEM di diagnosticare la causa dei ritardi e fornire consigli per migliorare l'esperienza.                                                                                                                                                                                                                                                                                      |
| Flussi multimediali                              | La valutazione **delle prestazioni di streaming media** consente di valutare le prestazioni di una configurazione del computer quando si esegue lo streaming di file multimediali tramite Internet Explorer. È possibile usare i risultati della valutazione per comprendere, confrontare e migliorare l'esperienza dei flussi multimediali.                                                                                                                                                                                                                                                                                                                 |
| WinSAT completa                         | **Windows System Assessment (WinSAT)** viene utilizzato per valutare e migliorare le prestazioni di un computer in diversi componenti di sistema, tra cui CPU, memoria, disco e grafica. I risultati della valutazione completa di WinSAT esprimono la funzionalità di configurazione hardware di un computer in numeri. I punteggi più alti indicano in genere che il computer valutato garantisce prestazioni migliori e più veloci rispetto a un computer con un punteggio più basso.                                                                                                                                                        |
| Efficienza energetica                            | Il processo di **efficienza energetica** fornisce un modo automatico per valutare la durata della batteria di un computer. Usando i carichi di lavoro, il processo di efficienza energetica esegue anche la diagnostica che valuta se i componenti di sistema usano l'alimentazione quando devono essere inattivi.                                                                                                                                                                                                                                                                                                               |
| Impostazioni di diagnostica mini               | L'opzione di **diagnostica mini** viene eseguita all'avvio della valutazione delle prestazioni di Internet Explorer, della valutazione della gestione dei file e della valutazione delle prestazioni di avvio (Windows 8). Selezionando questa opzione all'interno delle valutazioni che offrono l'opzione di diagnostica mini, vengono generate metriche che consentono di valutare l'impatto delle operazioni di mini su diversi scenari di valutazione.                                                                                                                                                                                  |
| Prestazioni e qualità di Windows Media Player | **Windows Media Player Performance and Quality** Assessment avvia WMP e riproduce più clip multimediali una dopo l'altra per acquisire le metriche relative a prestazioni e qualità correlate alla riproduzione multimediale.                                                                                                                                                                                                                                                                                                                                                                          |



 

Altri strumenti, ad esempio Windows Performance Toolkit, sono inclusi in ADK. Questi strumenti forniscono informazioni approfondite che consentono di analizzare e tracciare le prestazioni del sistema e delle app. Per altre informazioni, vedere la sezione risorse di seguito.

## <a name="resources"></a>Risorse

**Video**

-   [Video su Channel9 BUILD ADK](https://channel9.msdn.com/Events/BUILD/BUILD2011?sort=status&direction=asc&term=&t=assessment+and+deployment+kit)

  
**Documentazione**

-   [Windows Assessment and Deployment Kit](/previous-versions/windows/hh825420(v=win.10))
-   [Riferimento tecnico per Windows Assessment Toolkit](/previous-versions/windows/it-pro/windows-8.1-and-8/hh825508(v=win.10))
-   [Motore esecuzione valutazioni](/previous-versions/windows/desktop/axe/axe-access-portal)
-   [Analisi delle prestazioni di Windows](https://msdn.microsoft.com/performance/default.aspx)

  


 

