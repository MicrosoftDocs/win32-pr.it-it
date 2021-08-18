---
title: Linee guida per i servizi
description: I servizi devono rispettare queste linee guida per garantire che Gestione riavvio possa arrestare e riavviare i servizi, se necessario, per installare gli aggiornamenti. Le applicazioni possono usare le linee guida descritte in Linee guida per le applicazioni.
ms.assetid: 69a98f82-71bb-4780-8a3f-294cc5629900
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6198da0d4f6f7887aaf37c858d98f3eb48e72c0d7722a1b5785a1cb280c96fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010139"
---
# <a name="guidelines-for-services"></a>Linee guida per i servizi

I servizi devono rispettare queste linee guida per garantire che Gestione riavvio possa arrestare e riavviare i servizi, se necessario, per installare gli aggiornamenti. Le applicazioni possono usare le linee guida descritte in [Linee guida per le applicazioni](guidelines-for-applications.md).

-   I servizi devono essere in grado di essere arrestati e riavviati usando Gestione controllo [servizi](/windows/desktop/Services/service-control-manager) senza richiedere un riavvio del sistema. Le eccezioni a questa linea guida sono processi di sistema critici eseguiti nel contesto di lsass.exe o services.exe.
-   Restart Manager rispetta le dipendenze del servizio. Quando un servizio viene arrestato e riavviato, i servizi dipendenti vengono arrestati e riavviati.
-   I servizi devono specificare l'intervallo di ripristino e il periodo di reimpostazione in [Gestione controllo servizi .](/windows/desktop/Services/service-control-manager) L'intervallo di ripristino è il tempo, in msecs, dopo l'ultimo errore che SCM attende prima di eseguire l'azione di ripristino. Il periodo di reimpostazione è il tempo, in secondi, dopo l'ultimo errore che Gestione controllo servizi attende prima di reimpostare il numero di errori su 0. I servizi possono [**usare la funzione ChangeServiceConfig2**](/windows/desktop/api/winsvc/nf-winsvc-changeserviceconfig2a) per modificare le impostazioni di configurazione.

    [](critical-system-services.md) I servizi critici devono usare le impostazioni di ripristino seguenti per specificare che il servizio deve essere riavviato un minuto dopo il primo errore di riavvio del servizio, riavviato due minuti dopo il secondo errore e che il computer venga riavviato un minuto dopo il terzo errore. Il numero di errori viene reimpostato su 0 dopo 300 secondi.

    <dl> Azioni di ripristino: Restart/60000/Restart/120000/Reboot/60000 & Reset =300  
    </dl>

    [I servizi](critical-system-services.md) critici devono essere avviati prima dei servizi non critici. I servizi che non sono servizi critici devono usare le impostazioni di ripristino seguenti per specificare che il servizio deve essere riavviato due minuti dopo il primo errore di riavvio del servizio. Il servizio non viene riavviato dopo il secondo errore e un amministratore deve intervenire in questo caso. Il numero di errori viene reimpostato su 0 dopo 900 secondi.

    <dl> Azioni di ripristino: Riavvio/120000/Riavvio/300000/Nessuno/0 & reimpostazione = 900  
    </dl>

 

 