---
description: La \_ classe CIM SoftwareFeatureServiceImplementation rappresenta un'associazione tra un servizio e il modo in cui viene implementata nel software.
ms.assetid: fa80cc91-8dd7-4726-a24a-5c4dfa3e786b
ms.tgt_platform: multiple
title: Classe CIM_SoftwareFeatureServiceImplementation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareFeatureServiceImplementation
- CIM_SoftwareFeatureServiceImplementation.Dependent
- CIM_SoftwareFeatureServiceImplementation.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: dc521de933a4567c0760495880baf9251a774938
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126015"
---
# <a name="cim_softwarefeatureserviceimplementation-class"></a><span data-ttu-id="ce3cf-103">CIM \_ SoftwareFeatureServiceImplementation (classe)</span><span class="sxs-lookup"><span data-stu-id="ce3cf-103">CIM\_SoftwareFeatureServiceImplementation class</span></span>

<span data-ttu-id="ce3cf-104">La classe **CIM \_ SoftwareFeatureServiceImplementation** rappresenta un'associazione tra un servizio e il modo in cui viene implementata nel software.</span><span class="sxs-lookup"><span data-stu-id="ce3cf-104">The **CIM\_SoftwareFeatureServiceImplementation** class represents an association between a service and how it is implemented in software.</span></span> <span data-ttu-id="ce3cf-105">Un servizio può essere fornito da più di una funzionalità software, operando insieme tra loro.</span><span class="sxs-lookup"><span data-stu-id="ce3cf-105">A service can be provided by more than one software feature, operating in conjunction with one another.</span></span> <span data-ttu-id="ce3cf-106">Inoltre, una funzionalità software può fornire più di un servizio.</span><span class="sxs-lookup"><span data-stu-id="ce3cf-106">Additionally, a software feature can provide more than one service.</span></span> <span data-ttu-id="ce3cf-107">Quando più funzionalità software sono associate a un singolo servizio, si presuppone che gli elementi funzionino insieme per fornire il servizio.</span><span class="sxs-lookup"><span data-stu-id="ce3cf-107">When multiple software features are associated with a single service, it is assumed that the elements operate in conjunction to provide the service.</span></span> <span data-ttu-id="ce3cf-108">Se sono presenti implementazioni diverse di un servizio, ogni implementazione comporterebbe la creazione di istanze individuali dell'oggetto servizio.</span><span class="sxs-lookup"><span data-stu-id="ce3cf-108">If different implementations of a service exist, each implementation would result in individual instantiations of the service object.</span></span> <span data-ttu-id="ce3cf-109">Le singole creazioni di istanze avrebbero quindi le associazioni alle implementazioni univoche.</span><span class="sxs-lookup"><span data-stu-id="ce3cf-109">Individual instantiations would then have associations to the unique implementations.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ce3cf-110">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="ce3cf-110">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ce3cf-111">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="ce3cf-111">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="ce3cf-112">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="ce3cf-112">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="ce3cf-113">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="ce3cf-113">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce3cf-114">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ce3cf-114">Syntax</span></span>

``` syntax
[UUID("{8AC984F4-DB37-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_SoftwareFeatureServiceImplementation : CIM_Dependency
{
  CIM_Service         REF Dependent;
  CIM_SoftwareFeature REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="ce3cf-115">Members</span><span class="sxs-lookup"><span data-stu-id="ce3cf-115">Members</span></span>

<span data-ttu-id="ce3cf-116">La classe **CIM \_ SoftwareFeatureServiceImplementation** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ce3cf-116">The **CIM\_SoftwareFeatureServiceImplementation** class has these types of members:</span></span>

-   [<span data-ttu-id="ce3cf-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ce3cf-117">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ce3cf-118">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ce3cf-118">Properties</span></span>

<span data-ttu-id="ce3cf-119">La classe **CIM \_ SoftwareFeatureServiceImplementation** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="ce3cf-119">The **CIM\_SoftwareFeatureServiceImplementation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ce3cf-120">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="ce3cf-120">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce3cf-121">Tipo di dati: **CIM \_ SoftwareFeature**</span><span class="sxs-lookup"><span data-stu-id="ce3cf-121">Data type: **CIM\_SoftwareFeature**</span></span>
</dt> <dt>

<span data-ttu-id="ce3cf-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ce3cf-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce3cf-123">Qualificatori: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="ce3cf-123">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="ce3cf-124">Un [**\_ SoftwareFeature CIM**](cim-softwarefeature.md) che descrive la funzionalità del software precedente.</span><span class="sxs-lookup"><span data-stu-id="ce3cf-124">A [**CIM\_SoftwareFeature**](cim-softwarefeature.md) that describes the antecedent software feature.</span></span>

</dd> <dt>

<span data-ttu-id="ce3cf-125">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="ce3cf-125">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce3cf-126">Tipo di dati **: \_ servizio CIM**</span><span class="sxs-lookup"><span data-stu-id="ce3cf-126">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="ce3cf-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ce3cf-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ce3cf-128">Qualificatori: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="ce3cf-128">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="ce3cf-129">[**\_ Servizio CIM**](cim-service.md) che descrive il servizio dipendente.</span><span class="sxs-lookup"><span data-stu-id="ce3cf-129">A [**CIM\_Service**](cim-service.md) that describes the dependent service.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ce3cf-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="ce3cf-130">Remarks</span></span>

<span data-ttu-id="ce3cf-131">La classe **CIM \_ SoftwareFeatureServiceImplementation** è derivata dalla [**\_ dipendenza CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="ce3cf-131">The **CIM\_SoftwareFeatureServiceImplementation** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="ce3cf-132">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="ce3cf-132">WMI does not implement this class.</span></span>

<span data-ttu-id="ce3cf-133">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="ce3cf-133">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ce3cf-134">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="ce3cf-134">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce3cf-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ce3cf-135">Requirements</span></span>



| <span data-ttu-id="ce3cf-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce3cf-136">Requirement</span></span> | <span data-ttu-id="ce3cf-137">Valore</span><span class="sxs-lookup"><span data-stu-id="ce3cf-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ce3cf-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ce3cf-138">Minimum supported client</span></span><br/> | <span data-ttu-id="ce3cf-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ce3cf-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ce3cf-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ce3cf-140">Minimum supported server</span></span><br/> | <span data-ttu-id="ce3cf-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ce3cf-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ce3cf-142">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ce3cf-142">Namespace</span></span><br/>                | <span data-ttu-id="ce3cf-143">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="ce3cf-143">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ce3cf-144">MOF</span><span class="sxs-lookup"><span data-stu-id="ce3cf-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ce3cf-145"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ce3cf-145"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ce3cf-146">DLL</span><span class="sxs-lookup"><span data-stu-id="ce3cf-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ce3cf-147"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ce3cf-147"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce3cf-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ce3cf-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce3cf-149">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="ce3cf-149">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

