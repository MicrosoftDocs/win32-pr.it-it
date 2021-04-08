---
description: L'associazione di CIM \_ ancorata rappresenta la relazione tra due chassis. Ad esempio, un portatile (un tipo di chassis) può essere ancorato in una stazione di ancoraggio (un altro tipo di chassis). Questa relazione tipica è descritta in modo esplicito.
ms.assetid: 72cb36bb-f79e-4d1a-a859-4024031e4ebc
ms.tgt_platform: multiple
title: Classe CIM_Docked
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Docked
- CIM_Docked.Dependent
- CIM_Docked.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 899b85d63293861f0a36df3d3c30610f8cff05ac
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748490"
---
# <a name="cim_docked-class"></a><span data-ttu-id="1e174-105">\_Classe con docking CIM</span><span class="sxs-lookup"><span data-stu-id="1e174-105">CIM\_Docked class</span></span>

<span data-ttu-id="1e174-106">L'associazione di **CIM \_ ancorata** rappresenta la relazione tra due chassis.</span><span class="sxs-lookup"><span data-stu-id="1e174-106">The **CIM\_Docked** association represents the relationship between two chassis.</span></span> <span data-ttu-id="1e174-107">Ad esempio, un portatile (un tipo di chassis) può essere ancorato in una stazione di ancoraggio (un altro tipo di chassis).</span><span class="sxs-lookup"><span data-stu-id="1e174-107">For example, a laptop (a type of chassis) can be docked in a docking station (another type of chassis).</span></span> <span data-ttu-id="1e174-108">Questa relazione tipica è descritta in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="1e174-108">This typical relationship is explicitly described.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1e174-109">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="1e174-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="1e174-110">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="1e174-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="1e174-111">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="1e174-111">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e174-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1e174-112">Syntax</span></span>

``` syntax
[Abstract, MappingStrings("MIF.DMTF|Dynamic States|001.2"), UUID("{FAF76B75-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Docked : CIM_Dependency
{
  CIM_Chassis REF Dependent;
  CIM_Chassis REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="1e174-113">Members</span><span class="sxs-lookup"><span data-stu-id="1e174-113">Members</span></span>

<span data-ttu-id="1e174-114">La classe con **\_ docking CIM** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="1e174-114">The **CIM\_Docked** class has these types of members:</span></span>

-   [<span data-ttu-id="1e174-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1e174-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1e174-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1e174-116">Properties</span></span>

<span data-ttu-id="1e174-117">La **classe \_ ancorata CIM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="1e174-117">The **CIM\_Docked** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1e174-118">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="1e174-118">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e174-119">Tipo di dati **: \_ chassis CIM**</span><span class="sxs-lookup"><span data-stu-id="1e174-119">Data type: **CIM\_Chassis**</span></span>
</dt> <dt>

<span data-ttu-id="1e174-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1e174-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1e174-121">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="1e174-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="1e174-122">[**\_ Chassis CIM**](cim-chassis.md) che descrive la stazione di ancoraggio.</span><span class="sxs-lookup"><span data-stu-id="1e174-122">A [**CIM\_Chassis**](cim-chassis.md) describing the docking station.</span></span>

</dd> <dt>

<span data-ttu-id="1e174-123">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="1e174-123">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e174-124">Tipo di dati **: \_ chassis CIM**</span><span class="sxs-lookup"><span data-stu-id="1e174-124">Data type: **CIM\_Chassis**</span></span>
</dt> <dt>

<span data-ttu-id="1e174-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="1e174-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1e174-126">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente"), [**massimo**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="1e174-126">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="1e174-127">Uno [**\_ chassis CIM**](cim-chassis.md) che descrive il computer portatile ancorato.</span><span class="sxs-lookup"><span data-stu-id="1e174-127">A [**CIM\_Chassis**](cim-chassis.md) describing the docked laptop.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1e174-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="1e174-128">Remarks</span></span>

<span data-ttu-id="1e174-129">La classe **CIM \_ ancorata** è derivata dalla [**\_ dipendenza CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="1e174-129">The **CIM\_Docked** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="1e174-130">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="1e174-130">WMI does not implement this class.</span></span>

<span data-ttu-id="1e174-131">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="1e174-131">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="1e174-132">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="1e174-132">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e174-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1e174-133">Requirements</span></span>



| <span data-ttu-id="1e174-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e174-134">Requirement</span></span> | <span data-ttu-id="1e174-135">Valore</span><span class="sxs-lookup"><span data-stu-id="1e174-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1e174-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1e174-136">Minimum supported client</span></span><br/> | <span data-ttu-id="1e174-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1e174-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1e174-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1e174-138">Minimum supported server</span></span><br/> | <span data-ttu-id="1e174-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1e174-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1e174-140">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1e174-140">Namespace</span></span><br/>                | <span data-ttu-id="1e174-141">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="1e174-141">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1e174-142">MOF</span><span class="sxs-lookup"><span data-stu-id="1e174-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1e174-143"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1e174-143"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1e174-144">DLL</span><span class="sxs-lookup"><span data-stu-id="1e174-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e174-145"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e174-145"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e174-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1e174-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e174-147">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="1e174-147">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

