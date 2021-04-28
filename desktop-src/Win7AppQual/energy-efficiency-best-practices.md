---
description: Procedure consigliate per l'efficienza energetica
ms.assetid: 355abd0e-928e-442e-a724-855d9dd946fc
title: Procedure consigliate per l'efficienza energetica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67d9a348b9df49531358de2db50acc0936622c36
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088389"
---
# <a name="best-practices-for-energy-efficiency"></a>Procedure consigliate per l'efficienza energetica

## <a name="platform"></a>Piattaforma

 **Client** - Windows XP \| Windows Vista Windows \| 7  

## <a name="description"></a>Descrizione

I portatili basati su Windows devono soddisfare i requisiti normativi per l'efficienza energetica, ad esempio quelli del programma Stati Uniti Environmental Protection Agency (EPA) Energy Star. Inoltre, i sondaggi hanno dimostrato che una durata della batteria più lunga continua a essere ciò che i consumatori vogliono e hanno più bisogno nei portatili. Per soddisfare le esigenze dei consumatori, i portatili Windows devono continuare ad avanzare nelle aree seguenti:

-   Efficienza energetica in tutti gli scenari di utilizzo, inclusi carichi di lavoro inattivi, produttività, riproduzione di DVD e supporti e benchmark di settore
-   Durata della batteria dei PC mobili: per le piattaforme hardware e per Windows

La piattaforma Windows è altamente affidabile e consente prestazioni veloci in modalità on-and-off. Tuttavia, le estensioni fornite con sistemi pc mobili, ad esempio servizi, applet della barra delle applicazioni, driver e altro software, possono influire in modo significativo su prestazioni, affidabilità ed efficienza energetica.

L'efficienza energetica è un problema complesso, con fattori interessati e che interessano tutti gli elementi dell'ecosistema di PC. Piccoli miglioramenti in più scenari possono migliorare l'efficienza energetica, ma una singola funzionalità di applicazione, dispositivo o sistema con prestazioni ridotte può aumentare significativamente il consumo di energia.

