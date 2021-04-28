---
description: Procedure consigliate per le prestazioni di on/off
ms.assetid: 872c2a33-327e-41a8-81db-905c46673f13
title: Procedure consigliate per le prestazioni di on/off
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2c88eaf5175db43061e57bc4689d8bf256e6881
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088619"
---
# <a name="best-practices-for-onoff-performance"></a>Procedure consigliate per le prestazioni di on/off

## <a name="platform"></a>Piattaforma

**Client -** Windows Vista \| Windows 7  
**Server -** Windows Server 2008 \| Windows Server 2008 R2  

## <a name="description"></a>Descrizione

Gli stati di alimentazione del sistema (o stati S), come definito nella specifica ACPI (Advanced Computer Power Interface), vengono chiamati in modo colloquiale gli stati di accensione/spegnimento poiché la transizione di stato S più comune è un computer che si accende e si spegne. Le diverse transizioni di stato di on/off in un sistema che esegue Windows Vista o Windows 7 sono avvio, sospensione (ACPI S3), ibernazione (ACPI S4) e arresto.

Buone prestazioni durante queste transizioni di on/off non solo migliorano la qualità percepita di un computer, ma influiscono notevolmente sui modelli di utilizzo giornaliero del computer e sull'affidabilità del sistema. I clienti possono diventare frustrati dai sistemi che durano troppo a lungo per l'avvio o l'arresto. I sistemi mobili con lunghe transizioni di sospensione e ibernazione possono inutilmente esaurimento della durata della batteria. Anche tempi di arresto più lunghi possono influire negativamente sull'affidabilità dei sistemi mobili. Ad esempio, aumentano il rischio di interruzione imprevista dell'alimentazione.

Le estensioni di sistema, ad esempio driver, applicazioni e servizi, possono avere un impatto significativo sui tempi di transizione di on/off. Questa sezione illustra alcune delle procedure consigliate che gli sviluppatori di applicazioni e servizi possono seguire per evitare ritardi durante l'avvio, lo standby e l'arresto e per garantire un'esperienza utente reattiva dopo l'avvio e la ripresa. Per altre informazioni su come identificare i problemi di prestazioni di on/off usando Windows Performance Toolkit e implementare le raccomandazioni seguenti per l'applicazione o il servizio, vedere i white paper nella sezione "Collegamenti ad altre risorse".

## <a name="best-practices"></a>Procedure consigliate

-   Usare Windows Performance Toolkit per misurare le prestazioni durante tutte le transizioni di on/off.
-   Eseguire test in modo controllato ed eseguire confronti con una baseline valida:
    -   Ottenere una misurazione di base in un sistema con il numero massimo di estensioni di sistema possibile
    -   Aggiungere applicazioni e servizi uno alla volta
    -   Testare le regressioni inaccettabili nei tempi di transizione di on/off
-   Evitare di usare codice gestito per le applicazioni nel percorso di avvio critico.
-   Assicurarsi che tutte le applicazioni rispondano rapidamente alle notifiche di arresto (messaggi WM \_ QUERYENDSESSION e WM \_ ENDSESSION).
-   Ridurre i ritardi nel percorso di arresto di servizi e applicazioni riducendo al minimo l'attività di CPU, disco e rete in risposta alle notifiche di arresto.
-   Evitare ritardi nell'elaborazione della notifica di sospensione (messaggio WM \_ POWERBROADCAST).
-   Rispondere rapidamente per riprendere gli eventi e ridurre al minimo l'utilizzo della CPU, del disco e della rete post-ripresa.
-   Ridurre il consumo di risorse dell'applicazione dopo l'avvio.
-   Non avviare applicazioni dalla chiave RunOnce a ogni avvio.
-   Convertire tutti i servizi non di base all'avvio della richiesta o all'avvio del trigger per rendere disponibili le risorse di sistema durante l'avvio.
-   Evitare di usare gruppi di ordini di carico per esprimere le dipendenze del servizio.
-   Assicurarsi che tutti i servizi in esecuzione segnalano questo stato il prima possibile durante l'avvio per evitare di bloccare Gestione controllo servizi.
-   Evitare di usare codice gestito per i servizi nel percorso di avvio.
-   Non consentire ai servizi di acconsentire esplicitamente alla ricezione di notifiche di pre-arresto e arresto (codici di controllo SERVICE \_ CONTROL PRESHUTDOWN e SERVICE CONTROL SHUTDOWN) a meno che non \_ sia assolutamente \_ \_ necessario.
-   Assicurarsi che tutti i servizi che hanno scelto di ricevere notifiche di arresto rispondano rapidamente a Gestione controllo servizi.
-   Verificare che i servizi non acconsentano esplicitamente alla ricezione delle notifiche di sospensione, a meno che non sia assolutamente necessario.
-   Assicurarsi che tutti i servizi rispondano rapidamente per riprendere gli eventi e ridurre al minimo l'utilizzo della CPU, del disco e della rete post-ripresa.

## <a name="links-to-other-resources"></a>Collegamenti ad altre risorse

-   -   [Guida alle soluzioni per le transizioni di windows on/off](/windows-hardware/test/assessments/onoff-transition-performance)
-   [Analisi delle prestazioni di transizione on/off di Windows Vista](/windows-hardware/test/assessments/onoff-transition-performance)
-   [Analisi delle prestazioni di Windows](https://msdn.microsoft.com/performance/default.aspx)
-   [Documentazione di Windows Performance Toolkit su MSDN](/previous-versions/windows/desktop/xperf/windows-performance-analyzer--wpa-)
-   [Forum di Analisi delle prestazioni di Windows](https://social.msdn.microsoft.com/Forums/wptk_v4/threads/)
-   [Event Tracing for Windows su MSDN](../etw/event-tracing-portal.md)

 

 
