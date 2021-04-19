---
description: Richiede che lo stato del processo di migrazione venga modificato nello stato specificato.
ms.assetid: f0be5ea8-7e21-407e-b84d-8bd4ca5a6a2c
title: Metodo RequestStateChange della classe Msvm_MigrationJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MigrationJob.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 31011de619780ae36f390ee87038300a3b42fef2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311776"
---
# <a name="requeststatechange-method-of-the-msvm_migrationjob-class"></a><span data-ttu-id="3004c-103">Metodo RequestStateChange della classe MSVM \_ MigrationJob</span><span class="sxs-lookup"><span data-stu-id="3004c-103">RequestStateChange method of the Msvm\_MigrationJob class</span></span>

<span data-ttu-id="3004c-104">Richiede che lo stato del processo di migrazione venga modificato nello stato specificato.</span><span class="sxs-lookup"><span data-stu-id="3004c-104">Requests that the state of the migration job be changed to the specified state.</span></span> <span data-ttu-id="3004c-105">Richiamando il metodo **RequestStateChange** più volte è possibile che le richieste precedenti vengano sovrascritte o perse.</span><span class="sxs-lookup"><span data-stu-id="3004c-105">Invoking the **RequestStateChange** method multiple times can result in earlier requests being overwritten or lost.</span></span> <span data-ttu-id="3004c-106">Se viene restituito 0, l'attività è stata completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="3004c-106">If 0 is returned, then the task completed successfully.</span></span> <span data-ttu-id="3004c-107">Qualsiasi altro codice restituito indica una condizione di errore.</span><span class="sxs-lookup"><span data-stu-id="3004c-107">Any other return code indicates an error condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="3004c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3004c-108">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in] uint16   RequestedState,
  [in] datetime TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="3004c-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="3004c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3004c-110">*RequestedState* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3004c-110">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3004c-111">Nuovo stato di un processo.</span><span class="sxs-lookup"><span data-stu-id="3004c-111">The new state of a job.</span></span>

<dt>

<span id="Start"></span><span id="start"></span><span id="START"></span>

<span data-ttu-id="3004c-112"><span id="Start"></span><span id="start"></span><span id="START"></span>**Avvio** (2)</span><span class="sxs-lookup"><span data-stu-id="3004c-112"><span id="Start"></span><span id="start"></span><span id="START"></span>**Start** (2)</span></span>


</dt> <dd>

<span data-ttu-id="3004c-113">Imposta lo stato su "Running".</span><span class="sxs-lookup"><span data-stu-id="3004c-113">Changes the state to "Running".</span></span>

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span data-ttu-id="3004c-114"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Sospendi** (3)</span><span class="sxs-lookup"><span data-stu-id="3004c-114"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspend** (3)</span></span>


</dt> <dd>

<span data-ttu-id="3004c-115">Arresta temporaneamente il processo.</span><span class="sxs-lookup"><span data-stu-id="3004c-115">Stops the job temporarily.</span></span> <span data-ttu-id="3004c-116">Lo scopo è quello di riavviare successivamente il processo con "Start".</span><span class="sxs-lookup"><span data-stu-id="3004c-116">The intention is to subsequently restart the job with "Start".</span></span> <span data-ttu-id="3004c-117">Potrebbe essere possibile immettere lo stato "servizio" mentre è sospeso.</span><span class="sxs-lookup"><span data-stu-id="3004c-117">It might be possible to enter the "Service" state while suspended.</span></span> <span data-ttu-id="3004c-118">(Si tratta di un processo specifico).</span><span class="sxs-lookup"><span data-stu-id="3004c-118">(This is job specific.)</span></span>

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span data-ttu-id="3004c-119"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Termina** (4)</span><span class="sxs-lookup"><span data-stu-id="3004c-119"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (4)</span></span>


</dt> <dd>

<span data-ttu-id="3004c-120">Arresta il processo in modo corretto, salvando i dati, mantenendo lo stato e chiudendo tutti i processi sottostanti in modo ordinato.</span><span class="sxs-lookup"><span data-stu-id="3004c-120">Stops the job cleanly, saving data, preserving the state, and shutting down all underlying processes in an orderly manner.</span></span>

</dd> <dt>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>

<span data-ttu-id="3004c-121"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span><span class="sxs-lookup"><span data-stu-id="3004c-121"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span></span>


</dt> <dd>

<span data-ttu-id="3004c-122">Termina immediatamente il processo senza alcuna necessità di salvare i dati o mantenere lo stato.</span><span class="sxs-lookup"><span data-stu-id="3004c-122">Terminates the job immediately with no requirement to save data or preserve the state.</span></span>

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="3004c-123"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Servizio** (6)</span><span class="sxs-lookup"><span data-stu-id="3004c-123"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (6)</span></span>


</dt> <dd>

<span data-ttu-id="3004c-124">Inserisce il processo in uno stato del servizio specifico del fornitore.</span><span class="sxs-lookup"><span data-stu-id="3004c-124">Puts the job into a vendor-specific service state.</span></span> <span data-ttu-id="3004c-125">Potrebbe essere possibile riavviare il processo.</span><span class="sxs-lookup"><span data-stu-id="3004c-125">It might be possible to restart the job.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="3004c-126"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato**</span><span class="sxs-lookup"><span data-stu-id="3004c-126"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved**</span></span>


