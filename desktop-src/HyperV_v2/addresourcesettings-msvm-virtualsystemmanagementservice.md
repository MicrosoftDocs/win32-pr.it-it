---
description: Aggiunge risorse a una configurazione di macchina virtuale.
ms.assetid: e2878b60-dc8c-48fb-b163-29457a96d130
title: Metodo AddResourceSettings della classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.AddResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4b35379e0fe3925bbf0f7c4d753f77d1d207199b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881869"
---
# <a name="addresourcesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="43509-103">Metodo AddResourceSettings della classe MSVM \_ VirtualSystemManagementService</span><span class="sxs-lookup"><span data-stu-id="43509-103">AddResourceSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="43509-104">Aggiunge risorse a una configurazione di macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="43509-104">Adds resources to a virtual machine configuration.</span></span> <span data-ttu-id="43509-105">Quando viene applicato alla configurazione di una macchina virtuale "state", come effetto collaterale, le risorse vengono aggiunte alla macchina virtuale attiva.</span><span class="sxs-lookup"><span data-stu-id="43509-105">When applied to a "state" virtual machine configuration, as a side effect, resources are added to the active virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="43509-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="43509-106">Syntax</span></span>


```mof
uint32 AddResourceSettings(
  [in]  CIM_VirtualSystemSettingData      REF AffectedConfiguration,
  [in]  string                                ResourceSettings[],
  [out] CIM_ResourceAllocationSettingData REF ResultingResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="43509-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="43509-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43509-108">*AffectedConfiguration* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="43509-108">*AffectedConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43509-109">Riferimento a un oggetto [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)) che rappresenta la configurazione della macchina virtuale interessata.</span><span class="sxs-lookup"><span data-stu-id="43509-109">A reference to a [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) object that represents the affected virtual machine configuration.</span></span>

</dd> <dt>

<span data-ttu-id="43509-110">*ResourceSettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="43509-110">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43509-111">Matrice di stringhe che contengono un'istanza incorporata della classe [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) che descrive gli aspetti virtuali di una risorsa virtuale da aggiungere alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="43509-111">An array of strings that contain one embedded instance of the [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) class that describes the virtual aspects of a virtual resource to be added to the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="43509-112">*ResultingResourceSettings* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="43509-112">*ResultingResourceSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="43509-113">Matrice di riferimenti a istanze della classe [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) che rappresenta gli aspetti virtuali delle risorse virtuali aggiunte.</span><span class="sxs-lookup"><span data-stu-id="43509-113">An array of references to instances of the [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) class that represents virtual aspects of the added virtual resources.</span></span>

</dd> <dt>

<span data-ttu-id="43509-114">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="43509-114">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="43509-115">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="43509-115">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43509-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="43509-116">Return value</span></span>

<span data-ttu-id="43509-117">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="43509-117">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="43509-118">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="43509-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="43509-119">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="43509-119">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="43509-120">**Non riuscito** (2)</span><span class="sxs-lookup"><span data-stu-id="43509-120">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="43509-121">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="43509-121">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="43509-122">**Parametro non valido** (4)</span><span class="sxs-lookup"><span data-stu-id="43509-122">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="43509-123">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="43509-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="43509-124">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="43509-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="43509-125">**Metodo riservato** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="43509-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="43509-126">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="43509-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="43509-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="43509-127">Requirements</span></span>



| <span data-ttu-id="43509-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="43509-128">Requirement</span></span> | <span data-ttu-id="43509-129">Valore</span><span class="sxs-lookup"><span data-stu-id="43509-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43509-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="43509-130">Minimum supported client</span></span><br/> | <span data-ttu-id="43509-131">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="43509-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="43509-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="43509-132">Minimum supported server</span></span><br/> | <span data-ttu-id="43509-133">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="43509-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="43509-134">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="43509-134">Namespace</span></span><br/>                | <span data-ttu-id="43509-135">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="43509-135">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="43509-136">MOF</span><span class="sxs-lookup"><span data-stu-id="43509-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="43509-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="43509-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="43509-138">DLL</span><span class="sxs-lookup"><span data-stu-id="43509-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43509-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="43509-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="43509-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="43509-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43509-141">**\_VirtualSystemManagementService MSVM**</span><span class="sxs-lookup"><span data-stu-id="43509-141">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

