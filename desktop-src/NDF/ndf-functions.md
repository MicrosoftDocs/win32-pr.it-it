---
title: Funzioni NDF
description: Le funzioni seguenti consentono agli sviluppatori di software di usare la funzionalità fornita dal framework di diagnostica di rete (NDF).
ms.assetid: c2774e05-82f4-4d40-a80c-ad773bb03ca7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d3a039768b77d69072111f814cb871115bcca24
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298133"
---
# <a name="ndf-functions"></a><span data-ttu-id="bfcbc-103">Funzioni NDF</span><span class="sxs-lookup"><span data-stu-id="bfcbc-103">NDF Functions</span></span>

<span data-ttu-id="bfcbc-104">Le funzioni seguenti consentono agli sviluppatori di software di usare la funzionalità fornita dal framework di diagnostica di rete (NDF).</span><span class="sxs-lookup"><span data-stu-id="bfcbc-104">The following functions enable software developers to use the functionality provided by the Network Diagnostic Framework (NDF).</span></span> <span data-ttu-id="bfcbc-105">Quando si verificano problemi di rete, NDF è in grado di diagnosticare la causa radice e gestire correttamente la risoluzione necessaria, talvolta anche eseguendo le riparazioni necessarie.</span><span class="sxs-lookup"><span data-stu-id="bfcbc-105">When network issues occur, NDF can diagnose the root cause and handle the necessary resolution gracefully, sometimes even performing the necessary repairs.</span></span>

> [!Note]  
> <span data-ttu-id="bfcbc-106">Queste funzioni sono destinate agli sviluppatori che implementano la funzionalità NDF di base nelle proprie applicazioni.</span><span class="sxs-lookup"><span data-stu-id="bfcbc-106">These functions are for developers implementing basic NDF functionality in their applications.</span></span>

 

