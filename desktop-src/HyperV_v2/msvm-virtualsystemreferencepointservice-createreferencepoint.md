---
description: Crea un punto di riferimento di un sistema virtuale.
ms.assetid: 9cc7665a-9562-4267-bcd0-3162e426fbad
title: Metodo CreateReferencePoint della classe Msvm_VirtualSystemReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointService.CreateReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 08d28970288ba62346894d758ebac5ac156962ff
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320630"
---
# <a name="createreferencepoint-method-of-the-msvm_virtualsystemreferencepointservice-class"></a><span data-ttu-id="394a1-103">Metodo CreateReferencePoint della classe MSVM \_ VirtualSystemReferencePointService</span><span class="sxs-lookup"><span data-stu-id="394a1-103">CreateReferencePoint method of the Msvm\_VirtualSystemReferencePointService class</span></span>

<span data-ttu-id="394a1-104">Crea un punto di riferimento di un sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="394a1-104">Creates a reference point of a virtual system.</span></span>

## <a name="syntax"></a><span data-ttu-id="394a1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="394a1-105">Syntax</span></span>


```mof
uint32 CreateReferencePoint(
  [in]      Msvm_ComputerSystem              REF AffectedSystem,
  [in]      string                               ReferencePointSettings,
  [in]      uint16                               ReferencePointType,
  [in, out] Msvm_VirtualSystemReferencePoint REF ResultingReferencePoint,
  [out]     CIM_ConcreteJob                  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="394a1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="394a1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="394a1-107">*AffectedSystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="394a1-107">*AffectedSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="394a1-108">Un [**\_ ComputerSystem MSVM**](msvm-computersystem.md) che fa riferimento al sistema virtuale interessato.</span><span class="sxs-lookup"><span data-stu-id="394a1-108">A [**Msvm\_ComputerSystem**](msvm-computersystem.md) that references the affected virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="394a1-109">*ReferencePointSettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="394a1-109">*ReferencePointSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="394a1-110">Contiene le impostazioni dei parametri.</span><span class="sxs-lookup"><span data-stu-id="394a1-110">Contains the parameter settings.</span></span>

</dd> <dt>

<span data-ttu-id="394a1-111">*ReferencePointType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="394a1-111">*ReferencePointType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="394a1-112">Tipo di punto di riferimento richiesto:</span><span class="sxs-lookup"><span data-stu-id="394a1-112">Requested reference point type:</span></span>

<dt>

<span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>

<span data-ttu-id="394a1-113"><span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>**Basato su log** (0)</span><span class="sxs-lookup"><span data-stu-id="394a1-113"><span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>**Log based** (0)</span></span>


</dt> <dd>

<span data-ttu-id="394a1-114">In base al rilevamento del log della replica Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="394a1-114">Based on Hyper-V replica log tracking.</span></span>

</dd> <dt>

<span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>

<span data-ttu-id="394a1-115"><span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>**Basato su RCT** (1)</span><span class="sxs-lookup"><span data-stu-id="394a1-115"><span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>**RCT based** (1)</span></span>


</dt> <dd>

<span data-ttu-id="394a1-116">Basato su Rilevamento modifiche resiliente di dischi virtuali.</span><span class="sxs-lookup"><span data-stu-id="394a1-116">Based on Resilient Change Tracking of virtual disks.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="394a1-117">*ResultingReferencePoint* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="394a1-117">*ResultingReferencePoint* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="394a1-118">Punto di riferimento del sistema virtuale risultante</span><span class="sxs-lookup"><span data-stu-id="394a1-118">Resulting virtual system reference point</span></span>

</dd> <dt>

<span data-ttu-id="394a1-119">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="394a1-119">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="394a1-120">Se l'operazione è a esecuzione prolungata, è possibile che venga restituito un processo.</span><span class="sxs-lookup"><span data-stu-id="394a1-120">If the operation is long running, then optionally a job may be returned.</span></span> <span data-ttu-id="394a1-121">In questo caso, l'istanza della classe [**MSVM \_ VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) che rappresenta il nuovo punto di riferimento del sistema virtuale viene presentata tramite l'associazione [**CIM \_ AffectedJobElement**](cim-affectedjobelement.md) con il valore della proprietà **affected** che fa riferimento alla nuova istanza della classe **MSVM \_ VirtualSystemReferencePoint** che rappresenta il punto di riferimento del sistema virtuale e il valore di **ElementEffects** impostato su 5 (Create).</span><span class="sxs-lookup"><span data-stu-id="394a1-121">In this case, the instance of the [**Msvm\_VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) class representing the new virtual system reference point is presented via the [**CIM\_AffectedJobElement**](cim-affectedjobelement.md) association with the value of the **AffectedElement** property referring to the new instance of the **Msvm\_VirtualSystemReferencePoint** class representing the virtual system reference point and the value of the **ElementEffects** set to 5 (Create).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="394a1-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="394a1-122">Return value</span></span>

<span data-ttu-id="394a1-123">In caso di esito positivo, restituisce 0; in caso contrario, restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="394a1-123">On success, returns 0; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="394a1-124">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="394a1-124">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="394a1-125">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="394a1-125">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="394a1-126">**Non riuscito** (2)</span><span class="sxs-lookup"><span data-stu-id="394a1-126">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="394a1-127">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="394a1-127">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="394a1-128">**Parametro non valido** (4)</span><span class="sxs-lookup"><span data-stu-id="394a1-128">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="394a1-129">**Stato non valido** (5)</span><span class="sxs-lookup"><span data-stu-id="394a1-129">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="394a1-130">**Tipo non valido** (6)</span><span class="sxs-lookup"><span data-stu-id="394a1-130">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="394a1-131">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="394a1-131">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="394a1-132">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="394a1-132">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="394a1-133">**Metodo riservato** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="394a1-133">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="394a1-134">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="394a1-134">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="394a1-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="394a1-135">Requirements</span></span>



| <span data-ttu-id="394a1-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="394a1-136">Requirement</span></span> | <span data-ttu-id="394a1-137">Valore</span><span class="sxs-lookup"><span data-stu-id="394a1-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="394a1-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="394a1-138">Minimum supported client</span></span><br/> | <span data-ttu-id="394a1-139">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="394a1-139">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="394a1-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="394a1-140">Minimum supported server</span></span><br/> | <span data-ttu-id="394a1-141">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="394a1-141">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="394a1-142">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="394a1-142">Namespace</span></span><br/>                | <span data-ttu-id="394a1-143">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="394a1-143">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="394a1-144">MOF</span><span class="sxs-lookup"><span data-stu-id="394a1-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="394a1-145"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="394a1-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="394a1-146">DLL</span><span class="sxs-lookup"><span data-stu-id="394a1-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="394a1-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="394a1-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="394a1-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="394a1-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="394a1-149">**\_VirtualSystemReferencePointService MSVM**</span><span class="sxs-lookup"><span data-stu-id="394a1-149">**Msvm\_VirtualSystemReferencePointService**</span></span>](msvm-virtualsystemreferencepointservice.md)
</dt> </dl>

 

 