L'hardware e i dispositivi sono alla base dell'efficienza energetica. Tuttavia, anche il software dell'applicazione e del servizio deve essere efficiente per consentire al sistema di ottenere una durata ottimale della batteria. Ogni componente software nel sistema, inclusi il sistema operativo e le applicazioni e i servizi a valore aggiunto, deve essere conforme alle linee guida di base sull'efficienza. Un'unica applicazione o servizio che comporta un errore può eliminare qualsiasi miglioramento dell'efficienza energetica ottenuto dal processore, i dispositivi o l'hardware della piattaforma più recente. Per informazioni più dettagliate sulla durata della batteria e sull'efficienza energetica, vedere [la Guida alle](https://docs.microsoft.com/windows-hardware/design/component-guidelines/battery-and-charging#)soluzioni per la durata della batteria .

I principali problemi e componenti che influiscono sulla durata della batteria in un PC mobile sono:

**Caratteristiche della batteria**

-   Dimensioni, tipo e qualità della capacità della batteria influiscono sulla durata della batteria
-   Maggiore è la batteria, maggiore è l'alimentatore
-   Le batterie più grandi sono più costose e pesanti; gli utenti preferiscono sistemi più leggeri

**Componenti hardware**

-   Frequenza e profondità a cui l'hardware può immettere stati di alimentazione inferiori
-   Supporto hardware degli stati di alimentazione inferiori
-   Ottimizzazione dei driver per l'efficienza energetica

**Risparmio energia diretto dal sistema operativo**

-   Efficienza del codice Windows in condizioni di carico e inattive
-   Livello di collaborazione di tutti i componenti con il risparmio energia diretto da Windows
-   Configurazione corretta del sistema operativo per ottimizzare il risparmio energia tramite le impostazioni dei criteri di risparmio energia

**Software e servizi dell'applicazione**

-   Efficienza di applicazioni, driver e servizi in condizioni di carico e inattive
-   Livello di collaborazione delle applicazioni con la gestione del risparmio energia diretta da Windows
-   Capacità software del sistema o dei dispositivi di entrare in stati di inattività a basso consumo

Un'unica applicazione o componente del servizio può impedire a un sistema di realizzare una durata ottimale della batteria. Anche se Windows offre molte opzioni di configurazione del risparmio energia, le impostazioni dei criteri di risparmio energia o software preinstallate in molti sistemi non sono ottimizzate per la piattaforma hardware host.

Un metodo comune per valutare l'impatto della durata della batteria del software preinstallato è confrontare il consumo di energia del sistema con un'installazione pulita di Windows rispetto a un'installazione di Windows che include software e servizi a valore aggiunto. Anche se un'installazione pulita non rappresenta la piattaforma tipica che gli OEM forniscono ai clienti, il confronto del consumo di energia può fornire informazioni dettagliate sull'efficienza energetica del software preinstallato.

## <a name="best-practices"></a>Procedure consigliate

Per assicurarsi che l'applicazione sia ottimizzata nelle piattaforme Windows, seguire queste procedure consigliate quando si progettano applicazioni o servizi:

-   **Evitare l'uso di timer periodici ad alta risoluzione**

<dl> Uso di timer periodici ad alta risoluzione (<10 ms) reduces the efficiency of processor power-management technologies.  
</dl>

-   **Investire nelle ottimizzazioni delle prestazioni**

<dl> Ogni ottimizzazione delle prestazioni è un'ottimizzazione della durata della batteria. Le riduzioni delle risorse necessarie, ad esempio l'uso di meno tempo del processore o l'invio in batch/il clustering delle operazioni di lettura del disco, consentono all'hardware di sistema di diventare inattivo e di entrare in modalità a basso consumo.  
</dl>

-   **Adatta ai criteri di risparmio energia dell'utente**

<dl> Windows Vista e versioni successive rendono più semplice per l'utente scegliere il risparmio di energia complessivo o il comportamento delle prestazioni del sistema. L'applicazione deve rispondere alle modifiche dei criteri di risparmio energia e ridurre l'utilizzo delle risorse o aumentare le prestazioni di conseguenza. Ad esempio, un'applicazione deve disabilitare l'attività in background, ad esempio l'indicizzazione o l'analisi del sistema, quando l'utente ha selezionato una combinazione per il risparmio di energia.  
</dl>

-   **Ridurre l'utilizzo delle risorse quando il sistema è alimentato a batteria**

<dl> L'applicazione deve ridurre l'utilizzo delle risorse, ad esempio la frequenza di aggiornamento in background, quando il sistema è alimentato a batteria.  
</dl>

-   **Non eseguire il rendering sulla visualizzazione quando è disattivata**

<dl> La visualizzazione del sistema potrebbe essere disattivata per risparmiare energia. L'applicazione non deve eseguire il rendering della grafica non necessario quando lo schermo è spento, perché ciò spreca risorse di sistema e alimentazione.  
</dl>

-   **Evitare il polling e la rotazione in cicli ristretti**

<dl> Un utilizzo elevato del processore riduce l'efficacia delle tecnologie di risparmio energia del processore, ad esempio gli stati di inattività del processore e gli stati di prestazioni del processore.  
</dl>

-   **Non impedire al sistema di disattivare la visualizzazione o la disattivazione per la sospensione**

<dl> L'applicazione deve eseguire richieste di alimentazione concise con l'API SetThreadExecutionState. Il sistema deve effettuare queste richieste solo quando le operazioni critiche devono ritardare l'accensione dello schermo o l'immissione automatica della sospensione.  
</dl>

-   **Rispondere agli eventi comuni di risparmio energia**

<dl> L'applicazione deve registrarsi per e rispondere agli eventi di risparmio energia comuni, ad esempio le modifiche all'alimentazione del sistema e le notifiche di accensione e accensione per lo schermo.  
</dl>

-   **Non abilitare la registrazione di debug per impostazione predefinita. usare Event Tracing for Windows invece**

<dl> La registrazione di debug periodica può impedire lo spin-down del disco.  
</dl>

## <a name="links-to-other-resources"></a>Collegamenti ad altre risorse

-   [Guida alle soluzioni per la durata della batteria](https://docs.microsoft.com/windows-hardware/design/component-guidelines/battery-and-charging#)
-   [Portale per l'efficienza energetica](https://www.microsoft.com/whdc/system/pnppwr/mobilepwr.mspx)
-   [Windows Performance Toolkit](https://www.microsoft.com/whdc/system/sysperf/perftools.mspx)

 

 



