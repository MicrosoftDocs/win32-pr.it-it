---
description: La \_ classe CIM ComputerSystemResource rappresenta un'associazione tra un sistema di computer e le risorse di sistema disponibili.
ms.assetid: 365a3cc2-89f9-4fbd-aa70-a89608fc3c1f
ms.tgt_platform: multiple
title: Classe CIM_ComputerSystemResource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ComputerSystemResource
- CIM_ComputerSystemResource.PartComponent
- CIM_ComputerSystemResource.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 170e92b6c31ce038f1bccc4003248b8ae86d5f79
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049219"
---
# <a name="cim_computersystemresource-class"></a><span data-ttu-id="6c760-103">CIM \_ ComputerSystemResource (classe)</span><span class="sxs-lookup"><span data-stu-id="6c760-103">CIM\_ComputerSystemResource class</span></span>

<span data-ttu-id="6c760-104">La classe **CIM \_ ComputerSystemResource** rappresenta un'associazione tra un sistema di computer e le risorse di sistema disponibili.</span><span class="sxs-lookup"><span data-stu-id="6c760-104">The **CIM\_ComputerSystemResource** class represents an association between a computer system and its available system resources.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6c760-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="6c760-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="6c760-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="6c760-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="6c760-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="6c760-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="6c760-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="6c760-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c760-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6c760-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{9B81340A-E3D3-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_ComputerSystemResource : CIM_SystemComponent
{
  CIM_SystemResource REF PartComponent;
  CIM_ComputerSystem REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="6c760-110">Members</span><span class="sxs-lookup"><span data-stu-id="6c760-110">Members</span></span>

<span data-ttu-id="6c760-111">La classe **CIM \_ ComputerSystemResource** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="6c760-111">The **CIM\_ComputerSystemResource** class has these types of members:</span></span>

-   [<span data-ttu-id="6c760-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6c760-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6c760-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6c760-113">Properties</span></span>

<span data-ttu-id="6c760-114">La classe **CIM \_ ComputerSystemResource** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="6c760-114">The **CIM\_ComputerSystemResource** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6c760-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="6c760-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c760-116">Tipo di dati: **CIM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="6c760-116">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="6c760-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6c760-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c760-118">Qualificatori: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="6c760-118">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="6c760-119">Un [**\_ ComputerSystem CIM**](cim-computersystem.md) che descrive il computer.</span><span class="sxs-lookup"><span data-stu-id="6c760-119">A [**CIM\_ComputerSystem**](cim-computersystem.md) that describes the computer system.</span></span>

</dd> <dt>

<span data-ttu-id="6c760-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="6c760-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c760-121">Tipo di dati: **CIM \_ SystemResource**</span><span class="sxs-lookup"><span data-stu-id="6c760-121">Data type: **CIM\_SystemResource**</span></span>
</dt> <dt>

<span data-ttu-id="6c760-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="6c760-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c760-123">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="6c760-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="6c760-124">Un [**\_ SystemResource CIM**](cim-systemresource.md) che descrive una risorsa di sistema del computer.</span><span class="sxs-lookup"><span data-stu-id="6c760-124">A [**CIM\_SystemResource**](cim-systemresource.md) that describes a system resource of the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6c760-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="6c760-125">Remarks</span></span>

<span data-ttu-id="6c760-126">La classe **CIM \_ ComputerSystemResource** è derivata da [**CIM \_ SystemComponent**](cim-systemcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="6c760-126">The **CIM\_ComputerSystemResource** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).</span></span>

<span data-ttu-id="6c760-127">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="6c760-127">WMI does not implement this class.</span></span> <span data-ttu-id="6c760-128">Per ulteriori informazioni sulle classi derivate da **CIM \_ ComputerSystemResource**, vedere [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="6c760-128">For more information about classes derived from **CIM\_ComputerSystemResource**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="6c760-129">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="6c760-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="6c760-130">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="6c760-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c760-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6c760-131">Requirements</span></span>



| <span data-ttu-id="6c760-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c760-132">Requirement</span></span> | <span data-ttu-id="6c760-133">Valore</span><span class="sxs-lookup"><span data-stu-id="6c760-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c760-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6c760-134">Minimum supported client</span></span><br/> | <span data-ttu-id="6c760-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6c760-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6c760-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6c760-136">Minimum supported server</span></span><br/> | <span data-ttu-id="6c760-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6c760-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6c760-138">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="6c760-138">Namespace</span></span><br/>                | <span data-ttu-id="6c760-139">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="6c760-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6c760-140">MOF</span><span class="sxs-lookup"><span data-stu-id="6c760-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6c760-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6c760-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6c760-142">DLL</span><span class="sxs-lookup"><span data-stu-id="6c760-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c760-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c760-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c760-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6c760-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c760-145">**\_SYSTEMCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="6c760-145">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> </dl>

 

