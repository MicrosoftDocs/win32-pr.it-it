---
title: Stub del server
description: Lo stub del server fornisce punti di ingresso surrogati sul server per ciascuna delle operazioni definite nel file IDL di input.
ms.assetid: e3263543-e78b-40a8-aafa-4315850112a8
keywords:
- MIDL Compiler MIDL, MIDL e RPC MIDL, interfacce, stub server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b351c53fa9e1d1716e1240ddf4febdccdadda46
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045148"
---
# <a name="the-server-stub"></a><span data-ttu-id="7abd1-104">Stub del server</span><span class="sxs-lookup"><span data-stu-id="7abd1-104">The Server Stub</span></span>

<span data-ttu-id="7abd1-105">Lo stub del server fornisce punti di ingresso surrogati sul server per ciascuna delle operazioni definite nel file IDL di input.</span><span class="sxs-lookup"><span data-stu-id="7abd1-105">The server stub provides surrogate entry points on the server for each of the operations defined in the input IDL file.</span></span>

<span data-ttu-id="7abd1-106">Quando una routine stub del server viene richiamata dalla libreria di runtime RPC, esegue le funzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="7abd1-106">When a server stub routine is invoked by the RPC run-time library, it performs the following functions:</span></span>

-   <span data-ttu-id="7abd1-107">Esegue l'unmarshalling degli argomenti di input (decomprime gli argomenti dai formati trasmessi).</span><span class="sxs-lookup"><span data-stu-id="7abd1-107">Unmarshals input arguments (unpacks the arguments from their transmitted formats).</span></span>
-   <span data-ttu-id="7abd1-108">Chiama l'implementazione effettiva della stored procedure nel server.</span><span class="sxs-lookup"><span data-stu-id="7abd1-108">Calls the actual implementation of the procedure on the server.</span></span>
-   <span data-ttu-id="7abd1-109">Esegue il marshalling degli argomenti di output (crea il pacchetto degli argomenti nei form trasmessi).</span><span class="sxs-lookup"><span data-stu-id="7abd1-109">Marshals output arguments (packages the arguments into the transmitted forms).</span></span>

<span data-ttu-id="7abd1-110">Il compilatore MIDL commuta [**/Server**](-server.md), [**/sstub**](-sstub.md)e [**/out**](-out.md) influisce sul file stub del server.</span><span class="sxs-lookup"><span data-stu-id="7abd1-110">The MIDL compiler switches [**/server**](-server.md), [**/sstub**](-sstub.md), and [**/out**](-out.md) affect the server stub file.</span></span>

 

 




