---
description: Determina se è possibile eseguire la migrazione del sistema virtuale specificato a un host di destinazione specificato da un nome di rete o un indirizzo IP.
ms.assetid: eacc8448-4683-48df-81b9-8599292944db
title: Metodo CheckVirtualSystemIsMigratableToHost della classe Msvm_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.CheckVirtualSystemIsMigratableToHost
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b81f6562f892acbaa5bf7ff7f4f3c772574bd96d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310588"
---
# <a name="checkvirtualsystemismigratabletohost-method-of-the-msvm_virtualsystemmigrationservice-class"></a><span data-ttu-id="1ed53-103">Metodo CheckVirtualSystemIsMigratableToHost della classe MSVM \_ VirtualSystemMigrationService</span><span class="sxs-lookup"><span data-stu-id="1ed53-103">CheckVirtualSystemIsMigratableToHost method of the Msvm\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="1ed53-104">Determina se è possibile eseguire la migrazione del sistema virtuale specificato a un host di destinazione specificato da un nome di rete o un indirizzo IP.</span><span class="sxs-lookup"><span data-stu-id="1ed53-104">Determines whether the specified virtual system can be migrated to a target host specified by a network name or IP address.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ed53-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1ed53-105">Syntax</span></span>


```mof
uint32 CheckVirtualSystemIsMigratableToHost(
  [in]  Msvm_ComputerSystem REF ComputerSystem,
  [in]  string                  DestinationHost,
  [in]  string                  MigrationSettingData,
  [in]  string                  NewSystemSettingData,
  [in]  string                  NewResourceSettingData[],
  [out] boolean                 IsMigratable
);
```



## <a name="parameters"></a><span data-ttu-id="1ed53-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1ed53-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ed53-107">*ComputerSystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1ed53-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ed53-108">Riferimento a un'istanza della classe [**MSVM \_ ComputerSystem**](msvm-computersystem.md) che rappresenta la macchina virtuale di cui verificare la capacità di migrazione.</span><span class="sxs-lookup"><span data-stu-id="1ed53-108">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the virtual machine to test the migration ability of.</span></span>

</dd> <dt>

<span data-ttu-id="1ed53-109">*DestinationHost* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1ed53-109">*DestinationHost* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ed53-110">Nome del sistema host per la migrazione.</span><span class="sxs-lookup"><span data-stu-id="1ed53-110">The name of the host system for the migration.</span></span> <span data-ttu-id="1ed53-111">Il formato di questo nome è specificato dalla proprietà **DestinationHostFormatsSupported** della classe [**MSVM \_ VirtualSystemMigrationCapabilities**](msvm-virtualsystemmigrationcapabilities.md) associata a questa classe.</span><span class="sxs-lookup"><span data-stu-id="1ed53-111">The format of this name is specified by the **DestinationHostFormatsSupported** property of the [**Msvm\_VirtualSystemMigrationCapabilities**](msvm-virtualsystemmigrationcapabilities.md) class associated with this class.</span></span>

</dd> <dt>

<span data-ttu-id="1ed53-112">*MigrationSettingData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1ed53-112">*MigrationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ed53-113">Istanza incorporata della classe [**\_ VirtualSystemMigrationSettingData MSVM**](msvm-virtualsystemmigrationsettingdata.md) che rappresenta le impostazioni per l'operazione di migrazione.</span><span class="sxs-lookup"><span data-stu-id="1ed53-113">An embedded instance of the [**Msvm\_VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md) class that represents settings for the migration operation.</span></span>

</dd> <dt>

<span data-ttu-id="1ed53-114">*NewSystemSettingData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1ed53-114">*NewSystemSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ed53-115">Istanza incorporata della classe [**\_ VirtualSystemSettingData MSVM**](msvm-virtualsystemsettingdata.md) che rappresenta le nuove proprietà applicabili al sistema virtuale dopo la migrazione.</span><span class="sxs-lookup"><span data-stu-id="1ed53-115">An embedded instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class that represents new properties applicable to the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="1ed53-116">*NewResourceSettingData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1ed53-116">*NewResourceSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ed53-117">Matrice di stringhe che contengono un'istanza incorporata della classe [**\_ ResourceAllocationSettingData MSVM**](msvm-resourceallocationsettingdata.md) che rappresenta le nuove proprietà applicabili alle risorse virtuali del sistema virtuale dopo la migrazione.</span><span class="sxs-lookup"><span data-stu-id="1ed53-117">An array of strings that contain an embedded instance of the [**Msvm\_ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) class that represents the new properties applicable to virtual resources of the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="1ed53-118">*IsMigratable* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="1ed53-118">*IsMigratable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1ed53-119">Riceve il risultato del controllo della migrazione che indica se è possibile eseguire correttamente la migrazione del sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="1ed53-119">Receives the migration check result indicating whether the virtual system can be successfully migrated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ed53-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1ed53-120">Return value</span></span>

<span data-ttu-id="1ed53-121">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="1ed53-121">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="1ed53-122">**Completato senza errori** (0)</span><span class="sxs-lookup"><span data-stu-id="1ed53-122">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1ed53-123">**Non supportato** (1)</span><span class="sxs-lookup"><span data-stu-id="1ed53-123">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1ed53-124">**Non riuscito** (2)</span><span class="sxs-lookup"><span data-stu-id="1ed53-124">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1ed53-125">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="1ed53-125">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1ed53-126">**Parametro non valido** (4)</span><span class="sxs-lookup"><span data-stu-id="1ed53-126">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="1ed53-127">**Stato non valido** (5)</span><span class="sxs-lookup"><span data-stu-id="1ed53-127">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="1ed53-128">**Parametri incompatibili** (6)</span><span class="sxs-lookup"><span data-stu-id="1ed53-128">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="1ed53-129">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="1ed53-129">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="1ed53-130">**Metodo riservato** (4097.. 32767)</span><span class="sxs-lookup"><span data-stu-id="1ed53-130">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="1ed53-131">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="1ed53-131">**Vendor Specific** (32768..65535 )</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="1ed53-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1ed53-132">Requirements</span></span>



| <span data-ttu-id="1ed53-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ed53-133">Requirement</span></span> | <span data-ttu-id="1ed53-134">Valore</span><span class="sxs-lookup"><span data-stu-id="1ed53-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ed53-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1ed53-135">Minimum supported client</span></span><br/> | <span data-ttu-id="1ed53-136">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="1ed53-136">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="1ed53-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1ed53-137">Minimum supported server</span></span><br/> | <span data-ttu-id="1ed53-138">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="1ed53-138">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1ed53-139">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1ed53-139">Namespace</span></span><br/>                | <span data-ttu-id="1ed53-140">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="1ed53-140">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="1ed53-141">MOF</span><span class="sxs-lookup"><span data-stu-id="1ed53-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1ed53-142"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1ed53-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1ed53-143">DLL</span><span class="sxs-lookup"><span data-stu-id="1ed53-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1ed53-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1ed53-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1ed53-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1ed53-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ed53-146">**\_VirtualSystemMigrationService MSVM**</span><span class="sxs-lookup"><span data-stu-id="1ed53-146">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




