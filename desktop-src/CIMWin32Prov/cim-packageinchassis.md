---
description: L' \_ associazione CIM PackageInChassis rappresenta la relazione in cui uno chassis può contenere altri pacchetti, ad esempio altri chassis e schede.
ms.assetid: 3243bc0f-ce20-4108-b6e3-838bcb8f2fec
ms.tgt_platform: multiple
title: Classe CIM_PackageInChassis
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PackageInChassis
- CIM_PackageInChassis.LocationWithinContainer
- CIM_PackageInChassis.PartComponent
- CIM_PackageInChassis.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 26b65f983970c91d36e8d0a301277c67a2cc5639
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483357"
---
# <a name="cim_packageinchassis-class"></a><span data-ttu-id="628d4-103">CIM \_ PackageInChassis (classe)</span><span class="sxs-lookup"><span data-stu-id="628d4-103">CIM\_PackageInChassis class</span></span>

<span data-ttu-id="628d4-104">L'associazione **CIM \_ PackageInChassis** rappresenta la relazione in cui uno chassis può contenere altri pacchetti, ad esempio altri chassis e schede.</span><span class="sxs-lookup"><span data-stu-id="628d4-104">The **CIM\_PackageInChassis** association represents the relationship in which a chassis can contain other packages, such as other chassis and cards.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="628d4-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="628d4-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="628d4-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="628d4-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="628d4-107">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="628d4-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="628d4-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="628d4-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="628d4-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="628d4-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B74-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PackageInChassis : CIM_Container
{
  string                  LocationWithinContainer;
  CIM_PhysicalPackage REF PartComponent;
  CIM_Chassis         REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="628d4-110">Members</span><span class="sxs-lookup"><span data-stu-id="628d4-110">Members</span></span>

<span data-ttu-id="628d4-111">La classe **CIM \_ PackageInChassis** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="628d4-111">The **CIM\_PackageInChassis** class has these types of members:</span></span>

-   [<span data-ttu-id="628d4-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="628d4-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="628d4-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="628d4-113">Properties</span></span>

<span data-ttu-id="628d4-114">La classe **CIM \_ PackageInChassis** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="628d4-114">The **CIM\_PackageInChassis** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="628d4-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="628d4-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="628d4-116">Tipo di dati **: \_ chassis CIM**</span><span class="sxs-lookup"><span data-stu-id="628d4-116">Data type: **CIM\_Chassis**</span></span>
</dt> <dt>

<span data-ttu-id="628d4-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="628d4-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="628d4-118">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="628d4-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="628d4-119">[**\_ Chassis CIM**](cim-chassis.md) che descrive lo chassis che contiene altri pacchetti fisici.</span><span class="sxs-lookup"><span data-stu-id="628d4-119">A [**CIM\_Chassis**](cim-chassis.md) describing the chassis that contains other physical packages.</span></span>

</dd> <dt>

<span data-ttu-id="628d4-120">**LocationWithinContainer**</span><span class="sxs-lookup"><span data-stu-id="628d4-120">**LocationWithinContainer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="628d4-121">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="628d4-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="628d4-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="628d4-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="628d4-123">Stringa in formato libero che rappresenta il posizionamento dell'elemento fisico all'interno del pacchetto fisico.</span><span class="sxs-lookup"><span data-stu-id="628d4-123">Free-form string that represents the positioning of the physical element within the physical package.</span></span> <span data-ttu-id="628d4-124">Le informazioni relative agli elementi stazionari del contenitore (ad esempio, "seconda Bay Drive dalla parte superiore"), angoli, altezze e altri dati possono essere registrate in questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="628d4-124">Information relative to stationary elements in the container (for example, "second drive bay from the top"), angles, altitudes, and other data can be recorded in this property.</span></span> <span data-ttu-id="628d4-125">Questa stringa può essere aggiunta o utilizzata al posto della creazione di un'istanza dell'oggetto [**\_ percorso CIM**](cim-location.md) .</span><span class="sxs-lookup"><span data-stu-id="628d4-125">This string could supplement or be used in place of instantiating the [**CIM\_Location**](cim-location.md) object.</span></span>

<span data-ttu-id="628d4-126">Questa proprietà viene ereditata [**dal \_ contenitore CIM**](cim-container.md).</span><span class="sxs-lookup"><span data-stu-id="628d4-126">This property is inherited from [**CIM\_Container**](cim-container.md).</span></span>

</dd> <dt>

<span data-ttu-id="628d4-127">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="628d4-127">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="628d4-128">Tipo di dati: **CIM \_ PhysicalPackage**</span><span class="sxs-lookup"><span data-stu-id="628d4-128">Data type: **CIM\_PhysicalPackage**</span></span>
</dt> <dt>

<span data-ttu-id="628d4-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="628d4-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="628d4-130">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="628d4-130">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="628d4-131">Un [**\_ PhysicalPackage CIM**](cim-physicalpackage.md) che descrive il pacchetto fisico contenuto nello chassis.</span><span class="sxs-lookup"><span data-stu-id="628d4-131">A [**CIM\_PhysicalPackage**](cim-physicalpackage.md) describing the physical package which is contained in the chassis.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="628d4-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="628d4-132">Remarks</span></span>

<span data-ttu-id="628d4-133">La classe **CIM \_ PackageInChassis** è derivata dal [**\_ contenitore CIM**](cim-container.md).</span><span class="sxs-lookup"><span data-stu-id="628d4-133">The **CIM\_PackageInChassis** class is derived from [**CIM\_Container**](cim-container.md).</span></span>

<span data-ttu-id="628d4-134">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="628d4-134">WMI does not implement this class.</span></span>

<span data-ttu-id="628d4-135">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="628d4-135">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="628d4-136">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="628d4-136">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="628d4-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="628d4-137">Requirements</span></span>



| <span data-ttu-id="628d4-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="628d4-138">Requirement</span></span> | <span data-ttu-id="628d4-139">Valore</span><span class="sxs-lookup"><span data-stu-id="628d4-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="628d4-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="628d4-140">Minimum supported client</span></span><br/> | <span data-ttu-id="628d4-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="628d4-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="628d4-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="628d4-142">Minimum supported server</span></span><br/> | <span data-ttu-id="628d4-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="628d4-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="628d4-144">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="628d4-144">Namespace</span></span><br/>                | <span data-ttu-id="628d4-145">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="628d4-145">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="628d4-146">MOF</span><span class="sxs-lookup"><span data-stu-id="628d4-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="628d4-147"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="628d4-147"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="628d4-148">DLL</span><span class="sxs-lookup"><span data-stu-id="628d4-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="628d4-149"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="628d4-149"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="628d4-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="628d4-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="628d4-151">**\_Contenitore CIM**</span><span class="sxs-lookup"><span data-stu-id="628d4-151">**CIM\_Container**</span></span>](cim-container.md)
</dt> </dl>

 

