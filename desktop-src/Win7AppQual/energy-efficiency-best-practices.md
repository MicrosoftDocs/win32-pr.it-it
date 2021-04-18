---
description: .
ms.assetid: 355abd0e-928e-442e-a724-855d9dd946fc
title: Procedure consigliate per l'efficienza energetica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04a9980d199e2d95c6dbd01c642a1f00f45e584c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318883"
---
# <a name="best-practices-for-energy-efficiency"></a>Procedure consigliate per l'efficienza energetica

## <a name="platform"></a>Piattaforma

 **Client** – Windows XP Windows \| Vista Windows \| 7  

## <a name="description"></a>Descrizione

I portatili basati su Windows devono soddisfare i requisiti normativi di efficienza energetica, ad esempio quelli del programma Stati Uniti Environmental Protection Agency (EPA) Energy Star. Inoltre, i sondaggi hanno dimostrato che la durata della batteria più lunga continua a essere quello che i consumatori desiderano e necessitano di computer portatili. Per soddisfare le esigenze degli utenti, i computer portatili Windows devono sempre progredire nelle seguenti aree:

-   Efficienza energetica in tutti gli scenari di utilizzo, tra cui inattività, carichi di lavoro di produttività, riproduzione di DVD e supporti e benchmark di settore
-   Durata della batteria dei PC portatili: per le piattaforme hardware e per Windows

La piattaforma Windows è altamente affidabile e consente di ottenere prestazioni rapide. Tuttavia, le estensioni fornite con i sistemi per PC mobili, ad esempio servizi, applet della barra di sistema, driver e altro software, possono influenzare significativamente le prestazioni, l'affidabilità e l'efficienza energetica.

L'efficienza energetica è un problema complesso, con i fattori interessati da e che interessano tutti gli elementi dell'ecosistema di PC. I miglioramenti apportati a più scenari possono migliorare l'efficienza energetica, ma una singola funzionalità dell'applicazione, del dispositivo o del sistema con prestazioni scarse può aumentare in modo significativo il consumo di energia.

