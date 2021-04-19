---
description: Richiede che lo stato del sistema pianificato venga modificato nel valore specificato.
ms.assetid: 54ed9514-4f09-458e-8e86-a807ee66df17
title: Metodo RequestStateChange della classe Msvm_PlannedComputerSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_PlannedComputerSystem.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 172ec383473510a30ccde66b2617e8ef02ffdb72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311778"
---
# <a name="requeststatechange-method-of-the-msvm_plannedcomputersystem-class"></a><span data-ttu-id="73ae8-103">Metodo RequestStateChange della classe MSVM \_ PlannedComputerSystem</span><span class="sxs-lookup"><span data-stu-id="73ae8-103">RequestStateChange method of the Msvm\_PlannedComputerSystem class</span></span>

<span data-ttu-id="73ae8-104">Richiede che lo stato del sistema pianificato venga modificato nel valore specificato.</span><span class="sxs-lookup"><span data-stu-id="73ae8-104">Requests that the state of the planned system be changed to the value specified.</span></span>

## <a name="syntax"></a><span data-ttu-id="73ae8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="73ae8-105">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="73ae8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="73ae8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73ae8-107">*RequestedState* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="73ae8-107">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73ae8-108">Stato richiesto per il sistema pianificato.</span><span class="sxs-lookup"><span data-stu-id="73ae8-108">The requested state for the planned system.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="73ae8-109">**Abilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="73ae8-109">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="73ae8-110">**Disabilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="73ae8-110">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="73ae8-111">**Arresto** (4)</span><span class="sxs-lookup"><span data-stu-id="73ae8-111">**Shut Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="73ae8-112">**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="73ae8-112">**Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="73ae8-113">**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="73ae8-113">**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="73ae8-114">**Rinvia** (8)</span><span class="sxs-lookup"><span data-stu-id="73ae8-114">**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="73ae8-115">**Mettere in stato** (9)</span><span class="sxs-lookup"><span data-stu-id="73ae8-115">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="73ae8-116">**Riavvio** (10)</span><span class="sxs-lookup"><span data-stu-id="73ae8-116">**Reboot** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="73ae8-117">**Reimposta** (11)</span><span class="sxs-lookup"><span data-stu-id="73ae8-117">**Reset** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="73ae8-118">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="73ae8-118">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="73ae8-119">**Fornitore riservato** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="73ae8-119">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="73ae8-120">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="73ae8-120">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="73ae8-121">Questo parametro non viene utilizzato e deve essere **null**.</span><span class="sxs-lookup"><span data-stu-id="73ae8-121">This parameter is not used and should be **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="73ae8-122">*TimeoutPeriod* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="73ae8-122">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73ae8-123">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="73ae8-123">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73ae8-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="73ae8-124">Return value</span></span>

<span data-ttu-id="73ae8-125">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="73ae8-125">This method returns one of the following values.</span></span>



