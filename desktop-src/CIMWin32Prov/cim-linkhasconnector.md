---
description: La \_ classe CIM LinkHasConnector associa i cavi e i collegamenti usati come connettori fisici, che connettono gli elementi fisici. Questa associazione definisce in modo esplicito la relazione dei connettori per CIM \_ PhysicalLink.
ms.assetid: c8244b93-749a-424a-ab40-ce5ce79c8b02
ms.tgt_platform: multiple
title: Classe CIM_LinkHasConnector
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LinkHasConnector
- CIM_LinkHasConnector.PartComponent
- CIM_LinkHasConnector.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: daeb9d07fefc4c52c7b630dcc69099c1cae429a2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877882"
---
# <a name="cim_linkhasconnector-class"></a><span data-ttu-id="4e739-104">CIM \_ LinkHasConnector (classe)</span><span class="sxs-lookup"><span data-stu-id="4e739-104">CIM\_LinkHasConnector class</span></span>

<span data-ttu-id="4e739-105">La classe **CIM \_ LinkHasConnector** associa i cavi e i collegamenti usati come connettori fisici, che connettono gli elementi fisici.</span><span class="sxs-lookup"><span data-stu-id="4e739-105">The **CIM\_LinkHasConnector** class associates cables and links used as physical connectors, which connect the physical elements.</span></span> <span data-ttu-id="4e739-106">Questa associazione definisce in modo esplicito la relazione dei connettori per [**CIM \_ PhysicalLink**](cim-physicallink.md).</span><span class="sxs-lookup"><span data-stu-id="4e739-106">This association explicitly defines the relationship of connectors for [**CIM\_PhysicalLink**](cim-physicallink.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4e739-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="4e739-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="4e739-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="4e739-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="4e739-109">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="4e739-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="4e739-110">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="4e739-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e739-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4e739-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B8B-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_LinkHasConnector : CIM_Component
{
  CIM_PhysicalConnector REF PartComponent;
  CIM_PhysicalLink      REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="4e739-112">Members</span><span class="sxs-lookup"><span data-stu-id="4e739-112">Members</span></span>

<span data-ttu-id="4e739-113">La classe **CIM \_ LinkHasConnector** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="4e739-113">The **CIM\_LinkHasConnector** class has these types of members:</span></span>

-   [<span data-ttu-id="4e739-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4e739-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4e739-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4e739-115">Properties</span></span>

<span data-ttu-id="4e739-116">La classe **CIM \_ LinkHasConnector** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="4e739-116">The **CIM\_LinkHasConnector** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4e739-117">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="4e739-117">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e739-118">Tipo di dati: **CIM \_ PhysicalLink**</span><span class="sxs-lookup"><span data-stu-id="4e739-118">Data type: **CIM\_PhysicalLink**</span></span>
</dt> <dt>

<span data-ttu-id="4e739-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4e739-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e739-120">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="4e739-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="4e739-121">Un [**\_ PhysicalLink CIM**](cim-physicallink.md) che descrive il collegamento fisico con un connettore.</span><span class="sxs-lookup"><span data-stu-id="4e739-121">A [**CIM\_PhysicalLink**](cim-physicallink.md) that describes the physical link that has a connector.</span></span>

</dd> <dt>

<span data-ttu-id="4e739-122">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="4e739-122">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e739-123">Tipo di dati: **CIM \_ PhysicalConnector**</span><span class="sxs-lookup"><span data-stu-id="4e739-123">Data type: **CIM\_PhysicalConnector**</span></span>
</dt> <dt>

<span data-ttu-id="4e739-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4e739-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4e739-125">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="4e739-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="4e739-126">Un [**\_ PhysicalConnector CIM**](cim-physicalconnector.md) che descrive il connettore fisico.</span><span class="sxs-lookup"><span data-stu-id="4e739-126">A [**CIM\_PhysicalConnector**](cim-physicalconnector.md) that describes the physical connector.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4e739-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="4e739-127">Remarks</span></span>

<span data-ttu-id="4e739-128">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="4e739-128">WMI does not implement this class.</span></span>

<span data-ttu-id="4e739-129">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="4e739-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="4e739-130">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="4e739-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e739-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4e739-131">Requirements</span></span>



| <span data-ttu-id="4e739-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e739-132">Requirement</span></span> | <span data-ttu-id="4e739-133">Valore</span><span class="sxs-lookup"><span data-stu-id="4e739-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4e739-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4e739-134">Minimum supported client</span></span><br/> | <span data-ttu-id="4e739-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4e739-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4e739-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4e739-136">Minimum supported server</span></span><br/> | <span data-ttu-id="4e739-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4e739-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4e739-138">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4e739-138">Namespace</span></span><br/>                | <span data-ttu-id="4e739-139">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="4e739-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4e739-140">MOF</span><span class="sxs-lookup"><span data-stu-id="4e739-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4e739-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4e739-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4e739-142">DLL</span><span class="sxs-lookup"><span data-stu-id="4e739-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e739-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e739-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e739-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4e739-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e739-145">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="4e739-145">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

