---
description: Richiede che lo stato dell'elemento venga modificato in un valore specificato nel parametro RequestedState.
ms.assetid: 6d0061ad-ca14-400a-b813-af920f231eeb
title: Metodo RequestStateChange della classe CIM_EnabledLogicalElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_EnabledLogicalElement.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5b28a2c33b61893be24eacc882b29b5a2be18b14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104345796"
---
# <a name="requeststatechange-method-of-the-cim_enabledlogicalelement-class"></a><span data-ttu-id="1e3fd-103">Metodo RequestStateChange della classe CIM \_ EnabledLogicalElement</span><span class="sxs-lookup"><span data-stu-id="1e3fd-103">RequestStateChange method of the CIM\_EnabledLogicalElement class</span></span>

<span data-ttu-id="1e3fd-104">Richiede che lo stato dell'elemento venga modificato in un valore specificato nel parametro RequestedState.</span><span class="sxs-lookup"><span data-stu-id="1e3fd-104">Requests that the state of the element be changed to the value specified in the RequestedState parameter.</span></span> <span data-ttu-id="1e3fd-105">Quando viene apportata la modifica dello stato richiesto, EnabledState e RequestedState dell'elemento saranno uguali.</span><span class="sxs-lookup"><span data-stu-id="1e3fd-105">When the requested state change takes place, the EnabledState and RequestedState of the element will be the same.</span></span> <span data-ttu-id="1e3fd-106">Richiamando il metodo RequestStateChange più volte, le richieste precedenti potrebbero essere sovrascritte o perse.</span><span class="sxs-lookup"><span data-stu-id="1e3fd-106">Invoking the RequestStateChange method multiple times could result in earlier requests being overwritten or lost.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e3fd-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1e3fd-107">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="1e3fd-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="1e3fd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e3fd-109">*RequestedState* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1e3fd-109">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e3fd-110">Stato richiesto per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="1e3fd-110">The state requested for the element.</span></span> <span data-ttu-id="1e3fd-111">Queste informazioni verranno inserite nella proprietà **RequestedState** dell'istanza se il codice restituito del metodo **RequestStateChange** è 0 (' completed with No Error ') o 4096 (0X1000) (' job Started ').</span><span class="sxs-lookup"><span data-stu-id="1e3fd-111">This information will be placed into the **RequestedState** property of the instance if the return code of the **RequestStateChange** method is 0 ('Completed with No Error'), or 4096 (0x1000) ('Job Started').</span></span> <span data-ttu-id="1e3fd-112">Per una spiegazione dettagliata dei valori di **RequestedState** , vedere la descrizione delle proprietà **EnabledState** e **RequestedState** .</span><span class="sxs-lookup"><span data-stu-id="1e3fd-112">Refer to the description of the **EnabledState** and **RequestedState** properties for the detailed explanations of the **RequestedState** values.</span></span>

<dt>

<span id="Start"></span><span id="start"></span><span id="START"></span>

<span data-ttu-id="1e3fd-113"><span id="Start"></span><span id="start"></span><span id="START"></span>**Avvio** (2)</span><span class="sxs-lookup"><span data-stu-id="1e3fd-113"><span id="Start"></span><span id="start"></span><span id="START"></span>**Start** (2)</span></span>


</dt> <dd>

<span data-ttu-id="1e3fd-114">Imposta lo stato su "Running".</span><span class="sxs-lookup"><span data-stu-id="1e3fd-114">Changes the state to 'Running'.</span></span>

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span data-ttu-id="1e3fd-115"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Sospendi** (3)</span><span class="sxs-lookup"><span data-stu-id="1e3fd-115"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspend** (3)</span></span>


</dt> <dd>

