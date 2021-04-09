---
description: La \_ classe CIM AssociatedProcessorMemory associa il processore e la memoria di sistema o la cache di un processore.
ms.assetid: a4c28a0a-e4cc-4db2-bd77-b7b5023eace6
ms.tgt_platform: multiple
title: Classe CIM_AssociatedProcessorMemory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AssociatedProcessorMemory
- CIM_AssociatedProcessorMemory.Antecedent
- CIM_AssociatedProcessorMemory.Dependent
- CIM_AssociatedProcessorMemory.BusSpeed
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f35cdca92cb15e1c6fff215ff1363844e0d47012
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966235"
---
# <a name="cim_associatedprocessormemory-class"></a><span data-ttu-id="d1682-103">CIM \_ AssociatedProcessorMemory (classe)</span><span class="sxs-lookup"><span data-stu-id="d1682-103">CIM\_AssociatedProcessorMemory class</span></span>

<span data-ttu-id="d1682-104">La classe **CIM \_ AssociatedProcessorMemory** associa il processore e la memoria di sistema o la cache di un processore.</span><span class="sxs-lookup"><span data-stu-id="d1682-104">The **CIM\_AssociatedProcessorMemory** class associates the processor and system memory, or a processor's cache.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d1682-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="d1682-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="d1682-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="d1682-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="d1682-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="d1682-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="d1682-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="d1682-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1682-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d1682-109">Syntax</span></span>

``` syntax
[abstract, UUID("{464FFAB1-946F-11d2-AAE2-006008C78BC7}"), AMENDMENT]
class CIM_AssociatedProcessorMemory : CIM_AssociatedMemory
{
  CIM_Memory    REF Antecedent;
  CIM_Processor REF Dependent;
  uint32            BusSpeed;
};
```

## <a name="members"></a><span data-ttu-id="d1682-110">Members</span><span class="sxs-lookup"><span data-stu-id="d1682-110">Members</span></span>

<span data-ttu-id="d1682-111">La classe **CIM \_ AssociatedProcessorMemory** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="d1682-111">The **CIM\_AssociatedProcessorMemory** class has these types of members:</span></span>

-   [<span data-ttu-id="d1682-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d1682-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d1682-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d1682-113">Properties</span></span>

<span data-ttu-id="d1682-114">La classe **CIM \_ AssociatedProcessorMemory** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="d1682-114">The **CIM\_AssociatedProcessorMemory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d1682-115">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="d1682-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1682-116">Tipo di dati **: \_ memoria CIM**</span><span class="sxs-lookup"><span data-stu-id="d1682-116">Data type: **CIM\_Memory**</span></span>
</dt> <dt>

<span data-ttu-id="d1682-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d1682-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1682-118">[**\_ Memoria CIM**](cim-memory.md) che descrive la memoria installata in o associata a un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d1682-118">A [**CIM\_Memory**](cim-memory.md) that describes the memory installed on or associated with a device.</span></span>

<span data-ttu-id="d1682-119">Questa proprietà viene ereditata da [**CIM \_ AssociatedMemory**](cim-associatedmemory.md).</span><span class="sxs-lookup"><span data-stu-id="d1682-119">This property is inherited from [**CIM\_AssociatedMemory**](cim-associatedmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1682-120">**BusSpeed**</span><span class="sxs-lookup"><span data-stu-id="d1682-120">**BusSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1682-121">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d1682-121">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d1682-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d1682-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1682-123">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("megahertz")</span><span class="sxs-lookup"><span data-stu-id="d1682-123">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("megahertz")</span></span>
</dt> </dl>

<span data-ttu-id="d1682-124">Velocità del bus, in megahertz (MHz), tra il processore e la memoria.</span><span class="sxs-lookup"><span data-stu-id="d1682-124">Speed of the bus, in megahertz (MHz), between the processor and memory.</span></span>

</dd> <dt>

<span data-ttu-id="d1682-125">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="d1682-125">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1682-126">Tipo di dati **: \_ processore CIM**</span><span class="sxs-lookup"><span data-stu-id="d1682-126">Data type: **CIM\_Processor**</span></span>
</dt> <dt>

<span data-ttu-id="d1682-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d1682-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1682-128">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="d1682-128">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="d1682-129">Un [**\_ processore CIM**](cim-processor.md) che descrive il processore che accede alla memoria o utilizza la cache.</span><span class="sxs-lookup"><span data-stu-id="d1682-129">A [**CIM\_Processor**](cim-processor.md) describing the processor that accesses the memory or uses the cache.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d1682-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="d1682-130">Remarks</span></span>

<span data-ttu-id="d1682-131">La classe **CIM \_ AssociatedProcessorMemory** è derivata da [**CIM \_ AssociatedMemory**](cim-associatedmemory.md).</span><span class="sxs-lookup"><span data-stu-id="d1682-131">The **CIM\_AssociatedProcessorMemory** class is derived from [**CIM\_AssociatedMemory**](cim-associatedmemory.md).</span></span>

<span data-ttu-id="d1682-132">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="d1682-132">WMI does not implement this class.</span></span> <span data-ttu-id="d1682-133">Per ulteriori informazioni sulle classi derivate da **CIM \_ AssociatedProcessorMemory**, vedere [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="d1682-133">For more information about classes derived from **CIM\_AssociatedProcessorMemory**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="d1682-134">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="d1682-134">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="d1682-135">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="d1682-135">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1682-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d1682-136">Requirements</span></span>



| <span data-ttu-id="d1682-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1682-137">Requirement</span></span> | <span data-ttu-id="d1682-138">Valore</span><span class="sxs-lookup"><span data-stu-id="d1682-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d1682-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d1682-139">Minimum supported client</span></span><br/> | <span data-ttu-id="d1682-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d1682-140">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d1682-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d1682-141">Minimum supported server</span></span><br/> | <span data-ttu-id="d1682-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d1682-142">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d1682-143">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d1682-143">Namespace</span></span><br/>                | <span data-ttu-id="d1682-144">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="d1682-144">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d1682-145">MOF</span><span class="sxs-lookup"><span data-stu-id="d1682-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d1682-146"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d1682-146"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d1682-147">DLL</span><span class="sxs-lookup"><span data-stu-id="d1682-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1682-148"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1682-148"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1682-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d1682-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1682-150">**\_ASSOCIATEDMEMORY CIM**</span><span class="sxs-lookup"><span data-stu-id="d1682-150">**CIM\_AssociatedMemory**</span></span>](cim-associatedmemory.md)
</dt> </dl>

 

