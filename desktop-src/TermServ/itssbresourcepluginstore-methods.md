---
title: Metodi ITsSbResourcePluginStore
description: L'interfaccia ITsSbResourcePluginStore espone i metodi seguenti.
ms.assetid: D3D59244-E319-47C8-A931-72679C11AC40
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c56d403bc681152a5076d6c219790b452bd749d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856406"
---
# <a name="itssbresourcepluginstore-methods"></a><span data-ttu-id="f53b9-103">Metodi ITsSbResourcePluginStore</span><span class="sxs-lookup"><span data-stu-id="f53b9-103">ITsSbResourcePluginStore Methods</span></span>

<span data-ttu-id="f53b9-104">L'interfaccia [**ITsSbResourcePluginStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore) espone i metodi seguenti.</span><span class="sxs-lookup"><span data-stu-id="f53b9-104">The [**ITsSbResourcePluginStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore) interface exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f53b9-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="f53b9-105">In this section</span></span>

-   [<span data-ttu-id="f53b9-106">**Metodo AcquireTargetLock**</span><span class="sxs-lookup"><span data-stu-id="f53b9-106">**AcquireTargetLock method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-acquiretargetlock)
-   [<span data-ttu-id="f53b9-107">**Metodo AddEnvironmentToStore**</span><span class="sxs-lookup"><span data-stu-id="f53b9-107">**AddEnvironmentToStore method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-addenvironmenttostore)
-   [<span data-ttu-id="f53b9-108">**Metodo AddSessionToStore**</span><span class="sxs-lookup"><span data-stu-id="f53b9-108">**AddSessionToStore method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-addsessiontostore)
-   [<span data-ttu-id="f53b9-109">**Metodo AddTargetToStore**</span><span class="sxs-lookup"><span data-stu-id="f53b9-109">**AddTargetToStore method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-addtargettostore)
-   [<span data-ttu-id="f53b9-110">**Metodo DeleteTarget**</span><span class="sxs-lookup"><span data-stu-id="f53b9-110">**DeleteTarget method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-deletetarget)
-   [<span data-ttu-id="f53b9-111">**Metodo EnumerateEnvironments**</span><span class="sxs-lookup"><span data-stu-id="f53b9-111">**EnumerateEnvironments method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumerateenvironments)
-   [<span data-ttu-id="f53b9-112">**Metodo EnumerateFarms**</span><span class="sxs-lookup"><span data-stu-id="f53b9-112">**EnumerateFarms method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumeratefarms)
-   [<span data-ttu-id="f53b9-113">**Metodo EnumerateSessions**</span><span class="sxs-lookup"><span data-stu-id="f53b9-113">**EnumerateSessions method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumeratesessions)
-   [<span data-ttu-id="f53b9-114">**Metodo EnumerateTargets**</span><span class="sxs-lookup"><span data-stu-id="f53b9-114">**EnumerateTargets method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumeratetargets)
-   [<span data-ttu-id="f53b9-115">**Metodo GetFarmProperty**</span><span class="sxs-lookup"><span data-stu-id="f53b9-115">**GetFarmProperty method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-getfarmproperty)
-   [<span data-ttu-id="f53b9-116">**Metodo GetServerState**</span><span class="sxs-lookup"><span data-stu-id="f53b9-116">**GetServerState method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-getserverstate)
-   [<span data-ttu-id="f53b9-117">**Metodo QueryEnvironment**</span><span class="sxs-lookup"><span data-stu-id="f53b9-117">**QueryEnvironment method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-queryenvironment)
-   [<span data-ttu-id="f53b9-118">**Metodo QuerySessionBySessionId**</span><span class="sxs-lookup"><span data-stu-id="f53b9-118">**QuerySessionBySessionId method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-querysessionbysessionid)
-   [<span data-ttu-id="f53b9-119">**Metodo QueryTarget**</span><span class="sxs-lookup"><span data-stu-id="f53b9-119">**QueryTarget method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-querytarget)
-   [<span data-ttu-id="f53b9-120">**Metodo ReleaseTargetLock**</span><span class="sxs-lookup"><span data-stu-id="f53b9-120">**ReleaseTargetLock method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock)
-   [<span data-ttu-id="f53b9-121">**Metodo RemoveEnvironmentFromStore**</span><span class="sxs-lookup"><span data-stu-id="f53b9-121">**RemoveEnvironmentFromStore method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-removeenvironmentfromstore)
-   [<span data-ttu-id="f53b9-122">**Metodo SaveEnvironment**</span><span class="sxs-lookup"><span data-stu-id="f53b9-122">**SaveEnvironment method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-saveenvironment)
-   [<span data-ttu-id="f53b9-123">**Metodo SaveSession**</span><span class="sxs-lookup"><span data-stu-id="f53b9-123">**SaveSession method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-savesession)
-   [<span data-ttu-id="f53b9-124">**Metodo SaveTarget**</span><span class="sxs-lookup"><span data-stu-id="f53b9-124">**SaveTarget method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-savetarget)
-   [<span data-ttu-id="f53b9-125">**Metodo SetEnvironmentProperty**</span><span class="sxs-lookup"><span data-stu-id="f53b9-125">**SetEnvironmentProperty method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setenvironmentproperty)
-   [<span data-ttu-id="f53b9-126">**Metodo SetEnvironmentPropertyWithVersionCheck**</span><span class="sxs-lookup"><span data-stu-id="f53b9-126">**SetEnvironmentPropertyWithVersionCheck method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setenvironmentpropertywithversioncheck)
-   [<span data-ttu-id="f53b9-127">**Metodo SetServerDrainMode**</span><span class="sxs-lookup"><span data-stu-id="f53b9-127">**SetServerDrainMode method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setserverdrainmode)
-   [<span data-ttu-id="f53b9-128">**Metodo SetServerWaitingToStart**</span><span class="sxs-lookup"><span data-stu-id="f53b9-128">**SetServerWaitingToStart method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setserverwaitingtostart)
-   [<span data-ttu-id="f53b9-129">**Metodo SessionState**</span><span class="sxs-lookup"><span data-stu-id="f53b9-129">**SetSessionState method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setsessionstate)
-   [<span data-ttu-id="f53b9-130">**Metodo SetTargetProperty**</span><span class="sxs-lookup"><span data-stu-id="f53b9-130">**SetTargetProperty method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-settargetproperty)
-   [<span data-ttu-id="f53b9-131">**Metodo SetTargetPropertyWithVersionCheck**</span><span class="sxs-lookup"><span data-stu-id="f53b9-131">**SetTargetPropertyWithVersionCheck method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-settargetpropertywithversioncheck)
-   [<span data-ttu-id="f53b9-132">**Metodo SetTargetState**</span><span class="sxs-lookup"><span data-stu-id="f53b9-132">**SetTargetState method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-settargetstate)
-   [<span data-ttu-id="f53b9-133">**Metodo TestAndSetServerState**</span><span class="sxs-lookup"><span data-stu-id="f53b9-133">**TestAndSetServerState method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-testandsetserverstate)

 

 




