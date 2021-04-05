---
description: Avvia un processo per creare un ResourcePool radice. Il ResourcePool avrà come ambito lo stesso sistema di questo servizio.
ms.assetid: 357880dc-125a-452c-89f5-44cd17684436
title: Metodo CreateResourcePool della classe CIM_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService.CreateResourcePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: ca339eb2e2a4ec0fb441c5ed1a657608d71248bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752247"
---
# <a name="createresourcepool-method-of-the-cim_resourcepoolconfigurationservice-class"></a><span data-ttu-id="987aa-104">Metodo CreateResourcePool della classe CIM \_ ResourcePoolConfigurationService</span><span class="sxs-lookup"><span data-stu-id="987aa-104">CreateResourcePool method of the CIM\_ResourcePoolConfigurationService class</span></span>

<span data-ttu-id="987aa-105">Avvia un processo per creare un ResourcePool radice.</span><span class="sxs-lookup"><span data-stu-id="987aa-105">Starts a job to create a root ResourcePool.</span></span> <span data-ttu-id="987aa-106">Il ResourcePool avrà come ambito lo stesso sistema di questo servizio.</span><span class="sxs-lookup"><span data-stu-id="987aa-106">The ResourcePool will be scoped to the same System as this Service.</span></span>

## <a name="syntax"></a><span data-ttu-id="987aa-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="987aa-107">Syntax</span></span>


