---
description: Crea un punto di riferimento di una raccolta di sistemi virtuali.
ms.assetid: 40ec5715-0dbc-43e3-a305-c8c31de60977
title: Metodo CreateReferencePoint della classe Msvm_CollectionReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointService.CreateReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 7681795ee18965e3e04b75c800e3e574d6627ea9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350316"
---
# <a name="createreferencepoint-method-of-the-msvm_collectionreferencepointservice-class"></a><span data-ttu-id="5b2cc-103">Metodo CreateReferencePoint della classe MSVM \_ CollectionReferencePointService</span><span class="sxs-lookup"><span data-stu-id="5b2cc-103">CreateReferencePoint method of the Msvm\_CollectionReferencePointService class</span></span>

<span data-ttu-id="5b2cc-104">Crea un punto di riferimento di una raccolta di sistemi virtuali.</span><span class="sxs-lookup"><span data-stu-id="5b2cc-104">Creates a reference point of a virtual system collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b2cc-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5b2cc-105">Syntax</span></span>


```mof
uint32 CreateReferencePoint(
  [in]      Msvm_VirtualSystemCollection REF Collection,
  [in]      string                           ReferencePointSettings,
  [in]      uint16                           ReferencePointType,
  [in, out] CIM_Collection               REF ResultingReferencePointCollection,
  [out]     CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="5b2cc-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5b2cc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b2cc-107">*Raccolta* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="5b2cc-107">*Collection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b2cc-108">Riferimento alla raccolta di sistemi virtuali interessata.</span><span class="sxs-lookup"><span data-stu-id="5b2cc-108">Reference to the affected virtual system collection.</span></span>

</dd> <dt>

<span data-ttu-id="5b2cc-109">*ReferencePointSettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5b2cc-109">*ReferencePointSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b2cc-110">Impostazioni parametri.</span><span class="sxs-lookup"><span data-stu-id="5b2cc-110">Parameter settings.</span></span>

</dd> <dt>

<span data-ttu-id="5b2cc-111">*ReferencePointType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5b2cc-111">*ReferencePointType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b2cc-112">Indica il tipo del punto di riferimento.</span><span class="sxs-lookup"><span data-stu-id="5b2cc-112">Indicates the type of the reference point.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5b2cc-113"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="5b2cc-113"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>

<span data-ttu-id="5b2cc-114"><span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>**Basato su log** (1)</span><span class="sxs-lookup"><span data-stu-id="5b2cc-114"><span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>**Log based** (1)</span></span>


</dt> <dd>

<span data-ttu-id="5b2cc-115">Rilevamento del log della replica Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="5b2cc-115">Hyper-V replica log tracking.</span></span>

</dd> <dt>

<span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>

<span data-ttu-id="5b2cc-116"><span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>**Basato su RCT** (2)</span><span class="sxs-lookup"><span data-stu-id="5b2cc-116"><span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>**RCT based** (2)</span></span>


</dt> <dd>

<span data-ttu-id="5b2cc-117">Basato su Rilevamento modifiche resiliente di dischi virtuali.</span><span class="sxs-lookup"><span data-stu-id="5b2cc-117">Based on Resilient Change Tracking of virtual disks.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="5b2cc-118"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="5b2cc-118"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span data-ttu-id="5b2cc-119"><span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="5b2cc-119"><span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Vendor Specific** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="5b2cc-120">*ResultingReferencePointCollection* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="5b2cc-120">*ResultingReferencePointCollection* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5b2cc-121">Punto di riferimento risultante di una raccolta di sistemi virtuali.</span><span class="sxs-lookup"><span data-stu-id="5b2cc-121">Resulting reference point of a virtual system collection.</span></span>

</dd> <dt>

<span data-ttu-id="5b2cc-122">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="5b2cc-122">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5b2cc-123">Se l'operazione è a esecuzione prolungata, è possibile che venga restituito un processo.</span><span class="sxs-lookup"><span data-stu-id="5b2cc-123">If the operation is long running, then optionally a job may be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b2cc-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5b2cc-124">Return value</span></span>

<span data-ttu-id="5b2cc-125">Se ha esito positivo, restituisce 0 (nessun errore) o 4096 (processo avviato); in caso contrario, viene restituito un errore.</span><span class="sxs-lookup"><span data-stu-id="5b2cc-125">If successful, returns either 0 (no error), or 4096 (job started); otherwise, return an error.</span></span>

<dl> <dt>

<span data-ttu-id="5b2cc-126">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="5b2cc-126">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="5b2cc-127">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="5b2cc-127">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="5b2cc-128">**Non riuscito** (2)</span><span class="sxs-lookup"><span data-stu-id="5b2cc-128">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="5b2cc-129">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="5b2cc-129">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="5b2cc-130">**Parametro non valido** (4)</span><span class="sxs-lookup"><span data-stu-id="5b2cc-130">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="5b2cc-131">**Stato non valido** (5)</span><span class="sxs-lookup"><span data-stu-id="5b2cc-131">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="5b2cc-132">**Tipo non valido** (6)</span><span class="sxs-lookup"><span data-stu-id="5b2cc-132">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="5b2cc-133">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="5b2cc-133">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="5b2cc-134">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="5b2cc-134">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="5b2cc-135">**Metodo riservato** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="5b2cc-135">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="5b2cc-136">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="5b2cc-136">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="5b2cc-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5b2cc-137">Requirements</span></span>



| <span data-ttu-id="5b2cc-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b2cc-138">Requirement</span></span> | <span data-ttu-id="5b2cc-139">Valore</span><span class="sxs-lookup"><span data-stu-id="5b2cc-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b2cc-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5b2cc-140">Minimum supported client</span></span><br/> | <span data-ttu-id="5b2cc-141">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="5b2cc-141">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="5b2cc-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5b2cc-142">Minimum supported server</span></span><br/> | <span data-ttu-id="5b2cc-143">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="5b2cc-143">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="5b2cc-144">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5b2cc-144">Namespace</span></span><br/>                | <span data-ttu-id="5b2cc-145">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="5b2cc-145">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="5b2cc-146">MOF</span><span class="sxs-lookup"><span data-stu-id="5b2cc-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5b2cc-147"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5b2cc-147"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5b2cc-148">DLL</span><span class="sxs-lookup"><span data-stu-id="5b2cc-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5b2cc-149"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5b2cc-149"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5b2cc-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5b2cc-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b2cc-151">**\_CollectionReferencePointService MSVM**</span><span class="sxs-lookup"><span data-stu-id="5b2cc-151">**Msvm\_CollectionReferencePointService**</span></span>](msvm-collectionreferencepointservice.md)
</dt> </dl>

 

 




