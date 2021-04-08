---
title: Pipe asincrone
description: L'utilizzo di parametri pipe con RPC asincrono consente di trasmettere i dati in modo incrementale, così come diventano disponibili, senza vincolare il client e il server.
ms.assetid: e5c466b8-c0b0-4fa8-8867-d0715fd614b2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be9d6dd5a3e8de7d5c4ad233a577187a49d04ed8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729431"
---
# <a name="asynchronous-pipes"></a><span data-ttu-id="bb1b2-103">Pipe asincrone</span><span class="sxs-lookup"><span data-stu-id="bb1b2-103">Asynchronous Pipes</span></span>

<span data-ttu-id="bb1b2-104">L'utilizzo di parametri [pipe](/windows/desktop/Midl/pipe) con RPC asincrono consente di trasmettere i dati in modo incrementale, così come diventano disponibili, senza vincolare il client e il server.</span><span class="sxs-lookup"><span data-stu-id="bb1b2-104">Using [pipe](/windows/desktop/Midl/pipe) parameters with asynchronous RPC allows you to transmit data incrementally, as it becomes available, without tying up the client and server.</span></span> <span data-ttu-id="bb1b2-105">Questa operazione è particolarmente utile quando si dispone di una grande quantità di dati da trasferire, combinati con un client lento, un server lento o una rete lenta.</span><span class="sxs-lookup"><span data-stu-id="bb1b2-105">This is particularly useful when you have a large amount of data to transfer, combined with a slow client, a slow server, or a slow network.</span></span> <span data-ttu-id="bb1b2-106">Se si usa una pipe in una chiamata di funzione asincrona, è, per definizione, una pipe asincrona.</span><span class="sxs-lookup"><span data-stu-id="bb1b2-106">If you use a pipe in an asynchronous function call, it is, by definition, an asynchronous pipe.</span></span> <span data-ttu-id="bb1b2-107">Le pipe sincrone non sono supportate insieme alle funzioni asincrone.</span><span class="sxs-lookup"><span data-stu-id="bb1b2-107">Synchronous pipes are not supported in conjunction with asynchronous functions.</span></span>

<span data-ttu-id="bb1b2-108">Diversamente dalle pipe convenzionali (sincrone), in cui il server gestisce tutti i dettagli relativi all'invio e alla ricezione dei dati della pipe, le pipe asincrone sono simmetriche.</span><span class="sxs-lookup"><span data-stu-id="bb1b2-108">Unlike conventional (synchronous) pipes where the server handles all the details of sending and receiving pipe data, asynchronous pipes are symmetrical.</span></span> <span data-ttu-id="bb1b2-109">Ovvero sia il client che il server possono eseguire il push e il pull dei dati attraverso la pipe.</span><span class="sxs-lookup"><span data-stu-id="bb1b2-109">That is, both the client and the server can push and pull data through the pipe.</span></span>

> [!Note]  
> <span data-ttu-id="bb1b2-110">I parametri pipe possono essere passati solo per riferimento.</span><span class="sxs-lookup"><span data-stu-id="bb1b2-110">Pipe parameters can only be passed by reference.</span></span> <span data-ttu-id="bb1b2-111">Anche se il file IDL Mostra i parametri della [pipe](/windows/desktop/Midl/pipe) passati per valore, gli stub generati accetteranno parametri pipe solo per riferimento.</span><span class="sxs-lookup"><span data-stu-id="bb1b2-111">Even if the IDL file shows [pipe](/windows/desktop/Midl/pipe) parameters being passed by value, the generated stubs will accept pipe parameters by reference only.</span></span>

 

<span data-ttu-id="bb1b2-112">Nella discussione seguente sulle pipe asincrone si presuppone una certa familiarità con il costruttore del tipo di pipe.</span><span class="sxs-lookup"><span data-stu-id="bb1b2-112">In the following discussion of asynchronous pipes, familiarity with the pipe type constructor is assumed.</span></span> <span data-ttu-id="bb1b2-113">Per ulteriori informazioni sulle procedure di pipe descritte in questi argomenti, vedere [pipe](pipes.md).</span><span class="sxs-lookup"><span data-stu-id="bb1b2-113">For more information on the pipe procedures described in these topics, see [Pipes](pipes.md).</span></span>

 

 