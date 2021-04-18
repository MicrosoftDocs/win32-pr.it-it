---
title: Interfaccia IDeliveryOptimizationFile
description: Implementare l'interfaccia IDeliveryOptimizationFile per identificare lo stato di un file specifico.
ms.assetid: 4D1D82E1-B39C-4634-A0B7-BC4322796AB2
keywords:
- Interfaccia IDeliveryOptimizationFile
- Interfaccia IDeliveryOptimizationFile, descritta
topic_type:
- apiref
api_name:
- IDeliveryOptimizationFile
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2b86434f4be2f7d14ae46f4af92784c1be4fd1aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301434"
---
# <a name="ideliveryoptimizationfile-interface"></a><span data-ttu-id="f6a20-105">Interfaccia IDeliveryOptimizationFile</span><span class="sxs-lookup"><span data-stu-id="f6a20-105">IDeliveryOptimizationFile interface</span></span>

<span data-ttu-id="f6a20-106">Implementare l'interfaccia **IDeliveryOptimizationFile** per identificare lo stato di un file specifico.</span><span class="sxs-lookup"><span data-stu-id="f6a20-106">Implement the **IDeliveryOptimizationFile** interface to identify the status of a specific file.</span></span>

## <a name="members"></a><span data-ttu-id="f6a20-107">Membri</span><span class="sxs-lookup"><span data-stu-id="f6a20-107">Members</span></span>

<span data-ttu-id="f6a20-108">L'interfaccia **IDeliveryOptimizationFile** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="f6a20-108">The **IDeliveryOptimizationFile** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f6a20-109">**IDeliveryOptimizationFile** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f6a20-109">**IDeliveryOptimizationFile** also has these types of members:</span></span>

-   [<span data-ttu-id="f6a20-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="f6a20-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f6a20-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="f6a20-111">Methods</span></span>

<span data-ttu-id="f6a20-112">L'interfaccia **IDeliveryOptimizationFile** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="f6a20-112">The **IDeliveryOptimizationFile** interface has these methods.</span></span>



| <span data-ttu-id="f6a20-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="f6a20-113">Method</span></span>                                                 | <span data-ttu-id="f6a20-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f6a20-114">Description</span></span>                                                       |
|:-------------------------------------------------------|:------------------------------------------------------------------|
| [<span data-ttu-id="f6a20-115">**GetStats**</span><span class="sxs-lookup"><span data-stu-id="f6a20-115">**GetStats**</span></span>](ideliveryoptimizationfile-getstats.md) | <span data-ttu-id="f6a20-116">Restituisce le statistiche di download e caricamento per un file specifico.</span><span class="sxs-lookup"><span data-stu-id="f6a20-116">Returns download and upload stats for a specific file.</span></span><br/> |

## <a name="requirements"></a><span data-ttu-id="f6a20-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f6a20-117">Requirements</span></span>

| <span data-ttu-id="f6a20-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6a20-118">Requirement</span></span> | <span data-ttu-id="f6a20-119">Valore</span><span class="sxs-lookup"><span data-stu-id="f6a20-119">Value</span></span> |
|-------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f6a20-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f6a20-120">Minimum supported client</span></span>      | <span data-ttu-id="f6a20-121">Solo app desktop Windows 10 versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="f6a20-121">Windows 10, version 1709 \[desktop apps only\]</span></span>                                   |
| <span data-ttu-id="f6a20-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f6a20-122">Minimum supported server</span></span>      | <span data-ttu-id="f6a20-123">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f6a20-123">Windows Server, version 1709 \[desktop apps only\]</span></span>                               |
| <span data-ttu-id="f6a20-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f6a20-124">Header</span></span>                        | <span data-ttu-id="f6a20-125">Deliveryoptimization. h</span><span class="sxs-lookup"><span data-stu-id="f6a20-125">Deliveryoptimization.h</span></span>                                                           |
| <span data-ttu-id="f6a20-126">IDL</span><span class="sxs-lookup"><span data-stu-id="f6a20-126">IDL</span></span>                           | <span data-ttu-id="f6a20-127">DeliveryOptimization. idl</span><span class="sxs-lookup"><span data-stu-id="f6a20-127">DeliveryOptimization.idl</span></span>                                                         |
| <span data-ttu-id="f6a20-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="f6a20-128">Library</span></span>                       | <span data-ttu-id="f6a20-129">Dosvc. lib</span><span class="sxs-lookup"><span data-stu-id="f6a20-129">Dosvc.lib</span></span>                                                                        |
| <span data-ttu-id="f6a20-130">DLL</span><span class="sxs-lookup"><span data-stu-id="f6a20-130">DLL</span></span>                           | <span data-ttu-id="f6a20-131">Dosvc.dll</span><span class="sxs-lookup"><span data-stu-id="f6a20-131">Dosvc.dll</span></span>                                                                        |
| <span data-ttu-id="f6a20-132">IID</span><span class="sxs-lookup"><span data-stu-id="f6a20-132">IID</span></span>                           | <span data-ttu-id="f6a20-133">IID_IDeliveryOptimizationFile viene definito come B76B9699-E99E-4101-803F-A20E325D93E2</span><span class="sxs-lookup"><span data-stu-id="f6a20-133">IID_IDeliveryOptimizationFile is defined as B76B9699-E99E-4101-803F-A20E325D93E2</span></span> |
