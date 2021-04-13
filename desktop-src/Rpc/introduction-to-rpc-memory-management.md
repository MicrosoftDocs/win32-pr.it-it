---
title: Introduzione alla gestione della memoria RPC
description: Introduzione alla gestione della memoria RPC (Remote Procedure Call).
ms.assetid: 3474d79c-93ef-4221-b9ea-9173978e2929
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94ac4b6aecb2fd78448ebe31c72587fafb8f6fde
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338711"
---
# <a name="introduction-to-rpc-memory-management"></a><span data-ttu-id="8fb30-103">Introduzione alla gestione della memoria RPC</span><span class="sxs-lookup"><span data-stu-id="8fb30-103">Introduction to RPC Memory Management</span></span>

<span data-ttu-id="8fb30-104">Nel contesto di RPC, la gestione della memoria comporta:</span><span class="sxs-lookup"><span data-stu-id="8fb30-104">In the context of RPC, memory management involves:</span></span>

-   <span data-ttu-id="8fb30-105">Allocazione e deallocazione della memoria necessaria per simulare un singolo spazio di indirizzi concettuale tra il client e il server nei diversi spazi di indirizzi dei thread del client e del server.</span><span class="sxs-lookup"><span data-stu-id="8fb30-105">Allocating and deallocating the memory needed to simulate a single conceptual address space between the client and the server in the different address spaces of the client and server's threads.</span></span>
-   <span data-ttu-id="8fb30-106">Determinare quale componente software è responsabile della gestione della memoria, dell'applicazione o dello stub generato da MIDL.</span><span class="sxs-lookup"><span data-stu-id="8fb30-106">Determining which software component is responsible for managing memory — the application or the MIDL-generated stub.</span></span>
-   <span data-ttu-id="8fb30-107">Selezione degli attributi MIDL che influiscono sulla gestione della memoria: attributi direzionali, attributi del puntatore, attributi di matrice e \[ [ \_ numero di byte](/windows/desktop/Midl/byte-count)degli attributi ACF \] , \[ [allocate](/windows/desktop/Midl/allocate) \] e \[ [enable \_ allocate](/windows/desktop/Midl/enable-allocate) \] .</span><span class="sxs-lookup"><span data-stu-id="8fb30-107">Selecting MIDL attributes that affect memory management: directional attributes, pointer attributes, array attributes, and the ACF attributes \[ [byte\_count](/windows/desktop/Midl/byte-count)\], \[ [allocate](/windows/desktop/Midl/allocate)\], and \[ [enable\_allocate](/windows/desktop/Midl/enable-allocate)\].</span></span>

<span data-ttu-id="8fb30-108">Quando un programma chiama una funzione o una routine nello spazio degli indirizzi, la gestione della memoria è più semplice che in un'applicazione distribuita.</span><span class="sxs-lookup"><span data-stu-id="8fb30-108">When a program calls a function or procedure in its address space, memory management is more straightforward than in a distributed application.</span></span> <span data-ttu-id="8fb30-109">Per illustrare, il diagramma seguente illustra un albero binario.</span><span class="sxs-lookup"><span data-stu-id="8fb30-109">To illustrate, the following diagram depicts a binary tree.</span></span> <span data-ttu-id="8fb30-110">Per passare la struttura dei dati a una routine nello spazio degli indirizzi, un programma passa semplicemente un puntatore alla radice dell'albero.</span><span class="sxs-lookup"><span data-stu-id="8fb30-110">To pass this data structure to a procedure in its address space, a program simply passes a pointer to the root of the tree.</span></span>

![struttura ad albero binaria con puntatori ai dati della struttura ospitati alla radice dell'albero](images/bintree.png)

<span data-ttu-id="8fb30-112">Le applicazioni RPC client/server condividono i dati tra due spazi di memoria diversi.</span><span class="sxs-lookup"><span data-stu-id="8fb30-112">Client/server RPC applications share data across two different memory spaces.</span></span> <span data-ttu-id="8fb30-113">Questi spazi di memoria possono o non ritrovarsi nello stesso computer.</span><span class="sxs-lookup"><span data-stu-id="8fb30-113">These memory spaces may or may not be on the same computer.</span></span> <span data-ttu-id="8fb30-114">In entrambi i casi, il client e il server non dispongono di accesso diretto allo spazio di memoria dell'altro.</span><span class="sxs-lookup"><span data-stu-id="8fb30-114">Either way, the client and server have no direct access to each other's memory space.</span></span> <span data-ttu-id="8fb30-115">La RPC dipende dalla capacità di simulare lo spazio degli indirizzi del programma client nello spazio degli indirizzi del programma server.</span><span class="sxs-lookup"><span data-stu-id="8fb30-115">RPC depends on the ability to simulate the client program's address space in the server program's address space.</span></span> <span data-ttu-id="8fb30-116">Deve inoltre restituire dati, inclusi i dati nuovi e modificati, dal server alla memoria del client.</span><span class="sxs-lookup"><span data-stu-id="8fb30-116">It must also return data, including new and changed data, from the server to the client memory.</span></span>

<span data-ttu-id="8fb30-117">Nei casi come l'albero binario illustrato nel diagramma precedente, non è sufficiente passare un puntatore al nodo radice a una procedura remota.</span><span class="sxs-lookup"><span data-stu-id="8fb30-117">In cases such as the binary tree depicted in the preceding diagram, it is not sufficient to pass a pointer to the root node to a remote procedure.</span></span> <span data-ttu-id="8fb30-118">Il programma o gli stub devono passare l'intero albero allo spazio degli indirizzi del server affinché la procedura remota agisca su di essa.</span><span class="sxs-lookup"><span data-stu-id="8fb30-118">Either the program or the stubs must pass the entire tree to the server's address space for the remote procedure to operate on it.</span></span>

 

 