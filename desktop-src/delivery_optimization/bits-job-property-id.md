---
title: Enumerazione BITS_JOB_PROPERTY_ID (Deliveryoptimization. h)
description: L'enumerazione BITS_JOB_PROPERTY_ID specifica l'ID della proprietà per il processo di esecuzione. Questa enumerazione viene utilizzata nell'Unione BITS_JOB_PROPERTY_VALUE per determinare il tipo di valore contenuto nell'Unione.
ms.assetid: B0F3C6C2-474F-4FD8-990A-770FAA993550
keywords:
- Enumerazione BITS_JOB_PROPERTY_ID
topic_type:
- apiref
api_name:
- BITS_JOB_PROPERTY_ID
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cd1d00d4dc12b27c1c80b0e18bb095641a56e322
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740319"
---
# <a name="bits_job_property_id-enumeration"></a><span data-ttu-id="cff3d-105">Enumerazione BITS_JOB_PROPERTY_ID</span><span class="sxs-lookup"><span data-stu-id="cff3d-105">BITS_JOB_PROPERTY_ID enumeration</span></span>

<span data-ttu-id="cff3d-106">L'enumerazione **BITS_JOB_PROPERTY_ID** specifica l'ID della proprietà per il processo di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="cff3d-106">The **BITS_JOB_PROPERTY_ID** enumeration specifies the ID of the property for the DO job.</span></span> <span data-ttu-id="cff3d-107">Questa enumerazione viene utilizzata nell'Unione [**BITS_JOB_PROPERTY_VALUE**](bits-job-property-value-.md) per determinare il tipo di valore contenuto nell'Unione.</span><span class="sxs-lookup"><span data-stu-id="cff3d-107">This enumeration is used in the [**BITS_JOB_PROPERTY_VALUE**](bits-job-property-value-.md) union to determine the type of value contained in the union.</span></span>

## <a name="syntax"></a><span data-ttu-id="cff3d-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cff3d-108">Syntax</span></span>


```C++
typedef enum  { 
  BITS_JOB_PROPERTY_ID_COST_FLAGS                     = 1,
  BITS_JOB_PROPERTY_NOTIFICATION_CLSID                = 2,
  BITS_JOB_PROPERTY_DYNAMIC_CONTENT                   = 3,
  BITS_JOB_PROPERTY_HIGH_PERFORMANCE                  = 4,
  BITS_JOB_PROPERTY_MAX_DOWNLOAD_SIZE                 = 5,
  BITS_JOB_PROPERTY_USE_STORED_CREDENTIALS            = 7,
  BITS_JOB_PROPERTY_MINIMUM_NOTIFICATION_INTERVAL_MS  = 9,
  BITS_JOB_PROPERTY_ON_DEMAND_MODE                    = 10
} BITS_JOB_PROPERTY_ID;
```



## <a name="constants"></a><span data-ttu-id="cff3d-109">Costanti</span><span class="sxs-lookup"><span data-stu-id="cff3d-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="cff3d-110"><span id="BITS_JOB_PROPERTY_ID_COST_FLAGS"></span><span id="bits_job_property_id_cost_flags"></span>**BITS_JOB_PROPERTY_ID_COST_FLAGS**</span><span class="sxs-lookup"><span data-stu-id="cff3d-110"><span id="BITS_JOB_PROPERTY_ID_COST_FLAGS"></span><span id="bits_job_property_id_cost_flags"></span>**BITS_JOB_PROPERTY_ID_COST_FLAGS**</span></span>
</dt> <dd>

