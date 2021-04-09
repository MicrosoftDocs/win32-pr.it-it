---
description: L' \_ associazione CIM PackageInSlot rappresenta la relazione tra le schede dispositivo e lo chassis in cui sono montate.
ms.assetid: 439f28a8-24fd-4a53-9d42-48fabb58e84a
ms.tgt_platform: multiple
title: Classe CIM_PackageInSlot
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PackageInSlot
- CIM_PackageInSlot.Dependent
- CIM_PackageInSlot.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a17e133f16f838d6353b6d74ee2054bd5ec52cd0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126141"
---
# <a name="cim_packageinslot-class"></a><span data-ttu-id="44ae9-103">CIM \_ PackageInSlot (classe)</span><span class="sxs-lookup"><span data-stu-id="44ae9-103">CIM\_PackageInSlot class</span></span>

<span data-ttu-id="44ae9-104">L'associazione **CIM \_ PackageInSlot** rappresenta la relazione tra le schede dispositivo e lo chassis in cui sono montate.</span><span class="sxs-lookup"><span data-stu-id="44ae9-104">The **CIM\_PackageInSlot** association represents the relationship between device cards and the chassis in which they are mounted.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="44ae9-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="44ae9-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="44ae9-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="44ae9-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="44ae9-107">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="44ae9-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="44ae9-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="44ae9-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="44ae9-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="44ae9-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B89-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PackageInSlot : CIM_Dependency
{
  CIM_PhysicalPackage REF Dependent;
  CIM_Slot            REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="44ae9-110">Members</span><span class="sxs-lookup"><span data-stu-id="44ae9-110">Members</span></span>

<span data-ttu-id="44ae9-111">La classe **CIM \_ PackageInSlot** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="44ae9-111">The **CIM\_PackageInSlot** class has these types of members:</span></span>

-   [<span data-ttu-id="44ae9-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="44ae9-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="44ae9-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="44ae9-113">Properties</span></span>

<span data-ttu-id="44ae9-114">La classe **CIM \_ PackageInSlot** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="44ae9-114">The **CIM\_PackageInSlot** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="44ae9-115">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="44ae9-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44ae9-116">Tipo di dati **: \_ slot CIM**</span><span class="sxs-lookup"><span data-stu-id="44ae9-116">Data type: **CIM\_Slot**</span></span>
</dt> <dt>

<span data-ttu-id="44ae9-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="44ae9-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44ae9-118">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="44ae9-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="44ae9-119">Uno [**\_ slot CIM**](cim-slot.md) che descrive lo slot in cui viene inserito il pacchetto fisico.</span><span class="sxs-lookup"><span data-stu-id="44ae9-119">A [**CIM\_Slot**](cim-slot.md) describing the slot into which the physical package is inserted.</span></span>

</dd> <dt>

<span data-ttu-id="44ae9-120">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="44ae9-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44ae9-121">Tipo di dati: **CIM \_ PhysicalPackage**</span><span class="sxs-lookup"><span data-stu-id="44ae9-121">Data type: **CIM\_PhysicalPackage**</span></span>
</dt> <dt>

<span data-ttu-id="44ae9-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="44ae9-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44ae9-123">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente"), [**massimo**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="44ae9-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="44ae9-124">[**\_ PhysicalPackage CIM**](cim-physicalpackage.md) che descrive il pacchetto nello slot.</span><span class="sxs-lookup"><span data-stu-id="44ae9-124">A [**CIM\_PhysicalPackage**](cim-physicalpackage.md) describing the package in the slot.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="44ae9-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="44ae9-125">Remarks</span></span>

<span data-ttu-id="44ae9-126">**CIM \_ PackageInSlot** è derivato dalla [**\_ dipendenza CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="44ae9-126">**CIM\_PackageInSlot** is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="44ae9-127">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="44ae9-127">WMI does not implement this class.</span></span>

<span data-ttu-id="44ae9-128">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="44ae9-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="44ae9-129">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="44ae9-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="44ae9-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="44ae9-130">Requirements</span></span>



| <span data-ttu-id="44ae9-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="44ae9-131">Requirement</span></span> | <span data-ttu-id="44ae9-132">Valore</span><span class="sxs-lookup"><span data-stu-id="44ae9-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="44ae9-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="44ae9-133">Minimum supported client</span></span><br/> | <span data-ttu-id="44ae9-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="44ae9-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="44ae9-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="44ae9-135">Minimum supported server</span></span><br/> | <span data-ttu-id="44ae9-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="44ae9-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="44ae9-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="44ae9-137">Namespace</span></span><br/>                | <span data-ttu-id="44ae9-138">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="44ae9-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="44ae9-139">MOF</span><span class="sxs-lookup"><span data-stu-id="44ae9-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="44ae9-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="44ae9-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="44ae9-141">DLL</span><span class="sxs-lookup"><span data-stu-id="44ae9-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44ae9-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44ae9-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44ae9-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="44ae9-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44ae9-144">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="44ae9-144">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

