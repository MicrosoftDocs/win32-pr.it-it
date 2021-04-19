---
description: Richiede che lo stato del processo venga modificato nello stato specificato.
ms.assetid: 5D7D7D20-4BB9-4375-BBBF-7AA64FEE6D13
title: Metodo RequestStateChange della classe Msvm_ConcreteJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ConcreteJob.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 0e7abf5f4bf78ac469e528ab72bb5786130e9cf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314322"
---
# <a name="requeststatechange-method-of-the-msvm_concretejob-class"></a><span data-ttu-id="6b8a5-103">Metodo RequestStateChange della classe MSVM \_ ConcreteJob</span><span class="sxs-lookup"><span data-stu-id="6b8a5-103">RequestStateChange method of the Msvm\_ConcreteJob class</span></span>

<span data-ttu-id="6b8a5-104">Richiede che lo stato del processo venga modificato nello stato specificato.</span><span class="sxs-lookup"><span data-stu-id="6b8a5-104">Requests that the state of the job be changed to the specified state.</span></span> <span data-ttu-id="6b8a5-105">Richiamando il metodo **RequestStateChange** più volte è possibile che le richieste precedenti vengano sovrascritte o perse.</span><span class="sxs-lookup"><span data-stu-id="6b8a5-105">Invoking the **RequestStateChange** method multiple times can result in earlier requests being overwritten or lost.</span></span> <span data-ttu-id="6b8a5-106">Se viene restituito 0, l'attività è stata completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="6b8a5-106">If 0 is returned, then the task completed successfully.</span></span> <span data-ttu-id="6b8a5-107">Qualsiasi altro codice restituito indica una condizione di errore.</span><span class="sxs-lookup"><span data-stu-id="6b8a5-107">Any other return code indicates an error condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b8a5-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6b8a5-108">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in] uint16   RequestedState,
  [in] datetime TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="6b8a5-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="6b8a5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b8a5-110">*RequestedState* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6b8a5-110">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b8a5-111">Tipo: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6b8a5-111">Type: **uint16**</span></span>

<span data-ttu-id="6b8a5-112">Nuovo stato di un processo.</span><span class="sxs-lookup"><span data-stu-id="6b8a5-112">The new state of a job.</span></span>

<dt>

<span id="Start"></span><span id="start"></span><span id="START"></span>

<span data-ttu-id="6b8a5-113"><span id="Start"></span><span id="start"></span><span id="START"></span>**Avvio** (2)</span><span class="sxs-lookup"><span data-stu-id="6b8a5-113"><span id="Start"></span><span id="start"></span><span id="START"></span>**Start** (2)</span></span>


</dt> <dd>

<span data-ttu-id="6b8a5-114">Imposta lo stato su "Running".</span><span class="sxs-lookup"><span data-stu-id="6b8a5-114">Changes the state to "Running".</span></span>

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span data-ttu-id="6b8a5-115"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Sospendi** (3)</span><span class="sxs-lookup"><span data-stu-id="6b8a5-115"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspend** (3)</span></span>


</dt> <dd>

<span data-ttu-id="6b8a5-116">Arresta temporaneamente il processo.</span><span class="sxs-lookup"><span data-stu-id="6b8a5-116">Stops the job temporarily.</span></span> <span data-ttu-id="6b8a5-117">Lo scopo è quello di riavviare successivamente il processo con "Start".</span><span class="sxs-lookup"><span data-stu-id="6b8a5-117">The intention is to subsequently restart the job with "Start".</span></span> <span data-ttu-id="6b8a5-118">Potrebbe essere possibile immettere lo stato "servizio" mentre è sospeso.</span><span class="sxs-lookup"><span data-stu-id="6b8a5-118">It might be possible to enter the "Service" state while suspended.</span></span> <span data-ttu-id="6b8a5-119">(Si tratta di un processo specifico).</span><span class="sxs-lookup"><span data-stu-id="6b8a5-119">(This is job specific.)</span></span>

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span data-ttu-id="6b8a5-120"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Termina** (4)</span><span class="sxs-lookup"><span data-stu-id="6b8a5-120"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (4)</span></span>


