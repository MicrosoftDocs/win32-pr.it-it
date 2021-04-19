---
description: .
ms.assetid: 872c2a33-327e-41a8-81db-905c46673f13
title: Procedure consigliate per le prestazioni on/off
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fda45cb1ec7fb66b8afdcdebab7c92bdb071a79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318891"
---
# <a name="best-practices-for-onoff-performance"></a>Procedure consigliate per le prestazioni on/off

## <a name="platform"></a>Piattaforma

**Client-** Windows Vista \| Windows 7  
**Server-** Windows Server 2008 \| Windows server 2008 R2  

## <a name="description"></a>Descrizione

Gli Stati di alimentazione del sistema (o gli Stati), come definito nella specifica di Advanced computer Power Interface (ACPI), sono comunemente chiamati stati on/off, perché la transizione dello stato S più comune è un computer che si sta attivando e disattivando. Le diverse transizioni di stato on/off in un sistema che esegue Windows Vista o Windows 7 sono avvio, sospensione (ACPI S3), ibernazione (ACPI S4) e Shutdown.

Le prestazioni ottimali durante queste transizioni on/off non solo migliorano la qualità percepita di un computer, ma influiscono notevolmente sui modelli di utilizzo del computer e sull'affidabilità del sistema. I clienti possono essere frustrati dai sistemi che imprendono troppo tempo per l'avvio o l'arresto. I sistemi mobili con lunghe transizioni di sospensione e ibernazione possono esaurire inutilmente la durata della batteria. Tempi di arresto più lunghi possono anche influire negativamente sull'affidabilità dei sistemi mobili. Ad esempio, aumentano il rischio di tagli di energia imprevisti.

Le estensioni di sistema come driver, applicazioni e servizi possono avere un impatto significativo sui tempi di transizione on/off. In questa sezione vengono illustrate alcune delle procedure consigliate che gli sviluppatori di applicazioni e servizi possono seguire per evitare ritardi durante l'avvio, la standby e l'arresto e per garantire un'esperienza utente di post-avvio e post-ripresa reattiva. Per altri dettagli su come identificare i problemi di prestazioni in base all'uso di Windows Performance Toolkit e implementare le raccomandazioni seguenti per l'applicazione o il servizio, fare riferimento a white paper nella sezione "collegamenti ad altre risorse".

## <a name="best-practices"></a>Procedure consigliate

-   Usare Windows Performance Toolkit per misurare le prestazioni durante tutte le transizioni on/off.
-   Eseguire i test in modo controllato e confrontare i risultati con una baseline valida:
    -   Ottenere una misurazione di base in un sistema con il minor numero possibile di estensioni di sistema
    -   Aggiungere applicazioni e servizi uno alla volta
    -   Verificare la presenza di regressioni inaccettabili in tempi di transizione on/off
-   Evitare di usare codice gestito per le applicazioni nel percorso di avvio critico.
-   Assicurarsi che tutte le applicazioni rispondano rapidamente alle notifiche di arresto ( \_ messaggi WM QUERYENDSESSION e WM \_ ENDSESSION).
-   Ridurre i ritardi nel percorso di arresto dei servizi e delle applicazioni riducendo al minimo le attività di CPU, disco e rete in risposta alle notifiche di arresto.
-   Evitare ritardi nell'elaborazione della notifica di sospensione ( \_ messaggio WM POWERBROADCAST).
-   Rispondere rapidamente per riprendere gli eventi e ridurre al minimo l'utilizzo della CPU, del disco e della rete dopo la riattivazione.
-   Ridurre il consumo di risorse dell'applicazione dopo l'avvio.
-   Non avviare le applicazioni dalla chiave RunOnce a ogni avvio.
-   Per rendere disponibili le risorse di sistema durante l'avvio, convertire tutti i servizi non essenziali per avviare la richiesta o avviare il trigger.
-   Evitare di utilizzare i gruppi di ordini di caricamento per esprimere le dipendenze del servizio.
-   Verificare che tutti i servizi in esecuzione segnalino questo stato il prima possibile durante l'avvio per evitare di bloccare Gestione controllo servizi (SCM).
-   Evitare di usare codice gestito per i servizi nel percorso di avvio.
-   Non consentire ai servizi di acconsentire esplicitamente a ricevere notifiche di pre-arresto e arresto ( \_ PREspegnimento del controllo del servizio \_ e codici di controllo di arresto del controllo del servizio \_ ) a \_ meno che non sia assolutamente necessario.
-   Assicurarsi che tutti i servizi che hanno scelto di ricevere le notifiche di chiusura rispondano rapidamente a SCM.
-   Verificare che i servizi non optino per ricevere notifiche di sospensione, a meno che non sia assolutamente necessario.
-   Assicurarsi che tutti i servizi rispondano rapidamente per riprendere gli eventi e ridurre al minimo l'utilizzo della CPU, del disco e della rete dopo la riattivazione.

## <a name="links-to-other-resources"></a>Collegamenti ad altre risorse

-   -   [Guida alle soluzioni per le transizioni on/off di Windows](/windows-hardware/test/assessments/onoff-transition-performance)
-   [Analisi delle prestazioni di transizione on/off di Windows Vista](/windows-hardware/test/assessments/onoff-transition-performance)
-   [Analisi delle prestazioni di Windows](https://msdn.microsoft.com/performance/default.aspx)
-   [Documentazione di Windows Performance Toolkit su MSDN](/previous-versions/windows/desktop/xperf/windows-performance-analyzer--wpa-)
-   [Forum di analisi delle prestazioni di Windows](https://social.msdn.microsoft.com/Forums/wptk_v4/threads/)
-   [Event Tracing for Windows su MSDN](../etw/event-tracing-portal.md)

 

 
