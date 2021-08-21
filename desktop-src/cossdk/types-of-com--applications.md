---
description: Tipi di applicazioni COM+
ms.assetid: 4b731f22-6837-4c03-9c8c-a76451369cf1
title: Tipi di applicazioni COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13bf55f7c2f25c490f0806a7924d32c6cbf981e79b8461ba12fc0f95964691c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119499671"
---
# <a name="types-of-com-applications"></a>Tipi di applicazioni COM+

Di seguito sono riportati i quattro tipi di base di applicazioni COM+:

-   **Applicazioni server.** Un'applicazione *server* COM+ viene eseguita nel proprio processo. Le applicazioni server possono supportare tutti i servizi COM+.
-   **Applicazioni di libreria.** Un'applicazione *libreria* COM+ viene eseguita nel processo del client che la crea. In particolare, i componenti in un'applicazione libreria vengono sempre caricati nel processo dell'autore. Le applicazioni di libreria non sono associate in modo esplicito a un processo server. Possono usare la sicurezza basata sui ruoli, ma non supportano l'accesso remoto o i componenti in coda.
-   **Proxy dell'applicazione.** Un *proxy di applicazione* è un set di file contenenti informazioni di registrazione che consentono a un client di accedere in remoto a un'applicazione server. Quando viene eseguito in un computer client, un file proxy dell'applicazione scrive informazioni sull'applicazione server COM+, inclusi CLSID, ProgID, RemoteServerName e informazioni di marshalling, nel computer client. L'applicazione server è quindi accessibile in modalità remota dal computer client.
-   **Applicazioni preinstallate COM+**. COM+ include un set di applicazioni preinstallate che gestiscono funzioni interne. Le applicazioni preinstallate sono elencate nella cartella Applicazioni COM+ dello strumento amministrativo Servizi componenti, ma non possono essere modificate o eliminate. Queste applicazioni includono quanto segue:
    -   Utilità .NET
    -   Applicazione di controllo dell'Publisher analizzatore
    -   COM+ Explorer
    -   Listener della coda di messaggi non recapitati di com+ QC
    -   Utilità COM+
    -   Applicazioni In-Process IIS
    -   Applicazioni in pool out-of-process IIS
    -   Applicazione di sistema

## <a name="notes"></a>Note

A Windows Server 2003, è possibile eseguire applicazioni COM+ anche se l'applicazione di sistema è disabilitata. Le applicazioni COM+ verranno eseguite, anche se senza i servizi in genere forniti dall'applicazione di sistema. Questi servizi includono l'uso dello strumento amministrativo Servizi componenti e del rilevamento degli eventi di sistema.

Anche a Windows Server 2003, la funzionalità di autenticazione per l'applicazione di sistema COM+ include il valore EOAC \_ DISABLE \_ AAA. Questo valore, che disabilita le attivazioni activate-as-activator (AAA), viene usato con la funzione [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) all'avvio dell'applicazione di sistema. L'impostazione della funzionalità di autenticazione su EOAC DISABLE AAA consente a un'applicazione eseguita con un account con privilegi (ad esempio LocalSystem) di impedire che la propria identità venga usata per avviare componenti non \_ \_ attendibili.

 

 
