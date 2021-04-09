---
title: Sviluppo di applicazioni Windows RPC
description: Quando si installa Platform Software Development Kit (SDK), l'ambiente di sviluppo RPC seguente, le librerie di runtime e gli strumenti vengono installati automaticamente
ms.assetid: d5da3bca-5251-4ba4-b873-0817fe0f298d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b418358649d0cf7205b9a3bde236cf66d3ce81e0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047251"
---
# <a name="developing-rpc-windows-applications"></a><span data-ttu-id="83994-103">Sviluppo di applicazioni Windows RPC</span><span class="sxs-lookup"><span data-stu-id="83994-103">Developing RPC Windows Applications</span></span>

<span data-ttu-id="83994-104">Quando si installa Platform Software Development Kit (SDK), l'ambiente di sviluppo RPC seguente, le librerie di runtime e gli strumenti vengono installati automaticamente:</span><span class="sxs-lookup"><span data-stu-id="83994-104">When you install the Platform Software Development Kit (SDK), the following RPC development environment, the run-time libraries, and tools are automatically installed:</span></span>

-   <span data-ttu-id="83994-105">Intestazione del linguaggio C/C++ (. File H)</span><span class="sxs-lookup"><span data-stu-id="83994-105">C/C++ language header (.H) files</span></span>
-   <span data-ttu-id="83994-106">File delle librerie di importazione RPC (lib)</span><span class="sxs-lookup"><span data-stu-id="83994-106">RPC import libraries (.lib) files</span></span>
-   <span data-ttu-id="83994-107">Programmi di esempio</span><span class="sxs-lookup"><span data-stu-id="83994-107">Sample programs</span></span>
-   <span data-ttu-id="83994-108">File della Guida di riferimento RPC</span><span class="sxs-lookup"><span data-stu-id="83994-108">RPC reference Help files</span></span>
-   <span data-ttu-id="83994-109">Utilità **uuidgen**</span><span class="sxs-lookup"><span data-stu-id="83994-109">The **uuidgen** utility</span></span>

<span data-ttu-id="83994-110">Quando si installa Windows, vengono installati i seguenti elementi:</span><span class="sxs-lookup"><span data-stu-id="83994-110">When you install Windows, the following are installed:</span></span>

-   <span data-ttu-id="83994-111">Dll di runtime RPC</span><span class="sxs-lookup"><span data-stu-id="83994-111">RPC Run-time DLLs</span></span>
-   <span data-ttu-id="83994-112">Microsoft Locator (non supportato in Windows Vista e versioni successive)</span><span class="sxs-lookup"><span data-stu-id="83994-112">Microsoft Locator (not supported on Windows Vista and later)</span></span>
-   <span data-ttu-id="83994-113">Servizi di mapping degli endpoint RPC</span><span class="sxs-lookup"><span data-stu-id="83994-113">RPC Endpoint-mapping services</span></span>

<span data-ttu-id="83994-114">Librerie di importazione RPC seguenti.</span><span class="sxs-lookup"><span data-stu-id="83994-114">The following RPC import libraries.</span></span>



| <span data-ttu-id="83994-115">Libreria di importazione</span><span class="sxs-lookup"><span data-stu-id="83994-115">Import library</span></span> | <span data-ttu-id="83994-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="83994-116">Description</span></span>                |
|----------------|----------------------------|
| <span data-ttu-id="83994-117">Rpcns4. lib</span><span class="sxs-lookup"><span data-stu-id="83994-117">Rpcns4.lib</span></span>     | <span data-ttu-id="83994-118">Nome-funzioni servizio</span><span class="sxs-lookup"><span data-stu-id="83994-118">Name-service functions</span></span>     |
| <span data-ttu-id="83994-119">Rpcrt4. lib</span><span class="sxs-lookup"><span data-stu-id="83994-119">Rpcrt4.lib</span></span>     | <span data-ttu-id="83994-120">Funzioni di runtime di Windows</span><span class="sxs-lookup"><span data-stu-id="83994-120">Windows run-time functions</span></span> |



 

