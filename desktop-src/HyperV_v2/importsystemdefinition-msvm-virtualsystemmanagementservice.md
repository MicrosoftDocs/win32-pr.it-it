---
description: Crea un nuovo sistema di computer pianificato in base alla definizione della macchina virtuale specificata.
ms.assetid: 885d399f-5bcf-4f34-b2f1-582cbfcd7c10
title: Metodo ImportSystemDefinition della classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ImportSystemDefinition
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: bb38ab343a3d92fabd1dc44ed100d2d2f7f7bf01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309511"
---
# <a name="importsystemdefinition-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="17214-103">Metodo ImportSystemDefinition della classe MSVM \_ VirtualSystemManagementService</span><span class="sxs-lookup"><span data-stu-id="17214-103">ImportSystemDefinition method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="17214-104">Crea un nuovo sistema di computer pianificato in base alla definizione della macchina virtuale specificata.</span><span class="sxs-lookup"><span data-stu-id="17214-104">Creates a new planned computer system based on the specified virtual machine definition.</span></span>

## <a name="syntax"></a><span data-ttu-id="17214-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="17214-105">Syntax</span></span>


```mof
uint32 ImportSystemDefinition(
  [in]  string                         SystemDefinitionFile,
  [in]  string                         SnapshotFolder,
  [in]  boolean                        GenerateNewSystemIdentifier,
  [out] Msvm_PlannedComputerSystem REF ImportedSystem,
  [out] CIM_ConcreteJob            REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="17214-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="17214-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17214-107">*SystemDefinitionFile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="17214-107">*SystemDefinitionFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17214-108">Percorso completo del file di definizione del sistema (con estensione XML o EXP) che rappresenta la macchina virtuale da importare.</span><span class="sxs-lookup"><span data-stu-id="17214-108">The fully qualified path to the system definition file (.xml or .exp) representing the virtual machine which is to be imported.</span></span> <span data-ttu-id="17214-109">Il file di definizione non deve essere già utilizzato dal sistema host o dalla piattaforma di virtualizzazione.</span><span class="sxs-lookup"><span data-stu-id="17214-109">The definition file must not already be in use by the host system or the virtualization platform.</span></span>

</dd> <dt>

<span data-ttu-id="17214-110">*SnapshotFolder* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="17214-110">*SnapshotFolder* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17214-111">Percorso completo della cartella in cui è possibile trovare le configurazioni dello snapshot per questa macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="17214-111">The fully qualified path to the folder where the snapshot configurations for this virtual machine can be found.</span></span> <span data-ttu-id="17214-112">Verrà eseguita una ricerca nella cartella per individuare gli snapshot a cui fa riferimento la definizione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="17214-112">This folder will be searched in order to locate any snapshots referenced by the virtual machine definition.</span></span> <span data-ttu-id="17214-113">Gli snapshot a cui viene fatto riferimento non trovati in questo percorso devono essere eliminati usando il metodo [**DestroySnapshot**](destroysnapshot-msvm-virtualsystemsnapshotservice.md) o importati usando il metodo [**ImportSnapshotDefinitions**](importsnapshotdefinitions-msvm-virtualsystemmanagementservice.md) prima di realizzare il computer pianificato.</span><span class="sxs-lookup"><span data-stu-id="17214-113">Any referenced snapshots not found in this location must be deleted using the [**DestroySnapshot**](destroysnapshot-msvm-virtualsystemsnapshotservice.md) method, or imported using the [**ImportSnapshotDefinitions**](importsnapshotdefinitions-msvm-virtualsystemmanagementservice.md) method prior to realizing the planned computer system.</span></span>

</dd> <dt>

<span data-ttu-id="17214-114">*GenerateNewSystemIdentifier* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="17214-114">*GenerateNewSystemIdentifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17214-115">Indica se riutilizzare l'identificatore univoco per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="17214-115">Indicates whether to reuse the unique identifier for the virtual machine.</span></span> <span data-ttu-id="17214-116">Se questo parametro è **true**, viene generato un nuovo identificatore di sistema.</span><span class="sxs-lookup"><span data-stu-id="17214-116">If this parameter is **True**, then a new system identifier is generated.</span></span> <span data-ttu-id="17214-117">Se questo parametro è **false**, viene utilizzato l'identificatore di sistema esistente.</span><span class="sxs-lookup"><span data-stu-id="17214-117">If this parameter is **False**, then the existing system identifier is used.</span></span>

</dd> <dt>

<span data-ttu-id="17214-118">*ImportedSystem* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="17214-118">*ImportedSystem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="17214-119">Se l'operazione viene completata in modo sincrono, un riferimento a un oggetto [**\_ PlannedComputerSystem MSVM**](msvm-plannedcomputersystem.md) che rappresenta la macchina virtuale importata.</span><span class="sxs-lookup"><span data-stu-id="17214-119">If the operation completes synchronously, a reference to an [**Msvm\_PlannedComputerSystem**](msvm-plannedcomputersystem.md) object that represents the imported virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="17214-120">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="17214-120">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="17214-121">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="17214-121">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17214-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="17214-122">Return value</span></span>

<span data-ttu-id="17214-123">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="17214-123">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="17214-124">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="17214-124">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="17214-125">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="17214-125">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="17214-126">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="17214-126">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="17214-127">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="17214-127">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="17214-128">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="17214-128">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="17214-129">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="17214-129">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="17214-130">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="17214-130">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="17214-131">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="17214-131">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="17214-132">Il **sistema è in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="17214-132">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="17214-133">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="17214-133">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="17214-134">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="17214-134">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="17214-135">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="17214-135">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="17214-136">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="17214-136">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="17214-137">**File in uso** (32779)</span><span class="sxs-lookup"><span data-stu-id="17214-137">**File in Use** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="17214-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="17214-138">Requirements</span></span>



| <span data-ttu-id="17214-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="17214-139">Requirement</span></span> | <span data-ttu-id="17214-140">Valore</span><span class="sxs-lookup"><span data-stu-id="17214-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17214-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="17214-141">Minimum supported client</span></span><br/> | <span data-ttu-id="17214-142">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="17214-142">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="17214-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="17214-143">Minimum supported server</span></span><br/> | <span data-ttu-id="17214-144">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="17214-144">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="17214-145">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="17214-145">Namespace</span></span><br/>                | <span data-ttu-id="17214-146">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="17214-146">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="17214-147">MOF</span><span class="sxs-lookup"><span data-stu-id="17214-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="17214-148"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="17214-148"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="17214-149">DLL</span><span class="sxs-lookup"><span data-stu-id="17214-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17214-150"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="17214-150"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="17214-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="17214-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17214-152">**\_VirtualSystemManagementService MSVM**</span><span class="sxs-lookup"><span data-stu-id="17214-152">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