</dt> <dd>

<span data-ttu-id="6b8a5-121">Arresta il processo in modo corretto, salvando i dati, mantenendo lo stato e chiudendo tutti i processi sottostanti in modo ordinato.</span><span class="sxs-lookup"><span data-stu-id="6b8a5-121">Stops the job cleanly, saving data, preserving the state, and shutting down all underlying processes in an orderly manner.</span></span>

</dd> <dt>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>

<span data-ttu-id="6b8a5-122"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span><span class="sxs-lookup"><span data-stu-id="6b8a5-122"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span></span>


</dt> <dd>

<span data-ttu-id="6b8a5-123">Termina immediatamente il processo senza alcuna necessità di salvare i dati o mantenere lo stato.</span><span class="sxs-lookup"><span data-stu-id="6b8a5-123">Terminates the job immediately with no requirement to save data or preserve the state.</span></span>

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="6b8a5-124"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Servizio** (6)</span><span class="sxs-lookup"><span data-stu-id="6b8a5-124"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (6)</span></span>


</dt> <dd>

<span data-ttu-id="6b8a5-125">Inserisce il processo in uno stato del servizio specifico del fornitore.</span><span class="sxs-lookup"><span data-stu-id="6b8a5-125">Puts the job into a vendor-specific service state.</span></span> <span data-ttu-id="6b8a5-126">Potrebbe essere possibile riavviare il processo.</span><span class="sxs-lookup"><span data-stu-id="6b8a5-126">It might be possible to restart the job.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="6b8a5-127"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato**</span><span class="sxs-lookup"><span data-stu-id="6b8a5-127"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved**</span></span>


</dt> <dd>

<span data-ttu-id="6b8a5-128">Riservato.</span><span class="sxs-lookup"><span data-stu-id="6b8a5-128">Reserved.</span></span>

</dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="6b8a5-129"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornitore riservato**</span><span class="sxs-lookup"><span data-stu-id="6b8a5-129"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved**</span></span>


</dt> <dd>

<span data-ttu-id="6b8a5-130">Riservato.</span><span class="sxs-lookup"><span data-stu-id="6b8a5-130">Reserved.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="6b8a5-131">*TimeoutPeriod* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6b8a5-131">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b8a5-132">Tipo: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6b8a5-132">Type: **datetime**</span></span>

<span data-ttu-id="6b8a5-133">Periodo di timeout che specifica la quantità massima di tempo per cui il client prevede che la transizione al nuovo stato venga eseguita.</span><span class="sxs-lookup"><span data-stu-id="6b8a5-133">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="6b8a5-134">Per specificare il periodo di timeout, è necessario utilizzare il formato intervallo.</span><span class="sxs-lookup"><span data-stu-id="6b8a5-134">The interval format must be used to specify the timeout period.</span></span> <span data-ttu-id="6b8a5-135">Il valore 0 o **null** indica che il client non dispone di requisiti temporali per la transizione.</span><span class="sxs-lookup"><span data-stu-id="6b8a5-135">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="6b8a5-136">Se questa proprietà non contiene 0 o **null** e l'implementazione non supporta questo parametro, deve essere restituito un codice restituito 4098 (utilizzo del parametro timeout non supportato).</span><span class="sxs-lookup"><span data-stu-id="6b8a5-136">If this property does not contain 0 or **Null** and the implementation does not support this parameter, a return code of 4098 (Use Of Timeout Parameter Not Supported) must be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b8a5-137">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6b8a5-137">Return value</span></span>

<span data-ttu-id="6b8a5-138">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6b8a5-138">Type: **uint32**</span></span>

<span data-ttu-id="6b8a5-139">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="6b8a5-139">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="6b8a5-140">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="6b8a5-140">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6b8a5-141">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="6b8a5-141">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="6b8a5-142">**Errore sconosciuto/non specificato** (2)</span><span class="sxs-lookup"><span data-stu-id="6b8a5-142">**Unknown/Unspecified Error** (2)</span></span>
</dt> <dt>

