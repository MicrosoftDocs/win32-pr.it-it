---
title: Creazione di un sink di notifica
description: Creazione di un sink di notifica
ms.assetid: 6a3cc771-1fef-4b79-baa1-c8d050e36d92
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2acf76d77e69df41b7fbd3fb83fbd232dfdfd03682d39681e1f2a4fa9f2d19ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118480093"
---
# <a name="creating-a-notification-sink"></a>Creazione di un sink di notifica

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Per ricevere una notifica degli eventi da Parte di Microsoft Agent, è necessario implementare [**l'interfaccia IAgentNotifySink**](events.md)o [**IAgentNotifySinkEx**](iagentnotifysinkex.md) e creare e registrare un oggetto del tipo in base alle convenzioni COM seguenti:


```
// Create a notification sink

pSinkEx = new AgentNotifySinkEx;

pSinkEx->AddRef();

// And register it with Microsoft Agent

hRes = pAgentEx->Register((IUnknown *)pSinkEx, &lNotifySinkID);
```



Ricordarsi di annullare la registrazione del sink di notifica quando l'applicazione viene arrestata e rilascia le interfacce di Microsoft Agent.

 

 




