---
description: Esigenze di prestazioni di utenti e amministratori con Windows Sockets (Winsock).
ms.assetid: 6c4365c6-a406-497b-a313-1faeb3e3b7f5
title: 'Esigenze di prestazioni: utenti e amministratori'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93c74f4ec6f0a545a98a890f0bc8ff954fe43a3f79fc04fd2c2d92e68ea9f646
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097671"
---
# <a name="performance-needs-users-and-administrators"></a>Esigenze di prestazioni: utenti e amministratori

Gli utenti valutano le prestazioni dell'applicazione in base all'esperienza:

-   L'applicazione risponde rapidamente?
-   Durante l'esecuzione delle operazioni in background viene visualizzata un'icona a forma di clessidra?
-   L'applicazione viene avviata e chiusa rapidamente?
-   Gli errori vengono gestiti in modo comprensibile?

Per riepilogare, gli utenti vogliono che le applicazioni siano veloci e prevedibili.

Al contrario, gli amministratori spesso valutano le prestazioni di un'applicazione sull'efficienza con cui usa le risorse di rete. Gli amministratori possono chiedere:

-   L'applicazione ha un sovraccarico ridotto e un utilizzo efficiente della rete?
-   Viene usato il numero minimo di connessioni, in modo che il server possa usare il maggior numero possibile di utenti contemporaneamente?
-   Si chiama costantemente il supporto?

In breve, gli amministratori vogliono ridimensionare le applicazioni.

## <a name="best-practices-for-performance-needs"></a>Procedure consigliate per le esigenze di prestazioni

Quando si sviluppa un'Windows Sockets, questi requisiti di prestazioni si traducono in regole utili.

-   Fare in modo che le applicazioni di rete si a inizializzano rapidamente.

    L'interfaccia utente non deve attendere le risposte di rete. Alcune attività possono essere eseguite prima che la rete sia disponibile o senza la rete. Se la rete non risponde, l'utente potrebbe avere bisogno dell'interfaccia utente per operazioni semplici, ad esempio la chiusura dell'applicazione.

-   Non attendere l'arresto della rete.

    Le applicazioni client-server scritte correttamente gestiscono correttamente le disconnessioni interrotte. Non avviare un'operazione potenzialmente lunga, ad esempio la sincronizzazione di file o cartelle con un server, che non può essere interrotta all'arresto. Le reti non sono costantemente reattive, quindi anche le operazioni di piccole dimensioni potrebbero rivelarsi dispendiose in termini di tempo. Fornire un feedback positivo per gli utenti, incluse le indicazioni sullo stato di avanzamento e i tempi di completamento stimati.

-   Assicurarsi un'interfaccia utente reattiva.

    La velocità di risposta dell'applicazione consente di eliminare le chiamate al supporto help desk non necessarie. Una buona guida per la risposta interattiva è di 500 millisecondi. Gli utenti percepiranno pause più lunghe di 500 millisecondi come un ritardo nelle prestazioni. Le applicazioni devono essere sufficientemente reattive da fornire all'utente la sicurezza dell'applicazione.

-   Esaminare gli errori di rete.

    Non tutti gli errori di rete sono critici. Ad esempio, un'applicazione che ha ricevuto o pubblicato tutti i dati può probabilmente ignorare gli errori durante la chiusura della connessione. Non presupporre che la rete o l'utente sia disponibile; gestire gli errori senza l'intervento dell'utente o ignorarli se gli errori non sono critici.

-   Un'applicazione deve definire i propri timeout ragionevoli.

    Ad esempio, una richiesta Windows Sockets connect() può bloccarsi in alcune condizioni per un massimo di 21 secondi. Le applicazioni potrebbero dover introdurre i propri timeout in base alle esigenze degli utenti.

-   Ridurre al minimo il sovraccarico del protocollo.

    La conservazione della larghezza di banda di rete consente di ridurre al minimo l'overhead del protocollo dovuto all'applicazione. Si tratta anche di eliminare il traffico di rete non necessario. I protocolli con un overhead di intestazione inferiore possono essere usati per trasferire i dati dell'applicazione. Ad esempio, quando si inviano piccole quantità di dati non critici o ripetibili, usare UDP anziché TCP per ridurre il sovraccarico associato alla creazione e alla manutenzione della connessione. Se gli stessi dati devono essere inviati a più destinatari, prendere in considerazione il multicast. Tenere presente che le applicazioni UDP non sono controllate dal flusso. Il push oltre la larghezza di banda disponibile può causare un errore irreversibile della rete. L'utilità Netstat può essere usata con le opzioni **-e** **e -s** per visualizzare statistiche per vari protocolli.

-   Conservare le risorse di sistema.

    Le risorse di sistema possono essere utilizzate rapidamente se non viene usata una limitazione appropriata. Ad esempio, i socket e le connessioni TCP utilizzano risorse. Non usare diverse connessioni TCP per ogni client in cui uno sarà utilizzato per lo scopo dell'applicazione.

Per le applicazioni transazionali, una buona esperienza utente e un utilizzo ridotto della rete non sono obiettivi in conflitto. La rete è un collo di bottiglia. Le applicazioni a elevato utilizzo di rete dedicano più tempo all'attesa e le applicazioni di rete ben scritte sono progettate per ridurre al minimo il tempo di attesa non necessario, sia per l'interfaccia utente che per le trasmissioni di rete.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Applicazioni socket Windows ad alte prestazioni](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[Dimensioni delle prestazioni](performance-dimensions-2.md)
</dt> </dl>

 

 



