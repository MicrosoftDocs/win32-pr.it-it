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
# <a name="creating-a-notification-sink"></a>Creazione di un sink di notifica

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Per ricevere notifiche di eventi da Microsoft Agent, è necessario implementare l'interfaccia [**IAgentNotifySink**](events.md)o [**IAgentNotifySinkEx**](iagentnotifysinkex.md) e creare e registrare un oggetto di tale tipo seguendo le convenzioni com:


```
// Create a notification sink

pSinkEx = new AgentNotifySinkEx;

pSinkEx->AddRef();

// And register it with Microsoft Agent

hRes = pAgentEx->Register((IUnknown *)pSinkEx, &lNotifySinkID);
```



Ricordarsi di annullare la registrazione del sink di notifica quando l'applicazione viene arrestata e rilascia le interfacce di Microsoft Agent.

 

 




