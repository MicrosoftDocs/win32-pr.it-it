---
description: La \_ classe CIM SoftwareFeatureSAPImplementation rappresenta un'associazione tra un punto di accesso al servizio (SAP) e il modo in cui viene implementato nel software.
ms.assetid: d9a5a747-b37b-4005-a661-2bfc6a83bbb2
ms.tgt_platform: multiple
title: Classe CIM_SoftwareFeatureSAPImplementation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareFeatureSAPImplementation
- CIM_SoftwareFeatureSAPImplementation.Dependent
- CIM_SoftwareFeatureSAPImplementation.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4130163ce90aea7a72b4d76a5c6c20b0631edf3b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877285"
---
# <a name="cim_softwarefeaturesapimplementation-class"></a><span data-ttu-id="06196-103">CIM \_ SoftwareFeatureSAPImplementation (classe)</span><span class="sxs-lookup"><span data-stu-id="06196-103">CIM\_SoftwareFeatureSAPImplementation class</span></span>

<span data-ttu-id="06196-104">La classe **CIM \_ SoftwareFeatureSAPImplementation** rappresenta un'associazione tra un punto di accesso al servizio (SAP) e il modo in cui viene implementato nel software.</span><span class="sxs-lookup"><span data-stu-id="06196-104">The **CIM\_SoftwareFeatureSAPImplementation** class represents an association between a service access point (SAP) and how it is implemented in software.</span></span> <span data-ttu-id="06196-105">Un SAP può essere fornito da più di una funzionalità software per operare insieme tra loro.</span><span class="sxs-lookup"><span data-stu-id="06196-105">A SAP can be provided by more than one software feature to operate in conjunction with one another.</span></span> <span data-ttu-id="06196-106">Inoltre, una funzionalità software può fornire più di un SAP.</span><span class="sxs-lookup"><span data-stu-id="06196-106">Additionally, a software feature can provide more than one SAP.</span></span> <span data-ttu-id="06196-107">Quando molte funzionalità software sono associate a un singolo SAP, si presuppone che gli elementi funzionino insieme per fornire il punto di accesso.</span><span class="sxs-lookup"><span data-stu-id="06196-107">When many software features are associated with a single SAP, it is assumed that the elements operate in conjunction to provide the access point.</span></span> <span data-ttu-id="06196-108">Se sono presenti implementazioni diverse di un SAP, ogni implementazione comporterebbe la creazione di istanze singole dell'oggetto SAP.</span><span class="sxs-lookup"><span data-stu-id="06196-108">If different implementations of a SAP exist, each implementation would result in individual instantiations of the SAP object.</span></span> <span data-ttu-id="06196-109">Le singole creazioni di istanze avrebbero quindi le associazioni alle implementazioni univoche.</span><span class="sxs-lookup"><span data-stu-id="06196-109">Individual instantiations would then have associations to the unique implementations.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="06196-110">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="06196-110">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="06196-111">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="06196-111">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="06196-112">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="06196-112">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="06196-113">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="06196-113">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="06196-114">Sintassi</span><span class="sxs-lookup"><span data-stu-id="06196-114">Syntax</span></span>

``` syntax
[UUID("{7EFCC186-DB37-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_SoftwareFeatureSAPImplementation : CIM_Dependency
{
  CIM_ServiceAccessPoint REF Dependent;
  CIM_SoftwareFeature    REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="06196-115">Members</span><span class="sxs-lookup"><span data-stu-id="06196-115">Members</span></span>

<span data-ttu-id="06196-116">La classe **CIM \_ SoftwareFeatureSAPImplementation** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="06196-116">The **CIM\_SoftwareFeatureSAPImplementation** class has these types of members:</span></span>

-   [<span data-ttu-id="06196-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="06196-117">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="06196-118">Proprietà</span><span class="sxs-lookup"><span data-stu-id="06196-118">Properties</span></span>

<span data-ttu-id="06196-119">La classe **CIM \_ SoftwareFeatureSAPImplementation** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="06196-119">The **CIM\_SoftwareFeatureSAPImplementation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="06196-120">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="06196-120">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06196-121">Tipo di dati: **CIM \_ SoftwareFeature**</span><span class="sxs-lookup"><span data-stu-id="06196-121">Data type: **CIM\_SoftwareFeature**</span></span>
</dt> <dt>

<span data-ttu-id="06196-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="06196-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06196-123">Qualificatori: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="06196-123">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="06196-124">Un [**\_ SoftwareFeature CIM**](cim-softwarefeature.md) che descrive la funzionalità del software precedente.</span><span class="sxs-lookup"><span data-stu-id="06196-124">A [**CIM\_SoftwareFeature**](cim-softwarefeature.md) that describes the antecedent software feature.</span></span>

</dd> <dt>

<span data-ttu-id="06196-125">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="06196-125">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06196-126">Tipo di dati: **CIM \_ serviceAccessPoint**</span><span class="sxs-lookup"><span data-stu-id="06196-126">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="06196-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="06196-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06196-128">Qualificatori: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="06196-128">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="06196-129">Un [**\_ serviceAccessPoint CIM**](cim-serviceaccesspoint.md) che descrive il punto di accesso al servizio dipendente.</span><span class="sxs-lookup"><span data-stu-id="06196-129">A [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) that describes the dependent service access point.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="06196-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="06196-130">Remarks</span></span>

<span data-ttu-id="06196-131">La classe **CIM \_ SoftwareFeatureSAPImplementation** è derivata dalla [**\_ dipendenza CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="06196-131">The **CIM\_SoftwareFeatureSAPImplementation** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="06196-132">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="06196-132">WMI does not implement this class.</span></span>

<span data-ttu-id="06196-133">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="06196-133">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="06196-134">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="06196-134">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="06196-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="06196-135">Requirements</span></span>



| <span data-ttu-id="06196-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="06196-136">Requirement</span></span> | <span data-ttu-id="06196-137">Valore</span><span class="sxs-lookup"><span data-stu-id="06196-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="06196-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="06196-138">Minimum supported client</span></span><br/> | <span data-ttu-id="06196-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="06196-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="06196-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="06196-140">Minimum supported server</span></span><br/> | <span data-ttu-id="06196-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="06196-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="06196-142">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="06196-142">Namespace</span></span><br/>                | <span data-ttu-id="06196-143">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="06196-143">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="06196-144">MOF</span><span class="sxs-lookup"><span data-stu-id="06196-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="06196-145"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="06196-145"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="06196-146">DLL</span><span class="sxs-lookup"><span data-stu-id="06196-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="06196-147"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="06196-147"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06196-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="06196-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06196-149">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="06196-149">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

