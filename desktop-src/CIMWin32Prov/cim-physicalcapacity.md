---
description: La \_ classe CIM PhysicalCapacity è una classe astratta che rappresenta i requisiti minimi e massimi di un elemento fisico e la capacità di supportare diversi tipi di hardware.
ms.assetid: e422aec0-1830-464e-ac52-2911652165a2
ms.tgt_platform: multiple
title: Classe CIM_PhysicalCapacity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalCapacity
- CIM_PhysicalCapacity.Caption
- CIM_PhysicalCapacity.Description
- CIM_PhysicalCapacity.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 50f928f69d34600c0f90865a4df44a5d7697fc89
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966198"
---
# <a name="cim_physicalcapacity-class"></a><span data-ttu-id="5933a-103">CIM \_ PhysicalCapacity (classe)</span><span class="sxs-lookup"><span data-stu-id="5933a-103">CIM\_PhysicalCapacity class</span></span>

<span data-ttu-id="5933a-104">La classe **CIM \_ PhysicalCapacity** è una classe astratta che rappresenta i requisiti minimi e massimi di un elemento fisico e la capacità di supportare diversi tipi di hardware.</span><span class="sxs-lookup"><span data-stu-id="5933a-104">The **CIM\_PhysicalCapacity** class is an abstract class that represents a physical element's minimum and maximum requirements and its ability to support different types of hardware.</span></span> <span data-ttu-id="5933a-105">Ad esempio, è possibile modellare i requisiti di memoria minimi e massimi come sottoclasse di **CIM \_ PhysicalCapacity**.</span><span class="sxs-lookup"><span data-stu-id="5933a-105">For example, minimum and maximum memory requirements can be modeled as a subclass of **CIM\_PhysicalCapacity**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5933a-106">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="5933a-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="5933a-107">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="5933a-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="5933a-108">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="5933a-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="5933a-109">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="5933a-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5933a-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5933a-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B69-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalCapacity
{
  string Caption;
  string Description;
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="5933a-111">Members</span><span class="sxs-lookup"><span data-stu-id="5933a-111">Members</span></span>

<span data-ttu-id="5933a-112">La classe **CIM \_ PhysicalCapacity** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="5933a-112">The **CIM\_PhysicalCapacity** class has these types of members:</span></span>

-   [<span data-ttu-id="5933a-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5933a-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5933a-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5933a-114">Properties</span></span>

<span data-ttu-id="5933a-115">La classe **CIM \_ PhysicalCapacity** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="5933a-115">The **CIM\_PhysicalCapacity** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5933a-116">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="5933a-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5933a-117">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5933a-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5933a-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5933a-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5933a-119">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="5933a-119">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="5933a-120">Breve descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5933a-120">Short textual description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="5933a-121">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="5933a-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5933a-122">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5933a-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5933a-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5933a-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5933a-124">Descrizione testuale dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5933a-124">Textual description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="5933a-125">**Nome**</span><span class="sxs-lookup"><span data-stu-id="5933a-125">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5933a-126">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="5933a-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5933a-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5933a-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5933a-128">Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="5933a-128">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="5933a-129">Etichetta con cui l'oggetto è noto.</span><span class="sxs-lookup"><span data-stu-id="5933a-129">Label by which the object is known.</span></span> <span data-ttu-id="5933a-130">Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="5933a-130">When subclassed, this property can be overridden to be a key property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5933a-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="5933a-131">Remarks</span></span>

<span data-ttu-id="5933a-132">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="5933a-132">WMI does not implement this class.</span></span>

<span data-ttu-id="5933a-133">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="5933a-133">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="5933a-134">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="5933a-134">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="5933a-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5933a-135">Requirements</span></span>



| <span data-ttu-id="5933a-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="5933a-136">Requirement</span></span> | <span data-ttu-id="5933a-137">Valore</span><span class="sxs-lookup"><span data-stu-id="5933a-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5933a-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5933a-138">Minimum supported client</span></span><br/> | <span data-ttu-id="5933a-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5933a-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5933a-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5933a-140">Minimum supported server</span></span><br/> | <span data-ttu-id="5933a-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5933a-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5933a-142">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5933a-142">Namespace</span></span><br/>                | <span data-ttu-id="5933a-143">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="5933a-143">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5933a-144">MOF</span><span class="sxs-lookup"><span data-stu-id="5933a-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5933a-145"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5933a-145"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5933a-146">DLL</span><span class="sxs-lookup"><span data-stu-id="5933a-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5933a-147"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5933a-147"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

