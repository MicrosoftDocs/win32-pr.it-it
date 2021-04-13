---
description: La \_ classe CIM PExtentRedundancyComponent rappresenta gli extent fisici che fanno parte di un gruppo di ridondanza di archiviazione.
ms.assetid: 5a4bb1e8-7b99-410a-bba5-2c63beabd00e
ms.tgt_platform: multiple
title: Classe CIM_PExtentRedundancyComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PExtentRedundancyComponent
- CIM_PExtentRedundancyComponent.PartComponent
- CIM_PExtentRedundancyComponent.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fb2b6a88a789e93ca45f8469e0e67449e3473ddc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104482933"
---
# <a name="cim_pextentredundancycomponent-class"></a><span data-ttu-id="6970e-103">CIM \_ PExtentRedundancyComponent (classe)</span><span class="sxs-lookup"><span data-stu-id="6970e-103">CIM\_PExtentRedundancyComponent class</span></span>

<span data-ttu-id="6970e-104">La classe **CIM \_ PExtentRedundancyComponent** rappresenta gli extent fisici che fanno parte di un gruppo di ridondanza di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="6970e-104">The **CIM\_PExtentRedundancyComponent** class represents the physical extents that participate in a storage redundancy group.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6970e-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="6970e-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="6970e-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="6970e-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="6970e-107">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="6970e-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="6970e-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="6970e-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6970e-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6970e-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{AD3C1FA2-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_PExtentRedundancyComponent : CIM_RedundancyComponent
{
  CIM_PhysicalExtent         REF PartComponent;
  CIM_StorageRedundancyGroup REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="6970e-110">Members</span><span class="sxs-lookup"><span data-stu-id="6970e-110">Members</span></span>

<span data-ttu-id="6970e-111">La classe **CIM \_ PExtentRedundancyComponent** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="6970e-111">The **CIM\_PExtentRedundancyComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="6970e-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6970e-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6970e-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6970e-113">Properties</span></span>

<span data-ttu-id="6970e-114">La classe **CIM \_ PExtentRedundancyComponent** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="6970e-114">The **CIM\_PExtentRedundancyComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6970e-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="6970e-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6970e-116">Tipo di dati: **CIM \_ StorageRedundancyGroup**</span><span class="sxs-lookup"><span data-stu-id="6970e-116">Data type: **CIM\_StorageRedundancyGroup**</span></span>
</dt> <dt>

<span data-ttu-id="6970e-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6970e-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6970e-118">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="6970e-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="6970e-119">Un [**\_ StorageRedundancyGroup CIM**](cim-storageredundancygroup.md) che descrive il gruppo di ridondanza di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="6970e-119">A [**CIM\_StorageRedundancyGroup**](cim-storageredundancygroup.md) that describes the storage redundancy group.</span></span>

</dd> <dt>

<span data-ttu-id="6970e-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="6970e-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6970e-121">Tipo di dati: **CIM \_ PhysicalExtent**</span><span class="sxs-lookup"><span data-stu-id="6970e-121">Data type: **CIM\_PhysicalExtent**</span></span>
</dt> <dt>

<span data-ttu-id="6970e-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6970e-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6970e-123">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="6970e-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="6970e-124">Un [**\_ PhysicalExtent CIM**](cim-physicalextent.md) che descrive l'extent fisico che partecipa al gruppo di ridondanza.</span><span class="sxs-lookup"><span data-stu-id="6970e-124">A [**CIM\_PhysicalExtent**](cim-physicalextent.md) that describes the physical extent participating in the redundancy group.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6970e-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="6970e-125">Remarks</span></span>

<span data-ttu-id="6970e-126">La classe **CIM \_ PExtentRedundancyComponent** è derivata da [**CIM \_ RedundancyComponent**](cim-redundancycomponent.md).</span><span class="sxs-lookup"><span data-stu-id="6970e-126">The **CIM\_PExtentRedundancyComponent** class is derived from [**CIM\_RedundancyComponent**](cim-redundancycomponent.md).</span></span>

<span data-ttu-id="6970e-127">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="6970e-127">WMI does not implement this class.</span></span>

<span data-ttu-id="6970e-128">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="6970e-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="6970e-129">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="6970e-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="6970e-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6970e-130">Requirements</span></span>



| <span data-ttu-id="6970e-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="6970e-131">Requirement</span></span> | <span data-ttu-id="6970e-132">Valore</span><span class="sxs-lookup"><span data-stu-id="6970e-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6970e-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6970e-133">Minimum supported client</span></span><br/> | <span data-ttu-id="6970e-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6970e-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6970e-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6970e-135">Minimum supported server</span></span><br/> | <span data-ttu-id="6970e-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6970e-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6970e-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6970e-137">Namespace</span></span><br/>                | <span data-ttu-id="6970e-138">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="6970e-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6970e-139">MOF</span><span class="sxs-lookup"><span data-stu-id="6970e-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6970e-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6970e-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6970e-141">DLL</span><span class="sxs-lookup"><span data-stu-id="6970e-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6970e-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6970e-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6970e-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6970e-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6970e-144">**\_REDUNDANCYCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="6970e-144">**CIM\_RedundancyComponent**</span></span>](cim-redundancycomponent.md)
</dt> </dl>

 

