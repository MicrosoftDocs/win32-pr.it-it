---
description: Modifica le impostazioni delle risorse per un commutire virtuale.
ms.assetid: 1ae2456f-921c-4ea6-b3fb-7065110063fb
title: Metodo ModifyResourceSettings della classe Msvm_VirtualEthernetSwitchManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService.ModifyResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f40044b20389914281ad4f651019f3e8dc6b6148
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315491"
---
# <a name="modifyresourcesettings-method-of-the-msvm_virtualethernetswitchmanagementservice-class"></a><span data-ttu-id="1d078-103">Metodo ModifyResourceSettings della classe MSVM \_ VirtualEthernetSwitchManagementService</span><span class="sxs-lookup"><span data-stu-id="1d078-103">ModifyResourceSettings method of the Msvm\_VirtualEthernetSwitchManagementService class</span></span>

<span data-ttu-id="1d078-104">Modifica le impostazioni delle risorse per un commutire virtuale.</span><span class="sxs-lookup"><span data-stu-id="1d078-104">Modifies resource settings for a virtual switch.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d078-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1d078-105">Syntax</span></span>


```mof
uint32 ModifyResourceSettings(
  [in]  string                                ResourceSettings[],
  [out] CIM_ResourceAllocationSettingData REF ResultingResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="1d078-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1d078-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d078-107">*ResourceSettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1d078-107">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d078-108">Matrice di stringhe che contengono un'istanza incorporata di una classe derivata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), che contiene gli aspetti modificati delle risorse virtuali esistenti.</span><span class="sxs-lookup"><span data-stu-id="1d078-108">An array of strings that contain an embedded instance of a class derived from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), that contain the modified aspects of existing virtual resources.</span></span> <span data-ttu-id="1d078-109">La proprietà **InstanceID** di ogni istanza identifica l'impostazione della risorsa virtuale da modificare.</span><span class="sxs-lookup"><span data-stu-id="1d078-109">The **InstanceID** property of each instance identifies the virtual resource setting to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="1d078-110">*ResultingResourceSettings* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="1d078-110">*ResultingResourceSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1d078-111">Matrice di riferimenti a istanze di oggetti derivati [**da \_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) che rappresentano gli aspetti virtuali delle risorse virtuali modificate.</span><span class="sxs-lookup"><span data-stu-id="1d078-111">An array of references to instances of objects derived from [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) representing virtual aspects of the modified virtual resources.</span></span>

</dd> <dt>

<span data-ttu-id="1d078-112">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="1d078-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1d078-113">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1d078-113">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d078-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1d078-114">Return value</span></span>

<span data-ttu-id="1d078-115">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="1d078-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="1d078-116">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="1d078-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1d078-117">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="1d078-117">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1d078-118">**Non riuscito** (2)</span><span class="sxs-lookup"><span data-stu-id="1d078-118">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1d078-119">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="1d078-119">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1d078-120">**Parametro non valido** (4)</span><span class="sxs-lookup"><span data-stu-id="1d078-120">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="1d078-121">**Stato non valido** (5)</span><span class="sxs-lookup"><span data-stu-id="1d078-121">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="1d078-122">**Parametri incompatibili** (6)</span><span class="sxs-lookup"><span data-stu-id="1d078-122">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="1d078-123">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="1d078-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="1d078-124">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="1d078-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="1d078-125">**Metodo riservato** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="1d078-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="1d078-126">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="1d078-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="1d078-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1d078-127">Requirements</span></span>



| <span data-ttu-id="1d078-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d078-128">Requirement</span></span> | <span data-ttu-id="1d078-129">Valore</span><span class="sxs-lookup"><span data-stu-id="1d078-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d078-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1d078-130">Minimum supported client</span></span><br/> | <span data-ttu-id="1d078-131">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="1d078-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="1d078-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1d078-132">Minimum supported server</span></span><br/> | <span data-ttu-id="1d078-133">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="1d078-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1d078-134">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1d078-134">Namespace</span></span><br/>                | <span data-ttu-id="1d078-135">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="1d078-135">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="1d078-136">MOF</span><span class="sxs-lookup"><span data-stu-id="1d078-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1d078-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1d078-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1d078-138">DLL</span><span class="sxs-lookup"><span data-stu-id="1d078-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d078-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1d078-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1d078-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1d078-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d078-141">**AddResourceSettings**</span><span class="sxs-lookup"><span data-stu-id="1d078-141">**AddResourceSettings**</span></span>](addresourcesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[<span data-ttu-id="1d078-142">**RemoveResourceSettings**</span><span class="sxs-lookup"><span data-stu-id="1d078-142">**RemoveResourceSettings**</span></span>](removeresourcesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[<span data-ttu-id="1d078-143">**\_VirtualEthernetSwitchManagementService MSVM**</span><span class="sxs-lookup"><span data-stu-id="1d078-143">**Msvm\_VirtualEthernetSwitchManagementService**</span></span>](msvm-virtualethernetswitchmanagementservice.md)
</dt> </dl>

 

