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
# <a name="cancellation"></a><span data-ttu-id="c99e0-106">Annullamento</span><span class="sxs-lookup"><span data-stu-id="c99e0-106">Cancellation</span></span>

<span data-ttu-id="c99e0-107">La maggior parte delle operazioni in WWSAPI può essere annullata durante l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="c99e0-107">Most of operations in the WWSAPI can be canceled during execution.</span></span>

<span data-ttu-id="c99e0-108">La funzione usata per annullare un'operazione dipende dall'oggetto interessato.</span><span class="sxs-lookup"><span data-stu-id="c99e0-108">Which function you use to cancel an operation depends on the object affected.</span></span>

| <span data-ttu-id="c99e0-109">Funzione</span><span class="sxs-lookup"><span data-stu-id="c99e0-109">Function</span></span>                                           | <span data-ttu-id="c99e0-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c99e0-110">Description</span></span>                                                                                                            |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c99e0-111">**WsAbortChannel**</span><span class="sxs-lookup"><span data-stu-id="c99e0-111">**WsAbortChannel**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsabortchannel)           | <span data-ttu-id="c99e0-112">Annulla tutti i dati di input e output in sospeso su un canale specificato e imposta lo stato del canale su WS \_ Channel \_ stato non \_ riuscito.</span><span class="sxs-lookup"><span data-stu-id="c99e0-112">Cancels all pending input and output on a specified channel and sets the channel state to WS\_CHANNEL\_STATE\_FAULTED.</span></span> |
| [<span data-ttu-id="c99e0-113">**WsAbortListener**</span><span class="sxs-lookup"><span data-stu-id="c99e0-113">**WsAbortListener**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener)         | <span data-ttu-id="c99e0-114">Annulla tutti gli input e output in sospeso in un listener specificato.</span><span class="sxs-lookup"><span data-stu-id="c99e0-114">Cancels all pending input and output on a specified listener.</span></span>                                                          |
| [<span data-ttu-id="c99e0-115">**WsAbortServiceProxy**</span><span class="sxs-lookup"><span data-stu-id="c99e0-115">**WsAbortServiceProxy**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsabortserviceproxy) | <span data-ttu-id="c99e0-116">Annulla tutti gli input e output in sospeso in un proxy del servizio specificato.</span><span class="sxs-lookup"><span data-stu-id="c99e0-116">Cancels all pending input and output on a specified service proxy.</span></span>                                                     |
| [<span data-ttu-id="c99e0-117">**WsAbortServiceHost**</span><span class="sxs-lookup"><span data-stu-id="c99e0-117">**WsAbortServiceHost**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsabortservicehost)   | <span data-ttu-id="c99e0-118">Interrompe e sospende le operazioni correnti nell'host del servizio.</span><span class="sxs-lookup"><span data-stu-id="c99e0-118">Interrupts and discontinues current operations on the service host.</span></span>                                                    |
| [<span data-ttu-id="c99e0-119">**WsAbandonCall**</span><span class="sxs-lookup"><span data-stu-id="c99e0-119">**WsAbandonCall**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall)             | <span data-ttu-id="c99e0-120">Abbandona una chiamata, una chiamata specificata su un proxy del servizio specificato.</span><span class="sxs-lookup"><span data-stu-id="c99e0-120">Abandons a call, a specified call on a specified service proxy.</span></span>                                                        |



 

<span data-ttu-id="c99e0-121">Per informazioni sugli annullamenti che interessano [le operazioni del servizio sul lato server](server-side-service-operations.md) e i callback del modello di servizio, vedere [annullamento della chiamata](call-cancellation.md).</span><span class="sxs-lookup"><span data-stu-id="c99e0-121">For information on cancellations that affect [server side service operations](server-side-service-operations.md) and service-model callbacks, see [Call Cancellation](call-cancellation.md).</span></span>


 

 




