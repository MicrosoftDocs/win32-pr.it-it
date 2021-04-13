---
description: L' \_ associazione CIM CardOnCard descrive le relazioni sulle schede che possono essere inserite in schede madri/battiscopa, daughtercards di un adapter o schede che supportano moduli speciali di tipo scheda.
ms.assetid: a500b29d-d836-4755-b5df-b296e3cbd2ab
ms.tgt_platform: multiple
title: Classe CIM_CardOnCard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CardOnCard
- CIM_CardOnCard.LocationWithinContainer
- CIM_CardOnCard.PartComponent
- CIM_CardOnCard.GroupComponent
- CIM_CardOnCard.MountOrSlotDescription
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 15f94bb8d0f159e71cac44f069f9d8e7d9453509
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401458"
---
# <a name="cim_cardoncard-class"></a><span data-ttu-id="182bc-103">CIM \_ CardOnCard (classe)</span><span class="sxs-lookup"><span data-stu-id="182bc-103">CIM\_CardOnCard class</span></span>

<span data-ttu-id="182bc-104">L'associazione **CIM \_ CardOnCard** descrive le relazioni sulle schede che possono essere inserite in schede madri/battiscopa, daughtercards di un adapter o schede che supportano moduli speciali di tipo scheda.</span><span class="sxs-lookup"><span data-stu-id="182bc-104">The **CIM\_CardOnCard** association describes relationships about cards that can be plugged into motherboards/baseboards, daughtercards of an adapter, or cards that support special card-like modules.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="182bc-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="182bc-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="182bc-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="182bc-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="182bc-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="182bc-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="182bc-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="182bc-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="182bc-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="182bc-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B77-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_CardOnCard : CIM_Container
{
  string       LocationWithinContainer;
  CIM_Card REF PartComponent;
  CIM_Card REF GroupComponent;
  string       MountOrSlotDescription;
};
```

## <a name="members"></a><span data-ttu-id="182bc-110">Members</span><span class="sxs-lookup"><span data-stu-id="182bc-110">Members</span></span>

<span data-ttu-id="182bc-111">La classe **CIM \_ CardOnCard** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="182bc-111">The **CIM\_CardOnCard** class has these types of members:</span></span>

-   [<span data-ttu-id="182bc-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="182bc-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="182bc-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="182bc-113">Properties</span></span>

<span data-ttu-id="182bc-114">La classe **CIM \_ CardOnCard** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="182bc-114">The **CIM\_CardOnCard** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="182bc-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="182bc-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="182bc-116">Tipo di dati **: \_ scheda CIM**</span><span class="sxs-lookup"><span data-stu-id="182bc-116">Data type: **CIM\_Card**</span></span>
</dt> <dt>

<span data-ttu-id="182bc-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="182bc-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="182bc-118">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="182bc-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="182bc-119">Una [**\_ scheda CIM**](cim-card.md) che descrive la scheda che ospita un'altra scheda.</span><span class="sxs-lookup"><span data-stu-id="182bc-119">A [**CIM\_Card**](cim-card.md) that describes the card that hosts another card.</span></span>

</dd> <dt>

<span data-ttu-id="182bc-120">**LocationWithinContainer**</span><span class="sxs-lookup"><span data-stu-id="182bc-120">**LocationWithinContainer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="182bc-121">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="182bc-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="182bc-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="182bc-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="182bc-123">Stringa in formato libero che rappresenta il posizionamento dell'elemento fisico all'interno del pacchetto fisico.</span><span class="sxs-lookup"><span data-stu-id="182bc-123">Free-form string that represents the positioning of the physical element within the physical package.</span></span> <span data-ttu-id="182bc-124">Le informazioni relative agli elementi stazionari del contenitore (ad esempio, "seconda Bay Drive dalla parte superiore"), angoli, altezze e altri dati possono essere registrate in questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="182bc-124">Information relative to stationary elements in the container (for example, "second drive bay from the top"), angles, altitudes, and other data can be recorded in this property.</span></span> <span data-ttu-id="182bc-125">Questa stringa può essere aggiunta o utilizzata al posto della creazione di un'istanza dell'oggetto [**\_ percorso CIM**](cim-location.md) .</span><span class="sxs-lookup"><span data-stu-id="182bc-125">This string could supplement or be used in place of instantiating the [**CIM\_Location**](cim-location.md) object.</span></span>

<span data-ttu-id="182bc-126">Questa proprietà viene ereditata [**dal \_ contenitore CIM**](cim-container.md).</span><span class="sxs-lookup"><span data-stu-id="182bc-126">This property is inherited from [**CIM\_Container**](cim-container.md).</span></span>

</dd> <dt>

<span data-ttu-id="182bc-127">**MountOrSlotDescription**</span><span class="sxs-lookup"><span data-stu-id="182bc-127">**MountOrSlotDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="182bc-128">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="182bc-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="182bc-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="182bc-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="182bc-130">Descrive e identifica il modo in cui la scheda è montata o collegata alla scheda "altro".</span><span class="sxs-lookup"><span data-stu-id="182bc-130">Describes and identifies how the card is mounted on or plugged into the "other" card.</span></span> <span data-ttu-id="182bc-131">Le informazioni sugli slot possono essere incluse in questo campo e possono essere sufficienti per determinati scopi di gestione, evitando di creare creazioni di istanze di oggetti connettore/slot solo per modellare la relazione tra le schede e le lavagne di hosting o altri adapter.</span><span class="sxs-lookup"><span data-stu-id="182bc-131">Slot information can be included in this field and may be sufficient for certain management purposes, which avoids creating instantiations of connector/slot objects just to model the relationship of cards to hosting boards or other adapters.</span></span> <span data-ttu-id="182bc-132">D'altra parte, se sono disponibili informazioni sullo slot e sul connettore, questo campo può essere usato per fornire dati dettagliati di inserimento di slot o di montaggio.</span><span class="sxs-lookup"><span data-stu-id="182bc-132">On the other hand, if slot and connector information is available, this field can be used to provide detailed mounting or slot insertion data.</span></span>

</dd> <dt>

<span data-ttu-id="182bc-133">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="182bc-133">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="182bc-134">Tipo di dati **: \_ scheda CIM**</span><span class="sxs-lookup"><span data-stu-id="182bc-134">Data type: **CIM\_Card**</span></span>
</dt> <dt>

<span data-ttu-id="182bc-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="182bc-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="182bc-136">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="182bc-136">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="182bc-137">Una [**\_ scheda CIM**](cim-card.md) che descrive la scheda collegata o montata in altro modo su un'altra scheda.</span><span class="sxs-lookup"><span data-stu-id="182bc-137">A [**CIM\_Card**](cim-card.md) that describes the card that is plugged into or otherwise mounted on another card.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="182bc-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="182bc-138">Remarks</span></span>

<span data-ttu-id="182bc-139">La classe **CIM \_ CardOnCard** è derivata dal [**\_ contenitore CIM**](cim-container.md).</span><span class="sxs-lookup"><span data-stu-id="182bc-139">The **CIM\_CardOnCard** class is derived from [**CIM\_Container**](cim-container.md).</span></span>

<span data-ttu-id="182bc-140">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="182bc-140">WMI does not implement this class.</span></span>

<span data-ttu-id="182bc-141">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="182bc-141">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="182bc-142">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="182bc-142">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="182bc-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="182bc-143">Requirements</span></span>



| <span data-ttu-id="182bc-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="182bc-144">Requirement</span></span> | <span data-ttu-id="182bc-145">Valore</span><span class="sxs-lookup"><span data-stu-id="182bc-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="182bc-146">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="182bc-146">Minimum supported client</span></span><br/> | <span data-ttu-id="182bc-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="182bc-147">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="182bc-148">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="182bc-148">Minimum supported server</span></span><br/> | <span data-ttu-id="182bc-149">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="182bc-149">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="182bc-150">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="182bc-150">Namespace</span></span><br/>                | <span data-ttu-id="182bc-151">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="182bc-151">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="182bc-152">MOF</span><span class="sxs-lookup"><span data-stu-id="182bc-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="182bc-153"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="182bc-153"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="182bc-154">DLL</span><span class="sxs-lookup"><span data-stu-id="182bc-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="182bc-155"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="182bc-155"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="182bc-156">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="182bc-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="182bc-157">**\_Contenitore CIM**</span><span class="sxs-lookup"><span data-stu-id="182bc-157">**CIM\_Container**</span></span>](cim-container.md)
</dt> </dl>

 

