---
description: Determina se è possibile eseguire la migrazione del sistema virtuale specificato a un sistema di destinazione.
ms.assetid: 2E340737-DEE9-4853-ACD8-BEE2A8C69D6D
title: Metodo CheckVirtualSystemIsMigratableToSystem della classe Msvm_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.CheckVirtualSystemIsMigratableToSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 3e8f294f7e30740e3afab8987c734dbbdbd12acf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305993"
---
# <a name="checkvirtualsystemismigratabletosystem-method-of-the-msvm_virtualsystemmigrationservice-class"></a><span data-ttu-id="3e4e0-103">Metodo CheckVirtualSystemIsMigratableToSystem della classe MSVM \_ VirtualSystemMigrationService</span><span class="sxs-lookup"><span data-stu-id="3e4e0-103">CheckVirtualSystemIsMigratableToSystem method of the Msvm\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="3e4e0-104">Determina se è possibile eseguire la migrazione del sistema virtuale specificato a un sistema di destinazione.</span><span class="sxs-lookup"><span data-stu-id="3e4e0-104">Determines whether the specified virtual system can be migrated to a destination system.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e4e0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3e4e0-105">Syntax</span></span>


```mof
uint32 CheckVirtualSystemIsMigratableToSystem(
  [in]  Msvm_ComputerSystem REF ComputerSystem,
  [in]  Msvm_ComputerSystem REF DestinationSystem,
  [in]  string                  MigrationSettingData,
  [in]  string                  NewSystemSettingData,
  [in]  string                  NewResourceSettingData[],
  [out] boolean                 IsMigratable
);
```



## <a name="parameters"></a><span data-ttu-id="3e4e0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3e4e0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e4e0-107">*ComputerSystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3e4e0-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e4e0-108">Riferimento a un'istanza della classe [**MSVM \_ ComputerSystem**](msvm-computersystem.md) che rappresenta la macchina virtuale di cui verificare la capacità di migrazione.</span><span class="sxs-lookup"><span data-stu-id="3e4e0-108">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the virtual machine to test the migration ability of.</span></span>

</dd> <dt>

<span data-ttu-id="3e4e0-109">*DestinationSystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3e4e0-109">*DestinationSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e4e0-110">Riferimento a un'istanza della classe [**\_ ComputerSystem di MSVM**](msvm-computersystem.md) che rappresenta la macchina virtuale per cui verificare la capacità di migrazione.</span><span class="sxs-lookup"><span data-stu-id="3e4e0-110">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the virtual machine to test the migration ability to.</span></span>

</dd> <dt>

<span data-ttu-id="3e4e0-111">*MigrationSettingData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3e4e0-111">*MigrationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e4e0-112">Istanza incorporata della classe [**\_ VirtualSystemMigrationSettingData MSVM**](msvm-virtualsystemmigrationsettingdata.md) che rappresenta le impostazioni per l'operazione di migrazione.</span><span class="sxs-lookup"><span data-stu-id="3e4e0-112">An embedded instance of the [**Msvm\_VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md) class that represents settings for the migration operation.</span></span>

</dd> <dt>

<span data-ttu-id="3e4e0-113">*NewSystemSettingData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3e4e0-113">*NewSystemSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e4e0-114">Istanza incorporata della classe [**\_ VirtualSystemSettingData MSVM**](msvm-virtualsystemsettingdata.md) che rappresenta le nuove proprietà applicabili al sistema virtuale dopo la migrazione.</span><span class="sxs-lookup"><span data-stu-id="3e4e0-114">An embedded instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class that represents new properties applicable to the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="3e4e0-115">*NewResourceSettingData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3e4e0-115">*NewResourceSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e4e0-116">Matrice di stringhe che contengono un'istanza incorporata della classe [**\_ ResourceAllocationSettingData MSVM**](msvm-resourceallocationsettingdata.md) che rappresenta le nuove proprietà applicabili alle risorse virtuali del sistema virtuale dopo la migrazione.</span><span class="sxs-lookup"><span data-stu-id="3e4e0-116">An array of strings that contain an embedded instance of the [**Msvm\_ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) class that represents the new properties applicable to virtual resources of the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="3e4e0-117">*IsMigratable* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3e4e0-117">*IsMigratable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3e4e0-118">Riceve il risultato del controllo della migrazione che indica se è possibile eseguire correttamente la migrazione del sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="3e4e0-118">Receives the migration check result indicating whether the virtual system can be successfully migrated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e4e0-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3e4e0-119">Return value</span></span>

<span data-ttu-id="3e4e0-120">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="3e4e0-120">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="3e4e0-121">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="3e4e0-121">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3e4e0-122">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="3e4e0-122">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3e4e0-123">**Non riuscito** (2)</span><span class="sxs-lookup"><span data-stu-id="3e4e0-123">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3e4e0-124">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="3e4e0-124">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3e4e0-125">**Parametro non valido** (4)</span><span class="sxs-lookup"><span data-stu-id="3e4e0-125">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="3e4e0-126">**Stato non valido** (5)</span><span class="sxs-lookup"><span data-stu-id="3e4e0-126">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="3e4e0-127">**Parametri incompatibili** (6)</span><span class="sxs-lookup"><span data-stu-id="3e4e0-127">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="3e4e0-128">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="3e4e0-128">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="3e4e0-129">**Metodo riservato** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="3e4e0-129">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="3e4e0-130">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="3e4e0-130">**Vendor Specific** (32768..65535 )</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="3e4e0-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3e4e0-131">Requirements</span></span>



| <span data-ttu-id="3e4e0-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e4e0-132">Requirement</span></span> | <span data-ttu-id="3e4e0-133">Valore</span><span class="sxs-lookup"><span data-stu-id="3e4e0-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e4e0-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3e4e0-134">Minimum supported client</span></span><br/> | <span data-ttu-id="3e4e0-135">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="3e4e0-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="3e4e0-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3e4e0-136">Minimum supported server</span></span><br/> | <span data-ttu-id="3e4e0-137">\[Solo app desktop Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="3e4e0-137">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3e4e0-138">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3e4e0-138">Namespace</span></span><br/>                | <span data-ttu-id="3e4e0-139">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="3e4e0-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3e4e0-140">MOF</span><span class="sxs-lookup"><span data-stu-id="3e4e0-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3e4e0-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3e4e0-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3e4e0-142">DLL</span><span class="sxs-lookup"><span data-stu-id="3e4e0-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e4e0-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3e4e0-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3e4e0-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3e4e0-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e4e0-145">**\_VirtualSystemMigrationService MSVM**</span><span class="sxs-lookup"><span data-stu-id="3e4e0-145">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




