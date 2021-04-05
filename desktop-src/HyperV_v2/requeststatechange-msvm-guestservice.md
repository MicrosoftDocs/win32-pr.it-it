---
description: Richiede che lo stato del servizio Guest venga modificato nel valore specificato.
ms.assetid: F2853BB3-4074-431C-9E10-26AA0757FE99
title: 'Metodo Msvm_GuestService:: RequestStateChange'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestService.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1360c36b58c96b7e621e5f339bd503ce4f1390b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757649"
---
# <a name="msvm_guestservicerequeststatechange-method"></a><span data-ttu-id="80dad-103">\_Metodo MSVM GuestService:: RequestStateChange</span><span class="sxs-lookup"><span data-stu-id="80dad-103">Msvm\_GuestService::RequestStateChange method</span></span>

<span data-ttu-id="80dad-104">Richiede che lo stato del servizio Guest venga modificato nel valore specificato.</span><span class="sxs-lookup"><span data-stu-id="80dad-104">Requests that the state of the guest service be changed to the specified value.</span></span>

## <a name="syntax"></a><span data-ttu-id="80dad-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="80dad-105">Syntax</span></span>


```C++
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="80dad-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="80dad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80dad-107">*RequestedState* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="80dad-107">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80dad-108">Nuovo stato.</span><span class="sxs-lookup"><span data-stu-id="80dad-108">The new state.</span></span> <span data-ttu-id="80dad-109">Le informazioni vengono inserite nella proprietà **RequestedState** dell'istanza se il codice restituito del metodo **RequestStateChange** è 0 o 4096.</span><span class="sxs-lookup"><span data-stu-id="80dad-109">The info is placed in the **RequestedState** property of the instance if the return code of the **RequestStateChange** method is 0 or 4096.</span></span> <span data-ttu-id="80dad-110">Per ulteriori informazioni, vedere la descrizione delle proprietà **EnabledState** e **RequestedState** per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="80dad-110">For more info, see the description of the **EnabledState** and **RequestedState** properties for the element.</span></span> <span data-ttu-id="80dad-111">Deve essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="80dad-111">This must be one of the following values.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="80dad-112">**Abilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="80dad-112">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="80dad-113">**Disabilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="80dad-113">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="80dad-114">**Arresto** (4)</span><span class="sxs-lookup"><span data-stu-id="80dad-114">**Shut Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="80dad-115">**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="80dad-115">**Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="80dad-116">**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="80dad-116">**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="80dad-117">**Rinvia** (8)</span><span class="sxs-lookup"><span data-stu-id="80dad-117">**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="80dad-118">**Mettere in stato** (9)</span><span class="sxs-lookup"><span data-stu-id="80dad-118">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="80dad-119">**Riavvio** (10)</span><span class="sxs-lookup"><span data-stu-id="80dad-119">**Reboot** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="80dad-120">**Reimposta** (11)</span><span class="sxs-lookup"><span data-stu-id="80dad-120">**Reset** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="80dad-121">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="80dad-121">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="80dad-122">**Fornitore riservato** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="80dad-122">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="80dad-123">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="80dad-123">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="80dad-124">Riferimento facoltativo a un oggetto [**\_ ConcreteJob CIM**](cim-concretejob.md) restituito se l'operazione viene eseguita in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="80dad-124">An optional reference to a [**CIM\_ConcreteJob**](cim-concretejob.md) object that is returned if the operation is executed asynchronously.</span></span> <span data-ttu-id="80dad-125">Se presente, il riferimento restituito può essere usato per monitorare lo stato di avanzamento e ottenere il risultato del metodo.</span><span class="sxs-lookup"><span data-stu-id="80dad-125">If present, the returned reference can be used to monitor progress and obtain the result of the method.</span></span>

</dd> <dt>

<span data-ttu-id="80dad-126">*TimeoutPeriod* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="80dad-126">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80dad-127">Periodo di timeout che specifica la quantità massima di tempo per cui il client prevede che la transizione al nuovo stato venga eseguita.</span><span class="sxs-lookup"><span data-stu-id="80dad-127">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="80dad-128">Per specificare il periodo di timeout, è necessario utilizzare il formato intervallo.</span><span class="sxs-lookup"><span data-stu-id="80dad-128">The interval format must be used to specify the timeout period.</span></span> <span data-ttu-id="80dad-129">Il valore 0 o **null** indica che il client non dispone di requisiti temporali per la transizione.</span><span class="sxs-lookup"><span data-stu-id="80dad-129">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="80dad-130">Se questa proprietà non contiene 0 o **null** e l'implementazione non supporta questo parametro, deve essere restituito un codice restituito 4098 (**utilizzo del parametro timeout non supportato**).</span><span class="sxs-lookup"><span data-stu-id="80dad-130">If this property does not contain 0 or **Null** and the implementation does not support this parameter, a return code of 4098 (**Use Of Timeout Parameter Not Supported**) must be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80dad-131">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="80dad-131">Return value</span></span>

<span data-ttu-id="80dad-132">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="80dad-132">This method returns one of the following values.</span></span>



| <span data-ttu-id="80dad-133">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="80dad-133">Return code/value</span></span>                                                                                                                                                                       | <span data-ttu-id="80dad-134">Descrizione</span><span class="sxs-lookup"><span data-stu-id="80dad-134">Description</span></span>                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="80dad-135"><dt>**Completato senza errori**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="80dad-135"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>                           | <span data-ttu-id="80dad-136">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="80dad-136">Success.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="80dad-137"><dt>**Non supportato**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="80dad-137"><dt>**Not supported**</dt> <dt>1</dt></span></span> </dl>                                     |                                                                                    |
| <dl> <span data-ttu-id="80dad-138"><dt>**Parametri del metodo controllati-transizione avviata**</dt> <dt>4096</dt></span><span class="sxs-lookup"><span data-stu-id="80dad-138"><dt>**Method Parameters Checked - Transition Started**</dt> <dt>4096</dt></span></span> </dl> | <span data-ttu-id="80dad-139">La transizione è asincrona.</span><span class="sxs-lookup"><span data-stu-id="80dad-139">The transition is asynchronous.</span></span><br/>                                         |
| <dl> <span data-ttu-id="80dad-140"><dt>**Uso del parametro timeout non supportato**</dt> <dt>4098</dt></span><span class="sxs-lookup"><span data-stu-id="80dad-140"><dt>**Use of Timeout Parameter Not Supported**</dt> <dt>4098</dt></span></span> </dl>         |                                                                                    |
| <dl> <span data-ttu-id="80dad-141"><dt>**Accesso negato**</dt> <dt>32769</dt></span><span class="sxs-lookup"><span data-stu-id="80dad-141"><dt>**Access Denied**</dt> <dt>32769</dt></span></span> </dl>                                 | <span data-ttu-id="80dad-142">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="80dad-142">Access denied.</span></span><br/>                                                          |
| <dl> <span data-ttu-id="80dad-143"><dt>**Stato non valido per l'operazione**</dt> <dt>32775</dt></span><span class="sxs-lookup"><span data-stu-id="80dad-143"><dt>**Invalid state for this operation**</dt> <dt>32775</dt></span></span> </dl>              | <span data-ttu-id="80dad-144">Il valore specificato nel parametro *RequestedState* non è supportato.</span><span class="sxs-lookup"><span data-stu-id="80dad-144">The value specified in the *RequestedState* parameter is not supported.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="80dad-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="80dad-145">Requirements</span></span>



| <span data-ttu-id="80dad-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="80dad-146">Requirement</span></span> | <span data-ttu-id="80dad-147">Valore</span><span class="sxs-lookup"><span data-stu-id="80dad-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80dad-148">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="80dad-148">Minimum supported client</span></span><br/> | <span data-ttu-id="80dad-149">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="80dad-149">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="80dad-150">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="80dad-150">Minimum supported server</span></span><br/> | <span data-ttu-id="80dad-151">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="80dad-151">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="80dad-152">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="80dad-152">Namespace</span></span><br/>                | <span data-ttu-id="80dad-153">\\\\\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="80dad-153">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="80dad-154">MOF</span><span class="sxs-lookup"><span data-stu-id="80dad-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="80dad-155"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="80dad-155"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="80dad-156">DLL</span><span class="sxs-lookup"><span data-stu-id="80dad-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80dad-157"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="80dad-157"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="80dad-158">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="80dad-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80dad-159">**\_GuestService MSVM**</span><span class="sxs-lookup"><span data-stu-id="80dad-159">**Msvm\_GuestService**</span></span>](msvm-guestservice.md)
</dt> </dl>

 

 




