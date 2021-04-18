---
description: Elimina definitivamente un sistema virtuale.
ms.assetid: 8d2504dc-ce23-4257-9dfd-6a35dfd84b2d
title: Metodo DestroySystem della classe CIM_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService.DestroySystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 41355970bb70063b8e90deb8f49b5e6f4b439017
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310551"
---
# <a name="destroysystem-method-of-the-cim_virtualsystemmanagementservice-class"></a><span data-ttu-id="bc201-103">Metodo DestroySystem della classe CIM \_ VirtualSystemManagementService</span><span class="sxs-lookup"><span data-stu-id="bc201-103">DestroySystem method of the CIM\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="bc201-104">Elimina definitivamente un sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="bc201-104">Destroys a virtual system.</span></span>

<span data-ttu-id="bc201-105">Il sistema virtuale a cui si fa riferimento viene eliminato definitivamente, inclusi tutti gli elementi con ambito.</span><span class="sxs-lookup"><span data-stu-id="bc201-105">The referenced virtual system is destroyed, including any elements scoped by it.</span></span> <span data-ttu-id="bc201-106">Le risorse virtuali vengono restituite ai pool di risorse, che possono implicare la distruzione di tali risorse (dipendente dall'implementazione).</span><span class="sxs-lookup"><span data-stu-id="bc201-106">Virtual resources are returned to their resource pools, which may imply the destruction of those resources (implementation dependent).</span></span> <span data-ttu-id="bc201-107">Se il sistema virtuale è attivo quando viene richiamata l'operazione, viene innanzitutto disattivato e quindi eliminato definitivamente.</span><span class="sxs-lookup"><span data-stu-id="bc201-107">If the virtual system is active when the operation is invoked, it is first deactivated and then destroyed.</span></span> <span data-ttu-id="bc201-108">Se sono stati creati snapshot dal sistema virtuale, anche questi vengono eliminati.</span><span class="sxs-lookup"><span data-stu-id="bc201-108">If snapshots were created from the virtual system, these are destroyed as well.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc201-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bc201-109">Syntax</span></span>


```mof
uint32 DestroySystem(
  [in]  CIM_ComputerSystem REF AffectedSystem,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="bc201-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="bc201-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc201-111">*AffectedSystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bc201-111">*AffectedSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc201-112">Riferimento a un'istanza della classe [**CIM \_ ComputerSystem**](cim-computersystem.md) che rappresenta il sistema di computer virtuale da eliminare definitivamente.</span><span class="sxs-lookup"><span data-stu-id="bc201-112">Reference to an instance of class [**CIM\_ComputerSystem**](cim-computersystem.md) representing the virtual computer system that is to be destroyed.</span></span>

</dd> <dt>

<span data-ttu-id="bc201-113">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="bc201-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bc201-114">Se l'operazione è a esecuzione prolungata, è possibile che venga restituito facoltativamente un [**\_ ConcreteJob CIM**](cim-concretejob.md) che rappresenta il processo.</span><span class="sxs-lookup"><span data-stu-id="bc201-114">If the operation is long running, then optionally a [**CIM\_ConcreteJob**](cim-concretejob.md) representing the job may be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc201-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bc201-115">Return value</span></span>

<span data-ttu-id="bc201-116">Restituisce 0 in caso di esito positivo; in caso contrario, restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="bc201-116">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="bc201-117">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="bc201-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="bc201-118">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="bc201-118">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="bc201-119">**Non riuscito** (2)</span><span class="sxs-lookup"><span data-stu-id="bc201-119">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="bc201-120">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="bc201-120">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="bc201-121">**Parametro non valido** (4)</span><span class="sxs-lookup"><span data-stu-id="bc201-121">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="bc201-122">**Stato non valido** (5)</span><span class="sxs-lookup"><span data-stu-id="bc201-122">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="bc201-123">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="bc201-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="bc201-124">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="bc201-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="bc201-125">**Metodo riservato** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="bc201-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="bc201-126">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="bc201-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="bc201-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bc201-127">Requirements</span></span>



| <span data-ttu-id="bc201-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc201-128">Requirement</span></span> | <span data-ttu-id="bc201-129">Valore</span><span class="sxs-lookup"><span data-stu-id="bc201-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc201-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bc201-130">Minimum supported client</span></span><br/> | <span data-ttu-id="bc201-131">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="bc201-131">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="bc201-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bc201-132">Minimum supported server</span></span><br/> | <span data-ttu-id="bc201-133">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="bc201-133">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="bc201-134">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="bc201-134">Namespace</span></span><br/>                | <span data-ttu-id="bc201-135">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="bc201-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="bc201-136">MOF</span><span class="sxs-lookup"><span data-stu-id="bc201-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bc201-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bc201-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bc201-138">DLL</span><span class="sxs-lookup"><span data-stu-id="bc201-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc201-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bc201-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="bc201-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bc201-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc201-141">**\_VIRTUALSYSTEMMANAGEMENTSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="bc201-141">**CIM\_VirtualSystemManagementService**</span></span>](cim-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