</dt> <dd>

<span data-ttu-id="3004c-127">Riservato.</span><span class="sxs-lookup"><span data-stu-id="3004c-127">Reserved.</span></span>

</dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="3004c-128"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornitore riservato**</span><span class="sxs-lookup"><span data-stu-id="3004c-128"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved**</span></span>


</dt> <dd>

<span data-ttu-id="3004c-129">Riservato.</span><span class="sxs-lookup"><span data-stu-id="3004c-129">Reserved.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="3004c-130">*TimeoutPeriod* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3004c-130">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3004c-131">Periodo di timeout che specifica la quantità massima di tempo per cui il client prevede che la transizione al nuovo stato venga eseguita.</span><span class="sxs-lookup"><span data-stu-id="3004c-131">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="3004c-132">Per specificare il periodo di timeout, è necessario utilizzare il formato intervallo.</span><span class="sxs-lookup"><span data-stu-id="3004c-132">The interval format must be used to specify the timeout period.</span></span> <span data-ttu-id="3004c-133">Il valore 0 o **null** indica che il client non dispone di requisiti temporali per la transizione.</span><span class="sxs-lookup"><span data-stu-id="3004c-133">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="3004c-134">Se questa proprietà non contiene 0 o **null** e l'implementazione non supporta questo parametro, deve essere restituito un codice restituito 4098 (utilizzo del parametro timeout non supportato).</span><span class="sxs-lookup"><span data-stu-id="3004c-134">If this property does not contain 0 or **Null** and the implementation does not support this parameter, a return code of 4098 (Use Of Timeout Parameter Not Supported) must be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3004c-135">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3004c-135">Return value</span></span>

<dl> <dt>

 <span data-ttu-id="3004c-136"> (0)</span><span class="sxs-lookup"><span data-stu-id="3004c-136">(0)</span></span>
</dt> <dt>

 <span data-ttu-id="3004c-137">(32768)</span><span class="sxs-lookup"><span data-stu-id="3004c-137">(32768)</span></span>
</dt> <dt>

 <span data-ttu-id="3004c-138">(32769)</span><span class="sxs-lookup"><span data-stu-id="3004c-138">(32769)</span></span>
</dt> <dt>

 <span data-ttu-id="3004c-139">(32770)</span><span class="sxs-lookup"><span data-stu-id="3004c-139">(32770)</span></span>
</dt> <dt>

 <span data-ttu-id="3004c-140">(32771)</span><span class="sxs-lookup"><span data-stu-id="3004c-140">(32771)</span></span>
</dt> <dt>

 <span data-ttu-id="3004c-141">(32772)</span><span class="sxs-lookup"><span data-stu-id="3004c-141">(32772)</span></span>
</dt> <dt>

 <span data-ttu-id="3004c-142">(32773)</span><span class="sxs-lookup"><span data-stu-id="3004c-142">(32773)</span></span>
</dt> <dt>

 <span data-ttu-id="3004c-143">(32774)</span><span class="sxs-lookup"><span data-stu-id="3004c-143">(32774)</span></span>
</dt> <dt>

 <span data-ttu-id="3004c-144">(32775)</span><span class="sxs-lookup"><span data-stu-id="3004c-144">(32775)</span></span>
</dt> <dt>

 <span data-ttu-id="3004c-145">(32776)</span><span class="sxs-lookup"><span data-stu-id="3004c-145">(32776)</span></span>
</dt> <dt>

 <span data-ttu-id="3004c-146">(32777)</span><span class="sxs-lookup"><span data-stu-id="3004c-146">(32777)</span></span>
</dt> <dt>

 <span data-ttu-id="3004c-147">(32778)</span><span class="sxs-lookup"><span data-stu-id="3004c-147">(32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="3004c-148">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3004c-148">Requirements</span></span>



| <span data-ttu-id="3004c-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="3004c-149">Requirement</span></span> | <span data-ttu-id="3004c-150">Valore</span><span class="sxs-lookup"><span data-stu-id="3004c-150">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3004c-151">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3004c-151">Minimum supported client</span></span><br/> | <span data-ttu-id="3004c-152">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="3004c-152">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3004c-153">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3004c-153">Minimum supported server</span></span><br/> | <span data-ttu-id="3004c-154">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="3004c-154">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3004c-155">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3004c-155">Namespace</span></span><br/>                | <span data-ttu-id="3004c-156">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="3004c-156">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3004c-157">MOF</span><span class="sxs-lookup"><span data-stu-id="3004c-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3004c-158"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3004c-158"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3004c-159">DLL</span><span class="sxs-lookup"><span data-stu-id="3004c-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3004c-160"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3004c-160"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3004c-161">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3004c-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3004c-162">**\_MigrationJob MSVM**</span><span class="sxs-lookup"><span data-stu-id="3004c-162">**Msvm\_MigrationJob**</span></span>](msvm-migrationjob.md)
</dt> </dl>

 

 




