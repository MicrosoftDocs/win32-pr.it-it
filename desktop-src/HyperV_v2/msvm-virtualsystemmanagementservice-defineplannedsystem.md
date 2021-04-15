---
description: Definisce un sistema virtuale pianificato.
ms.assetid: f129554b-e43e-4c3a-8418-d5d810f4c4b5
title: Metodo DefinePlannedSystem della classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.DefinePlannedSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d5e9fa8a49e86850d044216a3d95e3d4dd756fc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525206"
---
# <a name="defineplannedsystem-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="e49e0-103">Metodo DefinePlannedSystem della classe MSVM \_ VirtualSystemManagementService</span><span class="sxs-lookup"><span data-stu-id="e49e0-103">DefinePlannedSystem method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="e49e0-104">Definisce un sistema virtuale pianificato.</span><span class="sxs-lookup"><span data-stu-id="e49e0-104">Defines a planned virtual system.</span></span>

<span data-ttu-id="e49e0-105">L'input non completamente specificato può essere compilato con i valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="e49e0-105">Input that is not completely specified may be filled out with default values.</span></span>

## <a name="syntax"></a><span data-ttu-id="e49e0-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e49e0-106">Syntax</span></span>


```mof
uint32 DefinePlannedSystem(
  [in]  string                           SystemSettings,
  [in]  string                           ResourceSettings[],
  [in]  CIM_VirtualSystemSettingData REF ReferenceConfiguration,
  [out] CIM_ComputerSystem           REF ResultingSystem,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="e49e0-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="e49e0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e49e0-108">*SystemSettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e49e0-108">*SystemSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e49e0-109">Impostazioni di sistema per il sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="e49e0-109">The system settings for the virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="e49e0-110">*ResourceSettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e49e0-110">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e49e0-111">Impostazioni delle risorse per il sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="e49e0-111">The resource settings for the virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="e49e0-112">*ReferenceConfiguration* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e49e0-112">*ReferenceConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e49e0-113">[**\_ VirtualSystemSettingData CIM**](cim-virtualsystemsettingdata.md) contenente la configurazione di riferimento.</span><span class="sxs-lookup"><span data-stu-id="e49e0-113">A [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) containing the reference configuration.</span></span>

</dd> <dt>

<span data-ttu-id="e49e0-114">*ResultingSystem* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e49e0-114">*ResultingSystem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e49e0-115">[**\_ ComputerSystem CIM**](cim-computersystem.md) che contiene il sistema risultante.</span><span class="sxs-lookup"><span data-stu-id="e49e0-115">A [**CIM\_ComputerSystem**](cim-computersystem.md) containing the resulting system.</span></span>

</dd> <dt>

<span data-ttu-id="e49e0-116">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="e49e0-116">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e49e0-117">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e49e0-117">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e49e0-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e49e0-118">Return value</span></span>

<span data-ttu-id="e49e0-119">In caso di esito positivo, restituisce 0 o 4096; in caso contrario, restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="e49e0-119">On success, returns 0 or 4096; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="e49e0-120">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="e49e0-120">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e49e0-121">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="e49e0-121">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="e49e0-122">**Non riuscito** (2)</span><span class="sxs-lookup"><span data-stu-id="e49e0-122">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e49e0-123">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="e49e0-123">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="e49e0-124">**Parametro non valido** (4)</span><span class="sxs-lookup"><span data-stu-id="e49e0-124">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="e49e0-125">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="e49e0-125">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="e49e0-126">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="e49e0-126">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="e49e0-127">**Metodo riservato** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="e49e0-127">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="e49e0-128">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="e49e0-128">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="e49e0-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e49e0-129">Requirements</span></span>



| <span data-ttu-id="e49e0-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="e49e0-130">Requirement</span></span> | <span data-ttu-id="e49e0-131">Valore</span><span class="sxs-lookup"><span data-stu-id="e49e0-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e49e0-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e49e0-132">Minimum supported client</span></span><br/> | <span data-ttu-id="e49e0-133">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="e49e0-133">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="e49e0-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e49e0-134">Minimum supported server</span></span><br/> | <span data-ttu-id="e49e0-135">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="e49e0-135">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="e49e0-136">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e49e0-136">Namespace</span></span><br/>                | <span data-ttu-id="e49e0-137">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="e49e0-137">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e49e0-138">MOF</span><span class="sxs-lookup"><span data-stu-id="e49e0-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e49e0-139"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e49e0-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e49e0-140">DLL</span><span class="sxs-lookup"><span data-stu-id="e49e0-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e49e0-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e49e0-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e49e0-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e49e0-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e49e0-143">**\_VirtualSystemManagementService MSVM**</span><span class="sxs-lookup"><span data-stu-id="e49e0-143">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