<span data-ttu-id="cff3d-111">ID utilizzato per [controllare il comportamento di trasferimento](https://www.bing.com/search?q=control+transfer+behavior) su reti telefoniche e/o analoghe.</span><span class="sxs-lookup"><span data-stu-id="cff3d-111">The ID that is used to [control transfer behavior](https://www.bing.com/search?q=control+transfer+behavior) over cellular and/or similar networks.</span></span> <span data-ttu-id="cff3d-112">Questa proprietà può essere modificata mentre è in corso un trasferimento. i nuovi flag di costo diverranno effettivi immediatamente.</span><span class="sxs-lookup"><span data-stu-id="cff3d-112">This property may be changed while a transfer is ongoing   the new cost flags will take effect immediately.</span></span>

<span data-ttu-id="cff3d-113">Questa proprietà usa il campo **Dword** **BITS_JOB_PROPERTY_VALUE** s.</span><span class="sxs-lookup"><span data-stu-id="cff3d-113">This property uses the **BITS_JOB_PROPERTY_VALUE** s **Dword** field.</span></span>

</dd> <dt>

<span data-ttu-id="cff3d-114"><span id="BITS_JOB_PROPERTY_NOTIFICATION_CLSID"></span><span id="bits_job_property_notification_clsid"></span>**BITS_JOB_PROPERTY_NOTIFICATION_CLSID**</span><span class="sxs-lookup"><span data-stu-id="cff3d-114"><span id="BITS_JOB_PROPERTY_NOTIFICATION_CLSID"></span><span id="bits_job_property_notification_clsid"></span>**BITS_JOB_PROPERTY_NOTIFICATION_CLSID**</span></span>
</dt> <dd>

<span data-ttu-id="cff3d-115">ID utilizzato per [registrare un callback com](https://www.bing.com/search?q=register+a+COM+callback) tramite CLSID per ricevere notifiche sullo stato di avanzamento e il completamento di un processo di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="cff3d-115">The ID that is used to [register a COM callback](https://www.bing.com/search?q=register+a+COM+callback) by CLSID to receive notifications about the progress and completion of a DO job.</span></span> <span data-ttu-id="cff3d-116">Il CLSID deve fare riferimento a una classe associata a un server COM out-of-process registrato.</span><span class="sxs-lookup"><span data-stu-id="cff3d-116">The CLSID must refer to a class associated with a registered out-of-process COM server.</span></span> <span data-ttu-id="cff3d-117">Può anche essere impostato su **GUID_NULL** per cancellare una notifica CLSID precedentemente impostata.</span><span class="sxs-lookup"><span data-stu-id="cff3d-117">It may also be set to **GUID_NULL** to clear a previously set notification CLSID.</span></span>

<span data-ttu-id="cff3d-118">Questa proprietà usa il campo **CLsID** **BITS_JOB_PROPERTY_VALUE** s.</span><span class="sxs-lookup"><span data-stu-id="cff3d-118">This property uses the **BITS_JOB_PROPERTY_VALUE** s **CLsID** field.</span></span>

</dd> <dt>

<span data-ttu-id="cff3d-119"><span id="BITS_JOB_PROPERTY_DYNAMIC_CONTENT"></span><span id="bits_job_property_dynamic_content"></span>**BITS_JOB_PROPERTY_DYNAMIC_CONTENT**</span><span class="sxs-lookup"><span data-stu-id="cff3d-119"><span id="BITS_JOB_PROPERTY_DYNAMIC_CONTENT"></span><span id="bits_job_property_dynamic_content"></span>**BITS_JOB_PROPERTY_DYNAMIC_CONTENT**</span></span>
</dt> <dd>

<span data-ttu-id="cff3d-120">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="cff3d-120">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="cff3d-121"><span id="BITS_JOB_PROPERTY_HIGH_PERFORMANCE"></span><span id="bits_job_property_high_performance"></span>**BITS_JOB_PROPERTY_HIGH_PERFORMANCE**</span><span class="sxs-lookup"><span data-stu-id="cff3d-121"><span id="BITS_JOB_PROPERTY_HIGH_PERFORMANCE"></span><span id="bits_job_property_high_performance"></span>**BITS_JOB_PROPERTY_HIGH_PERFORMANCE**</span></span>
</dt> <dd>

<span data-ttu-id="cff3d-122">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="cff3d-122">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="cff3d-123"><span id="BITS_JOB_PROPERTY_MAX_DOWNLOAD_SIZE"></span><span id="bits_job_property_max_download_size"></span>**BITS_JOB_PROPERTY_MAX_DOWNLOAD_SIZE**</span><span class="sxs-lookup"><span data-stu-id="cff3d-123"><span id="BITS_JOB_PROPERTY_MAX_DOWNLOAD_SIZE"></span><span id="bits_job_property_max_download_size"></span>**BITS_JOB_PROPERTY_MAX_DOWNLOAD_SIZE**</span></span>
</dt> <dd>

<span data-ttu-id="cff3d-124">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="cff3d-124">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="cff3d-125"><span id="BITS_JOB_PROPERTY_USE_STORED_CREDENTIALS"></span><span id="bits_job_property_use_stored_credentials"></span>**BITS_JOB_PROPERTY_USE_STORED_CREDENTIALS**</span><span class="sxs-lookup"><span data-stu-id="cff3d-125"><span id="BITS_JOB_PROPERTY_USE_STORED_CREDENTIALS"></span><span id="bits_job_property_use_stored_credentials"></span>**BITS_JOB_PROPERTY_USE_STORED_CREDENTIALS**</span></span>
</dt> <dd>

<span data-ttu-id="cff3d-126">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="cff3d-126">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="cff3d-127"><span id="BITS_JOB_PROPERTY_MINIMUM_NOTIFICATION_INTERVAL_MS"></span><span id="bits_job_property_minimum_notification_interval_ms"></span>**BITS_JOB_PROPERTY_MINIMUM_NOTIFICATION_INTERVAL_MS**</span><span class="sxs-lookup"><span data-stu-id="cff3d-127"><span id="BITS_JOB_PROPERTY_MINIMUM_NOTIFICATION_INTERVAL_MS"></span><span id="bits_job_property_minimum_notification_interval_ms"></span>**BITS_JOB_PROPERTY_MINIMUM_NOTIFICATION_INTERVAL_MS**</span></span>
</dt> <dd>

<span data-ttu-id="cff3d-128">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="cff3d-128">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="cff3d-129"><span id="BITS_JOB_PROPERTY_ON_DEMAND_MODE"></span><span id="bits_job_property_on_demand_mode"></span>**BITS_JOB_PROPERTY_ON_DEMAND_MODE**</span><span class="sxs-lookup"><span data-stu-id="cff3d-129"><span id="BITS_JOB_PROPERTY_ON_DEMAND_MODE"></span><span id="bits_job_property_on_demand_mode"></span>**BITS_JOB_PROPERTY_ON_DEMAND_MODE**</span></span>
</dt> <dd>

<span data-ttu-id="cff3d-130">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="cff3d-130">Not supported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cff3d-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cff3d-131">Requirements</span></span>



| <span data-ttu-id="cff3d-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="cff3d-132">Requirement</span></span> | <span data-ttu-id="cff3d-133">Valore</span><span class="sxs-lookup"><span data-stu-id="cff3d-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cff3d-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cff3d-134">Minimum supported client</span></span><br/> | <span data-ttu-id="cff3d-135">Solo app desktop Windows 10 versione 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="cff3d-135">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="cff3d-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cff3d-136">Minimum supported server</span></span><br/> | <span data-ttu-id="cff3d-137">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="cff3d-137">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="cff3d-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cff3d-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="cff3d-139"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="cff3d-139"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cff3d-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cff3d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cff3d-141">**BITS_JOB_PROPERTY_ID**</span><span class="sxs-lookup"><span data-stu-id="cff3d-141">**BITS_JOB_PROPERTY_ID**</span></span>](bits-job-property-id.md)
</dt> <dt>

[<span data-ttu-id="cff3d-142">**BITS_JOB_PROPERTY_VALUE**</span><span class="sxs-lookup"><span data-stu-id="cff3d-142">**BITS_JOB_PROPERTY_VALUE**</span></span>](bits-job-property-value-.md)
</dt> <dt>

[<span data-ttu-id="cff3d-143">**BITS_JOB_TRANSFER_POLICY**</span><span class="sxs-lookup"><span data-stu-id="cff3d-143">**BITS_JOB_TRANSFER_POLICY**</span></span>](bits-job-transfer-policy-.md)
</dt> <dt>

[<span data-ttu-id="cff3d-144">**IBackgroundCopyJob5:: SetProperty**</span><span class="sxs-lookup"><span data-stu-id="cff3d-144">**IBackgroundCopyJob5::SetProperty**</span></span>](ibackgroundcopyjob5-setproperty.md)
</dt> <dt>

[<span data-ttu-id="cff3d-145">**IBackgroundCopyJob5:: GetProperty**</span><span class="sxs-lookup"><span data-stu-id="cff3d-145">**IBackgroundCopyJob5::GetProperty**</span></span>](ibackgroundcopyjob5-getproperty.md)
</dt> </dl>

 

 





