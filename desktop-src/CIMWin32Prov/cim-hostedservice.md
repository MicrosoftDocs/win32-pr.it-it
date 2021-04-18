---
description: La \_ classe CIM servizio ospitato rappresenta un'associazione tra un servizio e il sistema in cui risiede la funzionalità.
ms.assetid: 23bb385d-dd22-4126-aea9-d2f22527223e
ms.tgt_platform: multiple
title: Classe CIM_HostedService (provider WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedService
- CIM_HostedService.Dependent
- CIM_HostedService.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c63b28fed7977c9fce78fe1030afbe66d5b2d75e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304908"
---
# <a name="cim_hostedservice-class-cimwin32-wmi-providers"></a><span data-ttu-id="ab292-103">Classe CIM_HostedService (provider WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="ab292-103">CIM_HostedService class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="ab292-104">La classe **CIM \_ servizio ospitato** rappresenta un'associazione tra un servizio e il sistema in cui risiede la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="ab292-104">The **CIM\_HostedService** class represents an association between a service and the system on which the functionality resides.</span></span> <span data-ttu-id="ab292-105">Un sistema può ospitare molti servizi, che rinviano al sistema host.</span><span class="sxs-lookup"><span data-stu-id="ab292-105">A system may host many services, which defer to the hosting system.</span></span> <span data-ttu-id="ab292-106">Il modello non rappresenta servizi ospitati in più sistemi.</span><span class="sxs-lookup"><span data-stu-id="ab292-106">The model does not represent services hosted across multiple systems.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ab292-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="ab292-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ab292-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="ab292-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="ab292-109">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="ab292-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="ab292-110">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="ab292-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab292-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ab292-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{83B2A7AA-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_HostedService : CIM_Dependency
{
  CIM_Service REF Dependent;
  CIM_System  REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="ab292-112">Members</span><span class="sxs-lookup"><span data-stu-id="ab292-112">Members</span></span>

<span data-ttu-id="ab292-113">La classe **CIM \_ servizio ospitato** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="ab292-113">The **CIM\_HostedService** class has these types of members:</span></span>

-   [<span data-ttu-id="ab292-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ab292-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ab292-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="ab292-115">Properties</span></span>

<span data-ttu-id="ab292-116">La classe **CIM \_ servizio ospitato** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="ab292-116">The **CIM\_HostedService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ab292-117">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="ab292-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab292-118">Tipo di dati **: \_ sistema CIM**</span><span class="sxs-lookup"><span data-stu-id="ab292-118">Data type: **CIM\_System**</span></span>
</dt> <dt>

<span data-ttu-id="ab292-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ab292-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab292-120">Qualificatori: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="ab292-120">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="ab292-121">[**\_ Sistema CIM**](cim-system.md) che descrive il sistema host.</span><span class="sxs-lookup"><span data-stu-id="ab292-121">A [**CIM\_System**](cim-system.md) that describes the hosting system.</span></span>

</dd> <dt>

<span data-ttu-id="ab292-122">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="ab292-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab292-123">Tipo di dati **: \_ servizio CIM**</span><span class="sxs-lookup"><span data-stu-id="ab292-123">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="ab292-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="ab292-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab292-125">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente"), [**debole**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="ab292-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="ab292-126">[**\_ Servizio CIM**](cim-service.md) che descrive il servizio ospitato nel sistema.</span><span class="sxs-lookup"><span data-stu-id="ab292-126">A [**CIM\_Service**](cim-service.md) that describes the service hosted on the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ab292-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="ab292-127">Remarks</span></span>

<span data-ttu-id="ab292-128">**CIM \_ Servizio ospitato** è derivato dalla [**\_ dipendenza CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="ab292-128">**CIM\_HostedService** is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="ab292-129">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="ab292-129">WMI does not implement this class.</span></span>

<span data-ttu-id="ab292-130">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="ab292-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ab292-131">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="ab292-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab292-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ab292-132">Requirements</span></span>



| <span data-ttu-id="ab292-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab292-133">Requirement</span></span> | <span data-ttu-id="ab292-134">Valore</span><span class="sxs-lookup"><span data-stu-id="ab292-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ab292-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ab292-135">Minimum supported client</span></span><br/> | <span data-ttu-id="ab292-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ab292-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ab292-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ab292-137">Minimum supported server</span></span><br/> | <span data-ttu-id="ab292-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ab292-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ab292-139">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ab292-139">Namespace</span></span><br/>                | <span data-ttu-id="ab292-140">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="ab292-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ab292-141">MOF</span><span class="sxs-lookup"><span data-stu-id="ab292-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ab292-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ab292-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ab292-143">DLL</span><span class="sxs-lookup"><span data-stu-id="ab292-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab292-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab292-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab292-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ab292-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab292-146">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="ab292-146">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

