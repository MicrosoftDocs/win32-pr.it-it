---
description: L' \_ associazione CIM ChassisInRack rappresenta il &\# 0034, che contiene \# 0034&relazione tra un rack e uno chassis che contiene.
ms.assetid: 1c8a5058-58fe-42e0-b337-7e1a05120789
ms.tgt_platform: multiple
title: Classe CIM_ChassisInRack
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ChassisInRack
- CIM_ChassisInRack.LocationWithinContainer
- CIM_ChassisInRack.PartComponent
- CIM_ChassisInRack.GroupComponent
- CIM_ChassisInRack.BottomU
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fd582991df30bc36cd71c4c3fa08d9a5a5153819
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127114"
---
# <a name="cim_chassisinrack-class"></a><span data-ttu-id="4d841-103">CIM \_ ChassisInRack (classe)</span><span class="sxs-lookup"><span data-stu-id="4d841-103">CIM\_ChassisInRack class</span></span>

<span data-ttu-id="4d841-104">L'associazione **CIM \_ ChassisInRack** rappresenta la relazione "containing" tra un rack e uno chassis che contiene.</span><span class="sxs-lookup"><span data-stu-id="4d841-104">The **CIM\_ChassisInRack** association represents the "containing" relationship between a rack and a chassis that it contains.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4d841-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="4d841-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="4d841-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="4d841-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="4d841-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="4d841-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="4d841-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="4d841-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d841-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4d841-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B73-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_ChassisInRack : CIM_Container
{
  string          LocationWithinContainer;
  CIM_Chassis REF PartComponent;
  CIM_Rack    REF GroupComponent;
  uint16          BottomU;
};
```

## <a name="members"></a><span data-ttu-id="4d841-110">Members</span><span class="sxs-lookup"><span data-stu-id="4d841-110">Members</span></span>

<span data-ttu-id="4d841-111">La classe **CIM \_ ChassisInRack** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="4d841-111">The **CIM\_ChassisInRack** class has these types of members:</span></span>

-   [<span data-ttu-id="4d841-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4d841-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4d841-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4d841-113">Properties</span></span>

<span data-ttu-id="4d841-114">La classe **CIM \_ ChassisInRack** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="4d841-114">The **CIM\_ChassisInRack** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4d841-115">**In basso**</span><span class="sxs-lookup"><span data-stu-id="4d841-115">**BottomU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d841-116">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4d841-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4d841-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4d841-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d841-118">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("US")</span><span class="sxs-lookup"><span data-stu-id="4d841-118">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Us")</span></span>
</dt> </dl>

<span data-ttu-id="4d841-119">Integer che indica la "U" più bassa o inferiore in cui è montato lo chassis.</span><span class="sxs-lookup"><span data-stu-id="4d841-119">Integer that indicates the lowest or bottom "U" in which the chassis is mounted.</span></span> <span data-ttu-id="4d841-120">Un "U" è un'unità di misura standard per l'altezza di un rack o un componente montabile su rack ed è uguale a 1,75 centimetri o 4,445 centimetri.</span><span class="sxs-lookup"><span data-stu-id="4d841-120">A "U" is a standard unit of measure for the height of a rack, or rack-mountable component, and is equal to 1.75 inches or 4.445 centimeters.</span></span>

</dd> <dt>

<span data-ttu-id="4d841-121">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="4d841-121">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d841-122">Tipo di dati **: \_ rack CIM**</span><span class="sxs-lookup"><span data-stu-id="4d841-122">Data type: **CIM\_Rack**</span></span>
</dt> <dt>

<span data-ttu-id="4d841-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4d841-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d841-124">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="4d841-124">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="4d841-125">Un [**\_ rack CIM**](cim-rack.md) che descrive il rack che contiene lo chassis.</span><span class="sxs-lookup"><span data-stu-id="4d841-125">A [**CIM\_Rack**](cim-rack.md) that describes the rack that contains the chassis.</span></span>

</dd> <dt>

<span data-ttu-id="4d841-126">**LocationWithinContainer**</span><span class="sxs-lookup"><span data-stu-id="4d841-126">**LocationWithinContainer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d841-127">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="4d841-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d841-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4d841-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d841-129">Stringa in formato libero che rappresenta il posizionamento dell'elemento fisico all'interno del pacchetto fisico.</span><span class="sxs-lookup"><span data-stu-id="4d841-129">Free-form string that represents the positioning of the physical element within the physical package.</span></span> <span data-ttu-id="4d841-130">Le informazioni relative agli elementi stazionari del contenitore (ad esempio, "seconda Bay Drive dalla parte superiore"), angoli, altezze e altri dati possono essere registrate in questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="4d841-130">Information relative to stationary elements in the container (for example, "second drive bay from the top"), angles, altitudes, and other data can be recorded in this property.</span></span> <span data-ttu-id="4d841-131">Questa stringa può essere aggiunta o utilizzata al posto della creazione di un'istanza dell'oggetto [**\_ percorso CIM**](cim-location.md) .</span><span class="sxs-lookup"><span data-stu-id="4d841-131">This string could supplement or be used in place of instantiating the [**CIM\_Location**](cim-location.md) object.</span></span>

<span data-ttu-id="4d841-132">Questa proprietà viene ereditata [**dal \_ contenitore CIM**](cim-container.md).</span><span class="sxs-lookup"><span data-stu-id="4d841-132">This property is inherited from [**CIM\_Container**](cim-container.md).</span></span>

</dd> <dt>

<span data-ttu-id="4d841-133">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="4d841-133">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d841-134">Tipo di dati **: \_ chassis CIM**</span><span class="sxs-lookup"><span data-stu-id="4d841-134">Data type: **CIM\_Chassis**</span></span>
</dt> <dt>

<span data-ttu-id="4d841-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4d841-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d841-136">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="4d841-136">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="4d841-137">[**\_ Chassis CIM**](cim-chassis.md) che descrive lo chassis montato nel rack.</span><span class="sxs-lookup"><span data-stu-id="4d841-137">A [**CIM\_Chassis**](cim-chassis.md) that describes the chassis which is mounted in the rack.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4d841-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="4d841-138">Remarks</span></span>

<span data-ttu-id="4d841-139">La classe **CIM \_ ChassisInRack** è derivata dal [**\_ contenitore CIM**](cim-container.md).</span><span class="sxs-lookup"><span data-stu-id="4d841-139">The **CIM\_ChassisInRack** class is derived from [**CIM\_Container**](cim-container.md).</span></span>

<span data-ttu-id="4d841-140">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="4d841-140">WMI does not implement this class.</span></span>

<span data-ttu-id="4d841-141">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="4d841-141">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="4d841-142">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="4d841-142">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d841-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4d841-143">Requirements</span></span>



| <span data-ttu-id="4d841-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d841-144">Requirement</span></span> | <span data-ttu-id="4d841-145">Valore</span><span class="sxs-lookup"><span data-stu-id="4d841-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4d841-146">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4d841-146">Minimum supported client</span></span><br/> | <span data-ttu-id="4d841-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4d841-147">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4d841-148">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4d841-148">Minimum supported server</span></span><br/> | <span data-ttu-id="4d841-149">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4d841-149">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4d841-150">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4d841-150">Namespace</span></span><br/>                | <span data-ttu-id="4d841-151">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="4d841-151">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4d841-152">MOF</span><span class="sxs-lookup"><span data-stu-id="4d841-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4d841-153"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4d841-153"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4d841-154">DLL</span><span class="sxs-lookup"><span data-stu-id="4d841-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4d841-155"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d841-155"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d841-156">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4d841-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d841-157">**\_Contenitore CIM**</span><span class="sxs-lookup"><span data-stu-id="4d841-157">**CIM\_Container**</span></span>](cim-container.md)
</dt> </dl>

 

