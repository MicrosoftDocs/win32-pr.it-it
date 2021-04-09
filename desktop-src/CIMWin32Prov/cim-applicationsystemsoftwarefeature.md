---
description: La \_ classe CIM ApplicationSystemSoftwareFeature rappresenta un'associazione che identifica le funzionalità software che costituiscono un particolare sistema applicativo. Le funzionalità software possono essere incluse in prodotti diversi.
ms.assetid: e40d0d64-f9f0-4c05-aef6-c759256e408b
ms.tgt_platform: multiple
title: Classe CIM_ApplicationSystemSoftwareFeature
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ApplicationSystemSoftwareFeature
- CIM_ApplicationSystemSoftwareFeature.PartComponent
- CIM_ApplicationSystemSoftwareFeature.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6b13a15370b19583eef61fb36fda2d63fcb61989
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878069"
---
# <a name="cim_applicationsystemsoftwarefeature-class"></a><span data-ttu-id="3e9bd-104">CIM \_ ApplicationSystemSoftwareFeature (classe)</span><span class="sxs-lookup"><span data-stu-id="3e9bd-104">CIM\_ApplicationSystemSoftwareFeature class</span></span>

<span data-ttu-id="3e9bd-105">La classe **CIM \_ ApplicationSystemSoftwareFeature** rappresenta un'associazione che identifica le funzionalità software che costituiscono un particolare sistema applicativo.</span><span class="sxs-lookup"><span data-stu-id="3e9bd-105">The **CIM\_ApplicationSystemSoftwareFeature** class represents an association that identifies the software features that make up a particular application system.</span></span> <span data-ttu-id="3e9bd-106">Le funzionalità software possono essere incluse in prodotti diversi.</span><span class="sxs-lookup"><span data-stu-id="3e9bd-106">The software features can be included in different products.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3e9bd-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="3e9bd-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="3e9bd-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="3e9bd-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="3e9bd-109">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="3e9bd-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="3e9bd-110">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="3e9bd-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e9bd-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3e9bd-111">Syntax</span></span>

``` syntax
[UUID("{0E17B9EA-E3D3-11d2-8601-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_ApplicationSystemSoftwareFeature : CIM_SystemComponent
{
  CIM_SoftwareFeature   REF PartComponent;
  CIM_ApplicationSystem REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="3e9bd-112">Members</span><span class="sxs-lookup"><span data-stu-id="3e9bd-112">Members</span></span>

<span data-ttu-id="3e9bd-113">La classe **CIM \_ ApplicationSystemSoftwareFeature** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="3e9bd-113">The **CIM\_ApplicationSystemSoftwareFeature** class has these types of members:</span></span>

-   [<span data-ttu-id="3e9bd-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3e9bd-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3e9bd-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3e9bd-115">Properties</span></span>

<span data-ttu-id="3e9bd-116">La classe **CIM \_ ApplicationSystemSoftwareFeature** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="3e9bd-116">The **CIM\_ApplicationSystemSoftwareFeature** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3e9bd-117">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="3e9bd-117">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9bd-118">Tipo di dati: **CIM \_ ApplicationSystem**</span><span class="sxs-lookup"><span data-stu-id="3e9bd-118">Data type: **CIM\_ApplicationSystem**</span></span>
</dt> <dt>

<span data-ttu-id="3e9bd-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3e9bd-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e9bd-120">Qualificatori: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="3e9bd-120">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="3e9bd-121">Un [**\_ ApplicationSystem CIM**](cim-applicationsystem.md) che contiene il sistema padre nell'associazione.</span><span class="sxs-lookup"><span data-stu-id="3e9bd-121">A [**CIM\_ApplicationSystem**](cim-applicationsystem.md) that contains the parent system in the association.</span></span>

</dd> <dt>

<span data-ttu-id="3e9bd-122">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="3e9bd-122">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e9bd-123">Tipo di dati: **CIM \_ SoftwareFeature**</span><span class="sxs-lookup"><span data-stu-id="3e9bd-123">Data type: **CIM\_SoftwareFeature**</span></span>
</dt> <dt>

<span data-ttu-id="3e9bd-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3e9bd-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e9bd-125">Qualificatori: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="3e9bd-125">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="3e9bd-126">Un [**\_ SoftwareFeature CIM**](cim-softwarefeature.md) che contiene l'elemento figlio che è un componente di un sistema.</span><span class="sxs-lookup"><span data-stu-id="3e9bd-126">A [**CIM\_SoftwareFeature**](cim-softwarefeature.md) that contain the child element that is a component of a system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3e9bd-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="3e9bd-127">Remarks</span></span>

<span data-ttu-id="3e9bd-128">La classe **CIM \_ ApplicationSystemSoftwareFeature** è derivata da [**CIM \_ SystemComponent**](cim-systemcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="3e9bd-128">The **CIM\_ApplicationSystemSoftwareFeature** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).</span></span>

<span data-ttu-id="3e9bd-129">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="3e9bd-129">WMI does not implement this class.</span></span>

<span data-ttu-id="3e9bd-130">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="3e9bd-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="3e9bd-131">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="3e9bd-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e9bd-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3e9bd-132">Requirements</span></span>



| <span data-ttu-id="3e9bd-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e9bd-133">Requirement</span></span> | <span data-ttu-id="3e9bd-134">Valore</span><span class="sxs-lookup"><span data-stu-id="3e9bd-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3e9bd-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3e9bd-135">Minimum supported client</span></span><br/> | <span data-ttu-id="3e9bd-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3e9bd-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3e9bd-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3e9bd-137">Minimum supported server</span></span><br/> | <span data-ttu-id="3e9bd-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3e9bd-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3e9bd-139">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3e9bd-139">Namespace</span></span><br/>                | <span data-ttu-id="3e9bd-140">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="3e9bd-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3e9bd-141">MOF</span><span class="sxs-lookup"><span data-stu-id="3e9bd-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3e9bd-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3e9bd-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3e9bd-143">DLL</span><span class="sxs-lookup"><span data-stu-id="3e9bd-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e9bd-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e9bd-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e9bd-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3e9bd-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e9bd-146">**\_SYSTEMCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="3e9bd-146">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> </dl>

 

