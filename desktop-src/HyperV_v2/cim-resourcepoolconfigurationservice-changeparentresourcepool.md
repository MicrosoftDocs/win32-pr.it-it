---
description: Avviare un processo per modificare un pool padre utilizzando le impostazioni di allocazione specificate.
ms.assetid: 2eea1a60-fbf0-49a7-8f79-52c62c295316
title: Metodo ChangeParentResourcePool della classe CIM_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService.ChangeParentResourcePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 6ef852d6af8f0973b6b3f29fca5fcd90e9ce726a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307777"
---
# <a name="changeparentresourcepool-method-of-the-cim_resourcepoolconfigurationservice-class"></a><span data-ttu-id="0bc58-103">Metodo ChangeParentResourcePool della classe CIM \_ ResourcePoolConfigurationService</span><span class="sxs-lookup"><span data-stu-id="0bc58-103">ChangeParentResourcePool method of the CIM\_ResourcePoolConfigurationService class</span></span>

<span data-ttu-id="0bc58-104">Avviare un processo per modificare un pool padre utilizzando le impostazioni di allocazione specificate.</span><span class="sxs-lookup"><span data-stu-id="0bc58-104">Start a job to change a parent pool using the specified allocation settings.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bc58-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0bc58-105">Syntax</span></span>


```mof
uint32 ChangeParentResourcePool(
  [in]  CIM_ResourcePool REF ChildPool,
  [in]  CIM_ResourcePool REF ParentPool[],
  [in]  string               Settings[],
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="0bc58-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0bc58-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0bc58-107">*ChildPool* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0bc58-107">*ChildPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bc58-108">Un [**\_ ResourcePool CIM**](cim-resourcepool.md) che fa riferimento al pool figlio.</span><span class="sxs-lookup"><span data-stu-id="0bc58-108">A [**CIM\_ResourcePool**](cim-resourcepool.md) that references the child pool.</span></span>

</dd> <dt>

<span data-ttu-id="0bc58-109">*ParentPool* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0bc58-109">*ParentPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bc58-110">Matrice [**CIM \_ ResourcePool**](cim-resourcepool.md) che fa riferimento ai pool padre.</span><span class="sxs-lookup"><span data-stu-id="0bc58-110">A [**CIM\_ResourcePool**](cim-resourcepool.md) array that references the parent pool(s).</span></span>

</dd> <dt>

<span data-ttu-id="0bc58-111">*Impostazioni* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="0bc58-111">*Settings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bc58-112">Stringa facoltativa contenente una rappresentazione di un'istanza [**CIM \_ SettingData**](cim-settingdata.md) utilizzata per specificare le impostazioni per il pool padre.</span><span class="sxs-lookup"><span data-stu-id="0bc58-112">Optional string containing a representation of a [**CIM\_SettingData**](cim-settingdata.md) instance that is used to specify the settings for the parent pool.</span></span>

</dd> <dt>

<span data-ttu-id="0bc58-113">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="0bc58-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0bc58-114">Un [**\_ ConcreteJob CIM**](cim-concretejob.md) che fa riferimento al processo (può essere **null** se il processo è stato completato).</span><span class="sxs-lookup"><span data-stu-id="0bc58-114">A [**CIM\_ConcreteJob**](cim-concretejob.md) that references the job (may be **null** if job completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0bc58-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0bc58-115">Return value</span></span>

<span data-ttu-id="0bc58-116">Restituisce 0 in caso di esito positivo; in caso contrario, restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="0bc58-116">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="0bc58-117">**Processo completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="0bc58-117">**Job Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0bc58-118">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="0bc58-118">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="0bc58-119">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="0bc58-119">**Unknown** (2)</span></span>
</dt> <dt>

<span data-ttu-id="0bc58-120">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="0bc58-120">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="0bc58-121">**Non riuscito** (4)</span><span class="sxs-lookup"><span data-stu-id="0bc58-121">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="0bc58-122">**Parametro non valido** (5)</span><span class="sxs-lookup"><span data-stu-id="0bc58-122">**Invalid Parameter** (5)</span></span>
</dt> <dt>

<span data-ttu-id="0bc58-123">**In uso** (6)</span><span class="sxs-lookup"><span data-stu-id="0bc58-123">**In Use** (6)</span></span>
</dt> <dt>

<span data-ttu-id="0bc58-124">**ResourceType errato per il pool** (7)</span><span class="sxs-lookup"><span data-stu-id="0bc58-124">**Incorrect ResourceType for the Pool** (7)</span></span>
</dt> <dt>

<span data-ttu-id="0bc58-125">**Risorse insufficienti** (8)</span><span class="sxs-lookup"><span data-stu-id="0bc58-125">**Insufficient Resources** (8)</span></span>
</dt> <dt>

<span data-ttu-id="0bc58-126">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="0bc58-126">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="0bc58-127">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="0bc58-127">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="0bc58-128">**Dimensioni non supportate** (4097)</span><span class="sxs-lookup"><span data-stu-id="0bc58-128">**Size Not Supported** (4097)</span></span>
</dt> <dt>

<span data-ttu-id="0bc58-129">**Metodo riservato** (4098.. 32767)</span><span class="sxs-lookup"><span data-stu-id="0bc58-129">**Method Reserved** (4098..32767)</span></span>
</dt> <dt>

<span data-ttu-id="0bc58-130">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="0bc58-130">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="0bc58-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0bc58-131">Requirements</span></span>



| <span data-ttu-id="0bc58-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="0bc58-132">Requirement</span></span> | <span data-ttu-id="0bc58-133">Valore</span><span class="sxs-lookup"><span data-stu-id="0bc58-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0bc58-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0bc58-134">Minimum supported client</span></span><br/> | <span data-ttu-id="0bc58-135">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="0bc58-135">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="0bc58-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0bc58-136">Minimum supported server</span></span><br/> | <span data-ttu-id="0bc58-137">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="0bc58-137">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="0bc58-138">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0bc58-138">Namespace</span></span><br/>                | <span data-ttu-id="0bc58-139">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="0bc58-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="0bc58-140">MOF</span><span class="sxs-lookup"><span data-stu-id="0bc58-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0bc58-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0bc58-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0bc58-142">DLL</span><span class="sxs-lookup"><span data-stu-id="0bc58-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0bc58-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0bc58-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0bc58-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0bc58-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bc58-145">**\_RESOURCEPOOLCONFIGURATIONSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="0bc58-145">**CIM\_ResourcePoolConfigurationService**</span></span>](cim-resourcepoolconfigurationservice.md)
</dt> </dl>

 

 




