---
title: Puntatori e RPC
description: È molto efficiente usare i puntatori come parametri della funzione C.
ms.assetid: 5792bd45-9c2a-4dd2-b050-17082fd0c929
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbacce89046e2808acad539d19bbdcfeb1bc99c1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856637"
---
# <a name="pointers-and-rpc"></a><span data-ttu-id="a477d-103">Puntatori e RPC</span><span class="sxs-lookup"><span data-stu-id="a477d-103">Pointers and RPC</span></span>

<span data-ttu-id="a477d-104">È molto efficiente usare i puntatori come parametri della funzione C.</span><span class="sxs-lookup"><span data-stu-id="a477d-104">It is very efficient to use pointers as C-function parameters.</span></span> <span data-ttu-id="a477d-105">Il puntatore costa solo pochi byte e può essere usato per accedere a una grande quantità di memoria.</span><span class="sxs-lookup"><span data-stu-id="a477d-105">The pointer costs only a few bytes and can be used to access a large amount of memory.</span></span> <span data-ttu-id="a477d-106">Tuttavia, in un'applicazione distribuita, le procedure client e server si trovano in spazi di indirizzi diversi, ma possono trovarsi in computer diversi.</span><span class="sxs-lookup"><span data-stu-id="a477d-106">However, in a distributed application, the client and server procedures reside in different address spaces—they can be on different computers.</span></span> <span data-ttu-id="a477d-107">Pertanto, il client e il server in genere non hanno accesso allo stesso spazio di memoria.</span><span class="sxs-lookup"><span data-stu-id="a477d-107">Therefore, the client and the server usually do not have access to the same memory space.</span></span>

<span data-ttu-id="a477d-108">Quando uno dei parametri della procedura remota è un puntatore a un oggetto, il client deve trasmettere una copia di tale oggetto e il relativo puntatore al server.</span><span class="sxs-lookup"><span data-stu-id="a477d-108">When one of the remote procedure's parameters is a pointer to an object, the client must transmit a copy of that object and its pointer to the server.</span></span> <span data-ttu-id="a477d-109">Se la procedura remota modifica l'oggetto tramite il puntatore, il server restituisce il puntatore e la copia modificata.</span><span class="sxs-lookup"><span data-stu-id="a477d-109">If the remote procedure modifies the object through its pointer, the server returns the pointer and its modified copy.</span></span>

<span data-ttu-id="a477d-110">MIDL offre attributi puntatore per ridurre al minimo la quantità di overhead necessario e le dimensioni dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a477d-110">MIDL offers pointer attributes to minimize the amount of required overhead and the size of your application.</span></span> <span data-ttu-id="a477d-111">Questa sezione illustra lo scopo e gli usi degli attributi del puntatore MIDL.</span><span class="sxs-lookup"><span data-stu-id="a477d-111">This section discusses the purpose and uses of MIDL pointer attributes.</span></span> <span data-ttu-id="a477d-112">Vengono inoltre fornite informazioni sulla gestione dei puntatori nelle applicazioni RPC.</span><span class="sxs-lookup"><span data-stu-id="a477d-112">It also presents information on pointer handling in RPC applications.</span></span> <span data-ttu-id="a477d-113">È divisa negli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="a477d-113">It is divided into the following topics:</span></span>

-   [<span data-ttu-id="a477d-114">Tipi di puntatori</span><span class="sxs-lookup"><span data-stu-id="a477d-114">Kinds of Pointers</span></span>](kinds-of-pointers.md)
-   [<span data-ttu-id="a477d-115">Puntatori e allocazione di memoria</span><span class="sxs-lookup"><span data-stu-id="a477d-115">Pointers and Memory Allocation</span></span>](pointers-and-memory-allocation.md)
-   [<span data-ttu-id="a477d-116">Tipi di puntatore predefiniti</span><span class="sxs-lookup"><span data-stu-id="a477d-116">Default Pointer Types</span></span>](default-pointer-types.md)
-   [<span data-ttu-id="a477d-117">Puntatore-ereditarietà del tipo di attributo</span><span class="sxs-lookup"><span data-stu-id="a477d-117">Pointer-Attribute Type Inheritance</span></span>](pointer-attribute-type-inheritance.md)

 

 




