---
description: La \_ classe WMI dell'associazione PhysicalMemoryLocation Win32 mette in correlazione una matrice di memoria fisica e la relativa memoria fisica.
ms.assetid: 40252428-77ca-4dfb-8048-c05096a114d8
ms.tgt_platform: multiple
title: Classe Win32_PhysicalMemoryLocation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PhysicalMemoryLocation
- Win32_PhysicalMemoryLocation.LocationWithinContainer
- Win32_PhysicalMemoryLocation.PartComponent
- Win32_PhysicalMemoryLocation.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: daa6d47b13cb5caa74a10f28ab5fcd6e66e1524f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966359"
---
# <a name="win32_physicalmemorylocation-class"></a><span data-ttu-id="3b479-103">Win32 \_ PhysicalMemoryLocation (classe)</span><span class="sxs-lookup"><span data-stu-id="3b479-103">Win32\_PhysicalMemoryLocation class</span></span>

<span data-ttu-id="3b479-104">La [classe WMI](../wmisdk/retrieving-a-class.md) dell'associazione **\_ PhysicalMemoryLocation Win32** mette in correlazione una matrice di memoria fisica e la relativa memoria fisica.</span><span class="sxs-lookup"><span data-stu-id="3b479-104">The **Win32\_PhysicalMemoryLocation** association [WMI class](../wmisdk/retrieving-a-class.md) relates an array of physical memory and its physical memory.</span></span>

<span data-ttu-id="3b479-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="3b479-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="3b479-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="3b479-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b479-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3b479-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{B24EF562-BBBE-11d2-ABFB-00805F538618}"), AMENDMENT]
class Win32_PhysicalMemoryLocation : CIM_PackagedComponent
{
  string                        LocationWithinContainer;
  Win32_PhysicalMemory      REF PartComponent;
  Win32_PhysicalMemoryArray REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="3b479-108">Members</span><span class="sxs-lookup"><span data-stu-id="3b479-108">Members</span></span>

<span data-ttu-id="3b479-109">La classe **Win32 \_ PhysicalMemoryLocation** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="3b479-109">The **Win32\_PhysicalMemoryLocation** class has these types of members:</span></span>

-   [<span data-ttu-id="3b479-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3b479-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3b479-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3b479-111">Properties</span></span>

<span data-ttu-id="3b479-112">La classe **Win32 \_ PhysicalMemoryLocation** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="3b479-112">The **Win32\_PhysicalMemoryLocation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3b479-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="3b479-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b479-114">Tipo di dati: **Win32 \_ PhysicalMemoryArray**</span><span class="sxs-lookup"><span data-stu-id="3b479-114">Data type: **Win32\_PhysicalMemoryArray**</span></span>
</dt> <dt>

<span data-ttu-id="3b479-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3b479-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b479-116">Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ PhysicalMemoryArray")</span><span class="sxs-lookup"><span data-stu-id="3b479-116">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_PhysicalMemoryArray")</span></span>
</dt> </dl>

<span data-ttu-id="3b479-117">[**\_ PhysicalMemoryArray Win32**](win32-physicalmemoryarray.md) che rappresenta la matrice di memoria fisica che contiene la memoria fisica.</span><span class="sxs-lookup"><span data-stu-id="3b479-117">A [**Win32\_PhysicalMemoryArray**](win32-physicalmemoryarray.md) that represents the physical memory array that contains the physical memory.</span></span>

</dd> <dt>

<span data-ttu-id="3b479-118">**LocationWithinContainer**</span><span class="sxs-lookup"><span data-stu-id="3b479-118">**LocationWithinContainer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b479-119">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="3b479-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b479-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3b479-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3b479-121">Stringa in formato libero che rappresenta il posizionamento dell'elemento fisico all'interno del pacchetto fisico.</span><span class="sxs-lookup"><span data-stu-id="3b479-121">Free-form string that represents the positioning of the physical element within the physical package.</span></span> <span data-ttu-id="3b479-122">Le informazioni relative agli elementi stazionari del contenitore (ad esempio, "seconda Bay Drive dalla parte superiore"), angoli, altezze e altri dati possono essere registrate in questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="3b479-122">Information relative to stationary elements in the container (for example, "second drive bay from the top"), angles, altitudes, and other data can be recorded in this property.</span></span> <span data-ttu-id="3b479-123">Questa stringa può essere aggiunta o utilizzata al posto della creazione di un'istanza dell'oggetto [**\_ percorso CIM**](cim-location.md) .</span><span class="sxs-lookup"><span data-stu-id="3b479-123">This string could supplement or be used in place of instantiating the [**CIM\_Location**](cim-location.md) object.</span></span>

<span data-ttu-id="3b479-124">Questa proprietà viene ereditata [**dal \_ contenitore CIM**](cim-container.md).</span><span class="sxs-lookup"><span data-stu-id="3b479-124">This property is inherited from [**CIM\_Container**](cim-container.md).</span></span>

</dd> <dt>

<span data-ttu-id="3b479-125">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="3b479-125">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b479-126">Tipo di dati: **Win32 \_ PhysicalMemory**</span><span class="sxs-lookup"><span data-stu-id="3b479-126">Data type: **Win32\_PhysicalMemory**</span></span>
</dt> <dt>

<span data-ttu-id="3b479-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3b479-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b479-128">Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ PhysicalMemory")</span><span class="sxs-lookup"><span data-stu-id="3b479-128">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_PhysicalMemory")</span></span>
</dt> </dl>

<span data-ttu-id="3b479-129">[**\_ PhysicalMemory Win32**](win32-physicalmemory.md) che rappresenta la memoria fisica contenuta nella matrice di memoria fisica.</span><span class="sxs-lookup"><span data-stu-id="3b479-129">A [**Win32\_PhysicalMemory**](win32-physicalmemory.md) that represents the physical memory contained in the physical memory array.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3b479-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="3b479-130">Remarks</span></span>

<span data-ttu-id="3b479-131">La classe **Win32 \_ PhysicalMemoryLocation** è derivata da [**CIM \_ PackagedComponent**](cim-packagedcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="3b479-131">The **Win32\_PhysicalMemoryLocation** class is derived from [**CIM\_PackagedComponent**](cim-packagedcomponent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3b479-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3b479-132">Requirements</span></span>



| <span data-ttu-id="3b479-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b479-133">Requirement</span></span> | <span data-ttu-id="3b479-134">Valore</span><span class="sxs-lookup"><span data-stu-id="3b479-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b479-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3b479-135">Minimum supported client</span></span><br/> | <span data-ttu-id="3b479-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3b479-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3b479-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3b479-137">Minimum supported server</span></span><br/> | <span data-ttu-id="3b479-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3b479-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3b479-139">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3b479-139">Namespace</span></span><br/>                | <span data-ttu-id="3b479-140">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="3b479-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3b479-141">MOF</span><span class="sxs-lookup"><span data-stu-id="3b479-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3b479-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3b479-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3b479-143">DLL</span><span class="sxs-lookup"><span data-stu-id="3b479-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b479-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b479-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b479-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3b479-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b479-146">**\_PACKAGEDCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="3b479-146">**CIM\_PackagedComponent**</span></span>](cim-packagedcomponent.md)
</dt> <dt>

[<span data-ttu-id="3b479-147">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="3b479-147">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
