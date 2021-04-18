---
description: Uso \_ \_ del codice del comando di loopback MultiPoint di sio per abilitare o disabilitare il loopback del traffico multipoint.
ms.assetid: 7e11932b-ce9a-4500-888f-8a08ab67b46c
title: IOCTL SIO_MULTIPOINT_LOOPBACK
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c9f0c7527c8c8b8b32b872eccbbbcdc9a3a2c35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309927"
---
# <a name="sio_multipoint_loopback-ioctl"></a><span data-ttu-id="802cb-103">\_IOCTL di loopback MultiPoint di sio \_</span><span class="sxs-lookup"><span data-stu-id="802cb-103">SIO\_MULTIPOINT\_LOOPBACK Ioctl</span></span>

<span data-ttu-id="802cb-104">Quando si \_ usano i socket foglia d in un piano dati senza radice, è in genere consigliabile poter controllare se il traffico inviato viene ricevuto anche sullo stesso socket.</span><span class="sxs-lookup"><span data-stu-id="802cb-104">When d\_leaf sockets are used in a nonrooted data plane, it is generally desirable to be able to control whether traffic sent out is also received back on the same socket.</span></span> <span data-ttu-id="802cb-105">Il \_ codice del comando di loopback MultiPoint di sio \_ per [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) viene usato per abilitare o disabilitare il loopback del traffico multipoint.</span><span class="sxs-lookup"><span data-stu-id="802cb-105">The SIO\_MULTIPOINT\_LOOPBACK command code for [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) is used to enable or disable loopback of multipoint traffic.</span></span>

 

 
