---
description: L' \_ associazione CIM LogicalDiskBasedOnVolumeSet mette in relazione i dischi logici con il volume in cui sono stati trovati. I dischi logici possono essere basati su un singolo volume, ad esempio esposto da un responsabile del volume software, o una partizione disco.
ms.assetid: 15a588c9-a6b0-4393-927f-8e8818315542
ms.tgt_platform: multiple
title: Classe CIM_LogicalDiskBasedOnVolumeSet
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDiskBasedOnVolumeSet
- CIM_LogicalDiskBasedOnVolumeSet.EndingAddress
- CIM_LogicalDiskBasedOnVolumeSet.StartingAddress
- CIM_LogicalDiskBasedOnVolumeSet.Dependent
- CIM_LogicalDiskBasedOnVolumeSet.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f2af4c141fe0b64979c6fb6e5b7b0e6068d018d9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126153"
---
# <a name="cim_logicaldiskbasedonvolumeset-class"></a><span data-ttu-id="7f27a-104">CIM \_ LogicalDiskBasedOnVolumeSet (classe)</span><span class="sxs-lookup"><span data-stu-id="7f27a-104">CIM\_LogicalDiskBasedOnVolumeSet class</span></span>

<span data-ttu-id="7f27a-105">L'associazione **CIM \_ LogicalDiskBasedOnVolumeSet** mette in relazione i dischi logici con il volume in cui sono stati trovati.</span><span class="sxs-lookup"><span data-stu-id="7f27a-105">The **CIM\_LogicalDiskBasedOnVolumeSet** association relates logical disks with the volume on which they are found.</span></span> <span data-ttu-id="7f27a-106">I dischi logici possono essere basati su un singolo volume, ad esempio esposto da un responsabile del volume software, o una partizione disco.</span><span class="sxs-lookup"><span data-stu-id="7f27a-106">Logical disks can be based on a single volume (for example, exposed by a software volume manager) or a disk partition.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7f27a-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="7f27a-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="7f27a-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="7f27a-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="7f27a-109">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="7f27a-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="7f27a-110">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="7f27a-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f27a-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7f27a-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{3A608798-E3D3-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_LogicalDiskBasedOnVolumeSet : CIM_BasedOn
{
  uint64              EndingAddress;
  uint64              StartingAddress;
  CIM_LogicalDisk REF Dependent;
  CIM_VolumeSet   REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="7f27a-112">Members</span><span class="sxs-lookup"><span data-stu-id="7f27a-112">Members</span></span>

<span data-ttu-id="7f27a-113">La classe **CIM \_ LogicalDiskBasedOnVolumeSet** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="7f27a-113">The **CIM\_LogicalDiskBasedOnVolumeSet** class has these types of members:</span></span>

-   [<span data-ttu-id="7f27a-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7f27a-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7f27a-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7f27a-115">Properties</span></span>

<span data-ttu-id="7f27a-116">La classe **CIM \_ LogicalDiskBasedOnVolumeSet** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="7f27a-116">The **CIM\_LogicalDiskBasedOnVolumeSet** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7f27a-117">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="7f27a-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f27a-118">Tipo di dati **: \_ volume CIM**</span><span class="sxs-lookup"><span data-stu-id="7f27a-118">Data type: **CIM\_VolumeSet**</span></span>
</dt> <dt>

<span data-ttu-id="7f27a-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7f27a-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f27a-120">Qualificatori: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="7f27a-120">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="7f27a-121">Un set di [**\_ volumi CIM**](cim-volumeset.md) che descrive il set di volumi.</span><span class="sxs-lookup"><span data-stu-id="7f27a-121">A [**CIM\_VolumeSet**](cim-volumeset.md) that describes the volume set.</span></span>

</dd> <dt>

<span data-ttu-id="7f27a-122">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="7f27a-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f27a-123">Tipo di dati: **CIM \_ disco logico**</span><span class="sxs-lookup"><span data-stu-id="7f27a-123">Data type: **CIM\_LogicalDisk**</span></span>
</dt> <dt>

<span data-ttu-id="7f27a-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7f27a-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f27a-125">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="7f27a-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="7f27a-126">Un [**\_ disco logico CIM**](cim-logicaldisk.md) che descrive il disco logico basato sul set di volumi.</span><span class="sxs-lookup"><span data-stu-id="7f27a-126">A [**CIM\_LogicalDisk**](cim-logicaldisk.md) that describes the logical disk which is built on the volume set.</span></span>

</dd> <dt>

<span data-ttu-id="7f27a-127">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="7f27a-127">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f27a-128">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7f27a-128">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7f27a-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7f27a-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f27a-130">Indica la fine dell'extent di alto livello nell'archiviazione di livello inferiore.</span><span class="sxs-lookup"><span data-stu-id="7f27a-130">Indicates the end of the high-level extent in lower-level storage.</span></span> <span data-ttu-id="7f27a-131">Questa proprietà è utile quando si esegue il mapping di extent non contigui in un raggruppamento di livello superiore.</span><span class="sxs-lookup"><span data-stu-id="7f27a-131">This property is useful when mapping non-contiguous extents into a higher-level grouping.</span></span>

<span data-ttu-id="7f27a-132">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="7f27a-132">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="7f27a-133">Questa proprietà viene ereditata da [**CIM \_ BasedOn**](cim-basedon.md).</span><span class="sxs-lookup"><span data-stu-id="7f27a-133">This property is inherited from [**CIM\_BasedOn**](cim-basedon.md).</span></span>

</dd> <dt>

<span data-ttu-id="7f27a-134">**IndirizzoIniziale**</span><span class="sxs-lookup"><span data-stu-id="7f27a-134">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f27a-135">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7f27a-135">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7f27a-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7f27a-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f27a-137">Indica l'inizio dell'extent di alto livello nell'archiviazione di livello inferiore.</span><span class="sxs-lookup"><span data-stu-id="7f27a-137">Indicates the beginning of the high-level extent in lower-level storage.</span></span>

<span data-ttu-id="7f27a-138">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="7f27a-138">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="7f27a-139">Questa proprietà viene ereditata da [**CIM \_ BasedOn**](cim-basedon.md).</span><span class="sxs-lookup"><span data-stu-id="7f27a-139">This property is inherited from [**CIM\_BasedOn**](cim-basedon.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7f27a-140">Commenti</span><span class="sxs-lookup"><span data-stu-id="7f27a-140">Remarks</span></span>

<span data-ttu-id="7f27a-141">La classe **CIM \_ LogicalDiskBasedOnVolumeSet** è derivata da [**CIM \_ BasedOn**](cim-basedon.md).</span><span class="sxs-lookup"><span data-stu-id="7f27a-141">The **CIM\_LogicalDiskBasedOnVolumeSet** class is derived from [**CIM\_BasedOn**](cim-basedon.md).</span></span>

<span data-ttu-id="7f27a-142">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="7f27a-142">WMI does not implement this class.</span></span>

<span data-ttu-id="7f27a-143">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="7f27a-143">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="7f27a-144">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="7f27a-144">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f27a-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7f27a-145">Requirements</span></span>



| <span data-ttu-id="7f27a-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f27a-146">Requirement</span></span> | <span data-ttu-id="7f27a-147">Valore</span><span class="sxs-lookup"><span data-stu-id="7f27a-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7f27a-148">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7f27a-148">Minimum supported client</span></span><br/> | <span data-ttu-id="7f27a-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7f27a-149">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7f27a-150">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7f27a-150">Minimum supported server</span></span><br/> | <span data-ttu-id="7f27a-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7f27a-151">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7f27a-152">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7f27a-152">Namespace</span></span><br/>                | <span data-ttu-id="7f27a-153">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="7f27a-153">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7f27a-154">MOF</span><span class="sxs-lookup"><span data-stu-id="7f27a-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7f27a-155"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7f27a-155"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7f27a-156">DLL</span><span class="sxs-lookup"><span data-stu-id="7f27a-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7f27a-157"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f27a-157"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f27a-158">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7f27a-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f27a-159">**\_BASEDON CIM**</span><span class="sxs-lookup"><span data-stu-id="7f27a-159">**CIM\_BasedOn**</span></span>](cim-basedon.md)
</dt> </dl>

 

