---
title: Implementazione di Client-Side pipe
description: Implementazione della pipe lato client in RPC (Remote Procedure Call).
ms.assetid: d790f859-47a9-4b6c-a218-8cbe05db21b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5666656f1f7296c252395255c17902a91cb32a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856685"
---
# <a name="client-side-pipe-implementation"></a><span data-ttu-id="a21fa-103">Implementazione di Client-Side pipe</span><span class="sxs-lookup"><span data-stu-id="a21fa-103">Client-Side Pipe Implementation</span></span>

<span data-ttu-id="a21fa-104">L'applicazione client deve implementare le seguenti procedure, che lo stub client chiamerà durante il trasferimento dei dati:</span><span class="sxs-lookup"><span data-stu-id="a21fa-104">The client application must implement the following procedures, which the client stub will call during data transfer:</span></span>

-   <span data-ttu-id="a21fa-105">Procedura pull (per una pipe di input)</span><span class="sxs-lookup"><span data-stu-id="a21fa-105">A pull procedure (for an input pipe)</span></span>
-   <span data-ttu-id="a21fa-106">Procedura push (per una pipe di output)</span><span class="sxs-lookup"><span data-stu-id="a21fa-106">A push procedure (for an output pipe)</span></span>
-   <span data-ttu-id="a21fa-107">Una procedura di allocazione per l'allocazione di un buffer per i dati di trasferimento</span><span class="sxs-lookup"><span data-stu-id="a21fa-107">An alloc procedure to allocate a buffer for the transfer data</span></span>

<span data-ttu-id="a21fa-108">Tutte queste procedure devono usare gli argomenti specificati dal file di intestazione generato da MIDL.</span><span class="sxs-lookup"><span data-stu-id="a21fa-108">All of these procedures must use the arguments specified by the MIDL-generated header file.</span></span> <span data-ttu-id="a21fa-109">Inoltre, l'applicazione client deve avere una variabile di stato per identificare dove individuare o inserire i dati.</span><span class="sxs-lookup"><span data-stu-id="a21fa-109">In addition, the client application must have a state variable to identify where to locate or place data.</span></span>

<span data-ttu-id="a21fa-110">La procedura di allocazione può anche essere semplice o complessa se necessario.</span><span class="sxs-lookup"><span data-stu-id="a21fa-110">The alloc procedure can also be as simple or as complex as needed.</span></span> <span data-ttu-id="a21fa-111">Ad esempio, può restituire un puntatore allo stesso buffer ogni volta che lo stub chiama la funzione oppure può allocare una quantità di memoria diversa ogni volta.</span><span class="sxs-lookup"><span data-stu-id="a21fa-111">For example, it can return a pointer to the same buffer every time the stub calls the function, or it can allocate a different amount of memory each time.</span></span> <span data-ttu-id="a21fa-112">Se i dati sono già nel formato corretto, ad esempio una matrice di elementi pipe, è possibile coordinare la procedura di allocazione con la procedura pull per allocare un buffer che contiene già i dati.</span><span class="sxs-lookup"><span data-stu-id="a21fa-112">If your data is already in the proper form (an array of pipe elements, for example) you can coordinate the alloc procedure with the pull procedure to allocate a buffer that already contains the data.</span></span> <span data-ttu-id="a21fa-113">In tal caso, la procedura pull potrebbe essere una routine vuota.</span><span class="sxs-lookup"><span data-stu-id="a21fa-113">In that case, your pull procedure could be an empty routine.</span></span>

<span data-ttu-id="a21fa-114">L'allocazione del buffer deve essere in byte.</span><span class="sxs-lookup"><span data-stu-id="a21fa-114">The buffer allocation must be in bytes.</span></span> <span data-ttu-id="a21fa-115">Le procedure push e pull, d'altra parte, modificano gli elementi, le cui dimensioni in byte dipendono da come sono state definite.</span><span class="sxs-lookup"><span data-stu-id="a21fa-115">The push and pull procedures, on the other hand, manipulate elements, whose size in bytes depends on how they were defined.</span></span>

<span data-ttu-id="a21fa-116">In questa sezione viene illustrata l'implementazione client dei pipe di input e di output nelle seguenti sezioni:</span><span class="sxs-lookup"><span data-stu-id="a21fa-116">This section discusses the client implementation of input and output pipes in the following sections:</span></span>

-   [<span data-ttu-id="a21fa-117">Implementazione di pipe di input nel client</span><span class="sxs-lookup"><span data-stu-id="a21fa-117">Implementing Input Pipes on the Client</span></span>](implementing-input-pipes-on-the-client.md)
-   [<span data-ttu-id="a21fa-118">Implementazione di pipe di output nel client</span><span class="sxs-lookup"><span data-stu-id="a21fa-118">Implementing Output Pipes on the Client</span></span>](implementing-output-pipes-on-the-client.md)

 

 




