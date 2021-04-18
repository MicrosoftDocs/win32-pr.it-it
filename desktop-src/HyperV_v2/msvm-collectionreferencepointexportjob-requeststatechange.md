---
description: Richiede una modifica dello stato.
ms.assetid: 34d70ff2-4545-4ab7-8c84-6532c342768b
title: Metodo RequestStateChange della classe Msvm_CollectionReferencePointExportJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointExportJob.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: a3e8b3f3a7249896f023734d049fa3fa772514f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317198"
---
# <a name="requeststatechange-method-of-the-msvm_collectionreferencepointexportjob-class"></a><span data-ttu-id="e0401-103">Metodo RequestStateChange della classe MSVM \_ CollectionReferencePointExportJob</span><span class="sxs-lookup"><span data-stu-id="e0401-103">RequestStateChange method of the Msvm\_CollectionReferencePointExportJob class</span></span>

<span data-ttu-id="e0401-104">Richiede una modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="e0401-104">Requests a state change.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0401-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e0401-105">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in] uint16   RequestedState,
  [in] datetime TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="e0401-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e0401-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0401-107">*RequestedState* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e0401-107">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0401-108">RequestStateChange modifica lo stato di un processo.</span><span class="sxs-lookup"><span data-stu-id="e0401-108">RequestStateChange changes the state of a job.</span></span> <span data-ttu-id="e0401-109">I valori possibili sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="e0401-109">The possible values are as follows:</span></span>

<dt>

<span id="Start"></span><span id="start"></span><span id="START"></span>

<span data-ttu-id="e0401-110"><span id="Start"></span><span id="start"></span><span id="START"></span>**Avvio** (2)</span><span class="sxs-lookup"><span data-stu-id="e0401-110"><span id="Start"></span><span id="start"></span><span id="START"></span>**Start** (2)</span></span>


</dt> <dd>

<span data-ttu-id="e0401-111">Imposta lo stato su "Running".</span><span class="sxs-lookup"><span data-stu-id="e0401-111">Changes the state to 'Running'.</span></span>

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span data-ttu-id="e0401-112"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Sospendi** (3)</span><span class="sxs-lookup"><span data-stu-id="e0401-112"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspend** (3)</span></span>


</dt> <dd>

<span data-ttu-id="e0401-113">Arresta temporaneamente il processo.</span><span class="sxs-lookup"><span data-stu-id="e0401-113">Stops the job temporarily.</span></span> <span data-ttu-id="e0401-114">L'intenzione è di riavviare successivamente il processo con "Start".</span><span class="sxs-lookup"><span data-stu-id="e0401-114">The intention is to subsequently restart the job with 'Start'.</span></span> <span data-ttu-id="e0401-115">Potrebbe essere possibile immettere lo stato del servizio mentre è sospeso.</span><span class="sxs-lookup"><span data-stu-id="e0401-115">It might be possible to enter the 'Service' state while suspended.</span></span> <span data-ttu-id="e0401-116">(Si tratta di un processo specifico).</span><span class="sxs-lookup"><span data-stu-id="e0401-116">(This is job-specific.)</span></span>

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span data-ttu-id="e0401-117"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Termina** (4)</span><span class="sxs-lookup"><span data-stu-id="e0401-117"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (4)</span></span>


</dt> <dd>

<span data-ttu-id="e0401-118">Arresta il processo in modo pulito, Salva i dati, conserva lo stato e arresta tutti i processi sottostanti in modo ordinato.</span><span class="sxs-lookup"><span data-stu-id="e0401-118">Stops the job cleanly, saves data, preserves the state, and shuts down all underlying processes in an orderly manner.</span></span>

</dd> <dt>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>

<span data-ttu-id="e0401-119"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span><span class="sxs-lookup"><span data-stu-id="e0401-119"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span></span>


</dt> <dd>

<span data-ttu-id="e0401-120">Termina immediatamente il processo senza alcuna necessità di salvare i dati o mantenere lo stato.</span><span class="sxs-lookup"><span data-stu-id="e0401-120">Terminates the job immediately with no requirement to save data or preserve the state.</span></span>

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="e0401-121"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Servizio** (6)</span><span class="sxs-lookup"><span data-stu-id="e0401-121"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (6)</span></span>


</dt> <dd>

