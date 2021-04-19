---
description: L' \_ associazione CIM SoftwareElementActions identifica le azioni per un elemento software.
ms.assetid: 2f8a584c-dff0-48f8-bc5f-2b833b5c0b18
ms.tgt_platform: multiple
title: Classe CIM_SoftwareElementActions
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareElementActions
- CIM_SoftwareElementActions.Action
- CIM_SoftwareElementActions.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1f51cc122cdf354be9611ca1cca4ebcbe1635d14
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304582"
---
# <a name="cim_softwareelementactions-class"></a><span data-ttu-id="f12c9-103">CIM \_ SoftwareElementActions (classe)</span><span class="sxs-lookup"><span data-stu-id="f12c9-103">CIM\_SoftwareElementActions class</span></span>

<span data-ttu-id="f12c9-104">L'associazione **CIM \_ SoftwareElementActions** identifica le azioni per un elemento software.</span><span class="sxs-lookup"><span data-stu-id="f12c9-104">The **CIM\_SoftwareElementActions** association identifies the actions for a software element.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f12c9-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="f12c9-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f12c9-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="f12c9-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f12c9-107">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="f12c9-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="f12c9-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="f12c9-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f12c9-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f12c9-109">Syntax</span></span>

``` syntax
[UUID("{4B82D255-E3CD-11d2-8601-0000F8102E5F}"), Association, Aggregation, Abstract, AMENDMENT]
class CIM_SoftwareElementActions
{
  CIM_Action          REF Action;
  CIM_SoftwareElement REF Element;
};
```

## <a name="members"></a><span data-ttu-id="f12c9-110">Members</span><span class="sxs-lookup"><span data-stu-id="f12c9-110">Members</span></span>

<span data-ttu-id="f12c9-111">La classe **CIM \_ SoftwareElementActions** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f12c9-111">The **CIM\_SoftwareElementActions** class has these types of members:</span></span>

-   [<span data-ttu-id="f12c9-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f12c9-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f12c9-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f12c9-113">Properties</span></span>

<span data-ttu-id="f12c9-114">La classe **CIM \_ SoftwareElementActions** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="f12c9-114">The **CIM\_SoftwareElementActions** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f12c9-115">**Azione**</span><span class="sxs-lookup"><span data-stu-id="f12c9-115">**Action**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f12c9-116">Tipo di dati **: \_ azione CIM**</span><span class="sxs-lookup"><span data-stu-id="f12c9-116">Data type: **CIM\_Action**</span></span>
</dt> <dt>

<span data-ttu-id="f12c9-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f12c9-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f12c9-118">Qualificatori: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (false), [**debole**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="f12c9-118">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (FALSE), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="f12c9-119">Riferimento a un'istanza di [**\_ azione CIM**](cim-action.md) .</span><span class="sxs-lookup"><span data-stu-id="f12c9-119">Reference to a [**CIM\_Action**](cim-action.md) instance.</span></span>

</dd> <dt>

<span data-ttu-id="f12c9-120">**elemento**</span><span class="sxs-lookup"><span data-stu-id="f12c9-120">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f12c9-121">Tipo di dati: **CIM \_ SoftwareElement**</span><span class="sxs-lookup"><span data-stu-id="f12c9-121">Data type: **CIM\_SoftwareElement**</span></span>
</dt> <dt>

<span data-ttu-id="f12c9-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f12c9-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f12c9-123">Qualificatori: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="f12c9-123">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="f12c9-124">Riferimento a un'istanza di [**CIM \_ SoftwareElement**](cim-softwareelement.md) .</span><span class="sxs-lookup"><span data-stu-id="f12c9-124">Reference to a [**CIM\_SoftwareElement**](cim-softwareelement.md) instance.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f12c9-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="f12c9-125">Remarks</span></span>

<span data-ttu-id="f12c9-126">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="f12c9-126">WMI does not implement this class.</span></span> <span data-ttu-id="f12c9-127">Per le classi WMI derivate da **CIM \_ SoftwareElementActions**, vedere [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="f12c9-127">For WMI classes derived from **CIM\_SoftwareElementActions**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="f12c9-128">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="f12c9-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f12c9-129">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="f12c9-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f12c9-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f12c9-130">Requirements</span></span>



| <span data-ttu-id="f12c9-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="f12c9-131">Requirement</span></span> | <span data-ttu-id="f12c9-132">Valore</span><span class="sxs-lookup"><span data-stu-id="f12c9-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f12c9-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f12c9-133">Minimum supported client</span></span><br/> | <span data-ttu-id="f12c9-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f12c9-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f12c9-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f12c9-135">Minimum supported server</span></span><br/> | <span data-ttu-id="f12c9-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f12c9-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f12c9-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f12c9-137">Namespace</span></span><br/>                | <span data-ttu-id="f12c9-138">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="f12c9-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f12c9-139">MOF</span><span class="sxs-lookup"><span data-stu-id="f12c9-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f12c9-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f12c9-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f12c9-141">DLL</span><span class="sxs-lookup"><span data-stu-id="f12c9-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f12c9-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f12c9-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

