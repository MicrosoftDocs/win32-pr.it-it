---
description: La \_ classe CIM ComputerSystemIRQ rappresenta un'associazione tra un sistema di computer e le relative righe di richiesta di interrupt (IRQ) disponibili.
ms.assetid: c2a1f231-1f8e-48b2-9afe-fa798e6a8a1d
ms.tgt_platform: multiple
title: Classe CIM_ComputerSystemIRQ
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ComputerSystemIRQ
- CIM_ComputerSystemIRQ.GroupComponent
- CIM_ComputerSystemIRQ.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 490b1f26e8d100f675a6e57a8ddf7a53770d4ea1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304976"
---
# <a name="cim_computersystemirq-class"></a><span data-ttu-id="cdcdf-103">CIM \_ ComputerSystemIRQ (classe)</span><span class="sxs-lookup"><span data-stu-id="cdcdf-103">CIM\_ComputerSystemIRQ class</span></span>

<span data-ttu-id="cdcdf-104">La classe **CIM \_ ComputerSystemIRQ** rappresenta un'associazione tra un sistema di computer e le relative righe di richiesta di interrupt (IRQ) disponibili.</span><span class="sxs-lookup"><span data-stu-id="cdcdf-104">The **CIM\_ComputerSystemIRQ** class represents an association between a computer system and its available interrupt request lines (IRQs).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cdcdf-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="cdcdf-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="cdcdf-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="cdcdf-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="cdcdf-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="cdcdf-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="cdcdf-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="cdcdf-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdcdf-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cdcdf-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{A2EFC896-E3D3-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_ComputerSystemIRQ : CIM_ComputerSystemResource
{
  CIM_ComputerSystem REF GroupComponent;
  CIM_IRQ            REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="cdcdf-110">Members</span><span class="sxs-lookup"><span data-stu-id="cdcdf-110">Members</span></span>

<span data-ttu-id="cdcdf-111">La classe **CIM \_ ComputerSystemIRQ** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="cdcdf-111">The **CIM\_ComputerSystemIRQ** class has these types of members:</span></span>

-   [<span data-ttu-id="cdcdf-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="cdcdf-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cdcdf-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="cdcdf-113">Properties</span></span>

<span data-ttu-id="cdcdf-114">La classe **CIM \_ ComputerSystemIRQ** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="cdcdf-114">The **CIM\_ComputerSystemIRQ** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cdcdf-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="cdcdf-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdcdf-116">Tipo di dati: **CIM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="cdcdf-116">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="cdcdf-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cdcdf-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cdcdf-118">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (GroupComponent)</span><span class="sxs-lookup"><span data-stu-id="cdcdf-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) (GroupComponent)</span></span>
</dt> </dl>

<span data-ttu-id="cdcdf-119">Un [**\_ ComputerSystem CIM**](cim-computersystem.md) che descrive il computer associato all'IRQ.</span><span class="sxs-lookup"><span data-stu-id="cdcdf-119">A [**CIM\_ComputerSystem**](cim-computersystem.md) describing the computer associated with the IRQ.</span></span>

<span data-ttu-id="cdcdf-120">Questa proprietà viene ereditata da [ **CIM \_ ComputerSystemResource**](cim-computersystemresource.md)</span><span class="sxs-lookup"><span data-stu-id="cdcdf-120">This property is inherited from [**CIM\_ComputerSystemResource**](cim-computersystemresource.md)</span></span>

</dd> <dt>

<span data-ttu-id="cdcdf-121">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="cdcdf-121">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cdcdf-122">Tipo di dati **: \_ IRQ CIM**</span><span class="sxs-lookup"><span data-stu-id="cdcdf-122">Data type: **CIM\_IRQ**</span></span>
</dt> <dt>

<span data-ttu-id="cdcdf-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="cdcdf-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cdcdf-124">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**debole**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="cdcdf-124">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="cdcdf-125">Un [**\_ IRQ CIM**](cim-irq.md) che descrive un IRQ del sistema del computer.</span><span class="sxs-lookup"><span data-stu-id="cdcdf-125">A [**CIM\_IRQ**](cim-irq.md) describing an IRQ of the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cdcdf-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="cdcdf-126">Remarks</span></span>

<span data-ttu-id="cdcdf-127">La classe **CIM \_ ComputerSystemIRQ** è derivata da [**CIM \_ ComputerSystemResource**](cim-computersystemresource.md).</span><span class="sxs-lookup"><span data-stu-id="cdcdf-127">The **CIM\_ComputerSystemIRQ** class is derived from [**CIM\_ComputerSystemResource**](cim-computersystemresource.md).</span></span>

<span data-ttu-id="cdcdf-128">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="cdcdf-128">WMI does not implement this class.</span></span>

<span data-ttu-id="cdcdf-129">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="cdcdf-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="cdcdf-130">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="cdcdf-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="cdcdf-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cdcdf-131">Requirements</span></span>



| <span data-ttu-id="cdcdf-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="cdcdf-132">Requirement</span></span> | <span data-ttu-id="cdcdf-133">Valore</span><span class="sxs-lookup"><span data-stu-id="cdcdf-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cdcdf-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cdcdf-134">Minimum supported client</span></span><br/> | <span data-ttu-id="cdcdf-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cdcdf-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cdcdf-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cdcdf-136">Minimum supported server</span></span><br/> | <span data-ttu-id="cdcdf-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cdcdf-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cdcdf-138">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="cdcdf-138">Namespace</span></span><br/>                | <span data-ttu-id="cdcdf-139">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="cdcdf-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cdcdf-140">MOF</span><span class="sxs-lookup"><span data-stu-id="cdcdf-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cdcdf-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cdcdf-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cdcdf-142">DLL</span><span class="sxs-lookup"><span data-stu-id="cdcdf-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cdcdf-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cdcdf-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cdcdf-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cdcdf-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdcdf-145">**\_COMPUTERSYSTEMRESOURCE CIM**</span><span class="sxs-lookup"><span data-stu-id="cdcdf-145">**CIM\_ComputerSystemResource**</span></span>](cim-computersystemresource.md)
</dt> </dl>

 

