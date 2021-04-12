---
title: Creazione di un sink di notifica
description: Creazione di un sink di notifica
ms.assetid: 6a3cc771-1fef-4b79-baa1-c8d050e36d92
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 481cdd754e545ef87e3c0dc44324d46e48baf044
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396810"
---
# <a name="creating-a-notification-sink"></a><span data-ttu-id="cb3ce-103">Creazione di un sink di notifica</span><span class="sxs-lookup"><span data-stu-id="cb3ce-103">Creating a Notification Sink</span></span>

<span data-ttu-id="cb3ce-104">\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="cb3ce-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="cb3ce-105">Per ricevere notifiche di eventi da Microsoft Agent, è necessario implementare l'interfaccia [**IAgentNotifySink**](events.md)o [**IAgentNotifySinkEx**](iagentnotifysinkex.md) e creare e registrare un oggetto di tale tipo seguendo le convenzioni com:</span><span class="sxs-lookup"><span data-stu-id="cb3ce-105">To be notified of events by Microsoft Agent, you must implement either the [**IAgentNotifySink**](events.md)or the [**IAgentNotifySinkEx**](iagentnotifysinkex.md) interface, and create and register an object of that type following COM conventions:</span></span>


```
// Create a notification sink

pSinkEx = new AgentNotifySinkEx;

pSinkEx->AddRef();

// And register it with Microsoft Agent

hRes = pAgentEx->Register((IUnknown *)pSinkEx, &lNotifySinkID);
```



<span data-ttu-id="cb3ce-106">Ricordarsi di annullare la registrazione del sink di notifica quando l'applicazione viene arrestata e rilascia le interfacce di Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="cb3ce-106">Remember to unregister your notification sink when your application shuts down and releases Microsoft Agent's interfaces.</span></span>

 

 