<span data-ttu-id="1e3fd-116">Arresta temporaneamente il processo.</span><span class="sxs-lookup"><span data-stu-id="1e3fd-116">Stops the job temporarily.</span></span> <span data-ttu-id="1e3fd-117">L'intenzione è di riavviare successivamente il processo con "Start".</span><span class="sxs-lookup"><span data-stu-id="1e3fd-117">The intention is to subsequently restart the job with 'Start'.</span></span> <span data-ttu-id="1e3fd-118">Potrebbe essere possibile immettere lo stato del servizio mentre è sospeso.</span><span class="sxs-lookup"><span data-stu-id="1e3fd-118">It might be possible to enter the 'Service' state while suspended.</span></span> <span data-ttu-id="1e3fd-119">(Si tratta di un processo specifico).</span><span class="sxs-lookup"><span data-stu-id="1e3fd-119">(This is job-specific.)</span></span>

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span data-ttu-id="1e3fd-120"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Termina** (4)</span><span class="sxs-lookup"><span data-stu-id="1e3fd-120"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (4)</span></span>


</dt> <dd>

<span data-ttu-id="1e3fd-121">Arresta il processo in modo pulito, Salva i dati, conserva lo stato e arresta tutti i processi sottostanti in modo ordinato.</span><span class="sxs-lookup"><span data-stu-id="1e3fd-121">Stops the job cleanly, saves data, preserves the state, and shuts down all underlying processes in an orderly manner.</span></span>

</dd> <dt>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>

<span data-ttu-id="1e3fd-122"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span><span class="sxs-lookup"><span data-stu-id="1e3fd-122"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span></span>


</dt> <dd>

<span data-ttu-id="1e3fd-123">Termina immediatamente il processo senza alcuna necessità di salvare i dati o mantenere lo stato.</span><span class="sxs-lookup"><span data-stu-id="1e3fd-123">Terminates the job immediately with no requirement to save data or preserve the state.</span></span>

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="1e3fd-124"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Servizio** (6)</span><span class="sxs-lookup"><span data-stu-id="1e3fd-124"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (6)</span></span>


</dt> <dd>

