---
title: Isolamento del processo
description: L'API del server HTTP versione 2.0 offre la possibilità di creare un servizio più sicuro e affidabile isolando i processi di lavoro che forniscono le richieste nella coda delle richieste.
ms.assetid: 893741b7-025c-4642-aff4-a5d69244763f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 025e0829e020740aeeaf0381849b68bfde8b8244e845f9b5f24347bfa6bec1d6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119830077"
---
# <a name="process-isolation"></a>Isolamento del processo

L'API del server HTTP versione 2.0 offre la possibilità di creare un servizio più sicuro e affidabile isolando i processi di lavoro che forniscono le richieste nella coda delle richieste. La coda di richieste viene creata e amministrativa da un controller o da un processo di creazione che controlla rigorosamente l'accesso. Il processo controller avvia uno o più processi di lavoro separati che eseguono operazioni di I/O nella coda delle richieste. Il processo del controller viene eseguito con privilegi amministrativi e configura la coda delle richieste, mentre il ruolo di lavoro con privilegi inferiori elabora l'accesso e le richieste di servizio dalla coda delle richieste. Questa architettura supporta i criteri delle applicazioni in esecuzione con "privilegi minimi" e riduce la possibilità di vulnerabilità di sicurezza introdotte da codice di terze parti che potrebbero essere in esecuzione nei processi di lavoro.

L'accesso alla coda di richieste viene concesso quando il processo del controller crea la coda di richieste con un nome e un elenco di controllo di accesso (ACL). Le applicazioni Web incluse nell'ACL possono aprire una coda di richieste esistente in base al nome. Il processo creatore può anche essere un processo di lavoro nella coda delle richieste. Per altre informazioni, vedere [l'argomento Coda di richieste](named-request-queue.md) denominate. Il diagramma seguente illustra l'architettura di una tipica applicazione HTTP in esecuzione con il modello di processo di lavoro:

![Diagramma che illustra l'architettura di un'applicazione T-P che usa il modello di processo di lavoro.](images/processisolation.png)

I singoli processi di lavoro all'interno dell'applicazione sono isolati dagli altri processi di lavoro e l'integrità di ogni processo di lavoro può essere monitorata dal processo controller. Il processo del controller è isolato dai processi di lavoro. I componenti dell'architettura HTTP sono descritti di seguito:

-   Processo creatore o controller: il processo del controller può essere eseguito con o senza privilegi amministrativi per monitorare l'integrità e configurare il servizio. Il processo del controller crea in genere una singola sessione del server per il servizio e definisce i gruppi di URL nella sessione del server. Il gruppo di URL a cui è associato un particolare URL determina a quale servizio di accodamento richieste è associato lo spazio dei nomi specificato dall'URL specifico. Il processo del controller crea anche la coda delle richieste e avvia i processi di lavoro che possono accedere alla coda di richieste.
-   Processo di lavoro: i processi di lavoro, avviati dal processo del controller, eseguono operazioni di I/O nella coda di richieste associata agli URL che eseguono il servizio. All'applicazione Web viene concesso l'accesso alla coda di richieste dal processo del controller nell'elenco di controllo di accesso quando viene creata la coda di richieste. A meno che l'applicazione Web non sia anche il processo di creazione, non gestisce il servizio né configura la coda delle richieste. Il processo controller comunica il nome della coda di richieste al processo di lavoro e il processo di lavoro apre la coda di richieste in base al nome. I processi di lavoro possono caricare applicazioni Web di terze parti senza introdurre vulnerabilità di sicurezza in altre parti dell'applicazione.
-   Coda richieste: la coda di richieste viene creata e configurata dal processo del controller. Il controller specifica i processi a cui è consentito l'accesso alla coda di richieste nell'ACL quando viene creata la coda di richieste.
-   Sessione server: il processo del controller crea e configura in genere una singola sessione del server per l'applicazione. La sessione del server mantiene le proprietà di configurazione per l'intera applicazione. I gruppi di URL vengono creati nella sessione del server dal processo del controller.
-   Gruppo DI URL: il processo del controller crea i gruppi di URL nella sessione del server e configura il gruppo di URL indipendentemente dalla sessione del server. Gli URL vengono aggiunti al gruppo dal processo del controller. Le richieste vengono indirizzate alla coda di richieste a cui è associato il gruppo di URL.

 

 




