---
description: La \_ classe CIM ComputerSystemMappedIO rappresenta un'associazione tra un sistema di computer e le relative porte I/O mappate alla memoria disponibili.
ms.assetid: 5df9db36-67ad-4a94-a7db-150b58977af1
ms.tgt_platform: multiple
title: Classe CIM_ComputerSystemMappedIO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ComputerSystemMappedIO
- CIM_ComputerSystemMappedIO.GroupComponent
- CIM_ComputerSystemMappedIO.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ce7d00950038c7d94f97f9a6938b9190846f6ff0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127106"
---
# <a name="cim_computersystemmappedio-class"></a><span data-ttu-id="ce109-103">CIM \_ ComputerSystemMappedIO (classe)</span><span class="sxs-lookup"><span data-stu-id="ce109-103">CIM\_ComputerSystemMappedIO class</span></span>

<span data-ttu-id="ce109-104">La classe **CIM \_ ComputerSystemMappedIO** rappresenta un'associazione tra un sistema di computer e le relative porte I/O mappate alla memoria disponibili.</span><span class="sxs-lookup"><span data-stu-id="ce109-104">The **CIM\_ComputerSystemMappedIO** class represents an association between a computer system and its available memory-mapped I/O ports.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ce109-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="ce109-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ce109-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="ce109-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="ce109-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="ce109-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="ce109-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="ce109-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce109-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ce109-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{A2EFC897-E3D3-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_ComputerSystemMappedIO : CIM_ComputerSystemResource
{
  CIM_ComputerSystem REF GroupComponent;
  CIM_MemoryMappedIO REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="ce109-110">Members</span><span class="sxs-lookup"><span data-stu-id="ce109-110">Members</span></span>

<span data-ttu-id="ce109-111">La classe **CIM \_ ComputerSystemMappedIO** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ce109-111">The **CIM\_ComputerSystemMappedIO** class has these types of members:</span></span>

-   [<span data-ttu-id="ce109-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ce109-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ce109-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ce109-113">Properties</span></span>

<span data-ttu-id="ce109-114">La classe **CIM \_ ComputerSystemMappedIO** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="ce109-114">The **CIM\_ComputerSystemMappedIO** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ce109-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="ce109-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce109-116">Tipo di dati: **CIM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="ce109-116">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="ce109-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ce109-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce109-118">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (GroupComponent)</span><span class="sxs-lookup"><span data-stu-id="ce109-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) (GroupComponent)</span></span>
</dt> </dl>

<span data-ttu-id="ce109-119">Un [**\_ ComputerSystem CIM**](cim-computersystem.md) che descrive il sistema del computer mappato alla porta di i/O.</span><span class="sxs-lookup"><span data-stu-id="ce109-119">A [**CIM\_ComputerSystem**](cim-computersystem.md) that describes the computer system mapped to the I/O port.</span></span>

<span data-ttu-id="ce109-120">Questa proprietà viene ereditata da [ **CIM \_ ComputerSystemResource**](cim-computersystemresource.md)</span><span class="sxs-lookup"><span data-stu-id="ce109-120">This property is inherited from [**CIM\_ComputerSystemResource**](cim-computersystemresource.md)</span></span>

</dd> <dt>

<span data-ttu-id="ce109-121">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="ce109-121">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce109-122">Tipo di dati: **CIM \_ MemoryMappedIO**</span><span class="sxs-lookup"><span data-stu-id="ce109-122">Data type: **CIM\_MemoryMappedIO**</span></span>
</dt> <dt>

<span data-ttu-id="ce109-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ce109-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce109-124">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**debole**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="ce109-124">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="ce109-125">Un [**\_ MemoryMappedIO CIM**](cim-memorymappedio.md) che descrive una porta di i/O con mapping della memoria del sistema del computer.</span><span class="sxs-lookup"><span data-stu-id="ce109-125">A [**CIM\_MemoryMappedIO**](cim-memorymappedio.md) that describes a memory mapped I/O port of the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ce109-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="ce109-126">Remarks</span></span>

<span data-ttu-id="ce109-127">La classe **CIM \_ ComputerSystemMappedIO** è derivata da [**CIM \_ ComputerSystemResource**](cim-computersystemresource.md).</span><span class="sxs-lookup"><span data-stu-id="ce109-127">The **CIM\_ComputerSystemMappedIO** class is derived from [**CIM\_ComputerSystemResource**](cim-computersystemresource.md).</span></span>

<span data-ttu-id="ce109-128">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="ce109-128">WMI does not implement this class.</span></span>

<span data-ttu-id="ce109-129">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="ce109-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ce109-130">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="ce109-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce109-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ce109-131">Requirements</span></span>



| <span data-ttu-id="ce109-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce109-132">Requirement</span></span> | <span data-ttu-id="ce109-133">Valore</span><span class="sxs-lookup"><span data-stu-id="ce109-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ce109-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ce109-134">Minimum supported client</span></span><br/> | <span data-ttu-id="ce109-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ce109-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ce109-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ce109-136">Minimum supported server</span></span><br/> | <span data-ttu-id="ce109-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ce109-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ce109-138">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ce109-138">Namespace</span></span><br/>                | <span data-ttu-id="ce109-139">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="ce109-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ce109-140">MOF</span><span class="sxs-lookup"><span data-stu-id="ce109-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ce109-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ce109-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ce109-142">DLL</span><span class="sxs-lookup"><span data-stu-id="ce109-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ce109-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ce109-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce109-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ce109-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce109-145">**\_COMPUTERSYSTEMRESOURCE CIM**</span><span class="sxs-lookup"><span data-stu-id="ce109-145">**CIM\_ComputerSystemResource**</span></span>](cim-computersystemresource.md)
</dt> </dl>

 

