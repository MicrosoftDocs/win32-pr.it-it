---
description: Consente di spostare, migrare o rilocare un sistema virtuale in un sistema di destinazione.
ms.assetid: 3a0be791-4514-4ce2-b4e8-3735bd6ea1d7
title: Metodo MigrateVirtualSystemToSystem della classe Msvm_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.MigrateVirtualSystemToSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: a346596b094b60456af8e2b63865bec1171d99ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344971"
---
# <a name="migratevirtualsystemtosystem-method-of-the-msvm_virtualsystemmigrationservice-class"></a><span data-ttu-id="59175-103">Metodo MigrateVirtualSystemToSystem della classe MSVM \_ VirtualSystemMigrationService</span><span class="sxs-lookup"><span data-stu-id="59175-103">MigrateVirtualSystemToSystem method of the Msvm\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="59175-104">Consente di spostare, migrare o rilocare un sistema virtuale in un sistema di destinazione.</span><span class="sxs-lookup"><span data-stu-id="59175-104">Moves, migrates, or relocates a virtual system to a target system.</span></span>

## <a name="syntax"></a><span data-ttu-id="59175-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="59175-105">Syntax</span></span>


```mof
uint32 MigrateVirtualSystemToSystem(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  CIM_System         REF DestinationSystem,
  [in]  string                 MigrationSettingData,
  [in]  string                 NewSystemSettingData,
  [in]  string                 NewResourceSettingData[],
  [out] CIM_ComputerSystem REF NewComputerSystem,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="59175-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="59175-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59175-107">*ComputerSystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="59175-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59175-108">Riferimento a un'istanza della classe [**MSVM \_ ComputerSystem**](msvm-computersystem.md) che rappresenta il computer virtuale da migrare.</span><span class="sxs-lookup"><span data-stu-id="59175-108">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the virtual computer system to be migrated.</span></span>

</dd> <dt>

<span data-ttu-id="59175-109">*DestinationSystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="59175-109">*DestinationSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59175-110">Riferimento a un'istanza della classe [**MSVM \_ ComputerSystem**](msvm-computersystem.md) che rappresenta il sistema di cui eseguire la migrazione.</span><span class="sxs-lookup"><span data-stu-id="59175-110">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the system to be migrated to.</span></span>

</dd> <dt>

<span data-ttu-id="59175-111">*MigrationSettingData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="59175-111">*MigrationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59175-112">Istanza incorporata della classe [**\_ VirtualSystemMigrationSettingData MSVM**](msvm-virtualsystemmigrationsettingdata.md) che rappresenta le impostazioni per l'operazione di migrazione.</span><span class="sxs-lookup"><span data-stu-id="59175-112">An embedded instance of the [**Msvm\_VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md) class that represents settings for the migration operation.</span></span>

</dd> <dt>

<span data-ttu-id="59175-113">*NewSystemSettingData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="59175-113">*NewSystemSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59175-114">Istanza incorporata della classe [**\_ VirtualSystemSettingData MSVM**](msvm-virtualsystemsettingdata.md) che rappresenta le nuove proprietà applicabili al sistema virtuale dopo la migrazione.</span><span class="sxs-lookup"><span data-stu-id="59175-114">An embedded instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class that represents new properties applicable to the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="59175-115">*NewResourceSettingData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="59175-115">*NewResourceSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59175-116">Matrice di stringhe che contengono un'istanza incorporata della classe [**\_ ResourceAllocationSettingData MSVM**](msvm-resourceallocationsettingdata.md) che rappresenta le nuove proprietà applicabili alle risorse virtuali del sistema virtuale dopo la migrazione.</span><span class="sxs-lookup"><span data-stu-id="59175-116">An array of strings that contain an embedded instance of the [**Msvm\_ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) class that represents the new properties applicable to virtual resources of the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="59175-117">*NewComputerSystem* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="59175-117">*NewComputerSystem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="59175-118">Riferimento a un'istanza della classe [**MSVM \_ ComputerSystem**](msvm-computersystem.md) che rappresenta il nuovo sistema migrato.</span><span class="sxs-lookup"><span data-stu-id="59175-118">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the new migrated system.</span></span>

</dd> <dt>

<span data-ttu-id="59175-119">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="59175-119">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="59175-120">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="59175-120">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59175-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="59175-121">Return value</span></span>

<span data-ttu-id="59175-122">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="59175-122">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="59175-123">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="59175-123">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="59175-124">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="59175-124">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="59175-125">**Non riuscito** (2)</span><span class="sxs-lookup"><span data-stu-id="59175-125">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="59175-126">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="59175-126">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="59175-127">**Parametro non valido** (4)</span><span class="sxs-lookup"><span data-stu-id="59175-127">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="59175-128">**Stato non valido** (5)</span><span class="sxs-lookup"><span data-stu-id="59175-128">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="59175-129">**Parametri incompatibili** (6)</span><span class="sxs-lookup"><span data-stu-id="59175-129">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="59175-130">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="59175-130">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="59175-131">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="59175-131">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="59175-132">**Metodo riservato** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="59175-132">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="59175-133">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="59175-133">**Vendor Specific** (32768..65535 )</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="59175-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="59175-134">Requirements</span></span>



| <span data-ttu-id="59175-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="59175-135">Requirement</span></span> | <span data-ttu-id="59175-136">Valore</span><span class="sxs-lookup"><span data-stu-id="59175-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59175-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="59175-137">Minimum supported client</span></span><br/> | <span data-ttu-id="59175-138">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="59175-138">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="59175-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="59175-139">Minimum supported server</span></span><br/> | <span data-ttu-id="59175-140">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="59175-140">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="59175-141">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="59175-141">Namespace</span></span><br/>                | <span data-ttu-id="59175-142">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="59175-142">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="59175-143">MOF</span><span class="sxs-lookup"><span data-stu-id="59175-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="59175-144"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="59175-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="59175-145">DLL</span><span class="sxs-lookup"><span data-stu-id="59175-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="59175-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="59175-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="59175-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="59175-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59175-148">**\_VirtualSystemMigrationService MSVM**</span><span class="sxs-lookup"><span data-stu-id="59175-148">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

