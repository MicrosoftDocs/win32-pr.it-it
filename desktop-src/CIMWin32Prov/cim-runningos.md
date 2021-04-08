---
description: La \_ classe CIM RunningOS rappresenta il sistema operativo attualmente in esecuzione. Al massimo, un sistema operativo può essere eseguito in qualsiasi momento in un computer. il computer potrebbe non essere attualmente avviato o il sistema operativo potrebbe essere sconosciuto.
ms.assetid: 93e3d425-d751-4252-aa81-7d6774c8f8c5
ms.tgt_platform: multiple
title: Classe CIM_RunningOS
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RunningOS
- CIM_RunningOS.Dependent
- CIM_RunningOS.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1ff86af88342a1b8f0147ecd9721765794faf39e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748951"
---
# <a name="cim_runningos-class"></a><span data-ttu-id="c0f60-104">\_Classe CIM RunningOS</span><span class="sxs-lookup"><span data-stu-id="c0f60-104">CIM\_RunningOS class</span></span>

<span data-ttu-id="c0f60-105">La classe **CIM \_ RunningOS** rappresenta il sistema operativo attualmente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="c0f60-105">The **CIM\_RunningOS** class represents the currently executing operating system.</span></span> <span data-ttu-id="c0f60-106">Al massimo, un sistema operativo può essere eseguito in qualsiasi momento in un computer. il computer potrebbe non essere attualmente avviato o il sistema operativo potrebbe essere sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="c0f60-106">At most, one operating system can execute at any time on a computer system; the computer system may not be currently booted, or its operating system may be unknown.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c0f60-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="c0f60-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c0f60-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="c0f60-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c0f60-109">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="c0f60-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="c0f60-110">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="c0f60-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0f60-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c0f60-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{1F2EA300-DB37-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_RunningOS : CIM_Dependency
{
  CIM_ComputerSystem  REF Dependent;
  CIM_OperatingSystem REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="c0f60-112">Members</span><span class="sxs-lookup"><span data-stu-id="c0f60-112">Members</span></span>

<span data-ttu-id="c0f60-113">La classe **CIM \_ RunningOS** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="c0f60-113">The **CIM\_RunningOS** class has these types of members:</span></span>

-   [<span data-ttu-id="c0f60-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c0f60-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c0f60-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c0f60-115">Properties</span></span>

<span data-ttu-id="c0f60-116">La classe **CIM \_ RunningOS** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="c0f60-116">The **CIM\_RunningOS** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c0f60-117">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="c0f60-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0f60-118">Tipo di dati: **CIM \_ OperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="c0f60-118">Data type: **CIM\_OperatingSystem**</span></span>
</dt> <dt>

<span data-ttu-id="c0f60-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c0f60-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0f60-120">Qualificatori: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="c0f60-120">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="c0f60-121">Un [**\_ OperatingSystem CIM**](cim-operatingsystem.md) che descrive il sistema operativo attualmente in esecuzione nel computer.</span><span class="sxs-lookup"><span data-stu-id="c0f60-121">A [**CIM\_OperatingSystem**](cim-operatingsystem.md) that describes the operating system currently running on the computer system.</span></span>

</dd> <dt>

<span data-ttu-id="c0f60-122">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="c0f60-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0f60-123">Tipo di dati: **CIM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="c0f60-123">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="c0f60-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="c0f60-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0f60-125">Qualificatori: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="c0f60-125">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="c0f60-126">Un [**\_ ComputerSystem CIM**](cim-computersystem.md) che descrive il computer.</span><span class="sxs-lookup"><span data-stu-id="c0f60-126">A [**CIM\_ComputerSystem**](cim-computersystem.md) that describes the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c0f60-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="c0f60-127">Remarks</span></span>

<span data-ttu-id="c0f60-128">La classe **CIM \_ RunningOS** è derivata dalla [**\_ dipendenza CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="c0f60-128">The **CIM\_RunningOS** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="c0f60-129">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="c0f60-129">WMI does not implement this class.</span></span>

<span data-ttu-id="c0f60-130">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="c0f60-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c0f60-131">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="c0f60-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0f60-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c0f60-132">Requirements</span></span>



| <span data-ttu-id="c0f60-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0f60-133">Requirement</span></span> | <span data-ttu-id="c0f60-134">Valore</span><span class="sxs-lookup"><span data-stu-id="c0f60-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c0f60-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c0f60-135">Minimum supported client</span></span><br/> | <span data-ttu-id="c0f60-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c0f60-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c0f60-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c0f60-137">Minimum supported server</span></span><br/> | <span data-ttu-id="c0f60-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c0f60-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c0f60-139">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c0f60-139">Namespace</span></span><br/>                | <span data-ttu-id="c0f60-140">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="c0f60-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c0f60-141">MOF</span><span class="sxs-lookup"><span data-stu-id="c0f60-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c0f60-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c0f60-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c0f60-143">DLL</span><span class="sxs-lookup"><span data-stu-id="c0f60-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0f60-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0f60-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0f60-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c0f60-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0f60-146">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="c0f60-146">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

