---
description: Crea un pool di risorse figlio.
ms.assetid: 30a70231-f1b7-4f0e-ac47-cf5a79ddb8ab
title: Metodo CreatePool della classe Msvm_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolConfigurationService.CreatePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: fb29a4b5a47d88232a6b0df6a828d482030b3f1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314346"
---
# <a name="createpool-method-of-the-msvm_resourcepoolconfigurationservice-class"></a><span data-ttu-id="c83d7-103">Metodo CreatePool della classe MSVM \_ ResourcePoolConfigurationService</span><span class="sxs-lookup"><span data-stu-id="c83d7-103">CreatePool method of the Msvm\_ResourcePoolConfigurationService class</span></span>

<span data-ttu-id="c83d7-104">Crea un pool di risorse figlio.</span><span class="sxs-lookup"><span data-stu-id="c83d7-104">Creates a child resource pool.</span></span> <span data-ttu-id="c83d7-105">Il pool di risorse avrà come ambito lo stesso sistema di questo servizio.</span><span class="sxs-lookup"><span data-stu-id="c83d7-105">The resource pool will be scoped to the same System as this Service.</span></span> <span data-ttu-id="c83d7-106">Il pool risultante sarà un pool figlio.</span><span class="sxs-lookup"><span data-stu-id="c83d7-106">The resulting pool will be a child pool.</span></span>

## <a name="syntax"></a><span data-ttu-id="c83d7-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c83d7-107">Syntax</span></span>


