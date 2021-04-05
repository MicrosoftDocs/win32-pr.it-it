---
title: Uso di RPC asincrone con pipe DCE
description: Microsoft RPC supporta l'uso di pipe DCE. Sebbene condividono un nome simile, le pipe DCE non sono correlate alle named pipe. Le named pipe sono un protocollo di trasporto. Le pipe DCE sono un metodo indipendente dal protocollo della comunicazione client/server.
ms.assetid: 9de4f6dc-0aa9-446e-b68c-e0d1e247fea7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43e9c98f4d4191a064d78cff2c918077f27d676f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044668"
---
# <a name="using-asynchronous-rpc-with-dce-pipes"></a><span data-ttu-id="a7fce-106">Uso di RPC asincrone con pipe DCE</span><span class="sxs-lookup"><span data-stu-id="a7fce-106">Using Asynchronous RPC with DCE Pipes</span></span>

<span data-ttu-id="a7fce-107">Microsoft RPC supporta l'uso di pipe DCE.</span><span class="sxs-lookup"><span data-stu-id="a7fce-107">Microsoft RPC supports the use of DCE pipes.</span></span> <span data-ttu-id="a7fce-108">Sebbene condividono un nome simile, le pipe DCE non sono correlate alle [named pipe](asynchronous-rpc-over-the-named-pipe-protocol.md).</span><span class="sxs-lookup"><span data-stu-id="a7fce-108">Although they share a similar name, DCE pipes are unrelated to [named pipes](asynchronous-rpc-over-the-named-pipe-protocol.md).</span></span> <span data-ttu-id="a7fce-109">Le named pipe sono un protocollo di trasporto.</span><span class="sxs-lookup"><span data-stu-id="a7fce-109">Named pipes are a transport protocol.</span></span> <span data-ttu-id="a7fce-110">Le pipe DCE sono un metodo indipendente dal protocollo della comunicazione client/server.</span><span class="sxs-lookup"><span data-stu-id="a7fce-110">DCE pipes are a protocol-independent method of client/server communication.</span></span>

<span data-ttu-id="a7fce-111">Questa sezione presenta una discussione sulla RPC che usa le pipe DCE asincrone.</span><span class="sxs-lookup"><span data-stu-id="a7fce-111">This section presents a discussion of RPC using asynchronous DCE pipes.</span></span> <span data-ttu-id="a7fce-112">È divisa negli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="a7fce-112">It is divided into the following topics:</span></span>

-   [<span data-ttu-id="a7fce-113">Pipe asincrone</span><span class="sxs-lookup"><span data-stu-id="a7fce-113">Asynchronous Pipes</span></span>](asynchronous-pipes.md)
-   [<span data-ttu-id="a7fce-114">Dichiarazione di pipe asincrone</span><span class="sxs-lookup"><span data-stu-id="a7fce-114">Declaring Asynchronous Pipes</span></span>](declaring-asynchronous-pipes.md)
-   [<span data-ttu-id="a7fce-115">Gestione della pipe asincrona sul lato client</span><span class="sxs-lookup"><span data-stu-id="a7fce-115">Client-side Asynchronous Pipe Handling</span></span>](client-side-asynchronous-pipe-handling.md)
-   [<span data-ttu-id="a7fce-116">Gestione della pipe asincrona sul lato server</span><span class="sxs-lookup"><span data-stu-id="a7fce-116">Server-side Asynchronous Pipe Handling</span></span>](server-side-asynchronous-pipe-handling.md)

<span data-ttu-id="a7fce-117">Per un'applicazione RPC pipe asincrona di esempio, vedere l'esempio FileRep nel Software Development Kit (SDK) della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="a7fce-117">For a sample asynchronous pipe RPC application, see the FileRep sample in the Platform Software Development Kit (SDK).</span></span>

 

 




