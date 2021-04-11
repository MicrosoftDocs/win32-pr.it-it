---
description: La \_ classe CIM PSExtentBasedOnPExtent associa gli extent dello spazio protetto basati su un extent fisico.
ms.assetid: 4b89319c-022c-4ff4-91ec-70c435a5888a
ms.tgt_platform: multiple
title: Classe CIM_PSExtentBasedOnPExtent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PSExtentBasedOnPExtent
- CIM_PSExtentBasedOnPExtent.EndingAddress
- CIM_PSExtentBasedOnPExtent.StartingAddress
- CIM_PSExtentBasedOnPExtent.Dependent
- CIM_PSExtentBasedOnPExtent.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d028cb99c2f2ca3c0afd8238a3c0c1c3b2e451a3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126672"
---
# <a name="cim_psextentbasedonpextent-class"></a><span data-ttu-id="9fa28-103">CIM \_ PSExtentBasedOnPExtent (classe)</span><span class="sxs-lookup"><span data-stu-id="9fa28-103">CIM\_PSExtentBasedOnPExtent class</span></span>

<span data-ttu-id="9fa28-104">La classe **CIM \_ PSExtentBasedOnPExtent** associa gli extent dello spazio protetto basati su un extent fisico.</span><span class="sxs-lookup"><span data-stu-id="9fa28-104">The **CIM\_PSExtentBasedOnPExtent** class associates protected space extents that are based on a physical extent.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9fa28-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="9fa28-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="9fa28-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="9fa28-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="9fa28-107">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="9fa28-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="9fa28-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="9fa28-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fa28-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9fa28-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{451FE14C-E3D3-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_PSExtentBasedOnPExtent : CIM_BasedOn
{
  uint64                       EndingAddress;
  uint64                       StartingAddress;
  CIM_ProtectedSpaceExtent REF Dependent;
  CIM_PhysicalExtent       REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="9fa28-110">Members</span><span class="sxs-lookup"><span data-stu-id="9fa28-110">Members</span></span>

<span data-ttu-id="9fa28-111">La classe **CIM \_ PSExtentBasedOnPExtent** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="9fa28-111">The **CIM\_PSExtentBasedOnPExtent** class has these types of members:</span></span>

-   [<span data-ttu-id="9fa28-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9fa28-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9fa28-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9fa28-113">Properties</span></span>

<span data-ttu-id="9fa28-114">La classe **CIM \_ PSExtentBasedOnPExtent** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="9fa28-114">The **CIM\_PSExtentBasedOnPExtent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9fa28-115">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="9fa28-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fa28-116">Tipo di dati: **CIM \_ PhysicalExtent**</span><span class="sxs-lookup"><span data-stu-id="9fa28-116">Data type: **CIM\_PhysicalExtent**</span></span>
</dt> <dt>

<span data-ttu-id="9fa28-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9fa28-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9fa28-118">Qualificatori: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="9fa28-118">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="9fa28-119">[**\_ PhysicalExtent CIM**](cim-physicalextent.md) che descrive l'extent fisico.</span><span class="sxs-lookup"><span data-stu-id="9fa28-119">A [**CIM\_PhysicalExtent**](cim-physicalextent.md) that describes the physical extent.</span></span>

</dd> <dt>

<span data-ttu-id="9fa28-120">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="9fa28-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fa28-121">Tipo di dati: **CIM \_ ProtectedSpaceExtent**</span><span class="sxs-lookup"><span data-stu-id="9fa28-121">Data type: **CIM\_ProtectedSpaceExtent**</span></span>
</dt> <dt>

<span data-ttu-id="9fa28-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9fa28-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9fa28-123">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="9fa28-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="9fa28-124">Un [**\_ ProtectedSpaceExtent CIM**](cim-protectedspaceextent.md) che descrive l'extent dello spazio protetto compilato in misura fisica.</span><span class="sxs-lookup"><span data-stu-id="9fa28-124">A [**CIM\_ProtectedSpaceExtent**](cim-protectedspaceextent.md) that describes the protected space extent which is built on the physical extent.</span></span>

</dd> <dt>

<span data-ttu-id="9fa28-125">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="9fa28-125">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fa28-126">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9fa28-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9fa28-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9fa28-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9fa28-128">Indica la fine dell'extent di alto livello nell'archiviazione di livello inferiore.</span><span class="sxs-lookup"><span data-stu-id="9fa28-128">Indicates the end of the high-level extent in lower-level storage.</span></span> <span data-ttu-id="9fa28-129">Questa proprietà è utile quando si esegue il mapping di extent non contigui in un raggruppamento di livello superiore.</span><span class="sxs-lookup"><span data-stu-id="9fa28-129">This property is useful when mapping non-contiguous extents into a higher-level grouping.</span></span>

<span data-ttu-id="9fa28-130">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="9fa28-130">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="9fa28-131">Questa proprietà viene ereditata da [**CIM \_ BasedOn**](cim-basedon.md).</span><span class="sxs-lookup"><span data-stu-id="9fa28-131">This property is inherited from [**CIM\_BasedOn**](cim-basedon.md).</span></span>

</dd> <dt>

<span data-ttu-id="9fa28-132">**IndirizzoIniziale**</span><span class="sxs-lookup"><span data-stu-id="9fa28-132">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fa28-133">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="9fa28-133">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="9fa28-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9fa28-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9fa28-135">Indica l'inizio dell'extent di alto livello nell'archiviazione di livello inferiore.</span><span class="sxs-lookup"><span data-stu-id="9fa28-135">Indicates the beginning of the high-level extent in lower-level storage.</span></span>

<span data-ttu-id="9fa28-136">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="9fa28-136">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="9fa28-137">Questa proprietà viene ereditata da [**CIM \_ BasedOn**](cim-basedon.md).</span><span class="sxs-lookup"><span data-stu-id="9fa28-137">This property is inherited from [**CIM\_BasedOn**](cim-basedon.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9fa28-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="9fa28-138">Remarks</span></span>

<span data-ttu-id="9fa28-139">La classe **CIM \_ PSExtentBasedOnPExtent** è derivata da [**CIM \_ BasedOn**](cim-basedon.md).</span><span class="sxs-lookup"><span data-stu-id="9fa28-139">The **CIM\_PSExtentBasedOnPExtent** class is derived from [**CIM\_BasedOn**](cim-basedon.md).</span></span>

<span data-ttu-id="9fa28-140">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="9fa28-140">WMI does not implement this class.</span></span>

<span data-ttu-id="9fa28-141">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="9fa28-141">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="9fa28-142">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="9fa28-142">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9fa28-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9fa28-143">Requirements</span></span>



| <span data-ttu-id="9fa28-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="9fa28-144">Requirement</span></span> | <span data-ttu-id="9fa28-145">Valore</span><span class="sxs-lookup"><span data-stu-id="9fa28-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9fa28-146">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9fa28-146">Minimum supported client</span></span><br/> | <span data-ttu-id="9fa28-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9fa28-147">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9fa28-148">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9fa28-148">Minimum supported server</span></span><br/> | <span data-ttu-id="9fa28-149">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9fa28-149">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9fa28-150">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9fa28-150">Namespace</span></span><br/>                | <span data-ttu-id="9fa28-151">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="9fa28-151">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9fa28-152">MOF</span><span class="sxs-lookup"><span data-stu-id="9fa28-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9fa28-153"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9fa28-153"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9fa28-154">DLL</span><span class="sxs-lookup"><span data-stu-id="9fa28-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9fa28-155"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9fa28-155"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9fa28-156">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9fa28-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fa28-157">**\_BASEDON CIM**</span><span class="sxs-lookup"><span data-stu-id="9fa28-157">**CIM\_BasedOn**</span></span>](cim-basedon.md)
</dt> </dl>

 