```mof
uint32 CreateResourcePool(
  [in]  string                ElementName,
  [in]  CIM_LogicalDevice REF HostResources[],
  [in]  string                ResourceType,
  [out] CIM_ResourcePool  REF Pool,
  [out] CIM_ConcreteJob   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="987aa-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="987aa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="987aa-109">*ElementName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="987aa-109">*ElementName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="987aa-110">Nome pertinente dell'utente finale per il pool da creare.</span><span class="sxs-lookup"><span data-stu-id="987aa-110">A end user relevant name for the pool being created.</span></span> <span data-ttu-id="987aa-111">Se è **null**, è possibile usare un nome predefinito fornito dal sistema.</span><span class="sxs-lookup"><span data-stu-id="987aa-111">If **NULL**, then a system supplied default name can be used.</span></span> <span data-ttu-id="987aa-112">Il valore verrà archiviato nella proprietà **ElementName** per il pool creato.</span><span class="sxs-lookup"><span data-stu-id="987aa-112">The value will be stored in the **ElementName** property for the created pool.</span></span>

</dd> <dt>

<span data-ttu-id="987aa-113">*HostResources* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="987aa-113">*HostResources* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="987aa-114">Matrice di zero o più dispositivi [**CIM \_ LogicalDevice**](cim-logicaldevice.md) usati per creare il pool o modificare gli extent di origine.</span><span class="sxs-lookup"><span data-stu-id="987aa-114">Array of zero or more [**CIM\_LogicalDevice**](cim-logicaldevice.md) devices that are used to create the Pool or modify the source extents.</span></span> <span data-ttu-id="987aa-115">Tutti gli elementi della matrice devono essere dello stesso tipo.</span><span class="sxs-lookup"><span data-stu-id="987aa-115">All elements in the array must be of the same type.</span></span>

</dd> <dt>

<span data-ttu-id="987aa-116">*ResourceType* \[in\]</span><span class="sxs-lookup"><span data-stu-id="987aa-116">*ResourceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="987aa-117">Il tipo di risorse che il pool creato gestirà.</span><span class="sxs-lookup"><span data-stu-id="987aa-117">The type of resources the created pool will manage.</span></span> <span data-ttu-id="987aa-118">Se *HostResources* contiene elementi, è necessario che questa proprietà machi il tipo.</span><span class="sxs-lookup"><span data-stu-id="987aa-118">If *HostResources* contains elements, this property must mach their type.</span></span>

</dd> <dt>

<span data-ttu-id="987aa-119">*Pool* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="987aa-119">*Pool* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="987aa-120">In seguito all'esito positivo, restituisce un riferimento al [**\_ ResourcePool CIM**](cim-resourcepool.md)risultante.</span><span class="sxs-lookup"><span data-stu-id="987aa-120">On success, returns a reference to the resulting [**CIM\_ResourcePool**](cim-resourcepool.md).</span></span> <span data-ttu-id="987aa-121">Quando viene restituito un processo, può essere **null**, nel qual caso il client deve usare il processo per trovare il ResourcePool risultante dopo il completamento del processo.</span><span class="sxs-lookup"><span data-stu-id="987aa-121">When a Job is returned, this may be **NULL**, in which case, the client must use the Job to find the resulting ResourcePool once the Job completes.</span></span>

</dd> <dt>

<span data-ttu-id="987aa-122">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="987aa-122">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="987aa-123">Riferimento a un [**\_ ConcreteJob CIM**](cim-concretejob.md) che rappresenta il processo (può essere null se il processo è stato completato).</span><span class="sxs-lookup"><span data-stu-id="987aa-123">Reference to a [**CIM\_ConcreteJob**](cim-concretejob.md) that represents the job (may be null if job completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="987aa-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="987aa-124">Return value</span></span>

<span data-ttu-id="987aa-125">Restituisce 0 in caso di esito positivo; in caso contrario, restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="987aa-125">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="987aa-126">**Processo completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="987aa-126">**Job Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="987aa-127">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="987aa-127">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="987aa-128">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="987aa-128">**Unknown** (2)</span></span>
</dt> <dt>

<span data-ttu-id="987aa-129">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="987aa-129">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="987aa-130">**Non riuscito** (4)</span><span class="sxs-lookup"><span data-stu-id="987aa-130">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="987aa-131">**Parametro non valido** (5)</span><span class="sxs-lookup"><span data-stu-id="987aa-131">**Invalid Parameter** (5)</span></span>
</dt> <dt>

<span data-ttu-id="987aa-132">**In uso** (6)</span><span class="sxs-lookup"><span data-stu-id="987aa-132">**In Use** (6)</span></span>
</dt> <dt>

<span data-ttu-id="987aa-133">**ResourceType errato per il pool** (7)</span><span class="sxs-lookup"><span data-stu-id="987aa-133">**Incorrect ResourceType for the Pool** (7)</span></span>
</dt> <dt>

<span data-ttu-id="987aa-134">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="987aa-134">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="987aa-135">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="987aa-135">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="987aa-136">**Dimensioni non supportate** (4097)</span><span class="sxs-lookup"><span data-stu-id="987aa-136">**Size Not Supported** (4097)</span></span>
</dt> <dt>

<span data-ttu-id="987aa-137">**Metodo riservato** (4098.. 32767)</span><span class="sxs-lookup"><span data-stu-id="987aa-137">**Method Reserved** (4098..32767)</span></span>
</dt> <dt>

<span data-ttu-id="987aa-138">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="987aa-138">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="987aa-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="987aa-139">Requirements</span></span>



| <span data-ttu-id="987aa-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="987aa-140">Requirement</span></span> | <span data-ttu-id="987aa-141">Valore</span><span class="sxs-lookup"><span data-stu-id="987aa-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="987aa-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="987aa-142">Minimum supported client</span></span><br/> | <span data-ttu-id="987aa-143">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="987aa-143">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="987aa-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="987aa-144">Minimum supported server</span></span><br/> | <span data-ttu-id="987aa-145">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="987aa-145">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="987aa-146">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="987aa-146">Namespace</span></span><br/>                | <span data-ttu-id="987aa-147">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="987aa-147">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="987aa-148">MOF</span><span class="sxs-lookup"><span data-stu-id="987aa-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="987aa-149"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="987aa-149"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="987aa-150">DLL</span><span class="sxs-lookup"><span data-stu-id="987aa-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="987aa-151"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="987aa-151"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="987aa-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="987aa-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="987aa-153">**\_RESOURCEPOOLCONFIGURATIONSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="987aa-153">**CIM\_ResourcePoolConfigurationService**</span></span>](cim-resourcepoolconfigurationservice.md)
</dt> </dl>

 

 




