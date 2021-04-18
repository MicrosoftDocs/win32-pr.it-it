---
title: Ricerca del programma server
description: Quando il tempo di esecuzione RPC lato client si connette a un sistema host server richiesto nell'handle di binding, la libreria di runtime RPC client trova il processo server.
ms.assetid: 0c863018-746a-4793-abe7-1838d988e0f4
keywords:
- RPC (Remote Procedure Call), attività, ricerca del programma server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73b822dbca1a927e13f01d7c91aa7c78267db4d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298341"
---
# <a name="finding-the-server-program"></a><span data-ttu-id="2e6c5-104">Ricerca del programma server</span><span class="sxs-lookup"><span data-stu-id="2e6c5-104">Finding the Server Program</span></span>

<span data-ttu-id="2e6c5-105">Quando il tempo di esecuzione RPC lato client si connette a un sistema host server richiesto nell'handle di binding, la libreria di runtime RPC client trova il processo server.</span><span class="sxs-lookup"><span data-stu-id="2e6c5-105">After the client side RPC run time connects to a server host system requested in the binding handle, the client RPC run-time library finds the server process.</span></span> <span data-ttu-id="2e6c5-106">A tale scopo, viene eseguita una query sulla mappa dell'endpoint sul sistema host del server.</span><span class="sxs-lookup"><span data-stu-id="2e6c5-106">To do this, it queries the endpoint map on the server host system.</span></span> <span data-ttu-id="2e6c5-107">La mappa dell'endpoint contiene informazioni sull'endpoint su cui il server è in ascolto.</span><span class="sxs-lookup"><span data-stu-id="2e6c5-107">The endpoint map contains information about which endpoint the server is listening to.</span></span>

 

 




