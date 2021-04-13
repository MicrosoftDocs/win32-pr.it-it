---
title: Chiamata di procedura remota
description: Microsoft Remote Procedure Call (RPC) definisce una tecnologia potente per la creazione di programmi client/server distribuiti.
ms.assetid: 27c7c352-5fc1-47cf-99b1-fdf3eca986bc
keywords:
- RPC
- RPC (vedere Remote Procedure Call)
- RPC (Remote Procedure Call), pagina iniziale
- RPC RPC (Remote Procedure Call)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3461116468bf1d686d1a5695924e5fe66007b35
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399540"
---
# <a name="remote-procedure-call"></a><span data-ttu-id="e4f8d-107">Chiamata di procedura remota</span><span class="sxs-lookup"><span data-stu-id="e4f8d-107">Remote Procedure Call</span></span>

## <a name="purpose"></a><span data-ttu-id="e4f8d-108">Scopo</span><span class="sxs-lookup"><span data-stu-id="e4f8d-108">Purpose</span></span>

<span data-ttu-id="e4f8d-109">Microsoft Remote Procedure Call (RPC) definisce una tecnologia potente per la creazione di programmi client/server distribuiti.</span><span class="sxs-lookup"><span data-stu-id="e4f8d-109">Microsoft Remote Procedure Call (RPC) defines a powerful technology for creating distributed client/server programs.</span></span> <span data-ttu-id="e4f8d-110">Gli stub e le librerie di runtime RPC gestiscono la maggior parte dei processi correlati alla comunicazione e ai protocolli di rete.</span><span class="sxs-lookup"><span data-stu-id="e4f8d-110">The RPC run-time stubs and libraries manage most of the processes relating to network protocols and communication.</span></span> <span data-ttu-id="e4f8d-111">In questo modo è possibile concentrarsi sui dettagli dell'applicazione anziché sui dettagli della rete.</span><span class="sxs-lookup"><span data-stu-id="e4f8d-111">This enables you to focus on the details of the application rather than the details of the network.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="e4f8d-112">Se applicabile</span><span class="sxs-lookup"><span data-stu-id="e4f8d-112">Where applicable</span></span>

<span data-ttu-id="e4f8d-113">RPC può essere usato in tutte le applicazioni client/server basate su sistemi operativi Windows.</span><span class="sxs-lookup"><span data-stu-id="e4f8d-113">RPC can be used in all client/server applications based on Windows operating systems.</span></span> <span data-ttu-id="e4f8d-114">Può essere usato anche per creare programmi client e server per ambienti di rete eterogenei che includono sistemi operativi come UNIX e Apple.</span><span class="sxs-lookup"><span data-stu-id="e4f8d-114">It can also be used to create client and server programs for heterogeneous network environments that include such operating systems as Unix and Apple.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="e4f8d-115">Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="e4f8d-115">Developer audience</span></span>

<span data-ttu-id="e4f8d-116">RPC è progettato per essere utilizzato dai programmatori C/C++.</span><span class="sxs-lookup"><span data-stu-id="e4f8d-116">RPC is designed to be used by C/C++ programmers.</span></span> <span data-ttu-id="e4f8d-117">È necessaria una certa familiarità con il Microsoft Interface Definition Language (MIDL) e il compilatore MIDL.</span><span class="sxs-lookup"><span data-stu-id="e4f8d-117">Familiarity with the Microsoft Interface Definition Language (MIDL) and the MIDL compiler are required.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="e4f8d-118">Requisiti di runtime</span><span class="sxs-lookup"><span data-stu-id="e4f8d-118">Run-time requirements</span></span>

<span data-ttu-id="e4f8d-119">Le librerie di runtime RPC sono incluse in Windows.</span><span class="sxs-lookup"><span data-stu-id="e4f8d-119">The RPC run-time libraries are included with Windows.</span></span> <span data-ttu-id="e4f8d-120">I componenti dell'ambiente di sviluppo RPC vengono installati quando si installa il Software Development Kit (SDK) di Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="e4f8d-120">The components of the RPC development environment are installed when you install the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="e4f8d-121">Per informazioni dettagliate, vedere [installazione dell'ambiente di programmazione RPC](installing-the-rpc-programming-environment.md).</span><span class="sxs-lookup"><span data-stu-id="e4f8d-121">For details, see [Installing the RPC Programming Environment](installing-the-rpc-programming-environment.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="e4f8d-122">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="e4f8d-122">In this section</span></span>



| <span data-ttu-id="e4f8d-123">Argomento</span><span class="sxs-lookup"><span data-stu-id="e4f8d-123">Topic</span></span>                                                                           | <span data-ttu-id="e4f8d-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e4f8d-124">Description</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e4f8d-125">Procedure di programmazione RPC migliori</span><span class="sxs-lookup"><span data-stu-id="e4f8d-125">Best RPC Programming Practices</span></span>](best-rpc-programming-practices.md)<br/> | <span data-ttu-id="e4f8d-126">Indicazioni sulle procedure di programmazione RPC che consentono di creare le migliori applicazioni RPC possibili.</span><span class="sxs-lookup"><span data-stu-id="e4f8d-126">Guidance on RPC programming practices that help create the best possible RPC applications.</span></span><br/>                            |
| [<span data-ttu-id="e4f8d-127">Overview</span><span class="sxs-lookup"><span data-stu-id="e4f8d-127">Overview</span></span>](overviews.md)<br/>                                            | <span data-ttu-id="e4f8d-128">Informazioni generali sull'incorporamento di RPC nelle applicazioni client/server.</span><span class="sxs-lookup"><span data-stu-id="e4f8d-128">General information about incorporating RPC into your client/server applications.</span></span><br/>                                     |
| [<span data-ttu-id="e4f8d-129">Riferimento</span><span class="sxs-lookup"><span data-stu-id="e4f8d-129">Reference</span></span>](reference.md)<br/>                                           | <span data-ttu-id="e4f8d-130">Documentazione di tipi, funzioni e costanti RPC.</span><span class="sxs-lookup"><span data-stu-id="e4f8d-130">Documentation of RPC types, functions, and constants.</span></span><br/>                                                                 |
| [<span data-ttu-id="e4f8d-131">Motore di recapito RPC</span><span class="sxs-lookup"><span data-stu-id="e4f8d-131">RPC NDR Engine</span></span>](rpc-ndr-engine.md)<br/>                                 | <span data-ttu-id="e4f8d-132">Documentazione del motore di marshalling per i componenti RPC e DCOM, il motore di rappresentazione dei dati di rete RPC (NDR).</span><span class="sxs-lookup"><span data-stu-id="e4f8d-132">Documentation of the marshaling engine for RPC and DCOM components, the RPC Network Data Representation (NDR) Engine.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="e4f8d-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e4f8d-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4f8d-134">Microsoft Interface Definition Language (MIDL)</span><span class="sxs-lookup"><span data-stu-id="e4f8d-134">Microsoft Interface Definition Language (MIDL)</span></span>](/windows/desktop/Midl/midl-start-page)
</dt> </dl>

 

