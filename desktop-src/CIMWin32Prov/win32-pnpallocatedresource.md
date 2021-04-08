---
description: La \_ classe WMI dell'associazione PnPAllocatedResource Win32 rappresenta un'associazione tra dispositivi logici e risorse di sistema.
ms.assetid: e3cef457-cf88-4df5-8db8-b0495f636904
ms.tgt_platform: multiple
title: Classe Win32_PnPAllocatedResource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PnPAllocatedResource
- Win32_PnPAllocatedResource.Antecedent
- Win32_PnPAllocatedResource.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 353009016c8d4d54cdc92fb8f0ed062567dded6f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878354"
---
# <a name="win32_pnpallocatedresource-class"></a><span data-ttu-id="fad0e-103">Win32 \_ PnPAllocatedResource (classe)</span><span class="sxs-lookup"><span data-stu-id="fad0e-103">Win32\_PnPAllocatedResource class</span></span>

<span data-ttu-id="fad0e-104">La [classe WMI](../wmisdk/retrieving-a-class.md) dell'associazione **\_ PnPAllocatedResource Win32** rappresenta un'associazione tra dispositivi logici e risorse di sistema.</span><span class="sxs-lookup"><span data-stu-id="fad0e-104">The **Win32\_PnPAllocatedResource** association [WMI class](../wmisdk/retrieving-a-class.md) represents an association between logical devices and system resources.</span></span> <span data-ttu-id="fad0e-105">Questa classe viene usata per individuare le risorse in uso da un dispositivo specifico, ad esempio una richiesta di interrupt (IRQ) o un canale di accesso diretto alla memoria (DMA).</span><span class="sxs-lookup"><span data-stu-id="fad0e-105">This class is used to discover the resources that are in-use by a specific device, such as an Interrupt ReQuest (IRQ) or a Direct Memory Access (DMA) channel.</span></span>

<span data-ttu-id="fad0e-106">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="fad0e-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="fad0e-107">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="fad0e-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="fad0e-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fad0e-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("970C0998-41FE-4275-B7D9-7DABAD3FBC4D"), AMENDMENT]
class Win32_PnPAllocatedResource : CIM_AllocatedResource
{
  CIM_SystemResource REF Antecedent;
  Win32_PnPEntity    REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="fad0e-109">Members</span><span class="sxs-lookup"><span data-stu-id="fad0e-109">Members</span></span>

<span data-ttu-id="fad0e-110">La classe **Win32 \_ PnPAllocatedResource** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="fad0e-110">The **Win32\_PnPAllocatedResource** class has these types of members:</span></span>

-   [<span data-ttu-id="fad0e-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="fad0e-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fad0e-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="fad0e-112">Properties</span></span>

<span data-ttu-id="fad0e-113">La classe **Win32 \_ PnPAllocatedResource** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="fad0e-113">The **Win32\_PnPAllocatedResource** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fad0e-114">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="fad0e-114">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fad0e-115">Tipo di dati: **CIM \_ SystemResource**</span><span class="sxs-lookup"><span data-stu-id="fad0e-115">Data type: **CIM\_SystemResource**</span></span>
</dt> <dt>

<span data-ttu-id="fad0e-116">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fad0e-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fad0e-117">Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("antecedente"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| CIM \_ CIM SystemResource")</span><span class="sxs-lookup"><span data-stu-id="fad0e-117">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_SystemResource")</span></span>
</dt> </dl>

<span data-ttu-id="fad0e-118">Riferimento all'istanza [**CIM \_ SystemResource**](cim-systemresource.md) che rappresenta le proprietà di una risorsa di sistema disponibile per il dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="fad0e-118">Reference to the [**CIM\_SystemResource**](cim-systemresource.md) instance that represents the properties of a system resource available to the logical device.</span></span> <span data-ttu-id="fad0e-119">Questa proprietà viene ereditata [**dalla \_ dipendenza CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="fad0e-119">This property is inherited from [**CIM\_Dependency**](cim-dependency.md).</span></span>

</dd> <dt>

<span data-ttu-id="fad0e-120">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="fad0e-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fad0e-121">Tipo di dati: **Win32 \_ PnPEntity**</span><span class="sxs-lookup"><span data-stu-id="fad0e-121">Data type: **Win32\_PnPEntity**</span></span>
</dt> <dt>

<span data-ttu-id="fad0e-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fad0e-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fad0e-123">Qualificatori: [**chiave**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("dipendente"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ LogicalDevice")</span><span class="sxs-lookup"><span data-stu-id="fad0e-123">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Dependent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="fad0e-124">Riferimento all'istanza [**Win32 \_ PnPEntity**](win32-pnpentity.md) che rappresenta le proprietà del dispositivo logico utilizzando le risorse di sistema assegnate.</span><span class="sxs-lookup"><span data-stu-id="fad0e-124">Reference to the [**Win32\_PnPEntity**](win32-pnpentity.md) instance that represents the properties of the logical device using the system resources assigned to it.</span></span> <span data-ttu-id="fad0e-125">Questa proprietà viene ereditata [**dalla \_ dipendenza CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="fad0e-125">This property is inherited from [**CIM\_Dependency**](cim-dependency.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fad0e-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="fad0e-126">Remarks</span></span>

<span data-ttu-id="fad0e-127">La classe **Win32 \_ PnPAllocatedResource** è derivata da [**CIM \_ AllocatedResource**](cim-allocatedresource.md).</span><span class="sxs-lookup"><span data-stu-id="fad0e-127">The **Win32\_PnPAllocatedResource** class is derived from [**CIM\_AllocatedResource**](cim-allocatedresource.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fad0e-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fad0e-128">Requirements</span></span>



| <span data-ttu-id="fad0e-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="fad0e-129">Requirement</span></span> | <span data-ttu-id="fad0e-130">Valore</span><span class="sxs-lookup"><span data-stu-id="fad0e-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fad0e-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fad0e-131">Minimum supported client</span></span><br/> | <span data-ttu-id="fad0e-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fad0e-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fad0e-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fad0e-133">Minimum supported server</span></span><br/> | <span data-ttu-id="fad0e-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fad0e-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fad0e-135">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="fad0e-135">Namespace</span></span><br/>                | <span data-ttu-id="fad0e-136">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="fad0e-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fad0e-137">MOF</span><span class="sxs-lookup"><span data-stu-id="fad0e-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fad0e-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fad0e-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fad0e-139">DLL</span><span class="sxs-lookup"><span data-stu-id="fad0e-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fad0e-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fad0e-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fad0e-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fad0e-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fad0e-142">**\_ALLOCATEDRESOURCE CIM**</span><span class="sxs-lookup"><span data-stu-id="fad0e-142">**CIM\_AllocatedResource**</span></span>](cim-allocatedresource.md)
</dt> <dt>

[<span data-ttu-id="fad0e-143">Classi hardware del sistema del computer</span><span class="sxs-lookup"><span data-stu-id="fad0e-143">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
