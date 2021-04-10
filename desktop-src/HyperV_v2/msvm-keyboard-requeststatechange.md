---
description: Richiede che lo stato dell'elemento venga modificato.
ms.assetid: D1742588-D932-4FE1-8D2A-E410BEE371FF
title: Metodo RequestStateChange della classe Msvm_Keyboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c3358c6c9907717e536466466dd074faf3a038a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966788"
---
# <a name="requeststatechange-method-of-the-msvm_keyboard-class"></a><span data-ttu-id="d170b-103">Metodo RequestStateChange della classe della \_ tastiera MSVM</span><span class="sxs-lookup"><span data-stu-id="d170b-103">RequestStateChange method of the Msvm\_Keyboard class</span></span>

<span data-ttu-id="d170b-104">Richiede che lo stato dell'elemento venga modificato.</span><span class="sxs-lookup"><span data-stu-id="d170b-104">Requests that the state of the element be changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="d170b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d170b-105">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="d170b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d170b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d170b-107">*RequestedState* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d170b-107">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d170b-108">Nuovo stato richiesto per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="d170b-108">The new state requested for the element.</span></span> <span data-ttu-id="d170b-109">Queste informazioni verranno inserite nella proprietà **RequestedState** dell'istanza se il codice restituito è 0 (' completato senza errori '), 3 (' timeout ') o 4096 (0x1000) (' processo avviato ').</span><span class="sxs-lookup"><span data-stu-id="d170b-109">This information will be placed into the **RequestedState** property of the instance if the return code is 0 ('Completed with No Error'), 3 ('Timeout'), or 4096 (0x1000) ('Job Started').</span></span> <span data-ttu-id="d170b-110">Per una spiegazione dettagliata dei valori *RequestedState* , vedere la descrizione delle proprietà **EnabledState** e **RequestedState** .</span><span class="sxs-lookup"><span data-stu-id="d170b-110">For detailed explanations of the *RequestedState* values, see the description of the **EnabledState** and **RequestedState** properties.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="d170b-111">**Abilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="d170b-111">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="d170b-112">**Disabilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="d170b-112">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="d170b-113">**Arresto** (4)</span><span class="sxs-lookup"><span data-stu-id="d170b-113">**Shut Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="d170b-114">**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="d170b-114">**Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="d170b-115">**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="d170b-115">**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="d170b-116">**Rinvia** (8)</span><span class="sxs-lookup"><span data-stu-id="d170b-116">**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="d170b-117">**Mettere in stato** (9)</span><span class="sxs-lookup"><span data-stu-id="d170b-117">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="d170b-118">**Riavvio** (10)</span><span class="sxs-lookup"><span data-stu-id="d170b-118">**Reboot** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="d170b-119">**Reimposta** (11)</span><span class="sxs-lookup"><span data-stu-id="d170b-119">**Reset** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="d170b-120">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="d170b-120">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="d170b-121">**Fornitore riservato** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="d170b-121">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="d170b-122">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="d170b-122">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d170b-123">Riferimento al processo.</span><span class="sxs-lookup"><span data-stu-id="d170b-123">A reference to the job.</span></span> <span data-ttu-id="d170b-124">Questo parametro può essere **null** se l'attività è stata completata.</span><span class="sxs-lookup"><span data-stu-id="d170b-124">This parameter can be **Null** if the task is completed.</span></span>

</dd> <dt>

<span data-ttu-id="d170b-125">*TimeoutPeriod* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d170b-125">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d170b-126">Quantità massima di tempo per cui il client prevede che la transizione al nuovo stato venga eseguita.</span><span class="sxs-lookup"><span data-stu-id="d170b-126">The maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="d170b-127">Per specificare questo periodo di timeout, è necessario utilizzare il formato intervallo.</span><span class="sxs-lookup"><span data-stu-id="d170b-127">The interval format must be used to specify this time-out period.</span></span> <span data-ttu-id="d170b-128">Il valore 0 o **null** indica che il client non dispone di requisiti temporali per la transizione.</span><span class="sxs-lookup"><span data-stu-id="d170b-128">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="d170b-129">Se questa proprietà non contiene 0 o **null** e l'implementazione non supporta questo parametro, viene restituito un codice restituito di 4098 ("utilizzo del parametro timeout non supportato").</span><span class="sxs-lookup"><span data-stu-id="d170b-129">If this property does not contain 0 or **Null**, and the implementation does not support this parameter, a return code of 4098 ("Use Of Timeout Parameter Not Supported") is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d170b-130">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d170b-130">Return value</span></span>

<dl> <dt>

<span data-ttu-id="d170b-131">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="d170b-131">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d170b-132">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="d170b-132">**Not supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d170b-133">**Errore sconosciuto o non specificato** (2)</span><span class="sxs-lookup"><span data-stu-id="d170b-133">**Unknown or Unspecified Error** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d170b-134">**Non può essere completato entro il periodo di timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="d170b-134">**Cannot complete within Timeout Period** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d170b-135">**Non riuscito** (4)</span><span class="sxs-lookup"><span data-stu-id="d170b-135">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d170b-136">**Parametro non valido** (5)</span><span class="sxs-lookup"><span data-stu-id="d170b-136">**Invalid Parameter** (5)</span></span>
</dt> <dt>

<span data-ttu-id="d170b-137">**In uso** (6)</span><span class="sxs-lookup"><span data-stu-id="d170b-137">**In Use** (6)</span></span>
</dt> <dt>

<span data-ttu-id="d170b-138">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="d170b-138">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d170b-139">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="d170b-139">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="d170b-140">**Transizione di stato non valida** (4097)</span><span class="sxs-lookup"><span data-stu-id="d170b-140">**Invalid State Transition** (4097)</span></span>
</dt> <dt>

<span data-ttu-id="d170b-141">**Utilizzo del parametro timeout non supportato** (4098)</span><span class="sxs-lookup"><span data-stu-id="d170b-141">**Use of Timeout Parameter Not Supported** (4098)</span></span>
</dt> <dt>

<span data-ttu-id="d170b-142">**Occupato** (4099)</span><span class="sxs-lookup"><span data-stu-id="d170b-142">**Busy** (4099)</span></span>
</dt> <dt>

<span data-ttu-id="d170b-143">**Metodo riservato** (4100.. 32767)</span><span class="sxs-lookup"><span data-stu-id="d170b-143">**Method Reserved** (4100..32767)</span></span>
</dt> <dt>

<span data-ttu-id="d170b-144">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="d170b-144">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="d170b-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d170b-145">Requirements</span></span>



| <span data-ttu-id="d170b-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="d170b-146">Requirement</span></span> | <span data-ttu-id="d170b-147">Valore</span><span class="sxs-lookup"><span data-stu-id="d170b-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d170b-148">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d170b-148">Minimum supported client</span></span><br/> | <span data-ttu-id="d170b-149">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d170b-149">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="d170b-150">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d170b-150">Minimum supported server</span></span><br/> | <span data-ttu-id="d170b-151">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="d170b-151">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d170b-152">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d170b-152">Namespace</span></span><br/>                | <span data-ttu-id="d170b-153">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="d170b-153">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d170b-154">MOF</span><span class="sxs-lookup"><span data-stu-id="d170b-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d170b-155"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d170b-155"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d170b-156">DLL</span><span class="sxs-lookup"><span data-stu-id="d170b-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d170b-157"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d170b-157"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d170b-158">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d170b-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d170b-159">**\_Tastiera MSVM**</span><span class="sxs-lookup"><span data-stu-id="d170b-159">**Msvm\_Keyboard**</span></span>](msvm-keyboard.md)
</dt> </dl>

 

 




