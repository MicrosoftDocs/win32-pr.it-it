---
description: Modifica le impostazioni delle risorse virtuali.
ms.assetid: 4942f167-0e53-4ae2-b973-4a06b636b44a
title: Metodo ModifyResourceSettings della classe CIM_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService.ModifyResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e27729429d02c2412e05344779cc40461dbd9dfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485364"
---
# <a name="modifyresourcesettings-method-of-the-cim_virtualsystemmanagementservice-class"></a><span data-ttu-id="62011-103">Metodo ModifyResourceSettings della classe CIM \_ VirtualSystemManagementService</span><span class="sxs-lookup"><span data-stu-id="62011-103">ModifyResourceSettings method of the CIM\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="62011-104">Modifica le impostazioni delle risorse virtuali.</span><span class="sxs-lookup"><span data-stu-id="62011-104">Modifies virtual resource settings.</span></span>

<span data-ttu-id="62011-105">Quando viene applicato alle parti di una configurazione di sistema virtuale "corrente", è possibile che le risorse degli effetti collaterali del sistema virtuale attivo vengano modificate.</span><span class="sxs-lookup"><span data-stu-id="62011-105">When applied to parts of a "current" virtual system configuration, as a side effect resources of the active virtual system may be modified.</span></span>

## <a name="syntax"></a><span data-ttu-id="62011-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="62011-106">Syntax</span></span>


```mof
uint32 ModifyResourceSettings(
  [in]  string                                ResourceSettings[],
  [out] CIM_ResourceAllocationSettingData REF ResultingResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="62011-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="62011-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62011-108">*ResourceSettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="62011-108">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62011-109">Matrice di stringhe, ognuna delle quali contiene un'istanza incorporata della classe [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) che descrive le modifiche agli aspetti virtuali di una risorsa virtuale esistente.</span><span class="sxs-lookup"><span data-stu-id="62011-109">Array of strings each containing an embedded instance of class [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) that describes modifications to the virtual aspects of an existing virtual resource.</span></span> <span data-ttu-id="62011-110">Per identificare l'impostazione della risorsa virtuale da modificare, tutte le istanze devono avere un **InstanceID** valido.</span><span class="sxs-lookup"><span data-stu-id="62011-110">All instances must have a valid **InstanceID** in order to identify the virtual resource setting to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="62011-111">*ResultingResourceSettings* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="62011-111">*ResultingResourceSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="62011-112">Matrice di riferimenti a istanze della classe [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) che rappresentano gli aspetti virtuali delle risorse virtuali modificate.</span><span class="sxs-lookup"><span data-stu-id="62011-112">Array of references to instances of class [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) representing virtual aspects of the modified virtual resources.</span></span>

</dd> <dt>

<span data-ttu-id="62011-113">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="62011-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="62011-114">Se l'operazione è a esecuzione prolungata, è possibile che venga restituito un processo.</span><span class="sxs-lookup"><span data-stu-id="62011-114">If the operation is long running, then optionally a job be returned.</span></span> <span data-ttu-id="62011-115">In questo caso, le istanze della classe [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) che rappresentano le impostazioni delle risorse modificate sono disponibili tramite Association **CIM \_ ConreteComponent** dall'istanza della classe [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) che rappresenta la configurazione del sistema virtuale interessata.</span><span class="sxs-lookup"><span data-stu-id="62011-115">In this case, the instances of class [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) representing the modified resource settings are available via association **CIM\_ConreteComponent** from the instance of class [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) representing the affected virtual system configuration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62011-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="62011-116">Return value</span></span>

<span data-ttu-id="62011-117">Restituisce 0 in caso di esito positivo; in caso contrario, restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="62011-117">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="62011-118">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="62011-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="62011-119">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="62011-119">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="62011-120">**Non riuscito** (2)</span><span class="sxs-lookup"><span data-stu-id="62011-120">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="62011-121">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="62011-121">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="62011-122">**Parametro non valido** (4)</span><span class="sxs-lookup"><span data-stu-id="62011-122">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="62011-123">**Stato non valido** (5)</span><span class="sxs-lookup"><span data-stu-id="62011-123">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="62011-124">**Parametri incompatibili** (6)</span><span class="sxs-lookup"><span data-stu-id="62011-124">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="62011-125">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="62011-125">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="62011-126">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="62011-126">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="62011-127">**Metodo riservato** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="62011-127">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="62011-128">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="62011-128">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="62011-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="62011-129">Requirements</span></span>



| <span data-ttu-id="62011-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="62011-130">Requirement</span></span> | <span data-ttu-id="62011-131">Valore</span><span class="sxs-lookup"><span data-stu-id="62011-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62011-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="62011-132">Minimum supported client</span></span><br/> | <span data-ttu-id="62011-133">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="62011-133">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="62011-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="62011-134">Minimum supported server</span></span><br/> | <span data-ttu-id="62011-135">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="62011-135">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="62011-136">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="62011-136">Namespace</span></span><br/>                | <span data-ttu-id="62011-137">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="62011-137">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="62011-138">MOF</span><span class="sxs-lookup"><span data-stu-id="62011-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="62011-139"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="62011-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="62011-140">DLL</span><span class="sxs-lookup"><span data-stu-id="62011-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62011-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="62011-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="62011-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="62011-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62011-143">**\_VIRTUALSYSTEMMANAGEMENTSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="62011-143">**CIM\_VirtualSystemManagementService**</span></span>](cim-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




