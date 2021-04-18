---
description: Elimina un pool di risorse.
ms.assetid: bc3111a4-9687-49ec-890e-190358230c53
title: Metodo DeletePool della classe Msvm_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolConfigurationService.DeletePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 84273daa0aa30dca8722d90d4fcec22b88325bad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315510"
---
# <a name="deletepool-method-of-the-msvm_resourcepoolconfigurationservice-class"></a><span data-ttu-id="12bfd-103">Metodo DeletePool della classe MSVM \_ ResourcePoolConfigurationService</span><span class="sxs-lookup"><span data-stu-id="12bfd-103">DeletePool method of the Msvm\_ResourcePoolConfigurationService class</span></span>

<span data-ttu-id="12bfd-104">Elimina un pool di risorse.</span><span class="sxs-lookup"><span data-stu-id="12bfd-104">Deletes a resource pool.</span></span> <span data-ttu-id="12bfd-105">Per eliminare correttamente un pool di risorse, nessuna allocazione può essere in attesa o l'eliminazione avrà esito negativo con 32774 (in uso).</span><span class="sxs-lookup"><span data-stu-id="12bfd-105">To successfully delete a resource pool, no allocations can be outstanding or the delete will fail with 32774 (In Use).</span></span> <span data-ttu-id="12bfd-106">Se il pool di risorse è un pool di risorse radice, tutte le risorse host vengono restituite al sistema sottostante.</span><span class="sxs-lookup"><span data-stu-id="12bfd-106">If the resource pool is a root resource pool, any host resources are returned back to the underlying system.</span></span>

## <a name="syntax"></a><span data-ttu-id="12bfd-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="12bfd-107">Syntax</span></span>


```mof
uint32 DeletePool(
  [in]  CIM_ResourcePool REF Pool,
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="12bfd-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="12bfd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12bfd-109">*Pool* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="12bfd-109">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12bfd-110">Riferimento a un'istanza della classe [**CIM \_ ResourcePool**](cim-resourcepool.md) che rappresenta il pool da eliminare.</span><span class="sxs-lookup"><span data-stu-id="12bfd-110">A reference to an instance of the [**CIM\_ResourcePool**](cim-resourcepool.md) class that represents the pool to delete.</span></span>

</dd> <dt>

<span data-ttu-id="12bfd-111">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="12bfd-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="12bfd-112">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="12bfd-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12bfd-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="12bfd-113">Return value</span></span>

<span data-ttu-id="12bfd-114">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="12bfd-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="12bfd-115">**Processo completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="12bfd-115">**Job Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="12bfd-116">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="12bfd-116">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="12bfd-117">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="12bfd-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="12bfd-118">**Metodo riservato** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="12bfd-118">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="12bfd-119">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="12bfd-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="12bfd-120">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="12bfd-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="12bfd-121">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="12bfd-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="12bfd-122">**Sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="12bfd-122">**Unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="12bfd-123">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="12bfd-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="12bfd-124">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="12bfd-124">**Invalid Parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="12bfd-125">**In uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="12bfd-125">**In Use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="12bfd-126">**Stato non valido** (32775)</span><span class="sxs-lookup"><span data-stu-id="12bfd-126">**Invalid State** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="12bfd-127">**Tipo di risorsa non corretto per il pool** (32776)</span><span class="sxs-lookup"><span data-stu-id="12bfd-127">**Incorrect Resource Type for the Pool** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="12bfd-128">Non **disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="12bfd-128">**Unavailable** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="12bfd-129">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="12bfd-129">**Out of Memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="12bfd-130">**Fornitore riservato** (32779)</span><span class="sxs-lookup"><span data-stu-id="12bfd-130">**Vendor Reserved** (32779)</span></span>
</dt> <dt>

<span data-ttu-id="12bfd-131">**Risorse insufficienti** (32780)</span><span class="sxs-lookup"><span data-stu-id="12bfd-131">**Insufficient Resources** (32780)</span></span>
</dt> <dt>

<span data-ttu-id="12bfd-132">**Oggetto non trovato** (32781.. 32787)</span><span class="sxs-lookup"><span data-stu-id="12bfd-132">**Object Not Found** (32781..32787)</span></span>
</dt> <dt>

<span data-ttu-id="12bfd-133">**Oggetto esistente** (32788)</span><span class="sxs-lookup"><span data-stu-id="12bfd-133">**Object Exists** (32788)</span></span>
</dt> <dt>

<span data-ttu-id="12bfd-134">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="12bfd-134">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="12bfd-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="12bfd-135">Requirements</span></span>



| <span data-ttu-id="12bfd-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="12bfd-136">Requirement</span></span> | <span data-ttu-id="12bfd-137">Valore</span><span class="sxs-lookup"><span data-stu-id="12bfd-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12bfd-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="12bfd-138">Minimum supported client</span></span><br/> | <span data-ttu-id="12bfd-139">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="12bfd-139">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="12bfd-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="12bfd-140">Minimum supported server</span></span><br/> | <span data-ttu-id="12bfd-141">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="12bfd-141">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="12bfd-142">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="12bfd-142">Namespace</span></span><br/>                | <span data-ttu-id="12bfd-143">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="12bfd-143">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="12bfd-144">MOF</span><span class="sxs-lookup"><span data-stu-id="12bfd-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="12bfd-145"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="12bfd-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="12bfd-146">DLL</span><span class="sxs-lookup"><span data-stu-id="12bfd-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="12bfd-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="12bfd-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="12bfd-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="12bfd-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12bfd-149">**\_ResourcePoolConfigurationService MSVM**</span><span class="sxs-lookup"><span data-stu-id="12bfd-149">**Msvm\_ResourcePoolConfigurationService**</span></span>](msvm-resourcepoolconfigurationservice.md)
</dt> </dl>

 