> [!Note]  
> <span data-ttu-id="83994-121">Rpcns4. lib è obsoleto e non è più supportato.</span><span class="sxs-lookup"><span data-stu-id="83994-121">Rpcns4.lib is obsolete and no longer supported.</span></span>

 

<span data-ttu-id="83994-122">Per il supporto di livello inferiore sono incluse le librerie RPC seguenti.</span><span class="sxs-lookup"><span data-stu-id="83994-122">The following RPC libraries are included for down-level support.</span></span>



| <span data-ttu-id="83994-123">Libreria a collegamento dinamico</span><span class="sxs-lookup"><span data-stu-id="83994-123">Dynamic-link library</span></span> | <span data-ttu-id="83994-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="83994-124">Description</span></span>                 | <span data-ttu-id="83994-125">Piattaforma</span><span class="sxs-lookup"><span data-stu-id="83994-125">Platform</span></span>                           |
|----------------------|-----------------------------|------------------------------------|
| <span data-ttu-id="83994-126">Rpcltc1.dll</span><span class="sxs-lookup"><span data-stu-id="83994-126">Rpcltc1.dll</span></span>          | <span data-ttu-id="83994-127">Trasporto named pipe del client</span><span class="sxs-lookup"><span data-stu-id="83994-127">Client named-pipe transport</span></span> | <span data-ttu-id="83994-128">Windows NT, Windows 98, Windows 95</span><span class="sxs-lookup"><span data-stu-id="83994-128">Windows NT, Windows 98, Windows 95</span></span> |
| <span data-ttu-id="83994-129">Rpclts1.dll</span><span class="sxs-lookup"><span data-stu-id="83994-129">Rpclts1.dll</span></span>          | <span data-ttu-id="83994-130">Trasporto named pipe del server</span><span class="sxs-lookup"><span data-stu-id="83994-130">Server named-pipe transport</span></span> | <span data-ttu-id="83994-131">Windows NT, Windows 98, Windows 95</span><span class="sxs-lookup"><span data-stu-id="83994-131">Windows NT, Windows 98, Windows 95</span></span> |
| <span data-ttu-id="83994-132">Rpcltc3.dll</span><span class="sxs-lookup"><span data-stu-id="83994-132">Rpcltc3.dll</span></span>          | <span data-ttu-id="83994-133">Trasporto TCP/IP client</span><span class="sxs-lookup"><span data-stu-id="83994-133">Client TCP/IP transport</span></span>     | <span data-ttu-id="83994-134">Windows NT, Windows 98, Windows 95</span><span class="sxs-lookup"><span data-stu-id="83994-134">Windows NT, Windows 98, Windows 95</span></span> |
| <span data-ttu-id="83994-135">Rpclts3.dll</span><span class="sxs-lookup"><span data-stu-id="83994-135">Rpclts3.dll</span></span>          | <span data-ttu-id="83994-136">Trasporto TCP/IP del server</span><span class="sxs-lookup"><span data-stu-id="83994-136">Server TCP/IP transport</span></span>     | <span data-ttu-id="83994-137">Windows NT, Windows 98, Windows 95</span><span class="sxs-lookup"><span data-stu-id="83994-137">Windows NT, Windows 98, Windows 95</span></span> |
| <span data-ttu-id="83994-138">Rpcltc5.dll</span><span class="sxs-lookup"><span data-stu-id="83994-138">Rpcltc5.dll</span></span>          | <span data-ttu-id="83994-139">Trasporto NetBIOS client</span><span class="sxs-lookup"><span data-stu-id="83994-139">Client NetBIOS transport</span></span>    | <span data-ttu-id="83994-140">Windows NT, Windows 98, Windows 95</span><span class="sxs-lookup"><span data-stu-id="83994-140">Windows NT, Windows 98, Windows 95</span></span> |
| <span data-ttu-id="83994-141">Rpclts5.dll</span><span class="sxs-lookup"><span data-stu-id="83994-141">Rpclts5.dll</span></span>          | <span data-ttu-id="83994-142">Trasporto NetBIOS server</span><span class="sxs-lookup"><span data-stu-id="83994-142">Server NetBIOS transport</span></span>    | <span data-ttu-id="83994-143">Windows NT, Windows 98, Windows 95</span><span class="sxs-lookup"><span data-stu-id="83994-143">Windows NT, Windows 98, Windows 95</span></span> |
| <span data-ttu-id="83994-144">Rpcltc6.dll</span><span class="sxs-lookup"><span data-stu-id="83994-144">Rpcltc6.dll</span></span>          | <span data-ttu-id="83994-145">Trasporto SPX client</span><span class="sxs-lookup"><span data-stu-id="83994-145">Client SPX transport</span></span>        | <span data-ttu-id="83994-146">Windows NT, Windows 98, Windows 95</span><span class="sxs-lookup"><span data-stu-id="83994-146">Windows NT, Windows 98, Windows 95</span></span> |
| <span data-ttu-id="83994-147">Rpclts6.dll</span><span class="sxs-lookup"><span data-stu-id="83994-147">Rpclts6.dll</span></span>          | <span data-ttu-id="83994-148">Trasporto SPX server</span><span class="sxs-lookup"><span data-stu-id="83994-148">Server SPX transport</span></span>        | <span data-ttu-id="83994-149">Windows NT, Windows 98, Windows 95</span><span class="sxs-lookup"><span data-stu-id="83994-149">Windows NT, Windows 98, Windows 95</span></span> |
| <span data-ttu-id="83994-150">Rpcdgc6.dll</span><span class="sxs-lookup"><span data-stu-id="83994-150">Rpcdgc6.dll</span></span>          | <span data-ttu-id="83994-151">Trasporto IPX client</span><span class="sxs-lookup"><span data-stu-id="83994-151">Client IPX transport</span></span>        | <span data-ttu-id="83994-152">Windows NT</span><span class="sxs-lookup"><span data-stu-id="83994-152">Windows NT</span></span>                         |
| <span data-ttu-id="83994-153">Rpcdgs6.dll</span><span class="sxs-lookup"><span data-stu-id="83994-153">Rpcdgs6.dll</span></span>          | <span data-ttu-id="83994-154">Trasporto IPX server</span><span class="sxs-lookup"><span data-stu-id="83994-154">Server IPX transport</span></span>        | <span data-ttu-id="83994-155">Windows NT</span><span class="sxs-lookup"><span data-stu-id="83994-155">Windows NT</span></span>                         |
| <span data-ttu-id="83994-156">Rpcdgc3.dll</span><span class="sxs-lookup"><span data-stu-id="83994-156">Rpcdgc3.dll</span></span>          | <span data-ttu-id="83994-157">Trasporto UDP client</span><span class="sxs-lookup"><span data-stu-id="83994-157">Client UDP transport</span></span>        | <span data-ttu-id="83994-158">Windows NT</span><span class="sxs-lookup"><span data-stu-id="83994-158">Windows NT</span></span>                         |
| <span data-ttu-id="83994-159">Rpcdgs3.dll</span><span class="sxs-lookup"><span data-stu-id="83994-159">Rpcdgs3.dll</span></span>          | <span data-ttu-id="83994-160">Trasporto UDP del server</span><span class="sxs-lookup"><span data-stu-id="83994-160">Server UDP transport</span></span>        | <span data-ttu-id="83994-161">Windows NT</span><span class="sxs-lookup"><span data-stu-id="83994-161">Windows NT</span></span>                         |



 

<span data-ttu-id="83994-162">Sarà inoltre necessario il compilatore Microsoft Interface Definition Language (MIDL).</span><span class="sxs-lookup"><span data-stu-id="83994-162">You will also need the Microsoft Interface Definition Language (MIDL) compiler.</span></span> <span data-ttu-id="83994-163">Per altre informazioni, vedere [uso del compilatore MIDL](/windows/desktop/Midl/using-the-midl-compiler-2).</span><span class="sxs-lookup"><span data-stu-id="83994-163">For more information, see [Using The MIDL Compiler](/windows/desktop/Midl/using-the-midl-compiler-2).</span></span>

 

 