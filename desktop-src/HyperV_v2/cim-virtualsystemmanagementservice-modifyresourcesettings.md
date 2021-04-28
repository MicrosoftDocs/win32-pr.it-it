---
description: 'Metodo ModifyResourceSettings della classe CIM_VirtualSystemManagementService: modifica le impostazioni delle risorse virtuali.'
ms.assetid: 4942f167-0e53-4ae2-b973-4a06b636b44a
title: Metodo ModifyResourceSettings della classe CIM_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService.ModifyResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 26971c80ce6f7d0ffcdcef069d76aef5fdc15138
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112289"
---
# <a name="modifyresourcesettings-method-of-the-cim_virtualsystemmanagementservice-class"></a><span data-ttu-id="37546-103">Metodo ModifyResourceSettings della classe \_ CIM VirtualSystemManagementService</span><span class="sxs-lookup"><span data-stu-id="37546-103">ModifyResourceSettings method of the CIM\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="37546-104">Modifica le impostazioni delle risorse virtuali.</span><span class="sxs-lookup"><span data-stu-id="37546-104">Modifies virtual resource settings.</span></span>

<span data-ttu-id="37546-105">Se applicato a parti di una configurazione del sistema virtuale "corrente", come effetto collaterale le risorse del sistema virtuale attivo possono essere modificate.</span><span class="sxs-lookup"><span data-stu-id="37546-105">When applied to parts of a "current" virtual system configuration, as a side effect resources of the active virtual system may be modified.</span></span>

## <a name="syntax"></a><span data-ttu-id="37546-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="37546-106">Syntax</span></span>


```mof
uint32 ModifyResourceSettings(
  [in]  string                                ResourceSettings[],
  [out] CIM_ResourceAllocationSettingData REF ResultingResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="37546-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="37546-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37546-108">*ResourceSettings* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="37546-108">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37546-109">Matrice di stringhe ognuna delle quali contiene un'istanza incorporata della classe [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) che descrive le modifiche agli aspetti virtuali di una risorsa virtuale esistente.</span><span class="sxs-lookup"><span data-stu-id="37546-109">Array of strings each containing an embedded instance of class [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) that describes modifications to the virtual aspects of an existing virtual resource.</span></span> <span data-ttu-id="37546-110">Tutte le istanze devono avere un **InstanceID valido** per identificare l'impostazione della risorsa virtuale da modificare.</span><span class="sxs-lookup"><span data-stu-id="37546-110">All instances must have a valid **InstanceID** in order to identify the virtual resource setting to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="37546-111">*ResultingResourceSettings* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="37546-111">*ResultingResourceSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="37546-112">Matrice di riferimenti a istanze della classe [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) che rappresentano gli aspetti virtuali delle risorse virtuali modificate.</span><span class="sxs-lookup"><span data-stu-id="37546-112">Array of references to instances of class [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) representing virtual aspects of the modified virtual resources.</span></span>

</dd> <dt>

<span data-ttu-id="37546-113">*Processo* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="37546-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="37546-114">Se l'operazione è a esecuzione lunga, facoltativamente viene restituito un processo.</span><span class="sxs-lookup"><span data-stu-id="37546-114">If the operation is long running, then optionally a job be returned.</span></span> <span data-ttu-id="37546-115">In questo caso, le istanze della classe [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) che rappresentano le impostazioni delle risorse modificate sono disponibili tramite l'associazione **CIM \_ ConreteComponent** dall'istanza della classe [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) che rappresenta la configurazione del sistema virtuale interessata.</span><span class="sxs-lookup"><span data-stu-id="37546-115">In this case, the instances of class [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) representing the modified resource settings are available via association **CIM\_ConreteComponent** from the instance of class [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) representing the affected virtual system configuration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37546-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="37546-116">Return value</span></span>

<span data-ttu-id="37546-117">Restituisce un valore 0 in esito positivo. In caso contrario, restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="37546-117">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="37546-118">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="37546-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="37546-119">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="37546-119">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="37546-120">**Operazione non** riuscita (2)</span><span class="sxs-lookup"><span data-stu-id="37546-120">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="37546-121">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="37546-121">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="37546-122">**Parametro non** valido (4)</span><span class="sxs-lookup"><span data-stu-id="37546-122">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="37546-123">**Stato non valido** (5)</span><span class="sxs-lookup"><span data-stu-id="37546-123">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="37546-124">**Parametri incompatibili** (6)</span><span class="sxs-lookup"><span data-stu-id="37546-124">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="37546-125">**DmTF Reserved** (..)</span><span class="sxs-lookup"><span data-stu-id="37546-125">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="37546-126">**Parametri del metodo verificati - Processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="37546-126">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="37546-127">**Metodo riservato** (4097..32767)</span><span class="sxs-lookup"><span data-stu-id="37546-127">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="37546-128">**Specifico del** fornitore (32768..65535)</span><span class="sxs-lookup"><span data-stu-id="37546-128">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="37546-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="37546-129">Requirements</span></span>



| <span data-ttu-id="37546-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="37546-130">Requirement</span></span> | <span data-ttu-id="37546-131">Valore</span><span class="sxs-lookup"><span data-stu-id="37546-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37546-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="37546-132">Minimum supported client</span></span><br/> | <span data-ttu-id="37546-133">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="37546-133">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="37546-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="37546-134">Minimum supported server</span></span><br/> | <span data-ttu-id="37546-135">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="37546-135">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="37546-136">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="37546-136">Namespace</span></span><br/>                | <span data-ttu-id="37546-137">Virtualizzazione \\ radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="37546-137">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="37546-138">MOF</span><span class="sxs-lookup"><span data-stu-id="37546-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="37546-139"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="37546-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="37546-140">DLL</span><span class="sxs-lookup"><span data-stu-id="37546-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37546-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="37546-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="37546-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="37546-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37546-143">**CIM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="37546-143">**CIM\_VirtualSystemManagementService**</span></span>](cim-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




