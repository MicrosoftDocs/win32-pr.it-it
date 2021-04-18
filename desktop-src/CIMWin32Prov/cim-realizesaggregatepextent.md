---
description: L' \_ associazione CIM RealizesAggregatePExtent rappresenta la relazione in cui la \_ classe CIM AggregatePExtent è realizzata su un supporto fisico.
ms.assetid: 420dde1d-daa8-4cd3-b3fd-c2aefdc1e217
ms.tgt_platform: multiple
title: Classe CIM_RealizesAggregatePExtent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RealizesAggregatePExtent
- CIM_RealizesAggregatePExtent.Dependent
- CIM_RealizesAggregatePExtent.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: eb80414134534d09a4030e2e87003a660e69fd9f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304774"
---
# <a name="cim_realizesaggregatepextent-class"></a><span data-ttu-id="3d908-103">CIM \_ RealizesAggregatePExtent (classe)</span><span class="sxs-lookup"><span data-stu-id="3d908-103">CIM\_RealizesAggregatePExtent class</span></span>

<span data-ttu-id="3d908-104">L'associazione **CIM \_ RealizesAggregatePExtent** rappresenta la relazione in cui la classe [**CIM \_ AggregatePExtent**](cim-aggregatepextent.md) è realizzata su un supporto fisico.</span><span class="sxs-lookup"><span data-stu-id="3d908-104">The **CIM\_RealizesAggregatePExtent** association represents the relationship in which the [**CIM\_AggregatePExtent**](cim-aggregatepextent.md) class is realized on a physical media.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3d908-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="3d908-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="3d908-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="3d908-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="3d908-107">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="3d908-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="3d908-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="3d908-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d908-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3d908-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B81-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_RealizesAggregatePExtent : CIM_Realizes
{
  CIM_AggregatePExtent REF Dependent;
  CIM_PhysicalMedia    REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="3d908-110">Members</span><span class="sxs-lookup"><span data-stu-id="3d908-110">Members</span></span>

<span data-ttu-id="3d908-111">La classe **CIM \_ RealizesAggregatePExtent** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="3d908-111">The **CIM\_RealizesAggregatePExtent** class has these types of members:</span></span>

-   [<span data-ttu-id="3d908-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3d908-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3d908-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3d908-113">Properties</span></span>

<span data-ttu-id="3d908-114">La classe **CIM \_ RealizesAggregatePExtent** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="3d908-114">The **CIM\_RealizesAggregatePExtent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3d908-115">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="3d908-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d908-116">Tipo di dati: **CIM \_ PhysicalMedia**</span><span class="sxs-lookup"><span data-stu-id="3d908-116">Data type: **CIM\_PhysicalMedia**</span></span>
</dt> <dt>

<span data-ttu-id="3d908-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3d908-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d908-118">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="3d908-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="3d908-119">Un [**\_ PhysicalMedia CIM**](cim-physicalmedia.md) che descrive il supporto fisico in cui si realizza l'extent.</span><span class="sxs-lookup"><span data-stu-id="3d908-119">A [**CIM\_PhysicalMedia**](cim-physicalmedia.md) that describes the physical media on which the extent is realized.</span></span>

</dd> <dt>

<span data-ttu-id="3d908-120">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="3d908-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d908-121">Tipo di dati: **CIM \_ AggregatePExtent**</span><span class="sxs-lookup"><span data-stu-id="3d908-121">Data type: **CIM\_AggregatePExtent**</span></span>
</dt> <dt>

<span data-ttu-id="3d908-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3d908-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d908-123">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="3d908-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="3d908-124">[**\_ AggregatePExtent CIM**](cim-aggregatepextent.md) disponibile sul supporto.</span><span class="sxs-lookup"><span data-stu-id="3d908-124">The [**CIM\_AggregatePExtent**](cim-aggregatepextent.md) that is located on the media.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3d908-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="3d908-125">Remarks</span></span>

<span data-ttu-id="3d908-126">La classe **CIM \_ RealizesAggregatePExtent** è derivata da [**CIM \_ realizzi**](cim-realizes.md).</span><span class="sxs-lookup"><span data-stu-id="3d908-126">The **CIM\_RealizesAggregatePExtent** class is derived from [**CIM\_Realizes**](cim-realizes.md).</span></span>

<span data-ttu-id="3d908-127">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="3d908-127">WMI does not implement this class.</span></span>

<span data-ttu-id="3d908-128">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="3d908-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="3d908-129">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="3d908-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d908-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3d908-130">Requirements</span></span>



| <span data-ttu-id="3d908-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d908-131">Requirement</span></span> | <span data-ttu-id="3d908-132">Valore</span><span class="sxs-lookup"><span data-stu-id="3d908-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3d908-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3d908-133">Minimum supported client</span></span><br/> | <span data-ttu-id="3d908-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3d908-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3d908-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3d908-135">Minimum supported server</span></span><br/> | <span data-ttu-id="3d908-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3d908-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3d908-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3d908-137">Namespace</span></span><br/>                | <span data-ttu-id="3d908-138">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="3d908-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3d908-139">MOF</span><span class="sxs-lookup"><span data-stu-id="3d908-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3d908-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3d908-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3d908-141">DLL</span><span class="sxs-lookup"><span data-stu-id="3d908-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3d908-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d908-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d908-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3d908-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d908-144">**CIM \_ realizza**</span><span class="sxs-lookup"><span data-stu-id="3d908-144">**CIM\_Realizes**</span></span>](cim-realizes.md)
</dt> </dl>

 

