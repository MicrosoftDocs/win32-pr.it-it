---
title: Interfaccia IDeliveryOptimizationJob (Deliveryoptimization. h)
description: Usare l'interfaccia IDeliveryOptimizationJob per scaricare gli intervalli di un file.
ms.assetid: 7549F3B2-47E9-44DA-BD9C-AEFB0C36FF15
keywords:
- Interfaccia IDeliveryOptimizationJob
- Interfaccia IDeliveryOptimizationJob, descritta
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6ee2ce35b8089e9b05b7291f535361e39140f856
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119754"
---
# <a name="ideliveryoptimizationjob-interface"></a><span data-ttu-id="aa15b-105">Interfaccia IDeliveryOptimizationJob</span><span class="sxs-lookup"><span data-stu-id="aa15b-105">IDeliveryOptimizationJob interface</span></span>

<span data-ttu-id="aa15b-106">Usare l'interfaccia **IDeliveryOptimizationJob** per scaricare gli intervalli di un file.</span><span class="sxs-lookup"><span data-stu-id="aa15b-106">Use the **IDeliveryOptimizationJob** interface to download ranges of a file.</span></span>

## <a name="members"></a><span data-ttu-id="aa15b-107">Membri</span><span class="sxs-lookup"><span data-stu-id="aa15b-107">Members</span></span>

<span data-ttu-id="aa15b-108">L'interfaccia **IDeliveryOptimizationJob** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="aa15b-108">The **IDeliveryOptimizationJob** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="aa15b-109">**IDeliveryOptimizationJob** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="aa15b-109">**IDeliveryOptimizationJob** also has these types of members:</span></span>

- [<span data-ttu-id="aa15b-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="aa15b-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="aa15b-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="aa15b-111">Methods</span></span>

<span data-ttu-id="aa15b-112">L'interfaccia **IDeliveryOptimizationJob** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="aa15b-112">The **IDeliveryOptimizationJob** interface has these methods.</span></span>



| <span data-ttu-id="aa15b-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="aa15b-113">Method</span></span>                                                                  | <span data-ttu-id="aa15b-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aa15b-114">Description</span></span>                                                                                         |
|:------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="aa15b-115">**AddFileWithRanges**</span><span class="sxs-lookup"><span data-stu-id="aa15b-115">**AddFileWithRanges**</span></span>](ideliveryoptimizationjob-addfilewithranges.md) | <span data-ttu-id="aa15b-116">Aggiunge un file a un processo di download e specifica gli intervalli del file che si desidera scaricare.</span><span class="sxs-lookup"><span data-stu-id="aa15b-116">Adds a file to a download job and specifies the ranges of the file you want to download.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="aa15b-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aa15b-117">Requirements</span></span>



| <span data-ttu-id="aa15b-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa15b-118">Requirement</span></span> | <span data-ttu-id="aa15b-119">Valore</span><span class="sxs-lookup"><span data-stu-id="aa15b-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa15b-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aa15b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="aa15b-121">Solo app desktop Windows 10 versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="aa15b-121">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="aa15b-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aa15b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="aa15b-123">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="aa15b-123">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="aa15b-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="aa15b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa15b-125"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa15b-125"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="aa15b-126">IDL</span><span class="sxs-lookup"><span data-stu-id="aa15b-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="aa15b-127"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="aa15b-127"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="aa15b-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="aa15b-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="aa15b-129"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="aa15b-129"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="aa15b-130">DLL</span><span class="sxs-lookup"><span data-stu-id="aa15b-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa15b-131"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa15b-131"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="aa15b-132">IID</span><span class="sxs-lookup"><span data-stu-id="aa15b-132">IID</span></span><br/>                      | <span data-ttu-id="aa15b-133">IID_IDeliveryOptimizationJob viene definito come EE2584CF-A69C-4848-B633-2649962B3EF7</span><span class="sxs-lookup"><span data-stu-id="aa15b-133">IID_IDeliveryOptimizationJob is defined as EE2584CF-A69C-4848-B633-2649962B3EF7</span></span><br/>         |



 

