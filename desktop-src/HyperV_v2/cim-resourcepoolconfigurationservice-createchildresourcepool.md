---
description: Avviare un processo per creare un pool secondario da un pool padre utilizzando le impostazioni di allocazione specificate.
ms.assetid: 9b09221a-7c4e-4648-a2a8-012df1818c3e
title: Metodo CreateChildResourcePool della classe CIM_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService.CreateChildResourcePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e4e709fd240c849581f6dcd343001a9b1dee7003
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307778"
---
# <a name="createchildresourcepool-method-of-the-cim_resourcepoolconfigurationservice-class"></a><span data-ttu-id="85dbb-103">Metodo CreateChildResourcePool della classe CIM \_ ResourcePoolConfigurationService</span><span class="sxs-lookup"><span data-stu-id="85dbb-103">CreateChildResourcePool method of the CIM\_ResourcePoolConfigurationService class</span></span>

<span data-ttu-id="85dbb-104">Avviare un processo per creare un pool secondario da un pool padre utilizzando le impostazioni di allocazione specificate.</span><span class="sxs-lookup"><span data-stu-id="85dbb-104">Start a job to create a sub-pool from a parent pool using the specified allocation settings.</span></span>

## <a name="syntax"></a><span data-ttu-id="85dbb-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="85dbb-105">Syntax</span></span>


```mof
uint32 CreateChildResourcePool(
  [in]  string               ElementName,
  [in]  string               Settings[],
  [in]  CIM_ResourcePool REF ParentPool[],
  [out] CIM_ResourcePool REF Pool,
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="85dbb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="85dbb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85dbb-107">*ElementName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="85dbb-107">*ElementName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85dbb-108">Nome pertinente dell'utente finale per il pool da creare.</span><span class="sxs-lookup"><span data-stu-id="85dbb-108">A end user relevant name for the pool being created.</span></span> <span data-ttu-id="85dbb-109">Se è **null**, è possibile usare un nome predefinito fornito dal sistema.</span><span class="sxs-lookup"><span data-stu-id="85dbb-109">If **NULL**, then a system supplied default name can be used.</span></span> <span data-ttu-id="85dbb-110">Il valore verrà archiviato nella proprietà **ElementName** per l'elemento creato.</span><span class="sxs-lookup"><span data-stu-id="85dbb-110">The value will be stored in the **ElementName** property for the created element.</span></span>

</dd> <dt>

<span data-ttu-id="85dbb-111">*Impostazioni* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="85dbb-111">*Settings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85dbb-112">Stringa contenente una rappresentazione di un'istanza [**CIM \_ SettingData**](cim-settingdata.md) utilizzata per specificare le impostazioni per il pool figlio.</span><span class="sxs-lookup"><span data-stu-id="85dbb-112">String containing a representation of a [**CIM\_SettingData**](cim-settingdata.md) instance that is used to specify the settings for the child Pool.</span></span>

</dd> <dt>

<span data-ttu-id="85dbb-113">*ParentPool* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="85dbb-113">*ParentPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85dbb-114">[**\_ ResourcePool CIM**](cim-resourcepool.md) da cui creare il nuovo pool.</span><span class="sxs-lookup"><span data-stu-id="85dbb-114">A [**CIM\_ResourcePool**](cim-resourcepool.md) from which to create the new Pool.</span></span>

</dd> <dt>

<span data-ttu-id="85dbb-115">*Pool* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="85dbb-115">*Pool* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="85dbb-116">Un [**\_ ResourcePool CIM**](cim-resourcepool.md) che fa riferimento al pool risultante.</span><span class="sxs-lookup"><span data-stu-id="85dbb-116">A [**CIM\_ResourcePool**](cim-resourcepool.md) that references the resulting pool.</span></span>

</dd> <dt>

<span data-ttu-id="85dbb-117">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="85dbb-117">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="85dbb-118">Riferimento al processo (può essere null se il processo è stato completato).</span><span class="sxs-lookup"><span data-stu-id="85dbb-118">Reference to the job (may be null if job completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85dbb-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="85dbb-119">Return value</span></span>

<span data-ttu-id="85dbb-120">Restituisce 0 in caso di esito positivo; in caso contrario, restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="85dbb-120">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="85dbb-121">**Processo completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="85dbb-121">**Job Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="85dbb-122">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="85dbb-122">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="85dbb-123">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="85dbb-123">**Unknown** (2)</span></span>
</dt> <dt>

<span data-ttu-id="85dbb-124">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="85dbb-124">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="85dbb-125">**Non riuscito** (4)</span><span class="sxs-lookup"><span data-stu-id="85dbb-125">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="85dbb-126">**Parametro non valido** (5)</span><span class="sxs-lookup"><span data-stu-id="85dbb-126">**Invalid Parameter** (5)</span></span>
</dt> <dt>

<span data-ttu-id="85dbb-127">**In uso** (6)</span><span class="sxs-lookup"><span data-stu-id="85dbb-127">**In Use** (6)</span></span>
</dt> <dt>

<span data-ttu-id="85dbb-128">**ResourceType errato per il pool** (7)</span><span class="sxs-lookup"><span data-stu-id="85dbb-128">**Incorrect ResourceType for the Pool** (7)</span></span>
</dt> <dt>

<span data-ttu-id="85dbb-129">**Risorse insufficienti** (8)</span><span class="sxs-lookup"><span data-stu-id="85dbb-129">**Insufficient Resources** (8)</span></span>
</dt> <dt>

<span data-ttu-id="85dbb-130">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="85dbb-130">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="85dbb-131">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="85dbb-131">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="85dbb-132">**Dimensioni non supportate** (4097)</span><span class="sxs-lookup"><span data-stu-id="85dbb-132">**Size Not Supported** (4097)</span></span>
</dt> <dt>

<span data-ttu-id="85dbb-133">**Metodo riservato** (4098.. 32767)</span><span class="sxs-lookup"><span data-stu-id="85dbb-133">**Method Reserved** (4098..32767)</span></span>
</dt> <dt>

<span data-ttu-id="85dbb-134">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="85dbb-134">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="85dbb-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="85dbb-135">Requirements</span></span>



| <span data-ttu-id="85dbb-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="85dbb-136">Requirement</span></span> | <span data-ttu-id="85dbb-137">Valore</span><span class="sxs-lookup"><span data-stu-id="85dbb-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85dbb-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="85dbb-138">Minimum supported client</span></span><br/> | <span data-ttu-id="85dbb-139">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="85dbb-139">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="85dbb-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="85dbb-140">Minimum supported server</span></span><br/> | <span data-ttu-id="85dbb-141">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="85dbb-141">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="85dbb-142">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="85dbb-142">Namespace</span></span><br/>                | <span data-ttu-id="85dbb-143">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="85dbb-143">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="85dbb-144">MOF</span><span class="sxs-lookup"><span data-stu-id="85dbb-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="85dbb-145"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="85dbb-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="85dbb-146">DLL</span><span class="sxs-lookup"><span data-stu-id="85dbb-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="85dbb-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="85dbb-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="85dbb-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="85dbb-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85dbb-149">**\_RESOURCEPOOLCONFIGURATIONSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="85dbb-149">**CIM\_ResourcePoolConfigurationService**</span></span>](cim-resourcepoolconfigurationservice.md)
</dt> </dl>

 

 




