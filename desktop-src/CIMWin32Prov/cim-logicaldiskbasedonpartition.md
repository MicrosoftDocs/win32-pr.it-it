---
description: La \_ classe CIM LogicalDiskBasedOnPartition associa un disco logico con la partizione del disco in cui risiede.
ms.assetid: 264b62ed-2af2-42dc-9cd2-41b26cc85ca4
ms.tgt_platform: multiple
title: Classe CIM_LogicalDiskBasedOnPartition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDiskBasedOnPartition
- CIM_LogicalDiskBasedOnPartition.EndingAddress
- CIM_LogicalDiskBasedOnPartition.StartingAddress
- CIM_LogicalDiskBasedOnPartition.Dependent
- CIM_LogicalDiskBasedOnPartition.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 67aac7ae8d295bd6d98e06e0ebb8135d3330f52f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523137"
---
# <a name="cim_logicaldiskbasedonpartition-class"></a><span data-ttu-id="533f1-103">CIM \_ LogicalDiskBasedOnPartition (classe)</span><span class="sxs-lookup"><span data-stu-id="533f1-103">CIM\_LogicalDiskBasedOnPartition class</span></span>

<span data-ttu-id="533f1-104">La classe **CIM \_ LogicalDiskBasedOnPartition** associa un disco logico con la partizione del disco in cui risiede.</span><span class="sxs-lookup"><span data-stu-id="533f1-104">The **CIM\_LogicalDiskBasedOnPartition** class associates a logical disk with the disk partition on which it resides.</span></span>

