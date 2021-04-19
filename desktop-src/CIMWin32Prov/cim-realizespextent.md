---
description: L' \_ associazione CIM RealizesPExtent rappresenta la relazione in cui gli extent fisici vengono realizzati su un supporto fisico. Inoltre, viene specificato l'indirizzo iniziale dell'extent fisico sul supporto fisico.
ms.assetid: 9abe1a7d-8463-4d48-8cec-52bf934ad08b
ms.tgt_platform: multiple
title: Classe CIM_RealizesPExtent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RealizesPExtent
- CIM_RealizesPExtent.Dependent
- CIM_RealizesPExtent.Antecedent
- CIM_RealizesPExtent.StartingAddress
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 906861c7bc7a7e09d40d3457d069cdb9dd3a6b11
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304772"
---
# <a name="cim_realizespextent-class"></a><span data-ttu-id="90af8-104">CIM \_ RealizesPExtent (classe)</span><span class="sxs-lookup"><span data-stu-id="90af8-104">CIM\_RealizesPExtent class</span></span>

<span data-ttu-id="90af8-105">L'associazione **CIM \_ RealizesPExtent** rappresenta la relazione in cui gli extent fisici vengono realizzati su un supporto fisico.</span><span class="sxs-lookup"><span data-stu-id="90af8-105">The **CIM\_RealizesPExtent** association represents the relationship in which physical extents are realized on a physical media.</span></span> <span data-ttu-id="90af8-106">Inoltre, viene specificato l'indirizzo iniziale dell'extent fisico sul supporto fisico.</span><span class="sxs-lookup"><span data-stu-id="90af8-106">In addition, the starting address of the physical extent on the physical media is specified.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="90af8-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="90af8-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="90af8-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="90af8-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="90af8-109">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="90af8-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="90af8-110">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="90af8-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="90af8-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="90af8-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B7F-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_RealizesPExtent : CIM_Realizes
{
  CIM_PhysicalExtent REF Dependent;
  CIM_PhysicalMedia  REF Antecedent;
  uint64                 StartingAddress;
};
```

## <a name="members"></a><span data-ttu-id="90af8-112">Members</span><span class="sxs-lookup"><span data-stu-id="90af8-112">Members</span></span>

<span data-ttu-id="90af8-113">La classe **CIM \_ RealizesPExtent** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="90af8-113">The **CIM\_RealizesPExtent** class has these types of members:</span></span>

-   [<span data-ttu-id="90af8-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="90af8-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="90af8-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="90af8-115">Properties</span></span>

<span data-ttu-id="90af8-116">La classe **CIM \_ RealizesPExtent** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="90af8-116">The **CIM\_RealizesPExtent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="90af8-117">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="90af8-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90af8-118">Tipo di dati: **CIM \_ PhysicalMedia**</span><span class="sxs-lookup"><span data-stu-id="90af8-118">Data type: **CIM\_PhysicalMedia**</span></span>
</dt> <dt>

<span data-ttu-id="90af8-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="90af8-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90af8-120">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="90af8-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="90af8-121">Un [**\_ PhysicalMedia CIM**](cim-physicalmedia.md) che descrive il supporto fisico in cui si realizza l'extent.</span><span class="sxs-lookup"><span data-stu-id="90af8-121">A [**CIM\_PhysicalMedia**](cim-physicalmedia.md) that describes the physical media on which the extent is realized.</span></span>

</dd> <dt>

<span data-ttu-id="90af8-122">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="90af8-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90af8-123">Tipo di dati: **CIM \_ PhysicalExtent**</span><span class="sxs-lookup"><span data-stu-id="90af8-123">Data type: **CIM\_PhysicalExtent**</span></span>
</dt> <dt>

<span data-ttu-id="90af8-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="90af8-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="90af8-125">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="90af8-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="90af8-126">Un [**\_ PhysicalExtent CIM**](cim-physicalextent.md) che descrive l'extent fisico che si trova sul supporto.</span><span class="sxs-lookup"><span data-stu-id="90af8-126">A [**CIM\_PhysicalExtent**](cim-physicalextent.md) that describes the physical extent that is located on the media.</span></span>

</dd> <dt>

<span data-ttu-id="90af8-127">**IndirizzoIniziale**</span><span class="sxs-lookup"><span data-stu-id="90af8-127">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="90af8-128">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="90af8-128">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="90af8-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="90af8-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="90af8-130">Indirizzo iniziale sul supporto fisico in cui inizia l'extent fisico.</span><span class="sxs-lookup"><span data-stu-id="90af8-130">Starting address on the physical media where the physical extent begins.</span></span> <span data-ttu-id="90af8-131">L'indirizzo finale dell'extent fisico viene determinato tramite le proprietà **Proprietà NumberOfBlocks** e **blockSize** dell'oggetto [**CIM \_ PhysicalExtent**](cim-physicalextent.md) .</span><span class="sxs-lookup"><span data-stu-id="90af8-131">The ending address of the physical extent is determined using the **NumberOfBlocks** and **BlockSize** properties of the [**CIM\_PhysicalExtent**](cim-physicalextent.md) object.</span></span>

<span data-ttu-id="90af8-132">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="90af8-132">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="90af8-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="90af8-133">Remarks</span></span>

<span data-ttu-id="90af8-134">La classe **CIM \_ RealizesPExtent** è derivata da [**CIM \_ realizzi**](cim-realizes.md).</span><span class="sxs-lookup"><span data-stu-id="90af8-134">The **CIM\_RealizesPExtent** class is derived from [**CIM\_Realizes**](cim-realizes.md).</span></span>

<span data-ttu-id="90af8-135">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="90af8-135">WMI does not implement this class.</span></span>

<span data-ttu-id="90af8-136">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="90af8-136">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="90af8-137">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="90af8-137">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="90af8-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="90af8-138">Requirements</span></span>



| <span data-ttu-id="90af8-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="90af8-139">Requirement</span></span> | <span data-ttu-id="90af8-140">Valore</span><span class="sxs-lookup"><span data-stu-id="90af8-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="90af8-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="90af8-141">Minimum supported client</span></span><br/> | <span data-ttu-id="90af8-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="90af8-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="90af8-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="90af8-143">Minimum supported server</span></span><br/> | <span data-ttu-id="90af8-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="90af8-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="90af8-145">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="90af8-145">Namespace</span></span><br/>                | <span data-ttu-id="90af8-146">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="90af8-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="90af8-147">MOF</span><span class="sxs-lookup"><span data-stu-id="90af8-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="90af8-148"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="90af8-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="90af8-149">DLL</span><span class="sxs-lookup"><span data-stu-id="90af8-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="90af8-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="90af8-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90af8-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="90af8-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90af8-152">**CIM \_ realizza**</span><span class="sxs-lookup"><span data-stu-id="90af8-152">**CIM\_Realizes**</span></span>](cim-realizes.md)
</dt> </dl>

 

