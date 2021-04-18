---
description: Poiché gli elementi duplicati sono i descrittori di socket e non i socket sottostanti, tutti gli Stati associati a un socket vengono mantenuti in comune in tutti i descrittori.
ms.assetid: f3a2cd5a-bc3a-4aeb-8606-7b8aa6afb105
title: Più handle per un singolo socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2356f24a69d132f87e0f6543f61509ff12acba5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306928"
---
# <a name="multiple-handles-to-a-single-socket"></a><span data-ttu-id="80387-103">Più handle per un singolo socket</span><span class="sxs-lookup"><span data-stu-id="80387-103">Multiple Handles to a Single Socket</span></span>

<span data-ttu-id="80387-104">Poiché gli elementi duplicati sono i descrittori di socket e non i socket sottostanti, tutti gli Stati associati a un socket vengono mantenuti in comune in tutti i descrittori.</span><span class="sxs-lookup"><span data-stu-id="80387-104">Since what are duplicated are the socket descriptors and not the underlying sockets, all of the states associated with a socket are held in common across all the descriptors.</span></span> <span data-ttu-id="80387-105">Ad esempio, un'operazione [**WSPSetSockOpt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85)) eseguita usando un descrittore è successivamente visibile usando un [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85)) da uno o tutti i descrittori.</span><span class="sxs-lookup"><span data-stu-id="80387-105">For example a [**WSPSetSockOpt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85)) operation performed using one descriptor is subsequently visible using a [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85)) from any or all descriptors.</span></span>

<span data-ttu-id="80387-106">La notifica sui socket condivisi è soggetta ai vincoli usuali di [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) e [**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="80387-106">Notification on shared sockets is subject to the usual constraints of [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) and [**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)).</span></span> <span data-ttu-id="80387-107">Quando si esegue una di queste chiamate utilizzando uno dei descrittori condivisi, viene annullata la registrazione di eventi precedente per il socket, indipendentemente dal descrittore utilizzato per effettuare la registrazione.</span><span class="sxs-lookup"><span data-stu-id="80387-107">Issuing either of these calls using any of the shared descriptors cancels any previous event registration for the socket, regardless of which descriptor was used to make that registration.</span></span> <span data-ttu-id="80387-108">Quindi, ad esempio, non sarebbe possibile avere un processo di ricezione di eventi di \_ lettura FD ed elaborare B ricevere \_ eventi di scrittura FD.</span><span class="sxs-lookup"><span data-stu-id="80387-108">Thus, for example, it would not be possible to have process A receive FD\_READ events and process B receive FD\_WRITE events.</span></span> <span data-ttu-id="80387-109">Per le situazioni in cui è necessario un coordinamento rigoroso, è consigliabile che gli sviluppatori utilizzino i thread anziché processi distinti.</span><span class="sxs-lookup"><span data-stu-id="80387-109">For situations when such tight coordination is required, it is suggested that developers consider using threads instead of separate processes.</span></span>

 

 
