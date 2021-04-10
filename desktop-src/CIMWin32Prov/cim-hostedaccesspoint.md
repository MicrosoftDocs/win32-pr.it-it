---
description: La \_ classe CIM HostedAccessPoint rappresenta un'associazione tra un punto di accesso al servizio (SAP) e il sistema in cui viene fornito. Ogni sistema può ospitare molti SAP.
ms.assetid: 7da9b781-a5cb-42f5-b03c-4fc818c94e88
ms.tgt_platform: multiple
title: Classe CIM_HostedAccessPoint (provider WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedAccessPoint
- CIM_HostedAccessPoint.Dependent
- CIM_HostedAccessPoint.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d451cec7ad42fa519b70c576fbd02a32d0289e8b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126974"
---
# <a name="cim_hostedaccesspoint-class-cimwin32-wmi-providers"></a><span data-ttu-id="e54dd-104">Classe CIM_HostedAccessPoint (provider WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="e54dd-104">CIM_HostedAccessPoint class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="e54dd-105">La classe **CIM \_ HostedAccessPoint** rappresenta un'associazione tra un punto di accesso al servizio (SAP) e il sistema in cui viene fornito.</span><span class="sxs-lookup"><span data-stu-id="e54dd-105">The **CIM\_HostedAccessPoint** class represents an association between a service access point (SAP) and the system on which it is provided.</span></span> <span data-ttu-id="e54dd-106">Ogni sistema può ospitare molti SAP.</span><span class="sxs-lookup"><span data-stu-id="e54dd-106">Each system may host many SAPs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e54dd-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="e54dd-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e54dd-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="e54dd-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e54dd-109">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="e54dd-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="e54dd-110">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="e54dd-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e54dd-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e54dd-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{576C3C56-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_HostedAccessPoint : CIM_Dependency
{
  CIM_ServiceAccessPoint REF Dependent;
  CIM_System             REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="e54dd-112">Members</span><span class="sxs-lookup"><span data-stu-id="e54dd-112">Members</span></span>

<span data-ttu-id="e54dd-113">La classe **CIM \_ HostedAccessPoint** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e54dd-113">The **CIM\_HostedAccessPoint** class has these types of members:</span></span>

-   [<span data-ttu-id="e54dd-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e54dd-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e54dd-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e54dd-115">Properties</span></span>

<span data-ttu-id="e54dd-116">La classe **CIM \_ HostedAccessPoint** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="e54dd-116">The **CIM\_HostedAccessPoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e54dd-117">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="e54dd-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e54dd-118">Tipo di dati **: \_ sistema CIM**</span><span class="sxs-lookup"><span data-stu-id="e54dd-118">Data type: **CIM\_System**</span></span>
</dt> <dt>

<span data-ttu-id="e54dd-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e54dd-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e54dd-120">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="e54dd-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="e54dd-121">[**\_ Sistema CIM**](cim-system.md) che descrive il sistema host.</span><span class="sxs-lookup"><span data-stu-id="e54dd-121">A [**CIM\_System**](cim-system.md) that describes the hosting system.</span></span>

</dd> <dt>

<span data-ttu-id="e54dd-122">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="e54dd-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e54dd-123">Tipo di dati: **CIM \_ serviceAccessPoint**</span><span class="sxs-lookup"><span data-stu-id="e54dd-123">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="e54dd-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e54dd-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e54dd-125">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente"), [**debole**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e54dd-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e54dd-126">Un [**\_ serviceAccessPoint CIM**](cim-serviceaccesspoint.md) che descrive i SAP ospitati in questo sistema.</span><span class="sxs-lookup"><span data-stu-id="e54dd-126">A [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) that describes The SAP(s) that are hosted on this system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e54dd-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="e54dd-127">Remarks</span></span>

<span data-ttu-id="e54dd-128">**CIM \_ HostedAccessPoint** è derivato dalla [**\_ dipendenza CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="e54dd-128">**CIM\_HostedAccessPoint** is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="e54dd-129">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="e54dd-129">WMI does not implement this class.</span></span>

<span data-ttu-id="e54dd-130">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="e54dd-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e54dd-131">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="e54dd-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e54dd-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e54dd-132">Requirements</span></span>



| <span data-ttu-id="e54dd-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="e54dd-133">Requirement</span></span> | <span data-ttu-id="e54dd-134">Valore</span><span class="sxs-lookup"><span data-stu-id="e54dd-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e54dd-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e54dd-135">Minimum supported client</span></span><br/> | <span data-ttu-id="e54dd-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e54dd-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e54dd-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e54dd-137">Minimum supported server</span></span><br/> | <span data-ttu-id="e54dd-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e54dd-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e54dd-139">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e54dd-139">Namespace</span></span><br/>                | <span data-ttu-id="e54dd-140">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="e54dd-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e54dd-141">MOF</span><span class="sxs-lookup"><span data-stu-id="e54dd-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e54dd-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e54dd-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e54dd-143">DLL</span><span class="sxs-lookup"><span data-stu-id="e54dd-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e54dd-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e54dd-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e54dd-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e54dd-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e54dd-146">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="e54dd-146">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

