---
description: 'Metodo RequestStateChange della classe Msvm_SyntheticEthernetPort : richiede una modifica dello stato.'
ms.assetid: 9aea3a8e-8b62-48c3-bbdb-49f24aeeca22
title: Metodo RequestStateChange della classe Msvm_SyntheticEthernetPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticEthernetPort.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 7a751ba40be7ddeb6d71f104036487dd8acb209a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108111309"
---
# <a name="requeststatechange-method-of-the-msvm_syntheticethernetport-class"></a><span data-ttu-id="2295e-103">Metodo RequestStateChange della classe Msvm \_ SyntheticEthernetPort</span><span class="sxs-lookup"><span data-stu-id="2295e-103">RequestStateChange method of the Msvm\_SyntheticEthernetPort class</span></span>

<span data-ttu-id="2295e-104">Richiede una modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="2295e-104">Requests a state change.</span></span>

## <a name="syntax"></a><span data-ttu-id="2295e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2295e-105">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="2295e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2295e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2295e-107">*RequestedState* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="2295e-107">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2295e-108">Nuovo stato.</span><span class="sxs-lookup"><span data-stu-id="2295e-108">The new state.</span></span> <span data-ttu-id="2295e-109">Le informazioni vengono inserite nella proprietà **RequestedState** dell'istanza se il codice restituito del metodo **RequestStateChange** è 0 (processo completato senza errori) o 4096 (processo avviato).</span><span class="sxs-lookup"><span data-stu-id="2295e-109">The info is placed in the **RequestedState** property of the instance if the return code of the **RequestStateChange** method is 0 (Job complete without error) or 4096 (Job started).</span></span> <span data-ttu-id="2295e-110">Per altre informazioni, vedi la descrizione delle **proprietà EnabledState** e **RequestedState** per l'elemento .</span><span class="sxs-lookup"><span data-stu-id="2295e-110">For more info, see the description of the **EnabledState** and **RequestedState** properties for the element.</span></span> <span data-ttu-id="2295e-111">Deve essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="2295e-111">This must be one of the following values.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="2295e-112">**Abilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="2295e-112">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="2295e-113">**Disabilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="2295e-113">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="2295e-114">**Arresta** (4)</span><span class="sxs-lookup"><span data-stu-id="2295e-114">**Shut Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="2295e-115">**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="2295e-115">**Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="2295e-116">**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="2295e-116">**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="2295e-117">**Rinvia** (8)</span><span class="sxs-lookup"><span data-stu-id="2295e-117">**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="2295e-118">**Inattiva** (9)</span><span class="sxs-lookup"><span data-stu-id="2295e-118">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="2295e-119">**Riavvio** (10)</span><span class="sxs-lookup"><span data-stu-id="2295e-119">**Reboot** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="2295e-120">**Reset** (11)</span><span class="sxs-lookup"><span data-stu-id="2295e-120">**Reset** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="2295e-121">**DmTF Reserved** (..)</span><span class="sxs-lookup"><span data-stu-id="2295e-121">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="2295e-122">**Vendor Reserved** (32768..65535)</span><span class="sxs-lookup"><span data-stu-id="2295e-122">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="2295e-123">*Processo* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="2295e-123">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2295e-124">Può contenere un riferimento al [**processo \_ concreto CIM**](cim-concretejob.md) creato per tenere traccia della transizione di stato avviata dalla chiamata al metodo.</span><span class="sxs-lookup"><span data-stu-id="2295e-124">May contain a reference to the [**CIM\_ConcreteJob**](cim-concretejob.md) created to track the state transition initiated by the method invocation.</span></span>

</dd> <dt>

<span data-ttu-id="2295e-125">*TimeoutPeriod* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="2295e-125">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2295e-126">Periodo di timeout che specifica la quantità massima di tempo prevista dal client per la transizione al nuovo stato.</span><span class="sxs-lookup"><span data-stu-id="2295e-126">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="2295e-127">Il formato dell'intervallo deve essere usato per specificare il periodo di timeout.</span><span class="sxs-lookup"><span data-stu-id="2295e-127">The interval format must be used to specify the timeout period.</span></span> <span data-ttu-id="2295e-128">Il valore 0 o **Null** indica che il client non ha requisiti di tempo per la transizione.</span><span class="sxs-lookup"><span data-stu-id="2295e-128">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="2295e-129">Se questa proprietà non contiene 0 o **Null** e l'implementazione non supporta questo parametro, deve essere restituito un codice restituito 4098 ( Utilizzo del parametro **di timeout** non supportato ).</span><span class="sxs-lookup"><span data-stu-id="2295e-129">If this property does not contain 0 or **Null** and the implementation does not support this parameter, a return code of 4098 (**Use Of Timeout Parameter Not Supported**) must be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2295e-130">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2295e-130">Return value</span></span>

<span data-ttu-id="2295e-131">Questo metodo restituisce uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="2295e-131">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="2295e-132">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="2295e-132">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2295e-133">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="2295e-133">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="2295e-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2295e-134">Requirements</span></span>



| <span data-ttu-id="2295e-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="2295e-135">Requirement</span></span> | <span data-ttu-id="2295e-136">Valore</span><span class="sxs-lookup"><span data-stu-id="2295e-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2295e-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2295e-137">Minimum supported client</span></span><br/> | <span data-ttu-id="2295e-138">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2295e-138">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="2295e-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2295e-139">Minimum supported server</span></span><br/> | <span data-ttu-id="2295e-140">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="2295e-140">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="2295e-141">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2295e-141">Namespace</span></span><br/>                | <span data-ttu-id="2295e-142">Virtualizzazione \\ radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="2295e-142">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="2295e-143">MOF</span><span class="sxs-lookup"><span data-stu-id="2295e-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2295e-144"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="2295e-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2295e-145">DLL</span><span class="sxs-lookup"><span data-stu-id="2295e-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2295e-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2295e-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2295e-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2295e-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2295e-148">**Msvm \_ SyntheticEthernetPort**</span><span class="sxs-lookup"><span data-stu-id="2295e-148">**Msvm\_SyntheticEthernetPort**</span></span>](msvm-syntheticethernetport.md)
</dt> </dl>

 

 




