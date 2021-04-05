---
description: Rimuove le impostazioni delle risorse virtuali da una configurazione di sistema virtuale.
ms.assetid: 7934a5e4-f54c-43fd-9ec3-d1fc1aad0acd
title: Metodo RemoveResourceSettings della classe CIM_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService.RemoveResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1f5b3ac1cc53f23d0d899a4c6b5d17408bca3b9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755439"
---
# <a name="removeresourcesettings-method-of-the-cim_virtualsystemmanagementservice-class"></a><span data-ttu-id="6ee95-103">Metodo RemoveResourceSettings della classe CIM \_ VirtualSystemManagementService</span><span class="sxs-lookup"><span data-stu-id="6ee95-103">RemoveResourceSettings method of the CIM\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="6ee95-104">Rimuove le impostazioni delle risorse virtuali da una configurazione di sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="6ee95-104">Removes virtual resource settings from a virtual system configuration.</span></span>

<span data-ttu-id="6ee95-105">Quando applicato alle parti di una configurazione di sistema virtuale "corrente", è possibile che vengano rimosse le risorse degli effetti collaterali del sistema virtuale attivo.</span><span class="sxs-lookup"><span data-stu-id="6ee95-105">When applied to parts of a "current" virtual system configuration, as a side effect resources of the active virtual system may be removed.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ee95-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6ee95-106">Syntax</span></span>


```mof
uint32 RemoveResourceSettings(
  [in]  CIM_ResourceAllocationSettingData REF ResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="6ee95-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="6ee95-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ee95-108">*ResourceSettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6ee95-108">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ee95-109">Matrice di riferimenti a istanze della classe [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) in cui ogni istanza rappresenta le impostazioni di una risorsa virtuale all'interno di una configurazione di sistema virtuale da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="6ee95-109">Array of references to instances of class [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) where each instance represents the settings of a virtual resource within a virtual system configuration that are to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="6ee95-110">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="6ee95-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6ee95-111">Se l'operazione è a esecuzione prolungata, è possibile che venga restituito facoltativamente un [**\_ ConcreteJob CIM**](cim-concretejob.md) che rappresenta il processo.</span><span class="sxs-lookup"><span data-stu-id="6ee95-111">If the operation is long running, then optionally a [**CIM\_ConcreteJob**](cim-concretejob.md) representing the job may be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ee95-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6ee95-112">Return value</span></span>

<span data-ttu-id="6ee95-113">Restituisce 0 in caso di esito positivo; in caso contrario, restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="6ee95-113">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="6ee95-114">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="6ee95-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6ee95-115">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="6ee95-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="6ee95-116">**Non riuscito** (2)</span><span class="sxs-lookup"><span data-stu-id="6ee95-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="6ee95-117">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="6ee95-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="6ee95-118">**Parametro non valido** (4)</span><span class="sxs-lookup"><span data-stu-id="6ee95-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="6ee95-119">**Stato non valido** (5)</span><span class="sxs-lookup"><span data-stu-id="6ee95-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="6ee95-120">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="6ee95-120">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="6ee95-121">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="6ee95-121">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="6ee95-122">**Metodo riservato** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="6ee95-122">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="6ee95-123">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="6ee95-123">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="6ee95-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6ee95-124">Requirements</span></span>



| <span data-ttu-id="6ee95-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ee95-125">Requirement</span></span> | <span data-ttu-id="6ee95-126">Valore</span><span class="sxs-lookup"><span data-stu-id="6ee95-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ee95-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6ee95-127">Minimum supported client</span></span><br/> | <span data-ttu-id="6ee95-128">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="6ee95-128">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="6ee95-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6ee95-129">Minimum supported server</span></span><br/> | <span data-ttu-id="6ee95-130">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="6ee95-130">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="6ee95-131">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6ee95-131">Namespace</span></span><br/>                | <span data-ttu-id="6ee95-132">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="6ee95-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="6ee95-133">MOF</span><span class="sxs-lookup"><span data-stu-id="6ee95-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6ee95-134"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6ee95-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6ee95-135">DLL</span><span class="sxs-lookup"><span data-stu-id="6ee95-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ee95-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6ee95-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6ee95-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6ee95-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ee95-138">**\_VIRTUALSYSTEMMANAGEMENTSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="6ee95-138">**CIM\_VirtualSystemManagementService**</span></span>](cim-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




