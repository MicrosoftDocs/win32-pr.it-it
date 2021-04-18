---
description: Rimuove le impostazioni delle risorse virtuali da una configurazione di macchina virtuale.
ms.assetid: 74d9a70a-5258-4e4b-8131-b25513d11a4b
title: Metodo RemoveResourceSettings della classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.RemoveResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 20a7c9fb10e4f7a6356e47f8c743266095de2042
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307866"
---
# <a name="removeresourcesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="7472d-103">Metodo RemoveResourceSettings della classe MSVM \_ VirtualSystemManagementService</span><span class="sxs-lookup"><span data-stu-id="7472d-103">RemoveResourceSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="7472d-104">Rimuove le impostazioni delle risorse virtuali da una configurazione di macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7472d-104">Removes virtual resource settings from a virtual machine configuration.</span></span> <span data-ttu-id="7472d-105">Quando applicato alle parti di una configurazione della macchina virtuale corrente, la macchina virtuale attiva può essere rimossa.</span><span class="sxs-lookup"><span data-stu-id="7472d-105">When applied to parts of a current virtual machine configuration, the active virtual machine may be removed.</span></span>

## <a name="syntax"></a><span data-ttu-id="7472d-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7472d-106">Syntax</span></span>


```mof
uint32 RemoveResourceSettings(
  [in]  CIM_ResourceAllocationSettingData REF ResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="7472d-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="7472d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7472d-108">*ResourceSettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7472d-108">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7472d-109">Matrice di riferimenti a istanze della classe [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) , in cui ogni istanza rappresenta le impostazioni di una risorsa virtuale all'interno di una configurazione di macchina virtuale da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="7472d-109">An array of references to instances of the [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) class, where each instance represents the settings of a virtual resource within a virtual machine configuration that are to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="7472d-110">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="7472d-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7472d-111">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7472d-111">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7472d-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7472d-112">Return value</span></span>

<span data-ttu-id="7472d-113">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="7472d-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="7472d-114">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="7472d-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7472d-115">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="7472d-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="7472d-116">**Non riuscito** (2)</span><span class="sxs-lookup"><span data-stu-id="7472d-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="7472d-117">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="7472d-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="7472d-118">**Parametro non valido** (4)</span><span class="sxs-lookup"><span data-stu-id="7472d-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="7472d-119">**Stato non valido** (5)</span><span class="sxs-lookup"><span data-stu-id="7472d-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="7472d-120">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="7472d-120">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="7472d-121">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="7472d-121">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="7472d-122">**Metodo riservato** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="7472d-122">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="7472d-123">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="7472d-123">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="7472d-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7472d-124">Requirements</span></span>



| <span data-ttu-id="7472d-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="7472d-125">Requirement</span></span> | <span data-ttu-id="7472d-126">Valore</span><span class="sxs-lookup"><span data-stu-id="7472d-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7472d-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7472d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="7472d-128">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="7472d-128">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="7472d-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7472d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="7472d-130">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="7472d-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7472d-131">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7472d-131">Namespace</span></span><br/>                | <span data-ttu-id="7472d-132">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="7472d-132">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="7472d-133">MOF</span><span class="sxs-lookup"><span data-stu-id="7472d-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7472d-134"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7472d-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7472d-135">DLL</span><span class="sxs-lookup"><span data-stu-id="7472d-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7472d-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7472d-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7472d-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7472d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7472d-138">**\_VirtualSystemManagementService MSVM**</span><span class="sxs-lookup"><span data-stu-id="7472d-138">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

