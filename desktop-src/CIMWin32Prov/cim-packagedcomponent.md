---
description: L' \_ associazione CIM PackagedComponent rappresenta una relazione esplicita in cui un componente è in genere contenuto in un pacchetto fisico, ad esempio uno chassis o una scheda.
ms.assetid: ef0cdbc4-41ee-4517-92ca-61cfcbe64c36
ms.tgt_platform: multiple
title: Classe CIM_PackagedComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PackagedComponent
- CIM_PackagedComponent.LocationWithinContainer
- CIM_PackagedComponent.PartComponent
- CIM_PackagedComponent.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1b95cbbea60bfbd6bb352e53cfecb8819d99ec24
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877393"
---
# <a name="cim_packagedcomponent-class"></a><span data-ttu-id="0c7ba-103">CIM \_ PackagedComponent (classe)</span><span class="sxs-lookup"><span data-stu-id="0c7ba-103">CIM\_PackagedComponent class</span></span>

<span data-ttu-id="0c7ba-104">L'associazione **CIM \_ PackagedComponent** rappresenta una relazione esplicita in cui un componente è in genere contenuto in un pacchetto fisico, ad esempio uno chassis o una scheda.</span><span class="sxs-lookup"><span data-stu-id="0c7ba-104">The **CIM\_PackagedComponent** association represents an explicit relationship in which a component is typically contained by a physical package, such as a chassis or card.</span></span>

