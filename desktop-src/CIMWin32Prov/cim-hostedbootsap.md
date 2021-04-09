---
description: La \_ classe CIM HostedBootSAP definisce il computer del sistema di hosting per una \_ classe CIM BootSAP.
ms.assetid: 2113de13-e7af-4a1c-ba80-27e2c57af8a0
ms.tgt_platform: multiple
title: Classe CIM_HostedBootSAP
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedBootSAP
- CIM_HostedBootSAP.Dependent
- CIM_HostedBootSAP.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 12e801f420ca2c56cc8960175391cdd9a669a00d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966154"
---
# <a name="cim_hostedbootsap-class"></a><span data-ttu-id="f67c9-103">CIM \_ HostedBootSAP (classe)</span><span class="sxs-lookup"><span data-stu-id="f67c9-103">CIM\_HostedBootSAP class</span></span>

<span data-ttu-id="f67c9-104">La classe **CIM \_ HostedBootSAP** definisce il computer del sistema di hosting per una classe [**CIM \_ BootSAP**](cim-bootsap.md) .</span><span class="sxs-lookup"><span data-stu-id="f67c9-104">The **CIM\_HostedBootSAP** class defines the hosting unitary computer system for a [**CIM\_BootSAP**](cim-bootsap.md) class.</span></span> <span data-ttu-id="f67c9-105">Poiché questa relazione è sottoclassata da [**CIM \_ HostedAccessPoint**](cim-hostedaccesspoint.md), eredita lo schema di ambito/denominazione definito per [**CIM \_ serviceAccessPoint**](cim-serviceaccesspoint.md), in cui un punto di accesso rinvia al relativo sistema di hosting.</span><span class="sxs-lookup"><span data-stu-id="f67c9-105">Since this relationship is subclassed from [**CIM\_HostedAccessPoint**](cim-hostedaccesspoint.md), it inherits the scoping/naming scheme defined for [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md), where an access point defers to its hosting system.</span></span> <span data-ttu-id="f67c9-106">In questo caso, **CIM \_ BootSAP** deve rinviare alla relativa classe [**CIM \_ UnitaryComputerSystem**](cim-unitarycomputersystem.md) di hosting.</span><span class="sxs-lookup"><span data-stu-id="f67c9-106">In this case, **CIM\_BootSAP** must defer to its hosting [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md) class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f67c9-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="f67c9-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f67c9-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="f67c9-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f67c9-109">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="f67c9-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="f67c9-110">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="f67c9-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f67c9-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f67c9-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{625B4512-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_HostedBootSAP : CIM_HostedAccessPoint
{
  CIM_BootSAP               REF Dependent;
  CIM_UnitaryComputerSystem REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="f67c9-112">Members</span><span class="sxs-lookup"><span data-stu-id="f67c9-112">Members</span></span>

<span data-ttu-id="f67c9-113">La classe **CIM \_ HostedBootSAP** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f67c9-113">The **CIM\_HostedBootSAP** class has these types of members:</span></span>

-   [<span data-ttu-id="f67c9-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f67c9-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f67c9-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f67c9-115">Properties</span></span>

<span data-ttu-id="f67c9-116">La classe **CIM \_ HostedBootSAP** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="f67c9-116">The **CIM\_HostedBootSAP** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f67c9-117">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="f67c9-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f67c9-118">Tipo di dati: **CIM \_ UnitaryComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="f67c9-118">Data type: **CIM\_UnitaryComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="f67c9-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f67c9-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f67c9-120">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="f67c9-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="f67c9-121">Un [**\_ UnitaryComputerSystem CIM**](cim-unitarycomputersystem.md) che descrive il sistema informatico.</span><span class="sxs-lookup"><span data-stu-id="f67c9-121">A [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md) that describes the unitary computer system.</span></span>

</dd> <dt>

<span data-ttu-id="f67c9-122">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="f67c9-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f67c9-123">Tipo di dati: **CIM \_ BootSAP**</span><span class="sxs-lookup"><span data-stu-id="f67c9-123">Data type: **CIM\_BootSAP**</span></span>
</dt> <dt>

<span data-ttu-id="f67c9-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f67c9-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f67c9-125">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="f67c9-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="f67c9-126">Un [**\_ BootSAP CIM**](cim-bootsap.md) che descrive la SAP di avvio ospitata nel sistema informatico.</span><span class="sxs-lookup"><span data-stu-id="f67c9-126">A [**CIM\_BootSAP**](cim-bootsap.md) that describes the Boot SAP hosted on the unitary computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f67c9-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="f67c9-127">Remarks</span></span>

<span data-ttu-id="f67c9-128">La classe **CIM \_ HostedBootSAP** è derivata da [**CIM \_ HostedAccessPoint**](cim-hostedaccesspoint.md).</span><span class="sxs-lookup"><span data-stu-id="f67c9-128">The **CIM\_HostedBootSAP** class is derived from [**CIM\_HostedAccessPoint**](cim-hostedaccesspoint.md).</span></span>

<span data-ttu-id="f67c9-129">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="f67c9-129">WMI does not implement this class.</span></span>

<span data-ttu-id="f67c9-130">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="f67c9-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f67c9-131">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="f67c9-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f67c9-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f67c9-132">Requirements</span></span>



| <span data-ttu-id="f67c9-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="f67c9-133">Requirement</span></span> | <span data-ttu-id="f67c9-134">Valore</span><span class="sxs-lookup"><span data-stu-id="f67c9-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f67c9-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f67c9-135">Minimum supported client</span></span><br/> | <span data-ttu-id="f67c9-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f67c9-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f67c9-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f67c9-137">Minimum supported server</span></span><br/> | <span data-ttu-id="f67c9-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f67c9-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f67c9-139">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f67c9-139">Namespace</span></span><br/>                | <span data-ttu-id="f67c9-140">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="f67c9-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f67c9-141">MOF</span><span class="sxs-lookup"><span data-stu-id="f67c9-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f67c9-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f67c9-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f67c9-143">DLL</span><span class="sxs-lookup"><span data-stu-id="f67c9-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f67c9-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f67c9-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f67c9-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f67c9-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f67c9-146">**\_HOSTEDACCESSPOINT CIM**</span><span class="sxs-lookup"><span data-stu-id="f67c9-146">**CIM\_HostedAccessPoint**</span></span>](cim-hostedaccesspoint.md)
</dt> </dl>

 

