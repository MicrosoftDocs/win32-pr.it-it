---
description: La \_ classe CIM ResidesOnExtent rappresenta un'associazione tra un file System e l'extent di archiviazione in cui si trova. In genere, un file system risiede su un disco logico.
ms.assetid: 911a81e9-3032-41ff-a337-044c06d02307
ms.tgt_platform: multiple
title: Classe CIM_ResidesOnExtent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResidesOnExtent
- CIM_ResidesOnExtent.Dependent
- CIM_ResidesOnExtent.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 526023fbcc1c961ecaca068be8b0d4ce3e2f84f8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127651"
---
# <a name="cim_residesonextent-class"></a><span data-ttu-id="841da-104">CIM \_ ResidesOnExtent (classe)</span><span class="sxs-lookup"><span data-stu-id="841da-104">CIM\_ResidesOnExtent class</span></span>

<span data-ttu-id="841da-105">La classe **CIM \_ ResidesOnExtent** rappresenta un'associazione tra un file System e l'extent di archiviazione in cui si trova.</span><span class="sxs-lookup"><span data-stu-id="841da-105">The **CIM\_ResidesOnExtent** class represents an association between a file system and the storage extent where it is located.</span></span> <span data-ttu-id="841da-106">In genere, un file system risiede su un disco logico.</span><span class="sxs-lookup"><span data-stu-id="841da-106">Typically, a file system resides on a logical disk.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="841da-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="841da-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="841da-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="841da-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="841da-109">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="841da-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="841da-110">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="841da-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="841da-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="841da-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{10458E26-DB37-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_ResidesOnExtent : CIM_Dependency
{
  CIM_FileSystem    REF Dependent;
  CIM_StorageExtent REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="841da-112">Members</span><span class="sxs-lookup"><span data-stu-id="841da-112">Members</span></span>

<span data-ttu-id="841da-113">La classe **CIM \_ ResidesOnExtent** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="841da-113">The **CIM\_ResidesOnExtent** class has these types of members:</span></span>

-   [<span data-ttu-id="841da-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="841da-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="841da-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="841da-115">Properties</span></span>

<span data-ttu-id="841da-116">La classe **CIM \_ ResidesOnExtent** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="841da-116">The **CIM\_ResidesOnExtent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="841da-117">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="841da-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="841da-118">Tipo di dati: **CIM \_ StorageExtent**</span><span class="sxs-lookup"><span data-stu-id="841da-118">Data type: **CIM\_StorageExtent**</span></span>
</dt> <dt>

<span data-ttu-id="841da-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="841da-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="841da-120">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="841da-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="841da-121">[**\_ StorageExtent CIM**](cim-storageextent.md) che descrive l'extent di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="841da-121">A [**CIM\_StorageExtent**](cim-storageextent.md) that describes the storage extent.</span></span>

</dd> <dt>

<span data-ttu-id="841da-122">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="841da-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="841da-123">Tipo di dati **: \_ file System CIM**</span><span class="sxs-lookup"><span data-stu-id="841da-123">Data type: **CIM\_FileSystem**</span></span>
</dt> <dt>

<span data-ttu-id="841da-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="841da-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="841da-125">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="841da-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="841da-126">Un [**\_ file System CIM**](cim-filesystem.md) che descrive la file System che si trova nell'ambito di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="841da-126">A [**CIM\_FileSystem**](cim-filesystem.md) that describes the file system that is located on the storage extent.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="841da-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="841da-127">Remarks</span></span>

<span data-ttu-id="841da-128">La classe **CIM \_ ResidesOnExtent** è derivata dalla [**\_ dipendenza CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="841da-128">The **CIM\_ResidesOnExtent** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="841da-129">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="841da-129">WMI does not implement this class.</span></span>

<span data-ttu-id="841da-130">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="841da-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="841da-131">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="841da-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="841da-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="841da-132">Requirements</span></span>



| <span data-ttu-id="841da-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="841da-133">Requirement</span></span> | <span data-ttu-id="841da-134">Valore</span><span class="sxs-lookup"><span data-stu-id="841da-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="841da-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="841da-135">Minimum supported client</span></span><br/> | <span data-ttu-id="841da-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="841da-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="841da-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="841da-137">Minimum supported server</span></span><br/> | <span data-ttu-id="841da-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="841da-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="841da-139">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="841da-139">Namespace</span></span><br/>                | <span data-ttu-id="841da-140">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="841da-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="841da-141">MOF</span><span class="sxs-lookup"><span data-stu-id="841da-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="841da-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="841da-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="841da-143">DLL</span><span class="sxs-lookup"><span data-stu-id="841da-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="841da-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="841da-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="841da-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="841da-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="841da-146">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="841da-146">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

