---
title: Avvio della richiesta nelle code di richieste della versione 2,0
description: .
ms.assetid: 84a744b7-1b0e-4fa7-8015-4840251aa856
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78d618ea3fa38a856eba743d2bf60bfbfec9a633
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103963095"
---
# <a name="demand-start-on-version-20-request-queues"></a>Avvio della richiesta nelle code di richieste della versione 2,0

La funzionalità di avvio della richiesta della coda di richieste API versione 2,0 del server HTTP consente all'applicazione controller di ritardare la creazione di un'istanza del processo di lavoro finché la prima richiesta arriva nella coda di richieste. Pertanto, le applicazioni possono evitare l'utilizzo di risorse fino a quando non sono necessarie. Per ulteriori informazioni sull'applicazione controller, vedere l'argomento relativo alla [coda di richieste denominata](named-request-queue.md) .

## <a name="asynchronous-demand-start"></a>Avvio della richiesta asincrona

L'applicazione controller chiama [**HttpWaitForDemandStart**](/windows/desktop/api/Http/nf-http-httpwaitfordemandstart) con l'handle per la coda di richieste per avviare una notifica di avvio della richiesta. Per il completamento asincrono, l'applicazione fornisce la struttura sovrapposta nel parametro *pOverlapped* . Quando **HttpWaitForDemandStart** viene chiamato in modo asincrono, l'applicazione controller riceve una notifica quando arriva la prima richiesta nella coda di richieste. Al termine della notifica di avvio della richiesta, l'applicazione controller può registrarsi per un'altra notifica di avvio della richiesta nella coda di richieste.

L'API server HTTP non consente più di una notifica di avvio della richiesta simultanea per una coda di richieste. Tuttavia, quando la notifica di avvio della richiesta in attesa viene completata, l'applicazione chiama di nuovo [**HttpWaitForDemandStart**](/windows/desktop/api/Http/nf-http-httpwaitfordemandstart) per avviare più processi di lavoro nella coda di richieste. Il protocollo HTTP non impone limitazioni sul numero di notifiche di avvio della richiesta o sul numero di processi di lavoro che operano nella coda di richieste. Tuttavia, le applicazioni controller possono applicare il numero di processi di lavoro consentiti in una coda di richieste.

L'API server HTTP supporta l'annullamento di chiamate [**HttpWaitForDemandStart**](/windows/desktop/api/Http/nf-http-httpwaitfordemandstart) asincrone. Le applicazioni possono utilizzare [**CancelIoEx**](/windows/desktop/FileIO/cancelioex-func) con la struttura sovrapposta fornita in *pOverlapped* per annullare una chiamata **HttpWaitForDemandStart** in attesa.

## <a name="synchronous-demand-start"></a>Avvio della richiesta sincrona

Non è consigliabile avviare la richiesta sincrona perché l'applicazione si blocca fino a quando non arriva una richiesta nella coda delle richieste.

 

 