---
title: Creazione e associazione a una coda di richieste
description: Una coda di richieste è una coda del servizio che include richieste in sospeso per un'applicazione specifica.
ms.assetid: 93f8b230-af0a-4582-b35b-d65f6841e525
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 945b8451f9128357b7da0ddc64600b74deffd0d7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396470"
---
# <a name="creating-and-binding-to-a-request-queue"></a><span data-ttu-id="84e20-103">Creazione e associazione a una coda di richieste</span><span class="sxs-lookup"><span data-stu-id="84e20-103">Creating and Binding to a Request Queue</span></span>

<span data-ttu-id="84e20-104">Una coda di richieste è una coda del servizio che include richieste in sospeso per un'applicazione specifica.</span><span class="sxs-lookup"><span data-stu-id="84e20-104">A request queue is a service queue that holds pending requests for a specific application.</span></span> <span data-ttu-id="84e20-105">Un'applicazione crea la coda delle richieste indipendentemente dal gruppo di URL o dalla sessione del server chiamando la funzione [**HttpCreateRequestQueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) e imposta le proprietà della coda delle richieste chiamando la funzione [**HttpSetRequestQueueProperty**](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty) .</span><span class="sxs-lookup"><span data-stu-id="84e20-105">An application creates the request queue independently of the URL group or server session by calling the [**HttpCreateRequestQueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) function, and sets the request queue properties by calling the [**HttpSetRequestQueueProperty**](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty) function.</span></span> <span data-ttu-id="84e20-106">Queste proprietà sono il livello di dettaglio delle risposte 503, la lunghezza massima della coda e lo stato dell'attività.</span><span class="sxs-lookup"><span data-stu-id="84e20-106">These properties are the verbosity of 503 responses, the maximum length of the queue, and the activity state.</span></span>

<span data-ttu-id="84e20-107">Per fare in modo che le richieste vengano instradate alla propria coda di richieste, l'applicazione associa il gruppo di URL creato come parte della configurazione della fase di [esecuzione](run-time-configuration.md) alla coda chiamando [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) con **HttpServerBindingProperty** specificato nel parametro *Property* .</span><span class="sxs-lookup"><span data-stu-id="84e20-107">To cause requests to be routed to its request queue, the application binds the URL group it created as part of [run-time configuration](run-time-configuration.md) to the queue by calling [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) with **HttpServerBindingProperty** specified in the *Property* parameter.</span></span> <span data-ttu-id="84e20-108">Le richieste in ingresso dagli URL nel gruppo vengono quindi indirizzate alla coda di richieste specificata.</span><span class="sxs-lookup"><span data-stu-id="84e20-108">Incoming requests from the URLs in the group are then routed to the specified request queue.</span></span>

 

 




