---
description: Un thread può, in qualsiasi momento, chiamare WSAIsBlocking per determinare se una chiamata di blocco è attualmente in corso.
ms.assetid: 6213ded4-feab-404f-86a0-3db9a0a42769
title: Annullamento di operazioni di blocco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 502870b8935dc97c1d6c3714808d1c6532780f7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307024"
---
# <a name="canceling-blocking-operations"></a><span data-ttu-id="328a3-103">Annullamento di operazioni di blocco</span><span class="sxs-lookup"><span data-stu-id="328a3-103">Canceling Blocking Operations</span></span>

<span data-ttu-id="328a3-104">Un thread può, in qualsiasi momento, chiamare [WSAIsBlocking](/windows/desktop/api/winsock2/nf-winsock2-wsaisblocking) per determinare se una chiamata di blocco è attualmente in corso.</span><span class="sxs-lookup"><span data-stu-id="328a3-104">A thread may, at any time, call [WSAIsBlocking](/windows/desktop/api/winsock2/nf-winsock2-wsaisblocking) to determine whether or not a blocking call is currently in progress.</span></span> <span data-ttu-id="328a3-105">Questa funzione è implementata all'interno degli shim di compatibilità di Windows Sockets 1,1 e pertanto non ha alcuna controparte SPI. Ovviamente questo è possibile solo quando il provider di servizi utilizza un pseudo blocco, invece del blocco effettivo.</span><span class="sxs-lookup"><span data-stu-id="328a3-105">(This function is implemented within the Windows Sockets 1.1 compatibility shims and hence has no SPI counterpart.) Clearly this is only possible when pseudo blocking, as opposed to true blocking, is being employed by the service provider.</span></span> <span data-ttu-id="328a3-106">Quando necessario, è possibile chiamare [**WSPCancelBlockingCall**](/previous-versions/windows/desktop/legacy/ms742269(v=vs.85)) in qualsiasi momento per annullare qualsiasi operazione di pseudo blocco corrente.</span><span class="sxs-lookup"><span data-stu-id="328a3-106">When necessary, [**WSPCancelBlockingCall**](/previous-versions/windows/desktop/legacy/ms742269(v=vs.85)) may be called at any time to cancel any current pseudo blocking operation.</span></span>

 

 
