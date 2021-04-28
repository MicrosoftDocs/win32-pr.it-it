---
description: 'Metodo RequestStateChange della classe Msvm_CollectionReferencePointExportJob : richiede una modifica dello stato.'
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
ms.openlocfilehash: 84956e206654de022c3151aa5a442651f9c2375a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119239"
---
# <a name="requeststatechange-method-of-the-msvm_collectionreferencepointexportjob-class"></a><span data-ttu-id="c5b6d-103">Metodo RequestStateChange della classe Msvm \_ CollectionReferencePointExportJob</span><span class="sxs-lookup"><span data-stu-id="c5b6d-103">RequestStateChange method of the Msvm\_CollectionReferencePointExportJob class</span></span>

<span data-ttu-id="c5b6d-104">Richiede una modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="c5b6d-104">Requests a state change.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5b6d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c5b6d-105">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in] uint16   RequestedState,
  [in] datetime TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="c5b6d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c5b6d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5b6d-107">*RequestedState* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="c5b6d-107">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5b6d-108">RequestStateChange modifica lo stato di un processo.</span><span class="sxs-lookup"><span data-stu-id="c5b6d-108">RequestStateChange changes the state of a job.</span></span> <span data-ttu-id="c5b6d-109">I valori possibili sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="c5b6d-109">The possible values are as follows:</span></span>

<dt>

<span id="Start"></span><span id="start"></span><span id="START"></span>

<span data-ttu-id="c5b6d-110"><span id="Start"></span><span id="start"></span><span id="START"></span>**Inizio** (2)</span><span class="sxs-lookup"><span data-stu-id="c5b6d-110"><span id="Start"></span><span id="start"></span><span id="START"></span>**Start** (2)</span></span>


</dt> <dd>

<span data-ttu-id="c5b6d-111">Modifica lo stato in "In esecuzione".</span><span class="sxs-lookup"><span data-stu-id="c5b6d-111">Changes the state to 'Running'.</span></span>

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span data-ttu-id="c5b6d-112"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Sospendi** (3)</span><span class="sxs-lookup"><span data-stu-id="c5b6d-112"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspend** (3)</span></span>


</dt> <dd>

<span data-ttu-id="c5b6d-113">Arresta temporaneamente il processo.</span><span class="sxs-lookup"><span data-stu-id="c5b6d-113">Stops the job temporarily.</span></span> <span data-ttu-id="c5b6d-114">L'intenzione è riavviare successivamente il processo con "Start".</span><span class="sxs-lookup"><span data-stu-id="c5b6d-114">The intention is to subsequently restart the job with 'Start'.</span></span> <span data-ttu-id="c5b6d-115">Potrebbe essere possibile immettere lo stato "Servizio" durante la sospensione.</span><span class="sxs-lookup"><span data-stu-id="c5b6d-115">It might be possible to enter the 'Service' state while suspended.</span></span> <span data-ttu-id="c5b6d-116">Si tratta di un processo specifico.</span><span class="sxs-lookup"><span data-stu-id="c5b6d-116">(This is job-specific.)</span></span>

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span data-ttu-id="c5b6d-117"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Termina** (4)</span><span class="sxs-lookup"><span data-stu-id="c5b6d-117"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (4)</span></span>


</dt> <dd>

<span data-ttu-id="c5b6d-118">Arresta il processo in modo pulito, salva i dati, mantiene lo stato e arresta tutti i processi sottostanti in modo ordinato.</span><span class="sxs-lookup"><span data-stu-id="c5b6d-118">Stops the job cleanly, saves data, preserves the state, and shuts down all underlying processes in an orderly manner.</span></span>

</dd> <dt>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>

<span data-ttu-id="c5b6d-119"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span><span class="sxs-lookup"><span data-stu-id="c5b6d-119"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span></span>


</dt> <dd>

<span data-ttu-id="c5b6d-120">Termina immediatamente il processo senza alcun requisito per salvare i dati o mantenere lo stato.</span><span class="sxs-lookup"><span data-stu-id="c5b6d-120">Terminates the job immediately with no requirement to save data or preserve the state.</span></span>

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="c5b6d-121"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Servizio** (6)</span><span class="sxs-lookup"><span data-stu-id="c5b6d-121"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (6)</span></span>


</dt> <dd>

