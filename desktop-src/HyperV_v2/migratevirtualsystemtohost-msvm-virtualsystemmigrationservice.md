---
description: Esegue la migrazione di un sistema virtuale o dell'archiviazione di un sistema virtuale a un host di destinazione specificato da un nome host.
ms.assetid: 796b043c-5ac9-4c69-9838-0f415be5a63e
title: Metodo MigrateVirtualSystemToHost della classe Msvm_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.MigrateVirtualSystemToHost
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f46d32f9e1af68cd4256c4eb5adff5c32b8766e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880745"
---
# <a name="migratevirtualsystemtohost-method-of-the-msvm_virtualsystemmigrationservice-class"></a><span data-ttu-id="8bef0-103">Metodo MigrateVirtualSystemToHost della classe MSVM \_ VirtualSystemMigrationService</span><span class="sxs-lookup"><span data-stu-id="8bef0-103">MigrateVirtualSystemToHost method of the Msvm\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="8bef0-104">Esegue la migrazione di un sistema virtuale o dell'archiviazione di un sistema virtuale a un host di destinazione specificato da un nome host.</span><span class="sxs-lookup"><span data-stu-id="8bef0-104">Migrates a virtual system or the storage of a virtual system to a destination host specified by a hostname.</span></span>

## <a name="syntax"></a><span data-ttu-id="8bef0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8bef0-105">Syntax</span></span>


```mof
uint32 MigrateVirtualSystemToHost(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 DestinationHost,
  [in]  string                 MigrationSettingData,
  [in]  string                 NewSystemSettingData,
  [in]  string                 NewResourceSettingData[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="8bef0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8bef0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8bef0-107">*ComputerSystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8bef0-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8bef0-108">Riferimento a un'istanza della classe [**MSVM \_ ComputerSystem**](msvm-computersystem.md) che rappresenta il computer virtuale da migrare.</span><span class="sxs-lookup"><span data-stu-id="8bef0-108">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the virtual computer system to be migrated.</span></span>

</dd> <dt>

<span data-ttu-id="8bef0-109">*DestinationHost* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8bef0-109">*DestinationHost* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8bef0-110">Nome del sistema host per la migrazione.</span><span class="sxs-lookup"><span data-stu-id="8bef0-110">The name of the host system for the migration.</span></span> <span data-ttu-id="8bef0-111">Il formato di questo nome è specificato dalla proprietà **DestinationHostFormatsSupported** della classe [**MSVM \_ VirtualSystemMigrationCapabilities**](msvm-virtualsystemmigrationcapabilities.md) associata a questa classe.</span><span class="sxs-lookup"><span data-stu-id="8bef0-111">The format of this name is specified by the **DestinationHostFormatsSupported** property of the [**Msvm\_VirtualSystemMigrationCapabilities**](msvm-virtualsystemmigrationcapabilities.md) class associated with this class.</span></span>

</dd> <dt>

<span data-ttu-id="8bef0-112">*MigrationSettingData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8bef0-112">*MigrationSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8bef0-113">Istanza incorporata della classe [**\_ VirtualSystemMigrationSettingData MSVM**](msvm-virtualsystemmigrationsettingdata.md) che rappresenta le impostazioni per l'operazione di migrazione.</span><span class="sxs-lookup"><span data-stu-id="8bef0-113">An embedded instance of the [**Msvm\_VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md) class that represents settings for the migration operation.</span></span>

</dd> <dt>

<span data-ttu-id="8bef0-114">*NewSystemSettingData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8bef0-114">*NewSystemSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8bef0-115">Istanza incorporata della classe [**\_ VirtualSystemSettingData MSVM**](msvm-virtualsystemsettingdata.md) che rappresenta le nuove proprietà applicabili al sistema virtuale dopo la migrazione.</span><span class="sxs-lookup"><span data-stu-id="8bef0-115">An embedded instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class that represents new properties applicable to the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="8bef0-116">*NewResourceSettingData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8bef0-116">*NewResourceSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8bef0-117">Matrice di stringhe che contengono un'istanza incorporata della classe [**\_ ResourceAllocationSettingData MSVM**](msvm-resourceallocationsettingdata.md) che rappresenta le nuove proprietà applicabili alle risorse virtuali del sistema virtuale dopo la migrazione.</span><span class="sxs-lookup"><span data-stu-id="8bef0-117">An array of strings that contain an embedded instance of the [**Msvm\_ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) class that represents the new properties applicable to virtual resources of the virtual system after it is migrated.</span></span>

</dd> <dt>

<span data-ttu-id="8bef0-118">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="8bef0-118">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8bef0-119">Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8bef0-119">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8bef0-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8bef0-120">Return value</span></span>

<span data-ttu-id="8bef0-121">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="8bef0-121">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="8bef0-122">**Parametri del metodo controllati-processo avviato** (4096)</span><span class="sxs-lookup"><span data-stu-id="8bef0-122">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="8bef0-123">**Non riuscito** (32768)</span><span class="sxs-lookup"><span data-stu-id="8bef0-123">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="8bef0-124">**Accesso negato** (32769)</span><span class="sxs-lookup"><span data-stu-id="8bef0-124">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="8bef0-125">**Non supportato** (32770)</span><span class="sxs-lookup"><span data-stu-id="8bef0-125">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="8bef0-126">**Stato sconosciuto** (32771)</span><span class="sxs-lookup"><span data-stu-id="8bef0-126">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="8bef0-127">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="8bef0-127">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="8bef0-128">**Parametro non valido** (32773)</span><span class="sxs-lookup"><span data-stu-id="8bef0-128">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="8bef0-129">**Sistema in uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="8bef0-129">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="8bef0-130">**Stato non valido per l'operazione** (32775)</span><span class="sxs-lookup"><span data-stu-id="8bef0-130">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="8bef0-131">**Tipo di dati non corretto** (32776)</span><span class="sxs-lookup"><span data-stu-id="8bef0-131">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="8bef0-132">**Sistema non disponibile** (32777)</span><span class="sxs-lookup"><span data-stu-id="8bef0-132">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="8bef0-133">**Memoria insufficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="8bef0-133">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="8bef0-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8bef0-134">Requirements</span></span>



| <span data-ttu-id="8bef0-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="8bef0-135">Requirement</span></span> | <span data-ttu-id="8bef0-136">Valore</span><span class="sxs-lookup"><span data-stu-id="8bef0-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8bef0-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8bef0-137">Minimum supported client</span></span><br/> | <span data-ttu-id="8bef0-138">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="8bef0-138">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="8bef0-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8bef0-139">Minimum supported server</span></span><br/> | <span data-ttu-id="8bef0-140">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="8bef0-140">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8bef0-141">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8bef0-141">Namespace</span></span><br/>                | <span data-ttu-id="8bef0-142">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="8bef0-142">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="8bef0-143">MOF</span><span class="sxs-lookup"><span data-stu-id="8bef0-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8bef0-144"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8bef0-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8bef0-145">DLL</span><span class="sxs-lookup"><span data-stu-id="8bef0-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8bef0-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8bef0-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8bef0-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8bef0-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bef0-148">**\_VirtualSystemMigrationService MSVM**</span><span class="sxs-lookup"><span data-stu-id="8bef0-148">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

