---
description: Richiede che lo stato del processo venga modificato in un valore specificato nel parametro RequestedState. Richiamando il metodo RequestStateChange più volte, le richieste precedenti potrebbero essere sovrascritte o perse.
ms.assetid: 64a9d63e-8af4-4ab1-8343-9a0418b951e2
title: Metodo RequestStateChange della classe CIM_ConcreteJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ConcreteJob.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 6e3efcea0f7ed7d6ecbfef7b543a0e82d90a15b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344131"
---
# <a name="requeststatechange-method-of-the-cim_concretejob-class"></a><span data-ttu-id="b9aad-104">Metodo RequestStateChange della classe CIM \_ ConcreteJob</span><span class="sxs-lookup"><span data-stu-id="b9aad-104">RequestStateChange method of the CIM\_ConcreteJob class</span></span>

<span data-ttu-id="b9aad-105">Richiede che lo stato del processo venga modificato in un valore specificato nel parametro RequestedState.</span><span class="sxs-lookup"><span data-stu-id="b9aad-105">Requests that the state of the job be changed to the value specified in the RequestedState parameter.</span></span> <span data-ttu-id="b9aad-106">Richiamando il metodo RequestStateChange più volte, le richieste precedenti potrebbero essere sovrascritte o perse.</span><span class="sxs-lookup"><span data-stu-id="b9aad-106">Invoking the RequestStateChange method multiple times could result in earlier requests being overwritten or lost.</span></span>

<span data-ttu-id="b9aad-107">Se viene restituito 0, l'attività è stata completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="b9aad-107">If 0 is returned, then the task completed successfully.</span></span> <span data-ttu-id="b9aad-108">Qualsiasi altro codice restituito indica una condizione di errore.</span><span class="sxs-lookup"><span data-stu-id="b9aad-108">Any other return code indicates an error condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9aad-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b9aad-109">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in] uint16   RequestedState,
  [in] datetime TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="b9aad-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="b9aad-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9aad-111">*RequestedState* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b9aad-111">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9aad-112">Stato da richiedere per un processo.</span><span class="sxs-lookup"><span data-stu-id="b9aad-112">The state to request for a job.</span></span> <span data-ttu-id="b9aad-113">I valori possibili sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="b9aad-113">The possible values are as follows:</span></span>

<dt>

<span id="Start"></span><span id="start"></span><span id="START"></span>

<span data-ttu-id="b9aad-114"><span id="Start"></span><span id="start"></span><span id="START"></span>**Avvio** (2)</span><span class="sxs-lookup"><span data-stu-id="b9aad-114"><span id="Start"></span><span id="start"></span><span id="START"></span>**Start** (2)</span></span>


</dt> <dd>

<span data-ttu-id="b9aad-115">Imposta lo stato su "Running".</span><span class="sxs-lookup"><span data-stu-id="b9aad-115">Changes the state to 'Running'.</span></span>

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span data-ttu-id="b9aad-116"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Sospendi** (3)</span><span class="sxs-lookup"><span data-stu-id="b9aad-116"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspend** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b9aad-117">Arresta temporaneamente il processo.</span><span class="sxs-lookup"><span data-stu-id="b9aad-117">Stops the job temporarily.</span></span> <span data-ttu-id="b9aad-118">L'intenzione è di riavviare successivamente il processo con "Start".</span><span class="sxs-lookup"><span data-stu-id="b9aad-118">The intention is to subsequently restart the job with 'Start'.</span></span> <span data-ttu-id="b9aad-119">Potrebbe essere possibile immettere lo stato del servizio mentre è sospeso.</span><span class="sxs-lookup"><span data-stu-id="b9aad-119">It might be possible to enter the 'Service' state while suspended.</span></span> <span data-ttu-id="b9aad-120">(Si tratta di un processo specifico).</span><span class="sxs-lookup"><span data-stu-id="b9aad-120">(This is job-specific.)</span></span>

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span data-ttu-id="b9aad-121"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Termina** (4)</span><span class="sxs-lookup"><span data-stu-id="b9aad-121"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (4)</span></span>


</dt> <dd>

<span data-ttu-id="b9aad-122">Arresta il processo in modo pulito, Salva i dati, conserva lo stato e arresta tutti i processi sottostanti in modo ordinato.</span><span class="sxs-lookup"><span data-stu-id="b9aad-122">Stops the job cleanly, saves data, preserves the state, and shuts down all underlying processes in an orderly manner.</span></span>

</dd> <dt>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>

<span data-ttu-id="b9aad-123"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span><span class="sxs-lookup"><span data-stu-id="b9aad-123"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span></span>


</dt> <dd>

<span data-ttu-id="b9aad-124">Termina immediatamente il processo senza alcuna necessità di salvare i dati o mantenere lo stato.</span><span class="sxs-lookup"><span data-stu-id="b9aad-124">Terminates the job immediately with no requirement to save data or preserve the state.</span></span>

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="b9aad-125"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Servizio** (6)</span><span class="sxs-lookup"><span data-stu-id="b9aad-125"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (6)</span></span>


</dt> <dd>