<span data-ttu-id="c5b6d-122">Inserisce il processo in uno stato del servizio specifico del fornitore.</span><span class="sxs-lookup"><span data-stu-id="c5b6d-122">Puts the job into a vendor-specific service state.</span></span> <span data-ttu-id="c5b6d-123">Potrebbe essere possibile riavviare il processo.</span><span class="sxs-lookup"><span data-stu-id="c5b6d-123">It might be possible to restart the job.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="c5b6d-124"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DmTF Reserved** (7..32767)</span><span class="sxs-lookup"><span data-stu-id="c5b6d-124"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (7..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="c5b6d-125"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span><span class="sxs-lookup"><span data-stu-id="c5b6d-125"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="c5b6d-126">*TimeoutPeriod* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="c5b6d-126">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5b6d-127">Periodo di timeout che specifica la quantità massima di tempo prevista dal client per la transizione al nuovo stato.</span><span class="sxs-lookup"><span data-stu-id="c5b6d-127">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="c5b6d-128">Il formato dell'intervallo deve essere usato per specificare il periodo di timeout.</span><span class="sxs-lookup"><span data-stu-id="c5b6d-128">The interval format must be used to specify the timeout period.</span></span> <span data-ttu-id="c5b6d-129">Il valore 0 o **Null** indica che il client non ha requisiti di tempo per la transizione.</span><span class="sxs-lookup"><span data-stu-id="c5b6d-129">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="c5b6d-130">Se questa proprietà non contiene 0 o **Null** e l'implementazione non supporta questo parametro, deve essere restituito un codice restituito 4098 (Utilizzo del parametro di **timeout** non supportato).</span><span class="sxs-lookup"><span data-stu-id="c5b6d-130">If this property does not contain 0 or **Null** and the implementation does not support this parameter, a return code of 4098 (**Use Of Timeout Parameter Not Supported**) must be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5b6d-131">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c5b6d-131">Return value</span></span>

<span data-ttu-id="c5b6d-132">Restituisce 0 se l'operazione ha esito positivo. In caso contrario, restituisce uno degli errori seguenti.</span><span class="sxs-lookup"><span data-stu-id="c5b6d-132">Returns 0 on success; otherwise, returns one of the following errors.</span></span>

<dl> <dt>

 <span data-ttu-id="c5b6d-133"> (0)</span><span class="sxs-lookup"><span data-stu-id="c5b6d-133">(0)</span></span>
</dt> <dt>

 <span data-ttu-id="c5b6d-134">(32768)</span><span class="sxs-lookup"><span data-stu-id="c5b6d-134">(32768)</span></span>
</dt> <dt>

 <span data-ttu-id="c5b6d-135">(32769)</span><span class="sxs-lookup"><span data-stu-id="c5b6d-135">(32769)</span></span>
</dt> <dt>

 <span data-ttu-id="c5b6d-136">(32770)</span><span class="sxs-lookup"><span data-stu-id="c5b6d-136">(32770)</span></span>
</dt> <dt>

 <span data-ttu-id="c5b6d-137">(32771)</span><span class="sxs-lookup"><span data-stu-id="c5b6d-137">(32771)</span></span>
</dt> <dt>

 <span data-ttu-id="c5b6d-138">(32772)</span><span class="sxs-lookup"><span data-stu-id="c5b6d-138">(32772)</span></span>
</dt> <dt>

 <span data-ttu-id="c5b6d-139">(32773)</span><span class="sxs-lookup"><span data-stu-id="c5b6d-139">(32773)</span></span>
</dt> <dt>

 <span data-ttu-id="c5b6d-140">(32774)</span><span class="sxs-lookup"><span data-stu-id="c5b6d-140">(32774)</span></span>
</dt> <dt>

 <span data-ttu-id="c5b6d-141">(32775)</span><span class="sxs-lookup"><span data-stu-id="c5b6d-141">(32775)</span></span>
</dt> <dt>

 <span data-ttu-id="c5b6d-142">(32776)</span><span class="sxs-lookup"><span data-stu-id="c5b6d-142">(32776)</span></span>
</dt> <dt>

 <span data-ttu-id="c5b6d-143">(32777)</span><span class="sxs-lookup"><span data-stu-id="c5b6d-143">(32777)</span></span>
</dt> <dt>

 <span data-ttu-id="c5b6d-144">(32778)</span><span class="sxs-lookup"><span data-stu-id="c5b6d-144">(32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="c5b6d-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c5b6d-145">Requirements</span></span>



| <span data-ttu-id="c5b6d-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5b6d-146">Requirement</span></span> | <span data-ttu-id="c5b6d-147">Valore</span><span class="sxs-lookup"><span data-stu-id="c5b6d-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5b6d-148">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c5b6d-148">Minimum supported client</span></span><br/> | <span data-ttu-id="c5b6d-149">Windows 10, solo app desktop versione 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="c5b6d-149">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="c5b6d-150">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c5b6d-150">Minimum supported server</span></span><br/> | <span data-ttu-id="c5b6d-151">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="c5b6d-151">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="c5b6d-152">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c5b6d-152">Namespace</span></span><br/>                | <span data-ttu-id="c5b6d-153">Virtualizzazione \\ radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="c5b6d-153">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c5b6d-154">MOF</span><span class="sxs-lookup"><span data-stu-id="c5b6d-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c5b6d-155"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="c5b6d-155"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c5b6d-156">DLL</span><span class="sxs-lookup"><span data-stu-id="c5b6d-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c5b6d-157"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c5b6d-157"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c5b6d-158">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c5b6d-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5b6d-159">**Msvm \_ CollectionReferencePointExportJob**</span><span class="sxs-lookup"><span data-stu-id="c5b6d-159">**Msvm\_CollectionReferencePointExportJob**</span></span>](msvm-collectionreferencepointexportjob.md)
</dt> </dl>

 

 