<span data-ttu-id="e0401-122">Inserisce il processo in uno stato del servizio specifico del fornitore.</span><span class="sxs-lookup"><span data-stu-id="e0401-122">Puts the job into a vendor-specific service state.</span></span> <span data-ttu-id="e0401-123">Potrebbe essere possibile riavviare il processo.</span><span class="sxs-lookup"><span data-stu-id="e0401-123">It might be possible to restart the job.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="e0401-124"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (7.. 32767)</span><span class="sxs-lookup"><span data-stu-id="e0401-124"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (7..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="e0401-125"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornitore riservato** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="e0401-125"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="e0401-126">*TimeoutPeriod* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e0401-126">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0401-127">Periodo di timeout che specifica la quantità massima di tempo per cui il client prevede che la transizione al nuovo stato venga eseguita.</span><span class="sxs-lookup"><span data-stu-id="e0401-127">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="e0401-128">Per specificare il periodo di timeout, è necessario utilizzare il formato intervallo.</span><span class="sxs-lookup"><span data-stu-id="e0401-128">The interval format must be used to specify the timeout period.</span></span> <span data-ttu-id="e0401-129">Il valore 0 o **null** indica che il client non dispone di requisiti temporali per la transizione.</span><span class="sxs-lookup"><span data-stu-id="e0401-129">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="e0401-130">Se questa proprietà non contiene 0 o **null** e l'implementazione non supporta questo parametro, deve essere restituito un codice restituito 4098 (**utilizzo del parametro timeout non supportato**).</span><span class="sxs-lookup"><span data-stu-id="e0401-130">If this property does not contain 0 or **Null** and the implementation does not support this parameter, a return code of 4098 (**Use Of Timeout Parameter Not Supported**) must be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0401-131">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e0401-131">Return value</span></span>

<span data-ttu-id="e0401-132">Restituisce 0 in caso di esito positivo; in caso contrario, restituisce uno dei seguenti errori.</span><span class="sxs-lookup"><span data-stu-id="e0401-132">Returns 0 on success; otherwise, returns one of the following errors.</span></span>

<dl> <dt>

 <span data-ttu-id="e0401-133"> (0)</span><span class="sxs-lookup"><span data-stu-id="e0401-133">(0)</span></span>
</dt> <dt>

 <span data-ttu-id="e0401-134">(32768)</span><span class="sxs-lookup"><span data-stu-id="e0401-134">(32768)</span></span>
</dt> <dt>

 <span data-ttu-id="e0401-135">(32769)</span><span class="sxs-lookup"><span data-stu-id="e0401-135">(32769)</span></span>
</dt> <dt>

 <span data-ttu-id="e0401-136">(32770)</span><span class="sxs-lookup"><span data-stu-id="e0401-136">(32770)</span></span>
</dt> <dt>

 <span data-ttu-id="e0401-137">(32771)</span><span class="sxs-lookup"><span data-stu-id="e0401-137">(32771)</span></span>
</dt> <dt>

 <span data-ttu-id="e0401-138">(32772)</span><span class="sxs-lookup"><span data-stu-id="e0401-138">(32772)</span></span>
</dt> <dt>

 <span data-ttu-id="e0401-139">(32773)</span><span class="sxs-lookup"><span data-stu-id="e0401-139">(32773)</span></span>
</dt> <dt>

 <span data-ttu-id="e0401-140">(32774)</span><span class="sxs-lookup"><span data-stu-id="e0401-140">(32774)</span></span>
</dt> <dt>

 <span data-ttu-id="e0401-141">(32775)</span><span class="sxs-lookup"><span data-stu-id="e0401-141">(32775)</span></span>
</dt> <dt>

 <span data-ttu-id="e0401-142">(32776)</span><span class="sxs-lookup"><span data-stu-id="e0401-142">(32776)</span></span>
</dt> <dt>

 <span data-ttu-id="e0401-143">(32777)</span><span class="sxs-lookup"><span data-stu-id="e0401-143">(32777)</span></span>
</dt> <dt>

 <span data-ttu-id="e0401-144">(32778)</span><span class="sxs-lookup"><span data-stu-id="e0401-144">(32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="e0401-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e0401-145">Requirements</span></span>



| <span data-ttu-id="e0401-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0401-146">Requirement</span></span> | <span data-ttu-id="e0401-147">Valore</span><span class="sxs-lookup"><span data-stu-id="e0401-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0401-148">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e0401-148">Minimum supported client</span></span><br/> | <span data-ttu-id="e0401-149">Solo app desktop Windows 10 versione 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="e0401-149">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="e0401-150">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e0401-150">Minimum supported server</span></span><br/> | <span data-ttu-id="e0401-151">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="e0401-151">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="e0401-152">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e0401-152">Namespace</span></span><br/>                | <span data-ttu-id="e0401-153">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="e0401-153">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e0401-154">MOF</span><span class="sxs-lookup"><span data-stu-id="e0401-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e0401-155"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e0401-155"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e0401-156">DLL</span><span class="sxs-lookup"><span data-stu-id="e0401-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e0401-157"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e0401-157"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e0401-158">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e0401-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0401-159">**\_CollectionReferencePointExportJob MSVM**</span><span class="sxs-lookup"><span data-stu-id="e0401-159">**Msvm\_CollectionReferencePointExportJob**</span></span>](msvm-collectionreferencepointexportjob.md)
</dt> </dl>

 

 




