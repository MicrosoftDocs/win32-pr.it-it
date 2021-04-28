---
description: 'Metodo RequestStateChange della classe Msvm_VirtualSystemReferencePointExportJob : richiede una modifica dello stato.'
ms.assetid: 53c24e17-2b59-4439-a6d1-e971c189d223
title: Metodo RequestStateChange della classe Msvm_VirtualSystemReferencePointExportJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointExportJob.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: bd12d7cd5b79e38260e671bf1408304390985dac
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109309"
---
# <a name="requeststatechange-method-of-the-msvm_virtualsystemreferencepointexportjob-class"></a><span data-ttu-id="a6325-103">Metodo RequestStateChange della classe Msvm \_ VirtualSystemReferencePointExportJob</span><span class="sxs-lookup"><span data-stu-id="a6325-103">RequestStateChange method of the Msvm\_VirtualSystemReferencePointExportJob class</span></span>

<span data-ttu-id="a6325-104">Richiede una modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="a6325-104">Requests a state change.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6325-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a6325-105">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in] uint16   RequestedState,
  [in] datetime TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="a6325-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a6325-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6325-107">*RequestedState* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="a6325-107">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6325-108">Modifica lo stato di un processo.</span><span class="sxs-lookup"><span data-stu-id="a6325-108">Changes the state of a job.</span></span> <span data-ttu-id="a6325-109">I valori possibili sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="a6325-109">The possible values are as follows:</span></span>

<dt>

<span id="Start"></span><span id="start"></span><span id="START"></span>

<span data-ttu-id="a6325-110"><span id="Start"></span><span id="start"></span><span id="START"></span>**Start** (2)</span><span class="sxs-lookup"><span data-stu-id="a6325-110"><span id="Start"></span><span id="start"></span><span id="START"></span>**Start** (2)</span></span>


</dt> <dd>

<span data-ttu-id="a6325-111">Modifica lo stato in "In esecuzione".</span><span class="sxs-lookup"><span data-stu-id="a6325-111">Changes the state to 'Running'.</span></span>

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span data-ttu-id="a6325-112"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspend** (3)</span><span class="sxs-lookup"><span data-stu-id="a6325-112"><span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspend** (3)</span></span>


</dt> <dd>

<span data-ttu-id="a6325-113">Arresta temporaneamente il processo.</span><span class="sxs-lookup"><span data-stu-id="a6325-113">Stops the job temporarily.</span></span> <span data-ttu-id="a6325-114">L'intenzione è di riavviare successivamente il processo con 'Start'.</span><span class="sxs-lookup"><span data-stu-id="a6325-114">The intention is to subsequently restart the job with 'Start'.</span></span> <span data-ttu-id="a6325-115">Potrebbe essere possibile entrare nello stato "Servizio" durante la sospensione.</span><span class="sxs-lookup"><span data-stu-id="a6325-115">It might be possible to enter the 'Service' state while suspended.</span></span> <span data-ttu-id="a6325-116">Si tratta di un processo specifico.</span><span class="sxs-lookup"><span data-stu-id="a6325-116">(This is job-specific.)</span></span>

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span data-ttu-id="a6325-117"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (4)</span><span class="sxs-lookup"><span data-stu-id="a6325-117"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (4)</span></span>


</dt> <dd>

<span data-ttu-id="a6325-118">Arresta il processo in modo pulito, salva i dati, mantiene lo stato e arresta tutti i processi sottostanti in modo ordinato.</span><span class="sxs-lookup"><span data-stu-id="a6325-118">Stops the job cleanly, saves data, preserves the state, and shuts down all underlying processes in an orderly manner.</span></span>

</dd> <dt>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>

<span data-ttu-id="a6325-119"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span><span class="sxs-lookup"><span data-stu-id="a6325-119"><span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)</span></span>


</dt> <dd>

<span data-ttu-id="a6325-120">Termina immediatamente il processo senza che sia necessario salvare i dati o mantenere lo stato.</span><span class="sxs-lookup"><span data-stu-id="a6325-120">Terminates the job immediately with no requirement to save data or preserve the state.</span></span>

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="a6325-121"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Servizio** (6)</span><span class="sxs-lookup"><span data-stu-id="a6325-121"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (6)</span></span>


</dt> <dd>