<span data-ttu-id="6b8a5-143">**Non può essere completato entro il periodo di timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="6b8a5-143">**Cannot complete within Timeout Period** (3)</span></span>
</dt> <dt>

<span data-ttu-id="6b8a5-144">**Non riuscito** (4)</span><span class="sxs-lookup"><span data-stu-id="6b8a5-144">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="6b8a5-145">**Parametro non valido** (5)</span><span class="sxs-lookup"><span data-stu-id="6b8a5-145">**Invalid Parameter** (5)</span></span>
</dt> <dt>

<span data-ttu-id="6b8a5-146">**In uso** (6)</span><span class="sxs-lookup"><span data-stu-id="6b8a5-146">**In Use** (6)</span></span>
</dt> <dt>

<span data-ttu-id="6b8a5-147">**DMTF riservato** (7 4095)</span><span class="sxs-lookup"><span data-stu-id="6b8a5-147">**DMTF Reserved** (7 4095)</span></span>
</dt> <dt>

<span data-ttu-id="6b8a5-148">**Parametri del metodo controllati-transizione avviata** (4096)</span><span class="sxs-lookup"><span data-stu-id="6b8a5-148">**Method Parameters Checked - Transition Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="6b8a5-149">**Transizione di stato non valida** (4097)</span><span class="sxs-lookup"><span data-stu-id="6b8a5-149">**Invalid State Transition** (4097)</span></span>
</dt> <dt>

<span data-ttu-id="6b8a5-150">**Utilizzo del parametro timeout non supportato** (4098)</span><span class="sxs-lookup"><span data-stu-id="6b8a5-150">**Use of Timeout Parameter Not Supported** (4098)</span></span>
</dt> <dt>

<span data-ttu-id="6b8a5-151">**Occupato** (4099)</span><span class="sxs-lookup"><span data-stu-id="6b8a5-151">**Busy** (4099)</span></span>
</dt> <dt>

<span data-ttu-id="6b8a5-152">**Metodo riservato** (4100 32767)</span><span class="sxs-lookup"><span data-stu-id="6b8a5-152">**Method Reserved** (4100 32767)</span></span>
</dt> <dt>

<span data-ttu-id="6b8a5-153">**Specifico del fornitore** (32768 65535)</span><span class="sxs-lookup"><span data-stu-id="6b8a5-153">**Vendor Specific** (32768 65535)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="6b8a5-154">Commenti</span><span class="sxs-lookup"><span data-stu-id="6b8a5-154">Remarks</span></span>

<span data-ttu-id="6b8a5-155">L'accesso alla [**classe \_ ConcreteJob di MSVM**](msvm-concretejob.md) potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="6b8a5-155">Access to the [**Msvm\_ConcreteJob**](msvm-concretejob.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="6b8a5-156">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="6b8a5-156">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="6b8a5-157">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6b8a5-157">Requirements</span></span>



| <span data-ttu-id="6b8a5-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b8a5-158">Requirement</span></span> | <span data-ttu-id="6b8a5-159">Valore</span><span class="sxs-lookup"><span data-stu-id="6b8a5-159">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b8a5-160">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6b8a5-160">Minimum supported client</span></span><br/> | <span data-ttu-id="6b8a5-161">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="6b8a5-161">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="6b8a5-162">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6b8a5-162">Minimum supported server</span></span><br/> | <span data-ttu-id="6b8a5-163">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="6b8a5-163">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6b8a5-164">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6b8a5-164">Namespace</span></span><br/>                | <span data-ttu-id="6b8a5-165">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="6b8a5-165">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="6b8a5-166">MOF</span><span class="sxs-lookup"><span data-stu-id="6b8a5-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6b8a5-167"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6b8a5-167"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6b8a5-168">DLL</span><span class="sxs-lookup"><span data-stu-id="6b8a5-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b8a5-169"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6b8a5-169"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6b8a5-170">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6b8a5-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b8a5-171">**\_ConcreteJob MSVM**</span><span class="sxs-lookup"><span data-stu-id="6b8a5-171">**Msvm\_ConcreteJob**</span></span>](msvm-concretejob.md)
</dt> </dl>

 

