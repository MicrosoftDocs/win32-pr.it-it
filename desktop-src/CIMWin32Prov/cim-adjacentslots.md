---
description: L' \_ associazione CIM AdjacentSlots descrive il layout degli slot in una scheda di hosting o scheda di scheda.
ms.assetid: d604647f-7b2f-4f99-8d98-adf115ae9dfb
ms.tgt_platform: multiple
title: Classe CIM_AdjacentSlots
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AdjacentSlots
- CIM_AdjacentSlots.DistanceBetweenSlots
- CIM_AdjacentSlots.SharedSlots
- CIM_AdjacentSlots.SlotA
- CIM_AdjacentSlots.SlotB
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 695f9c668d6f75864e46026deac9a969993596ff
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127222"
---
# <a name="cim_adjacentslots-class"></a><span data-ttu-id="560c7-103">CIM \_ AdjacentSlots (classe)</span><span class="sxs-lookup"><span data-stu-id="560c7-103">CIM\_AdjacentSlots class</span></span>

<span data-ttu-id="560c7-104">L'associazione **CIM \_ AdjacentSlots** descrive il layout degli slot in una scheda di hosting o scheda di scheda.</span><span class="sxs-lookup"><span data-stu-id="560c7-104">The **CIM\_AdjacentSlots** association describes the layout of slots on a hosting board or adapter card.</span></span> <span data-ttu-id="560c7-105">Le informazioni, ad esempio la distanza tra gli slot e il fatto che siano "condivise" (se ne viene popolato uno, non è possibile usare l'altro slot), vengono trasmesse come proprietà di associazione.</span><span class="sxs-lookup"><span data-stu-id="560c7-105">Information, such as the distance between the slots and whether they are "shared" (if one is populated, then the other slot cannot be used), is conveyed as association properties.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="560c7-106">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="560c7-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="560c7-107">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="560c7-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="560c7-108">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="560c7-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="560c7-109">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="560c7-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="560c7-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="560c7-110">Syntax</span></span>

``` syntax
[Abstract, Association, UUID("{FAF76B88-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_AdjacentSlots
{
  real32       DistanceBetweenSlots;
  boolean      SharedSlots;
  CIM_Slot REF SlotA;
  CIM_Slot REF SlotB;
};
```

## <a name="members"></a><span data-ttu-id="560c7-111">Members</span><span class="sxs-lookup"><span data-stu-id="560c7-111">Members</span></span>

<span data-ttu-id="560c7-112">La classe **CIM \_ AdjacentSlots** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="560c7-112">The **CIM\_AdjacentSlots** class has these types of members:</span></span>

-   [<span data-ttu-id="560c7-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="560c7-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="560c7-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="560c7-114">Properties</span></span>

<span data-ttu-id="560c7-115">La classe **CIM \_ AdjacentSlots** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="560c7-115">The **CIM\_AdjacentSlots** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="560c7-116">**DistanceBetweenSlots**</span><span class="sxs-lookup"><span data-stu-id="560c7-116">**DistanceBetweenSlots**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="560c7-117">Tipo di dati: **real32**</span><span class="sxs-lookup"><span data-stu-id="560c7-117">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="560c7-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="560c7-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="560c7-119">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("pollici")</span><span class="sxs-lookup"><span data-stu-id="560c7-119">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="560c7-120">Distanza, in pollici, tra gli slot adiacenti.</span><span class="sxs-lookup"><span data-stu-id="560c7-120">Distance, in inches, between adjacent slots.</span></span>

</dd> <dt>

<span data-ttu-id="560c7-121">**SharedSlots**</span><span class="sxs-lookup"><span data-stu-id="560c7-121">**SharedSlots**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="560c7-122">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="560c7-122">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="560c7-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="560c7-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="560c7-124">Se **true**, uno degli slot viene popolato da una scheda di adapter; l'altro slot deve essere lasciato vuoto.</span><span class="sxs-lookup"><span data-stu-id="560c7-124">If **TRUE**, one of the slots is populated by an adapter card; the other slot must be left empty.</span></span>

</dd> <dt>

<span data-ttu-id="560c7-125">**SlotA**</span><span class="sxs-lookup"><span data-stu-id="560c7-125">**SlotA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="560c7-126">Tipo di dati **: \_ slot CIM**</span><span class="sxs-lookup"><span data-stu-id="560c7-126">Data type: **CIM\_Slot**</span></span>
</dt> <dt>

<span data-ttu-id="560c7-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="560c7-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="560c7-128">Riferimento a uno degli slot adiacenti.</span><span class="sxs-lookup"><span data-stu-id="560c7-128">Reference to one of the adjacent slots.</span></span>

</dd> <dt>

<span data-ttu-id="560c7-129">**SlotB**</span><span class="sxs-lookup"><span data-stu-id="560c7-129">**SlotB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="560c7-130">Tipo di dati **: \_ slot CIM**</span><span class="sxs-lookup"><span data-stu-id="560c7-130">Data type: **CIM\_Slot**</span></span>
</dt> <dt>

<span data-ttu-id="560c7-131">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="560c7-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="560c7-132">Riferimento allo slot adiacente "altro".</span><span class="sxs-lookup"><span data-stu-id="560c7-132">Reference to the "other" adjacent slot.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="560c7-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="560c7-133">Remarks</span></span>

<span data-ttu-id="560c7-134">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="560c7-134">WMI does not implement this class.</span></span>

<span data-ttu-id="560c7-135">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="560c7-135">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="560c7-136">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="560c7-136">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="560c7-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="560c7-137">Requirements</span></span>



| <span data-ttu-id="560c7-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="560c7-138">Requirement</span></span> | <span data-ttu-id="560c7-139">Valore</span><span class="sxs-lookup"><span data-stu-id="560c7-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="560c7-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="560c7-140">Minimum supported client</span></span><br/> | <span data-ttu-id="560c7-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="560c7-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="560c7-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="560c7-142">Minimum supported server</span></span><br/> | <span data-ttu-id="560c7-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="560c7-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="560c7-144">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="560c7-144">Namespace</span></span><br/>                | <span data-ttu-id="560c7-145">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="560c7-145">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="560c7-146">MOF</span><span class="sxs-lookup"><span data-stu-id="560c7-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="560c7-147"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="560c7-147"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="560c7-148">DLL</span><span class="sxs-lookup"><span data-stu-id="560c7-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="560c7-149"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="560c7-149"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="560c7-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="560c7-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="560c7-151">Classi CIM</span><span class="sxs-lookup"><span data-stu-id="560c7-151">CIM Classes</span></span>](/windows/desktop/WmiSdk/cimclas)
</dt> </dl>

 

