---
title: Annullamento
description: La maggior parte delle operazioni in WWSAPI può essere annullata durante l'esecuzione.
ms.assetid: d73d76e1-bd78-40ce-9f92-e282b6b127ce
keywords:
- Annullamento dei servizi Web per Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf75bd8d07d8f78ddf0a5750e6f4f96feb073dc15b8e63ed23ab8ceb061de145
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117841781"
---
# <a name="cancellation"></a>Annullamento

La maggior parte delle operazioni in WWSAPI può essere annullata durante l'esecuzione.

La funzione utilizzata per annullare un'operazione dipende dall'oggetto interessato.

| Funzione                                           | Descrizione                                                                                                            |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**WsAbortChannel**](/windows/desktop/api/WebServices/nf-webservices-wsabortchannel)           | Annulla tutti gli input e l'output in sospeso in un canale specificato e imposta lo stato del canale su WS \_ CHANNEL \_ STATE \_ FAULTED. |
| [**WsAbortListener**](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener)         | Annulla tutti gli input e l'output in sospeso in un listener specificato.                                                          |
| [**WsAbortServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsabortserviceproxy) | Annulla tutti gli input e l'output in sospeso in un proxy del servizio specificato.                                                     |
| [**WsAbortServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsabortservicehost)   | Interrompe e interrompe le operazioni correnti nell'host del servizio.                                                    |
| [**WsAbandonCall**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall)             | Abbandona una chiamata, una chiamata specificata su un proxy di servizio specificato.                                                        |



 

Per informazioni sugli annullamenti che influiscono [sulle operazioni del servizio lato server](server-side-service-operations.md) e sui callback del modello di servizio, vedere [Annullamento delle chiamate](call-cancellation.md).


 

 




