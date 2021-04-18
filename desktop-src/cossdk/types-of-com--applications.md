---
description: Tipi di applicazioni COM+
ms.assetid: 4b731f22-6837-4c03-9c8c-a76451369cf1
title: Tipi di applicazioni COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fb365863ee2b2fbe41997facdf21d84866af1f6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304931"
---
# <a name="types-of-com-applications"></a>Tipi di applicazioni COM+

Di seguito sono riportati i quattro tipi di applicazioni COM+ di base:

-   **Applicazioni server.** Un' *applicazione server* com+ viene eseguita nel proprio processo. Le applicazioni server possono supportare tutti i servizi COM+.
-   **Applicazioni di libreria.** Un' *applicazione libreria* com+ viene eseguita nel processo del client che la crea. In particolare, i componenti in un'applicazione di libreria vengono sempre caricati nel processo del creatore. Le applicazioni di libreria non sono associate in modo esplicito a un processo server. Possono usare la sicurezza basata sui ruoli, ma non supportano l'accesso remoto o i componenti in coda.
-   **Proxy di applicazione.** Un *proxy di applicazione* è un set di file contenente le informazioni di registrazione che consentono a un client di accedere in remoto a un'applicazione server. Quando viene eseguito in un computer client, un file proxy di applicazione scrive le informazioni relative all'applicazione server COM+, tra cui CLSID, ProgID, RemoteServerName e informazioni di marshalling, al computer client. È quindi possibile accedere all'applicazione server in modalità remota dal computer client.
-   **Applicazioni preinstallate com+**. COM+ include un set di applicazioni preinstallate che gestiscono funzioni interne. Le applicazioni preinstallate sono elencate nella cartella applicazioni COM+ dello strumento di amministrazione Servizi componenti, ma non possono essere modificate o eliminate. Di seguito sono riportate le seguenti applicazioni:
    -   Utilità .NET
    -   Applicazione di pubblicazione del controllo analizzatore
    -   Esplora COM+
    -   Listener coda messaggi non recapitabili di COM+ QC
    -   Utilità COM+
    -   Applicazioni In-Process IIS
    -   Applicazioni in pool di IIS out-of-process
    -   Applicazione di sistema

## <a name="notes"></a>Note

A partire da Windows Server 2003, è possibile eseguire applicazioni COM+ anche se l'applicazione di sistema è disabilitata. Le applicazioni COM+ vengono eseguite, ma senza i servizi di solito forniti dall'applicazione di sistema. Questi servizi includono l'utilizzo dello strumento di amministrazione Servizi componenti e del rilevamento degli eventi di sistema.

Inoltre, a partire da Windows Server 2003, la funzionalità di autenticazione per l'applicazione di sistema COM+ include il valore EOAC \_ Disable \_ AAA. Questo valore, che disabilita le attivazioni di Activate-As-Activator (AAA), viene usato con la funzione [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) quando si avvia l'applicazione di sistema. Impostando la funzionalità di autenticazione su EOAC \_ Disable AAA è possibile consentire a \_ un'applicazione in esecuzione con un account con privilegi, ad esempio LocalSystem, di impedire l'utilizzo dell'identità per l'avvio di componenti non attendibili.

 

 
