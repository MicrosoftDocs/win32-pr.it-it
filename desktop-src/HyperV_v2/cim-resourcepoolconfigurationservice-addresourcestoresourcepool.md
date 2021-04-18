---
description: Avvia un processo per l'aggiunta di risorse a un pool di risorse.
ms.assetid: b163619a-19bd-43d7-ba35-ec4bd8192100
title: Metodo AddResourcesToResourcePool della classe CIM_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService.AddResourcesToResourcePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d3aed59267bd064e95b62431064fbd54bb9168aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307779"
---
# <a name="addresourcestoresourcepool-method-of-the-cim_resourcepoolconfigurationservice-class"></a><span data-ttu-id="ed2b1-103">Metodo AddResourcesToResourcePool della classe CIM \_ ResourcePoolConfigurationService</span><span class="sxs-lookup"><span data-stu-id="ed2b1-103">AddResourcesToResourcePool method of the CIM\_ResourcePoolConfigurationService class</span></span>

<span data-ttu-id="ed2b1-104">Avvia un processo per l'aggiunta di risorse a un pool di risorse.</span><span class="sxs-lookup"><span data-stu-id="ed2b1-104">Starts a job to add resources to a resource pool.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed2b1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ed2b1-105">Syntax</span></span>


```mof
uint32 AddResourcesToResourcePool(
  [in]  CIM_LogicalDevice REF HostResources[],
  [in]  CIM_ResourcePool  REF Pool,
  [out] CIM_ConcreteJob   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="ed2b1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ed2b1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed2b1-107">*HostResources* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ed2b1-107">*HostResources* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed2b1-108">Matrice di istanze [**CIM \_ LogicalDevice**](cim-logicaldevice.md) da aggiungere al pool.</span><span class="sxs-lookup"><span data-stu-id="ed2b1-108">Array of [**CIM\_LogicalDevice**](cim-logicaldevice.md) instances to add to the pool.</span></span>

</dd> <dt>

<span data-ttu-id="ed2b1-109">*Pool* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="ed2b1-109">*Pool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed2b1-110">Un [**\_ ResourcePool CIM**](cim-resourcepool.md) che rappresenta il pool al quale aggiungere le risorse.</span><span class="sxs-lookup"><span data-stu-id="ed2b1-110">A [**CIM\_ResourcePool**](cim-resourcepool.md) that represents the pool to add the resources to.</span></span>

</dd> <dt>

<span data-ttu-id="ed2b1-111">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="ed2b1-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ed2b1-112">Un [**\_ ConcreteJob CIM**](cim-concretejob.md) che fa riferimento al processo (può essere **null** se il processo è stato completato).</span><span class="sxs-lookup"><span data-stu-id="ed2b1-112">A [**CIM\_ConcreteJob**](cim-concretejob.md) that references the job (may be **null** if job completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed2b1-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ed2b1-113">Return value</span></span>

<span data-ttu-id="ed2b1-114">Restituisce 0 in caso di esito positivo; in caso contrario, restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="ed2b1-114">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="ed2b1-115">**Processo completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="ed2b1-115">**Job Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ed2b1-116">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="ed2b1-116">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ed2b1-117">**Sconosciuto** (2)</span><span class="sxs-lookup"><span data-stu-id="ed2b1-117">**Unknown** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ed2b1-118">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="ed2b1-118">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="ed2b1-119">**Non riuscito** (4)</span><span class="sxs-lookup"><span data-stu-id="ed2b1-119">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="ed2b1-120">**Parametro non valido** (5)</span><span class="sxs-lookup"><span data-stu-id="ed2b1-120">**Invalid Parameter** (5)</span></span>
</dt> <dt>

<span data-ttu-id="ed2b1-121">**In uso** (6)</span><span class="sxs-lookup"><span data-stu-id="ed2b1-121">**In Use** (6)</span></span>
</dt> <dt>

<span data-ttu-id="ed2b1-122">**ResourceType errato per il pool** (7)</span><span class="sxs-lookup"><span data-stu-id="ed2b1-122">**Incorrect ResourceType for the Pool** (7)</span></span>
</dt> <dt>

<span data-ttu-id="ed2b1-123">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="ed2b1-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="ed2b1-124">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="ed2b1-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="ed2b1-125">**Dimensioni non supportate** (4097)</span><span class="sxs-lookup"><span data-stu-id="ed2b1-125">**Size Not Supported** (4097)</span></span>
</dt> <dt>

<span data-ttu-id="ed2b1-126">**Metodo riservato** (4098.. 32767)</span><span class="sxs-lookup"><span data-stu-id="ed2b1-126">**Method Reserved** (4098..32767)</span></span>
</dt> <dt>

<span data-ttu-id="ed2b1-127">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="ed2b1-127">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="ed2b1-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ed2b1-128">Requirements</span></span>



| <span data-ttu-id="ed2b1-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed2b1-129">Requirement</span></span> | <span data-ttu-id="ed2b1-130">Valore</span><span class="sxs-lookup"><span data-stu-id="ed2b1-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed2b1-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ed2b1-131">Minimum supported client</span></span><br/> | <span data-ttu-id="ed2b1-132">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="ed2b1-132">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="ed2b1-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ed2b1-133">Minimum supported server</span></span><br/> | <span data-ttu-id="ed2b1-134">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="ed2b1-134">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="ed2b1-135">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ed2b1-135">Namespace</span></span><br/>                | <span data-ttu-id="ed2b1-136">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="ed2b1-136">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ed2b1-137">MOF</span><span class="sxs-lookup"><span data-stu-id="ed2b1-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ed2b1-138"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ed2b1-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ed2b1-139">DLL</span><span class="sxs-lookup"><span data-stu-id="ed2b1-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ed2b1-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ed2b1-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ed2b1-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ed2b1-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed2b1-142">**\_RESOURCEPOOLCONFIGURATIONSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="ed2b1-142">**CIM\_ResourcePoolConfigurationService**</span></span>](cim-resourcepoolconfigurationservice.md)
</dt> </dl>

 

 