<span data-ttu-id="0c7ba-105">**Nota**  Un componente può essere rimosso o non ancora inserito in, il pacchetto che lo contiene (ovvero la proprietà booleana **rimovibile** è **true**).</span><span class="sxs-lookup"><span data-stu-id="0c7ba-105">**Note**  A component may be removed from, or not yet inserted into, its containing package (that is, the **Removable** Boolean property is **TRUE**).</span></span> <span data-ttu-id="0c7ba-106">È pertanto possibile che un componente non sia sempre associato a un contenitore.</span><span class="sxs-lookup"><span data-stu-id="0c7ba-106">Therefore, a component may not always be associated with a container.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0c7ba-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="0c7ba-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="0c7ba-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="0c7ba-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="0c7ba-109">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="0c7ba-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="0c7ba-110">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="0c7ba-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c7ba-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0c7ba-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B79-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PackagedComponent : CIM_Container
{
  string                    LocationWithinContainer;
  CIM_PhysicalComponent REF PartComponent;
  CIM_PhysicalPackage   REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="0c7ba-112">Members</span><span class="sxs-lookup"><span data-stu-id="0c7ba-112">Members</span></span>

<span data-ttu-id="0c7ba-113">La classe **CIM \_ PackagedComponent** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="0c7ba-113">The **CIM\_PackagedComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="0c7ba-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0c7ba-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0c7ba-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0c7ba-115">Properties</span></span>

<span data-ttu-id="0c7ba-116">La classe **CIM \_ PackagedComponent** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="0c7ba-116">The **CIM\_PackagedComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0c7ba-117">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="0c7ba-117">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c7ba-118">Tipo di dati: **CIM \_ PhysicalPackage**</span><span class="sxs-lookup"><span data-stu-id="0c7ba-118">Data type: **CIM\_PhysicalPackage**</span></span>
</dt> <dt>

<span data-ttu-id="0c7ba-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0c7ba-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c7ba-120">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="0c7ba-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="0c7ba-121">Un [**\_ PhysicalPackage CIM**](cim-physicalpackage.md) che descrive il pacchetto fisico che contiene i componenti.</span><span class="sxs-lookup"><span data-stu-id="0c7ba-121">A [**CIM\_PhysicalPackage**](cim-physicalpackage.md) that describes the physical package that contains component(s).</span></span>

</dd> <dt>

<span data-ttu-id="0c7ba-122">**LocationWithinContainer**</span><span class="sxs-lookup"><span data-stu-id="0c7ba-122">**LocationWithinContainer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c7ba-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0c7ba-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c7ba-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0c7ba-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c7ba-125">Stringa in formato libero che rappresenta il posizionamento dell'elemento fisico all'interno del pacchetto fisico.</span><span class="sxs-lookup"><span data-stu-id="0c7ba-125">Free-form string that represents the positioning of the physical element within the physical package.</span></span> <span data-ttu-id="0c7ba-126">Le informazioni relative agli elementi stazionari del contenitore (ad esempio, "seconda Bay Drive dalla parte superiore"), angoli, altezze e altri dati possono essere registrate in questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="0c7ba-126">Information relative to stationary elements in the container (for example, "second drive bay from the top"), angles, altitudes, and other data can be recorded in this property.</span></span> <span data-ttu-id="0c7ba-127">Questa stringa può essere aggiunta o utilizzata al posto della creazione di un'istanza dell'oggetto [**\_ percorso CIM**](cim-location.md) .</span><span class="sxs-lookup"><span data-stu-id="0c7ba-127">This string could supplement or be used in place of instantiating the [**CIM\_Location**](cim-location.md) object.</span></span>

<span data-ttu-id="0c7ba-128">Questa proprietà viene ereditata [**dal \_ contenitore CIM**](cim-container.md).</span><span class="sxs-lookup"><span data-stu-id="0c7ba-128">This property is inherited from [**CIM\_Container**](cim-container.md).</span></span>

</dd> <dt>

<span data-ttu-id="0c7ba-129">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="0c7ba-129">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c7ba-130">Tipo di dati: **CIM \_ PhysicalComponent**</span><span class="sxs-lookup"><span data-stu-id="0c7ba-130">Data type: **CIM\_PhysicalComponent**</span></span>
</dt> <dt>

<span data-ttu-id="0c7ba-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0c7ba-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c7ba-132">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="0c7ba-132">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="0c7ba-133">Un [**\_ PhysicalComponent CIM**](cim-physicalcomponent.md) che descrive il componente fisico contenuto nel pacchetto.</span><span class="sxs-lookup"><span data-stu-id="0c7ba-133">A [**CIM\_PhysicalComponent**](cim-physicalcomponent.md) describing the physical component which is contained in the package.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0c7ba-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="0c7ba-134">Remarks</span></span>

<span data-ttu-id="0c7ba-135">La classe **CIM \_ PackagedComponent** è derivata dal [**\_ contenitore CIM**](cim-container.md).</span><span class="sxs-lookup"><span data-stu-id="0c7ba-135">The **CIM\_PackagedComponent** class is derived from [**CIM\_Container**](cim-container.md).</span></span>

<span data-ttu-id="0c7ba-136">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="0c7ba-136">WMI does not implement this class.</span></span>

<span data-ttu-id="0c7ba-137">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="0c7ba-137">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="0c7ba-138">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="0c7ba-138">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c7ba-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0c7ba-139">Requirements</span></span>



| <span data-ttu-id="0c7ba-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c7ba-140">Requirement</span></span> | <span data-ttu-id="0c7ba-141">Valore</span><span class="sxs-lookup"><span data-stu-id="0c7ba-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0c7ba-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0c7ba-142">Minimum supported client</span></span><br/> | <span data-ttu-id="0c7ba-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0c7ba-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0c7ba-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0c7ba-144">Minimum supported server</span></span><br/> | <span data-ttu-id="0c7ba-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0c7ba-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0c7ba-146">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0c7ba-146">Namespace</span></span><br/>                | <span data-ttu-id="0c7ba-147">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="0c7ba-147">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0c7ba-148">MOF</span><span class="sxs-lookup"><span data-stu-id="0c7ba-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0c7ba-149"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0c7ba-149"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0c7ba-150">DLL</span><span class="sxs-lookup"><span data-stu-id="0c7ba-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0c7ba-151"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0c7ba-151"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c7ba-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0c7ba-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c7ba-153">**\_Contenitore CIM**</span><span class="sxs-lookup"><span data-stu-id="0c7ba-153">**CIM\_Container**</span></span>](cim-container.md)
</dt> </dl>

 

