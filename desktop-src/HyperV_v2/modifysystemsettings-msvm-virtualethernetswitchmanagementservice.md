---
description: Modifica le impostazioni del Commuter virtuale.
ms.assetid: 8d323578-990f-483c-8515-8a21479767b1
title: Metodo ModifySystemSettings della classe Msvm_VirtualEthernetSwitchManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService.ModifySystemSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 3512debfd6d49e3c09cb8a508a7f0d748ab128e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315490"
---
# <a name="modifysystemsettings-method-of-the-msvm_virtualethernetswitchmanagementservice-class"></a><span data-ttu-id="1ca02-103">Metodo ModifySystemSettings della classe MSVM \_ VirtualEthernetSwitchManagementService</span><span class="sxs-lookup"><span data-stu-id="1ca02-103">ModifySystemSettings method of the Msvm\_VirtualEthernetSwitchManagementService class</span></span>

<span data-ttu-id="1ca02-104">Modifica le impostazioni del Commuter virtuale.</span><span class="sxs-lookup"><span data-stu-id="1ca02-104">Modifies virtual switch settings.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ca02-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1ca02-105">Syntax</span></span>


```mof
uint32 ModifySystemSettings(
  [in]  string              SystemSettings,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="1ca02-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1ca02-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ca02-107">*SystemSettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1ca02-107">*SystemSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ca02-108">Istanza incorporata della classe [**MSVM \_ VirtualEthernetSwitchSettingData**](msvm-virtualethernetswitchsettingdata.md) che contiene gli aspetti modificati del commutatore virtuale.</span><span class="sxs-lookup"><span data-stu-id="1ca02-108">An embedded instance of the [**Msvm\_VirtualEthernetSwitchSettingData**](msvm-virtualethernetswitchsettingdata.md) class that contains the modified aspects of the virtual switch.</span></span> <span data-ttu-id="1ca02-109">La proprietà **InstanceID** identifica l'impostazione del commutatore virtuale da modificare.</span><span class="sxs-lookup"><span data-stu-id="1ca02-109">The **InstanceID** property identifies the virtual switch setting to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="1ca02-110">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="1ca02-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1ca02-111">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1ca02-111">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ca02-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1ca02-112">Return value</span></span>

<span data-ttu-id="1ca02-113">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="1ca02-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="1ca02-114">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="1ca02-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1ca02-115">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="1ca02-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1ca02-116">**Non riuscito** (2)</span><span class="sxs-lookup"><span data-stu-id="1ca02-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1ca02-117">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="1ca02-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1ca02-118">**Parametro non valido** (4)</span><span class="sxs-lookup"><span data-stu-id="1ca02-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="1ca02-119">**Stato non valido** (5)</span><span class="sxs-lookup"><span data-stu-id="1ca02-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="1ca02-120">**Parametri incompatibili** (6)</span><span class="sxs-lookup"><span data-stu-id="1ca02-120">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="1ca02-121">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="1ca02-121">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="1ca02-122">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="1ca02-122">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="1ca02-123">**Metodo riservato** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="1ca02-123">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="1ca02-124">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="1ca02-124">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="1ca02-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1ca02-125">Requirements</span></span>



| <span data-ttu-id="1ca02-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ca02-126">Requirement</span></span> | <span data-ttu-id="1ca02-127">Valore</span><span class="sxs-lookup"><span data-stu-id="1ca02-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ca02-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1ca02-128">Minimum supported client</span></span><br/> | <span data-ttu-id="1ca02-129">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="1ca02-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="1ca02-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1ca02-130">Minimum supported server</span></span><br/> | <span data-ttu-id="1ca02-131">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="1ca02-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1ca02-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1ca02-132">Namespace</span></span><br/>                | <span data-ttu-id="1ca02-133">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="1ca02-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="1ca02-134">MOF</span><span class="sxs-lookup"><span data-stu-id="1ca02-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1ca02-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1ca02-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1ca02-136">DLL</span><span class="sxs-lookup"><span data-stu-id="1ca02-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1ca02-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1ca02-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1ca02-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1ca02-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ca02-139">**\_VirtualEthernetSwitchManagementService MSVM**</span><span class="sxs-lookup"><span data-stu-id="1ca02-139">**Msvm\_VirtualEthernetSwitchManagementService**</span></span>](msvm-virtualethernetswitchmanagementservice.md)
</dt> </dl>

 

