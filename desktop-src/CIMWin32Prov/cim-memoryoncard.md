---
description: La \_ classe CIM MemoryOnCard associa la memoria fisica che si trova sulle lavagne di hosting, schede scheda e così via. Questa associazione definisce in modo esplicito la relazione di memoria con le schede.
ms.assetid: 0d094cad-c542-4794-b6e1-87cdc8067668
ms.tgt_platform: multiple
title: Classe CIM_MemoryOnCard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MemoryOnCard
- CIM_MemoryOnCard.LocationWithinContainer
- CIM_MemoryOnCard.PartComponent
- CIM_MemoryOnCard.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2094101ab0cbbbc769194793273bf080cfe52818
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304965"
---
# <a name="cim_memoryoncard-class"></a><span data-ttu-id="89185-104">CIM \_ MemoryOnCard (classe)</span><span class="sxs-lookup"><span data-stu-id="89185-104">CIM\_MemoryOnCard class</span></span>

<span data-ttu-id="89185-105">La classe **CIM \_ MemoryOnCard** associa la memoria fisica che si trova sulle lavagne di hosting, schede scheda e così via.</span><span class="sxs-lookup"><span data-stu-id="89185-105">The **CIM\_MemoryOnCard** class associates physical memory located on hosting boards, adapter cards, and so on.</span></span> <span data-ttu-id="89185-106">Questa associazione definisce in modo esplicito la relazione di memoria con le schede.</span><span class="sxs-lookup"><span data-stu-id="89185-106">This association explicitly defines the relationship of memory to cards.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="89185-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="89185-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="89185-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="89185-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="89185-109">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="89185-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="89185-110">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="89185-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="89185-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="89185-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B7C-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_MemoryOnCard : CIM_PackagedComponent
{
  string                 LocationWithinContainer;
  CIM_PhysicalMemory REF PartComponent;
  CIM_Card           REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="89185-112">Members</span><span class="sxs-lookup"><span data-stu-id="89185-112">Members</span></span>

<span data-ttu-id="89185-113">La classe **CIM \_ MemoryOnCard** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="89185-113">The **CIM\_MemoryOnCard** class has these types of members:</span></span>

-   [<span data-ttu-id="89185-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="89185-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="89185-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="89185-115">Properties</span></span>

<span data-ttu-id="89185-116">La classe **CIM \_ MemoryOnCard** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="89185-116">The **CIM\_MemoryOnCard** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="89185-117">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="89185-117">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89185-118">Tipo di dati **: \_ scheda CIM**</span><span class="sxs-lookup"><span data-stu-id="89185-118">Data type: **CIM\_Card**</span></span>
</dt> <dt>

<span data-ttu-id="89185-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="89185-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89185-120">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="89185-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="89185-121">Una [**\_ scheda CIM**](cim-card.md) che descrive la scheda che include la memoria o ' Contains '.</span><span class="sxs-lookup"><span data-stu-id="89185-121">A [**CIM\_Card**](cim-card.md) describing the card that includes or 'contains' memory.</span></span>

</dd> <dt>

<span data-ttu-id="89185-122">**LocationWithinContainer**</span><span class="sxs-lookup"><span data-stu-id="89185-122">**LocationWithinContainer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89185-123">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="89185-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="89185-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="89185-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89185-125">Stringa in formato libero che rappresenta il posizionamento dell'elemento fisico all'interno del pacchetto fisico.</span><span class="sxs-lookup"><span data-stu-id="89185-125">Free-form string that represents the positioning of the physical element within the physical package.</span></span> <span data-ttu-id="89185-126">Le informazioni relative agli elementi stazionari del contenitore (ad esempio, "seconda Bay Drive dalla parte superiore"), angoli, altezze e altri dati possono essere registrate in questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="89185-126">Information relative to stationary elements in the container (for example, "second drive bay from the top"), angles, altitudes, and other data can be recorded in this property.</span></span> <span data-ttu-id="89185-127">Questa stringa può essere aggiunta o utilizzata al posto della creazione di un'istanza dell'oggetto [**\_ percorso CIM**](cim-location.md) .</span><span class="sxs-lookup"><span data-stu-id="89185-127">This string could supplement or be used in place of instantiating the [**CIM\_Location**](cim-location.md) object.</span></span>

<span data-ttu-id="89185-128">Questa proprietà viene ereditata [**dal \_ contenitore CIM**](cim-container.md).</span><span class="sxs-lookup"><span data-stu-id="89185-128">This property is inherited from [**CIM\_Container**](cim-container.md).</span></span>

</dd> <dt>

<span data-ttu-id="89185-129">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="89185-129">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89185-130">Tipo di dati: **CIM \_ PhysicalMemory**</span><span class="sxs-lookup"><span data-stu-id="89185-130">Data type: **CIM\_PhysicalMemory**</span></span>
</dt> <dt>

<span data-ttu-id="89185-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="89185-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89185-132">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="89185-132">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="89185-133">Un [**\_ PhysicalMemory CIM**](cim-physicalmemory.md) che descrive la memoria fisica che si trova nella scheda.</span><span class="sxs-lookup"><span data-stu-id="89185-133">A [**CIM\_PhysicalMemory**](cim-physicalmemory.md) describing the physical memory which is located on the card.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="89185-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="89185-134">Remarks</span></span>

<span data-ttu-id="89185-135">La classe **CIM \_ MemoryOnCard** è derivata da [**CIM \_ PackagedComponent**](cim-packagedcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="89185-135">The **CIM\_MemoryOnCard** class is derived from [**CIM\_PackagedComponent**](cim-packagedcomponent.md).</span></span>

<span data-ttu-id="89185-136">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="89185-136">WMI does not implement this class.</span></span>

<span data-ttu-id="89185-137">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="89185-137">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="89185-138">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="89185-138">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="89185-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="89185-139">Requirements</span></span>



| <span data-ttu-id="89185-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="89185-140">Requirement</span></span> | <span data-ttu-id="89185-141">Valore</span><span class="sxs-lookup"><span data-stu-id="89185-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="89185-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="89185-142">Minimum supported client</span></span><br/> | <span data-ttu-id="89185-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="89185-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="89185-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="89185-144">Minimum supported server</span></span><br/> | <span data-ttu-id="89185-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="89185-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="89185-146">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="89185-146">Namespace</span></span><br/>                | <span data-ttu-id="89185-147">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="89185-147">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="89185-148">MOF</span><span class="sxs-lookup"><span data-stu-id="89185-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="89185-149"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="89185-149"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="89185-150">DLL</span><span class="sxs-lookup"><span data-stu-id="89185-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="89185-151"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89185-151"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89185-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="89185-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89185-153">**\_PACKAGEDCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="89185-153">**CIM\_PackagedComponent**</span></span>](cim-packagedcomponent.md)
</dt> </dl>

 

