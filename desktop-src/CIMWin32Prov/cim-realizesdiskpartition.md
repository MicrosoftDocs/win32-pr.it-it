---
description: La \_ classe CIM RealizesDiskPartition rappresenta una partizione disco su un supporto fisico che modella la creazione di partizioni in un'unità IDE o SCSI non elaborata.
ms.assetid: cc317f7d-06cd-4126-8123-6a3eb32f792e
ms.tgt_platform: multiple
title: Classe CIM_RealizesDiskPartition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RealizesDiskPartition
- CIM_RealizesDiskPartition.Dependent
- CIM_RealizesDiskPartition.Antecedent
- CIM_RealizesDiskPartition.StartingAddress
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d138aafd179f5fefa40896fe4b9e6a0426b34422
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126669"
---
# <a name="cim_realizesdiskpartition-class"></a><span data-ttu-id="afed0-103">CIM \_ RealizesDiskPartition (classe)</span><span class="sxs-lookup"><span data-stu-id="afed0-103">CIM\_RealizesDiskPartition class</span></span>

<span data-ttu-id="afed0-104">La classe **CIM \_ RealizesDiskPartition** rappresenta una partizione disco su un supporto fisico che modella la creazione di partizioni in un'unità IDE o SCSI non elaborata.</span><span class="sxs-lookup"><span data-stu-id="afed0-104">The **CIM\_RealizesDiskPartition** class represents a disk partition on a physical media that models the creation of partitions on a raw SCSI or IDE drive.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="afed0-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="afed0-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="afed0-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="afed0-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="afed0-107">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="afed0-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="afed0-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="afed0-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="afed0-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="afed0-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B80-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_RealizesDiskPartition : CIM_Realizes
{
  CIM_DiskPartition REF Dependent;
  CIM_PhysicalMedia REF Antecedent;
  uint64                StartingAddress;
};
```

## <a name="members"></a><span data-ttu-id="afed0-110">Members</span><span class="sxs-lookup"><span data-stu-id="afed0-110">Members</span></span>

<span data-ttu-id="afed0-111">La classe **CIM \_ RealizesDiskPartition** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="afed0-111">The **CIM\_RealizesDiskPartition** class has these types of members:</span></span>

-   [<span data-ttu-id="afed0-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="afed0-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="afed0-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="afed0-113">Properties</span></span>

<span data-ttu-id="afed0-114">La classe **CIM \_ RealizesDiskPartition** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="afed0-114">The **CIM\_RealizesDiskPartition** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="afed0-115">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="afed0-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afed0-116">Tipo di dati: **CIM \_ PhysicalMedia**</span><span class="sxs-lookup"><span data-stu-id="afed0-116">Data type: **CIM\_PhysicalMedia**</span></span>
</dt> <dt>

<span data-ttu-id="afed0-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="afed0-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="afed0-118">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="afed0-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="afed0-119">Un [**\_ PhysicalMedia CIM**](cim-physicalmedia.md) che descrive il supporto fisico in cui si realizza l'extent.</span><span class="sxs-lookup"><span data-stu-id="afed0-119">A [**CIM\_PhysicalMedia**](cim-physicalmedia.md) that describes the physical media on which the extent is realized.</span></span>

</dd> <dt>

<span data-ttu-id="afed0-120">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="afed0-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afed0-121">Tipo di dati: **CIM \_ DiskPartition**</span><span class="sxs-lookup"><span data-stu-id="afed0-121">Data type: **CIM\_DiskPartition**</span></span>
</dt> <dt>

<span data-ttu-id="afed0-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="afed0-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="afed0-123">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="afed0-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="afed0-124">Un [**\_ DiskPartition CIM**](cim-diskpartition.md) che descrive la partizione del disco disponibile sul supporto.</span><span class="sxs-lookup"><span data-stu-id="afed0-124">A [**CIM\_DiskPartition**](cim-diskpartition.md) that describes the disk partition that is located on the media.</span></span>

</dd> <dt>

<span data-ttu-id="afed0-125">**IndirizzoIniziale**</span><span class="sxs-lookup"><span data-stu-id="afed0-125">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="afed0-126">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="afed0-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="afed0-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="afed0-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="afed0-128">Indirizzo iniziale sul supporto fisico in cui inizia la partizione del disco.</span><span class="sxs-lookup"><span data-stu-id="afed0-128">Starting address on the physical media where the disk partition begins.</span></span> <span data-ttu-id="afed0-129">L'indirizzo finale della partizione viene determinato tramite le proprietà **Proprietà NumberOfBlocks** e **blockSize** dell'oggetto [**CIM \_ DiskPartition**](cim-diskpartition.md) .</span><span class="sxs-lookup"><span data-stu-id="afed0-129">The partition's ending address is determined using the **NumberOfBlocks** and **BlockSize** properties of the [**CIM\_DiskPartition**](cim-diskpartition.md) object.</span></span>

<span data-ttu-id="afed0-130">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="afed0-130">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="afed0-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="afed0-131">Remarks</span></span>

<span data-ttu-id="afed0-132">La classe **CIM \_ RealizesDiskPartition** è derivata da [**CIM \_ realizzi**](cim-realizes.md).</span><span class="sxs-lookup"><span data-stu-id="afed0-132">The **CIM\_RealizesDiskPartition** class is derived from [**CIM\_Realizes**](cim-realizes.md).</span></span>

<span data-ttu-id="afed0-133">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="afed0-133">WMI does not implement this class.</span></span>

<span data-ttu-id="afed0-134">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="afed0-134">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="afed0-135">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="afed0-135">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="afed0-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="afed0-136">Requirements</span></span>



| <span data-ttu-id="afed0-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="afed0-137">Requirement</span></span> | <span data-ttu-id="afed0-138">Valore</span><span class="sxs-lookup"><span data-stu-id="afed0-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="afed0-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="afed0-139">Minimum supported client</span></span><br/> | <span data-ttu-id="afed0-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="afed0-140">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="afed0-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="afed0-141">Minimum supported server</span></span><br/> | <span data-ttu-id="afed0-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="afed0-142">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="afed0-143">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="afed0-143">Namespace</span></span><br/>                | <span data-ttu-id="afed0-144">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="afed0-144">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="afed0-145">MOF</span><span class="sxs-lookup"><span data-stu-id="afed0-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="afed0-146"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="afed0-146"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="afed0-147">DLL</span><span class="sxs-lookup"><span data-stu-id="afed0-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="afed0-148"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="afed0-148"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="afed0-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="afed0-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afed0-150">**CIM \_ realizza**</span><span class="sxs-lookup"><span data-stu-id="afed0-150">**CIM\_Realizes**</span></span>](cim-realizes.md)
</dt> </dl>

 

