---
description: Associa un sistema virtuale a uno snapshot acquisito dal sistema virtuale.
ms.assetid: CF1C1C04-02BC-4AC3-8327-FEE54ECE8541
title: Classe Msvm_SnapshotOfVirtualSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SnapshotOfVirtualSystem
- Msvm_SnapshotOfVirtualSystem.Antecedent
- Msvm_SnapshotOfVirtualSystem.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bd006093347d7eb9354944409082a0e069b0cd54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967029"
---
# <a name="msvm_snapshotofvirtualsystem-class"></a><span data-ttu-id="c5785-103">\_Classe MSVM SnapshotOfVirtualSystem</span><span class="sxs-lookup"><span data-stu-id="c5785-103">Msvm\_SnapshotOfVirtualSystem class</span></span>

<span data-ttu-id="c5785-104">Associa un sistema virtuale a uno snapshot acquisito dal sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="c5785-104">Associates a virtual system with a snapshot that was captured from the virtual system.</span></span>

<span data-ttu-id="c5785-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="c5785-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5785-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c5785-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SnapshotOfVirtualSystem : CIM_SnapshotOfVirtualSystem
{
  Msvm_ComputerSystem           REF Antecedent;
  Msvm_VirtualSystemSettingData REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="c5785-107">Members</span><span class="sxs-lookup"><span data-stu-id="c5785-107">Members</span></span>

<span data-ttu-id="c5785-108">La **classe \_ SnapshotOfVirtualSystem di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="c5785-108">The **Msvm\_SnapshotOfVirtualSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="c5785-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c5785-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c5785-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c5785-110">Properties</span></span>

<span data-ttu-id="c5785-111">La **classe \_ SnapshotOfVirtualSystem di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="c5785-111">The **Msvm\_SnapshotOfVirtualSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c5785-112">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="c5785-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5785-113">Tipo di dati: **[ **MSVM \_ ComputerSystem**](msvm-computersystem.md)**</span><span class="sxs-lookup"><span data-stu-id="c5785-113">Data type: **[**Msvm\_ComputerSystem**](msvm-computersystem.md)**</span></span>
</dt> <dt>

<span data-ttu-id="c5785-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c5785-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5785-115">Riferimento a un'istanza della classe [**MSVM \_ ComputerSystem**](msvm-computersystem.md) che rappresenta il sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="c5785-115">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the virtual system.</span></span> <span data-ttu-id="c5785-116">Questa proprietà è derivata dalla [**\_ dipendenza CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="c5785-116">This property is derived from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="c5785-117">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="c5785-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5785-118">Tipo di dati: **[ **MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**</span><span class="sxs-lookup"><span data-stu-id="c5785-118">Data type: **[**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**</span></span>
</dt> <dt>

<span data-ttu-id="c5785-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c5785-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c5785-120">Riferimento a un'istanza della classe [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) che rappresenta lo snapshot.</span><span class="sxs-lookup"><span data-stu-id="c5785-120">A reference to an instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class that represents the snapshot.</span></span> <span data-ttu-id="c5785-121">Questa proprietà è derivata dalla [**\_ dipendenza CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="c5785-121">This property is derived from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c5785-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c5785-122">Requirements</span></span>



| <span data-ttu-id="c5785-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5785-123">Requirement</span></span> | <span data-ttu-id="c5785-124">Valore</span><span class="sxs-lookup"><span data-stu-id="c5785-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5785-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c5785-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c5785-126">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="c5785-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c5785-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c5785-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c5785-128">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="c5785-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c5785-129">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c5785-129">Namespace</span></span><br/>                | <span data-ttu-id="c5785-130">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="c5785-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c5785-131">MOF</span><span class="sxs-lookup"><span data-stu-id="c5785-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c5785-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c5785-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c5785-133">DLL</span><span class="sxs-lookup"><span data-stu-id="c5785-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c5785-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c5785-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c5785-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c5785-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5785-136">**\_SNAPSHOTOFVIRTUALSYSTEM CIM**</span><span class="sxs-lookup"><span data-stu-id="c5785-136">**CIM\_SnapshotOfVirtualSystem**</span></span>](cim-snapshotofvirtualsystem.md)
</dt> <dt>

[<span data-ttu-id="c5785-137">**CreateSnapshot**</span><span class="sxs-lookup"><span data-stu-id="c5785-137">**CreateSnapshot**</span></span>](createsnapshot-msvm-virtualsystemsnapshotservice.md)
</dt> </dl>

 

