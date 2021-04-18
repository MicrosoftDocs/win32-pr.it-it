---
description: Richiede una modifica dello stato.
ms.assetid: 9dfa96b1-19d4-42ea-b927-80b0d63a9be1
title: Metodo RequestStateChange della classe Msvm_DiskDrive
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DiskDrive.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2de09b7f5ca7e212098f1299f597bf670e5a2970
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314333"
---
# <a name="requeststatechange-method-of-the-msvm_diskdrive-class"></a><span data-ttu-id="ffda1-103">Metodo RequestStateChange della classe MSVM \_ DiskDrive</span><span class="sxs-lookup"><span data-stu-id="ffda1-103">RequestStateChange method of the Msvm\_DiskDrive class</span></span>

<span data-ttu-id="ffda1-104">Richiede una modifica dello stato.</span><span class="sxs-lookup"><span data-stu-id="ffda1-104">Requests a state change.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffda1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ffda1-105">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="ffda1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ffda1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ffda1-107">*RequestedState* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ffda1-107">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ffda1-108">Stato richiesto per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="ffda1-108">The state requested for the element.</span></span> <span data-ttu-id="ffda1-109">Queste informazioni verranno inserite nella proprietà RequestedState dell'istanza se il codice restituito del metodo RequestStateChange è 0 (' completed with no error ') o 4096 (0x1000) (' job Started ').</span><span class="sxs-lookup"><span data-stu-id="ffda1-109">This information will be placed into the RequestedState property of the instance if the return code of the RequestStateChange method is 0 ('Completed with No Error'), or 4096 (0x1000) ('Job Started').</span></span> <span data-ttu-id="ffda1-110">Per una spiegazione dettagliata dei valori di RequestedState, vedere la descrizione delle proprietà EnabledState e RequestedState.</span><span class="sxs-lookup"><span data-stu-id="ffda1-110">Refer to the description of the EnabledState and RequestedState properties for the detailed explanations of the RequestedState values.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="ffda1-111">**Abilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="ffda1-111">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="ffda1-112">**Disabilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="ffda1-112">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="ffda1-113">**Arresto** (4)</span><span class="sxs-lookup"><span data-stu-id="ffda1-113">**Shut Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="ffda1-114">**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="ffda1-114">**Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="ffda1-115">**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="ffda1-115">**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="ffda1-116">**Rinvia** (8)</span><span class="sxs-lookup"><span data-stu-id="ffda1-116">**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="ffda1-117">**Mettere in stato** (9)</span><span class="sxs-lookup"><span data-stu-id="ffda1-117">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="ffda1-118">**Riavvio** (10)</span><span class="sxs-lookup"><span data-stu-id="ffda1-118">**Reboot** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="ffda1-119">**Reimposta** (11)</span><span class="sxs-lookup"><span data-stu-id="ffda1-119">**Reset** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="ffda1-120">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="ffda1-120">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="ffda1-121">**Fornitore riservato** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="ffda1-121">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="ffda1-122">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="ffda1-122">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ffda1-123">Può contenere un riferimento al ConcreteJob creato per tenere traccia della transizione di stato iniziata dalla chiamata al metodo.</span><span class="sxs-lookup"><span data-stu-id="ffda1-123">May contain a reference to the ConcreteJob created to track the state transition initiated by the method invocation.</span></span>

</dd> <dt>

<span data-ttu-id="ffda1-124">*TimeoutPeriod* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ffda1-124">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ffda1-125">Periodo di timeout che specifica la quantità massima di tempo per cui il client prevede che la transizione al nuovo stato venga eseguita.</span><span class="sxs-lookup"><span data-stu-id="ffda1-125">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="ffda1-126">Per specificare TimeoutPeriod, è necessario utilizzare il formato intervallo.</span><span class="sxs-lookup"><span data-stu-id="ffda1-126">The interval format must be used to specify the TimeoutPeriod.</span></span> <span data-ttu-id="ffda1-127">Il valore 0 o un parametro null indica che il client non dispone di requisiti temporali per la transizione.</span><span class="sxs-lookup"><span data-stu-id="ffda1-127">A value of 0 or a null parameter indicates that the client has no time requirements for the transition.</span></span>

<span data-ttu-id="ffda1-128">Se questa proprietà non contiene 0 o null e l'implementazione non supporta questo parametro, verrà restituito un codice restituito ' use of timeout parameter not supported '.</span><span class="sxs-lookup"><span data-stu-id="ffda1-128">If this property does not contain 0 or null and the implementation does not support this parameter, a return code of 'Use Of Timeout Parameter Not Supported' shall be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ffda1-129">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ffda1-129">Return value</span></span>

<span data-ttu-id="ffda1-130">Questo metodo restituisce uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="ffda1-130">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="ffda1-131">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="ffda1-131">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ffda1-132">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="ffda1-132">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="ffda1-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ffda1-133">Requirements</span></span>



| <span data-ttu-id="ffda1-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="ffda1-134">Requirement</span></span> | <span data-ttu-id="ffda1-135">Valore</span><span class="sxs-lookup"><span data-stu-id="ffda1-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffda1-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ffda1-136">Minimum supported client</span></span><br/> | <span data-ttu-id="ffda1-137">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="ffda1-137">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="ffda1-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ffda1-138">Minimum supported server</span></span><br/> | <span data-ttu-id="ffda1-139">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="ffda1-139">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="ffda1-140">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ffda1-140">Namespace</span></span><br/>                | <span data-ttu-id="ffda1-141">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="ffda1-141">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ffda1-142">MOF</span><span class="sxs-lookup"><span data-stu-id="ffda1-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ffda1-143"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ffda1-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ffda1-144">DLL</span><span class="sxs-lookup"><span data-stu-id="ffda1-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ffda1-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ffda1-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ffda1-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ffda1-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffda1-147">**\_DiskDrive MSVM**</span><span class="sxs-lookup"><span data-stu-id="ffda1-147">**Msvm\_DiskDrive**</span></span>](msvm-diskdrive.md)
</dt> </dl>

 

 