L'hardware e i dispositivi costituiscono la base per l'efficienza energetica. Tuttavia, il software per le applicazioni e i servizi deve essere efficiente anche per consentire al sistema di ottenere una durata ottimale della batteria. Ogni componente software del sistema, inclusi il sistema operativo e le applicazioni e i servizi a valore aggiunto, deve essere conforme alle linee guida di base sull'efficienza. Una singola applicazione o un servizio che funziona in modo non corretto può eliminare qualsiasi miglioramento dell'efficienza energetica per il processore, i dispositivi o l'hardware della piattaforma più recenti. Per informazioni più dettagliate sulla durata della batteria e sull'efficienza energetica, vedere la [Guida alle soluzioni](https://docs.microsoft.com/windows-hardware/design/component-guidelines/battery-and-charging#)per la durata della batteria.

I principali problemi e componenti che influiscono sulla durata della batteria in un computer portatile sono:

**Caratteristiche della batteria**

-   Le dimensioni, il tipo e la qualità della capacità della batteria influiscono sulla durata della batteria
-   Maggiore è la batteria, maggiore è l'alimentatore
-   Le batterie più grandi sono più costose e più pesanti; utenti che preferiscono sistemi più leggeri

**Componenti hardware**

-   Frequenza e profondità in cui l'hardware può accedere a stati di risparmio energia inferiori
-   Supporto hardware di Stati di alimentazione inferiore
-   Ottimizzazione driver per l'efficienza energetica

**Sistema operativo: risparmio energia guidato**

-   Efficienza del codice di Windows mentre è in corso un caricamento rispetto al tempo di inattività
-   Livello di collaborazione di tutti i componenti con il risparmio di energia guidato da Windows
-   Configurazione corretta del sistema operativo da ottimizzare per il risparmio energia tramite le impostazioni di criteri di risparmio energia

**Software e servizi dell'applicazione**

-   Efficienza di applicazioni, driver e servizi, in condizioni di carico e di inattività
-   Livello di collaborazione delle applicazioni con Windows: gestione del risparmio energia
-   Limite software del sistema o dei dispositivi da immettere in Stati di inattività a basso consumo

Un singolo componente dell'applicazione o del servizio può impedire a un sistema di realizzare una durata ottimale della batteria. Sebbene Windows fornisca molte opzioni di configurazione dell'alimentazione, il software preinstallato o le impostazioni dei criteri di risparmio energia in molti sistemi non sono ottimizzate per la piattaforma hardware host.

Un metodo comune per valutare la durata della batteria del software preinstallato consiste nel confrontare il consumo di energia del sistema con un'installazione pulita di Windows rispetto a un'installazione di Windows che includa software e servizi a valore aggiunto. Sebbene un'installazione pulita non rappresenti la piattaforma tipica distribuita dagli OEM ai clienti, il confronto del consumo di energia può fornire informazioni dettagliate sull'efficienza energetica del software preinstallato.

## <a name="best-practices"></a>Procedure consigliate

Per assicurarsi che l'applicazione sia ottimizzata sulle piattaforme Windows, seguire queste procedure consigliate per la progettazione di applicazioni o servizi:

-   **Evitare l'uso di timer periodici a risoluzione elevata**

<dl> Uso di timer periodici a risoluzione elevata (<10 ms) reduces the efficiency of processor power-management technologies.  
</dl>

-   **Investire nelle ottimizzazioni delle prestazioni**

<dl> Ogni ottimizzazione delle prestazioni è un'ottimizzazione della durata della batteria. Le riduzioni delle risorse necessarie, ad esempio l'utilizzo di un minor tempo del processore o l'invio in batch/clustering di letture disco, consentono all'hardware del sistema di diventare inattivo e di immettere le modalità a basso consumo.  
</dl>

-   **Modificare i criteri di risparmio energia utente**

<dl> Windows Vista e versioni successive rendono più semplice per l'utente la scelta del comportamento complessivo di risparmio energetico o delle prestazioni del sistema. L'applicazione deve rispondere alle modifiche apportate ai criteri di risparmio energia e ridurre l'utilizzo delle risorse o migliorare le prestazioni di conseguenza. Ad esempio, un'applicazione deve disabilitare l'attività in background, ad esempio l'indicizzazione o l'analisi del sistema, quando l'utente ha selezionato una combinazione per il risparmio di energia.  
</dl>

-   **Ridurre l'utilizzo delle risorse quando il sistema è alimentato a batteria**

<dl> L'applicazione dovrebbe ridurre l'utilizzo delle risorse, ad esempio la frequenza di aggiornamento in background, quando il sistema è alimentato a batteria.  
</dl>

-   **Non eseguire il rendering sullo schermo quando è disattivato**

<dl> La visualizzazione del sistema potrebbe essere disattivata per risparmiare energia. Quando la visualizzazione è spenta, l'applicazione non deve eseguire il rendering di grafica non necessario, perché questo spreco di risorse di sistema e di potenza.  
</dl>

-   **Evitare il polling e la rotazione in cicli rigidi**

<dl> Un utilizzo intensivo del processore riduce l'efficacia delle tecnologie di risparmio energia del processore, ad esempio Stati di inattività del processore e Stati delle prestazioni del processore.  
</dl>

-   **Non impedire al sistema di spegnere lo schermo o di dormire al minimo**

<dl> L'applicazione deve eseguire richieste di alimentazione giudiziose con l'API SetThreadExecutionState. Il sistema deve effettuare queste richieste solo quando le operazioni critiche devono ritardare la disattivazione dello schermo o l'immissione automatica della sospensione da parte del sistema.  
</dl>

-   **Rispondere a eventi di risparmio energia comuni**

<dl> L'applicazione deve registrarsi e rispondere a eventi di gestione del risparmio energia comuni, ad esempio le modifiche al risparmio energia del sistema e le notifiche di accensione e spegnimento per la visualizzazione.  
</dl>

-   **Non abilitare la registrazione debug per impostazione predefinita; usare invece Event Tracing for Windows**

<dl> La registrazione periodica del debug può impedire la rotazione del disco.  
</dl>

## <a name="links-to-other-resources"></a>Collegamenti ad altre risorse

-   [Guida alle soluzioni per la durata della batteria](https://docs.microsoft.com/windows-hardware/design/component-guidelines/battery-and-charging#)
-   [Portale di efficienza energetica](https://www.microsoft.com/whdc/system/pnppwr/mobilepwr.mspx)
-   [Windows Performance Toolkit](https://www.microsoft.com/whdc/system/sysperf/perftools.mspx)

 

 



