---
description: Fornisce informazioni aggiuntive da utilizzare con il metodo CreateSnapshot della \_ classe VirtualSystemSnapshotService di MSVM.
ms.assetid: d4a025c4-6a3c-4ae0-8f2c-421c1aa1eb23
title: Classe Msvm_VirtualSystemSnapshotSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSnapshotSettingData
- Msvm_VirtualSystemSnapshotSettingData.ConsistencyLevel
- Msvm_VirtualSystemSnapshotSettingData.IgnoreNonSnapshottableDisks
- Msvm_VirtualSystemSnapshotSettingData.GuestBackupType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 32ab52da97e9fcc943c3a70548bb6b1a6d7994a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401608"
---
# <a name="msvm_virtualsystemsnapshotsettingdata-class"></a><span data-ttu-id="96d3a-103">\_Classe MSVM VirtualSystemSnapshotSettingData</span><span class="sxs-lookup"><span data-stu-id="96d3a-103">Msvm\_VirtualSystemSnapshotSettingData class</span></span>

<span data-ttu-id="96d3a-104">Fornisce informazioni aggiuntive da utilizzare con il metodo [**CreateSnapshot**](cim-virtualsystemsnapshotservice-createsnapshot.md) della classe [**\_ VirtualSystemSnapshotService di MSVM**](msvm-virtualsystemsnapshotservice.md) .</span><span class="sxs-lookup"><span data-stu-id="96d3a-104">Provides additional information to be used with the [**CreateSnapshot**](cim-virtualsystemsnapshotservice-createsnapshot.md) method of the [**Msvm\_VirtualSystemSnapshotService**](msvm-virtualsystemsnapshotservice.md) class.</span></span>

<span data-ttu-id="96d3a-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="96d3a-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="96d3a-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="96d3a-106">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_VirtualSystemSnapshotSettingData : CIM_SettingData
{
  uint8   ConsistencyLevel;
  boolean IgnoreNonSnapshottableDisks;
  uint8   GuestBackupType;
};
```

## <a name="members"></a><span data-ttu-id="96d3a-107">Members</span><span class="sxs-lookup"><span data-stu-id="96d3a-107">Members</span></span>

<span data-ttu-id="96d3a-108">La **classe \_ VirtualSystemSnapshotSettingData di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="96d3a-108">The **Msvm\_VirtualSystemSnapshotSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="96d3a-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="96d3a-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="96d3a-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="96d3a-110">Properties</span></span>

<span data-ttu-id="96d3a-111">La **classe \_ VirtualSystemSnapshotSettingData di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="96d3a-111">The **Msvm\_VirtualSystemSnapshotSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="96d3a-112">**ConsistencyLevel**</span><span class="sxs-lookup"><span data-stu-id="96d3a-112">**ConsistencyLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96d3a-113">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="96d3a-113">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="96d3a-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="96d3a-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="96d3a-115">Livello di coerenza dello snapshot.</span><span class="sxs-lookup"><span data-stu-id="96d3a-115">The consistency level of the snapshot.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="96d3a-116">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="96d3a-116">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span data-ttu-id="96d3a-117">**Coerente** con l'applicazione (1)</span><span class="sxs-lookup"><span data-stu-id="96d3a-117">**Application Consistent** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>

<span data-ttu-id="96d3a-118">**Coerente con l'arresto anomalo** (2)</span><span class="sxs-lookup"><span data-stu-id="96d3a-118">**Crash Consistent** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="96d3a-119">**GuestBackupType**</span><span class="sxs-lookup"><span data-stu-id="96d3a-119">**GuestBackupType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96d3a-120">Tipo di dati: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="96d3a-120">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="96d3a-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="96d3a-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="96d3a-122">Tipo di backup da utilizzare nel guest.</span><span class="sxs-lookup"><span data-stu-id="96d3a-122">Backup type to be used inside the guest.</span></span>

> [!Note]  
> <span data-ttu-id="96d3a-123">Proprietà aggiunta in Windows 10, versione 1703</span><span class="sxs-lookup"><span data-stu-id="96d3a-123">Property added in Windows 10, version 1703</span></span>

 

<dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="96d3a-124">**Non definito** (0)</span><span class="sxs-lookup"><span data-stu-id="96d3a-124">**Undefined** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Full"></span><span id="full"></span><span id="FULL"></span>

<span data-ttu-id="96d3a-125">**Completo** (1)</span><span class="sxs-lookup"><span data-stu-id="96d3a-125">**Full** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Copy"></span><span id="copy"></span><span id="COPY"></span>

<span data-ttu-id="96d3a-126">**Copia** (2)</span><span class="sxs-lookup"><span data-stu-id="96d3a-126">**Copy** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="96d3a-127">**IgnoreNonSnapshottableDisks**</span><span class="sxs-lookup"><span data-stu-id="96d3a-127">**IgnoreNonSnapshottableDisks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96d3a-128">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="96d3a-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="96d3a-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="96d3a-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="96d3a-130">Specifica se i dischi non snapshottable come dischi pass-through e dischi Fibre Channel devono essere ignorati durante la creazione dello snapshot.</span><span class="sxs-lookup"><span data-stu-id="96d3a-130">Specifies if non-snapshottable disks like passthrough disks and Fibre Channel Disks are to be ignored while creating the snapshot.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="96d3a-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="96d3a-131">Requirements</span></span>



| <span data-ttu-id="96d3a-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="96d3a-132">Requirement</span></span> | <span data-ttu-id="96d3a-133">Valore</span><span class="sxs-lookup"><span data-stu-id="96d3a-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96d3a-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="96d3a-134">Minimum supported client</span></span><br/> | <span data-ttu-id="96d3a-135">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="96d3a-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="96d3a-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="96d3a-136">Minimum supported server</span></span><br/> | <span data-ttu-id="96d3a-137">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="96d3a-137">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="96d3a-138">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="96d3a-138">Namespace</span></span><br/>                | <span data-ttu-id="96d3a-139">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="96d3a-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="96d3a-140">MOF</span><span class="sxs-lookup"><span data-stu-id="96d3a-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="96d3a-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="96d3a-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="96d3a-142">DLL</span><span class="sxs-lookup"><span data-stu-id="96d3a-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="96d3a-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="96d3a-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="96d3a-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="96d3a-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96d3a-145">**\_SETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="96d3a-145">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

 




