---
description: La \_ classe CIM BasedOn rappresenta un'associazione che descrive come possono essere assemblati gli extent di archiviazione da extent di livello inferiore.
ms.assetid: 82132012-5851-4be8-82db-edbdb50b70e5
ms.tgt_platform: multiple
title: Classe CIM_BasedOn (provider WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BasedOn
- CIM_BasedOn.Dependent
- CIM_BasedOn.Antecedent
- CIM_BasedOn.EndingAddress
- CIM_BasedOn.StartingAddress
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5e25cd9a5f194df8c5cbc0c7dc24a4777cee3417
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225724"
---
# <a name="cim_basedon-class-cimwin32-wmi-providers"></a><span data-ttu-id="8c2da-103">Classe CIM_BasedOn (provider WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="8c2da-103">CIM_BasedOn class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="8c2da-104">La classe **CIM \_ BasedOn** rappresenta un'associazione che descrive come possono essere assemblati gli extent di archiviazione da extent di livello inferiore.</span><span class="sxs-lookup"><span data-stu-id="8c2da-104">The **CIM\_BasedOn** class represents an association that describes how storage extents can be assembled from lower-level extents.</span></span> <span data-ttu-id="8c2da-105">Ad esempio, gli extent fisici includono extent dello spazio protetto.</span><span class="sxs-lookup"><span data-stu-id="8c2da-105">For example, physical extents include protected space extents.</span></span> <span data-ttu-id="8c2da-106">I set di volumi vengono quindi assemblati da uno o più extent di spazio fisico o protetto.</span><span class="sxs-lookup"><span data-stu-id="8c2da-106">Thus, volume sets are assembled from one or more physical or protected space extents.</span></span> <span data-ttu-id="8c2da-107">La memoria cache può essere definita in modo indipendente e realizzata in un elemento fisico oppure può essere basata su extent di archiviazione volatili o non volatili.</span><span class="sxs-lookup"><span data-stu-id="8c2da-107">Cache memory can be defined independently and realized in a physical element, or it can be based on volatile or non-volatile storage extents.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8c2da-108">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="8c2da-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="8c2da-109">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="8c2da-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="8c2da-110">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="8c2da-110">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c2da-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8c2da-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C53E-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_BasedOn : CIM_Dependency
{
  CIM_StorageExtent REF Dependent;
  CIM_StorageExtent REF Antecedent;
  uint64                EndingAddress;
  uint64                StartingAddress;
};
```

## <a name="members"></a><span data-ttu-id="8c2da-112">Members</span><span class="sxs-lookup"><span data-stu-id="8c2da-112">Members</span></span>

<span data-ttu-id="8c2da-113">La classe **CIM \_ BasedOn** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="8c2da-113">The **CIM\_BasedOn** class has these types of members:</span></span>

-   [<span data-ttu-id="8c2da-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8c2da-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8c2da-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8c2da-115">Properties</span></span>

<span data-ttu-id="8c2da-116">La classe **CIM \_ BasedOn** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="8c2da-116">The **CIM\_BasedOn** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8c2da-117">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="8c2da-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c2da-118">Tipo di dati: **CIM \_ StorageExtent**</span><span class="sxs-lookup"><span data-stu-id="8c2da-118">Data type: **CIM\_StorageExtent**</span></span>
</dt> <dt>

<span data-ttu-id="8c2da-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8c2da-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c2da-120">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="8c2da-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="8c2da-121">Un [**\_ StorageExtent CIM**](cim-storageextent.md) che descrive l'extent di archiviazione di livello inferiore.</span><span class="sxs-lookup"><span data-stu-id="8c2da-121">A [**CIM\_StorageExtent**](cim-storageextent.md) that describes the lower level storage extent.</span></span>

</dd> <dt>

<span data-ttu-id="8c2da-122">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="8c2da-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c2da-123">Tipo di dati: **CIM \_ StorageExtent**</span><span class="sxs-lookup"><span data-stu-id="8c2da-123">Data type: **CIM\_StorageExtent**</span></span>
</dt> <dt>

<span data-ttu-id="8c2da-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8c2da-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c2da-125">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="8c2da-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="8c2da-126">Un [**\_ StorageExtent CIM**](cim-storageextent.md) che descrive l'extent di archiviazione di livello superiore.</span><span class="sxs-lookup"><span data-stu-id="8c2da-126">A [**CIM\_StorageExtent**](cim-storageextent.md) that describes the higher level storage extent.</span></span>

</dd> <dt>

<span data-ttu-id="8c2da-127">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="8c2da-127">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c2da-128">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8c2da-128">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8c2da-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8c2da-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8c2da-130">Indica la fine dell'extent di alto livello nell'archiviazione di livello inferiore.</span><span class="sxs-lookup"><span data-stu-id="8c2da-130">Indicates the end of the high-level extent in lower-level storage.</span></span> <span data-ttu-id="8c2da-131">Questa proprietà è utile quando si esegue il mapping di extent non contigui in un raggruppamento di livello superiore.</span><span class="sxs-lookup"><span data-stu-id="8c2da-131">This property is useful when mapping non-contiguous extents into a higher-level grouping.</span></span>

<span data-ttu-id="8c2da-132">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="8c2da-132">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="8c2da-133">**IndirizzoIniziale**</span><span class="sxs-lookup"><span data-stu-id="8c2da-133">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c2da-134">Tipo di dati: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8c2da-134">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8c2da-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="8c2da-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8c2da-136">Indica l'inizio dell'extent di alto livello nell'archiviazione di livello inferiore.</span><span class="sxs-lookup"><span data-stu-id="8c2da-136">Indicates the beginning of the high-level extent in lower-level storage.</span></span>

<span data-ttu-id="8c2da-137">Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="8c2da-137">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8c2da-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="8c2da-138">Remarks</span></span>

<span data-ttu-id="8c2da-139">La classe **CIM \_ BasedOn** è derivata dalla [**\_ dipendenza CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="8c2da-139">The **CIM\_BasedOn** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="8c2da-140">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="8c2da-140">WMI does not implement this class.</span></span>

<span data-ttu-id="8c2da-141">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="8c2da-141">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="8c2da-142">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="8c2da-142">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c2da-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8c2da-143">Requirements</span></span>



| <span data-ttu-id="8c2da-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c2da-144">Requirement</span></span> | <span data-ttu-id="8c2da-145">Valore</span><span class="sxs-lookup"><span data-stu-id="8c2da-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8c2da-146">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8c2da-146">Minimum supported client</span></span><br/> | <span data-ttu-id="8c2da-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8c2da-147">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8c2da-148">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8c2da-148">Minimum supported server</span></span><br/> | <span data-ttu-id="8c2da-149">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8c2da-149">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8c2da-150">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="8c2da-150">Namespace</span></span><br/>                | <span data-ttu-id="8c2da-151">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="8c2da-151">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8c2da-152">MOF</span><span class="sxs-lookup"><span data-stu-id="8c2da-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8c2da-153"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8c2da-153"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8c2da-154">DLL</span><span class="sxs-lookup"><span data-stu-id="8c2da-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8c2da-155"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c2da-155"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c2da-156">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8c2da-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c2da-157">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="8c2da-157">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

