---
description: Rimuove le impostazioni delle risorse virtuali da una configurazione di commutiri virtuali.
ms.assetid: 9992ebcd-8891-42ef-be7e-154f336e37f8
title: Metodo RemoveResourceSettings della classe Msvm_VirtualEthernetSwitchManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService.RemoveResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9e82117b14ab9975b069e5b340ba9ec504ae65ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049563"
---
# <a name="removeresourcesettings-method-of-the-msvm_virtualethernetswitchmanagementservice-class"></a><span data-ttu-id="2f2e9-103">Metodo RemoveResourceSettings della classe MSVM \_ VirtualEthernetSwitchManagementService</span><span class="sxs-lookup"><span data-stu-id="2f2e9-103">RemoveResourceSettings method of the Msvm\_VirtualEthernetSwitchManagementService class</span></span>

<span data-ttu-id="2f2e9-104">Rimuove le impostazioni delle risorse virtuali da una configurazione di commutiri virtuali.</span><span class="sxs-lookup"><span data-stu-id="2f2e9-104">Removes virtual resource settings from a virtual switch configuration.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f2e9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2f2e9-105">Syntax</span></span>


```mof
uint32 RemoveResourceSettings(
  [in]  CIM_ResourceAllocationSettingData REF ResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="2f2e9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2f2e9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f2e9-107">*ResourceSettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2f2e9-107">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f2e9-108">Matrice di riferimenti a istanze della classe [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) , in cui ogni istanza rappresenta le impostazioni di una risorsa virtuale all'interno di una configurazione di Commuter virtuale da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="2f2e9-108">An array of references to instances of the [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) class, where each instance represents the settings of a virtual resource within a virtual switch configuration that are to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="2f2e9-109">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="2f2e9-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2f2e9-110">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2f2e9-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f2e9-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2f2e9-111">Return value</span></span>

<span data-ttu-id="2f2e9-112">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="2f2e9-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="2f2e9-113">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="2f2e9-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2f2e9-114">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="2f2e9-114">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="2f2e9-115">**Non riuscito** (2)</span><span class="sxs-lookup"><span data-stu-id="2f2e9-115">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2f2e9-116">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="2f2e9-116">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="2f2e9-117">**Parametro non valido** (4)</span><span class="sxs-lookup"><span data-stu-id="2f2e9-117">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="2f2e9-118">**Stato non valido** (5)</span><span class="sxs-lookup"><span data-stu-id="2f2e9-118">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="2f2e9-119">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="2f2e9-119">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="2f2e9-120">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="2f2e9-120">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="2f2e9-121">**Metodo riservato** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="2f2e9-121">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="2f2e9-122">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="2f2e9-122">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="2f2e9-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2f2e9-123">Requirements</span></span>



| <span data-ttu-id="2f2e9-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f2e9-124">Requirement</span></span> | <span data-ttu-id="2f2e9-125">Valore</span><span class="sxs-lookup"><span data-stu-id="2f2e9-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f2e9-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2f2e9-126">Minimum supported client</span></span><br/> | <span data-ttu-id="2f2e9-127">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="2f2e9-127">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="2f2e9-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2f2e9-128">Minimum supported server</span></span><br/> | <span data-ttu-id="2f2e9-129">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="2f2e9-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2f2e9-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2f2e9-130">Namespace</span></span><br/>                | <span data-ttu-id="2f2e9-131">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="2f2e9-131">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="2f2e9-132">MOF</span><span class="sxs-lookup"><span data-stu-id="2f2e9-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2f2e9-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2f2e9-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2f2e9-134">DLL</span><span class="sxs-lookup"><span data-stu-id="2f2e9-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f2e9-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2f2e9-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2f2e9-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2f2e9-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f2e9-137">**AddResourceSettings**</span><span class="sxs-lookup"><span data-stu-id="2f2e9-137">**AddResourceSettings**</span></span>](addresourcesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[<span data-ttu-id="2f2e9-138">**ModifyResourceSettings**</span><span class="sxs-lookup"><span data-stu-id="2f2e9-138">**ModifyResourceSettings**</span></span>](modifyresourcesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[<span data-ttu-id="2f2e9-139">**\_VirtualEthernetSwitchManagementService MSVM**</span><span class="sxs-lookup"><span data-stu-id="2f2e9-139">**Msvm\_VirtualEthernetSwitchManagementService**</span></span>](msvm-virtualethernetswitchmanagementservice.md)
</dt> </dl>

 

