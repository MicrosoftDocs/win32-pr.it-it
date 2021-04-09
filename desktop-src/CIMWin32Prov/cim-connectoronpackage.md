---
description: La \_ classe CIM ConnectorOnPackage rappresenta un'associazione che rende esplicita la relazione di contenimento tra i connettori e i pacchetti. I pacchetti fisici contengono connettori, oltre ad altri elementi fisici.
ms.assetid: 67cfb8c7-b952-452c-aeb4-0f06b2b0570b
ms.tgt_platform: multiple
title: Classe CIM_ConnectorOnPackage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ConnectorOnPackage
- CIM_ConnectorOnPackage.LocationWithinContainer
- CIM_ConnectorOnPackage.PartComponent
- CIM_ConnectorOnPackage.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9dfac5cf2daa19f1d3c073ac65d30fa859d2523b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877977"
---
# <a name="cim_connectoronpackage-class"></a><span data-ttu-id="9fec4-104">CIM \_ ConnectorOnPackage (classe)</span><span class="sxs-lookup"><span data-stu-id="9fec4-104">CIM\_ConnectorOnPackage class</span></span>

<span data-ttu-id="9fec4-105">La classe **CIM \_ ConnectorOnPackage** rappresenta un'associazione che rende esplicita la relazione di contenimento tra i connettori e i pacchetti.</span><span class="sxs-lookup"><span data-stu-id="9fec4-105">The **CIM\_ConnectorOnPackage** class represents an association that makes explicit the containment relationship between connectors and packages.</span></span> <span data-ttu-id="9fec4-106">I pacchetti fisici contengono connettori, oltre ad altri elementi fisici.</span><span class="sxs-lookup"><span data-stu-id="9fec4-106">Physical packages contain connectors as well as other physical elements.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9fec4-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="9fec4-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="9fec4-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="9fec4-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="9fec4-109">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="9fec4-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="9fec4-110">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="9fec4-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fec4-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9fec4-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B8C-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_ConnectorOnPackage : CIM_Container
{
  string                    LocationWithinContainer;
  CIM_PhysicalConnector REF PartComponent;
  CIM_PhysicalPackage   REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="9fec4-112">Members</span><span class="sxs-lookup"><span data-stu-id="9fec4-112">Members</span></span>

<span data-ttu-id="9fec4-113">La classe **CIM \_ ConnectorOnPackage** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="9fec4-113">The **CIM\_ConnectorOnPackage** class has these types of members:</span></span>

-   [<span data-ttu-id="9fec4-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9fec4-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9fec4-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9fec4-115">Properties</span></span>

<span data-ttu-id="9fec4-116">La classe **CIM \_ ConnectorOnPackage** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="9fec4-116">The **CIM\_ConnectorOnPackage** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9fec4-117">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="9fec4-117">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fec4-118">Tipo di dati: **CIM \_ PhysicalPackage**</span><span class="sxs-lookup"><span data-stu-id="9fec4-118">Data type: **CIM\_PhysicalPackage**</span></span>
</dt> <dt>

<span data-ttu-id="9fec4-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9fec4-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9fec4-120">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="9fec4-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="9fec4-121">Un [**\_ PhysicalPackage CIM**](cim-physicalpackage.md) che descrive il pacchetto fisico con un connettore.</span><span class="sxs-lookup"><span data-stu-id="9fec4-121">A [**CIM\_PhysicalPackage**](cim-physicalpackage.md) that describes the physical package that has a connector.</span></span>

</dd> <dt>

<span data-ttu-id="9fec4-122">**LocationWithinContainer**</span><span class="sxs-lookup"><span data-stu-id="9fec4-122">**LocationWithinContainer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fec4-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9fec4-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9fec4-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9fec4-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9fec4-125">Stringa in formato libero che rappresenta il posizionamento dell'elemento fisico all'interno del pacchetto fisico.</span><span class="sxs-lookup"><span data-stu-id="9fec4-125">Free-form string that represents the positioning of the physical element within the physical package.</span></span> <span data-ttu-id="9fec4-126">Le informazioni relative agli elementi stazionari del contenitore (ad esempio, "seconda Bay Drive dalla parte superiore"), angoli, altezze e altri dati possono essere registrate in questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="9fec4-126">Information relative to stationary elements in the container (for example, "second drive bay from the top"), angles, altitudes, and other data can be recorded in this property.</span></span> <span data-ttu-id="9fec4-127">Questa stringa può essere aggiunta o utilizzata al posto della creazione di un'istanza dell'oggetto [**\_ percorso CIM**](cim-location.md) .</span><span class="sxs-lookup"><span data-stu-id="9fec4-127">This string could supplement or be used in place of instantiating the [**CIM\_Location**](cim-location.md) object.</span></span>

<span data-ttu-id="9fec4-128">Questa proprietà viene ereditata [**dal \_ contenitore CIM**](cim-container.md).</span><span class="sxs-lookup"><span data-stu-id="9fec4-128">This property is inherited from [**CIM\_Container**](cim-container.md).</span></span>

</dd> <dt>

<span data-ttu-id="9fec4-129">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="9fec4-129">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fec4-130">Tipo di dati: **CIM \_ PhysicalConnector**</span><span class="sxs-lookup"><span data-stu-id="9fec4-130">Data type: **CIM\_PhysicalConnector**</span></span>
</dt> <dt>

<span data-ttu-id="9fec4-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9fec4-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9fec4-132">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="9fec4-132">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="9fec4-133">Un [**\_ PhysicalConnector CIM**](cim-physicalconnector.md) che descrive il connettore fisico.</span><span class="sxs-lookup"><span data-stu-id="9fec4-133">A [**CIM\_PhysicalConnector**](cim-physicalconnector.md) that describes the physical connector.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9fec4-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="9fec4-134">Remarks</span></span>

<span data-ttu-id="9fec4-135">La classe **CIM \_ ConnectorOnPackage** è derivata dal [**\_ contenitore CIM**](cim-container.md).</span><span class="sxs-lookup"><span data-stu-id="9fec4-135">The **CIM\_ConnectorOnPackage** class is derived from [**CIM\_Container**](cim-container.md).</span></span>

<span data-ttu-id="9fec4-136">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="9fec4-136">WMI does not implement this class.</span></span>

<span data-ttu-id="9fec4-137">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="9fec4-137">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="9fec4-138">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="9fec4-138">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9fec4-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9fec4-139">Requirements</span></span>



| <span data-ttu-id="9fec4-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="9fec4-140">Requirement</span></span> | <span data-ttu-id="9fec4-141">Valore</span><span class="sxs-lookup"><span data-stu-id="9fec4-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9fec4-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9fec4-142">Minimum supported client</span></span><br/> | <span data-ttu-id="9fec4-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9fec4-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9fec4-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9fec4-144">Minimum supported server</span></span><br/> | <span data-ttu-id="9fec4-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9fec4-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9fec4-146">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9fec4-146">Namespace</span></span><br/>                | <span data-ttu-id="9fec4-147">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="9fec4-147">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9fec4-148">MOF</span><span class="sxs-lookup"><span data-stu-id="9fec4-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9fec4-149"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9fec4-149"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9fec4-150">DLL</span><span class="sxs-lookup"><span data-stu-id="9fec4-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9fec4-151"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9fec4-151"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9fec4-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9fec4-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fec4-153">**\_Contenitore CIM**</span><span class="sxs-lookup"><span data-stu-id="9fec4-153">**CIM\_Container**</span></span>](cim-container.md)
</dt> </dl>

 

