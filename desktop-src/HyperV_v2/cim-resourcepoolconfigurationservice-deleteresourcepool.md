---
description: Avviare un processo per eliminare un pool di risorse.
ms.assetid: af3d9c7c-a825-4568-822d-044b3d92d144
title: Metodo DeleteResourcePool della classe CIM_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService.DeleteResourcePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9cab27df07a6a3a9679cb5e6595b6ba558d8b05e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307776"
---
# <a name="deleteresourcepool-method-of-the-cim_resourcepoolconfigurationservice-class"></a><span data-ttu-id="58772-103">Metodo DeleteResourcePool della classe CIM \_ ResourcePoolConfigurationService</span><span class="sxs-lookup"><span data-stu-id="58772-103">DeleteResourcePool method of the CIM\_ResourcePoolConfigurationService class</span></span>

<span data-ttu-id="58772-104">Avviare un processo per eliminare un pool di risorse.</span><span class="sxs-lookup"><span data-stu-id="58772-104">Start a job to delete a resource pool.</span></span> <span data-ttu-id="58772-105">Nessuna allocazione può essere in attesa o l'eliminazione avrà esito negativo con "in uso".</span><span class="sxs-lookup"><span data-stu-id="58772-105">No allocations may be outstanding or the delete will fail with "In Use."</span></span> <span data-ttu-id="58772-106">Se il pool di risorse è un pool di risorse radice, tutte le risorse host vengono restituite al sistema sottostante.</span><span class="sxs-lookup"><span data-stu-id="58772-106">If the resource pool is a root resource pool, any host resources are returned back to the underlying system.</span></span>

## <a name="syntax"></a><span data-ttu-id="58772-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="58772-107">Syntax</span></span>


```mof
uint32 DeleteResourcePool(
  [in]  CIM_ResourcePool REF Pool,
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="58772-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="58772-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58772-109">*Pool* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="58772-109">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58772-110">Un [**\_ ResourcePool CIM**](cim-resourcepool.md) che fa riferimento al pool da eliminare.</span><span class="sxs-lookup"><span data-stu-id="58772-110">A [**CIM\_ResourcePool**](cim-resourcepool.md) that references to the pool to delete.</span></span>

</dd> <dt>

<span data-ttu-id="58772-111">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="58772-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="58772-112">Un [**\_ ConcreteJob CIM**](cim-concretejob.md) che fa riferimento al processo (può essere **null** se il processo è stato completato).</span><span class="sxs-lookup"><span data-stu-id="58772-112">A [**CIM\_ConcreteJob**](cim-concretejob.md) that references the job (may be **null** if job completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58772-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="58772-113">Return value</span></span>

<span data-ttu-id="58772-114">Restituisce 0 in caso di esito positivo; in caso contrario, restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="58772-114">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="58772-115">**Processo completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="58772-115">**Job Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="58772-116">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="58772-116">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="58772-117">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="58772-117">**Unknown** (2)</span></span>
</dt> <dt>

<span data-ttu-id="58772-118">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="58772-118">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="58772-119">**Non riuscito** (4)</span><span class="sxs-lookup"><span data-stu-id="58772-119">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="58772-120">**Parametro non valido** (5)</span><span class="sxs-lookup"><span data-stu-id="58772-120">**Invalid Parameter** (5)</span></span>
</dt> <dt>

<span data-ttu-id="58772-121">**In uso** (6)</span><span class="sxs-lookup"><span data-stu-id="58772-121">**In Use** (6)</span></span>
</dt> <dt>

<span data-ttu-id="58772-122">**ResourceType errato per il pool** (7)</span><span class="sxs-lookup"><span data-stu-id="58772-122">**Incorrect ResourceType for the Pool** (7)</span></span>
</dt> <dt>

<span data-ttu-id="58772-123">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="58772-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="58772-124">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="58772-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="58772-125">**Metodo riservato** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="58772-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="58772-126">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="58772-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="58772-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="58772-127">Requirements</span></span>



| <span data-ttu-id="58772-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="58772-128">Requirement</span></span> | <span data-ttu-id="58772-129">Valore</span><span class="sxs-lookup"><span data-stu-id="58772-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58772-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="58772-130">Minimum supported client</span></span><br/> | <span data-ttu-id="58772-131">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="58772-131">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="58772-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="58772-132">Minimum supported server</span></span><br/> | <span data-ttu-id="58772-133">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="58772-133">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="58772-134">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="58772-134">Namespace</span></span><br/>                | <span data-ttu-id="58772-135">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="58772-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="58772-136">MOF</span><span class="sxs-lookup"><span data-stu-id="58772-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="58772-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="58772-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="58772-138">DLL</span><span class="sxs-lookup"><span data-stu-id="58772-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58772-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="58772-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="58772-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="58772-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58772-141">**\_RESOURCEPOOLCONFIGURATIONSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="58772-141">**CIM\_ResourcePoolConfigurationService**</span></span>](cim-resourcepoolconfigurationservice.md)
</dt> </dl>

 

 




