---
description: Cerca nella cartella specificata tutti i file di definizione dello snapshot associati al sistema del computer pianificato specificato e crea un nuovo snapshot nel sistema del computer pianificato per ogni file di definizione associato in questo percorso.
ms.assetid: d240c24b-f788-4ea9-b3bd-af1f75f4f460
title: Metodo ImportSnapshotDefinitions della classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ImportSnapshotDefinitions
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9ebb36b030786ab88eab899190afcc7f3022286a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880214"
---
# <a name="importsnapshotdefinitions-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="552d8-103">Metodo ImportSnapshotDefinitions della classe MSVM \_ VirtualSystemManagementService</span><span class="sxs-lookup"><span data-stu-id="552d8-103">ImportSnapshotDefinitions method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="552d8-104">Cerca nella cartella specificata tutti i file di definizione dello snapshot associati al sistema del computer pianificato specificato e crea un nuovo snapshot nel sistema del computer pianificato per ogni file di definizione associato in questo percorso.</span><span class="sxs-lookup"><span data-stu-id="552d8-104">Searches the specified folder for any snapshot definition files associated with the specified planned computer system, and creates a new snapshot on the planned computer system for every associated definition file in this location.</span></span>

## <a name="syntax"></a><span data-ttu-id="552d8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="552d8-105">Syntax</span></span>


```mof
uint32 ImportSnapshotDefinitions(
  [in]  Msvm_PlannedComputerSystem    REF PlannedSystem,
  [in]  string                            SnapshotFolder,
  [out] Msvm_VirtualSystemSettingData REF ImportedSnapshots[],
  [out] CIM_ConcreteJob               REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="552d8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="552d8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="552d8-107">*PlannedSystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="552d8-107">*PlannedSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="552d8-108">Riferimento a un oggetto [**\_ PlannedComputerSystem MSVM**](msvm-plannedcomputersystem.md) che rappresenta la macchina virtuale pianificata che fa riferimento agli snapshot da importare.</span><span class="sxs-lookup"><span data-stu-id="552d8-108">A reference to an [**Msvm\_PlannedComputerSystem**](msvm-plannedcomputersystem.md) object that represents the planned virtual machine which references the snapshots to be imported.</span></span>

</dd> <dt>

<span data-ttu-id="552d8-109">*SnapshotFolder* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="552d8-109">*SnapshotFolder* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="552d8-110">Percorso completo della cartella in cui è possibile trovare le configurazioni dello snapshot per questa macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="552d8-110">The fully qualified path to the folder where the snapshot configurations for this virtual machine can be found.</span></span>

</dd> <dt>

<span data-ttu-id="552d8-111">*ImportedSnapshots* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="552d8-111">*ImportedSnapshots* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="552d8-112">Se l'operazione viene completata in modo sincrono, una matrice di riferimenti alle istanze [**\_ VirtualSystemSettingData di MSVM**](msvm-virtualsystemsettingdata.md) che rappresentano gli snapshot importati correttamente.</span><span class="sxs-lookup"><span data-stu-id="552d8-112">If the operation completes synchronously, an array of references to the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) instances representing the snapshots which were successfully imported.</span></span>

</dd> <dt>

<span data-ttu-id="552d8-113">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="552d8-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="552d8-114">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="552d8-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="552d8-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="552d8-115">Return value</span></span>

<span data-ttu-id="552d8-116">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="552d8-116">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="552d8-117">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="552d8-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="552d8-118">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="552d8-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="552d8-119">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="552d8-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="552d8-120">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="552d8-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="552d8-121">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="552d8-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="552d8-122">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="552d8-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="552d8-123">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="552d8-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="552d8-124">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="552d8-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="552d8-125">Il **sistema è in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="552d8-125">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="552d8-126">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="552d8-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="552d8-127">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="552d8-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="552d8-128">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="552d8-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="552d8-129">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="552d8-129">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="552d8-130">**File in uso** (32779)</span><span class="sxs-lookup"><span data-stu-id="552d8-130">**File in Use** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="552d8-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="552d8-131">Requirements</span></span>



| <span data-ttu-id="552d8-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="552d8-132">Requirement</span></span> | <span data-ttu-id="552d8-133">Valore</span><span class="sxs-lookup"><span data-stu-id="552d8-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="552d8-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="552d8-134">Minimum supported client</span></span><br/> | <span data-ttu-id="552d8-135">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="552d8-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="552d8-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="552d8-136">Minimum supported server</span></span><br/> | <span data-ttu-id="552d8-137">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="552d8-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="552d8-138">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="552d8-138">Namespace</span></span><br/>                | <span data-ttu-id="552d8-139">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="552d8-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="552d8-140">MOF</span><span class="sxs-lookup"><span data-stu-id="552d8-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="552d8-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="552d8-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="552d8-142">DLL</span><span class="sxs-lookup"><span data-stu-id="552d8-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="552d8-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="552d8-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="552d8-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="552d8-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="552d8-145">**\_VirtualSystemManagementService MSVM**</span><span class="sxs-lookup"><span data-stu-id="552d8-145">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