-   [<span data-ttu-id="bfcbc-107">**CopyHelperAttribute**</span><span class="sxs-lookup"><span data-stu-id="bfcbc-107">**CopyHelperAttribute**</span></span>](copyhelperattribute.md)
-   [<span data-ttu-id="bfcbc-108">**CopyRepairInfo**</span><span class="sxs-lookup"><span data-stu-id="bfcbc-108">**CopyRepairInfo**</span></span>](copyrepairinfo.md)
-   [<span data-ttu-id="bfcbc-109">**CopyRootCauseInfo**</span><span class="sxs-lookup"><span data-stu-id="bfcbc-109">**CopyRootCauseInfo**</span></span>](copyrootcauseinfo.md)
-   [<span data-ttu-id="bfcbc-110">**FreeRepairInfoExs**</span><span class="sxs-lookup"><span data-stu-id="bfcbc-110">**FreeRepairInfoExs**</span></span>](freerepairinfoexs.md)
-   [<span data-ttu-id="bfcbc-111">**FreeRepairInfos**</span><span class="sxs-lookup"><span data-stu-id="bfcbc-111">**FreeRepairInfos**</span></span>](freerepairinfos.md)
-   [<span data-ttu-id="bfcbc-112">**FreeRootCauseInfos**</span><span class="sxs-lookup"><span data-stu-id="bfcbc-112">**FreeRootCauseInfos**</span></span>](freerootcauseinfos.md)
-   [<span data-ttu-id="bfcbc-113">**FreeHelperAttributes**</span><span class="sxs-lookup"><span data-stu-id="bfcbc-113">**FreeHelperAttributes**</span></span>](freehelperattributes.md)
-   [<span data-ttu-id="bfcbc-114">**FreeUiInfo**</span><span class="sxs-lookup"><span data-stu-id="bfcbc-114">**FreeUiInfo**</span></span>](freeuiinfo.md)
-   [<span data-ttu-id="bfcbc-115">**NdfCancelIncident**</span><span class="sxs-lookup"><span data-stu-id="bfcbc-115">**NdfCancelIncident**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcancelincident)
-   [<span data-ttu-id="bfcbc-116">**NdfCloseIncident**</span><span class="sxs-lookup"><span data-stu-id="bfcbc-116">**NdfCloseIncident**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcloseincident)
-   [<span data-ttu-id="bfcbc-117">**NdfCreateConnectivityIncident**</span><span class="sxs-lookup"><span data-stu-id="bfcbc-117">**NdfCreateConnectivityIncident**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreateconnectivityincident)
-   [<span data-ttu-id="bfcbc-118">**NdfCreateDNSIncident**</span><span class="sxs-lookup"><span data-stu-id="bfcbc-118">**NdfCreateDNSIncident**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatednsincident)
-   [<span data-ttu-id="bfcbc-119">**NdfCreateGroupingIncident**</span><span class="sxs-lookup"><span data-stu-id="bfcbc-119">**NdfCreateGroupingIncident**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreategroupingincident)
-   [<span data-ttu-id="bfcbc-120">**NdfCreateInboundIncident**</span><span class="sxs-lookup"><span data-stu-id="bfcbc-120">**NdfCreateInboundIncident**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreateinboundincident)
-   [<span data-ttu-id="bfcbc-121">**NdfCreateIncident**</span><span class="sxs-lookup"><span data-stu-id="bfcbc-121">**NdfCreateIncident**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreateincident)
-   [<span data-ttu-id="bfcbc-122">**NdfCreateNetConnectionIncident**</span><span class="sxs-lookup"><span data-stu-id="bfcbc-122">**NdfCreateNetConnectionIncident**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatenetconnectionincident)
-   [<span data-ttu-id="bfcbc-123">**NdfCreatePnrpIncident**</span><span class="sxs-lookup"><span data-stu-id="bfcbc-123">**NdfCreatePnrpIncident**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatepnrpincident)
-   [<span data-ttu-id="bfcbc-124">**NdfCreateSharingIncident**</span><span class="sxs-lookup"><span data-stu-id="bfcbc-124">**NdfCreateSharingIncident**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatesharingincident)
-   [<span data-ttu-id="bfcbc-125">**NdfCreateWebIncident**</span><span class="sxs-lookup"><span data-stu-id="bfcbc-125">**NdfCreateWebIncident**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewebincident)
-   [<span data-ttu-id="bfcbc-126">**NdfCreateWebIncidentEx**</span><span class="sxs-lookup"><span data-stu-id="bfcbc-126">**NdfCreateWebIncidentEx**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewebincidentex)
-   [<span data-ttu-id="bfcbc-127">**NdfCreateWinSockIncident**</span><span class="sxs-lookup"><span data-stu-id="bfcbc-127">**NdfCreateWinSockIncident**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewinsockincident)
-   [<span data-ttu-id="bfcbc-128">**NdfDiagnoseIncident**</span><span class="sxs-lookup"><span data-stu-id="bfcbc-128">**NdfDiagnoseIncident**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfdiagnoseincident)
-   [<span data-ttu-id="bfcbc-129">**NdfExecuteDiagnosis**</span><span class="sxs-lookup"><span data-stu-id="bfcbc-129">**NdfExecuteDiagnosis**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfexecutediagnosis)
-   [<span data-ttu-id="bfcbc-130">**NdfGetTraceFile**</span><span class="sxs-lookup"><span data-stu-id="bfcbc-130">**NdfGetTraceFile**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfgettracefile)
-   [<span data-ttu-id="bfcbc-131">**NdfRepairIncident**</span><span class="sxs-lookup"><span data-stu-id="bfcbc-131">**NdfRepairIncident**</span></span>](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfrepairincident)
-   [<span data-ttu-id="bfcbc-132">**UtilAssembleStringsWithAlloc**</span><span class="sxs-lookup"><span data-stu-id="bfcbc-132">**UtilAssembleStringsWithAlloc**</span></span>](utilassemblestringswithalloc.md)
-   [<span data-ttu-id="bfcbc-133">**UtilLoadStringWithAlloc**</span><span class="sxs-lookup"><span data-stu-id="bfcbc-133">**UtilLoadStringWithAlloc**</span></span>](utilloadstringwithalloc.md)
-   [<span data-ttu-id="bfcbc-134">**UtilStringCopyWithAlloc**</span><span class="sxs-lookup"><span data-stu-id="bfcbc-134">**UtilStringCopyWithAlloc**</span></span>](utilstringcopywithalloc.md)

 

 




