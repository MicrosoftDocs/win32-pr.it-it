---
description: Il \_32.dll WS2 (e i protocolli sovrapposti) chiamerà WSPCleanup una volta per ogni chiamata di WSPStartup.
ms.assetid: c3b7b648-5727-47d6-9ddc-9d9f6511949d
title: Pulizia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc294183f964d00ae9ebb1d74b90b346c2ce8fc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307019"
---
# <a name="cleanup"></a><span data-ttu-id="74be4-103">Pulizia</span><span class="sxs-lookup"><span data-stu-id="74be4-103">Cleanup</span></span>

<span data-ttu-id="74be4-104">Il \_32.dll WS2 (e i protocolli sovrapposti) chiamerà [**WSPCleanup**](/previous-versions/windows/hardware/network/ff566270(v=vs.85)) una volta per ogni chiamata di [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup).</span><span class="sxs-lookup"><span data-stu-id="74be4-104">The Ws2\_32.dll (and layered protocols) will call [**WSPCleanup**](/previous-versions/windows/hardware/network/ff566270(v=vs.85)) once for each invocation of [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup).</span></span> <span data-ttu-id="74be4-105">A ogni chiamata, **WSPCleanup** deve decrementare un contatore dei riferimenti per processo e quando il contatore raggiunge lo zero, il provider di servizi deve prepararsi per essere scaricato dalla memoria.</span><span class="sxs-lookup"><span data-stu-id="74be4-105">On each invocation, **WSPCleanup** should decrement a per-process reference counter, and when the counter reaches zero, the service provider must prepare itself to be unloaded from memory.</span></span> <span data-ttu-id="74be4-106">Il primo ordine di business consiste nel completare la trasmissione di tutti i dati non inviati nei socket configurati per una chiusura normale.</span><span class="sxs-lookup"><span data-stu-id="74be4-106">The first order of business is to finish transmitting any unsent data on sockets that are configured for a graceful close.</span></span> <span data-ttu-id="74be4-107">Successivamente, tutte le risorse utilizzate dal provider devono essere liberate.</span><span class="sxs-lookup"><span data-stu-id="74be4-107">Thereafter, any and all resources held by the provider are to be freed.</span></span> <span data-ttu-id="74be4-108">Il provider di servizi deve essere lasciato in uno stato in cui può essere reinizializzato immediatamente da una chiamata a **WSPStartup**.</span><span class="sxs-lookup"><span data-stu-id="74be4-108">The service provider must be left in a state where it can be immediately reinitialized by a call to **WSPStartup**.</span></span>

 

 
