---
description: 'Metodo RequestStateChange della classe Msvm_ShutdownComponent : richiede una modifica dello stato.'
ms.assetid: bb1dea51-f9d6-4edc-8044-53380cc4d32e
title: Metodo RequestStateChange della classe Msvm_ShutdownComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ShutdownComponent.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 71237715f08e3775ff4c61660a789e000e4f5a5d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109609"
---
# <a name="requeststatechange-method-of-the-msvm_shutdowncomponent-class"></a><span data-ttu-id="71d69-103">Metodo RequestStateChange della classe Msvm \_ ShutdownComponent</span><span class="sxs-lookup"><span data-stu-id="71d69-103">RequestStateChange method of the Msvm\_ShutdownComponent class</span></span>

<span data-ttu-id="71d69-104">Richiede una modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="71d69-104">Requests a state change.</span></span>

## <a name="syntax"></a><span data-ttu-id="71d69-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="71d69-105">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="71d69-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="71d69-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71d69-107">*RequestedState* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="71d69-107">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71d69-108">Nuovo stato.</span><span class="sxs-lookup"><span data-stu-id="71d69-108">The new state.</span></span> <span data-ttu-id="71d69-109">Le informazioni vengono inserite nella **proprietà RequestedState** dell'istanza se il codice restituito del **metodo RequestStateChange** è 0 o 4096.</span><span class="sxs-lookup"><span data-stu-id="71d69-109">The info is placed in the **RequestedState** property of the instance if the return code of the **RequestStateChange** method is 0 or 4096.</span></span> <span data-ttu-id="71d69-110">Per altre informazioni, vedere la descrizione delle **proprietà EnabledState** e **RequestedState** per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="71d69-110">For more info, see the description of the **EnabledState** and **RequestedState** properties for the element.</span></span> <span data-ttu-id="71d69-111">Deve essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="71d69-111">This must be one of the following values.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="71d69-112">**Abilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="71d69-112">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="71d69-113">**Disabilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="71d69-113">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="71d69-114">**Arresto** (4)</span><span class="sxs-lookup"><span data-stu-id="71d69-114">**Shut Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="71d69-115">**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="71d69-115">**Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="71d69-116">**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="71d69-116">**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="71d69-117">**Rinvio** (8)</span><span class="sxs-lookup"><span data-stu-id="71d69-117">**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="71d69-118">**Inattiva** (9)</span><span class="sxs-lookup"><span data-stu-id="71d69-118">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="71d69-119">**Riavvio** (10)</span><span class="sxs-lookup"><span data-stu-id="71d69-119">**Reboot** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="71d69-120">**Reimposta** (11)</span><span class="sxs-lookup"><span data-stu-id="71d69-120">**Reset** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="71d69-121">**DmTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="71d69-121">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="71d69-122">**Fornitore riservato** (32768..65535)</span><span class="sxs-lookup"><span data-stu-id="71d69-122">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="71d69-123">*Processo* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="71d69-123">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="71d69-124">Può contenere un riferimento all'oggetto ConcreteJob creato per tenere traccia della transizione di stato avviata dalla chiamata al metodo.</span><span class="sxs-lookup"><span data-stu-id="71d69-124">May contain a reference to the ConcreteJob created to track the state transition initiated by the method invocation.</span></span>

</dd> <dt>

<span data-ttu-id="71d69-125">*TimeoutPeriod* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="71d69-125">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71d69-126">Periodo di timeout che specifica la quantità massima di tempo prevista dal client per la transizione al nuovo stato.</span><span class="sxs-lookup"><span data-stu-id="71d69-126">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="71d69-127">Il formato dell'intervallo deve essere usato per specificare TimeoutPeriod.</span><span class="sxs-lookup"><span data-stu-id="71d69-127">The interval format must be used to specify the TimeoutPeriod.</span></span> <span data-ttu-id="71d69-128">Il valore 0 o un parametro Null indica che il client non ha requisiti di tempo per la transizione.</span><span class="sxs-lookup"><span data-stu-id="71d69-128">A value of 0 or a null parameter indicates that the client has no time requirements for the transition.</span></span>

<span data-ttu-id="71d69-129">Se questa proprietà non contiene 0 o null e l'implementazione non supporta questo parametro, verrà restituito un codice restituito "Utilizzo del parametro di timeout non supportato".</span><span class="sxs-lookup"><span data-stu-id="71d69-129">If this property does not contain 0 or null and the implementation does not support this parameter, a return code of 'Use Of Timeout Parameter Not Supported' shall be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71d69-130">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="71d69-130">Return value</span></span>

<span data-ttu-id="71d69-131">Questo metodo restituisce uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="71d69-131">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="71d69-132">**Completata senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="71d69-132">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="71d69-133">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="71d69-133">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="71d69-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="71d69-134">Requirements</span></span>



| <span data-ttu-id="71d69-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="71d69-135">Requirement</span></span> | <span data-ttu-id="71d69-136">Valore</span><span class="sxs-lookup"><span data-stu-id="71d69-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71d69-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="71d69-137">Minimum supported client</span></span><br/> | <span data-ttu-id="71d69-138">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="71d69-138">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="71d69-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="71d69-139">Minimum supported server</span></span><br/> | <span data-ttu-id="71d69-140">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="71d69-140">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="71d69-141">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="71d69-141">Namespace</span></span><br/>                | <span data-ttu-id="71d69-142">Virtualizzazione \\ radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="71d69-142">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="71d69-143">MOF</span><span class="sxs-lookup"><span data-stu-id="71d69-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="71d69-144"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="71d69-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="71d69-145">DLL</span><span class="sxs-lookup"><span data-stu-id="71d69-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71d69-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="71d69-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="71d69-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="71d69-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71d69-148">**Msvm \_ ShutdownComponent**</span><span class="sxs-lookup"><span data-stu-id="71d69-148">**Msvm\_ShutdownComponent**</span></span>](msvm-shutdowncomponent.md)
</dt> </dl>

 

 




