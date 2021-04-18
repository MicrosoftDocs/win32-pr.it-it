---
description: La \_ classe CIM ServiceServiceDependency rappresenta un'associazione tra due servizi.
ms.assetid: 0fb43fb3-2c05-4762-b339-2dcc090ed38d
ms.tgt_platform: multiple
title: Classe CIM_ServiceServiceDependency
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ServiceServiceDependency
- CIM_ServiceServiceDependency.Dependent
- CIM_ServiceServiceDependency.Antecedent
- CIM_ServiceServiceDependency.TypeOfDependency
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fdc8ea1a3324395e5230ca6d47487b61c8c02ba9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304765"
---
# <a name="cim_serviceservicedependency-class"></a><span data-ttu-id="fa3f9-103">CIM \_ ServiceServiceDependency (classe)</span><span class="sxs-lookup"><span data-stu-id="fa3f9-103">CIM\_ServiceServiceDependency class</span></span>

<span data-ttu-id="fa3f9-104">La classe **CIM \_ ServiceServiceDependency** rappresenta un'associazione tra due servizi.</span><span class="sxs-lookup"><span data-stu-id="fa3f9-104">The **CIM\_ServiceServiceDependency** class represents an association between two services.</span></span> <span data-ttu-id="fa3f9-105">Il servizio associato deve essere presente, deve essere stato completato oppure deve essere assente affinché l'altro servizio funzioni.</span><span class="sxs-lookup"><span data-stu-id="fa3f9-105">The associated service must be present, must have completed, or must be absent for the other service to function.</span></span> <span data-ttu-id="fa3f9-106">È ad esempio possibile che i servizi di avvio dipendano da servizi BIOS, dischi e inizializzazione sottostanti.</span><span class="sxs-lookup"><span data-stu-id="fa3f9-106">For example, boot services can be dependent on underlying BIOS, disk, and initialization services.</span></span> <span data-ttu-id="fa3f9-107">Per i servizi di inizializzazione, il servizio di avvio dipende dal completamento dei servizi di inizializzazione.</span><span class="sxs-lookup"><span data-stu-id="fa3f9-107">For initialization services, the boot service is dependent on the initialization services completing.</span></span> <span data-ttu-id="fa3f9-108">Per i servizi disco, i servizi di avvio possono effettivamente utilizzare i succhi di questo servizio.</span><span class="sxs-lookup"><span data-stu-id="fa3f9-108">For disk services, boot services can actually use the SAPs of this service.</span></span> <span data-ttu-id="fa3f9-109">Questa dipendenza di utilizzo è modellata sull'associazione [**CIM \_ ServiceSAPDependency**](cim-servicesapdependency.md) .</span><span class="sxs-lookup"><span data-stu-id="fa3f9-109">This usage dependency is modeled on the [**CIM\_ServiceSAPDependency**](cim-servicesapdependency.md) association.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fa3f9-110">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="fa3f9-110">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="fa3f9-111">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="fa3f9-111">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="fa3f9-112">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="fa3f9-112">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="fa3f9-113">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="fa3f9-113">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa3f9-114">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fa3f9-114">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C53B-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_ServiceServiceDependency : CIM_Dependency
{
  CIM_Service REF Dependent;
  CIM_Service REF Antecedent;
  uint16          TypeOfDependency;
};
```

## <a name="members"></a><span data-ttu-id="fa3f9-115">Members</span><span class="sxs-lookup"><span data-stu-id="fa3f9-115">Members</span></span>

<span data-ttu-id="fa3f9-116">La classe **CIM \_ ServiceServiceDependency** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="fa3f9-116">The **CIM\_ServiceServiceDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="fa3f9-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="fa3f9-117">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fa3f9-118">Proprietà</span><span class="sxs-lookup"><span data-stu-id="fa3f9-118">Properties</span></span>

<span data-ttu-id="fa3f9-119">La classe **CIM \_ ServiceServiceDependency** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="fa3f9-119">The **CIM\_ServiceServiceDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fa3f9-120">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="fa3f9-120">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa3f9-121">Tipo di dati **: \_ servizio CIM**</span><span class="sxs-lookup"><span data-stu-id="fa3f9-121">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="fa3f9-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fa3f9-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa3f9-123">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="fa3f9-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="fa3f9-124">[**\_ Servizio CIM**](cim-service.md) che descrive il servizio richiesto.</span><span class="sxs-lookup"><span data-stu-id="fa3f9-124">A [**CIM\_Service**](cim-service.md) that describes the required service.</span></span>

</dd> <dt>

<span data-ttu-id="fa3f9-125">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="fa3f9-125">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa3f9-126">Tipo di dati **: \_ servizio CIM**</span><span class="sxs-lookup"><span data-stu-id="fa3f9-126">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="fa3f9-127">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fa3f9-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa3f9-128">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="fa3f9-128">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="fa3f9-129">[**\_ Servizio CIM**](cim-service.md) che descrive il servizio che dipende da un servizio sottostante.</span><span class="sxs-lookup"><span data-stu-id="fa3f9-129">A [**CIM\_Service**](cim-service.md) that describes the service that is dependent on an underlying service.</span></span>

</dd> <dt>

<span data-ttu-id="fa3f9-130">**TypeOfDependency**</span><span class="sxs-lookup"><span data-stu-id="fa3f9-130">**TypeOfDependency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa3f9-131">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fa3f9-131">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fa3f9-132">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fa3f9-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fa3f9-133">Natura della dipendenza da servizio a servizio.</span><span class="sxs-lookup"><span data-stu-id="fa3f9-133">Nature of the service-to-service dependency.</span></span> <span data-ttu-id="fa3f9-134">Questa proprietà indica che il servizio associato deve essere stato completato, deve essere avviato o non deve essere avviato per il funzionamento del servizio.</span><span class="sxs-lookup"><span data-stu-id="fa3f9-134">This property indicates that the associated service must have completed, must be started, or must not be started for the service to function.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fa3f9-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="fa3f9-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="fa3f9-136"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="fa3f9-136"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_Must_Have_Completed"></span><span id="service_must_have_completed"></span><span id="SERVICE_MUST_HAVE_COMPLETED"></span>

<span data-ttu-id="fa3f9-137"><span id="Service_Must_Have_Completed"></span><span id="service_must_have_completed"></span><span id="SERVICE_MUST_HAVE_COMPLETED"></span>Il **servizio deve essere stato completato** (2)</span><span class="sxs-lookup"><span data-stu-id="fa3f9-137"><span id="Service_Must_Have_Completed"></span><span id="service_must_have_completed"></span><span id="SERVICE_MUST_HAVE_COMPLETED"></span>**Service Must Have Completed** (2)</span></span>


</dt> <dd>

<span data-ttu-id="fa3f9-138">Il servizio deve essere stato completato.</span><span class="sxs-lookup"><span data-stu-id="fa3f9-138">Service must have completed.</span></span>

</dd> <dt>

<span id="Service_Must_Be_Started"></span><span id="service_must_be_started"></span><span id="SERVICE_MUST_BE_STARTED"></span>

<span data-ttu-id="fa3f9-139"><span id="Service_Must_Be_Started"></span><span id="service_must_be_started"></span><span id="SERVICE_MUST_BE_STARTED"></span>Il **servizio deve essere avviato** (3)</span><span class="sxs-lookup"><span data-stu-id="fa3f9-139"><span id="Service_Must_Be_Started"></span><span id="service_must_be_started"></span><span id="SERVICE_MUST_BE_STARTED"></span>**Service Must Be Started** (3)</span></span>


</dt> <dd>

<span data-ttu-id="fa3f9-140">Il servizio deve essere avviato.</span><span class="sxs-lookup"><span data-stu-id="fa3f9-140">Service must be started.</span></span>

</dd> <dt>

<span id="Service_Must_Not_Be_Started"></span><span id="service_must_not_be_started"></span><span id="SERVICE_MUST_NOT_BE_STARTED"></span>

<span data-ttu-id="fa3f9-141"><span id="Service_Must_Not_Be_Started"></span><span id="service_must_not_be_started"></span><span id="SERVICE_MUST_NOT_BE_STARTED"></span>Il **servizio non deve essere avviato** (4)</span><span class="sxs-lookup"><span data-stu-id="fa3f9-141"><span id="Service_Must_Not_Be_Started"></span><span id="service_must_not_be_started"></span><span id="SERVICE_MUST_NOT_BE_STARTED"></span>**Service Must Not Be Started** (4)</span></span>


</dt> <dd>

<span data-ttu-id="fa3f9-142">Il servizio non deve essere avviato.</span><span class="sxs-lookup"><span data-stu-id="fa3f9-142">Service must not be started.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fa3f9-143">Commenti</span><span class="sxs-lookup"><span data-stu-id="fa3f9-143">Remarks</span></span>

<span data-ttu-id="fa3f9-144">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="fa3f9-144">WMI does not implement this class.</span></span> <span data-ttu-id="fa3f9-145">Per le classi WMI derivate da **CIM \_ ServiceServiceDependency**, vedere [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="fa3f9-145">For WMI classes derived from **CIM\_ServiceServiceDependency**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="fa3f9-146">La classe **CIM \_ ServiceServiceDependency** è derivata dalla [**\_ dipendenza CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="fa3f9-146">The **CIM\_ServiceServiceDependency** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="fa3f9-147">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="fa3f9-147">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="fa3f9-148">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="fa3f9-148">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa3f9-149">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fa3f9-149">Requirements</span></span>



| <span data-ttu-id="fa3f9-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa3f9-150">Requirement</span></span> | <span data-ttu-id="fa3f9-151">Valore</span><span class="sxs-lookup"><span data-stu-id="fa3f9-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fa3f9-152">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fa3f9-152">Minimum supported client</span></span><br/> | <span data-ttu-id="fa3f9-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fa3f9-153">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fa3f9-154">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fa3f9-154">Minimum supported server</span></span><br/> | <span data-ttu-id="fa3f9-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fa3f9-155">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fa3f9-156">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="fa3f9-156">Namespace</span></span><br/>                | <span data-ttu-id="fa3f9-157">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="fa3f9-157">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fa3f9-158">MOF</span><span class="sxs-lookup"><span data-stu-id="fa3f9-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fa3f9-159"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fa3f9-159"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fa3f9-160">DLL</span><span class="sxs-lookup"><span data-stu-id="fa3f9-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa3f9-161"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa3f9-161"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa3f9-162">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fa3f9-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa3f9-163">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="fa3f9-163">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

