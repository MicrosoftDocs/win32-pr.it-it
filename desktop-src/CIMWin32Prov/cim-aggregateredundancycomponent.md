---
description: La \_ classe CIM AggregateRedundancyComponent descrive l'extent fisico aggregato in un gruppo di ridondanza di archiviazione.
ms.assetid: 3407e888-e17c-4f65-a33f-056002accbf7
ms.tgt_platform: multiple
title: Classe CIM_AggregateRedundancyComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AggregateRedundancyComponent
- CIM_AggregateRedundancyComponent.PartComponent
- CIM_AggregateRedundancyComponent.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9a5e638730578bad8d64f35b29a5152898c23fd6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748714"
---
# <a name="cim_aggregateredundancycomponent-class"></a><span data-ttu-id="14dda-103">CIM \_ AggregateRedundancyComponent (classe)</span><span class="sxs-lookup"><span data-stu-id="14dda-103">CIM\_AggregateRedundancyComponent class</span></span>

<span data-ttu-id="14dda-104">La classe **CIM \_ AggregateRedundancyComponent** descrive l'extent fisico aggregato in un gruppo di ridondanza di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="14dda-104">The **CIM\_AggregateRedundancyComponent** class describes the aggregate physical extent in a storage redundancy group.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="14dda-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="14dda-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="14dda-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="14dda-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="14dda-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="14dda-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="14dda-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="14dda-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="14dda-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="14dda-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{154E66D8-DB35-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_AggregateRedundancyComponent : CIM_RedundancyComponent
{
  CIM_AggregatePExtent       REF PartComponent;
  CIM_StorageRedundancyGroup REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="14dda-110">Members</span><span class="sxs-lookup"><span data-stu-id="14dda-110">Members</span></span>

<span data-ttu-id="14dda-111">La classe **CIM \_ AggregateRedundancyComponent** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="14dda-111">The **CIM\_AggregateRedundancyComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="14dda-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="14dda-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="14dda-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="14dda-113">Properties</span></span>

<span data-ttu-id="14dda-114">La classe **CIM \_ AggregateRedundancyComponent** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="14dda-114">The **CIM\_AggregateRedundancyComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="14dda-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="14dda-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14dda-116">Tipo di dati: **CIM \_ StorageRedundancyGroup**</span><span class="sxs-lookup"><span data-stu-id="14dda-116">Data type: **CIM\_StorageRedundancyGroup**</span></span>
</dt> <dt>

<span data-ttu-id="14dda-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="14dda-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14dda-118">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="14dda-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="14dda-119">Un [**\_ StorageRedundancyGroup CIM**](cim-storageredundancygroup.md) che contiene il gruppo di ridondanza di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="14dda-119">A [**CIM\_StorageRedundancyGroup**](cim-storageredundancygroup.md) that contains the storage redundancy group.</span></span>

</dd> <dt>

<span data-ttu-id="14dda-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="14dda-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14dda-121">Tipo di dati: **CIM \_ AggregatePExtent**</span><span class="sxs-lookup"><span data-stu-id="14dda-121">Data type: **CIM\_AggregatePExtent**</span></span>
</dt> <dt>

<span data-ttu-id="14dda-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="14dda-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14dda-123">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="14dda-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="14dda-124">Un [**\_ AggregatePExtent CIM**](cim-aggregatepextent.md) che contiene l'extent fisico aggregato che partecipa al gruppo di ridondanza.</span><span class="sxs-lookup"><span data-stu-id="14dda-124">A [**CIM\_AggregatePExtent**](cim-aggregatepextent.md) that contains the aggregate physical extent participating in the redundancy group.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="14dda-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="14dda-125">Remarks</span></span>

<span data-ttu-id="14dda-126">La classe **CIM \_ AggregateRedundancyComponent** è derivata da [**CIM \_ RedundancyComponent**](cim-redundancycomponent.md).</span><span class="sxs-lookup"><span data-stu-id="14dda-126">The **CIM\_AggregateRedundancyComponent** class is derived from [**CIM\_RedundancyComponent**](cim-redundancycomponent.md).</span></span>

<span data-ttu-id="14dda-127">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="14dda-127">WMI does not implement this class.</span></span>

<span data-ttu-id="14dda-128">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="14dda-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="14dda-129">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="14dda-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="14dda-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="14dda-130">Requirements</span></span>



| <span data-ttu-id="14dda-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="14dda-131">Requirement</span></span> | <span data-ttu-id="14dda-132">Valore</span><span class="sxs-lookup"><span data-stu-id="14dda-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="14dda-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="14dda-133">Minimum supported client</span></span><br/> | <span data-ttu-id="14dda-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="14dda-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="14dda-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="14dda-135">Minimum supported server</span></span><br/> | <span data-ttu-id="14dda-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="14dda-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="14dda-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="14dda-137">Namespace</span></span><br/>                | <span data-ttu-id="14dda-138">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="14dda-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="14dda-139">MOF</span><span class="sxs-lookup"><span data-stu-id="14dda-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="14dda-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="14dda-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="14dda-141">DLL</span><span class="sxs-lookup"><span data-stu-id="14dda-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="14dda-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14dda-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14dda-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="14dda-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14dda-144">**\_REDUNDANCYCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="14dda-144">**CIM\_RedundancyComponent**</span></span>](cim-redundancycomponent.md)
</dt> </dl>

 

