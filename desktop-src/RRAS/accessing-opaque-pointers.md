---
title: Accesso a puntatori opachi
description: I client sono in grado di accedere alle informazioni archiviate nelle destinazioni usando puntatori opachi.
ms.assetid: 1f6af84f-c6c9-4091-8e6b-2c773541ca97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25a3435fd468b41c70105b0b239b35fe24212a7f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515877"
---
# <a name="accessing-opaque-pointers"></a><span data-ttu-id="9b48a-103">Accesso a puntatori opachi</span><span class="sxs-lookup"><span data-stu-id="9b48a-103">Accessing Opaque Pointers</span></span>

<span data-ttu-id="9b48a-104">I client sono in grado di accedere alle informazioni archiviate nelle destinazioni usando puntatori opachi.</span><span class="sxs-lookup"><span data-stu-id="9b48a-104">Clients are able to access the information stored in destinations by using opaque pointers.</span></span> <span data-ttu-id="9b48a-105">Per usare lo spazio di archiviazione, il client deve prima chiamare [**RtmGetOpaqueInformationPointer**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetopaqueinformationpointer) per ottenere il puntatore.</span><span class="sxs-lookup"><span data-stu-id="9b48a-105">To use the storage, the client must first call [**RtmGetOpaqueInformationPointer**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetopaqueinformationpointer) to obtain the pointer.</span></span> <span data-ttu-id="9b48a-106">Ogni volta che è necessaria una modifica alle informazioni, il client deve prima bloccare la destinazione chiamando [**RtmLockDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockdestination) con il parametro *LockDest* impostato su **true**.</span><span class="sxs-lookup"><span data-stu-id="9b48a-106">Whenever a change to the information is necessary, the client must first lock the destination by calling [**RtmLockDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockdestination) with the *LockDest* parameter set to **TRUE**.</span></span> <span data-ttu-id="9b48a-107">Una volta bloccata la destinazione, il client può apportare le modifiche necessarie.</span><span class="sxs-lookup"><span data-stu-id="9b48a-107">Once the destination is locked, the client can make the necessary change.</span></span> <span data-ttu-id="9b48a-108">È possibile sbloccare la destinazione usando un'altra chiamata a **RtmLockDestination** con il parametro *LockDest* impostato su **false**.</span><span class="sxs-lookup"><span data-stu-id="9b48a-108">The destination can be unlocked using another call to **RtmLockDestination** with the *LockDest* parameter set to **FALSE**.</span></span>

<span data-ttu-id="9b48a-109">La funzione [**RtmLockDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockdestination) consente inoltre a un client di utilizzare un blocco di lettura o un blocco di scrittura, utilizzando il parametro *Exclusive* .</span><span class="sxs-lookup"><span data-stu-id="9b48a-109">The [**RtmLockDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlockdestination) function also allows a client to use either a read lock or a write lock, using the *Exclusive* parameter.</span></span> <span data-ttu-id="9b48a-110">Un client deve utilizzare il blocco di scrittura solo quando sta apportando modifiche alle informazioni conservate utilizzando il puntatore opaco.</span><span class="sxs-lookup"><span data-stu-id="9b48a-110">A client should use the write lock only when it is making changes to the information kept using the opaque pointer.</span></span> <span data-ttu-id="9b48a-111">I client possono utilizzare il blocco Read per visualizzare le informazioni del puntatore opaco archiviate in una destinazione.</span><span class="sxs-lookup"><span data-stu-id="9b48a-111">Clients can use the read lock to view the opaque pointer information stored in a destination.</span></span>

<span data-ttu-id="9b48a-112">Per il codice di esempio che illustra come usare queste funzioni, vedere [accedere al puntatore opaco in una destinazione](access-the-opaque-pointer-in-a-destination.md).</span><span class="sxs-lookup"><span data-stu-id="9b48a-112">For sample code that shows how to use these functions, see [Access the Opaque Pointer in a Destination](access-the-opaque-pointer-in-a-destination.md).</span></span>

 

 




