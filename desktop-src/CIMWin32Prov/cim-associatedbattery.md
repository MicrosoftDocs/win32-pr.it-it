---
description: La \_ dipendenza CIM AssociatedBattery associa una batteria a un dispositivo logico. Usare questa associazione per modellare singole batterie che costituiscono un gruppo di continuità (UPS, Power Supply).
ms.assetid: f8d8b3d3-edc5-438a-8be6-3ea4d765085b
ms.tgt_platform: multiple
title: Classe CIM_AssociatedBattery
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AssociatedBattery
- CIM_AssociatedBattery.Dependent
- CIM_AssociatedBattery.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 98c6394df79e53698ab6394f8572768f3728c503
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225727"
---
# <a name="cim_associatedbattery-class"></a><span data-ttu-id="9cc4e-104">CIM \_ AssociatedBattery (classe)</span><span class="sxs-lookup"><span data-stu-id="9cc4e-104">CIM\_AssociatedBattery class</span></span>

<span data-ttu-id="9cc4e-105">La dipendenza **CIM \_ AssociatedBattery** associa una batteria a un dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="9cc4e-105">The **CIM\_AssociatedBattery** dependency associates a battery with a logical device.</span></span> <span data-ttu-id="9cc4e-106">Usare questa associazione per modellare singole batterie che costituiscono un gruppo di continuità (UPS, Power Supply).</span><span class="sxs-lookup"><span data-stu-id="9cc4e-106">Use this association to model individual batteries that make up an uninterruptible power supply (UPS).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9cc4e-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="9cc4e-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="9cc4e-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="9cc4e-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="9cc4e-109">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="9cc4e-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="9cc4e-110">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="9cc4e-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9cc4e-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9cc4e-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C578-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_AssociatedBattery : CIM_Dependency
{
  CIM_LogicalDevice REF Dependent;
  CIM_Battery       REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="9cc4e-112">Members</span><span class="sxs-lookup"><span data-stu-id="9cc4e-112">Members</span></span>

<span data-ttu-id="9cc4e-113">La classe **CIM \_ AssociatedBattery** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="9cc4e-113">The **CIM\_AssociatedBattery** class has these types of members:</span></span>

-   [<span data-ttu-id="9cc4e-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9cc4e-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9cc4e-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9cc4e-115">Properties</span></span>

<span data-ttu-id="9cc4e-116">La classe **CIM \_ AssociatedBattery** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="9cc4e-116">The **CIM\_AssociatedBattery** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9cc4e-117">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="9cc4e-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cc4e-118">Tipo di dati **: \_ batteria CIM**</span><span class="sxs-lookup"><span data-stu-id="9cc4e-118">Data type: **CIM\_Battery**</span></span>
</dt> <dt>

<span data-ttu-id="9cc4e-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9cc4e-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9cc4e-120">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="9cc4e-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="9cc4e-121">[**\_ Batteria CIM**](cim-battery.md) che descrive la batteria.</span><span class="sxs-lookup"><span data-stu-id="9cc4e-121">A [**CIM\_Battery**](cim-battery.md) that describes the battery.</span></span>

</dd> <dt>

<span data-ttu-id="9cc4e-122">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="9cc4e-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cc4e-123">Tipo di dati: **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="9cc4e-123">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="9cc4e-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9cc4e-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9cc4e-125">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="9cc4e-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="9cc4e-126">Un [**\_ LogicalDevice CIM**](cim-logicaldevice.md) che contiene il dispositivo logico che necessita o è associato alla batteria.</span><span class="sxs-lookup"><span data-stu-id="9cc4e-126">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that contains the logical device needing or associated with the battery.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9cc4e-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="9cc4e-127">Remarks</span></span>

<span data-ttu-id="9cc4e-128">La classe **CIM \_ AssociatedBattery** è derivata dalla [**\_ dipendenza CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="9cc4e-128">The **CIM\_AssociatedBattery** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="9cc4e-129">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="9cc4e-129">WMI does not implement this class.</span></span> <span data-ttu-id="9cc4e-130">Per ulteriori informazioni sulle classi derivate da **CIM \_ AssociatedBattery**, vedere [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="9cc4e-130">For more information about classes derived from **CIM\_AssociatedBattery**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="9cc4e-131">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="9cc4e-131">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="9cc4e-132">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="9cc4e-132">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9cc4e-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9cc4e-133">Requirements</span></span>



| <span data-ttu-id="9cc4e-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="9cc4e-134">Requirement</span></span> | <span data-ttu-id="9cc4e-135">Valore</span><span class="sxs-lookup"><span data-stu-id="9cc4e-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9cc4e-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9cc4e-136">Minimum supported client</span></span><br/> | <span data-ttu-id="9cc4e-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9cc4e-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9cc4e-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9cc4e-138">Minimum supported server</span></span><br/> | <span data-ttu-id="9cc4e-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9cc4e-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9cc4e-140">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9cc4e-140">Namespace</span></span><br/>                | <span data-ttu-id="9cc4e-141">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="9cc4e-141">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9cc4e-142">MOF</span><span class="sxs-lookup"><span data-stu-id="9cc4e-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9cc4e-143"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9cc4e-143"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9cc4e-144">DLL</span><span class="sxs-lookup"><span data-stu-id="9cc4e-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9cc4e-145"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9cc4e-145"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9cc4e-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9cc4e-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cc4e-147">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="9cc4e-147">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

