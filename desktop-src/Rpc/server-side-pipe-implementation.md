---
title: Implementazione di Server-Side pipe
description: I programmi server per le applicazioni distribuite che utilizzano pipe non devono implementare alcuna funzione push, pull o allocazione.
ms.assetid: de733075-5767-4d46-b294-089c7e3cc695
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6927350e10061850c5fac0ab0db7c18570dd2bab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044972"
---
# <a name="server-side-pipe-implementation"></a><span data-ttu-id="205d5-103">Implementazione di Server-Side pipe</span><span class="sxs-lookup"><span data-stu-id="205d5-103">Server-Side Pipe Implementation</span></span>

<span data-ttu-id="205d5-104">I programmi server per le applicazioni distribuite che utilizzano pipe non devono implementare alcuna funzione push, pull o allocazione.</span><span class="sxs-lookup"><span data-stu-id="205d5-104">Server programs for distributed applications that use pipes need not implement any push, pull, or alloc functions.</span></span> <span data-ttu-id="205d5-105">Devono contenere procedure che i client possono richiamare in remoto per avviare i trasferimenti di dati.</span><span class="sxs-lookup"><span data-stu-id="205d5-105">They do need to contain procedures that clients can invoke remotely to initiate data transfers.</span></span> <span data-ttu-id="205d5-106">Negli argomenti seguenti, in questa sezione viene illustrato come è possibile implementare le procedure remote del server.</span><span class="sxs-lookup"><span data-stu-id="205d5-106">In the following topics, this section explains how the server's remote procedures can be implemented.</span></span>

-   [<span data-ttu-id="205d5-107">Implementazione di pipe di input nel server</span><span class="sxs-lookup"><span data-stu-id="205d5-107">Implementing Input Pipes on the Server</span></span>](implementing-input-pipes-on-the-server.md)
-   [<span data-ttu-id="205d5-108">Implementazione di pipe di output nel server</span><span class="sxs-lookup"><span data-stu-id="205d5-108">Implementing Output Pipes on the Server</span></span>](implementing-output-pipes-on-the-server.md)

 

 




