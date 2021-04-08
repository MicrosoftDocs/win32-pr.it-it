---
description: La \_ classe di associazione CIM SoftwareElementChecks mette in correlazione un elemento software con informazioni sulla condizione o sulla posizione che possono essere richieste da una funzionalità.
ms.assetid: ff130fe9-ddb2-4e4f-86d3-53f1d8ed14aa
ms.tgt_platform: multiple
title: Classe CIM_SoftwareElementChecks
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareElementChecks
- CIM_SoftwareElementChecks.Check
- CIM_SoftwareElementChecks.Element
- CIM_SoftwareElementChecks.Phase
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ea6fcb02794174e825994f70270745741c9b7713
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877485"
---
# <a name="cim_softwareelementchecks-class"></a><span data-ttu-id="51fda-103">CIM \_ SoftwareElementChecks (classe)</span><span class="sxs-lookup"><span data-stu-id="51fda-103">CIM\_SoftwareElementChecks class</span></span>

<span data-ttu-id="51fda-104">La classe di associazione **CIM \_ SoftwareElementChecks** mette in correlazione un elemento software con informazioni sulla condizione o sulla posizione che possono essere richieste da una funzionalità.</span><span class="sxs-lookup"><span data-stu-id="51fda-104">The **CIM\_SoftwareElementChecks** association class relates a software element with condition or location information that a feature may require.</span></span>

<span data-ttu-id="51fda-105">Poiché gli elementi software in uno stato pronto per l'esecuzione non possono passare a un altro stato, il valore della proprietà **fase** è limitato allo stato per gli oggetti [**CIM \_ SoftwareElement**](cim-softwareelement.md) in uno stato pronto per l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="51fda-105">Because software elements in a ready-to-run state cannot transition into another state, the value of the **Phase** property is restricted to in-state for [**CIM\_SoftwareElement**](cim-softwareelement.md) objects in a ready-to-run state.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="51fda-106">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="51fda-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="51fda-107">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="51fda-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="51fda-108">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="51fda-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="51fda-109">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="51fda-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="51fda-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="51fda-110">Syntax</span></span>

``` syntax
[UUID("{24783E8A-DB31-11d2-85FC-0000F8102E5F}"), Association, Aggregation, Abstract, AMENDMENT]
class CIM_SoftwareElementChecks
{
  CIM_Check           REF Check;
  CIM_SoftwareElement REF Element;
  uint16                  Phase;
};
```

## <a name="members"></a><span data-ttu-id="51fda-111">Members</span><span class="sxs-lookup"><span data-stu-id="51fda-111">Members</span></span>

<span data-ttu-id="51fda-112">La classe **CIM \_ SoftwareElementChecks** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="51fda-112">The **CIM\_SoftwareElementChecks** class has these types of members:</span></span>

-   [<span data-ttu-id="51fda-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="51fda-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="51fda-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="51fda-114">Properties</span></span>

<span data-ttu-id="51fda-115">La classe **CIM \_ SoftwareElementChecks** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="51fda-115">The **CIM\_SoftwareElementChecks** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="51fda-116">**Controllo**</span><span class="sxs-lookup"><span data-stu-id="51fda-116">**Check**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51fda-117">Tipo di dati **: \_ controllo CIM**</span><span class="sxs-lookup"><span data-stu-id="51fda-117">Data type: **CIM\_Check**</span></span>
</dt> <dt>

<span data-ttu-id="51fda-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="51fda-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51fda-119">Qualificatori: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (false), [**debole**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="51fda-119">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (FALSE), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="51fda-120">Riferimento al controllo.</span><span class="sxs-lookup"><span data-stu-id="51fda-120">Reference to the check.</span></span>

</dd> <dt>

<span data-ttu-id="51fda-121">**elemento**</span><span class="sxs-lookup"><span data-stu-id="51fda-121">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51fda-122">Tipo di dati: **CIM \_ SoftwareElement**</span><span class="sxs-lookup"><span data-stu-id="51fda-122">Data type: **CIM\_SoftwareElement**</span></span>
</dt> <dt>

<span data-ttu-id="51fda-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="51fda-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51fda-124">Qualificatori: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="51fda-124">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="51fda-125">Riferimento all'elemento.</span><span class="sxs-lookup"><span data-stu-id="51fda-125">Reference to the element.</span></span>

</dd> <dt>

<span data-ttu-id="51fda-126">**Fase**</span><span class="sxs-lookup"><span data-stu-id="51fda-126">**Phase**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51fda-127">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="51fda-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="51fda-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="51fda-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="51fda-129">Indica se il controllo a cui si fa riferimento è un controllo in stato o un controllo di stato successivo.</span><span class="sxs-lookup"><span data-stu-id="51fda-129">Indicates whether the referenced check is an in-state check or a next-state check.</span></span>

<dt>

<span id="In-State"></span><span id="in-state"></span><span id="IN-STATE"></span>

<span data-ttu-id="51fda-130">**In-state** (0)</span><span class="sxs-lookup"><span data-stu-id="51fda-130">**In-State** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Next-State"></span><span id="next-state"></span><span id="NEXT-STATE"></span>

<span data-ttu-id="51fda-131">**Stato successivo** (1)</span><span class="sxs-lookup"><span data-stu-id="51fda-131">**Next-State** (1)</span></span>


<span data-ttu-id="51fda-132"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="51fda-132"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="51fda-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="51fda-133">Remarks</span></span>

<span data-ttu-id="51fda-134">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="51fda-134">WMI does not implement this class.</span></span> <span data-ttu-id="51fda-135">Per le classi WMI derivate da **CIM \_ SoftwareElementChecks**, vedere [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="51fda-135">For WMI classes derived from **CIM\_SoftwareElementChecks**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="51fda-136">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="51fda-136">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="51fda-137">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="51fda-137">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="51fda-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="51fda-138">Requirements</span></span>



| <span data-ttu-id="51fda-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="51fda-139">Requirement</span></span> | <span data-ttu-id="51fda-140">Valore</span><span class="sxs-lookup"><span data-stu-id="51fda-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="51fda-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="51fda-141">Minimum supported client</span></span><br/> | <span data-ttu-id="51fda-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="51fda-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="51fda-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="51fda-143">Minimum supported server</span></span><br/> | <span data-ttu-id="51fda-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="51fda-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="51fda-145">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="51fda-145">Namespace</span></span><br/>                | <span data-ttu-id="51fda-146">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="51fda-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="51fda-147">MOF</span><span class="sxs-lookup"><span data-stu-id="51fda-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="51fda-148"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="51fda-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="51fda-149">DLL</span><span class="sxs-lookup"><span data-stu-id="51fda-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="51fda-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="51fda-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

