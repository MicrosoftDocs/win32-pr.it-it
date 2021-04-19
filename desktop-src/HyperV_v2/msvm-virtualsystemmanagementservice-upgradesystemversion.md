---
description: Aggiorna il sistema virtuale.
ms.assetid: 4b24aac9-b7b9-460f-9227-fd3c1e960191
title: Metodo UpgradeSystemVersion della classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.UpgradeSystemVersion
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4c34b33da14d8718f2c2414de3aea3079672bbb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305999"
---
# <a name="upgradesystemversion-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="f5541-103">Metodo UpgradeSystemVersion della classe MSVM \_ VirtualSystemManagementService</span><span class="sxs-lookup"><span data-stu-id="f5541-103">UpgradeSystemVersion method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="f5541-104">Aggiorna il sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="f5541-104">Upgrades the virtual system.</span></span>

<span data-ttu-id="f5541-105">Quando applicato alle impostazioni di sistema di una configurazione di sistema virtuale "corrente"</span><span class="sxs-lookup"><span data-stu-id="f5541-105">When applied to the system settings of a "current" virtual system configuration</span></span>

## <a name="syntax"></a><span data-ttu-id="f5541-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f5541-106">Syntax</span></span>


```mof
uint32 UpgradeSystemVersion(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 UpgradeSettingData,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="f5541-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="f5541-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5541-108">*ComputerSystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f5541-108">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5541-109">Riferimento a un [**\_ ComputerSystem CIM**](cim-computersystem.md) che rappresenta il sistema di computer virtuale da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="f5541-109">A reference to a [**CIM\_ComputerSystem**](cim-computersystem.md) that represents the virtual computer system to be upgraded.</span></span>

</dd> <dt>

<span data-ttu-id="f5541-110">*UpgradeSettingData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f5541-110">*UpgradeSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5541-111">Dati dell'impostazione dell'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="f5541-111">The upgrade setting data.</span></span>

</dd> <dt>

<span data-ttu-id="f5541-112">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="f5541-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f5541-113">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f5541-113">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5541-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f5541-114">Return value</span></span>

<span data-ttu-id="f5541-115">In caso di esito positivo, restituisce 0 o 4096; in caso contrario, restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="f5541-115">On success, returns a 0 or 4096; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="f5541-116">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="f5541-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f5541-117">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="f5541-117">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f5541-118">**Non riuscito** (2)</span><span class="sxs-lookup"><span data-stu-id="f5541-118">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f5541-119">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="f5541-119">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f5541-120">**Parametro non valido** (4)</span><span class="sxs-lookup"><span data-stu-id="f5541-120">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f5541-121">**Stato non valido** (5)</span><span class="sxs-lookup"><span data-stu-id="f5541-121">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="f5541-122">**Parametri incompatibili** (6)</span><span class="sxs-lookup"><span data-stu-id="f5541-122">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="f5541-123">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="f5541-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="f5541-124">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="f5541-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="f5541-125">**Metodo riservato** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="f5541-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="f5541-126">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="f5541-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="f5541-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f5541-127">Requirements</span></span>



| <span data-ttu-id="f5541-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5541-128">Requirement</span></span> | <span data-ttu-id="f5541-129">Valore</span><span class="sxs-lookup"><span data-stu-id="f5541-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5541-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f5541-130">Minimum supported client</span></span><br/> | <span data-ttu-id="f5541-131">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="f5541-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="f5541-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f5541-132">Minimum supported server</span></span><br/> | <span data-ttu-id="f5541-133">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="f5541-133">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="f5541-134">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f5541-134">Namespace</span></span><br/>                | <span data-ttu-id="f5541-135">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="f5541-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f5541-136">MOF</span><span class="sxs-lookup"><span data-stu-id="f5541-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f5541-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f5541-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f5541-138">DLL</span><span class="sxs-lookup"><span data-stu-id="f5541-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f5541-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f5541-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f5541-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f5541-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5541-141">**\_VirtualSystemManagementService MSVM**</span><span class="sxs-lookup"><span data-stu-id="f5541-141">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