```mof
uint32 CreatePool(
  [in]  string               PoolSettings,
  [in]  CIM_ResourcePool REF ParentPools[],
  [in]  string               AllocationSettings[],
  [out] CIM_ResourcePool REF Pool,
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="c83d7-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="c83d7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c83d7-109">*PoolSettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c83d7-109">*PoolSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c83d7-110">Istanza incorporata della classe [**MSVM \_ ResourcePoolSettingData**](msvm-resourcepoolsettingdata.md) utilizzata per specificare le impostazioni del pool che non sono correlate all'allocazione.</span><span class="sxs-lookup"><span data-stu-id="c83d7-110">An embedded instance of the [**Msvm\_ResourcePoolSettingData**](msvm-resourcepoolsettingdata.md) class that is used to specify the pool settings that are not allocation related.</span></span>

</dd> <dt>

<span data-ttu-id="c83d7-111">*ParentPools* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c83d7-111">*ParentPools* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c83d7-112">Matrice di riferimenti [**\_ ResourcePool MSVM**](msvm-resourcepool.md) che rappresentano il pool o i pool da cui creare il nuovo pool.</span><span class="sxs-lookup"><span data-stu-id="c83d7-112">An array of [**Msvm\_ResourcePool**](msvm-resourcepool.md) references that represent the pool or pools from which to create the new pool.</span></span>

</dd> <dt>

<span data-ttu-id="c83d7-113">*AllocationSettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c83d7-113">*AllocationSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c83d7-114">Matrice di una o più istanze incorporate della classe [**MSVM \_ ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) utilizzate per specificare le impostazioni relative all'allocazione del pool.</span><span class="sxs-lookup"><span data-stu-id="c83d7-114">An array of one or more embedded instances of the [**Msvm\_ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) class that are used to specify the pool allocation related settings.</span></span> <span data-ttu-id="c83d7-115">Questa matrice deve contenere un elemento per ogni elemento nella matrice *ParentPools* o esattamente un elemento.</span><span class="sxs-lookup"><span data-stu-id="c83d7-115">This array must contain either one element for each element in the *ParentPools* array, or exactly one element.</span></span> <span data-ttu-id="c83d7-116">Se la matrice contiene un elemento e *ParentPools* contiene più di un elemento, *AlllocationSettings* specifica un'allocazione di capacità condivisa che può essere soddisfatta da uno qualsiasi dei pool padre.</span><span class="sxs-lookup"><span data-stu-id="c83d7-116">If this array contains one element and *ParentPools* contains more than one element, *AlllocationSettings* specifies a shared capacity allocation that can be satisfied by any of the parent pools.</span></span>

<span data-ttu-id="c83d7-117">Viene usato per limitare le risorse che possono essere allocate dall'elemento figlio al pool a un limite inferiore rispetto alla capacità aggregata fornita dagli elementi padre.</span><span class="sxs-lookup"><span data-stu-id="c83d7-117">This is used to restrict the resources that can be allocated from the child to the pool to a lower limit than the aggregate capacity provided by its parents.</span></span> <span data-ttu-id="c83d7-118">Questa opzione non è supportata da tutti i tipi di risorsa.</span><span class="sxs-lookup"><span data-stu-id="c83d7-118">This option is not supported by all resource types.</span></span> <span data-ttu-id="c83d7-119">Se un tipo di risorsa non supporta l'allocazione di capacità condivisa, questo metodo restituirà 32770 (non supportato).</span><span class="sxs-lookup"><span data-stu-id="c83d7-119">If a resource type does not support shared capacity allocation, this method will return 32770 (Not Supported).</span></span>

</dd> <dt>

<span data-ttu-id="c83d7-120">*Pool* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="c83d7-120">*Pool* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c83d7-121">Riferimento al pool risultante.</span><span class="sxs-lookup"><span data-stu-id="c83d7-121">A reference to the resulting pool.</span></span>

</dd> <dt>

<span data-ttu-id="c83d7-122">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="c83d7-122">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c83d7-123">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c83d7-123">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c83d7-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c83d7-124">Return value</span></span>

<span data-ttu-id="c83d7-125">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="c83d7-125">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="c83d7-126">**Processo completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="c83d7-126">**Job Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c83d7-127">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="c83d7-127">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="c83d7-128">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="c83d7-128">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="c83d7-129">**Metodo riservato** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="c83d7-129">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="c83d7-130">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="c83d7-130">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="c83d7-131">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="c83d7-131">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="c83d7-132">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="c83d7-132">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="c83d7-133">**Sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="c83d7-133">**Unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="c83d7-134">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="c83d7-134">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="c83d7-135">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="c83d7-135">**Invalid Parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="c83d7-136">**In uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="c83d7-136">**In Use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="c83d7-137">**Stato non valido** (32775)</span><span class="sxs-lookup"><span data-stu-id="c83d7-137">**Invalid State** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="c83d7-138">**Tipo di risorsa non corretto per il pool** (32776)</span><span class="sxs-lookup"><span data-stu-id="c83d7-138">**Incorrect Resource Type for the Pool** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="c83d7-139">Non **disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="c83d7-139">**Unavailable** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="c83d7-140">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="c83d7-140">**Out of Memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="c83d7-141">**Fornitore riservato** (32779)</span><span class="sxs-lookup"><span data-stu-id="c83d7-141">**Vendor Reserved** (32779)</span></span>
</dt> <dt>

<span data-ttu-id="c83d7-142">**Risorse insufficienti** (32780)</span><span class="sxs-lookup"><span data-stu-id="c83d7-142">**Insufficient Resources** (32780)</span></span>
</dt> <dt>

<span data-ttu-id="c83d7-143">**Oggetto non trovato** (32781.. 32787)</span><span class="sxs-lookup"><span data-stu-id="c83d7-143">**Object Not Found** (32781..32787)</span></span>
</dt> <dt>

<span data-ttu-id="c83d7-144">**Oggetto esistente** (32788)</span><span class="sxs-lookup"><span data-stu-id="c83d7-144">**Object Exists** (32788)</span></span>
</dt> <dt>

<span data-ttu-id="c83d7-145">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="c83d7-145">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="c83d7-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c83d7-146">Requirements</span></span>



| <span data-ttu-id="c83d7-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="c83d7-147">Requirement</span></span> | <span data-ttu-id="c83d7-148">Valore</span><span class="sxs-lookup"><span data-stu-id="c83d7-148">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c83d7-149">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c83d7-149">Minimum supported client</span></span><br/> | <span data-ttu-id="c83d7-150">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="c83d7-150">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c83d7-151">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c83d7-151">Minimum supported server</span></span><br/> | <span data-ttu-id="c83d7-152">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="c83d7-152">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c83d7-153">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c83d7-153">Namespace</span></span><br/>                | <span data-ttu-id="c83d7-154">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="c83d7-154">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c83d7-155">MOF</span><span class="sxs-lookup"><span data-stu-id="c83d7-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c83d7-156"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c83d7-156"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c83d7-157">DLL</span><span class="sxs-lookup"><span data-stu-id="c83d7-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c83d7-158"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c83d7-158"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c83d7-159">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c83d7-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c83d7-160">**\_ResourcePoolConfigurationService MSVM**</span><span class="sxs-lookup"><span data-stu-id="c83d7-160">**Msvm\_ResourcePoolConfigurationService**</span></span>](msvm-resourcepoolconfigurationservice.md)
</dt> </dl>

 

