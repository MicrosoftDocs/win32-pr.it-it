---
description: Aggiunge risorse a una configurazione di sistema virtuale.
ms.assetid: c2541571-74f0-48f8-997c-56c152980eea
title: Metodo AddResourceSettings della classe CIM_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService.AddResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9563b1e8421dfa6724971450b117780435f6f39e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310553"
---
# <a name="addresourcesettings-method-of-the-cim_virtualsystemmanagementservice-class"></a><span data-ttu-id="4a8c7-103">Metodo AddResourceSettings della classe CIM \_ VirtualSystemManagementService</span><span class="sxs-lookup"><span data-stu-id="4a8c7-103">AddResourceSettings method of the CIM\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="4a8c7-104">Aggiunge risorse a una configurazione di sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="4a8c7-104">Adds resources to a virtual system configuration.</span></span>

<span data-ttu-id="4a8c7-105">Quando viene applicato a una configurazione di sistema virtuale "stato", le risorse degli effetti collaterali vengono aggiunte al sistema virtuale attivo.</span><span class="sxs-lookup"><span data-stu-id="4a8c7-105">When applied to a "state" virtual system configuration, as a side effect resources are added to the active virtual system.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a8c7-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4a8c7-106">Syntax</span></span>


```mof
uint32 AddResourceSettings(
  [in]  CIM_VirtualSystemSettingData      REF AffectedConfiguration,
  [in]  string                                ResourceSettings[],
  [out] CIM_ResourceAllocationSettingData REF ResultingResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="4a8c7-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="4a8c7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a8c7-108">*AffectedConfiguration* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4a8c7-108">*AffectedConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a8c7-109">Riferimento [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) alla configurazione del sistema virtuale interessata.</span><span class="sxs-lookup"><span data-stu-id="4a8c7-109">A [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) reference to the affected virtual system configuration.</span></span>

</dd> <dt>

<span data-ttu-id="4a8c7-110">*ResourceSettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4a8c7-110">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a8c7-111">Matrice di stringhe, ognuna delle quali contiene un'istanza incorporata della classe [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) che descrive gli aspetti virtuali di una risorsa virtuale da aggiungere al sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="4a8c7-111">Array of strings each containing one embedded instance of class [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) that describes the virtual aspects of a virtual resource to be added to the virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="4a8c7-112">*ResultingResourceSettings* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4a8c7-112">*ResultingResourceSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4a8c7-113">Matrice di riferimenti a istanze della classe [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) che rappresentano gli aspetti virtuali delle risorse virtuali aggiunte.</span><span class="sxs-lookup"><span data-stu-id="4a8c7-113">Array of references to instances of class [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) representing virtual aspects of the added virtual resources.</span></span>

</dd> <dt>

<span data-ttu-id="4a8c7-114">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="4a8c7-114">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4a8c7-115">Se l'operazione è a esecuzione prolungata, è possibile che venga restituito un processo.</span><span class="sxs-lookup"><span data-stu-id="4a8c7-115">If the operation is long running, then optionally a job may be returned.</span></span> <span data-ttu-id="4a8c7-116">In questo caso, le istanze della classe [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) che rappresentano le impostazioni delle risorse aggiunte sono disponibili tramite Association **CIM \_ ConreteComponent** dall'istanza della classe [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) che rappresenta la configurazione del sistema virtuale interessata.</span><span class="sxs-lookup"><span data-stu-id="4a8c7-116">In this case, the instances of class [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) representing the added resource settings are available via association **CIM\_ConreteComponent** from the instance of class [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) representing the affected virtual system configuration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a8c7-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4a8c7-117">Return value</span></span>

<span data-ttu-id="4a8c7-118">Restituisce 0 in caso di esito positivo; in caso contrario, restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="4a8c7-118">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="4a8c7-119">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="4a8c7-119">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4a8c7-120">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="4a8c7-120">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="4a8c7-121">**Non riuscito** (2)</span><span class="sxs-lookup"><span data-stu-id="4a8c7-121">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="4a8c7-122">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="4a8c7-122">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="4a8c7-123">**Parametro non valido** (4)</span><span class="sxs-lookup"><span data-stu-id="4a8c7-123">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="4a8c7-124">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="4a8c7-124">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="4a8c7-125">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="4a8c7-125">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="4a8c7-126">**Metodo riservato** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="4a8c7-126">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="4a8c7-127">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="4a8c7-127">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="4a8c7-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4a8c7-128">Requirements</span></span>



| <span data-ttu-id="4a8c7-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a8c7-129">Requirement</span></span> | <span data-ttu-id="4a8c7-130">Valore</span><span class="sxs-lookup"><span data-stu-id="4a8c7-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a8c7-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4a8c7-131">Minimum supported client</span></span><br/> | <span data-ttu-id="4a8c7-132">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="4a8c7-132">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="4a8c7-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4a8c7-133">Minimum supported server</span></span><br/> | <span data-ttu-id="4a8c7-134">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="4a8c7-134">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="4a8c7-135">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4a8c7-135">Namespace</span></span><br/>                | <span data-ttu-id="4a8c7-136">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="4a8c7-136">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="4a8c7-137">MOF</span><span class="sxs-lookup"><span data-stu-id="4a8c7-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4a8c7-138"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4a8c7-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4a8c7-139">DLL</span><span class="sxs-lookup"><span data-stu-id="4a8c7-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4a8c7-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4a8c7-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4a8c7-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4a8c7-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a8c7-142">**\_VIRTUALSYSTEMMANAGEMENTSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="4a8c7-142">**CIM\_VirtualSystemManagementService**</span></span>](cim-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




