---
description: La \_ classe CIM ElementCapacity associa un \_ oggetto CIM PhysicalCapacity a uno o più elementi fisici. Associa una descrizione dei requisiti hardware (o funzionalità) minimi e massimi agli elementi fisici descritti.
ms.assetid: 368c31e8-d56b-4b90-ba3f-20d9b0de8730
ms.tgt_platform: multiple
title: Classe CIM_ElementCapacity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementCapacity
- CIM_ElementCapacity.Capacity
- CIM_ElementCapacity.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7c6ecac913f6d4affcd9784a30d85fa08dfe0486
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483373"
---
# <a name="cim_elementcapacity-class"></a><span data-ttu-id="a22e7-104">CIM \_ ElementCapacity (classe)</span><span class="sxs-lookup"><span data-stu-id="a22e7-104">CIM\_ElementCapacity class</span></span>

<span data-ttu-id="a22e7-105">La classe **CIM \_ ElementCapacity** associa un oggetto [**CIM \_ PhysicalCapacity**](cim-physicalcapacity.md) a uno o più elementi fisici.</span><span class="sxs-lookup"><span data-stu-id="a22e7-105">The **CIM\_ElementCapacity** class associates a [**CIM\_PhysicalCapacity**](cim-physicalcapacity.md) object with one or more physical elements.</span></span> <span data-ttu-id="a22e7-106">Associa una descrizione dei requisiti hardware (o funzionalità) minimi e massimi agli elementi fisici descritti.</span><span class="sxs-lookup"><span data-stu-id="a22e7-106">It associates a description of the minimum and maximum hardware requirements (or capabilities) to the physical elements being described.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a22e7-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="a22e7-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a22e7-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="a22e7-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a22e7-109">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="a22e7-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="a22e7-110">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="a22e7-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a22e7-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a22e7-111">Syntax</span></span>

``` syntax
[Abstract, Association, UUID("{FAF76B6A-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_ElementCapacity
{
  CIM_PhysicalCapacity REF Capacity;
  CIM_PhysicalElement  REF Element;
};
```

## <a name="members"></a><span data-ttu-id="a22e7-112">Members</span><span class="sxs-lookup"><span data-stu-id="a22e7-112">Members</span></span>

<span data-ttu-id="a22e7-113">La classe **CIM \_ ElementCapacity** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="a22e7-113">The **CIM\_ElementCapacity** class has these types of members:</span></span>

-   [<span data-ttu-id="a22e7-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a22e7-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a22e7-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="a22e7-115">Properties</span></span>

<span data-ttu-id="a22e7-116">La classe **CIM \_ ElementCapacity** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="a22e7-116">The **CIM\_ElementCapacity** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a22e7-117">**Capacity**</span><span class="sxs-lookup"><span data-stu-id="a22e7-117">**Capacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a22e7-118">Tipo di dati: **CIM \_ PhysicalCapacity**</span><span class="sxs-lookup"><span data-stu-id="a22e7-118">Data type: **CIM\_PhysicalCapacity**</span></span>
</dt> <dt>

<span data-ttu-id="a22e7-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a22e7-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a22e7-120">Riferimento alla classe [**CIM \_ PhysicalCapacity**](cim-physicalcapacity.md) che descrive i requisiti minimi e massimi e la possibilità di supportare diversi tipi di hardware per un elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="a22e7-120">Reference to the [**CIM\_PhysicalCapacity**](cim-physicalcapacity.md) class that describes the minimum and maximum requirements and the ability to support different types of hardware for a physical element.</span></span>

</dd> <dt>

<span data-ttu-id="a22e7-121">**elemento**</span><span class="sxs-lookup"><span data-stu-id="a22e7-121">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a22e7-122">Tipo di dati **: \_ fisico CIM**</span><span class="sxs-lookup"><span data-stu-id="a22e7-122">Data type: **CIM\_PhysicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="a22e7-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="a22e7-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a22e7-124">Qualificatori: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="a22e7-124">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="a22e7-125">Riferimento all'elemento fisico da descrivere.</span><span class="sxs-lookup"><span data-stu-id="a22e7-125">Reference to the physical element being described.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a22e7-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="a22e7-126">Remarks</span></span>

<span data-ttu-id="a22e7-127">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="a22e7-127">WMI does not implement this class.</span></span>

<span data-ttu-id="a22e7-128">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="a22e7-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a22e7-129">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="a22e7-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a22e7-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a22e7-130">Requirements</span></span>



| <span data-ttu-id="a22e7-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="a22e7-131">Requirement</span></span> | <span data-ttu-id="a22e7-132">Valore</span><span class="sxs-lookup"><span data-stu-id="a22e7-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a22e7-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a22e7-133">Minimum supported client</span></span><br/> | <span data-ttu-id="a22e7-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a22e7-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a22e7-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a22e7-135">Minimum supported server</span></span><br/> | <span data-ttu-id="a22e7-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a22e7-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a22e7-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a22e7-137">Namespace</span></span><br/>                | <span data-ttu-id="a22e7-138">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="a22e7-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a22e7-139">MOF</span><span class="sxs-lookup"><span data-stu-id="a22e7-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a22e7-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a22e7-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a22e7-141">DLL</span><span class="sxs-lookup"><span data-stu-id="a22e7-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a22e7-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a22e7-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

