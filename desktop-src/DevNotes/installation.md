---
description: Installazione
ms.assetid: 02A7866F-0F72-4437-A882-EEE9C2E28EC7
title: Installazione (note per gli sviluppatori)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51ddb476b6688bbbbef27eab571e3219071656a8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878090"
---
# <a name="installation-developer-notes"></a><span data-ttu-id="f0f56-103">Installazione (note per gli sviluppatori)</span><span class="sxs-lookup"><span data-stu-id="f0f56-103">Installation (Developer Notes)</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f0f56-104">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="f0f56-104">In this section</span></span>

-   [<span data-ttu-id="f0f56-105">**Coinstallazione**</span><span class="sxs-lookup"><span data-stu-id="f0f56-105">**CoInstall**</span></span>](/windows/win32/api/objbase/nf-objbase-coinstall)
-   [<span data-ttu-id="f0f56-106">**IcfgInstallInetComponents**</span><span class="sxs-lookup"><span data-stu-id="f0f56-106">**IcfgInstallInetComponents**</span></span>](icfginstallinetcomponents.md)
-   [<span data-ttu-id="f0f56-107">**IcfgNeedInetComponents**</span><span class="sxs-lookup"><span data-stu-id="f0f56-107">**IcfgNeedInetComponents**</span></span>](icfgneedinetcomponents.md)
-   [<span data-ttu-id="f0f56-108">**InstallCatalog**</span><span class="sxs-lookup"><span data-stu-id="f0f56-108">**InstallCatalog**</span></span>](installcatalog.md)
-   [<span data-ttu-id="f0f56-109">**InstallComponentW**</span><span class="sxs-lookup"><span data-stu-id="f0f56-109">**InstallComponentW**</span></span>](installcomponentw.md)
-   [<span data-ttu-id="f0f56-110">**InstallPerfDll**</span><span class="sxs-lookup"><span data-stu-id="f0f56-110">**InstallPerfDll**</span></span>](/windows/desktop/api/LoadPerf/nf-loadperf-installperfdlla)
-   [<span data-ttu-id="f0f56-111">**LoadLibraryShim**</span><span class="sxs-lookup"><span data-stu-id="f0f56-111">**LoadLibraryShim**</span></span>](loadlibraryshim.md)
-   [<span data-ttu-id="f0f56-112">**OcInitialize**</span><span class="sxs-lookup"><span data-stu-id="f0f56-112">**OcInitialize**</span></span>](ocinitialize.md)
-   [<span data-ttu-id="f0f56-113">**OcTerminate**</span><span class="sxs-lookup"><span data-stu-id="f0f56-113">**OcTerminate**</span></span>](octerminate.md)
-   [<span data-ttu-id="f0f56-114">**pSetupGetFileTitle**</span><span class="sxs-lookup"><span data-stu-id="f0f56-114">**pSetupGetFileTitle**</span></span>](psetupgetfiletitle.md)
-   [<span data-ttu-id="f0f56-115">**pSetupGetGlobalFlags**</span><span class="sxs-lookup"><span data-stu-id="f0f56-115">**pSetupGetGlobalFlags**</span></span>](psetupgetglobalflags.md)
-   [<span data-ttu-id="f0f56-116">**pSetupInstallCatalog**</span><span class="sxs-lookup"><span data-stu-id="f0f56-116">**pSetupInstallCatalog**</span></span>](psetupinstallcatalog.md)
-   [<span data-ttu-id="f0f56-117">**pSetupIsUserAdmin**</span><span class="sxs-lookup"><span data-stu-id="f0f56-117">**pSetupIsUserAdmin**</span></span>](psetupisuseradmin.md)
-   [<span data-ttu-id="f0f56-118">**pSetupSetGlobalFlags**</span><span class="sxs-lookup"><span data-stu-id="f0f56-118">**pSetupSetGlobalFlags**</span></span>](psetupsetglobalflags.md)
-   [<span data-ttu-id="f0f56-119">**pSetupStringTableDestroy**</span><span class="sxs-lookup"><span data-stu-id="f0f56-119">**pSetupStringTableDestroy**</span></span>](psetupstringtabledestroy.md)
-   [<span data-ttu-id="f0f56-120">**pSetupStringTableAddStringEx**</span><span class="sxs-lookup"><span data-stu-id="f0f56-120">**pSetupStringTableAddStringEx**</span></span>](psetupstringtableaddstringex.md)
-   [<span data-ttu-id="f0f56-121">**pSetupStringTableInitializeEx**</span><span class="sxs-lookup"><span data-stu-id="f0f56-121">**pSetupStringTableInitializeEx**</span></span>](psetupstringtableinitializeex.md)
-   [<span data-ttu-id="f0f56-122">**pSetupStringTableInitialize**</span><span class="sxs-lookup"><span data-stu-id="f0f56-122">**pSetupStringTableInitialize**</span></span>](psetupstringtableinitialize.md)
-   [<span data-ttu-id="f0f56-123">**pSetupVerifyCatalogFile**</span><span class="sxs-lookup"><span data-stu-id="f0f56-123">**pSetupVerifyCatalogFile**</span></span>](psetupverifycatalogfile.md)
-   [<span data-ttu-id="f0f56-124">**ricarica \_ configurazione**</span><span class="sxs-lookup"><span data-stu-id="f0f56-124">**reload\_config**</span></span>](reload-config.md)
-   [<span data-ttu-id="f0f56-125">**SxsLookupClrGuid**</span><span class="sxs-lookup"><span data-stu-id="f0f56-125">**SxsLookupClrGuid**</span></span>](sxslookupclrguid.md)
-   [<span data-ttu-id="f0f56-126">**UninstallComponent**</span><span class="sxs-lookup"><span data-stu-id="f0f56-126">**UninstallComponent**</span></span>](uninstallcomponent.md)
-   [<span data-ttu-id="f0f56-127">**VerifyCatalogFile**</span><span class="sxs-lookup"><span data-stu-id="f0f56-127">**VerifyCatalogFile**</span></span>](verifycatalogfile.md)

 

 
