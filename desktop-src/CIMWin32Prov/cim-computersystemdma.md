---
description: La \_ classe CIM ComputerSystemDMA rappresenta un'associazione tra un sistema di computer e i canali di accesso diretto alla memoria (DMA) disponibili.
ms.assetid: 7d5bce4b-973f-4452-b403-a2196bd4017a
ms.tgt_platform: multiple
title: Classe CIM_ComputerSystemDMA
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ComputerSystemDMA
- CIM_ComputerSystemDMA.PartComponent
- CIM_ComputerSystemDMA.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 23748a3b10c11878069a81cd82f7f69d0ab75792
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304977"
---
# <a name="cim_computersystemdma-class"></a><span data-ttu-id="e9f1e-103">CIM \_ ComputerSystemDMA (classe)</span><span class="sxs-lookup"><span data-stu-id="e9f1e-103">CIM\_ComputerSystemDMA class</span></span>

<span data-ttu-id="e9f1e-104">La classe **CIM \_ ComputerSystemDMA** rappresenta un'associazione tra un sistema di computer e i canali di accesso diretto alla memoria (DMA) disponibili.</span><span class="sxs-lookup"><span data-stu-id="e9f1e-104">The **CIM\_ComputerSystemDMA** class represents an association between a computer system and its available direct memory access (DMA) channels.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e9f1e-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="e9f1e-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e9f1e-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="e9f1e-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e9f1e-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="e9f1e-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="e9f1e-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="e9f1e-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9f1e-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e9f1e-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{9B81340B-E3D3-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_ComputerSystemDMA : CIM_ComputerSystemResource
{
  CIM_DMA            REF PartComponent;
  CIM_ComputerSystem REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="e9f1e-110">Members</span><span class="sxs-lookup"><span data-stu-id="e9f1e-110">Members</span></span>

<span data-ttu-id="e9f1e-111">La classe **CIM \_ ComputerSystemDMA** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e9f1e-111">The **CIM\_ComputerSystemDMA** class has these types of members:</span></span>

-   [<span data-ttu-id="e9f1e-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e9f1e-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e9f1e-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e9f1e-113">Properties</span></span>

<span data-ttu-id="e9f1e-114">La classe **CIM \_ ComputerSystemDMA** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="e9f1e-114">The **CIM\_ComputerSystemDMA** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e9f1e-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="e9f1e-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9f1e-116">Tipo di dati: **CIM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="e9f1e-116">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="e9f1e-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9f1e-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9f1e-118">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="e9f1e-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="e9f1e-119">Un [**\_ ComputerSystem CIM**](cim-computersystem.md) che descrive il computer associato al DMA.</span><span class="sxs-lookup"><span data-stu-id="e9f1e-119">A [**CIM\_ComputerSystem**](cim-computersystem.md) that describes the computer associated with the DMA.</span></span>

</dd> <dt>

<span data-ttu-id="e9f1e-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="e9f1e-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9f1e-121">Tipo di dati: **CIM \_ DMA**</span><span class="sxs-lookup"><span data-stu-id="e9f1e-121">Data type: **CIM\_DMA**</span></span>
</dt> <dt>

<span data-ttu-id="e9f1e-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e9f1e-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9f1e-123">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**debole**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e9f1e-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e9f1e-124">Un [**\_ DMA CIM**](cim-dma.md) che descrive un canale DMA del sistema del computer.</span><span class="sxs-lookup"><span data-stu-id="e9f1e-124">A [**CIM\_DMA**](cim-dma.md) that describes a DMA channel of the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e9f1e-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="e9f1e-125">Remarks</span></span>

<span data-ttu-id="e9f1e-126">La classe **CIM \_ ComputerSystemDMA** è derivata da [**CIM \_ ComputerSystemResource**](cim-computersystemresource.md).</span><span class="sxs-lookup"><span data-stu-id="e9f1e-126">The **CIM\_ComputerSystemDMA** class is derived from [**CIM\_ComputerSystemResource**](cim-computersystemresource.md).</span></span>

<span data-ttu-id="e9f1e-127">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="e9f1e-127">WMI does not implement this class.</span></span>

<span data-ttu-id="e9f1e-128">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="e9f1e-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e9f1e-129">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="e9f1e-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9f1e-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e9f1e-130">Requirements</span></span>



| <span data-ttu-id="e9f1e-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9f1e-131">Requirement</span></span> | <span data-ttu-id="e9f1e-132">Valore</span><span class="sxs-lookup"><span data-stu-id="e9f1e-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e9f1e-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e9f1e-133">Minimum supported client</span></span><br/> | <span data-ttu-id="e9f1e-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e9f1e-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e9f1e-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e9f1e-135">Minimum supported server</span></span><br/> | <span data-ttu-id="e9f1e-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e9f1e-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e9f1e-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e9f1e-137">Namespace</span></span><br/>                | <span data-ttu-id="e9f1e-138">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="e9f1e-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e9f1e-139">MOF</span><span class="sxs-lookup"><span data-stu-id="e9f1e-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e9f1e-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e9f1e-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e9f1e-141">DLL</span><span class="sxs-lookup"><span data-stu-id="e9f1e-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9f1e-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9f1e-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9f1e-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e9f1e-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9f1e-144">**\_COMPUTERSYSTEMRESOURCE CIM**</span><span class="sxs-lookup"><span data-stu-id="e9f1e-144">**CIM\_ComputerSystemResource**</span></span>](cim-computersystemresource.md)
</dt> </dl>

 

