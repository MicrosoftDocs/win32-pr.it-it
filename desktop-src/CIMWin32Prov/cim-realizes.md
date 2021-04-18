---
description: La \_ classe CIM realizza la classe che rappresenta l'associazione che definisce il mapping tra un dispositivo logico e il componente fisico che implementa il dispositivo.
ms.assetid: 3bddb0c8-dca5-4877-9e30-322516a8d388
ms.tgt_platform: multiple
title: Classe CIM_Realizes
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Realizes
- CIM_Realizes.Dependent
- CIM_Realizes.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b37b2f5f3fe9cfce78e16530df8b94e4333e9a33
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304776"
---
# <a name="cim_realizes-class"></a><span data-ttu-id="14cad-103">\_Classe CIM réalisateurs</span><span class="sxs-lookup"><span data-stu-id="14cad-103">CIM\_Realizes class</span></span>

<span data-ttu-id="14cad-104">La classe **CIM \_ realizza** la classe che rappresenta l'associazione che definisce il mapping tra un dispositivo logico e il componente fisico che implementa il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="14cad-104">The **CIM\_Realizes** class represents the association that defines the mapping between a logical device and the physical component that implements the device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="14cad-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="14cad-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="14cad-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="14cad-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="14cad-107">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="14cad-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="14cad-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="14cad-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="14cad-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="14cad-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B62-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Realizes : CIM_Dependency
{
  CIM_LogicalDevice   REF Dependent;
  CIM_PhysicalElement REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="14cad-110">Members</span><span class="sxs-lookup"><span data-stu-id="14cad-110">Members</span></span>

<span data-ttu-id="14cad-111">La classe **CIM \_ realizza** la classe con questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="14cad-111">The **CIM\_Realizes** class has these types of members:</span></span>

-   [<span data-ttu-id="14cad-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="14cad-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="14cad-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="14cad-113">Properties</span></span>

<span data-ttu-id="14cad-114">La classe **CIM \_ realizza** queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="14cad-114">The **CIM\_Realizes** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="14cad-115">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="14cad-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14cad-116">Tipo di dati **: \_ fisico CIM**</span><span class="sxs-lookup"><span data-stu-id="14cad-116">Data type: **CIM\_PhysicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="14cad-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="14cad-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14cad-118">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="14cad-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="14cad-119">Oggetto [**\_ fisico CIM**](cim-physicalelement.md) che descrive il componente fisico che implementa il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="14cad-119">A [**CIM\_PhysicalElement**](cim-physicalelement.md) that describes the physical component that implements the device.</span></span>

</dd> <dt>

<span data-ttu-id="14cad-120">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="14cad-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="14cad-121">Tipo di dati: **CIM \_ LogicalDevice**</span><span class="sxs-lookup"><span data-stu-id="14cad-121">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="14cad-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="14cad-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="14cad-123">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="14cad-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="14cad-124">Un [**\_ LogicalDevice CIM**](cim-logicaldevice.md) che descrive il dispositivo logico.</span><span class="sxs-lookup"><span data-stu-id="14cad-124">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the logical device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="14cad-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="14cad-125">Remarks</span></span>

<span data-ttu-id="14cad-126">La classe **CIM \_ realizzations** deriva dalla [**\_ dipendenza CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="14cad-126">The **CIM\_Realizes** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="14cad-127">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="14cad-127">WMI does not implement this class.</span></span>

<span data-ttu-id="14cad-128">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="14cad-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="14cad-129">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="14cad-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="14cad-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="14cad-130">Requirements</span></span>



| <span data-ttu-id="14cad-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="14cad-131">Requirement</span></span> | <span data-ttu-id="14cad-132">Valore</span><span class="sxs-lookup"><span data-stu-id="14cad-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="14cad-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="14cad-133">Minimum supported client</span></span><br/> | <span data-ttu-id="14cad-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="14cad-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="14cad-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="14cad-135">Minimum supported server</span></span><br/> | <span data-ttu-id="14cad-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="14cad-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="14cad-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="14cad-137">Namespace</span></span><br/>                | <span data-ttu-id="14cad-138">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="14cad-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="14cad-139">MOF</span><span class="sxs-lookup"><span data-stu-id="14cad-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="14cad-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="14cad-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="14cad-141">DLL</span><span class="sxs-lookup"><span data-stu-id="14cad-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="14cad-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14cad-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14cad-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="14cad-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14cad-144">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="14cad-144">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