<span data-ttu-id="b9aad-126">Inserisce il processo in uno stato del servizio specifico del fornitore.</span><span class="sxs-lookup"><span data-stu-id="b9aad-126">Puts the job into a vendor-specific service state.</span></span> <span data-ttu-id="b9aad-127">Potrebbe essere possibile riavviare il processo.</span><span class="sxs-lookup"><span data-stu-id="b9aad-127">It might be possible to restart the job.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="b9aad-128"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (7.. 32767)</span><span class="sxs-lookup"><span data-stu-id="b9aad-128"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (7..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="b9aad-129"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornitore riservato** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="b9aad-129"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="b9aad-130">*TimeoutPeriod* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b9aad-130">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9aad-131">Periodo di timeout che specifica la quantità massima di tempo per cui il client prevede che la transizione al nuovo stato venga eseguita.</span><span class="sxs-lookup"><span data-stu-id="b9aad-131">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="b9aad-132">Per specificare il periodo di timeout, è necessario utilizzare il formato intervallo.</span><span class="sxs-lookup"><span data-stu-id="b9aad-132">The interval format must be used to specify the timeout period.</span></span> <span data-ttu-id="b9aad-133">Il valore 0 o **null** indica che il client non dispone di requisiti temporali per la transizione.</span><span class="sxs-lookup"><span data-stu-id="b9aad-133">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="b9aad-134">Se questa proprietà non contiene 0 o **null** e l'implementazione non supporta questo parametro, deve essere restituito un codice restituito 4098 (**utilizzo del parametro timeout non supportato**).</span><span class="sxs-lookup"><span data-stu-id="b9aad-134">If this property does not contain 0 or **Null** and the implementation does not support this parameter, a return code of 4098 (**Use Of Timeout Parameter Not Supported**) must be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9aad-135">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b9aad-135">Return value</span></span>

<span data-ttu-id="b9aad-136">Restituisce 0 in caso di esito positivo; in caso contrario, restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="b9aad-136">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="b9aad-137">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="b9aad-137">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b9aad-138">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="b9aad-138">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="b9aad-139">**Errore sconosciuto/non specificato** (2)</span><span class="sxs-lookup"><span data-stu-id="b9aad-139">**Unknown/Unspecified Error** (2)</span></span>
</dt> <dt>

<span data-ttu-id="b9aad-140">**Non può essere completato entro il periodo di timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="b9aad-140">**Can NOT complete within Timeout Period** (3)</span></span>
</dt> <dt>

<span data-ttu-id="b9aad-141">**Non riuscito** (4)</span><span class="sxs-lookup"><span data-stu-id="b9aad-141">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="b9aad-142">**Parametro non valido** (5)</span><span class="sxs-lookup"><span data-stu-id="b9aad-142">**Invalid Parameter** (5)</span></span>
</dt> <dt>

<span data-ttu-id="b9aad-143">**In uso** (6)</span><span class="sxs-lookup"><span data-stu-id="b9aad-143">**In Use** (6)</span></span>
</dt> <dt>

<span data-ttu-id="b9aad-144">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="b9aad-144">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="b9aad-145">**Parametri del metodo controllati-transizione avviata** (4096)</span><span class="sxs-lookup"><span data-stu-id="b9aad-145">**Method Parameters Checked - Transition Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="b9aad-146">**Transizione di stato non valida** (4097)</span><span class="sxs-lookup"><span data-stu-id="b9aad-146">**Invalid State Transition** (4097)</span></span>
</dt> <dt>

<span data-ttu-id="b9aad-147">**Utilizzo del parametro timeout non supportato** (4098)</span><span class="sxs-lookup"><span data-stu-id="b9aad-147">**Use of Timeout Parameter Not Supported** (4098)</span></span>
</dt> <dt>

<span data-ttu-id="b9aad-148">**Occupato** (4099)</span><span class="sxs-lookup"><span data-stu-id="b9aad-148">**Busy** (4099)</span></span>
</dt> <dt>

<span data-ttu-id="b9aad-149">**Metodo riservato** (4100.. 32767)</span><span class="sxs-lookup"><span data-stu-id="b9aad-149">**Method Reserved** (4100..32767)</span></span>
</dt> <dt>

<span data-ttu-id="b9aad-150">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="b9aad-150">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="b9aad-151">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b9aad-151">Requirements</span></span>



| <span data-ttu-id="b9aad-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9aad-152">Requirement</span></span> | <span data-ttu-id="b9aad-153">Valore</span><span class="sxs-lookup"><span data-stu-id="b9aad-153">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9aad-154">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b9aad-154">Minimum supported client</span></span><br/> | <span data-ttu-id="b9aad-155">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="b9aad-155">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="b9aad-156">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b9aad-156">Minimum supported server</span></span><br/> | <span data-ttu-id="b9aad-157">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="b9aad-157">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="b9aad-158">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b9aad-158">Namespace</span></span><br/>                | <span data-ttu-id="b9aad-159">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="b9aad-159">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b9aad-160">MOF</span><span class="sxs-lookup"><span data-stu-id="b9aad-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b9aad-161"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b9aad-161"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b9aad-162">DLL</span><span class="sxs-lookup"><span data-stu-id="b9aad-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b9aad-163"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b9aad-163"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b9aad-164">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b9aad-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9aad-165">**\_CONCRETEJOB CIM**</span><span class="sxs-lookup"><span data-stu-id="b9aad-165">**CIM\_ConcreteJob**</span></span>](cim-concretejob.md)
</dt> </dl>

 

 