<span data-ttu-id="533f1-105">Ad esempio, un'unità C del computer può trovarsi in una partizione su un supporto fisico locale, il che determina che un disco logico non può estendersi a più di una partizione.</span><span class="sxs-lookup"><span data-stu-id="533f1-105">For example, a computer's drive C can be located on a partition on local physical media, which dictates that a logical disk cannot span more than one partition.</span></span> <span data-ttu-id="533f1-106">Quando un disco logico può estendersi su più di una partizione, tuttavia, il disco logico è basato sulla configurazione RAID, ad esempio un set di mirroring o di striping.</span><span class="sxs-lookup"><span data-stu-id="533f1-106">When a logical disk can span more than one partition, however, the logical disk is based on RAID configuration (for example, a mirror or stripe set).</span></span> <span data-ttu-id="533f1-107">In tal caso, il disco logico è basato sul volume di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="533f1-107">In which case, the logical disk is based on storage volume.</span></span> <span data-ttu-id="533f1-108">Per impedire l'uso errato dell'associazione **CIM \_ LogicalDiskBasedOnPartition** , il qualificatore **Max (1)** è stato inserito nel riferimento **precedente** alla partizione del disco.</span><span class="sxs-lookup"><span data-stu-id="533f1-108">To prevent using the **CIM\_LogicalDiskBasedOnPartition** association incorrectly, the **Max(1)** qualifier was put on the **Antecedent** reference to the disk partition.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="533f1-109">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="533f1-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="533f1-110">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="533f1-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="533f1-111">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="533f1-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="533f1-112">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="533f1-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="533f1-113">Sintassi</span><span class="sxs-lookup"><span data-stu-id="533f1-113">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C53F-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_LogicalDiskBasedOnPartition : CIM_BasedOn
{
  uint64                EndingAddress;
  uint64                StartingAddress;
  CIM_LogicalDisk   REF Dependent;
  CIM_DiskPartition REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="533f1-114">Members</span><span class="sxs-lookup"><span data-stu-id="533f1-114">Members</span></span>

<span data-ttu-id="533f1-115">La classe **CIM \_ LogicalDiskBasedOnPartition** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="533f1-115">The **CIM\_LogicalDiskBasedOnPartition** class has these types of members:</span></span>

-   [<span data-ttu-id="533f1-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="533f1-116">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="533f1-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="533f1-117">Properties</span></span>

<span data-ttu-id="533f1-118">La classe **CIM \_ LogicalDiskBasedOnPartition** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="533f1-118">The **CIM\_LogicalDiskBasedOnPartition** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="533f1-119">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="533f1-119">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="533f1-120">Tipo di dati: **CIM \_ DiskPartition**</span><span class="sxs-lookup"><span data-stu-id="533f1-120">Data type: **CIM\_DiskPartition**</span></span>
</dt> <dt>

<span data-ttu-id="533f1-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="533f1-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="533f1-122">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="533f1-122">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="533f1-123">[**\_ DiskPartition CIM**](cim-diskpartition.md) che descrive la partizione del disco.</span><span class="sxs-lookup"><span data-stu-id="533f1-123">A [**CIM\_DiskPartition**](cim-diskpartition.md) that describes the disk partition.</span></span>

</dd> <dt>

<span data-ttu-id="533f1-124">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="533f1-124">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="533f1-125">Tipo di dati: **CIM \_ disco logico**</span><span class="sxs-lookup"><span data-stu-id="533f1-125">Data type: **CIM\_LogicalDisk**</span></span>
</dt> <dt>

<span data-ttu-id="533f1-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="533f1-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="533f1-127">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="533f1-127">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="533f1-128">Un [**\_ disco logico CIM**](cim-logicaldisk.md) che descrive il disco logico compilato sulla partizione.</span><span class="sxs-lookup"><span data-stu-id="533f1-128">A [**CIM\_LogicalDisk**](cim-logicaldisk.md) that describes the logical disk which is built on the partition.</span></span>

</dd> <dt>

<span data-ttu-id="533f1-129">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="533f1-129">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="533f1-130">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="533f1-130">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="533f1-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="533f1-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="533f1-132">Indica la fine dell'extent di alto livello nell'archiviazione di livello inferiore.</span><span class="sxs-lookup"><span data-stu-id="533f1-132">Indicates the end of the high-level extent in lower-level storage.</span></span> <span data-ttu-id="533f1-133">Questa proprietà è utile quando si esegue il mapping di extent non contigui in un raggruppamento di livello superiore.</span><span class="sxs-lookup"><span data-stu-id="533f1-133">This property is useful when mapping non-contiguous extents into a higher-level grouping.</span></span>

<span data-ttu-id="533f1-134">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="533f1-134">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="533f1-135">Questa proprietà viene ereditata da [**CIM \_ BasedOn**](cim-basedon.md).</span><span class="sxs-lookup"><span data-stu-id="533f1-135">This property is inherited from [**CIM\_BasedOn**](cim-basedon.md).</span></span>

</dd> <dt>

<span data-ttu-id="533f1-136">**IndirizzoIniziale**</span><span class="sxs-lookup"><span data-stu-id="533f1-136">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="533f1-137">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="533f1-137">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="533f1-138">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="533f1-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="533f1-139">Indica l'inizio dell'extent di alto livello nell'archiviazione di livello inferiore.</span><span class="sxs-lookup"><span data-stu-id="533f1-139">Indicates the beginning of the high-level extent in lower-level storage.</span></span>

<span data-ttu-id="533f1-140">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="533f1-140">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="533f1-141">Questa proprietà viene ereditata da [**CIM \_ BasedOn**](cim-basedon.md).</span><span class="sxs-lookup"><span data-stu-id="533f1-141">This property is inherited from [**CIM\_BasedOn**](cim-basedon.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="533f1-142">Commenti</span><span class="sxs-lookup"><span data-stu-id="533f1-142">Remarks</span></span>

<span data-ttu-id="533f1-143">La classe **CIM \_ LogicalDiskBasedOnPartition** è derivata da [**CIM \_ BasedOn**](cim-basedon.md).</span><span class="sxs-lookup"><span data-stu-id="533f1-143">The **CIM\_LogicalDiskBasedOnPartition** class is derived from [**CIM\_BasedOn**](cim-basedon.md).</span></span>

<span data-ttu-id="533f1-144">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="533f1-144">WMI does not implement this class.</span></span> <span data-ttu-id="533f1-145">Per le classi derivate da **CIM \_ LogicalDiskBasedOnPartition**, vedere [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="533f1-145">For classes derived from **CIM\_LogicalDiskBasedOnPartition**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="533f1-146">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="533f1-146">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="533f1-147">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="533f1-147">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="533f1-148">Requisiti</span><span class="sxs-lookup"><span data-stu-id="533f1-148">Requirements</span></span>



| <span data-ttu-id="533f1-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="533f1-149">Requirement</span></span> | <span data-ttu-id="533f1-150">Valore</span><span class="sxs-lookup"><span data-stu-id="533f1-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="533f1-151">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="533f1-151">Minimum supported client</span></span><br/> | <span data-ttu-id="533f1-152">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="533f1-152">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="533f1-153">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="533f1-153">Minimum supported server</span></span><br/> | <span data-ttu-id="533f1-154">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="533f1-154">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="533f1-155">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="533f1-155">Namespace</span></span><br/>                | <span data-ttu-id="533f1-156">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="533f1-156">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="533f1-157">MOF</span><span class="sxs-lookup"><span data-stu-id="533f1-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="533f1-158"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="533f1-158"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="533f1-159">DLL</span><span class="sxs-lookup"><span data-stu-id="533f1-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="533f1-160"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="533f1-160"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="533f1-161">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="533f1-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="533f1-162">**\_BASEDON CIM**</span><span class="sxs-lookup"><span data-stu-id="533f1-162">**CIM\_BasedOn**</span></span>](cim-basedon.md)
</dt> </dl>

 

