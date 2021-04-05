---
title: Informazioni di riferimento sul driver installabile
description: Informazioni di riferimento sul driver installabile
ms.assetid: 869b92f1-2711-4198-9911-3df1ebc58d5f
keywords:
- Windows Multimedia, Guida di riferimento per i driver installabili
- informazioni di riferimento sul driver installabile
- driver installabili, informazioni di riferimento
- informazioni di riferimento sul driver installabile, informazioni
- informazioni di riferimento per i driver installabili, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e90475063f9d9211e841902fe73d2f09dc6130d8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103872373"
---
# <a name="installable-driver-reference"></a><span data-ttu-id="23ecf-108">Informazioni di riferimento sul driver installabile</span><span class="sxs-lookup"><span data-stu-id="23ecf-108">Installable Driver Reference</span></span>

<span data-ttu-id="23ecf-109">Le funzioni e i messaggi associati a driver installabili sono raggruppati come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="23ecf-109">The functions and messages associated with installable drivers are grouped as follows.</span></span>

## <a name="loading-and-unloading-drivers"></a><span data-ttu-id="23ecf-110">Caricamento e scaricamento di driver</span><span class="sxs-lookup"><span data-stu-id="23ecf-110">Loading and Unloading Drivers</span></span>

-   [<span data-ttu-id="23ecf-111">GetDriverModuleHandle</span><span class="sxs-lookup"><span data-stu-id="23ecf-111">GetDriverModuleHandle</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-getdrivermodulehandle)
-   [<span data-ttu-id="23ecf-112">OpenDriver</span><span class="sxs-lookup"><span data-stu-id="23ecf-112">OpenDriver</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-opendriver)
-   [<span data-ttu-id="23ecf-113">SendDriverMessage</span><span class="sxs-lookup"><span data-stu-id="23ecf-113">SendDriverMessage</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-senddrivermessage)

## <a name="closedriver"></a><span data-ttu-id="23ecf-114">CloseDriver</span><span class="sxs-lookup"><span data-stu-id="23ecf-114">CloseDriver</span></span>

-   [<span data-ttu-id="23ecf-115">**\_chiusura DRV**</span><span class="sxs-lookup"><span data-stu-id="23ecf-115">**DRV\_CLOSE**</span></span>](drv-close.md)
-   [<span data-ttu-id="23ecf-116">**\_disabilitazione DRV**</span><span class="sxs-lookup"><span data-stu-id="23ecf-116">**DRV\_DISABLE**</span></span>](drv-disable.md)
-   [<span data-ttu-id="23ecf-117">**\_Abilitazione di DRV**</span><span class="sxs-lookup"><span data-stu-id="23ecf-117">**DRV\_ENABLE**</span></span>](drv-enable.md)
-   [<span data-ttu-id="23ecf-118">**DRV \_ disponibile**</span><span class="sxs-lookup"><span data-stu-id="23ecf-118">**DRV\_FREE**</span></span>](drv-free.md)
-   [<span data-ttu-id="23ecf-119">**\_caricamento DRV**</span><span class="sxs-lookup"><span data-stu-id="23ecf-119">**DRV\_LOAD**</span></span>](drv-load.md)
-   [<span data-ttu-id="23ecf-120">**DRV \_ aperto**</span><span class="sxs-lookup"><span data-stu-id="23ecf-120">**DRV\_OPEN**</span></span>](drv-open.md)

## <a name="configuring-a-driver"></a><span data-ttu-id="23ecf-121">Configurazione di un driver</span><span class="sxs-lookup"><span data-stu-id="23ecf-121">Configuring a Driver</span></span>

-   [<span data-ttu-id="23ecf-122">**configurazione di DRV \_**</span><span class="sxs-lookup"><span data-stu-id="23ecf-122">**DRV\_CONFIGURE**</span></span>](drv-configure.md)
-   [<span data-ttu-id="23ecf-123">**\_QUERYCONFIGURE DRV**</span><span class="sxs-lookup"><span data-stu-id="23ecf-123">**DRV\_QUERYCONFIGURE**</span></span>](drv-queryconfigure.md)
-   [<span data-ttu-id="23ecf-124">**DRVCONFIGINFO**</span><span class="sxs-lookup"><span data-stu-id="23ecf-124">**DRVCONFIGINFO**</span></span>](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo)

## <a name="installing-a-driver"></a><span data-ttu-id="23ecf-125">Installazione di un driver</span><span class="sxs-lookup"><span data-stu-id="23ecf-125">Installing a Driver</span></span>

-   [<span data-ttu-id="23ecf-126">**installazione di DRV \_**</span><span class="sxs-lookup"><span data-stu-id="23ecf-126">**DRV\_INSTALL**</span></span>](drv-install.md)
-   [<span data-ttu-id="23ecf-127">**\_Rimuovi DRV**</span><span class="sxs-lookup"><span data-stu-id="23ecf-127">**DRV\_REMOVE**</span></span>](drv-remove.md)

## <a name="driver-functions"></a><span data-ttu-id="23ecf-128">Funzioni driver</span><span class="sxs-lookup"><span data-stu-id="23ecf-128">Driver Functions</span></span>

-   [<span data-ttu-id="23ecf-129">DefDriverProc</span><span class="sxs-lookup"><span data-stu-id="23ecf-129">DefDriverProc</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-defdriverproc)
-   [<span data-ttu-id="23ecf-130">DriverCallback</span><span class="sxs-lookup"><span data-stu-id="23ecf-130">DriverCallback</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-drivercallback)
-   [<span data-ttu-id="23ecf-131">DriverProc</span><span class="sxs-lookup"><span data-stu-id="23ecf-131">DriverProc</span></span>](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc)

## <a name="related-topics"></a><span data-ttu-id="23ecf-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="23ecf-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23ecf-133">Driver installabili</span><span class="sxs-lookup"><span data-stu-id="23ecf-133">Installable Drivers</span></span>](installable-drivers.md)
</dt> </dl>

 

 