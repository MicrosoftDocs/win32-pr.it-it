---
title: Isolamento del processo
description: L'API server HTTP versione 2,0 offre la possibilità di creare un servizio più sicuro e affidabile isolando i processi di lavoro che gestiscono le richieste nella coda di richieste.
ms.assetid: 893741b7-025c-4642-aff4-a5d69244763f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efcfccc78bbef435aa0c74e918003383135bc4ed
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/06/2021
ms.locfileid: "103885900"
---
# <a name="process-isolation"></a>Isolamento del processo

L'API server HTTP versione 2,0 offre la possibilità di creare un servizio più sicuro e affidabile isolando i processi di lavoro che gestiscono le richieste nella coda di richieste. La coda di richieste viene creata e gestita da un controller o da un processo Creator che controlla rigorosamente l'accesso. Il processo controller avvia uno o più processi di lavoro distinti che eseguono I/O nella coda delle richieste. Il processo controller viene eseguito con privilegi amministrativi e configura la coda di richieste, mentre il ruolo di lavoro con privilegi inferiori elabora le richieste di accesso e di servizio dalla coda delle richieste. Questa architettura supporta i criteri di applicazioni in esecuzione con "privilegio minimo" e riduce la possibilità di vulnerabilità della sicurezza introdotte da codice di terze parti che potrebbe essere in esecuzione nei processi di lavoro.

L'accesso alla coda di richieste viene concesso quando il processo controller crea la coda di richieste con un nome e un elenco di controllo di accesso (ACL). Le applicazioni Web incluse nell'ACL possono aprire una coda di richieste esistente in base al nome. Il processo Creator può anche essere un processo di lavoro nella coda di richieste. Per ulteriori informazioni, vedere l'argomento relativo alla [coda di richieste denominata](named-request-queue.md) . Il diagramma seguente illustra l'architettura di una tipica applicazione HTTP in esecuzione con il modello di processo di lavoro:

![Diagramma che illustra l'architettura di un'applicazione H T T P utilizzando il modello di processo di lavoro.](images/processisolation.png)

I singoli processi di lavoro all'interno dell'applicazione sono isolati dagli altri processi di lavoro e l'integrità di ogni processo di lavoro può essere monitorata dal processo del controller. Il processo del controller è isolato dai processi di lavoro. I componenti dell'architettura HTTP sono descritti di seguito:

-   Processo del creatore o del controller: il processo del controller può essere eseguito con o senza privilegi amministrativi per monitorare l'integrità e configurare il servizio. Il processo controller crea in genere una singola sessione del server per il servizio e definisce i gruppi di URL nella sessione del server. Il gruppo di URL a cui è associato un particolare URL determina quale coda di richieste servizi lo spazio dei nomi indicato dall'URL specifico. Il processo controller crea anche la coda di richieste e avvia i processi di lavoro che possono accedere alla coda di richieste.
-   Processo di lavoro: i processi di lavoro, avviati dal processo del controller, eseguono operazioni di i/o nella coda di richieste associata agli URL che il servizio. All'applicazione Web viene concesso l'accesso alla coda di richieste da parte del processo controller nell'ACL quando viene creata la coda di richieste. A meno che l'applicazione Web non sia anche il processo Creator, non gestisce il servizio o configura la coda delle richieste. Il processo controller comunica il nome della coda di richieste al processo di lavoro e il processo di lavoro apre la coda delle richieste in base al nome. I processi di lavoro possono caricare applicazioni Web di terze parti senza introdurre vulnerabilità di sicurezza in altre parti dell'applicazione.
-   Coda di richieste: la coda di richieste viene creata e configurata dal processo del controller. Il controller specifica i processi a cui è consentito l'accesso alla coda di richieste nell'ACL quando viene creata la coda di richieste.
-   Sessione del server: il processo controller crea in genere e configura una singola sessione del server per l'applicazione. La sessione del server gestisce le proprietà di configurazione per l'intera applicazione. I gruppi di URL vengono creati nella sessione del server dal processo del controller.
-   Gruppo URL: il processo controller crea i gruppi di URL nella sessione del server e configura il gruppo di URL indipendentemente dalla sessione del server. Gli URL vengono aggiunti al gruppo dal processo del controller. Le richieste vengono indirizzate alla coda di richieste a cui è associato il gruppo di URL.

 

 




