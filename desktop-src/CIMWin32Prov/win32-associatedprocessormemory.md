---
description: La \_ classe WMI dell'associazione AssociatedProcessorMemory Win32 mette in correlazione un processore e la relativa memoria cache.
ms.assetid: 23da2a9d-772e-4258-9489-07d47801b2d8
ms.tgt_platform: multiple
title: Classe Win32_AssociatedProcessorMemory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_AssociatedProcessorMemory
- Win32_AssociatedProcessorMemory.BusSpeed
- Win32_AssociatedProcessorMemory.Dependent
- Win32_AssociatedProcessorMemory.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3737dca869c539d1414c4399f35fb8f107697b70
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966298"
---
# <a name="win32_associatedprocessormemory-class"></a><span data-ttu-id="d2327-103">Win32 \_ AssociatedProcessorMemory (classe)</span><span class="sxs-lookup"><span data-stu-id="d2327-103">Win32\_AssociatedProcessorMemory class</span></span>

<span data-ttu-id="d2327-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) dell'associazione **\_ AssociatedProcessorMemory Win32** mette in correlazione un processore e la relativa memoria cache.</span><span class="sxs-lookup"><span data-stu-id="d2327-104">The **Win32\_AssociatedProcessorMemory** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a processor and its cache memory.</span></span>

<span data-ttu-id="d2327-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="d2327-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="d2327-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="d2327-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2327-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d2327-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{074737F0-ACBC-11d2-ABF6-00805F538618}"), AMENDMENT]
class Win32_AssociatedProcessorMemory : CIM_AssociatedProcessorMemory
{
  uint32                BusSpeed;
  Win32_Processor   REF Dependent;
  Win32_CacheMemory REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="d2327-108">Members</span><span class="sxs-lookup"><span data-stu-id="d2327-108">Members</span></span>

<span data-ttu-id="d2327-109">La classe **Win32 \_ AssociatedProcessorMemory** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="d2327-109">The **Win32\_AssociatedProcessorMemory** class has these types of members:</span></span>

-   [<span data-ttu-id="d2327-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d2327-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d2327-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d2327-111">Properties</span></span>

<span data-ttu-id="d2327-112">La classe **Win32 \_ AssociatedProcessorMemory** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="d2327-112">The **Win32\_AssociatedProcessorMemory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d2327-113">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="d2327-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2327-114">Tipo di dati: **Win32 \_ CacheMemory**</span><span class="sxs-lookup"><span data-stu-id="d2327-114">Data type: **Win32\_CacheMemory**</span></span>
</dt> <dt>

<span data-ttu-id="d2327-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d2327-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2327-116">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| WMI \_ Win32 CacheMemory")</span><span class="sxs-lookup"><span data-stu-id="d2327-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_CacheMemory")</span></span>
</dt> </dl>

<span data-ttu-id="d2327-117">[**\_ CacheMemory Win32**](win32-cachememory.md) che descrive la memoria cache disponibile per il processore.</span><span class="sxs-lookup"><span data-stu-id="d2327-117">A [**Win32\_CacheMemory**](win32-cachememory.md) that describes the cache memory available to the processor.</span></span>

</dd> <dt>

<span data-ttu-id="d2327-118">**BusSpeed**</span><span class="sxs-lookup"><span data-stu-id="d2327-118">**BusSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2327-119">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d2327-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d2327-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d2327-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2327-121">Qualificatori: [**unità**](/windows/desktop/WmiSdk/standard-qualifiers) ("megahertz")</span><span class="sxs-lookup"><span data-stu-id="d2327-121">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("megahertz")</span></span>
</dt> </dl>

<span data-ttu-id="d2327-122">Velocità del bus, in megahertz (MHz), tra il processore e la memoria.</span><span class="sxs-lookup"><span data-stu-id="d2327-122">Speed of the bus, in megahertz (MHz), between the processor and memory.</span></span>

<span data-ttu-id="d2327-123">Questa proprietà viene ereditata da [**CIM \_ AssociatedProcessorMemory**](cim-associatedprocessormemory.md).</span><span class="sxs-lookup"><span data-stu-id="d2327-123">This property is inherited from [**CIM\_AssociatedProcessorMemory**](cim-associatedprocessormemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="d2327-124">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="d2327-124">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2327-125">Tipo di dati **: \_ processore Win32**</span><span class="sxs-lookup"><span data-stu-id="d2327-125">Data type: **Win32\_Processor**</span></span>
</dt> <dt>

<span data-ttu-id="d2327-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="d2327-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2327-127">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| processore Win32 WMI \_ ")</span><span class="sxs-lookup"><span data-stu-id="d2327-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_Processor")</span></span>
</dt> </dl>

<span data-ttu-id="d2327-128">[**\_ Processore Win32**](win32-processor.md) che descrive il processore che utilizza la memoria cache.</span><span class="sxs-lookup"><span data-stu-id="d2327-128">A [**Win32\_Processor**](win32-processor.md) that describes the processor that is using the cache memory.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d2327-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="d2327-129">Remarks</span></span>

<span data-ttu-id="d2327-130">La classe **Win32 \_ AssociatedProcessorMemory** è derivata da [**CIM \_ AssociatedProcessorMemory**](cim-associatedprocessormemory.md).</span><span class="sxs-lookup"><span data-stu-id="d2327-130">The **Win32\_AssociatedProcessorMemory** class is derived from [**CIM\_AssociatedProcessorMemory**](cim-associatedprocessormemory.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d2327-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d2327-131">Requirements</span></span>



| <span data-ttu-id="d2327-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2327-132">Requirement</span></span> | <span data-ttu-id="d2327-133">Valore</span><span class="sxs-lookup"><span data-stu-id="d2327-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d2327-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d2327-134">Minimum supported client</span></span><br/> | <span data-ttu-id="d2327-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d2327-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d2327-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d2327-136">Minimum supported server</span></span><br/> | <span data-ttu-id="d2327-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d2327-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d2327-138">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d2327-138">Namespace</span></span><br/>                | <span data-ttu-id="d2327-139">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="d2327-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d2327-140">MOF</span><span class="sxs-lookup"><span data-stu-id="d2327-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d2327-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d2327-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d2327-142">DLL</span><span class="sxs-lookup"><span data-stu-id="d2327-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d2327-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d2327-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2327-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d2327-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2327-145">**\_ASSOCIATEDPROCESSORMEMORY CIM**</span><span class="sxs-lookup"><span data-stu-id="d2327-145">**CIM\_AssociatedProcessorMemory**</span></span>](cim-associatedprocessormemory.md)
</dt> <dt>

[<span data-ttu-id="d2327-146">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="d2327-146">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

