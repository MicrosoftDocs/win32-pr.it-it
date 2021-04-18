---
description: Uso \_ \_ del codice del comando per ambito multicast Sio per specificare l'ambito in cui deve essere eseguito il multicast.
ms.assetid: 3acec987-9cb4-446c-af6e-ea0e6a96e70c
title: IOCTL SIO_MULTICAST_SCOPE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90d1fd6f2bea76d095ea88d66c0ac029fb9168ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315779"
---
# <a name="sio_multicast_scope-ioctl"></a><span data-ttu-id="b2c3a-103">\_ \_ IOCTL ambito multicast sio</span><span class="sxs-lookup"><span data-stu-id="b2c3a-103">SIO\_MULTICAST\_SCOPE Ioctl</span></span>

<span data-ttu-id="b2c3a-104">Quando viene utilizzato il multicast, in genere è necessario specificare l'ambito sul quale deve essere eseguito il multicast.</span><span class="sxs-lookup"><span data-stu-id="b2c3a-104">When multicasting is employed, it is usually necessary to specify the scope over which the multicast should occur.</span></span> <span data-ttu-id="b2c3a-105">Questo ambito è definito come il numero di segmenti di rete indirizzati da coprire.</span><span class="sxs-lookup"><span data-stu-id="b2c3a-105">Here scope is defined to be the number of routed network segments to be covered.</span></span> <span data-ttu-id="b2c3a-106">Il \_ codice del \_ comando per l'ambito multicast Sio per [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) viene usato per controllare questa operazione.</span><span class="sxs-lookup"><span data-stu-id="b2c3a-106">The SIO\_MULTICAST\_SCOPE command code for [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) is used to control this.</span></span> <span data-ttu-id="b2c3a-107">Un ambito pari a zero indicherà che la trasmissione multicast non verrà distribuita in transito, ma potrebbe essere divulgata tra i socket all'interno dell'host locale.</span><span class="sxs-lookup"><span data-stu-id="b2c3a-107">A scope of zero would indicate that the multicast transmission would not be placed on the wire but could be disseminated across sockets within the local host.</span></span> <span data-ttu-id="b2c3a-108">Un valore di ambito pari a uno (impostazione predefinita) indica che la trasmissione verrà posizionata in transito, ma non incrocierà alcun router.</span><span class="sxs-lookup"><span data-stu-id="b2c3a-108">A scope value of one (the default) indicates that the transmission will be placed on the wire, but will not cross any routers.</span></span> <span data-ttu-id="b2c3a-109">I valori di ambito più elevati determinano il numero di router che possono essere superati.</span><span class="sxs-lookup"><span data-stu-id="b2c3a-109">Higher scope values determine the number of routers that may be crossed.</span></span> <span data-ttu-id="b2c3a-110">Si noti che corrisponde al parametro time-to-Live (TTL) in multicast IP.</span><span class="sxs-lookup"><span data-stu-id="b2c3a-110">Note that this corresponds to the time-to-live (TTL) parameter in IP multicasting.</span></span>

 

 
