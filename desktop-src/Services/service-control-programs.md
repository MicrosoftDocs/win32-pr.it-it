---
description: Un programma di controllo del servizio avvia e controlla i servizi.
ms.assetid: e7ba295f-2937-44ad-89e8-40200c5e58b6
title: Programmi di controllo del servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78b34232f5f87d84bdf30acd51f57afbf79a8385
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879026"
---
# <a name="service-control-programs"></a><span data-ttu-id="8a631-103">Programmi di controllo del servizio</span><span class="sxs-lookup"><span data-stu-id="8a631-103">Service Control Programs</span></span>

<span data-ttu-id="8a631-104">Un programma di controllo del servizio avvia e controlla i servizi.</span><span class="sxs-lookup"><span data-stu-id="8a631-104">A service control program starts and controls services.</span></span> <span data-ttu-id="8a631-105">Esegue le azioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="8a631-105">It performs the following actions:</span></span>

-   <span data-ttu-id="8a631-106">Avvia un servizio o un servizio driver, se il tipo di avvio è servizio di \_ \_ avvio richiesta.</span><span class="sxs-lookup"><span data-stu-id="8a631-106">Starts a service or driver service, if the start type is SERVICE\_DEMAND\_START.</span></span>
-   <span data-ttu-id="8a631-107">Invia le richieste di controllo a un servizio in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="8a631-107">Sends control requests to a running service.</span></span>
-   <span data-ttu-id="8a631-108">Esegue una query sullo stato corrente di un servizio in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="8a631-108">Queries the current status of a running service.</span></span>

<span data-ttu-id="8a631-109">Queste azioni richiedono un handle aperto per l'oggetto servizio.</span><span class="sxs-lookup"><span data-stu-id="8a631-109">These actions require an open handle to the service object.</span></span> <span data-ttu-id="8a631-110">Per ottenere l'handle, il programma di controllo del servizio deve:</span><span class="sxs-lookup"><span data-stu-id="8a631-110">To obtain the handle, the service control program must:</span></span>

1.  <span data-ttu-id="8a631-111">Utilizzare la funzione [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) per ottenere un handle per il database SCM in un computer specificato.</span><span class="sxs-lookup"><span data-stu-id="8a631-111">Use the [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) function to obtain a handle to the SCM database on a specified machine.</span></span>
2.  <span data-ttu-id="8a631-112">Utilizzare la funzione [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) o [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) per ottenere un handle per l'oggetto servizio.</span><span class="sxs-lookup"><span data-stu-id="8a631-112">Use the [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) or [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) function to obtain a handle to the service object.</span></span>

<span data-ttu-id="8a631-113">Per altre informazioni, vedere i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="8a631-113">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="8a631-114">Avvio del servizio</span><span class="sxs-lookup"><span data-stu-id="8a631-114">Service Startup</span></span>](service-startup.md)
-   [<span data-ttu-id="8a631-115">Richieste di controllo del servizio</span><span class="sxs-lookup"><span data-stu-id="8a631-115">Service Control Requests</span></span>](service-control-requests.md)
-   [<span data-ttu-id="8a631-116">Controllo di un servizio con SC</span><span class="sxs-lookup"><span data-stu-id="8a631-116">Controlling a Service Using SC</span></span>](controlling-a-service-using-sc.md)

 

 



