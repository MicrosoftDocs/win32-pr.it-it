---
description: Classe di associazione Common Information Model (CIM) che stabilisce le relazioni tra un sistema e gli elementi del sistema gestito di cui è composto.
ms.assetid: 11ad6dc1-a09a-4bab-bb1d-2131a8fdb812
ms.tgt_platform: multiple
title: Classe CIM_SystemComponent (provider WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SystemComponent
- CIM_SystemComponent.PartComponent
- CIM_SystemComponent.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9d9aae4e4ef916916f54bddea814844f23ed7315
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127102"
---
# <a name="cim_systemcomponent-class-cimwin32-wmi-providers"></a><span data-ttu-id="4de07-103">Classe CIM_SystemComponent (provider WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="4de07-103">CIM_SystemComponent class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="4de07-104">La classe **CIM \_ SystemComponent** è una classe di associazione Common Information Model (CIM) che stabilisce le relazioni tra un sistema e gli elementi del sistema gestito di cui è composto.</span><span class="sxs-lookup"><span data-stu-id="4de07-104">The **CIM\_SystemComponent** class is a Common Information Model (CIM) association class that establishes relationships between a system and the managed system elements of which it is composed.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4de07-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="4de07-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="4de07-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="4de07-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="4de07-107">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="4de07-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="4de07-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="4de07-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4de07-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4de07-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{527BC6CE-BAFE-11d2-85E5-0000F8102E5F}"), AMENDMENT]
class CIM_SystemComponent : CIM_Component
{
  CIM_ManagedSystemElement REF PartComponent;
  CIM_System               REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="4de07-110">Members</span><span class="sxs-lookup"><span data-stu-id="4de07-110">Members</span></span>

<span data-ttu-id="4de07-111">La classe **CIM \_ SystemComponent** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="4de07-111">The **CIM\_SystemComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="4de07-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4de07-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4de07-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4de07-113">Properties</span></span>

<span data-ttu-id="4de07-114">La classe **CIM \_ SystemComponent** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="4de07-114">The **CIM\_SystemComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4de07-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="4de07-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4de07-116">Tipo di dati **: \_ sistema CIM**</span><span class="sxs-lookup"><span data-stu-id="4de07-116">Data type: **CIM\_System**</span></span>
</dt> <dt>

<span data-ttu-id="4de07-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4de07-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4de07-118">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="4de07-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="4de07-119">[**\_ Sistema CIM**](cim-system.md) che descrive il sistema padre nell'associazione.</span><span class="sxs-lookup"><span data-stu-id="4de07-119">A [**CIM\_System**](cim-system.md) that describes the parent system in the association.</span></span>

</dd> <dt>

<span data-ttu-id="4de07-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="4de07-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4de07-121">Tipo di dati: **CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="4de07-121">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="4de07-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4de07-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4de07-123">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="4de07-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="4de07-124">[**\_ ManagedSystemElement CIM**](cim-managedsystemelement.md) che descrive l'elemento figlio che è un componente di un sistema.</span><span class="sxs-lookup"><span data-stu-id="4de07-124">A [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) that describes the child element that is a component of a system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4de07-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="4de07-125">Remarks</span></span>

<span data-ttu-id="4de07-126">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="4de07-126">WMI does not implement this class.</span></span> <span data-ttu-id="4de07-127">Per le classi WMI derivate da **CIM \_ SystemComponent**, vedere [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="4de07-127">For WMI classes derived from **CIM\_SystemComponent**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="4de07-128">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="4de07-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="4de07-129">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="4de07-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="4de07-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4de07-130">Requirements</span></span>



| <span data-ttu-id="4de07-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="4de07-131">Requirement</span></span> | <span data-ttu-id="4de07-132">Valore</span><span class="sxs-lookup"><span data-stu-id="4de07-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4de07-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4de07-133">Minimum supported client</span></span><br/> | <span data-ttu-id="4de07-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4de07-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4de07-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4de07-135">Minimum supported server</span></span><br/> | <span data-ttu-id="4de07-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4de07-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4de07-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4de07-137">Namespace</span></span><br/>                | <span data-ttu-id="4de07-138">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="4de07-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4de07-139">MOF</span><span class="sxs-lookup"><span data-stu-id="4de07-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4de07-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4de07-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4de07-141">DLL</span><span class="sxs-lookup"><span data-stu-id="4de07-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4de07-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4de07-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4de07-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4de07-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4de07-144">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="4de07-144">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

