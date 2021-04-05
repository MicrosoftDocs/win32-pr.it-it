---
description: Esigenze di prestazioni degli utenti e degli amministratori con le applicazioni Windows Sockets (Winsock).
ms.assetid: 6c4365c6-a406-497b-a313-1faeb3e3b7f5
title: 'Esigenze di prestazioni: utenti e amministratori'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 009a8178cf1d7516e9c16493916f8cf911752b9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049478"
---
# <a name="performance-needs-users-and-administrators"></a>Esigenze di prestazioni: utenti e amministratori

Gli utenti possono valutare le prestazioni delle applicazioni in base alla loro esperienza:

-   L'applicazione è pronta per rispondere?
-   Icona a forma di clessidra visualizzata durante l'esecuzione delle operazioni in background.
-   L'applicazione viene avviata e chiusa rapidamente?
-   Gli errori vengono gestiti in modo comprensibile?

Per riepilogare, gli utenti desiderano che le applicazioni siano veloci e prevedibili.

Al contrario, gli amministratori spesso giudicano le prestazioni di un'applicazione sull'efficienza dell'utilizzo delle risorse di rete. Gli amministratori possono richiedere:

-   L'applicazione ha un sovraccarico ridotto e un utilizzo efficiente della rete?
-   Il numero minimo di connessioni viene utilizzato, quindi il server può servire il maggior numero possibile di utenti in una sola volta?
-   Sto chiamando sempre helpdesk?

In breve, gli amministratori desiderano la scalabilità delle applicazioni.

## <a name="best-practices-for-performance-needs"></a>Procedure consigliate per le esigenze di prestazioni

Quando si sviluppa un'applicazione Windows Sockets, questi requisiti di prestazioni vengono convertiti in regole utili.

-   L'inizializzazione delle applicazioni di rete è rapida.

    L'interfaccia utente non deve attendere la risposta alla rete. Alcune attività possono essere eseguite prima che la rete sia disponibile o senza la rete. Se la rete non risponde, l'utente potrebbe avere bisogno dell'interfaccia utente per operazioni semplici, ad esempio la chiusura dell'applicazione.

-   Non attendere che la rete venga arrestata.

    Le applicazioni client-server scritte correttamente gestiscono le disconnessioni interrotte normalmente. Non avviare un'operazione potenzialmente lunga, ad esempio la sincronizzazione di file o cartelle con un server, che non può essere interrotta al momento dell'arresto. Le reti non rispondono in modo coerente, quindi anche le piccole operazioni possono rivelarsi molto tempo. Fornire un feedback positivo per gli utenti, incluse le indicazioni sullo stato di avanzamento e i tempi di completamento stimati.

-   Assicurarsi di disporre di un'interfaccia utente reattiva.

    La velocità di risposta dell'applicazione consente di eliminare chiamate al supporto tecnico non necessarie. Una guida efficace per la risposta interattiva è 500 millisecondi. Gli utenti percepiscono pause più lunghe di 500 millisecondi come un ritardo nelle prestazioni. Le applicazioni devono essere sufficientemente reattive per fornire all'utente l'attendibilità dell'applicazione.

-   Esaminare gli errori di rete.

    Non tutti gli errori di rete sono di importanza critica. Ad esempio, un'applicazione che ha ricevuto o inviato tutti i relativi dati può probabilmente ignorare gli errori quando si chiude la connessione. Non presupporre che la rete o l'utente sia disponibile; è possibile gestire gli errori senza l'intervento dell'utente o ignorarli se gli errori sono non critici.

-   Un'applicazione deve definire il proprio timeout ragionevole.

    Una richiesta Windows Sockets Connect (), ad esempio, può bloccarsi in alcune condizioni per un tempo di 21 secondi. È possibile che le applicazioni debbano introdurre i propri timeout nel modo appropriato per gli utenti.

-   Ridurre al minimo il sovraccarico del protocollo.

    La conservazione della larghezza di banda della rete riguarda parzialmente la riduzione del sovraccarico del protocollo sostenuto dall'applicazione. Si tratta anche di eliminare il traffico di rete superfluo. Per il trasferimento dei dati dell'applicazione è possibile usare protocolli con sovraccarico di intestazione inferiore. Ad esempio, quando si inviano quantità minori di dati non critici o ripetibili, utilizzare UDP anziché TCP per ridurre l'overhead associato alla creazione e manutenzione della connessione. Se gli stessi dati devono essere inviati a più destinatari, prendere in considerazione il multicast. Tenere presente che le applicazioni UDP non sono controllate dal flusso. Se si supera la larghezza di banda disponibile, è possibile che si verifichi un errore irreversibile della rete. L'utilità netstat può essere usata con le opzioni **-e** e **-s** per visualizzare le statistiche per diversi protocolli.

-   Conservare le risorse di sistema.

    Le risorse di sistema possono essere utilizzate rapidamente se non viene utilizzato il vincolo appropriato. Ad esempio, le connessioni Sockets e TCP utilizzano risorse. Non usare più connessioni TCP per ogni client, dove ne sarà disponibile uno per lo scopo dell'applicazione.

Per le applicazioni transazionali, un'esperienza utente ottimale e un basso utilizzo della rete non rappresentano obiettivi in conflitto. La rete è un collo di bottiglia. Le applicazioni con utilizzo intensivo di rete dedicano più tempo all'attesa e le applicazioni di rete ben scritte sono progettate per ridurre al minimo il tempo di attesa superfluo, sia per l'interfaccia utente che per trasmissioni di rete.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Applicazioni Windows Sockets a prestazioni elevate](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[Dimensioni prestazioni](performance-dimensions-2.md)
</dt> </dl>

 

 