| <span data-ttu-id="73ae8-126">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="73ae8-126">Return code/value</span></span>                                                                                                                      | <span data-ttu-id="73ae8-127">Descrizione</span><span class="sxs-lookup"><span data-stu-id="73ae8-127">Description</span></span>                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="73ae8-128"><dt></dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="73ae8-128"><dt></dt> <dt>0</dt></span></span> </dl>     | <span data-ttu-id="73ae8-129">Operazione riuscita</span><span class="sxs-lookup"><span data-stu-id="73ae8-129">Success</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="73ae8-130"><dt></dt><dt>4096</dt></span><span class="sxs-lookup"><span data-stu-id="73ae8-130"><dt></dt> <dt>4096</dt></span></span> </dl>  |                                                                                    |
| <dl> <span data-ttu-id="73ae8-131"><dt></dt><dt>32768</dt></span><span class="sxs-lookup"><span data-stu-id="73ae8-131"><dt></dt> <dt>32768</dt></span></span> </dl> |                                                                                    |
| <dl> <span data-ttu-id="73ae8-132"><dt></dt><dt>32769</dt></span><span class="sxs-lookup"><span data-stu-id="73ae8-132"><dt></dt> <dt>32769</dt></span></span> </dl> | <span data-ttu-id="73ae8-133">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="73ae8-133">Access denied.</span></span><br/>                                                          |
| <dl> <span data-ttu-id="73ae8-134"><dt></dt><dt>32770</dt></span><span class="sxs-lookup"><span data-stu-id="73ae8-134"><dt></dt> <dt>32770</dt></span></span> </dl> |                                                                                    |
| <dl> <span data-ttu-id="73ae8-135"><dt></dt><dt>32771</dt></span><span class="sxs-lookup"><span data-stu-id="73ae8-135"><dt></dt> <dt>32771</dt></span></span> </dl> |                                                                                    |
| <dl> <span data-ttu-id="73ae8-136"><dt></dt><dt>32772</dt></span><span class="sxs-lookup"><span data-stu-id="73ae8-136"><dt></dt> <dt>32772</dt></span></span> </dl> |                                                                                    |
| <dl> <span data-ttu-id="73ae8-137"><dt></dt><dt>32773</dt></span><span class="sxs-lookup"><span data-stu-id="73ae8-137"><dt></dt> <dt>32773</dt></span></span> </dl> |                                                                                    |
| <dl> <span data-ttu-id="73ae8-138"><dt></dt><dt>32774</dt></span><span class="sxs-lookup"><span data-stu-id="73ae8-138"><dt></dt> <dt>32774</dt></span></span> </dl> |                                                                                    |
| <dl> <span data-ttu-id="73ae8-139"><dt></dt><dt>32775</dt></span><span class="sxs-lookup"><span data-stu-id="73ae8-139"><dt></dt> <dt>32775</dt></span></span> </dl> | <span data-ttu-id="73ae8-140">Il valore specificato nel parametro *RequestedState* non è supportato.</span><span class="sxs-lookup"><span data-stu-id="73ae8-140">The value specified in the *RequestedState* parameter is not supported.</span></span><br/> |
| <dl> <span data-ttu-id="73ae8-141"><dt></dt><dt>32776</dt></span><span class="sxs-lookup"><span data-stu-id="73ae8-141"><dt></dt> <dt>32776</dt></span></span> </dl> |                                                                                    |
| <dl> <span data-ttu-id="73ae8-142"><dt></dt><dt>32777</dt></span><span class="sxs-lookup"><span data-stu-id="73ae8-142"><dt></dt> <dt>32777</dt></span></span> </dl> |                                                                                    |
| <dl> <span data-ttu-id="73ae8-143"><dt></dt><dt>32778</dt></span><span class="sxs-lookup"><span data-stu-id="73ae8-143"><dt></dt> <dt>32778</dt></span></span> </dl> |                                                                                    |



 

## <a name="requirements"></a><span data-ttu-id="73ae8-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="73ae8-144">Requirements</span></span>



| <span data-ttu-id="73ae8-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="73ae8-145">Requirement</span></span> | <span data-ttu-id="73ae8-146">Valore</span><span class="sxs-lookup"><span data-stu-id="73ae8-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73ae8-147">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="73ae8-147">Minimum supported client</span></span><br/> | <span data-ttu-id="73ae8-148">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="73ae8-148">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="73ae8-149">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="73ae8-149">Minimum supported server</span></span><br/> | <span data-ttu-id="73ae8-150">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="73ae8-150">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="73ae8-151">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="73ae8-151">Namespace</span></span><br/>                | <span data-ttu-id="73ae8-152">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="73ae8-152">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="73ae8-153">MOF</span><span class="sxs-lookup"><span data-stu-id="73ae8-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="73ae8-154"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="73ae8-154"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="73ae8-155">DLL</span><span class="sxs-lookup"><span data-stu-id="73ae8-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="73ae8-156"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="73ae8-156"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="73ae8-157">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="73ae8-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73ae8-158">**\_PlannedComputerSystem MSVM**</span><span class="sxs-lookup"><span data-stu-id="73ae8-158">**Msvm\_PlannedComputerSystem**</span></span>](msvm-plannedcomputersystem.md)
</dt> </dl>

 

 




