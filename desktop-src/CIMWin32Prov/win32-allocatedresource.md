---
description: La \_ classe WMI dell'associazione AllocatedResource Win32 mette in correlazione un dispositivo logico a una risorsa di sistema. Questa classe viene usata per individuare le risorse, ad esempio IRQ o i canali DMA, usate da un dispositivo specifico.
ms.assetid: cfac1209-1405-4fee-847c-8a61504bfac1
ms.tgt_platform: multiple
title: Classe Win32_AllocatedResource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_AllocatedResource
- Win32_AllocatedResource.Dependent
- Win32_AllocatedResource.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 87a57e53a85e4433ae325fc2ed441211db75b79f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966299"
---
# <a name="win32_allocatedresource-class"></a><span data-ttu-id="ba975-104">Win32 \_ AllocatedResource (classe)</span><span class="sxs-lookup"><span data-stu-id="ba975-104">Win32\_AllocatedResource class</span></span>

<span data-ttu-id="ba975-105">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) dell'associazione **\_ AllocatedResource Win32** mette in correlazione un dispositivo logico a una risorsa di sistema.</span><span class="sxs-lookup"><span data-stu-id="ba975-105">The **Win32\_AllocatedResource** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a logical device to a system resource.</span></span> <span data-ttu-id="ba975-106">Questa classe viene usata per individuare le risorse, ad esempio IRQ o i canali DMA, usate da un dispositivo specifico.</span><span class="sxs-lookup"><span data-stu-id="ba975-106">This class is used to discover which resources, such as IRQs or DMA channels, are in use by a specific device.</span></span>

<span data-ttu-id="ba975-107">Questa classe è obsoleta.</span><span class="sxs-lookup"><span data-stu-id="ba975-107">This class is obsolete.</span></span> <span data-ttu-id="ba975-108">Al posto di questa classe, è necessario usare le proprietà nella classe [**Win32 \_ PNPAllocatedResource**](win32-pnpallocatedresource.md) .</span><span class="sxs-lookup"><span data-stu-id="ba975-108">In place of this class, you should use the properties in the [**Win32\_PNPAllocatedResource**](win32-pnpallocatedresource.md) class.</span></span>

<span data-ttu-id="ba975-109">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="ba975-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="ba975-110">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="ba975-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba975-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ba975-111">Syntax</span></span>

``` syntax
[DEPRECATED, Dynamic, Provider("CIMWin32"), UUID("{8502C50D-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_AllocatedResource : CIM_Dependency
{
  CIM_LogicalDevice  REF Dependent;
  CIM_SystemResource REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="ba975-112">Members</span><span class="sxs-lookup"><span data-stu-id="ba975-112">Members</span></span>

<span data-ttu-id="ba975-113">La classe **Win32 \_ AllocatedResource** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ba975-113">The **Win32\_AllocatedResource** class has these types of members:</span></span>

-   [<span data-ttu-id="ba975-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ba975-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ba975-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ba975-115">Properties</span></span>

<span data-ttu-id="ba975-116">La classe **Win32 \_ AllocatedResource** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="ba975-116">The **Win32\_AllocatedResource** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ba975-117">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="ba975-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba975-118">Tipo di dati: **CIM \_ SystemResource**</span><span class="sxs-lookup"><span data-stu-id="ba975-118">Data type: **CIM\_SystemResource**</span></span>
</dt> <dt>

<span data-ttu-id="ba975-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ba975-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba975-120">Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| CIM \_ CIM SystemResource")</span><span class="sxs-lookup"><span data-stu-id="ba975-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|CIM\_SystemResource")</span></span>
</dt> </dl>

<span data-ttu-id="ba975-121">Un [**\_ SystemResource CIM**](cim-systemresource.md) che descrive le proprietà di una risorsa di sistema disponibile per il dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="ba975-121">A [**CIM\_SystemResource**](cim-systemresource.md) that describes the properties of a system resource available to the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="ba975-122">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="ba975-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba975-123">Tipo di dati: **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="ba975-123">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="ba975-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ba975-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba975-125">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \| CIM \_ LogicalDevice")</span><span class="sxs-lookup"><span data-stu-id="ba975-125">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="ba975-126">Un [**\_ LogicalDevice CIM**](cim-logicaldevice.md) che rappresenta le proprietà del dispositivo logico che utilizza le risorse di sistema assegnate.</span><span class="sxs-lookup"><span data-stu-id="ba975-126">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that represents the properties of the logical device that is using the system resources assigned to it.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ba975-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="ba975-127">Remarks</span></span>

<span data-ttu-id="ba975-128">La classe **Win32 \_ AllocatedResource** è derivata dalla [**\_ dipendenza CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="ba975-128">The **Win32\_AllocatedResource** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ba975-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ba975-129">Requirements</span></span>



| <span data-ttu-id="ba975-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba975-130">Requirement</span></span> | <span data-ttu-id="ba975-131">Valore</span><span class="sxs-lookup"><span data-stu-id="ba975-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ba975-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ba975-132">Minimum supported client</span></span><br/> | <span data-ttu-id="ba975-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ba975-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ba975-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ba975-134">Minimum supported server</span></span><br/> | <span data-ttu-id="ba975-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ba975-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ba975-136">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ba975-136">Namespace</span></span><br/>                | <span data-ttu-id="ba975-137">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="ba975-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ba975-138">MOF</span><span class="sxs-lookup"><span data-stu-id="ba975-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ba975-139"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ba975-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ba975-140">DLL</span><span class="sxs-lookup"><span data-stu-id="ba975-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ba975-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba975-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba975-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ba975-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba975-143">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="ba975-143">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

[<span data-ttu-id="ba975-144">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="ba975-144">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

