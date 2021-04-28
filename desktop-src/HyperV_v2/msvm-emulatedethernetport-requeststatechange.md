---
description: 'Metodo RequestStateChange della classe Msvm_EmulatedEthernetPort: richiede una modifica dello stato.'
ms.assetid: 3fbfa303-2fee-4c70-9bc1-1882821e9317
title: Metodo RequestStateChange della classe Msvm_EmulatedEthernetPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EmulatedEthernetPort.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: cb66663be6ca1628ed15d3bd914d9773c0dd8ed8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119159"
---
# <a name="requeststatechange-method-of-the-msvm_emulatedethernetport-class"></a><span data-ttu-id="0e0ef-103">Metodo RequestStateChange della classe Msvm \_ EmulatedEthernetPort</span><span class="sxs-lookup"><span data-stu-id="0e0ef-103">RequestStateChange method of the Msvm\_EmulatedEthernetPort class</span></span>

<span data-ttu-id="0e0ef-104">Richiede una modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="0e0ef-104">Requests a state change.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e0ef-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0e0ef-105">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="0e0ef-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0e0ef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e0ef-107">*RequestedState* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="0e0ef-107">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e0ef-108">Nuovo stato.</span><span class="sxs-lookup"><span data-stu-id="0e0ef-108">The new state.</span></span> <span data-ttu-id="0e0ef-109">Le informazioni vengono inserite nella **proprietà RequestedState** dell'istanza se il codice restituito del **metodo RequestStateChange** è 0 o 4096.</span><span class="sxs-lookup"><span data-stu-id="0e0ef-109">The info is placed in the **RequestedState** property of the instance if the return code of the **RequestStateChange** method is 0 or 4096.</span></span> <span data-ttu-id="0e0ef-110">Per altre informazioni, vedere la descrizione delle **proprietà EnabledState** e **RequestedState** per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="0e0ef-110">For more info, see the description of the **EnabledState** and **RequestedState** properties for the element.</span></span> <span data-ttu-id="0e0ef-111">Deve essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="0e0ef-111">This must be one of the following values.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="0e0ef-112">**Abilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="0e0ef-112">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="0e0ef-113">**Disabilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="0e0ef-113">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="0e0ef-114">**Arresto** (4)</span><span class="sxs-lookup"><span data-stu-id="0e0ef-114">**Shut Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="0e0ef-115">**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="0e0ef-115">**Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="0e0ef-116">**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="0e0ef-116">**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="0e0ef-117">**Rinvio** (8)</span><span class="sxs-lookup"><span data-stu-id="0e0ef-117">**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="0e0ef-118">**Inattiva** (9)</span><span class="sxs-lookup"><span data-stu-id="0e0ef-118">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="0e0ef-119">**Riavvio** (10)</span><span class="sxs-lookup"><span data-stu-id="0e0ef-119">**Reboot** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="0e0ef-120">**Reimposta** (11)</span><span class="sxs-lookup"><span data-stu-id="0e0ef-120">**Reset** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="0e0ef-121">**DmTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="0e0ef-121">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="0e0ef-122">**Fornitore riservato** (32768..65535)</span><span class="sxs-lookup"><span data-stu-id="0e0ef-122">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="0e0ef-123">*Processo* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="0e0ef-123">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0e0ef-124">Può contenere un riferimento a [**CIM \_ ConcreteJob**](cim-concretejob.md) creato per tenere traccia della transizione di stato avviata dalla chiamata al metodo.</span><span class="sxs-lookup"><span data-stu-id="0e0ef-124">May contain a reference to the [**CIM\_ConcreteJob**](cim-concretejob.md) created to track the state transition initiated by the method invocation.</span></span>

</dd> <dt>

<span data-ttu-id="0e0ef-125">*TimeoutPeriod* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="0e0ef-125">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e0ef-126">Periodo di timeout che specifica la quantità massima di tempo prevista dal client per la transizione al nuovo stato.</span><span class="sxs-lookup"><span data-stu-id="0e0ef-126">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="0e0ef-127">Il formato dell'intervallo deve essere usato per specificare il periodo di timeout.</span><span class="sxs-lookup"><span data-stu-id="0e0ef-127">The interval format must be used to specify the timeout period.</span></span> <span data-ttu-id="0e0ef-128">Il valore 0 o **Null** indica che il client non ha requisiti di tempo per la transizione.</span><span class="sxs-lookup"><span data-stu-id="0e0ef-128">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="0e0ef-129">Se questa proprietà non contiene 0 o **Null** e l'implementazione non supporta questo parametro, deve essere restituito un codice restituito 4098 (Utilizzo del parametro di **timeout** non supportato).</span><span class="sxs-lookup"><span data-stu-id="0e0ef-129">If this property does not contain 0 or **Null** and the implementation does not support this parameter, a return code of 4098 (**Use Of Timeout Parameter Not Supported**) must be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e0ef-130">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0e0ef-130">Return value</span></span>

<span data-ttu-id="0e0ef-131">Questo metodo restituisce uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="0e0ef-131">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="0e0ef-132">**Completata senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="0e0ef-132">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0e0ef-133">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="0e0ef-133">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="0e0ef-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0e0ef-134">Requirements</span></span>



| <span data-ttu-id="0e0ef-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e0ef-135">Requirement</span></span> | <span data-ttu-id="0e0ef-136">Valore</span><span class="sxs-lookup"><span data-stu-id="0e0ef-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e0ef-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0e0ef-137">Minimum supported client</span></span><br/> | <span data-ttu-id="0e0ef-138">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="0e0ef-138">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="0e0ef-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0e0ef-139">Minimum supported server</span></span><br/> | <span data-ttu-id="0e0ef-140">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="0e0ef-140">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="0e0ef-141">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0e0ef-141">Namespace</span></span><br/>                | <span data-ttu-id="0e0ef-142">Virtualizzazione \\ radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="0e0ef-142">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="0e0ef-143">MOF</span><span class="sxs-lookup"><span data-stu-id="0e0ef-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0e0ef-144"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="0e0ef-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0e0ef-145">DLL</span><span class="sxs-lookup"><span data-stu-id="0e0ef-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e0ef-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0e0ef-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0e0ef-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0e0ef-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e0ef-148">**Msvm \_ EmulatedEthernetPort**</span><span class="sxs-lookup"><span data-stu-id="0e0ef-148">**Msvm\_EmulatedEthernetPort**</span></span>](msvm-emulatedethernetport.md)
</dt> </dl>

 

 




