---
description: Modifica lo stato del processo.
ms.assetid: 3B11CE45-63E4-43D1-AAF6-02F83C9CBB85
title: 'Metodo Msvm_CopyFileToGuestJob:: RequestStateChange'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CopyFileToGuestJob.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: adf5d866989f3b3518cf53b52e073239e023e3c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314321"
---
# <a name="msvm_copyfiletoguestjobrequeststatechange-method"></a><span data-ttu-id="7abb2-103">\_Metodo MSVM CopyFileToGuestJob:: RequestStateChange</span><span class="sxs-lookup"><span data-stu-id="7abb2-103">Msvm\_CopyFileToGuestJob::RequestStateChange method</span></span>

<span data-ttu-id="7abb2-104">Modifica lo stato del processo.</span><span class="sxs-lookup"><span data-stu-id="7abb2-104">Changes the state of the job.</span></span>

## <a name="syntax"></a><span data-ttu-id="7abb2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7abb2-105">Syntax</span></span>


```C++
uint32 RequestStateChange(
  [in] uint16   RequestedState,
  [in] datetime TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="7abb2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7abb2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7abb2-107">*RequestedState* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7abb2-107">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7abb2-108">Nuovo stato.</span><span class="sxs-lookup"><span data-stu-id="7abb2-108">The new state.</span></span> <span data-ttu-id="7abb2-109">Questi sono i valori possibili:</span><span class="sxs-lookup"><span data-stu-id="7abb2-109">These are the possible values:</span></span>

<dt>

<span id="Start"></span><span id="start"></span><span id="START"></span>

<span data-ttu-id="7abb2-110"><span id="Start"></span><span id="start"></span><span id="START"></span>**Avvio** (2)</span><span class="sxs-lookup"><span data-stu-id="7abb2-110"><span id="Start"></span><span id="start"></span><span id="START"></span>**Start** (2)</span></span>


</dt> <dd>

<span data-ttu-id="7abb2-111">Imposta lo stato su "Running".</span><span class="sxs-lookup"><span data-stu-id="7abb2-111">Changes the state to 'Running'.</span></span>

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span data-ttu-id="7abb2-112"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Sospendi** (3)</span><span class="sxs-lookup"><span data-stu-id="7abb2-112"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspend** (3)</span></span>


</dt> <dd>

<span data-ttu-id="7abb2-113">Arresta temporaneamente il processo.</span><span class="sxs-lookup"><span data-stu-id="7abb2-113">Stops the job temporarily.</span></span> <span data-ttu-id="7abb2-114">Il client può quindi riavviare il processo con ' Start '.</span><span class="sxs-lookup"><span data-stu-id="7abb2-114">The client can then subsequently restart the job with 'Start'.</span></span> <span data-ttu-id="7abb2-115">Il client può eventualmente immettere lo stato ' servizio ' mentre è sospeso (specifico del processo).</span><span class="sxs-lookup"><span data-stu-id="7abb2-115">The client can possibly enter the 'Service' state while suspended (this is job-specific).</span></span>

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span data-ttu-id="7abb2-116"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Termina** (4)</span><span class="sxs-lookup"><span data-stu-id="7abb2-116"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (4)</span></span>


</dt> <dd>

<span data-ttu-id="7abb2-117">Arresta il processo in modo corretto, salvando i dati, mantenendo lo stato e chiudendo tutti i processi sottostanti in modo ordinato.</span><span class="sxs-lookup"><span data-stu-id="7abb2-117">Stops the job cleanly, saving data, preserving the state, and shutting down all underlying processes in an orderly manner.</span></span>

</dd> <dt>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>

<span data-ttu-id="7abb2-118"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span><span class="sxs-lookup"><span data-stu-id="7abb2-118"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span></span>


</dt> <dd>

<span data-ttu-id="7abb2-119">Termina immediatamente il processo senza alcuna necessità di salvare i dati o mantenere lo stato.</span><span class="sxs-lookup"><span data-stu-id="7abb2-119">Terminates the job immediately with no requirement to save data or preserve the state.</span></span>

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="7abb2-120"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Servizio** (6)</span><span class="sxs-lookup"><span data-stu-id="7abb2-120"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (6)</span></span>


</dt> <dd>

<span data-ttu-id="7abb2-121">Inserisce il processo in uno stato del servizio specifico del fornitore.</span><span class="sxs-lookup"><span data-stu-id="7abb2-121">Puts the job into a vendor-specific service state.</span></span> <span data-ttu-id="7abb2-122">Il client può eventualmente riavviare il processo.</span><span class="sxs-lookup"><span data-stu-id="7abb2-122">The client can possibly restart the job.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="7abb2-123"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (7.. 32767)</span><span class="sxs-lookup"><span data-stu-id="7abb2-123"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (7..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="7abb2-124"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornitore riservato** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="7abb2-124"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="7abb2-125">*TimeoutPeriod* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7abb2-125">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7abb2-126">Periodo di timeout che specifica la quantità massima di tempo per cui il client prevede che la transizione al nuovo stato venga eseguita.</span><span class="sxs-lookup"><span data-stu-id="7abb2-126">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="7abb2-127">Per specificare il periodo di timeout, è necessario utilizzare il formato intervallo.</span><span class="sxs-lookup"><span data-stu-id="7abb2-127">The interval format must be used to specify the timeout period.</span></span> <span data-ttu-id="7abb2-128">Il valore 0 o **null** indica che il client non dispone di requisiti temporali per la transizione.</span><span class="sxs-lookup"><span data-stu-id="7abb2-128">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="7abb2-129">Se questa proprietà non contiene 0 o **null** e l'implementazione non supporta questo parametro, deve essere restituito un codice restituito 4098 (**utilizzo del parametro timeout non supportato**).</span><span class="sxs-lookup"><span data-stu-id="7abb2-129">If this property does not contain 0 or **Null** and the implementation does not support this parameter, a return code of 4098 (**Use Of Timeout Parameter Not Supported**) must be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7abb2-130">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7abb2-130">Return value</span></span>

<span data-ttu-id="7abb2-131">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="7abb2-131">This method returns one of the following values.</span></span>



| <span data-ttu-id="7abb2-132">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="7abb2-132">Return code/value</span></span>                                                                                                                                                               | <span data-ttu-id="7abb2-133">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7abb2-133">Description</span></span>                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7abb2-134"><dt>**Completato senza errori**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7abb2-134"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>                   | <span data-ttu-id="7abb2-135">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="7abb2-135">Success.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="7abb2-136"><dt>**Uso del parametro timeout non supportato**</dt> <dt>4098</dt></span><span class="sxs-lookup"><span data-stu-id="7abb2-136"><dt>**Use of Timeout Parameter Not Supported**</dt> <dt>4098</dt></span></span> </dl> |                                                                                    |
| <dl> <span data-ttu-id="7abb2-137"><dt>**Errore**</dt> <dt>32768</dt></span><span class="sxs-lookup"><span data-stu-id="7abb2-137"><dt>**Failed**</dt> <dt>32768</dt></span></span> </dl>                                |                                                                                    |
| <dl> <span data-ttu-id="7abb2-138"><dt>**Accesso negato**</dt> <dt>32769</dt></span><span class="sxs-lookup"><span data-stu-id="7abb2-138"><dt>**Access Denied**</dt> <dt>32769</dt></span></span> </dl>                         | <span data-ttu-id="7abb2-139">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="7abb2-139">Access denied.</span></span><br/>                                                          |
| <dl> <span data-ttu-id="7abb2-140"><dt>**Non supportato**</dt> <dt>32770</dt></span><span class="sxs-lookup"><span data-stu-id="7abb2-140"><dt>**Not Supported**</dt> <dt>32770</dt></span></span> </dl>                         |                                                                                    |
| <dl> <span data-ttu-id="7abb2-141"><dt>**Stato sconosciuto**</dt> <dt>32771</dt></span><span class="sxs-lookup"><span data-stu-id="7abb2-141"><dt>**Status is unknown**</dt> <dt>32771</dt></span></span> </dl>                     |                                                                                    |
| <dl> <span data-ttu-id="7abb2-142"><dt>**Timeout**</dt> <dt>32772</dt></span><span class="sxs-lookup"><span data-stu-id="7abb2-142"><dt>**Timeout**</dt> <dt>32772</dt></span></span> </dl>                               |                                                                                    |
| <dl> <span data-ttu-id="7abb2-143"><dt>**Parametro non valido**</dt> <dt>32773</dt></span><span class="sxs-lookup"><span data-stu-id="7abb2-143"><dt>**Invalid parameter**</dt> <dt>32773</dt></span></span> </dl>                     |                                                                                    |
| <dl> <span data-ttu-id="7abb2-144">Il <dt>**sistema è in uso**</dt> <dt>32774</dt></span><span class="sxs-lookup"><span data-stu-id="7abb2-144"><dt>**System is in use**</dt> <dt>32774</dt></span></span> </dl>                      |                                                                                    |
| <dl> <span data-ttu-id="7abb2-145"><dt>**Stato non valido per l'operazione**</dt> <dt>32775</dt></span><span class="sxs-lookup"><span data-stu-id="7abb2-145"><dt>**Invalid state for this operation**</dt> <dt>32775</dt></span></span> </dl>      | <span data-ttu-id="7abb2-146">Il valore specificato nel parametro *RequestedState* non è supportato.</span><span class="sxs-lookup"><span data-stu-id="7abb2-146">The value specified in the *RequestedState* parameter is not supported.</span></span><br/> |
| <dl> <span data-ttu-id="7abb2-147"><dt>**Tipo di dati non corretto**</dt> <dt>32776</dt></span><span class="sxs-lookup"><span data-stu-id="7abb2-147"><dt>**Incorrect data type**</dt> <dt>32776</dt></span></span> </dl>                   |                                                                                    |
| <dl> <span data-ttu-id="7abb2-148">Il <dt>**sistema non è disponibile**</dt> <dt>32777</dt></span><span class="sxs-lookup"><span data-stu-id="7abb2-148"><dt>**System is not available**</dt> <dt>32777</dt></span></span> </dl>               |                                                                                    |
| <dl> <span data-ttu-id="7abb2-149"><dt>**Memoria insufficiente**</dt> <dt>32778</dt></span><span class="sxs-lookup"><span data-stu-id="7abb2-149"><dt>**Out of memory**</dt> <dt>32778</dt></span></span> </dl>                         |                                                                                    |



 

## <a name="requirements"></a><span data-ttu-id="7abb2-150">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7abb2-150">Requirements</span></span>



| <span data-ttu-id="7abb2-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="7abb2-151">Requirement</span></span> | <span data-ttu-id="7abb2-152">Valore</span><span class="sxs-lookup"><span data-stu-id="7abb2-152">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7abb2-153">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7abb2-153">Minimum supported client</span></span><br/> | <span data-ttu-id="7abb2-154">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7abb2-154">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="7abb2-155">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7abb2-155">Minimum supported server</span></span><br/> | <span data-ttu-id="7abb2-156">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="7abb2-156">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7abb2-157">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7abb2-157">Namespace</span></span><br/>                | <span data-ttu-id="7abb2-158">\\\\\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="7abb2-158">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="7abb2-159">MOF</span><span class="sxs-lookup"><span data-stu-id="7abb2-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7abb2-160"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7abb2-160"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7abb2-161">DLL</span><span class="sxs-lookup"><span data-stu-id="7abb2-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7abb2-162"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7abb2-162"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7abb2-163">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7abb2-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7abb2-164">**\_CopyFileToGuestJob MSVM**</span><span class="sxs-lookup"><span data-stu-id="7abb2-164">**Msvm\_CopyFileToGuestJob**</span></span>](msvm-copyfiletoguestjob.md)
</dt> </dl>

 

 




