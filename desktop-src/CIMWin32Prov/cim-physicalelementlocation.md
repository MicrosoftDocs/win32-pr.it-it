---
description: La \_ classe CIM PhysicalElementLocation associa un elemento fisico a un \_ oggetto percorso CIM a scopo di inventario o sostituzione.
ms.assetid: d1698c1a-0eda-4e32-9a29-fb741b987671
ms.tgt_platform: multiple
title: Classe CIM_PhysicalElementLocation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalElementLocation
- CIM_PhysicalElementLocation.Element
- CIM_PhysicalElementLocation.PhysicalLocation
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5e47460a3563d9b7a86aa6ee65704fcb0a422c39
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127383"
---
# <a name="cim_physicalelementlocation-class"></a><span data-ttu-id="dd005-103">CIM \_ PhysicalElementLocation (classe)</span><span class="sxs-lookup"><span data-stu-id="dd005-103">CIM\_PhysicalElementLocation class</span></span>

<span data-ttu-id="dd005-104">La classe **CIM \_ PhysicalElementLocation** associa un elemento fisico a un [**oggetto \_ percorso CIM**](cim-location.md) a scopo di inventario o sostituzione.</span><span class="sxs-lookup"><span data-stu-id="dd005-104">The **CIM\_PhysicalElementLocation** class associates a physical element with a [**CIM\_Location**](cim-location.md) object for inventory or replacement purposes.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dd005-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="dd005-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="dd005-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="dd005-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="dd005-107">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="dd005-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="dd005-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="dd005-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd005-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dd005-109">Syntax</span></span>

``` syntax
[Abstract, Association, UUID("{FAF76B68-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalElementLocation
{
  CIM_PhysicalElement REF Element;
  CIM_Location        REF PhysicalLocation;
};
```

## <a name="members"></a><span data-ttu-id="dd005-110">Members</span><span class="sxs-lookup"><span data-stu-id="dd005-110">Members</span></span>

<span data-ttu-id="dd005-111">La classe **CIM \_ PhysicalElementLocation** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="dd005-111">The **CIM\_PhysicalElementLocation** class has these types of members:</span></span>

-   [<span data-ttu-id="dd005-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="dd005-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dd005-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="dd005-113">Properties</span></span>

<span data-ttu-id="dd005-114">La classe **CIM \_ PhysicalElementLocation** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="dd005-114">The **CIM\_PhysicalElementLocation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dd005-115">**elemento**</span><span class="sxs-lookup"><span data-stu-id="dd005-115">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd005-116">Tipo di dati **: \_ fisico CIM**</span><span class="sxs-lookup"><span data-stu-id="dd005-116">Data type: **CIM\_PhysicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="dd005-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dd005-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dd005-118">Riferimento all'elemento fisico il cui percorso è specificato.</span><span class="sxs-lookup"><span data-stu-id="dd005-118">Reference to the physical element whose location is specified.</span></span>

</dd> <dt>

<span data-ttu-id="dd005-119">**PhysicalLocation**</span><span class="sxs-lookup"><span data-stu-id="dd005-119">**PhysicalLocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd005-120">Tipo di dati **: \_ percorso CIM**</span><span class="sxs-lookup"><span data-stu-id="dd005-120">Data type: **CIM\_Location**</span></span>
</dt> <dt>

<span data-ttu-id="dd005-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="dd005-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd005-122">Qualificatori: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="dd005-122">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="dd005-123">Riferimento alla posizione dell'elemento fisico.</span><span class="sxs-lookup"><span data-stu-id="dd005-123">Reference to the physical element's location.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dd005-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="dd005-124">Remarks</span></span>

<span data-ttu-id="dd005-125">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="dd005-125">WMI does not implement this class.</span></span>

<span data-ttu-id="dd005-126">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="dd005-126">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="dd005-127">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="dd005-127">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd005-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dd005-128">Requirements</span></span>



| <span data-ttu-id="dd005-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd005-129">Requirement</span></span> | <span data-ttu-id="dd005-130">Valore</span><span class="sxs-lookup"><span data-stu-id="dd005-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dd005-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dd005-131">Minimum supported client</span></span><br/> | <span data-ttu-id="dd005-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dd005-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dd005-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dd005-133">Minimum supported server</span></span><br/> | <span data-ttu-id="dd005-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dd005-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dd005-135">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="dd005-135">Namespace</span></span><br/>                | <span data-ttu-id="dd005-136">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="dd005-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="dd005-137">MOF</span><span class="sxs-lookup"><span data-stu-id="dd005-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dd005-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dd005-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="dd005-139">DLL</span><span class="sxs-lookup"><span data-stu-id="dd005-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd005-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd005-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