<span data-ttu-id="a6325-122">Inserisce il processo in uno stato del servizio specifico del fornitore.</span><span class="sxs-lookup"><span data-stu-id="a6325-122">Puts the job into a vendor-specific service state.</span></span> <span data-ttu-id="a6325-123">Potrebbe essere possibile riavviare il processo.</span><span class="sxs-lookup"><span data-stu-id="a6325-123">It might be possible to restart the job.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="a6325-124"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DmTF riservato** (7..32767)</span><span class="sxs-lookup"><span data-stu-id="a6325-124"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (7..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="a6325-125"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornitore riservato** (32768..65535)</span><span class="sxs-lookup"><span data-stu-id="a6325-125"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="a6325-126">*TimeoutPeriod* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="a6325-126">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6325-127">Periodo di timeout che specifica la quantità massima di tempo prevista dal client per la transizione al nuovo stato.</span><span class="sxs-lookup"><span data-stu-id="a6325-127">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="a6325-128">Il formato dell'intervallo deve essere usato per specificare il periodo di timeout.</span><span class="sxs-lookup"><span data-stu-id="a6325-128">The interval format must be used to specify the timeout period.</span></span> <span data-ttu-id="a6325-129">Il valore 0 o **Null** indica che il client non ha requisiti di tempo per la transizione.</span><span class="sxs-lookup"><span data-stu-id="a6325-129">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="a6325-130">Se questa proprietà non contiene 0 o **Null** e l'implementazione non supporta questo parametro, deve essere restituito un codice restituito 4098 ( Utilizzo del parametro **di timeout** non supportato ).</span><span class="sxs-lookup"><span data-stu-id="a6325-130">If this property does not contain 0 or **Null** and the implementation does not support this parameter, a return code of 4098 (**Use Of Timeout Parameter Not Supported**) must be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6325-131">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a6325-131">Return value</span></span>

<span data-ttu-id="a6325-132">Restituisce un valore 0 in esito positivo. In caso contrario, restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="a6325-132">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

 <span data-ttu-id="a6325-133"> (0)</span><span class="sxs-lookup"><span data-stu-id="a6325-133">(0)</span></span>
</dt> <dt>

 <span data-ttu-id="a6325-134">(32768)</span><span class="sxs-lookup"><span data-stu-id="a6325-134">(32768)</span></span>
</dt> <dt>

 <span data-ttu-id="a6325-135">(32769)</span><span class="sxs-lookup"><span data-stu-id="a6325-135">(32769)</span></span>
</dt> <dt>

 <span data-ttu-id="a6325-136">(32770)</span><span class="sxs-lookup"><span data-stu-id="a6325-136">(32770)</span></span>
</dt> <dt>

 <span data-ttu-id="a6325-137">(32771)</span><span class="sxs-lookup"><span data-stu-id="a6325-137">(32771)</span></span>
</dt> <dt>

 <span data-ttu-id="a6325-138">(32772)</span><span class="sxs-lookup"><span data-stu-id="a6325-138">(32772)</span></span>
</dt> <dt>

 <span data-ttu-id="a6325-139">(32773)</span><span class="sxs-lookup"><span data-stu-id="a6325-139">(32773)</span></span>
</dt> <dt>

 <span data-ttu-id="a6325-140">(32774)</span><span class="sxs-lookup"><span data-stu-id="a6325-140">(32774)</span></span>
</dt> <dt>

 <span data-ttu-id="a6325-141">(32775)</span><span class="sxs-lookup"><span data-stu-id="a6325-141">(32775)</span></span>
</dt> <dt>

 <span data-ttu-id="a6325-142">(32776)</span><span class="sxs-lookup"><span data-stu-id="a6325-142">(32776)</span></span>
</dt> <dt>

 <span data-ttu-id="a6325-143">(32777)</span><span class="sxs-lookup"><span data-stu-id="a6325-143">(32777)</span></span>
</dt> <dt>

 <span data-ttu-id="a6325-144">(32778)</span><span class="sxs-lookup"><span data-stu-id="a6325-144">(32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="a6325-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a6325-145">Requirements</span></span>



| <span data-ttu-id="a6325-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6325-146">Requirement</span></span> | <span data-ttu-id="a6325-147">Valore</span><span class="sxs-lookup"><span data-stu-id="a6325-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6325-148">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a6325-148">Minimum supported client</span></span><br/> | <span data-ttu-id="a6325-149">Windows 10, solo app desktop versione 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="a6325-149">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="a6325-150">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a6325-150">Minimum supported server</span></span><br/> | <span data-ttu-id="a6325-151">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="a6325-151">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="a6325-152">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a6325-152">Namespace</span></span><br/>                | <span data-ttu-id="a6325-153">Virtualizzazione \\ radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="a6325-153">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="a6325-154">MOF</span><span class="sxs-lookup"><span data-stu-id="a6325-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a6325-155"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="a6325-155"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a6325-156">DLL</span><span class="sxs-lookup"><span data-stu-id="a6325-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a6325-157"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a6325-157"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a6325-158">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a6325-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6325-159">**Msvm \_ VirtualSystemReferencePointExportJob**</span><span class="sxs-lookup"><span data-stu-id="a6325-159">**Msvm\_VirtualSystemReferencePointExportJob**</span></span>](msvm-virtualsystemreferencepointexportjob.md)
</dt> </dl>

 

 




