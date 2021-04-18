---
description: L' \_ associazione CIM ActionSequence definisce una serie di operazioni che consentono di eseguire la transizione dell'elemento software (a cui fa riferimento l' \_ associazione CIM SoftwareElementActions) allo stato successivo oppure di rimuovere l'elemento software dallo stato corrente.
ms.assetid: b539c424-bc2a-414b-b56c-72550004720f
ms.tgt_platform: multiple
title: Classe CIM_ActionSequence
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ActionSequence
- CIM_ActionSequence.Next
- CIM_ActionSequence.Prior
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 71150d1ad9785d81579d8f305fe46bc6b7e57d00
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304783"
---
# <a name="cim_actionsequence-class"></a><span data-ttu-id="86afc-103">CIM \_ ActionSequence (classe)</span><span class="sxs-lookup"><span data-stu-id="86afc-103">CIM\_ActionSequence class</span></span>

<span data-ttu-id="86afc-104">L'associazione **CIM \_ ActionSequence** definisce una serie di operazioni che consentono di eseguire la transizione dell'elemento software (a cui fa riferimento l'associazione [**CIM \_ SoftwareElementActions**](cim-softwareelementactions.md) ) allo stato successivo oppure di rimuovere l'elemento software dallo stato corrente.</span><span class="sxs-lookup"><span data-stu-id="86afc-104">The **CIM\_ActionSequence** association defines a series of operations that transition the software element (referenced by the [**CIM\_SoftwareElementActions**](cim-softwareelementactions.md) association) to its next state, or removes the software element from its current state.</span></span>

<span data-ttu-id="86afc-105">Le azioni successive e le azioni di disinstallazione associate a un particolare elemento software devono essere una sequenza continua.</span><span class="sxs-lookup"><span data-stu-id="86afc-105">The next-state actions and uninstall actions associated with a particular software element must be a continuous sequence.</span></span> <span data-ttu-id="86afc-106">Poiché **CIM \_ ActionSequence** è un'associazione, i cicli sulla classe [**di \_ azione CIM**](cim-action.md) , con i ruoli per l'azione "Priore" e "Next", formano una sequenza.</span><span class="sxs-lookup"><span data-stu-id="86afc-106">Since **CIM\_ActionSequence** is an association, the loops on the [**CIM\_Action**](cim-action.md) class, with roles for the "prior" action and "next" action, form a sequence.</span></span>

<span data-ttu-id="86afc-107">La necessità di una sequenza continua implica:</span><span class="sxs-lookup"><span data-stu-id="86afc-107">The need for a continuous sequence implies:</span></span>

-   <span data-ttu-id="86afc-108">All'interno del set di azioni di disinstallazione o di stato successivo, esiste una sola azione che non ha un'istanza dell'associazione **CIM \_ ActionSequence** che fa riferimento a essa nel ruolo "Next".</span><span class="sxs-lookup"><span data-stu-id="86afc-108">Within the set of next-state or uninstall actions, there is only one action that does not have an instance of the **CIM\_ActionSequence** association referencing it in the "next" role.</span></span> <span data-ttu-id="86afc-109">Si tratta della prima azione della sequenza.</span><span class="sxs-lookup"><span data-stu-id="86afc-109">This is the first action in the sequence.</span></span>
-   <span data-ttu-id="86afc-110">All'interno del set di azioni di disinstallazione o di stato successivo, esiste una sola azione che non ha un'istanza dell'associazione **CIM \_ ActionSequence** che fa riferimento a essa nel ruolo "Priore".</span><span class="sxs-lookup"><span data-stu-id="86afc-110">Within the set of next-state or uninstall actions, there is only one action that does not have an instance of the **CIM\_ActionSequence** association referencing it in the "prior" role.</span></span> <span data-ttu-id="86afc-111">Si tratta dell'ultima azione della sequenza.</span><span class="sxs-lookup"><span data-stu-id="86afc-111">This is the last action in the sequence.</span></span>
-   <span data-ttu-id="86afc-112">Tutte le altre azioni all'interno del set di azioni di stato e di disinstallazione successive devono far parte di due istanze dell'associazione **CIM \_ ActionSequence** , una in un ruolo "Priore" e una nel ruolo "Next".</span><span class="sxs-lookup"><span data-stu-id="86afc-112">All other actions within the set of next-state and uninstall actions must participate in two instances of the **CIM\_ActionSequence** association, one in a "prior" role and one in the "next" role.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="86afc-113">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="86afc-113">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="86afc-114">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="86afc-114">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="86afc-115">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="86afc-115">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="86afc-116">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="86afc-116">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="86afc-117">Sintassi</span><span class="sxs-lookup"><span data-stu-id="86afc-117">Syntax</span></span>

``` syntax
[Abstract, Association, UUID("{F127E50E-E3E0-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_ActionSequence
{
  CIM_Action REF Next;
  CIM_Action REF Prior;
};
```

## <a name="members"></a><span data-ttu-id="86afc-118">Members</span><span class="sxs-lookup"><span data-stu-id="86afc-118">Members</span></span>

<span data-ttu-id="86afc-119">La classe **CIM \_ ActionSequence** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="86afc-119">The **CIM\_ActionSequence** class has these types of members:</span></span>

-   [<span data-ttu-id="86afc-120">Proprietà</span><span class="sxs-lookup"><span data-stu-id="86afc-120">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="86afc-121">Proprietà</span><span class="sxs-lookup"><span data-stu-id="86afc-121">Properties</span></span>

<span data-ttu-id="86afc-122">La classe **CIM \_ ActionSequence** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="86afc-122">The **CIM\_ActionSequence** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="86afc-123">**Avanti**</span><span class="sxs-lookup"><span data-stu-id="86afc-123">**Next**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86afc-124">Tipo di dati **: \_ azione CIM**</span><span class="sxs-lookup"><span data-stu-id="86afc-124">Data type: **CIM\_Action**</span></span>
</dt> <dt>

<span data-ttu-id="86afc-125">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="86afc-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86afc-126">Qualificatori: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="86afc-126">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="86afc-127">Riferimento all'azione successiva.</span><span class="sxs-lookup"><span data-stu-id="86afc-127">Reference to the next action.</span></span>

</dd> <dt>

<span data-ttu-id="86afc-128">**Prima**</span><span class="sxs-lookup"><span data-stu-id="86afc-128">**Prior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="86afc-129">Tipo di dati **: \_ azione CIM**</span><span class="sxs-lookup"><span data-stu-id="86afc-129">Data type: **CIM\_Action**</span></span>
</dt> <dt>

<span data-ttu-id="86afc-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="86afc-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="86afc-131">Qualificatori: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="86afc-131">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="86afc-132">Riferimento all'azione precedente.</span><span class="sxs-lookup"><span data-stu-id="86afc-132">Reference to the prior action.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="86afc-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="86afc-133">Remarks</span></span>

<span data-ttu-id="86afc-134">Le classi di [**\_ azione CIM**](cim-action.md) che partecipano a questa associazione devono avere lo stesso valore per la proprietà **Direction** .</span><span class="sxs-lookup"><span data-stu-id="86afc-134">The [**CIM\_Action**](cim-action.md) classes participating in this association must have the same value for the **Direction** property.</span></span>

<span data-ttu-id="86afc-135">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="86afc-135">WMI does not implement this class.</span></span>

<span data-ttu-id="86afc-136">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="86afc-136">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="86afc-137">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="86afc-137">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="86afc-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="86afc-138">Requirements</span></span>



| <span data-ttu-id="86afc-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="86afc-139">Requirement</span></span> | <span data-ttu-id="86afc-140">Valore</span><span class="sxs-lookup"><span data-stu-id="86afc-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="86afc-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="86afc-141">Minimum supported client</span></span><br/> | <span data-ttu-id="86afc-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="86afc-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="86afc-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="86afc-143">Minimum supported server</span></span><br/> | <span data-ttu-id="86afc-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="86afc-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="86afc-145">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="86afc-145">Namespace</span></span><br/>                | <span data-ttu-id="86afc-146">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="86afc-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="86afc-147">MOF</span><span class="sxs-lookup"><span data-stu-id="86afc-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="86afc-148"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="86afc-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="86afc-149">DLL</span><span class="sxs-lookup"><span data-stu-id="86afc-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="86afc-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86afc-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86afc-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="86afc-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86afc-152">Classi CIM</span><span class="sxs-lookup"><span data-stu-id="86afc-152">CIM Classes</span></span>](/windows/desktop/WmiSdk/cimclas)
</dt> </dl>

 

