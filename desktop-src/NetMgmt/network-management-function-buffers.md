---
title: Buffer della funzione di gestione di rete
description: La libreria di runtime RPC gestisce i buffer richiesti dalle funzioni di gestione della rete per il recupero dei dati a 32 bit, come indicato di seguito.
ms.assetid: f27e6cf5-f26a-4e6c-8d77-873bff6cc8e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 385382d12aa5b5c8c7c93b9a833f684d913c5783
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221572"
---
# <a name="network-management-function-buffers"></a><span data-ttu-id="a3e34-103">Buffer della funzione di gestione di rete</span><span class="sxs-lookup"><span data-stu-id="a3e34-103">Network Management Function Buffers</span></span>

<span data-ttu-id="a3e34-104">La libreria di runtime RPC gestisce i buffer richiesti dalle funzioni di gestione della rete per il recupero dei dati a 32 bit, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="a3e34-104">The RPC run-time library handles the buffers required by the 32-bit data retrieval network management functions as follows:</span></span>

-   <span data-ttu-id="a3e34-105">**Invio di dati al server** (dati specificati da \[ nei \] parametri in).</span><span class="sxs-lookup"><span data-stu-id="a3e34-105">**Sending data to the server** (data specified by \[in\] parameters).</span></span>

    <span data-ttu-id="a3e34-106">Il chiamante deve allocare e deallocare il buffer per la struttura delle informazioni (o le strutture) pertinente e passare una variabile puntatore alla funzione.</span><span class="sxs-lookup"><span data-stu-id="a3e34-106">The caller must allocate and deallocate the buffer for the relevant information structure (or structures) and pass a pointer variable to the function.</span></span> <span data-ttu-id="a3e34-107">Non è necessario che il chiamante specifichi la lunghezza del buffer.</span><span class="sxs-lookup"><span data-stu-id="a3e34-107">The caller does not need to specify the buffer length.</span></span>

    <span data-ttu-id="a3e34-108">Esempio: [ **NetGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadd)</span><span class="sxs-lookup"><span data-stu-id="a3e34-108">Example: [**NetGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadd)</span></span>

-   <span data-ttu-id="a3e34-109">**Recupero dei dati dal server** (dati specificati da \[ parametri out \] ).</span><span class="sxs-lookup"><span data-stu-id="a3e34-109">**Retrieving data from the server** (data specified by \[out\] parameters).</span></span>

    <span data-ttu-id="a3e34-110">Il sistema alloca il buffer per le informazioni restituite.</span><span class="sxs-lookup"><span data-stu-id="a3e34-110">The system allocates the buffer for the returned information.</span></span> <span data-ttu-id="a3e34-111">Il chiamante deve passare una variabile puntatore alla funzione nell'input.</span><span class="sxs-lookup"><span data-stu-id="a3e34-111">The caller must pass a pointer variable to the function on input.</span></span> <span data-ttu-id="a3e34-112">In esito positivo, il puntatore riceve l'indirizzo del buffer allocato dal sistema che contiene le informazioni restituite.</span><span class="sxs-lookup"><span data-stu-id="a3e34-112">On successful return, the pointer receives the address of the system-allocated buffer that contains the returned information.</span></span> <span data-ttu-id="a3e34-113">In questo modo il codice chiamante viene semplificato, perché il chiamante non deve stimare la dimensione del buffer o ridimensionare il buffer e riemettere la funzione.</span><span class="sxs-lookup"><span data-stu-id="a3e34-113">This simplifies the calling code, because the caller does not need to estimate the size of the buffer, or resize the buffer and reissue the function.</span></span>

    <span data-ttu-id="a3e34-114">Al termine dell'elaborazione delle informazioni restituite, il chiamante deve liberare la memoria allocata dal sistema chiamando la funzione [**NetApiBufferFree**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferfree) .</span><span class="sxs-lookup"><span data-stu-id="a3e34-114">When the caller has finished processing the returned information, it must free the system-allocated memory by calling the [**NetApiBufferFree**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferfree) function.</span></span> <span data-ttu-id="a3e34-115">Per ulteriori informazioni su come specificare le dimensioni del buffer, vedere [lunghezze del buffer della funzione di gestione di rete](network-management-function-buffer-lengths.md).</span><span class="sxs-lookup"><span data-stu-id="a3e34-115">For more information about specifying buffer sizes, see [Network Management Function Buffer Lengths](network-management-function-buffer-lengths.md).</span></span>

    <span data-ttu-id="a3e34-116">Esempio: [ **NetGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupenum)</span><span class="sxs-lookup"><span data-stu-id="a3e34-116">Example: [**NetGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupenum)</span></span>

 

 




