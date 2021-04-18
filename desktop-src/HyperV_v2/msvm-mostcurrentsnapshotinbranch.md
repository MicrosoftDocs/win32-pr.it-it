---
description: Associa un'istanza della classe MSVM \_ ComputerSystem o MSVM \_ PlannedComputerSystem che rappresenta un sistema virtuale, con un'istanza della classe MSVM \_ VirtualSystemSettingData che rappresenta lo snapshot del sistema virtuale che rappresenta lo snapshot più recente in un ramo di snapshot dipendenti.
ms.assetid: EEB9D2C1-C463-4EFE-862F-95E8AD8E1753
title: Classe Msvm_MostCurrentSnapshotInBranch
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MostCurrentSnapshotInBranch
- Msvm_MostCurrentSnapshotInBranch.Antecedent
- Msvm_MostCurrentSnapshotInBranch.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d3ed0824fd68670245e2c8d09b73733ff23be16b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318330"
---
# <a name="msvm_mostcurrentsnapshotinbranch-class"></a><span data-ttu-id="7ce58-103">\_Classe MSVM MostCurrentSnapshotInBranch</span><span class="sxs-lookup"><span data-stu-id="7ce58-103">Msvm\_MostCurrentSnapshotInBranch class</span></span>

<span data-ttu-id="7ce58-104">Associa un'istanza della classe [**MSVM \_ ComputerSystem**](msvm-computersystem.md) o [**MSVM \_ PlannedComputerSystem**](msvm-plannedcomputersystem.md) che rappresenta un sistema virtuale, con un'istanza della classe [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) che rappresenta lo snapshot del sistema virtuale che rappresenta lo snapshot più recente in un ramo di snapshot dipendenti.</span><span class="sxs-lookup"><span data-stu-id="7ce58-104">Associates an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) or [**Msvm\_PlannedComputerSystem**](msvm-plannedcomputersystem.md) class representing a virtual system, with an instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class representing the virtual system snapshot that is the most current snapshot in a branch of dependent snapshots.</span></span>

<span data-ttu-id="7ce58-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="7ce58-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ce58-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7ce58-106">Syntax</span></span>

``` syntax
[Association, Experimental, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MostCurrentSnapshotInBranch : CIM_MostCurrentSnapshotInBranch
{
  CIM_ComputerSystem            REF Antecedent;
  Msvm_VirtualSystemSettingData REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="7ce58-107">Members</span><span class="sxs-lookup"><span data-stu-id="7ce58-107">Members</span></span>

<span data-ttu-id="7ce58-108">La **classe \_ MostCurrentSnapshotInBranch di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="7ce58-108">The **Msvm\_MostCurrentSnapshotInBranch** class has these types of members:</span></span>

-   [<span data-ttu-id="7ce58-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7ce58-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7ce58-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7ce58-110">Properties</span></span>

<span data-ttu-id="7ce58-111">La **classe \_ MostCurrentSnapshotInBranch di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="7ce58-111">The **Msvm\_MostCurrentSnapshotInBranch** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7ce58-112">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="7ce58-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ce58-113">Tipo di dati: **[ **CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)**</span><span class="sxs-lookup"><span data-stu-id="7ce58-113">Data type: **[**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)**</span></span>
</dt> <dt>

<span data-ttu-id="7ce58-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7ce58-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ce58-115">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="7ce58-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="7ce58-116">Riferimento a un'istanza della classe [**MSVM \_ ComputerSystem**](msvm-computersystem.md) o [**MSVM \_ PlannedComputerSystem**](msvm-plannedcomputersystem.md) che rappresenta il sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="7ce58-116">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) or [**Msvm\_PlannedComputerSystem**](msvm-plannedcomputersystem.md) class representing the virtual system.</span></span> <span data-ttu-id="7ce58-117">Questa proprietà viene ereditata [**dalla \_ dipendenza CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="7ce58-117">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="7ce58-118">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="7ce58-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ce58-119">Tipo di dati: **[ **MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**</span><span class="sxs-lookup"><span data-stu-id="7ce58-119">Data type: **[**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**</span></span>
</dt> <dt>

<span data-ttu-id="7ce58-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7ce58-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ce58-121">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="7ce58-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="7ce58-122">Riferimento a un'istanza della classe [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) che rappresenta lo snapshot del sistema virtuale che rappresenta lo snapshot più recente in un ramo di snapshot dipendenti.</span><span class="sxs-lookup"><span data-stu-id="7ce58-122">A reference to an instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class that represents the virtual system snapshot that is the most current snapshot in a branch of dependent snapshots.</span></span> <span data-ttu-id="7ce58-123">Questa proprietà viene ereditata [**dalla \_ dipendenza CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="7ce58-123">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7ce58-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7ce58-124">Requirements</span></span>



| <span data-ttu-id="7ce58-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ce58-125">Requirement</span></span> | <span data-ttu-id="7ce58-126">Valore</span><span class="sxs-lookup"><span data-stu-id="7ce58-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ce58-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7ce58-127">Minimum supported client</span></span><br/> | <span data-ttu-id="7ce58-128">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="7ce58-128">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="7ce58-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7ce58-129">Minimum supported server</span></span><br/> | <span data-ttu-id="7ce58-130">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="7ce58-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7ce58-131">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7ce58-131">Namespace</span></span><br/>                | <span data-ttu-id="7ce58-132">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="7ce58-132">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="7ce58-133">MOF</span><span class="sxs-lookup"><span data-stu-id="7ce58-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7ce58-134"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7ce58-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7ce58-135">DLL</span><span class="sxs-lookup"><span data-stu-id="7ce58-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ce58-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7ce58-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

