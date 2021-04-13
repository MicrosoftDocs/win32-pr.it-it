---
description: La \_ classe CIM MemoryWithMedia associa la memoria fisica a un supporto fisico e alla relativa cartuccia. La memoria fornisce l'identificazione dei supporti e archivia i dati specifici dell'utente.
ms.assetid: 99806d2d-6575-431d-9149-dc8ea767146c
ms.tgt_platform: multiple
title: Classe CIM_MemoryWithMedia
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MemoryWithMedia
- CIM_MemoryWithMedia.Dependent
- CIM_MemoryWithMedia.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3b990f8ba842f313449b6f24f4e2ce59787f7841
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351636"
---
# <a name="cim_memorywithmedia-class"></a><span data-ttu-id="323d7-104">CIM \_ MemoryWithMedia (classe)</span><span class="sxs-lookup"><span data-stu-id="323d7-104">CIM\_MemoryWithMedia class</span></span>

<span data-ttu-id="323d7-105">La classe **CIM \_ MemoryWithMedia** associa la memoria fisica a un supporto fisico e alla relativa cartuccia.</span><span class="sxs-lookup"><span data-stu-id="323d7-105">The **CIM\_MemoryWithMedia** class associates physical memory with a physical media and its cartridge.</span></span> <span data-ttu-id="323d7-106">La memoria fornisce l'identificazione dei supporti e archivia i dati specifici dell'utente.</span><span class="sxs-lookup"><span data-stu-id="323d7-106">The memory provides media identification and stores user-specific data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="323d7-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="323d7-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="323d7-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="323d7-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="323d7-109">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="323d7-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="323d7-110">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="323d7-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="323d7-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="323d7-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B7E-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_MemoryWithMedia : CIM_Dependency
{
  CIM_PhysicalMedia  REF Dependent;
  CIM_PhysicalMemory REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="323d7-112">Members</span><span class="sxs-lookup"><span data-stu-id="323d7-112">Members</span></span>

<span data-ttu-id="323d7-113">La classe **CIM \_ MemoryWithMedia** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="323d7-113">The **CIM\_MemoryWithMedia** class has these types of members:</span></span>

-   [<span data-ttu-id="323d7-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="323d7-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="323d7-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="323d7-115">Properties</span></span>

<span data-ttu-id="323d7-116">La classe **CIM \_ MemoryWithMedia** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="323d7-116">The **CIM\_MemoryWithMedia** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="323d7-117">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="323d7-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="323d7-118">Tipo di dati: **CIM \_ PhysicalMemory**</span><span class="sxs-lookup"><span data-stu-id="323d7-118">Data type: **CIM\_PhysicalMemory**</span></span>
</dt> <dt>

<span data-ttu-id="323d7-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="323d7-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="323d7-120">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="323d7-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="323d7-121">Un [**\_ PhysicalMemory CIM**](cim-physicalmemory.md) che descrive la memoria associata ai supporti fisici.</span><span class="sxs-lookup"><span data-stu-id="323d7-121">A [**CIM\_PhysicalMemory**](cim-physicalmemory.md) that describes the memory associated with physical media.</span></span>

</dd> <dt>

<span data-ttu-id="323d7-122">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="323d7-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="323d7-123">Tipo di dati: **CIM \_ PhysicalMedia**</span><span class="sxs-lookup"><span data-stu-id="323d7-123">Data type: **CIM\_PhysicalMedia**</span></span>
</dt> <dt>

<span data-ttu-id="323d7-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="323d7-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="323d7-125">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="323d7-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="323d7-126">Un [**\_ PhysicalMedia CIM**](cim-physicalmedia.md) che descrive i supporti fisici.</span><span class="sxs-lookup"><span data-stu-id="323d7-126">A [**CIM\_PhysicalMedia**](cim-physicalmedia.md) that describes the physical media.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="323d7-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="323d7-127">Remarks</span></span>

<span data-ttu-id="323d7-128">**CIM \_ MemoryWithMedia** viene ereditato dalla [**\_ dipendenza CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="323d7-128">**CIM\_MemoryWithMedia** is inherited from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="323d7-129">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="323d7-129">WMI does not implement this class.</span></span>

<span data-ttu-id="323d7-130">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="323d7-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="323d7-131">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="323d7-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="323d7-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="323d7-132">Requirements</span></span>



| <span data-ttu-id="323d7-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="323d7-133">Requirement</span></span> | <span data-ttu-id="323d7-134">Valore</span><span class="sxs-lookup"><span data-stu-id="323d7-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="323d7-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="323d7-135">Minimum supported client</span></span><br/> | <span data-ttu-id="323d7-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="323d7-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="323d7-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="323d7-137">Minimum supported server</span></span><br/> | <span data-ttu-id="323d7-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="323d7-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="323d7-139">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="323d7-139">Namespace</span></span><br/>                | <span data-ttu-id="323d7-140">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="323d7-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="323d7-141">MOF</span><span class="sxs-lookup"><span data-stu-id="323d7-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="323d7-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="323d7-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="323d7-143">DLL</span><span class="sxs-lookup"><span data-stu-id="323d7-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="323d7-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="323d7-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="323d7-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="323d7-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="323d7-146">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="323d7-146">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

