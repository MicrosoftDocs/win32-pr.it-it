---
description: Esportare i dati delle impostazioni da passare al metodo ExportSnapshot della classe MSVM \_ CollectionSnapshotService.
ms.assetid: 03b448ed-72bc-485e-bb31-4445c53baa1c
title: Classe Msvm_CollectionSnapshotExportSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotExportSettingData
- Msvm_CollectionSnapshotExportSettingData.CopyVmStorage
- Msvm_CollectionSnapshotExportSettingData.DifferentialBackupBase
- Msvm_CollectionSnapshotExportSettingData.BackupIntent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3e146fe2e2af17223e792d86cff16bf1c4149dd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306636"
---
# <a name="msvm_collectionsnapshotexportsettingdata-class"></a><span data-ttu-id="d39d8-103">\_Classe MSVM CollectionSnapshotExportSettingData</span><span class="sxs-lookup"><span data-stu-id="d39d8-103">Msvm\_CollectionSnapshotExportSettingData class</span></span>

<span data-ttu-id="d39d8-104">Esportare i dati delle impostazioni da passare al metodo ExportSnapshot della classe [**MSVM \_ CollectionSnapshotService**](msvm-collectionsnapshotservice.md) .</span><span class="sxs-lookup"><span data-stu-id="d39d8-104">Export setting data to be passed in to the ExportSnapshot method of [**Msvm\_CollectionSnapshotService**](msvm-collectionsnapshotservice.md) class.</span></span>

<span data-ttu-id="d39d8-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="d39d8-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d39d8-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d39d8-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectionSnapshotExportSettingData : CIM_SettingData
{
  boolean CopyVmStorage;
  string  DifferentialBackupBase;
  uint16  BackupIntent;
};
```

## <a name="members"></a><span data-ttu-id="d39d8-107">Members</span><span class="sxs-lookup"><span data-stu-id="d39d8-107">Members</span></span>

<span data-ttu-id="d39d8-108">La **classe \_ CollectionSnapshotExportSettingData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="d39d8-108">The **Msvm\_CollectionSnapshotExportSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="d39d8-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d39d8-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d39d8-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d39d8-110">Properties</span></span>

<span data-ttu-id="d39d8-111">La **classe \_ CollectionSnapshotExportSettingData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="d39d8-111">The **Msvm\_CollectionSnapshotExportSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d39d8-112">**BackupIntent**</span><span class="sxs-lookup"><span data-stu-id="d39d8-112">**BackupIntent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d39d8-113">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d39d8-113">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d39d8-114">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d39d8-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d39d8-115">Indica l'intenzione di utilizzare i set di backup esportati:</span><span class="sxs-lookup"><span data-stu-id="d39d8-115">Indicates the intent how the exported backup sets would be used:</span></span>

<dt>

<span id="BackupIntentPreserveChain"></span><span id="backupintentpreservechain"></span><span id="BACKUPINTENTPRESERVECHAIN"></span>

<span data-ttu-id="d39d8-116"><span id="BackupIntentPreserveChain"></span><span id="backupintentpreservechain"></span><span id="BACKUPINTENTPRESERVECHAIN"></span>**BackupIntentPreserveChain** (1)</span><span class="sxs-lookup"><span data-stu-id="d39d8-116"><span id="BackupIntentPreserveChain"></span><span id="backupintentpreservechain"></span><span id="BACKUPINTENTPRESERVECHAIN"></span>**BackupIntentPreserveChain** (1)</span></span>


</dt> <dd>

<span data-ttu-id="d39d8-117">Tutti i set di backup completi e differenziali esportati verranno conservati così come sono.</span><span class="sxs-lookup"><span data-stu-id="d39d8-117">All exported full and differential backup sets would be preserved as they are.</span></span>

</dd> <dt>

<span id="BackupIntentMerge"></span><span id="backupintentmerge"></span><span id="BACKUPINTENTMERGE"></span>

<span data-ttu-id="d39d8-118"><span id="BackupIntentMerge"></span><span id="backupintentmerge"></span><span id="BACKUPINTENTMERGE"></span>**BackupIntentMerge** (2)</span><span class="sxs-lookup"><span data-stu-id="d39d8-118"><span id="BackupIntentMerge"></span><span id="backupintentmerge"></span><span id="BACKUPINTENTMERGE"></span>**BackupIntentMerge** (2)</span></span>


</dt> <dd>

<span data-ttu-id="d39d8-119">I set di backup completi e differenziali esportati verranno uniti per sintetizzare set di backup completi.</span><span class="sxs-lookup"><span data-stu-id="d39d8-119">The exported full and differential backup sets would be merged to synthesize full backup sets.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d39d8-120">**CopyVmStorage**</span><span class="sxs-lookup"><span data-stu-id="d39d8-120">**CopyVmStorage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d39d8-121">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="d39d8-121">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d39d8-122">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d39d8-122">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d39d8-123">Se **true**, l'archiviazione della macchina virtuale verrà copiata quando viene esportata la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="d39d8-123">if **true**, the VM storage will be copied when the VM is exported.</span></span> <span data-ttu-id="d39d8-124">In caso contrario, **false.**</span><span class="sxs-lookup"><span data-stu-id="d39d8-124">Otherwise, **false.**</span></span>

</dd> <dt>

<span data-ttu-id="d39d8-125">**DifferentialBackupBase**</span><span class="sxs-lookup"><span data-stu-id="d39d8-125">**DifferentialBackupBase**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d39d8-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="d39d8-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d39d8-127">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="d39d8-127">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d39d8-128">Base per l'esportazione differenziale.</span><span class="sxs-lookup"><span data-stu-id="d39d8-128">Base for differential export.</span></span> <span data-ttu-id="d39d8-129">Si tratta del percorso di un'istanza di [**\_ ReferencePointCollection MSVM**](msvm-referencepointcollection.md) che rappresenta il punto di riferimento oppure il percorso di un'istanza di [**MSVM \_ snapshotcollection**](msvm-snapshotcollection.md) che rappresenta lo snapshot da utilizzare come base per l'esportazione differenziale.</span><span class="sxs-lookup"><span data-stu-id="d39d8-129">This is either path to an [**Msvm\_ReferencePointCollection**](msvm-referencepointcollection.md) instance that represents the reference point, or path to an [**Msvm\_SnapshotCollection**](msvm-snapshotcollection.md) instance that represents the snapshot to be used as a base for differential export.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d39d8-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d39d8-130">Requirements</span></span>



| <span data-ttu-id="d39d8-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="d39d8-131">Requirement</span></span> | <span data-ttu-id="d39d8-132">Valore</span><span class="sxs-lookup"><span data-stu-id="d39d8-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d39d8-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d39d8-133">Minimum supported client</span></span><br/> | <span data-ttu-id="d39d8-134">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="d39d8-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="d39d8-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d39d8-135">Minimum supported server</span></span><br/> | <span data-ttu-id="d39d8-136">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="d39d8-136">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="d39d8-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d39d8-137">Namespace</span></span><br/>                | <span data-ttu-id="d39d8-138">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="d39d8-138">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="d39d8-139">MOF</span><span class="sxs-lookup"><span data-stu-id="d39d8-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d39d8-140"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d39d8-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d39d8-141">DLL</span><span class="sxs-lookup"><span data-stu-id="d39d8-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d39d8-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d39d8-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d39d8-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d39d8-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d39d8-144">**\_SETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="d39d8-144">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

 




