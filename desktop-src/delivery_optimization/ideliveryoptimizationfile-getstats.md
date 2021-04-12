---
title: Metodo GetStats di IDeliveryOptimizationFile (Deliveryoptimization. h)
description: Restituisce le statistiche di download e caricamento per un file specifico.
ms.assetid: 8A3AD658-F1AD-4EA5-B010-AB7B88126FD6
keywords:
- GetStats (metodo)
- Metodo GetStats, interfaccia IDeliveryOptimizationFile
- Interfaccia IDeliveryOptimizationFile, Metodo GetStats
topic_type:
- apiref
api_name:
- IDeliveryOptimizationFile.GetStats
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 08c5cff0672130049c325a00cb63c8dbc5c2e8ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400839"
---
# <a name="ideliveryoptimizationfilegetstats-method"></a><span data-ttu-id="f61ef-106">Metodo IDeliveryOptimizationFile:: GetStats</span><span class="sxs-lookup"><span data-stu-id="f61ef-106">IDeliveryOptimizationFile::GetStats method</span></span>

<span data-ttu-id="f61ef-107">Restituisce le statistiche di download e caricamento per un file specifico.</span><span class="sxs-lookup"><span data-stu-id="f61ef-107">Returns download and upload stats for a specific file.</span></span>

## <a name="syntax"></a><span data-ttu-id="f61ef-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f61ef-108">Syntax</span></span>


```C++
HRESULT GetStats(
  [out] DOSwarmStats *swarmStats
);
```



## <a name="parameters"></a><span data-ttu-id="f61ef-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="f61ef-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f61ef-110">*swarmStats* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f61ef-110">*swarmStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f61ef-111">Restituisce le statistiche di download e caricamento per un file specifico.</span><span class="sxs-lookup"><span data-stu-id="f61ef-111">Returns download and upload stats for a specific file.</span></span> <span data-ttu-id="f61ef-112">Per informazioni dettagliate, vedere la struttura [**DOSwarmStats**](doswarmstats.md) .</span><span class="sxs-lookup"><span data-stu-id="f61ef-112">See the [**DOSwarmStats**](doswarmstats.md) structure for details.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f61ef-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f61ef-113">Return value</span></span>

<span data-ttu-id="f61ef-114">Questo metodo deve restituire **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="f61ef-114">This method should return **S_OK**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f61ef-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f61ef-115">Requirements</span></span>



| <span data-ttu-id="f61ef-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f61ef-116">Requirement</span></span> | <span data-ttu-id="f61ef-117">Valore</span><span class="sxs-lookup"><span data-stu-id="f61ef-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f61ef-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f61ef-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f61ef-119">Solo app desktop Windows 10 versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="f61ef-119">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f61ef-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f61ef-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f61ef-121">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f61ef-121">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="f61ef-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f61ef-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f61ef-123"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="f61ef-123"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="f61ef-124">IDL</span><span class="sxs-lookup"><span data-stu-id="f61ef-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f61ef-125"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f61ef-125"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="f61ef-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="f61ef-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="f61ef-127"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f61ef-127"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="f61ef-128">DLL</span><span class="sxs-lookup"><span data-stu-id="f61ef-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f61ef-129"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f61ef-129"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="f61ef-130">IID</span><span class="sxs-lookup"><span data-stu-id="f61ef-130">IID</span></span><br/>                      | <span data-ttu-id="f61ef-131">IID_IDeliveryOptimizationFile viene definito come B76B9699-E99E-4101-803F-A20E325D93E2</span><span class="sxs-lookup"><span data-stu-id="f61ef-131">IID_IDeliveryOptimizationFile is defined as B76B9699-E99E-4101-803F-A20E325D93E2</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="f61ef-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f61ef-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f61ef-133">**IDeliveryOptimizationFile**</span><span class="sxs-lookup"><span data-stu-id="f61ef-133">**IDeliveryOptimizationFile**</span></span>](ideliveryoptimizationfile.md)
</dt> </dl>

 

 





