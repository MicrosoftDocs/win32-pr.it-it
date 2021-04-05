---
title: Funzioni di utilità NAP
description: Le funzioni di utilità seguenti supportano l'API NAP.
ms.assetid: 0819067c-cca5-4140-8b4d-f3b996826152
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 260c423909011c81f52ea89ce8d3137b35c55167
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709799"
---
# <a name="nap-utility-functions"></a><span data-ttu-id="13c33-103">Funzioni di utilità NAP</span><span class="sxs-lookup"><span data-stu-id="13c33-103">NAP Utility Functions</span></span>

> [!Note]  
> <span data-ttu-id="13c33-104">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="13c33-104">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="13c33-105">Le funzioni di utilità seguenti supportano l'API NAP.</span><span class="sxs-lookup"><span data-stu-id="13c33-105">The following utility functions support the NAP API.</span></span>

<span data-ttu-id="13c33-106">Tutte le interfacce COM supportate dal sistema NAP utilizzano le regole di gestione della memoria COM standard e l'allocatore di memoria COM (CoTaskMemAlloc e CoTaskMemFree).</span><span class="sxs-lookup"><span data-stu-id="13c33-106">All the COM interfaces supported by the NAP system use standard COM memory management rules and the COM memory allocator (CoTaskMemAlloc and CoTaskMemFree).</span></span>

-   <span data-ttu-id="13c33-107">IN Parameters-allocato e liberato dal chiamante.</span><span class="sxs-lookup"><span data-stu-id="13c33-107">IN parameters — allocated and freed by caller.</span></span>
-   <span data-ttu-id="13c33-108">Parametri OUT, allocati dal chiamato, liberati dal chiamante tramite CoTaskMem \* ()</span><span class="sxs-lookup"><span data-stu-id="13c33-108">OUT parameters — allocated by callee, freed by caller using CoTaskMem\*()</span></span>
-   <span data-ttu-id="13c33-109">Parametri IN/OUT, allocati dal chiamante, liberati e riallocati dal chiamato, infine liberati dal chiamante, utilizzando CoTaskMem \* ()</span><span class="sxs-lookup"><span data-stu-id="13c33-109">IN/OUT parameters — allocated by caller, freed and reallocated by callee, ultimately freed by caller, using CoTaskMem\*()</span></span>

<span data-ttu-id="13c33-110">Nelle funzioni FreeXxx () verranno liberati anche tutti i puntatori incorporati.</span><span class="sxs-lookup"><span data-stu-id="13c33-110">In the FreeXxx() functions, all embedded pointers will also be freed.</span></span>

-   [<span data-ttu-id="13c33-111">**AllocConnections**</span><span class="sxs-lookup"><span data-stu-id="13c33-111">**AllocConnections**</span></span>](allocconnections-func.md)
-   [<span data-ttu-id="13c33-112">**AllocCountedString**</span><span class="sxs-lookup"><span data-stu-id="13c33-112">**AllocCountedString**</span></span>](alloccountedstring-func.md)
-   [<span data-ttu-id="13c33-113">**AllocFixupInfo**</span><span class="sxs-lookup"><span data-stu-id="13c33-113">**AllocFixupInfo**</span></span>](allocfixupinfo-func.md)
-   [<span data-ttu-id="13c33-114">**FreeConnections**</span><span class="sxs-lookup"><span data-stu-id="13c33-114">**FreeConnections**</span></span>](freeconnections-func.md)
-   [<span data-ttu-id="13c33-115">**FreeCountedString**</span><span class="sxs-lookup"><span data-stu-id="13c33-115">**FreeCountedString**</span></span>](freecountedstring-func.md)
-   [<span data-ttu-id="13c33-116">**FreeFixupInfo**</span><span class="sxs-lookup"><span data-stu-id="13c33-116">**FreeFixupInfo**</span></span>](freefixupinfo-func.md)
-   [<span data-ttu-id="13c33-117">**FreeIsolationInfo**</span><span class="sxs-lookup"><span data-stu-id="13c33-117">**FreeIsolationInfo**</span></span>](freeisolationinfo-func.md)
-   [<span data-ttu-id="13c33-118">**FreeIsolationInfoEx**</span><span class="sxs-lookup"><span data-stu-id="13c33-118">**FreeIsolationInfoEx**</span></span>](freeisolationinfoex.md)
-   [<span data-ttu-id="13c33-119">**FreeNapComponentRegistrationInfoArray**</span><span class="sxs-lookup"><span data-stu-id="13c33-119">**FreeNapComponentRegistrationInfoArray**</span></span>](freenapcomponentregistrationinfoarray-func.md)
-   [<span data-ttu-id="13c33-120">**FreeNetworkSoH**</span><span class="sxs-lookup"><span data-stu-id="13c33-120">**FreeNetworkSoH**</span></span>](freenetworksoh-func.md)
-   [<span data-ttu-id="13c33-121">**FreePrivateData**</span><span class="sxs-lookup"><span data-stu-id="13c33-121">**FreePrivateData**</span></span>](freeprivatedata-func.md)
-   [<span data-ttu-id="13c33-122">**FreeSoH**</span><span class="sxs-lookup"><span data-stu-id="13c33-122">**FreeSoH**</span></span>](freesoh-func.md)
-   [<span data-ttu-id="13c33-123">**FreeSoHAttributeValue**</span><span class="sxs-lookup"><span data-stu-id="13c33-123">**FreeSoHAttributeValue**</span></span>](freesohattributevalue-func.md)
-   [<span data-ttu-id="13c33-124">**FreeSystemHealthAgentState**</span><span class="sxs-lookup"><span data-stu-id="13c33-124">**FreeSystemHealthAgentState**</span></span>](freesystemhealthagentstate-func.md)
-   [<span data-ttu-id="13c33-125">**InitializeNapAgentNotifier**</span><span class="sxs-lookup"><span data-stu-id="13c33-125">**InitializeNapAgentNotifier**</span></span>](initializenapagentnotifier.md)
-   [<span data-ttu-id="13c33-126">**UninitializeNapAgentNotifier**</span><span class="sxs-lookup"><span data-stu-id="13c33-126">**UninitializeNapAgentNotifier**</span></span>](uninitializenapagentnotifier.md)

 

 




