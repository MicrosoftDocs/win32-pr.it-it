---
title: Annullamento
description: La maggior parte delle operazioni in WWSAPI può essere annullata durante l'esecuzione.
ms.assetid: d73d76e1-bd78-40ce-9f92-e282b6b127ce
keywords:
- Servizi Web di annullamento per Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6e979455e898922dfb7c81381c1f1aafd455274
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104339755"
---
# <a name="cancellation"></a>Annullamento

La maggior parte delle operazioni in WWSAPI può essere annullata durante l'esecuzione.

La funzione usata per annullare un'operazione dipende dall'oggetto interessato.

| Funzione                                           | Descrizione                                                                                                            |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**WsAbortChannel**](/windows/desktop/api/WebServices/nf-webservices-wsabortchannel)           | Annulla tutti i dati di input e output in sospeso su un canale specificato e imposta lo stato del canale su WS \_ Channel \_ stato non \_ riuscito. |
| [**WsAbortListener**](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener)         | Annulla tutti gli input e output in sospeso in un listener specificato.                                                          |
| [**WsAbortServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsabortserviceproxy) | Annulla tutti gli input e output in sospeso in un proxy del servizio specificato.                                                     |
| [**WsAbortServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsabortservicehost)   | Interrompe e sospende le operazioni correnti nell'host del servizio.                                                    |
| [**WsAbandonCall**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall)             | Abbandona una chiamata, una chiamata specificata su un proxy del servizio specificato.                                                        |



 

Per informazioni sugli annullamenti che interessano [le operazioni del servizio sul lato server](server-side-service-operations.md) e i callback del modello di servizio, vedere [annullamento della chiamata](call-cancellation.md).


 

 




