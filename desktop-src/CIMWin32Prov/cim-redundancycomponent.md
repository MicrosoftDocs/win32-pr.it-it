---
description: La \_ classe CIM RedundancyComponent associa un gruppo di ridondanza composto da elementi di sistema gestiti e indica che, insieme, gli elementi forniscono la ridondanza.
ms.assetid: 2511ae26-011a-4e0d-ad34-d5fe9c78f0ff
ms.tgt_platform: multiple
title: Classe CIM_RedundancyComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RedundancyComponent
- CIM_RedundancyComponent.GroupComponent
- CIM_RedundancyComponent.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5bcd1c16417ba0c02e13579f9e471076d4c61818
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877290"
---
# <a name="cim_redundancycomponent-class"></a><span data-ttu-id="25810-103">CIM \_ RedundancyComponent (classe)</span><span class="sxs-lookup"><span data-stu-id="25810-103">CIM\_RedundancyComponent class</span></span>

<span data-ttu-id="25810-104">La classe **CIM \_ RedundancyComponent** associa un gruppo di ridondanza composto da elementi di sistema gestiti e indica che, insieme, gli elementi forniscono la ridondanza.</span><span class="sxs-lookup"><span data-stu-id="25810-104">The **CIM\_RedundancyComponent** class associates a redundancy group composed of managed system elements and indicates that, together, the elements provide redundancy.</span></span> <span data-ttu-id="25810-105">Tutti gli elementi aggregati in un gruppo di ridondanza devono essere istanze della stessa classe di oggetti.</span><span class="sxs-lookup"><span data-stu-id="25810-105">All elements aggregated in a redundancy group should be instantiations of the same object class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="25810-106">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="25810-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="25810-107">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="25810-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="25810-108">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="25810-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="25810-109">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="25810-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="25810-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="25810-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{FB9D6E62-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_RedundancyComponent : CIM_Component
{
  CIM_RedundancyGroup      REF GroupComponent;
  CIM_ManagedSystemElement REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="25810-111">Members</span><span class="sxs-lookup"><span data-stu-id="25810-111">Members</span></span>

<span data-ttu-id="25810-112">La classe **CIM \_ RedundancyComponent** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="25810-112">The **CIM\_RedundancyComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="25810-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="25810-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="25810-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="25810-114">Properties</span></span>

<span data-ttu-id="25810-115">La classe **CIM \_ RedundancyComponent** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="25810-115">The **CIM\_RedundancyComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="25810-116">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="25810-116">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25810-117">Tipo di dati: **CIM \_ RedundancyGroup**</span><span class="sxs-lookup"><span data-stu-id="25810-117">Data type: **CIM\_RedundancyGroup**</span></span>
</dt> <dt>

<span data-ttu-id="25810-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="25810-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25810-119">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="25810-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="25810-120">L'associazione **CIM \_ RedundancyComponent** indica che "questo set di ventilatori" o "questi extent fisici" partecipano a un singolo gruppo di ridondanza.</span><span class="sxs-lookup"><span data-stu-id="25810-120">The **CIM\_RedundancyComponent** association indicates that 'this set of fans' or 'these physical extents' participate in a single redundancy group.</span></span>

</dd> <dt>

<span data-ttu-id="25810-121">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="25810-121">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25810-122">Tipo di dati: **CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="25810-122">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="25810-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="25810-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="25810-124">[**\_ ManagedSystemElement CIM**](cim-managedsystemelement.md) che descrive l'elemento figlio nell'associazione.</span><span class="sxs-lookup"><span data-stu-id="25810-124">A [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) that describes the child element in the association.</span></span>

<span data-ttu-id="25810-125">Questa proprietà viene ereditata [**dal \_ componente CIM**](cim-component.md).</span><span class="sxs-lookup"><span data-stu-id="25810-125">This property is inherited from [**CIM\_Component**](cim-component.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="25810-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="25810-126">Remarks</span></span>

<span data-ttu-id="25810-127">**CIM \_ RedundancyComponent** deriva dal [**\_ componente CIM**](cim-component.md).</span><span class="sxs-lookup"><span data-stu-id="25810-127">**CIM\_RedundancyComponent** is derived from [**CIM\_Component**](cim-component.md).</span></span>

<span data-ttu-id="25810-128">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="25810-128">WMI does not implement this class.</span></span>

<span data-ttu-id="25810-129">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="25810-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="25810-130">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="25810-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="25810-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="25810-131">Requirements</span></span>



| <span data-ttu-id="25810-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="25810-132">Requirement</span></span> | <span data-ttu-id="25810-133">Valore</span><span class="sxs-lookup"><span data-stu-id="25810-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="25810-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="25810-134">Minimum supported client</span></span><br/> | <span data-ttu-id="25810-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="25810-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="25810-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="25810-136">Minimum supported server</span></span><br/> | <span data-ttu-id="25810-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="25810-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="25810-138">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="25810-138">Namespace</span></span><br/>                | <span data-ttu-id="25810-139">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="25810-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="25810-140">MOF</span><span class="sxs-lookup"><span data-stu-id="25810-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="25810-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="25810-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="25810-142">DLL</span><span class="sxs-lookup"><span data-stu-id="25810-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="25810-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25810-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25810-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="25810-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25810-145">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="25810-145">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

