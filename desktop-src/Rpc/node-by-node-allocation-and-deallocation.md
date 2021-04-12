---
title: Allocazione e deallocazione di nodi per nodo
description: L'allocazione nodo per nodo e la deallocazione di strutture di dati dagli Stub è il metodo predefinito di gestione della memoria per tutti i parametri nel client e nel server.
ms.assetid: 04752fd9-438c-4b52-830b-ce136f83b3b8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6cc6b3ff61d4db3ba716664a2ff854e94cb28fc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473638"
---
# <a name="node-by-node-allocation-and-deallocation"></a><span data-ttu-id="8d8fc-103">Allocazione e deallocazione di nodi per nodo</span><span class="sxs-lookup"><span data-stu-id="8d8fc-103">Node-by-Node Allocation and Deallocation</span></span>

<span data-ttu-id="8d8fc-104">L'allocazione nodo per nodo e la deallocazione di strutture di dati dagli Stub è il metodo predefinito di gestione della memoria per tutti i parametri nel client e nel server.</span><span class="sxs-lookup"><span data-stu-id="8d8fc-104">Node-by-node allocation and deallocation of data structures by the stubs is the default method of memory management for all parameters on both the client and the server.</span></span> <span data-ttu-id="8d8fc-105">Sul lato client lo stub alloca ogni nodo con una chiamata separata a [MIDL \_ User \_ allocate](/windows/desktop/Midl/midl-user-allocate-1).</span><span class="sxs-lookup"><span data-stu-id="8d8fc-105">On the client side, the stub allocates each node with a separate call to [midl\_user\_allocate](/windows/desktop/Midl/midl-user-allocate-1).</span></span> <span data-ttu-id="8d8fc-106">Sul lato server, anziché chiamare **MIDL \_ User \_ allocate**, viene usata la memoria privata quando possibile.</span><span class="sxs-lookup"><span data-stu-id="8d8fc-106">On the server side, rather than calling **midl\_user\_allocate**, private memory is used whenever possible.</span></span> <span data-ttu-id="8d8fc-107">Se viene chiamato l' **\_ utente MIDL \_ allocate** , gli stub del server chiameranno l' **\_ utente MIDL \_ gratuitamente** per liberare i dati.</span><span class="sxs-lookup"><span data-stu-id="8d8fc-107">If **midl\_user\_allocate** is called, the server stubs will call **midl\_user\_free** to free the data.</span></span> <span data-ttu-id="8d8fc-108">Nella maggior parte dei casi, l'utilizzo dell'allocazione e della deallocazione di nodi anziché di **\[ allocare (tutti i \_ nodi) \]** comporterà un miglioramento delle prestazioni degli stub lato server.</span><span class="sxs-lookup"><span data-stu-id="8d8fc-108">In most cases, using node-by-node allocation and deallocation instead of using **\[allocate (all\_nodes)\]** will result in increased performance of the server side stubs.</span></span>

 

 