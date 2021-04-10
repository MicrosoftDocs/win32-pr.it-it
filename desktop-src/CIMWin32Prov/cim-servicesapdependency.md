---
description: La \_ classe CIM ServiceSAPDependency rappresenta un'associazione tra un servizio e un punto di accesso al servizio (SAP), che indica che il servizio SAP a cui viene fatto riferimento viene usato dal servizio per fornire le funzionalità.
ms.assetid: cf5a8b9b-a38e-4173-861c-e417fbea6016
ms.tgt_platform: multiple
title: Classe CIM_ServiceSAPDependency (provider WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ServiceSAPDependency
- CIM_ServiceSAPDependency.Dependent
- CIM_ServiceSAPDependency.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e47283c962b377b70bc14efe998752d9009796df
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126663"
---
# <a name="cim_servicesapdependency-class-cimwin32-wmi-providers"></a><span data-ttu-id="ff96e-103">Classe CIM_ServiceSAPDependency (provider WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="ff96e-103">CIM_ServiceSAPDependency class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="ff96e-104">La classe **CIM \_ ServiceSAPDependency** rappresenta un'associazione tra un servizio e un punto di accesso al servizio (SAP), che indica che il servizio SAP a cui viene fatto riferimento viene usato dal servizio per fornire le funzionalità.</span><span class="sxs-lookup"><span data-stu-id="ff96e-104">The **CIM\_ServiceSAPDependency** class represents an association between a service and a service access point (SAP), which indicates that the referenced SAP is used by the service to provide its functionality.</span></span> <span data-ttu-id="ff96e-105">Ad esempio, i servizi di avvio possono richiamare i servizi disco BIOS (interrupt) per funzionare.</span><span class="sxs-lookup"><span data-stu-id="ff96e-105">For example, boot services can invoke BIOS disk services (interrupts) to function.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ff96e-106">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="ff96e-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ff96e-107">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="ff96e-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="ff96e-108">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="ff96e-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="ff96e-109">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="ff96e-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff96e-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ff96e-110">Syntax</span></span>

``` syntax
[UUID("{652E2D58-DB37-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_ServiceSAPDependency : CIM_Dependency
{
  CIM_Service            REF Dependent;
  CIM_ServiceAccessPoint REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="ff96e-111">Members</span><span class="sxs-lookup"><span data-stu-id="ff96e-111">Members</span></span>

<span data-ttu-id="ff96e-112">La classe **CIM \_ ServiceSAPDependency** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ff96e-112">The **CIM\_ServiceSAPDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="ff96e-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ff96e-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ff96e-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ff96e-114">Properties</span></span>

<span data-ttu-id="ff96e-115">La classe **CIM \_ ServiceSAPDependency** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="ff96e-115">The **CIM\_ServiceSAPDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ff96e-116">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="ff96e-116">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff96e-117">Tipo di dati: **CIM \_ serviceAccessPoint**</span><span class="sxs-lookup"><span data-stu-id="ff96e-117">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="ff96e-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ff96e-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ff96e-119">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="ff96e-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="ff96e-120">Un [**\_ serviceAccessPoint CIM**](cim-serviceaccesspoint.md) che descrive il punto di accesso al servizio richiesto.</span><span class="sxs-lookup"><span data-stu-id="ff96e-120">A [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) that describes the required service access point.</span></span>

</dd> <dt>

<span data-ttu-id="ff96e-121">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="ff96e-121">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff96e-122">Tipo di dati **: \_ servizio CIM**</span><span class="sxs-lookup"><span data-stu-id="ff96e-122">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="ff96e-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ff96e-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ff96e-124">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="ff96e-124">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="ff96e-125">[**\_ Servizio CIM**](cim-service.md) che descrive il servizio che dipende da un SAP sottostante.</span><span class="sxs-lookup"><span data-stu-id="ff96e-125">A [**CIM\_Service**](cim-service.md) that describes the service that is dependent on an underlying SAP.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ff96e-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="ff96e-126">Remarks</span></span>

<span data-ttu-id="ff96e-127">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="ff96e-127">WMI does not implement this class.</span></span>

<span data-ttu-id="ff96e-128">La classe **CIM \_ ServiceSAPDependency** è derivata dalla [**\_ dipendenza CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="ff96e-128">The **CIM\_ServiceSAPDependency** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="ff96e-129">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="ff96e-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ff96e-130">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="ff96e-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff96e-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ff96e-131">Requirements</span></span>



| <span data-ttu-id="ff96e-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff96e-132">Requirement</span></span> | <span data-ttu-id="ff96e-133">Valore</span><span class="sxs-lookup"><span data-stu-id="ff96e-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ff96e-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ff96e-134">Minimum supported client</span></span><br/> | <span data-ttu-id="ff96e-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ff96e-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ff96e-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ff96e-136">Minimum supported server</span></span><br/> | <span data-ttu-id="ff96e-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ff96e-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ff96e-138">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ff96e-138">Namespace</span></span><br/>                | <span data-ttu-id="ff96e-139">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="ff96e-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ff96e-140">MOF</span><span class="sxs-lookup"><span data-stu-id="ff96e-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ff96e-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ff96e-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ff96e-142">DLL</span><span class="sxs-lookup"><span data-stu-id="ff96e-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ff96e-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ff96e-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff96e-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ff96e-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff96e-145">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="ff96e-145">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

