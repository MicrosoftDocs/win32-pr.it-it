---
title: Linee guida per i servizi
description: I servizi devono rispettare queste linee guida per assicurarsi che Gestione riavvio possa arrestare e riavviare i servizi, se necessario, per installare gli aggiornamenti. Le applicazioni possono utilizzare le linee guida descritte in linee guida per le applicazioni.
ms.assetid: 69a98f82-71bb-4780-8a3f-294cc5629900
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51374c0a4c6fc561b8259aadf15e3d5487e12483
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047085"
---
# <a name="guidelines-for-services"></a>Linee guida per i servizi

I servizi devono rispettare queste linee guida per assicurarsi che Gestione riavvio possa arrestare e riavviare i servizi, se necessario, per installare gli aggiornamenti. Le applicazioni possono utilizzare le linee guida descritte in [linee guida per le applicazioni](guidelines-for-applications.md).

-   I servizi devono essere in grado di essere arrestati e riavviati utilizzando [Gestione controllo servizi](/windows/desktop/Services/service-control-manager) senza richiedere un riavvio del sistema. Le eccezioni a questa linea guida sono processi di sistema critici che vengono eseguiti nel contesto di lsass.exe o services.exe.
-   Gestione riavvio rispetta le dipendenze del servizio. Quando un servizio viene arrestato e riavviato, i servizi dipendenti vengono arrestati e riavviati.
-   I servizi devono specificare l'intervallo di recupero e il periodo di ripristino in [Gestione controllo servizi (SCM)](/windows/desktop/Services/service-control-manager). L'intervallo di recupero è il tempo, in millisecondi, dopo l'ultimo errore che il controllo SCM attende prima di intraprendere l'azione di ripristino. Il periodo di reimpostazione è il tempo, in secondi, dopo l'ultimo errore che Gestione controllo servizi attende prima di reimpostare il numero di errori su 0. I servizi possono usare la funzione [**ChangeServiceConfig2**](/windows/desktop/api/winsvc/nf-winsvc-changeserviceconfig2a) per modificare le impostazioni di configurazione.

    Per specificare che il servizio deve essere riavviato un minuto dopo il primo errore di riavvio del servizio, i [servizi critici](critical-system-services.md) devono usare le impostazioni di ripristino seguenti, riavviate due minuti dopo il secondo errore e che il computer venga riavviato un minuto dopo il terzo errore. Il numero di errori viene reimpostato su 0 dopo 300 secondi.

    <dl> Azioni di ripristino: Restart/60000/restart/120000/reboot/60000 & Reset = 300  
    </dl>

    I [servizi critici](critical-system-services.md) devono essere avviati prima di servizi non critici. I servizi che non sono servizi critici devono usare le impostazioni di ripristino seguenti per specificare che il servizio venga riavviato due minuti dopo il primo errore per riavviare il servizio. Il servizio non viene riavviato dopo il secondo errore e un amministratore deve intervenire in questo caso. Il numero di errori viene reimpostato su 0 dopo 900 secondi.

    <dl> Azioni di ripristino: riavvio/120000/riavvio/300.000/None/0 & Reset = 900  
    </dl>

 

 