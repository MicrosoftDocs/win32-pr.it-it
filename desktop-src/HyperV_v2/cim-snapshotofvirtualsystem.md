---
description: Associa un sistema virtuale a uno snapshot del sistema virtuale.
ms.assetid: f85f6914-dbb8-42c9-a732-11d48613c15c
title: Classe CIM_SnapshotOfVirtualSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SnapshotOfVirtualSystem
- CIM_SnapshotOfVirtualSystem.Antecedent
- CIM_SnapshotOfVirtualSystem.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6e8e0929f1198ececea5ea5ec144e2f7313ec35c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967919"
---
# <a name="cim_snapshotofvirtualsystem-class"></a><span data-ttu-id="52886-103">CIM \_ SnapshotOfVirtualSystem (classe)</span><span class="sxs-lookup"><span data-stu-id="52886-103">CIM\_SnapshotOfVirtualSystem class</span></span>

<span data-ttu-id="52886-104">Associa un sistema virtuale a uno snapshot del sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="52886-104">Associates a virtual system a snapshot of the virtual system.</span></span>

## <a name="syntax"></a><span data-ttu-id="52886-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="52886-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.22.0"), AMENDMENT]
class CIM_SnapshotOfVirtualSystem : CIM_Dependency
{
  CIM_ComputerSystem           REF Antecedent;
  CIM_VirtualSystemSettingData REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="52886-106">Members</span><span class="sxs-lookup"><span data-stu-id="52886-106">Members</span></span>

<span data-ttu-id="52886-107">La classe **CIM \_ SnapshotOfVirtualSystem** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="52886-107">The **CIM\_SnapshotOfVirtualSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="52886-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="52886-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="52886-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="52886-109">Properties</span></span>

<span data-ttu-id="52886-110">La classe **CIM \_ SnapshotOfVirtualSystem** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="52886-110">The **CIM\_SnapshotOfVirtualSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="52886-111">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="52886-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52886-112">Tipo di dati: **CIM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="52886-112">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="52886-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="52886-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52886-114">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="52886-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="52886-115">Riferimento al sistema del computer che rappresenta il sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="52886-115">A reference to the computer system that represents the virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="52886-116">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="52886-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52886-117">Tipo di dati: **CIM \_ VirtualSystemSettingData**</span><span class="sxs-lookup"><span data-stu-id="52886-117">Data type: **CIM\_VirtualSystemSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="52886-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="52886-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52886-119">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="52886-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="52886-120">Riferimento all'oggetto dati delle impostazioni che rappresenta lo snapshot del sistema virtuale.</span><span class="sxs-lookup"><span data-stu-id="52886-120">A reference to the settings data object that represents the snapshot of the virtual system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="52886-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="52886-121">Requirements</span></span>



| <span data-ttu-id="52886-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="52886-122">Requirement</span></span> | <span data-ttu-id="52886-123">Valore</span><span class="sxs-lookup"><span data-stu-id="52886-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52886-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="52886-124">Minimum supported client</span></span><br/> | <span data-ttu-id="52886-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="52886-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="52886-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="52886-126">Minimum supported server</span></span><br/> | <span data-ttu-id="52886-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="52886-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="52886-128">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="52886-128">Namespace</span></span><br/>                | <span data-ttu-id="52886-129">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="52886-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="52886-130">MOF</span><span class="sxs-lookup"><span data-stu-id="52886-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="52886-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="52886-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="52886-132">DLL</span><span class="sxs-lookup"><span data-stu-id="52886-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="52886-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="52886-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="52886-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="52886-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52886-135">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="52886-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

