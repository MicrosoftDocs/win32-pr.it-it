---
description: Richiede una modifica dello stato.
ms.assetid: d0a75ede-7f59-4464-abea-e5a84a7f16da
title: Metodo RequestStateChange della classe Msvm_TransparentBridgingService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TransparentBridgingService.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d4a549c12a825a96456df7844b947b0652caf277
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130326"
---
# <a name="requeststatechange-method-of-the-msvm_transparentbridgingservice-class"></a><span data-ttu-id="90a0c-103">Metodo RequestStateChange della classe MSVM \_ TransparentBridgingService</span><span class="sxs-lookup"><span data-stu-id="90a0c-103">RequestStateChange method of the Msvm\_TransparentBridgingService class</span></span>

<span data-ttu-id="90a0c-104">Richiede una modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="90a0c-104">Requests a state change.</span></span>

## <a name="syntax"></a><span data-ttu-id="90a0c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="90a0c-105">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="90a0c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="90a0c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90a0c-107">*RequestedState* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="90a0c-107">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90a0c-108">Nuovo stato.</span><span class="sxs-lookup"><span data-stu-id="90a0c-108">The new state.</span></span> <span data-ttu-id="90a0c-109">Le informazioni vengono inserite nella proprietà **RequestedState** dell'istanza se il codice restituito del metodo **RequestStateChange** è 0 (processo completato senza errori) o 4096 (processo avviato).</span><span class="sxs-lookup"><span data-stu-id="90a0c-109">The info is placed in the **RequestedState** property of the instance if the return code of the **RequestStateChange** method is 0 (Job complete without error) or 4096 (Job started).</span></span> <span data-ttu-id="90a0c-110">Per ulteriori informazioni, vedere la descrizione delle proprietà **EnabledState** e **RequestedState** per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="90a0c-110">For more info, see the description of the **EnabledState** and **RequestedState** properties for the element.</span></span> <span data-ttu-id="90a0c-111">Deve essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="90a0c-111">This must be one of the following values.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="90a0c-112">**Abilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="90a0c-112">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="90a0c-113">**Disabilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="90a0c-113">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="90a0c-114">**Arresto** (4)</span><span class="sxs-lookup"><span data-stu-id="90a0c-114">**Shut Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="90a0c-115">**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="90a0c-115">**Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="90a0c-116">**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="90a0c-116">**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="90a0c-117">**Rinvia** (8)</span><span class="sxs-lookup"><span data-stu-id="90a0c-117">**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="90a0c-118">**Mettere in stato** (9)</span><span class="sxs-lookup"><span data-stu-id="90a0c-118">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="90a0c-119">**Riavvio** (10)</span><span class="sxs-lookup"><span data-stu-id="90a0c-119">**Reboot** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="90a0c-120">**Reimposta** (11)</span><span class="sxs-lookup"><span data-stu-id="90a0c-120">**Reset** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="90a0c-121">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="90a0c-121">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="90a0c-122">**Fornitore riservato** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="90a0c-122">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="90a0c-123">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="90a0c-123">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="90a0c-124">Può contenere un riferimento al [**\_ ConcreteJob CIM**](cim-concretejob.md) creato per tenere traccia della transizione di stato iniziata dalla chiamata al metodo.</span><span class="sxs-lookup"><span data-stu-id="90a0c-124">May contain a reference to the [**CIM\_ConcreteJob**](cim-concretejob.md) created to track the state transition initiated by the method invocation.</span></span>

</dd> <dt>

<span data-ttu-id="90a0c-125">*TimeoutPeriod* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="90a0c-125">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90a0c-126">Periodo di timeout che specifica la quantità massima di tempo per cui il client prevede che la transizione al nuovo stato venga eseguita.</span><span class="sxs-lookup"><span data-stu-id="90a0c-126">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="90a0c-127">Per specificare il periodo di timeout, è necessario utilizzare il formato intervallo.</span><span class="sxs-lookup"><span data-stu-id="90a0c-127">The interval format must be used to specify the timeout period.</span></span> <span data-ttu-id="90a0c-128">Il valore 0 o **null** indica che il client non dispone di requisiti temporali per la transizione.</span><span class="sxs-lookup"><span data-stu-id="90a0c-128">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="90a0c-129">Se questa proprietà non contiene 0 o **null** e l'implementazione non supporta questo parametro, deve essere restituito un codice restituito 4098 (**utilizzo del parametro timeout non supportato**).</span><span class="sxs-lookup"><span data-stu-id="90a0c-129">If this property does not contain 0 or **Null** and the implementation does not support this parameter, a return code of 4098 (**Use Of Timeout Parameter Not Supported**) must be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90a0c-130">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="90a0c-130">Return value</span></span>

<span data-ttu-id="90a0c-131">Questo metodo restituisce uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="90a0c-131">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="90a0c-132">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="90a0c-132">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="90a0c-133">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="90a0c-133">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="90a0c-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="90a0c-134">Requirements</span></span>



| <span data-ttu-id="90a0c-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="90a0c-135">Requirement</span></span> | <span data-ttu-id="90a0c-136">Valore</span><span class="sxs-lookup"><span data-stu-id="90a0c-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90a0c-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="90a0c-137">Minimum supported client</span></span><br/> | <span data-ttu-id="90a0c-138">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="90a0c-138">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="90a0c-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="90a0c-139">Minimum supported server</span></span><br/> | <span data-ttu-id="90a0c-140">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="90a0c-140">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="90a0c-141">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="90a0c-141">Namespace</span></span><br/>                | <span data-ttu-id="90a0c-142">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="90a0c-142">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="90a0c-143">MOF</span><span class="sxs-lookup"><span data-stu-id="90a0c-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="90a0c-144"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="90a0c-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="90a0c-145">DLL</span><span class="sxs-lookup"><span data-stu-id="90a0c-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="90a0c-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="90a0c-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="90a0c-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="90a0c-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90a0c-148">**\_TransparentBridgingService MSVM**</span><span class="sxs-lookup"><span data-stu-id="90a0c-148">**Msvm\_TransparentBridgingService**</span></span>](msvm-transparentbridgingservice.md)
</dt> </dl>

 

 