<span data-ttu-id="1e3fd-125">Inserisce il processo in uno stato del servizio specifico del fornitore.</span><span class="sxs-lookup"><span data-stu-id="1e3fd-125">Puts the job into a vendor-specific service state.</span></span> <span data-ttu-id="1e3fd-126">Potrebbe essere possibile riavviare il processo.</span><span class="sxs-lookup"><span data-stu-id="1e3fd-126">It might be possible to restart the job.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="1e3fd-127"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (7.. 32767)</span><span class="sxs-lookup"><span data-stu-id="1e3fd-127"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (7..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="1e3fd-128"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornitore riservato** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="1e3fd-128"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="1e3fd-129">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="1e3fd-129">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1e3fd-130">Può contenere un riferimento al [**\_ ConcreteJob CIM**](cim-concretejob.md) creato per tenere traccia della transizione di stato iniziata dalla chiamata al metodo.</span><span class="sxs-lookup"><span data-stu-id="1e3fd-130">May contain a reference to the [**CIM\_ConcreteJob**](cim-concretejob.md) created to track the state transition initiated by the method invocation.</span></span>

</dd> <dt>

<span data-ttu-id="1e3fd-131">*TimeoutPeriod* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1e3fd-131">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e3fd-132">Periodo di timeout che specifica la quantità massima di tempo per cui il client prevede che la transizione al nuovo stato venga eseguita.</span><span class="sxs-lookup"><span data-stu-id="1e3fd-132">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="1e3fd-133">Per specificare il periodo di timeout, è necessario utilizzare il formato intervallo.</span><span class="sxs-lookup"><span data-stu-id="1e3fd-133">The interval format must be used to specify the timeout period.</span></span> <span data-ttu-id="1e3fd-134">Il valore 0 o **null** indica che il client non dispone di requisiti temporali per la transizione.</span><span class="sxs-lookup"><span data-stu-id="1e3fd-134">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="1e3fd-135">Se questa proprietà non contiene 0 o **null** e l'implementazione non supporta questo parametro, deve essere restituito un codice restituito 4098 (**utilizzo del parametro timeout non supportato**).</span><span class="sxs-lookup"><span data-stu-id="1e3fd-135">If this property does not contain 0 or **Null** and the implementation does not support this parameter, a return code of 4098 (**Use Of Timeout Parameter Not Supported**) must be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e3fd-136">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1e3fd-136">Return value</span></span>

<span data-ttu-id="1e3fd-137">Restituisce 0 in caso di esito positivo; in caso contrario, restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="1e3fd-137">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="1e3fd-138">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="1e3fd-138">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1e3fd-139">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="1e3fd-139">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1e3fd-140">**Errore sconosciuto o non specificato** (2)</span><span class="sxs-lookup"><span data-stu-id="1e3fd-140">**Unknown or Unspecified Error** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1e3fd-141">**Non può essere completato entro il periodo di timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="1e3fd-141">**Cannot complete within Timeout Period** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1e3fd-142">**Non riuscito** (4)</span><span class="sxs-lookup"><span data-stu-id="1e3fd-142">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="1e3fd-143">**Parametro non valido** (5)</span><span class="sxs-lookup"><span data-stu-id="1e3fd-143">**Invalid Parameter** (5)</span></span>
</dt> <dt>

<span data-ttu-id="1e3fd-144">**In uso** (6)</span><span class="sxs-lookup"><span data-stu-id="1e3fd-144">**In Use** (6)</span></span>
</dt> <dt>

<span data-ttu-id="1e3fd-145">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="1e3fd-145">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="1e3fd-146">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="1e3fd-146">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="1e3fd-147">**Transizione di stato non valida** (4097)</span><span class="sxs-lookup"><span data-stu-id="1e3fd-147">**Invalid State Transition** (4097)</span></span>
</dt> <dt>

<span data-ttu-id="1e3fd-148">**Utilizzo del parametro timeout non supportato** (4098)</span><span class="sxs-lookup"><span data-stu-id="1e3fd-148">**Use of Timeout Parameter Not Supported** (4098)</span></span>
</dt> <dt>

<span data-ttu-id="1e3fd-149">**Occupato** (4099)</span><span class="sxs-lookup"><span data-stu-id="1e3fd-149">**Busy** (4099)</span></span>
</dt> <dt>

<span data-ttu-id="1e3fd-150">**Metodo riservato** (4100.. 32767)</span><span class="sxs-lookup"><span data-stu-id="1e3fd-150">**Method Reserved** (4100..32767)</span></span>
</dt> <dt>

<span data-ttu-id="1e3fd-151">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="1e3fd-151">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="1e3fd-152">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1e3fd-152">Requirements</span></span>



| <span data-ttu-id="1e3fd-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e3fd-153">Requirement</span></span> | <span data-ttu-id="1e3fd-154">Valore</span><span class="sxs-lookup"><span data-stu-id="1e3fd-154">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e3fd-155">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1e3fd-155">Minimum supported client</span></span><br/> | <span data-ttu-id="1e3fd-156">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="1e3fd-156">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="1e3fd-157">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1e3fd-157">Minimum supported server</span></span><br/> | <span data-ttu-id="1e3fd-158">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="1e3fd-158">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="1e3fd-159">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1e3fd-159">Namespace</span></span><br/>                | <span data-ttu-id="1e3fd-160">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="1e3fd-160">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="1e3fd-161">MOF</span><span class="sxs-lookup"><span data-stu-id="1e3fd-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1e3fd-162"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1e3fd-162"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1e3fd-163">DLL</span><span class="sxs-lookup"><span data-stu-id="1e3fd-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e3fd-164"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1e3fd-164"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1e3fd-165">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1e3fd-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e3fd-166">**\_ENABLEDLOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="1e3fd-166">**CIM\_EnabledLogicalElement**</span></span>](cim-enabledlogicalelement.md)
</dt> </dl>

 

 




