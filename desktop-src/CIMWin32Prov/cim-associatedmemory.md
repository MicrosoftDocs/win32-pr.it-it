---
description: La \_ classe CIM AssociateMemory associa la memoria installata o associata, ad esempio la memoria della cache con un dispositivo logico.
ms.assetid: b108d0cc-9353-4940-a5f6-34bb93330a62
ms.tgt_platform: multiple
title: Classe CIM_AssociatedMemory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AssociatedMemory
- CIM_AssociatedMemory.Dependent
- CIM_AssociatedMemory.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3cb1443f54ab273ef6c114b8645e5322c24785f8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483637"
---
# <a name="cim_associatedmemory-class"></a><span data-ttu-id="76d9e-103">CIM \_ AssociatedMemory (classe)</span><span class="sxs-lookup"><span data-stu-id="76d9e-103">CIM\_AssociatedMemory class</span></span>

<span data-ttu-id="76d9e-104">La classe **CIM \_ AssociateMemory** associa la memoria installata o associata, ad esempio la memoria della cache con un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="76d9e-104">The **CIM\_AssociateMemory** class associates installed or associated memory, such as cache memory with a logical device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="76d9e-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="76d9e-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="76d9e-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="76d9e-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="76d9e-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="76d9e-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="76d9e-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="76d9e-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="76d9e-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="76d9e-109">Syntax</span></span>

``` syntax
[abstract, UUID("{464FFAB0-946F-11d2-AAE2-006008C78BC7}"), AMENDMENT]
class CIM_AssociatedMemory : CIM_Dependency
{
  CIM_LogicalDevice REF Dependent;
  CIM_Memory        REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="76d9e-110">Members</span><span class="sxs-lookup"><span data-stu-id="76d9e-110">Members</span></span>

<span data-ttu-id="76d9e-111">La classe **CIM \_ AssociatedMemory** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="76d9e-111">The **CIM\_AssociatedMemory** class has these types of members:</span></span>

-   [<span data-ttu-id="76d9e-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="76d9e-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="76d9e-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="76d9e-113">Properties</span></span>

<span data-ttu-id="76d9e-114">La classe **CIM \_ AssociatedMemory** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="76d9e-114">The **CIM\_AssociatedMemory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="76d9e-115">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="76d9e-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76d9e-116">Tipo di dati **: \_ memoria CIM**</span><span class="sxs-lookup"><span data-stu-id="76d9e-116">Data type: **CIM\_Memory**</span></span>
</dt> <dt>

<span data-ttu-id="76d9e-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="76d9e-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76d9e-118">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="76d9e-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="76d9e-119">[**\_ Memoria CIM**](cim-memory.md) che descrive la memoria installata in o associata a un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="76d9e-119">A [**CIM\_Memory**](cim-memory.md) that describes the memory installed on or associated with a device.</span></span>

</dd> <dt>

<span data-ttu-id="76d9e-120">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="76d9e-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="76d9e-121">Tipo di dati: **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="76d9e-121">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="76d9e-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="76d9e-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="76d9e-123">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="76d9e-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="76d9e-124">Un [**\_ LogicalDevice CIM**](cim-logicaldevice.md) che descrive il dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="76d9e-124">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the logical device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="76d9e-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="76d9e-125">Remarks</span></span>

<span data-ttu-id="76d9e-126">La classe **CIM \_ AssociatedMemory** è derivata dalla [**\_ dipendenza CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="76d9e-126">The **CIM\_AssociatedMemory** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="76d9e-127">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="76d9e-127">WMI does not implement this class.</span></span>

<span data-ttu-id="76d9e-128">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="76d9e-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="76d9e-129">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="76d9e-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="76d9e-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="76d9e-130">Requirements</span></span>



| <span data-ttu-id="76d9e-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="76d9e-131">Requirement</span></span> | <span data-ttu-id="76d9e-132">Valore</span><span class="sxs-lookup"><span data-stu-id="76d9e-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="76d9e-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="76d9e-133">Minimum supported client</span></span><br/> | <span data-ttu-id="76d9e-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="76d9e-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="76d9e-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="76d9e-135">Minimum supported server</span></span><br/> | <span data-ttu-id="76d9e-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="76d9e-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="76d9e-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="76d9e-137">Namespace</span></span><br/>                | <span data-ttu-id="76d9e-138">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="76d9e-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="76d9e-139">MOF</span><span class="sxs-lookup"><span data-stu-id="76d9e-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="76d9e-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="76d9e-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="76d9e-141">DLL</span><span class="sxs-lookup"><span data-stu-id="76d9e-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="76d9e-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="76d9e-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76d9e-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="76d9e-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76d9e-144">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="76d9e-144">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

