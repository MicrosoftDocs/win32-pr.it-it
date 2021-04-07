---
description: Modifica le impostazioni delle risorse del pool padre per le risorse assegnate a un pool figlio.
ms.assetid: 419fca70-5f15-4593-80ac-ef2af2c3dde5
title: Metodo ModifyPoolResources della classe Msvm_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolConfigurationService.ModifyPoolResources
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2efffdbcc34577f675556874c4153eea2670768c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883714"
---
# <a name="modifypoolresources-method-of-the-msvm_resourcepoolconfigurationservice-class"></a><span data-ttu-id="16b80-103">Metodo ModifyPoolResources della classe MSVM \_ ResourcePoolConfigurationService</span><span class="sxs-lookup"><span data-stu-id="16b80-103">ModifyPoolResources method of the Msvm\_ResourcePoolConfigurationService class</span></span>

<span data-ttu-id="16b80-104">Modifica le impostazioni delle risorse del pool padre per le risorse assegnate a un pool figlio.</span><span class="sxs-lookup"><span data-stu-id="16b80-104">Changes the parent pool resource settings for resources assigned to a child pool.</span></span>

## <a name="syntax"></a><span data-ttu-id="16b80-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="16b80-105">Syntax</span></span>


```mof
uint32 ModifyPoolResources(
  [in]  CIM_ResourcePool REF ChildPool,
  [in]  CIM_ResourcePool REF ParentPools[],
  [in]  string               AllocationSettings[],
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="16b80-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="16b80-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16b80-107">*ChildPool* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="16b80-107">*ChildPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16b80-108">Riferimento a un'istanza della classe [**CIM \_ ResourcePool**](cim-resourcepool.md) che rappresenta il pool figlio da modificare.</span><span class="sxs-lookup"><span data-stu-id="16b80-108">A reference to an instance of the [**CIM\_ResourcePool**](cim-resourcepool.md) class that represents the child pool to modify.</span></span>

</dd> <dt>

<span data-ttu-id="16b80-109">*ParentPools* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="16b80-109">*ParentPools* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16b80-110">Matrice di riferimenti [**CIM \_ ResourcePool**](cim-resourcepool.md) che rappresentano i nuovi pool padre da assegnare al pool figlio.</span><span class="sxs-lookup"><span data-stu-id="16b80-110">An array of [**CIM\_ResourcePool**](cim-resourcepool.md) references that represent the new parent pools to assign to the child pool.</span></span>

</dd> <dt>

<span data-ttu-id="16b80-111">*AllocationSettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="16b80-111">*AllocationSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16b80-112">Matrice facoltativa di una o più istanze incorporate della classe [**MSVM \_ ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) utilizzate per specificare le impostazioni relative all'allocazione del pool.</span><span class="sxs-lookup"><span data-stu-id="16b80-112">An optional array of one or more embedded instances of the [**Msvm\_ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) class that are used to specify the pool allocation related settings.</span></span>

</dd> <dt>

<span data-ttu-id="16b80-113">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="16b80-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="16b80-114">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="16b80-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16b80-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="16b80-115">Return value</span></span>

<span data-ttu-id="16b80-116">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="16b80-116">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="16b80-117">**Processo completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="16b80-117">**Job Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="16b80-118">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="16b80-118">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="16b80-119">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="16b80-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="16b80-120">**Metodo riservato** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="16b80-120">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="16b80-121">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="16b80-121">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="16b80-122">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="16b80-122">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="16b80-123">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="16b80-123">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="16b80-124">**Sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="16b80-124">**Unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="16b80-125">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="16b80-125">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="16b80-126">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="16b80-126">**Invalid Parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="16b80-127">**In uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="16b80-127">**In Use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="16b80-128">**Stato non valido** (32775)</span><span class="sxs-lookup"><span data-stu-id="16b80-128">**Invalid State** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="16b80-129">**Tipo di risorsa non corretto per il pool** (32776)</span><span class="sxs-lookup"><span data-stu-id="16b80-129">**Incorrect Resource Type for the Pool** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="16b80-130">Non **disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="16b80-130">**Unavailable** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="16b80-131">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="16b80-131">**Out of Memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="16b80-132">**Fornitore riservato** (32779)</span><span class="sxs-lookup"><span data-stu-id="16b80-132">**Vendor Reserved** (32779)</span></span>
</dt> <dt>

<span data-ttu-id="16b80-133">**Risorse insufficienti** (32780)</span><span class="sxs-lookup"><span data-stu-id="16b80-133">**Insufficient Resources** (32780)</span></span>
</dt> <dt>

<span data-ttu-id="16b80-134">**Oggetto non trovato** (32781.. 32787)</span><span class="sxs-lookup"><span data-stu-id="16b80-134">**Object Not Found** (32781..32787)</span></span>
</dt> <dt>

<span data-ttu-id="16b80-135">**Oggetto esistente** (32788)</span><span class="sxs-lookup"><span data-stu-id="16b80-135">**Object Exists** (32788)</span></span>
</dt> <dt>

<span data-ttu-id="16b80-136">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="16b80-136">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="16b80-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="16b80-137">Requirements</span></span>



| <span data-ttu-id="16b80-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="16b80-138">Requirement</span></span> | <span data-ttu-id="16b80-139">Valore</span><span class="sxs-lookup"><span data-stu-id="16b80-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16b80-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="16b80-140">Minimum supported client</span></span><br/> | <span data-ttu-id="16b80-141">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="16b80-141">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="16b80-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="16b80-142">Minimum supported server</span></span><br/> | <span data-ttu-id="16b80-143">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="16b80-143">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="16b80-144">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="16b80-144">Namespace</span></span><br/>                | <span data-ttu-id="16b80-145">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="16b80-145">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="16b80-146">MOF</span><span class="sxs-lookup"><span data-stu-id="16b80-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="16b80-147"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="16b80-147"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="16b80-148">DLL</span><span class="sxs-lookup"><span data-stu-id="16b80-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="16b80-149"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="16b80-149"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="16b80-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="16b80-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16b80-151">**\_ResourcePoolConfigurationService MSVM**</span><span class="sxs-lookup"><span data-stu-id="16b80-151">**Msvm\_ResourcePoolConfigurationService**</span></span>](msvm-resourcepoolconfigurationservice.md)
</dt> </dl>

 

