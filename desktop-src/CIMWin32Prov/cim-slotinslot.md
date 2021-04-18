---
description: La \_ relazione CIM SlotInSlot rappresenta la capacità di un adattatore speciale di estendere la struttura degli slot esistente per consentire l'inserimento di schede altrimenti incompatibili in un frame o in una lavagna di hosting.
ms.assetid: 688231de-49fd-415d-b2c8-ef0dd4dcaee4
ms.tgt_platform: multiple
title: Classe CIM_SlotInSlot
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SlotInSlot
- CIM_SlotInSlot.Dependent
- CIM_SlotInSlot.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0102a431393906b5ff98339569a027cbe3ef5b40
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304491"
---
# <a name="cim_slotinslot-class"></a><span data-ttu-id="81154-103">CIM \_ SlotInSlot (classe)</span><span class="sxs-lookup"><span data-stu-id="81154-103">CIM\_SlotInSlot class</span></span>

<span data-ttu-id="81154-104">La relazione **CIM \_ SlotInSlot** rappresenta la capacità di un adattatore speciale di estendere la struttura degli slot esistente per consentire l'inserimento di schede altrimenti incompatibili in un frame o in una lavagna di hosting.</span><span class="sxs-lookup"><span data-stu-id="81154-104">The **CIM\_SlotInSlot** relationship represents the ability of a special adapter to extend the existing slot structure to enable otherwise incompatible cards to be plugged into a frame or hosting board.</span></span> <span data-ttu-id="81154-105">Gli slot sono tipi speciali di connettori in cui vengono in genere inserite le schede scheda.</span><span class="sxs-lookup"><span data-stu-id="81154-105">Slots are special types of connectors into which adapter cards are typically inserted.</span></span> <span data-ttu-id="81154-106">L'adapter crea in modo efficace un nuovo slot e può essere considerato (concettualmente) come uno slot in uno slot.</span><span class="sxs-lookup"><span data-stu-id="81154-106">The adapter effectively creates a new slot and can be thought of (conceptually) as a slot in a slot.</span></span> <span data-ttu-id="81154-107">Le schede che altrimenti sarebbero fisicamente o elettricamente incompatibili con gli slot esistenti sarebbero supportate dall'interazione con lo slot fornito dall'adapter.</span><span class="sxs-lookup"><span data-stu-id="81154-107">Cards that would otherwise be physically or electrically incompatible with the existing slots would be supported by interfacing to the slot provided by the adapter.</span></span> <span data-ttu-id="81154-108">Le schede di rete, ad esempio, sono molto costose.</span><span class="sxs-lookup"><span data-stu-id="81154-108">For example, networking boards are very expensive.</span></span> <span data-ttu-id="81154-109">Quando diventa disponibile un nuovo hardware, le configurazioni dello chassis e della scheda cambiano.</span><span class="sxs-lookup"><span data-stu-id="81154-109">As new hardware becomes available, chassis and card configurations change.</span></span> <span data-ttu-id="81154-110">Per proteggere l'investimento dei clienti, i fornitori di reti produrrà adattatori speciali che consentono alle vecchie schede di rientrare in nuovi chassis o lavagne di hosting o nuove schede per adattarle a schede obsolete usando un adattatore speciale che si adatta a uno o più slot esistenti e presenta un nuovo slot in cui è possibile adattare la scheda.</span><span class="sxs-lookup"><span data-stu-id="81154-110">To protect the investment of their customers, networking vendors will manufacture special adapters that enable old cards to fit into new chassis or hosting boards or new cards to fit into old cards by using a special adapter that fits over one or more existing slots and presents a new slot into which the card can fit.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="81154-111">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="81154-111">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="81154-112">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="81154-112">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="81154-113">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="81154-113">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="81154-114">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="81154-114">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="81154-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="81154-115">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B87-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_SlotInSlot : CIM_ConnectedTo
{
  CIM_Slot REF Dependent;
  CIM_Slot REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="81154-116">Members</span><span class="sxs-lookup"><span data-stu-id="81154-116">Members</span></span>

<span data-ttu-id="81154-117">La classe **CIM \_ SlotInSlot** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="81154-117">The **CIM\_SlotInSlot** class has these types of members:</span></span>

-   [<span data-ttu-id="81154-118">Proprietà</span><span class="sxs-lookup"><span data-stu-id="81154-118">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="81154-119">Proprietà</span><span class="sxs-lookup"><span data-stu-id="81154-119">Properties</span></span>

<span data-ttu-id="81154-120">La classe **CIM \_ SlotInSlot** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="81154-120">The **CIM\_SlotInSlot** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="81154-121">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="81154-121">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81154-122">Tipo di dati **: \_ slot CIM**</span><span class="sxs-lookup"><span data-stu-id="81154-122">Data type: **CIM\_Slot**</span></span>
</dt> <dt>

<span data-ttu-id="81154-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="81154-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81154-124">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="81154-124">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="81154-125">Uno [**\_ slot CIM**](cim-slot.md) che descrive gli slot esistenti della lavagna di hosting o il frame che viene adattato per contenere una scheda che altrimenti non sarebbe fisicamente e/o elettricamente compatibile con essa.</span><span class="sxs-lookup"><span data-stu-id="81154-125">A [**CIM\_Slot**](cim-slot.md) that describes the existing slot(s) of the hosting board, or frame that are being adapted to accommodate a card that would otherwise not be physically and/or electrically compatible with it.</span></span>

</dd> <dt>

<span data-ttu-id="81154-126">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="81154-126">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81154-127">Tipo di dati **: \_ slot CIM**</span><span class="sxs-lookup"><span data-stu-id="81154-127">Data type: **CIM\_Slot**</span></span>
</dt> <dt>

<span data-ttu-id="81154-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="81154-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="81154-129">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente"), [**massimo**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="81154-129">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="81154-130">Uno [**\_ slot CIM**](cim-slot.md) che descrive il nuovo slot fornito dalla scheda adapter.</span><span class="sxs-lookup"><span data-stu-id="81154-130">A [**CIM\_Slot**](cim-slot.md) that describes the new slot provided by the adapter board.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="81154-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="81154-131">Remarks</span></span>

<span data-ttu-id="81154-132">La classe **CIM \_ SlotInSlot** è derivata da [**CIM \_ ConnectedTo**](cim-connectedto.md).</span><span class="sxs-lookup"><span data-stu-id="81154-132">The **CIM\_SlotInSlot** class is derived from [**CIM\_ConnectedTo**](cim-connectedto.md).</span></span>

<span data-ttu-id="81154-133">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="81154-133">WMI does not implement this class.</span></span>

<span data-ttu-id="81154-134">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="81154-134">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="81154-135">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="81154-135">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="81154-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="81154-136">Requirements</span></span>



| <span data-ttu-id="81154-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="81154-137">Requirement</span></span> | <span data-ttu-id="81154-138">Valore</span><span class="sxs-lookup"><span data-stu-id="81154-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="81154-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="81154-139">Minimum supported client</span></span><br/> | <span data-ttu-id="81154-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="81154-140">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="81154-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="81154-141">Minimum supported server</span></span><br/> | <span data-ttu-id="81154-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="81154-142">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="81154-143">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="81154-143">Namespace</span></span><br/>                | <span data-ttu-id="81154-144">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="81154-144">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="81154-145">MOF</span><span class="sxs-lookup"><span data-stu-id="81154-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="81154-146"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="81154-146"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="81154-147">DLL</span><span class="sxs-lookup"><span data-stu-id="81154-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81154-148"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81154-148"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81154-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="81154-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81154-150">**\_CONNECTEDTO CIM**</span><span class="sxs-lookup"><span data-stu-id="81154-150">**CIM\_ConnectedTo**</span></span>](cim-connectedto.md)
</dt> </dl>

 

