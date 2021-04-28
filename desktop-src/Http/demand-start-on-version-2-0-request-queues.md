---
title: Avvio della richiesta nelle code di richieste della versione 2.0
description: Avvio della richiesta nelle code di richieste della versione 2.0
ms.assetid: 84a744b7-1b0e-4fa7-8015-4840251aa856
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06f6b14759e60fb69a47cda6975f6559c00771f1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090929"
---
# <a name="demand-start-on-version-20-request-queues"></a>Avvio della richiesta nelle code di richieste della versione 2.0

La funzionalità di avvio della richiesta delle code di richieste api del server HTTP versione 2.0 consente all'applicazione controller di ritardare la creazione di istanze del processo di lavoro fino all'arrivo della prima richiesta nella coda di richieste. Di conseguenza, le applicazioni possono evitare di utilizzare le risorse fino a quando non sono necessarie. Per altre informazioni sull'applicazione controller, vedere [l'argomento Coda di richieste](named-request-queue.md) denominate.

## <a name="asynchronous-demand-start"></a>Avvio della richiesta asincrona

L'applicazione controller [**chiama HttpWaitForDemandStart**](/windows/desktop/api/Http/nf-http-httpwaitfordemandstart) con l'handle per la coda di richieste per avviare una notifica di avvio della richiesta. Per il completamento asincrono, l'applicazione fornisce la struttura sovrapposta nel *parametro pOverlapped.* Quando **HttpWaitForDemandStart** viene chiamato in modo asincrono, l'applicazione controller invia una notifica all'arrivo della prima richiesta nella coda di richieste. Al termine della notifica di avvio della richiesta, l'applicazione controller può registrarsi per un'altra notifica di avvio della richiesta nella coda delle richieste.

L'API del server HTTP non consente più di una notifica di avvio della richiesta simultanea per una coda di richieste. Tuttavia, al termine della notifica di avvio della richiesta in sospeso, l'applicazione chiama di nuovo [**HttpWaitForDemandStart**](/windows/desktop/api/Http/nf-http-httpwaitfordemandstart) per avviare più processi di lavoro nella coda delle richieste. HTTP non applica limitazioni al numero di notifiche di avvio della richiesta o al numero di processi di lavoro che operano nella coda delle richieste. Le applicazioni controller possono tuttavia imporre il numero di processi di lavoro consentiti in una coda di richieste.

L'API server HTTP supporta l'annullamento di [**chiamate HttpWaitForDemandStart**](/windows/desktop/api/Http/nf-http-httpwaitfordemandstart) asincrone. Le applicazioni possono [**usare CancelIoEx**](/windows/desktop/FileIO/cancelioex-func) con la struttura sovrapposta fornita in *pOverlapped* per annullare una chiamata **HttpWaitForDemandStart in** sospeso.

## <a name="synchronous-demand-start"></a>Avvio della richiesta sincrona

L'avvio della richiesta sincrona non è consigliato perché l'applicazione si blocca fino all'arrivo di una richiesta nella coda di richieste.

 

 
