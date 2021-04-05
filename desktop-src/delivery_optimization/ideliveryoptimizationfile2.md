---
title: Interfaccia IDeliveryOptimizationFile2
description: IDeliveryOptimizationFile2 supporta l'impostazione e il recupero di proprietà facoltative dei file.
keywords:
- Interfaccia IDeliveryOptimizationFile2
- Interfaccia IDeliveryOptimizationFile2, descritta
topic_type:
- apiref
api_name:
- IDeliveryOptimizationFile2
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a45efd821116b24e883ec29d494a1d588559f57a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048133"
---
# <a name="ideliveryoptimizationfile2-interface"></a><span data-ttu-id="4e2aa-105">Interfaccia IDeliveryOptimizationFile2</span><span class="sxs-lookup"><span data-stu-id="4e2aa-105">IDeliveryOptimizationFile2 interface</span></span>

<span data-ttu-id="4e2aa-106">**IDeliveryOptimizationFile2** supporta l'impostazione e il recupero di proprietà facoltative dei file.</span><span class="sxs-lookup"><span data-stu-id="4e2aa-106">The **IDeliveryOptimizationFile2** supports setting and getting optional file properties.</span></span> 

## <a name="members"></a><span data-ttu-id="4e2aa-107">Membri</span><span class="sxs-lookup"><span data-stu-id="4e2aa-107">Members</span></span>

<span data-ttu-id="4e2aa-108">L'interfaccia **IDeliveryOptimizationFile2** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="4e2aa-108">The **IDeliveryOptimizationFile2** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="4e2aa-109">**IDeliveryOptimizationFile2** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="4e2aa-109">**IDeliveryOptimizationFile2** also has these types of members:</span></span>

- [<span data-ttu-id="4e2aa-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="4e2aa-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4e2aa-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="4e2aa-111">Methods</span></span>

<span data-ttu-id="4e2aa-112">L'interfaccia **IDeliveryOptimizationFile2** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="4e2aa-112">The **IDeliveryOptimizationFile2** interface has these methods.</span></span>

| <span data-ttu-id="4e2aa-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="4e2aa-113">Method</span></span>                                                 | <span data-ttu-id="4e2aa-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4e2aa-114">Description</span></span>                                                  |
|:-------------------------------------------------------|:-------------------------------------------------------------|
| [<span data-ttu-id="4e2aa-115">**GetProperty**</span><span class="sxs-lookup"><span data-stu-id="4e2aa-115">**GetProperty**</span></span>](ideliveryoptimizationfile2-getproperty.md)  | <span data-ttu-id="4e2aa-116">Questo metodo restituisce una singola proprietà del file DO.</span><span class="sxs-lookup"><span data-stu-id="4e2aa-116">This method returns a single property of the DO file.</span></span> |
| [<span data-ttu-id="4e2aa-117">**SetProperty**</span><span class="sxs-lookup"><span data-stu-id="4e2aa-117">**SetProperty**</span></span>](ideliveryoptimizationfile2-setproperty.md)  | <span data-ttu-id="4e2aa-118">Questo metodo imposta una singola proprietà del file DO.</span><span class="sxs-lookup"><span data-stu-id="4e2aa-118">This method sets a single property of the DO file.</span></span>    |

## <a name="requirements"></a><span data-ttu-id="4e2aa-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4e2aa-119">Requirements</span></span>

| <span data-ttu-id="4e2aa-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e2aa-120">Requirement</span></span> | <span data-ttu-id="4e2aa-121">Valore</span><span class="sxs-lookup"><span data-stu-id="4e2aa-121">Value</span></span> |
|-------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="4e2aa-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4e2aa-122">Minimum supported client</span></span>      | <span data-ttu-id="4e2aa-123">Solo app desktop Windows 10 versione 1803 \[\]</span><span class="sxs-lookup"><span data-stu-id="4e2aa-123">Windows 10, version 1803 \[desktop apps only\]</span></span>                                    |
| <span data-ttu-id="4e2aa-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4e2aa-124">Minimum supported server</span></span>      | <span data-ttu-id="4e2aa-125">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4e2aa-125">Windows Server, version 1709 \[desktop apps only\]</span></span>                                |
| <span data-ttu-id="4e2aa-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4e2aa-126">Header</span></span>                        | <span data-ttu-id="4e2aa-127">Deliveryoptimization. h</span><span class="sxs-lookup"><span data-stu-id="4e2aa-127">Deliveryoptimization.h</span></span>                                                            |
| <span data-ttu-id="4e2aa-128">IDL</span><span class="sxs-lookup"><span data-stu-id="4e2aa-128">IDL</span></span>                           | <span data-ttu-id="4e2aa-129">DeliveryOptimization. idl</span><span class="sxs-lookup"><span data-stu-id="4e2aa-129">DeliveryOptimization.idl</span></span>                                                          |
| <span data-ttu-id="4e2aa-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="4e2aa-130">Library</span></span>                       | <span data-ttu-id="4e2aa-131">Dosvc. lib</span><span class="sxs-lookup"><span data-stu-id="4e2aa-131">Dosvc.lib</span></span>                                                                         |
| <span data-ttu-id="4e2aa-132">DLL</span><span class="sxs-lookup"><span data-stu-id="4e2aa-132">DLL</span></span>                           | <span data-ttu-id="4e2aa-133">Dosvc.dll</span><span class="sxs-lookup"><span data-stu-id="4e2aa-133">Dosvc.dll</span></span>                                                                         |
| <span data-ttu-id="4e2aa-134">IID</span><span class="sxs-lookup"><span data-stu-id="4e2aa-134">IID</span></span>                           | <span data-ttu-id="4e2aa-135">IID_IDeliveryOptimizationFile2 viene definito come 3A87296F-6EC2-4126-AB29-E3F8DC4CC390</span><span class="sxs-lookup"><span data-stu-id="4e2aa-135">IID_IDeliveryOptimizationFile2 is defined as 3A87296F-6EC2-4126-AB29-E3F8DC4CC390</span></span> |
