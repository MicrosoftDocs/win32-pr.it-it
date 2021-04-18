---
description: Un processo può chiamare WSPCloseSocket su un socket duplicato e il descrittore verrà deallocato. Il socket sottostante, tuttavia, resterà aperto fino a quando non viene chiamato WSPCloseSocket sull'ultimo descrittore rimanente.
ms.assetid: dff1e932-5e87-4ec5-995d-686d20ba6236
title: Conteggio dei riferimenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72d9ef7b3e5e31cc7941d30c47f107fc068489ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309941"
---
# <a name="reference-counting"></a><span data-ttu-id="ca823-104">Conteggio dei riferimenti</span><span class="sxs-lookup"><span data-stu-id="ca823-104">Reference Counting</span></span>

<span data-ttu-id="ca823-105">Un processo può chiamare [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) su un socket duplicato e il descrittore verrà deallocato.</span><span class="sxs-lookup"><span data-stu-id="ca823-105">A process may call [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) on a duplicated socket and the descriptor will become deallocated.</span></span> <span data-ttu-id="ca823-106">Il socket sottostante, tuttavia, resterà aperto fino a quando non viene chiamato **WSPCloseSocket** sull'ultimo descrittore rimanente.</span><span class="sxs-lookup"><span data-stu-id="ca823-106">The underlying socket, however, will remain open until **WSPCloseSocket** is called on the last remaining descriptor.</span></span>

 

 
