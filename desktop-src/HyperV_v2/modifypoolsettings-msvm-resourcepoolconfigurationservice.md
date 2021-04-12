---
description: Modifica le impostazioni di un pool figlio che non sono correlate all'allocazione.
ms.assetid: f60068e0-f333-41e2-8f11-78aa48dfa260
title: Metodo ModifyPoolSettings della classe Msvm_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolConfigurationService.ModifyPoolSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: edc5f48dabfb84554954cc80d9c4e8a20678d34f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232689"
---
# <a name="modifypoolsettings-method-of-the-msvm_resourcepoolconfigurationservice-class"></a><span data-ttu-id="2187d-103">Metodo ModifyPoolSettings della classe MSVM \_ ResourcePoolConfigurationService</span><span class="sxs-lookup"><span data-stu-id="2187d-103">ModifyPoolSettings method of the Msvm\_ResourcePoolConfigurationService class</span></span>

<span data-ttu-id="2187d-104">Modifica le impostazioni di un pool figlio che non sono correlate all'allocazione.</span><span class="sxs-lookup"><span data-stu-id="2187d-104">Changes the settings of a child pool that are not allocation related.</span></span>

## <a name="syntax"></a><span data-ttu-id="2187d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2187d-105">Syntax</span></span>


```mof
uint32 ModifyPoolSettings(
  [in]  CIM_ResourcePool REF ChildPool,
  [in]  string               PoolSettings,
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="2187d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2187d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2187d-107">*ChildPool* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2187d-107">*ChildPool* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2187d-108">Riferimento a un'istanza della classe [**CIM \_ ResourcePool**](cim-resourcepool.md) che rappresenta il pool figlio da modificare.</span><span class="sxs-lookup"><span data-stu-id="2187d-108">A reference to an instance of the [**CIM\_ResourcePool**](cim-resourcepool.md) class that represents the child pool to modify.</span></span>

</dd> <dt>

<span data-ttu-id="2187d-109">*PoolSettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2187d-109">*PoolSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2187d-110">Istanza incorporata della classe [**MSVM \_ ResourcePoolSettingData**](msvm-resourcepoolsettingdata.md) utilizzata per specificare le nuove impostazioni per il pool.</span><span class="sxs-lookup"><span data-stu-id="2187d-110">An embedded instance of the [**Msvm\_ResourcePoolSettingData**](msvm-resourcepoolsettingdata.md) class that is used to specify the new settings for the pool.</span></span>

</dd> <dt>

<span data-ttu-id="2187d-111">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="2187d-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2187d-112">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2187d-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2187d-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2187d-113">Return value</span></span>

<span data-ttu-id="2187d-114">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="2187d-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="2187d-115">**Processo completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="2187d-115">**Job Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2187d-116">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="2187d-116">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="2187d-117">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="2187d-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="2187d-118">**Metodo riservato** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="2187d-118">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="2187d-119">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="2187d-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="2187d-120">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="2187d-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="2187d-121">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="2187d-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="2187d-122">**Sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="2187d-122">**Unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="2187d-123">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="2187d-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="2187d-124">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="2187d-124">**Invalid Parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="2187d-125">**In uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="2187d-125">**In Use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="2187d-126">**Stato non valido** (32775)</span><span class="sxs-lookup"><span data-stu-id="2187d-126">**Invalid State** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="2187d-127">**Tipo di risorsa non corretto per il pool** (32776)</span><span class="sxs-lookup"><span data-stu-id="2187d-127">**Incorrect Resource Type for the Pool** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="2187d-128">Non **disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="2187d-128">**Unavailable** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="2187d-129">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="2187d-129">**Out of Memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="2187d-130">**Fornitore riservato** (32779)</span><span class="sxs-lookup"><span data-stu-id="2187d-130">**Vendor Reserved** (32779)</span></span>
</dt> <dt>

<span data-ttu-id="2187d-131">**Risorse insufficienti** (32780)</span><span class="sxs-lookup"><span data-stu-id="2187d-131">**Insufficient Resources** (32780)</span></span>
</dt> <dt>

<span data-ttu-id="2187d-132">**Oggetto non trovato** (32781.. 32787)</span><span class="sxs-lookup"><span data-stu-id="2187d-132">**Object Not Found** (32781..32787)</span></span>
</dt> <dt>

<span data-ttu-id="2187d-133">**Oggetto esistente** (32788)</span><span class="sxs-lookup"><span data-stu-id="2187d-133">**Object Exists** (32788)</span></span>
</dt> <dt>

<span data-ttu-id="2187d-134">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="2187d-134">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="2187d-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2187d-135">Requirements</span></span>



| <span data-ttu-id="2187d-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="2187d-136">Requirement</span></span> | <span data-ttu-id="2187d-137">Valore</span><span class="sxs-lookup"><span data-stu-id="2187d-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2187d-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2187d-138">Minimum supported client</span></span><br/> | <span data-ttu-id="2187d-139">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="2187d-139">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="2187d-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2187d-140">Minimum supported server</span></span><br/> | <span data-ttu-id="2187d-141">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="2187d-141">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2187d-142">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2187d-142">Namespace</span></span><br/>                | <span data-ttu-id="2187d-143">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="2187d-143">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="2187d-144">MOF</span><span class="sxs-lookup"><span data-stu-id="2187d-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2187d-145"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2187d-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2187d-146">DLL</span><span class="sxs-lookup"><span data-stu-id="2187d-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2187d-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2187d-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2187d-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2187d-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2187d-149">**\_ResourcePoolConfigurationService MSVM**</span><span class="sxs-lookup"><span data-stu-id="2187d-149">**Msvm\_ResourcePoolConfigurationService**</span></span>](msvm-resourcepoolconfigurationservice.md)
</dt> </dl>

 

