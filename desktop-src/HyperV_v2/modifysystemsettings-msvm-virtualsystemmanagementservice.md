---
description: Modifica le impostazioni della macchina virtuale.
ms.assetid: 3266bd0d-398b-4d3b-9248-e29c069aab11
title: Metodo ModifySystemSettings della classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ModifySystemSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4e6bf40b3dd206affcdc014e98554bfa8f88b4c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315488"
---
# <a name="modifysystemsettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="59f78-103">Metodo ModifySystemSettings della classe MSVM \_ VirtualSystemManagementService</span><span class="sxs-lookup"><span data-stu-id="59f78-103">ModifySystemSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="59f78-104">Modifica le impostazioni della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="59f78-104">Modifies virtual machine settings.</span></span> <span data-ttu-id="59f78-105">Quando viene applicata alle impostazioni di sistema di una configurazione di macchina virtuale "corrente", come effetto collaterale è possibile che l'istanza della macchina virtuale venga modificata.</span><span class="sxs-lookup"><span data-stu-id="59f78-105">When applied to the system settings of a "current" virtual machine configuration, as a side effect the virtual machine instance may be modified.</span></span>

## <a name="syntax"></a><span data-ttu-id="59f78-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="59f78-106">Syntax</span></span>


```mof
uint32 ModifySystemSettings(
  [in]  string              SystemSettings,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="59f78-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="59f78-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59f78-108">*SystemSettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="59f78-108">*SystemSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59f78-109">Istanza incorporata della classe [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) che contiene gli aspetti modificati della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="59f78-109">An embedded instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class that contains the modified aspects of the virtual machine.</span></span> <span data-ttu-id="59f78-110">La proprietà **InstanceID** identifica l'impostazione della macchina virtuale da modificare.</span><span class="sxs-lookup"><span data-stu-id="59f78-110">The **InstanceID** property identifies the virtual machine setting to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="59f78-111">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="59f78-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="59f78-112">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="59f78-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59f78-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="59f78-113">Return value</span></span>

<span data-ttu-id="59f78-114">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="59f78-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="59f78-115">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="59f78-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="59f78-116">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="59f78-116">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="59f78-117">**Non riuscito** (2)</span><span class="sxs-lookup"><span data-stu-id="59f78-117">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="59f78-118">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="59f78-118">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="59f78-119">**Parametro non valido** (4)</span><span class="sxs-lookup"><span data-stu-id="59f78-119">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="59f78-120">**Stato non valido** (5)</span><span class="sxs-lookup"><span data-stu-id="59f78-120">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="59f78-121">**Parametri incompatibili** (6)</span><span class="sxs-lookup"><span data-stu-id="59f78-121">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="59f78-122">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="59f78-122">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="59f78-123">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="59f78-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="59f78-124">**Metodo riservato** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="59f78-124">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="59f78-125">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="59f78-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="59f78-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="59f78-126">Requirements</span></span>



| <span data-ttu-id="59f78-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="59f78-127">Requirement</span></span> | <span data-ttu-id="59f78-128">Valore</span><span class="sxs-lookup"><span data-stu-id="59f78-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59f78-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="59f78-129">Minimum supported client</span></span><br/> | <span data-ttu-id="59f78-130">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="59f78-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="59f78-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="59f78-131">Minimum supported server</span></span><br/> | <span data-ttu-id="59f78-132">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="59f78-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="59f78-133">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="59f78-133">Namespace</span></span><br/>                | <span data-ttu-id="59f78-134">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="59f78-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="59f78-135">MOF</span><span class="sxs-lookup"><span data-stu-id="59f78-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="59f78-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="59f78-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="59f78-137">DLL</span><span class="sxs-lookup"><span data-stu-id="59f78-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="59f78-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="59f78-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="59f78-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="59f78-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59f78-140">**ModifyVirtualSystem (V1)**</span><span class="sxs-lookup"><span data-stu-id="59f78-140">**ModifyVirtualSystem (V1)**</span></span>](/previous-versions/windows/desktop/virtual/modifyvirtualsystem-msvm-virtualsystemmanagementservice)
</dt> <dt>

[<span data-ttu-id="59f78-141">**\_VirtualSystemManagementService MSVM**</span><span class="sxs-lookup"><span data-stu-id="59f78-141">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

