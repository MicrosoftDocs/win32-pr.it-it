---
description: La \_ classe CIM ComputerSystemPackage rappresenta un'associazione che definisce in modo esplicito la relazione tra i sistemi di computer unitari e uno o più pacchetti fisici.
ms.assetid: a91bf09d-0768-4d2a-a0e5-16237b2e6ddc
ms.tgt_platform: multiple
title: Classe CIM_ComputerSystemPackage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ComputerSystemPackage
- CIM_ComputerSystemPackage.Dependent
- CIM_ComputerSystemPackage.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a5a2f166c4494b6120bfc5e2aaedeaba4721b155
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966201"
---
# <a name="cim_computersystempackage-class"></a><span data-ttu-id="5b381-103">CIM \_ ComputerSystemPackage (classe)</span><span class="sxs-lookup"><span data-stu-id="5b381-103">CIM\_ComputerSystemPackage class</span></span>

<span data-ttu-id="5b381-104">La classe **CIM \_ ComputerSystemPackage** rappresenta un'associazione che definisce in modo esplicito la relazione tra i sistemi di computer unitari e uno o più pacchetti fisici.</span><span class="sxs-lookup"><span data-stu-id="5b381-104">The **CIM\_ComputerSystemPackage** class represents an association that explicitly defines the relationship between unitary computer systems and one or more physical packages.</span></span> <span data-ttu-id="5b381-105">L'associazione è simile al modo in cui i dispositivi logici vengono realizzati da elementi fisici.</span><span class="sxs-lookup"><span data-stu-id="5b381-105">The association is similar to the way that logical devices are realized by physical elements.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5b381-106">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="5b381-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="5b381-107">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="5b381-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="5b381-108">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="5b381-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="5b381-109">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="5b381-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b381-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5b381-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B8D-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_ComputerSystemPackage : CIM_Dependency
{
  CIM_UnitaryComputerSystem REF Dependent;
  CIM_PhysicalPackage       REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="5b381-111">Members</span><span class="sxs-lookup"><span data-stu-id="5b381-111">Members</span></span>

<span data-ttu-id="5b381-112">La classe **CIM \_ ComputerSystemPackage** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="5b381-112">The **CIM\_ComputerSystemPackage** class has these types of members:</span></span>

-   [<span data-ttu-id="5b381-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5b381-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5b381-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5b381-114">Properties</span></span>

<span data-ttu-id="5b381-115">La classe **CIM \_ ComputerSystemPackage** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="5b381-115">The **CIM\_ComputerSystemPackage** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5b381-116">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="5b381-116">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b381-117">Tipo di dati: **CIM \_ PhysicalPackage**</span><span class="sxs-lookup"><span data-stu-id="5b381-117">Data type: **CIM\_PhysicalPackage**</span></span>
</dt> <dt>

<span data-ttu-id="5b381-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5b381-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b381-119">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="5b381-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="5b381-120">Un [**\_ PhysicalPackage CIM**](cim-physicalpackage.md) che descrive i pacchetti fisici che realizzano un sistema informatico.</span><span class="sxs-lookup"><span data-stu-id="5b381-120">A [**CIM\_PhysicalPackage**](cim-physicalpackage.md) that describes the physical package(s) that realize a unitary computer system.</span></span>

</dd> <dt>

<span data-ttu-id="5b381-121">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="5b381-121">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5b381-122">Tipo di dati: **CIM \_ UnitaryComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="5b381-122">Data type: **CIM\_UnitaryComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="5b381-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5b381-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5b381-124">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="5b381-124">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="5b381-125">Un [**\_ UnitaryComputerSystem CIM**](cim-unitarycomputersystem.md) che descrive il sistema informatico.</span><span class="sxs-lookup"><span data-stu-id="5b381-125">A [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md) that describes the unitary computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5b381-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="5b381-126">Remarks</span></span>

<span data-ttu-id="5b381-127">La classe **CIM \_ ComputerSystemPackage** è derivata dalla [**\_ dipendenza CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="5b381-127">The **CIM\_ComputerSystemPackage** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="5b381-128">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="5b381-128">WMI does not implement this class.</span></span>

<span data-ttu-id="5b381-129">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="5b381-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="5b381-130">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="5b381-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b381-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5b381-131">Requirements</span></span>



| <span data-ttu-id="5b381-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b381-132">Requirement</span></span> | <span data-ttu-id="5b381-133">Valore</span><span class="sxs-lookup"><span data-stu-id="5b381-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5b381-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5b381-134">Minimum supported client</span></span><br/> | <span data-ttu-id="5b381-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5b381-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5b381-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5b381-136">Minimum supported server</span></span><br/> | <span data-ttu-id="5b381-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5b381-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5b381-138">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5b381-138">Namespace</span></span><br/>                | <span data-ttu-id="5b381-139">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="5b381-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5b381-140">MOF</span><span class="sxs-lookup"><span data-stu-id="5b381-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5b381-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5b381-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5b381-142">DLL</span><span class="sxs-lookup"><span data-stu-id="5b381-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5b381-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b381-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b381-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5b381-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b381-145">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="5b381-145">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

