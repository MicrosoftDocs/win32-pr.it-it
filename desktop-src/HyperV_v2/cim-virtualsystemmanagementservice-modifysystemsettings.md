---
description: Modifica le impostazioni del sistema virtuale.
ms.assetid: 9c3d28f8-9806-411a-866f-d062c6d31818
title: Metodo ModifySystemSettings della classe CIM_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService.ModifySystemSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: da610d03e683b06ad743d1b6d4fe413dc5b31d34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967156"
---
# <a name="modifysystemsettings-method-of-the-cim_virtualsystemmanagementservice-class"></a><span data-ttu-id="ba5ce-103">Metodo ModifySystemSettings della classe CIM \_ VirtualSystemManagementService</span><span class="sxs-lookup"><span data-stu-id="ba5ce-103">ModifySystemSettings method of the CIM\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="ba5ce-104">Modifica le impostazioni del sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="ba5ce-104">Modifies virtual system settings.</span></span>

<span data-ttu-id="ba5ce-105">Quando applicato alle impostazioni di sistema di una configurazione di sistema virtuale "corrente", come effetto collaterale è possibile che l'istanza di sistema virtuale venga modificata.</span><span class="sxs-lookup"><span data-stu-id="ba5ce-105">When applied to the system settings of a "current" virtual system configuration, as a side effect the virtual system instance may be modified.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba5ce-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ba5ce-106">Syntax</span></span>


```mof
uint32 ModifySystemSettings(
  [in]  string              SystemSettings,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="ba5ce-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="ba5ce-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba5ce-108">*SystemSettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ba5ce-108">*SystemSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba5ce-109">Stringa contenente un'istanza della classe [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) utilizzata per modificare le impostazioni del sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="ba5ce-109">String containing an instance of class [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) that is used to modify the settings of the virtual system.</span></span> <span data-ttu-id="ba5ce-110">Per identificare l'impostazione del sistema virtuale da modificare, l'istanza deve disporre di un **InstanceID** valido.</span><span class="sxs-lookup"><span data-stu-id="ba5ce-110">The instance must have a valid **InstanceID** in order to identify the virtual system setting to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="ba5ce-111">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="ba5ce-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ba5ce-112">Se l'operazione è a esecuzione prolungata, è possibile che venga restituito facoltativamente un [**\_ ConcreteJob CIM**](cim-concretejob.md) che rappresenta il processo.</span><span class="sxs-lookup"><span data-stu-id="ba5ce-112">If the operation is long running, then optionally a [**CIM\_ConcreteJob**](cim-concretejob.md) representing the job may be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba5ce-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ba5ce-113">Return value</span></span>

<span data-ttu-id="ba5ce-114">Restituisce 0 in caso di esito positivo; in caso contrario, restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="ba5ce-114">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="ba5ce-115">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="ba5ce-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ba5ce-116">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="ba5ce-116">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ba5ce-117">**Non riuscito** (2)</span><span class="sxs-lookup"><span data-stu-id="ba5ce-117">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ba5ce-118">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="ba5ce-118">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="ba5ce-119">**Parametro non valido** (4)</span><span class="sxs-lookup"><span data-stu-id="ba5ce-119">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="ba5ce-120">**Stato non valido** (5)</span><span class="sxs-lookup"><span data-stu-id="ba5ce-120">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="ba5ce-121">**Parametri incompatibili** (6)</span><span class="sxs-lookup"><span data-stu-id="ba5ce-121">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="ba5ce-122">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="ba5ce-122">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="ba5ce-123">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="ba5ce-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="ba5ce-124">**Metodo riservato** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="ba5ce-124">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="ba5ce-125">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="ba5ce-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="ba5ce-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ba5ce-126">Requirements</span></span>



| <span data-ttu-id="ba5ce-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba5ce-127">Requirement</span></span> | <span data-ttu-id="ba5ce-128">Valore</span><span class="sxs-lookup"><span data-stu-id="ba5ce-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba5ce-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ba5ce-129">Minimum supported client</span></span><br/> | <span data-ttu-id="ba5ce-130">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="ba5ce-130">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="ba5ce-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ba5ce-131">Minimum supported server</span></span><br/> | <span data-ttu-id="ba5ce-132">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="ba5ce-132">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="ba5ce-133">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ba5ce-133">Namespace</span></span><br/>                | <span data-ttu-id="ba5ce-134">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="ba5ce-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ba5ce-135">MOF</span><span class="sxs-lookup"><span data-stu-id="ba5ce-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ba5ce-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ba5ce-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ba5ce-137">DLL</span><span class="sxs-lookup"><span data-stu-id="ba5ce-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ba5ce-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ba5ce-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ba5ce-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ba5ce-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba5ce-140">**\_VIRTUALSYSTEMMANAGEMENTSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="ba5ce-140">**CIM\_VirtualSystemManagementService**</span></span>](cim-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




