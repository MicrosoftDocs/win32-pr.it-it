---
description: Aggiunge risorse a una configurazione di Commuter virtuale.
ms.assetid: aad5fac1-3884-4a95-abe3-bf192f23ea41
title: Metodo AddResourceSettings della classe Msvm_VirtualEthernetSwitchManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService.AddResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: cc29376a03403949c57b831f40b2437ced30a51a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312340"
---
# <a name="addresourcesettings-method-of-the-msvm_virtualethernetswitchmanagementservice-class"></a><span data-ttu-id="84c48-103">Metodo AddResourceSettings della classe MSVM \_ VirtualEthernetSwitchManagementService</span><span class="sxs-lookup"><span data-stu-id="84c48-103">AddResourceSettings method of the Msvm\_VirtualEthernetSwitchManagementService class</span></span>

<span data-ttu-id="84c48-104">Aggiunge risorse a una configurazione di Commuter virtuale.</span><span class="sxs-lookup"><span data-stu-id="84c48-104">Adds resources to a virtual switch configuration.</span></span> <span data-ttu-id="84c48-105">Quando viene applicato a una configurazione di macchina virtuale "stato", le risorse degli effetti collaterali vengono aggiunte alla macchina virtuale attiva.</span><span class="sxs-lookup"><span data-stu-id="84c48-105">When applied to a "state" virtual machine configuration, as a side effect resources are added to the active virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="84c48-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="84c48-106">Syntax</span></span>


```mof
uint32 AddResourceSettings(
  [in]  CIM_VirtualSystemSettingData      REF AffectedConfiguration,
  [in]  string                                ResourceSettings[],
  [out] CIM_ResourceAllocationSettingData REF ResultingResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="84c48-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="84c48-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84c48-108">*AffectedConfiguration* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="84c48-108">*AffectedConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84c48-109">Riferimento a un oggetto [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)) che rappresenta la configurazione del Commuter virtuale interessata.</span><span class="sxs-lookup"><span data-stu-id="84c48-109">A reference to a [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) object that represents the affected virtual switch configuration.</span></span>

</dd> <dt>

<span data-ttu-id="84c48-110">*ResourceSettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="84c48-110">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84c48-111">Matrice di stringhe che contengono un'istanza incorporata della classe [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) che descrive gli aspetti virtuali di una risorsa virtuale da aggiungere al Commuter virtuale.</span><span class="sxs-lookup"><span data-stu-id="84c48-111">An array of strings that contain one embedded instance of the [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) class that describes the virtual aspects of a virtual resource to be added to the virtual switch.</span></span>

</dd> <dt>

<span data-ttu-id="84c48-112">*ResultingResourceSettings* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="84c48-112">*ResultingResourceSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="84c48-113">Matrice di riferimenti a istanze della classe [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) che rappresenta gli aspetti virtuali delle risorse virtuali aggiunte.</span><span class="sxs-lookup"><span data-stu-id="84c48-113">An array of references to instances of the [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) class that represents virtual aspects of the added virtual resources.</span></span>

</dd> <dt>

<span data-ttu-id="84c48-114">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="84c48-114">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="84c48-115">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="84c48-115">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84c48-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="84c48-116">Return value</span></span>

<span data-ttu-id="84c48-117">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="84c48-117">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="84c48-118">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="84c48-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="84c48-119">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="84c48-119">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="84c48-120">**Non riuscito** (2)</span><span class="sxs-lookup"><span data-stu-id="84c48-120">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="84c48-121">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="84c48-121">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="84c48-122">**Parametro non valido** (4)</span><span class="sxs-lookup"><span data-stu-id="84c48-122">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="84c48-123">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="84c48-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="84c48-124">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="84c48-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="84c48-125">**Metodo riservato** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="84c48-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="84c48-126">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="84c48-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="84c48-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="84c48-127">Requirements</span></span>



| <span data-ttu-id="84c48-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="84c48-128">Requirement</span></span> | <span data-ttu-id="84c48-129">Valore</span><span class="sxs-lookup"><span data-stu-id="84c48-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84c48-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="84c48-130">Minimum supported client</span></span><br/> | <span data-ttu-id="84c48-131">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="84c48-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="84c48-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="84c48-132">Minimum supported server</span></span><br/> | <span data-ttu-id="84c48-133">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="84c48-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="84c48-134">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="84c48-134">Namespace</span></span><br/>                | <span data-ttu-id="84c48-135">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="84c48-135">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="84c48-136">MOF</span><span class="sxs-lookup"><span data-stu-id="84c48-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="84c48-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="84c48-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="84c48-138">DLL</span><span class="sxs-lookup"><span data-stu-id="84c48-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84c48-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="84c48-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="84c48-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="84c48-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84c48-141">**ModifyResourceSettings**</span><span class="sxs-lookup"><span data-stu-id="84c48-141">**ModifyResourceSettings**</span></span>](modifyresourcesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[<span data-ttu-id="84c48-142">**RemoveResourceSettings**</span><span class="sxs-lookup"><span data-stu-id="84c48-142">**RemoveResourceSettings**</span></span>](removeresourcesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[<span data-ttu-id="84c48-143">**\_VirtualEthernetSwitchManagementService MSVM**</span><span class="sxs-lookup"><span data-stu-id="84c48-143">**Msvm\_VirtualEthernetSwitchManagementService**</span></span>](msvm-virtualethernetswitchmanagementservice.md)
</dt> </dl>

 

