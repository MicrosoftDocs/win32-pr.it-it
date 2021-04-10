---
description: La \_ classe CIM HostedJobDestination rappresenta un'associazione tra una destinazione del processo e il sistema in cui risiede. Un sistema può ospitare numerose code di processi. Le destinazioni dei processi rinviano al sistema host.
ms.assetid: 5d853826-1f27-417b-a053-5e0ee9816376
ms.tgt_platform: multiple
title: Classe CIM_HostedJobDestination
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedJobDestination
- CIM_HostedJobDestination.Dependent
- CIM_HostedJobDestination.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c22e911c6b0adcc38de11fd2410e4797c9381a25
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225683"
---
# <a name="cim_hostedjobdestination-class"></a><span data-ttu-id="51f5a-105">CIM \_ HostedJobDestination (classe)</span><span class="sxs-lookup"><span data-stu-id="51f5a-105">CIM\_HostedJobDestination class</span></span>

<span data-ttu-id="51f5a-106">La classe **CIM \_ HostedJobDestination** rappresenta un'associazione tra una destinazione del processo e il sistema in cui risiede.</span><span class="sxs-lookup"><span data-stu-id="51f5a-106">The **CIM\_HostedJobDestination** class represents an association between a job destination and the system on which it resides.</span></span> <span data-ttu-id="51f5a-107">Un sistema può ospitare numerose code di processi.</span><span class="sxs-lookup"><span data-stu-id="51f5a-107">A system may host many job queues.</span></span> <span data-ttu-id="51f5a-108">Le destinazioni dei processi rinviano al sistema host.</span><span class="sxs-lookup"><span data-stu-id="51f5a-108">Job destinations defer to the hosting system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="51f5a-109">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="51f5a-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="51f5a-110">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="51f5a-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="51f5a-111">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="51f5a-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="51f5a-112">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="51f5a-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="51f5a-113">Sintassi</span><span class="sxs-lookup"><span data-stu-id="51f5a-113">Syntax</span></span>

``` syntax
[Abstract, UUID("{7880DD16-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_HostedJobDestination : CIM_Dependency
{
  CIM_JobDestination REF Dependent;
  CIM_System         REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="51f5a-114">Members</span><span class="sxs-lookup"><span data-stu-id="51f5a-114">Members</span></span>

<span data-ttu-id="51f5a-115">La classe **CIM \_ HostedJobDestination** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="51f5a-115">The **CIM\_HostedJobDestination** class has these types of members:</span></span>

-   [<span data-ttu-id="51f5a-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="51f5a-116">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="51f5a-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="51f5a-117">Properties</span></span>

<span data-ttu-id="51f5a-118">La classe **CIM \_ HostedJobDestination** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="51f5a-118">The **CIM\_HostedJobDestination** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="51f5a-119">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="51f5a-119">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51f5a-120">Tipo di dati **: \_ sistema CIM**</span><span class="sxs-lookup"><span data-stu-id="51f5a-120">Data type: **CIM\_System**</span></span>
</dt> <dt>

<span data-ttu-id="51f5a-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="51f5a-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51f5a-122">Qualificatori: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="51f5a-122">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="51f5a-123">[**\_ Sistema CIM**](cim-system.md) che descrive il sistema host.</span><span class="sxs-lookup"><span data-stu-id="51f5a-123">A [**CIM\_System**](cim-system.md) that describes the hosting system.</span></span>

</dd> <dt>

<span data-ttu-id="51f5a-124">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="51f5a-124">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51f5a-125">Tipo di dati: **CIM \_ JobDestination**</span><span class="sxs-lookup"><span data-stu-id="51f5a-125">Data type: **CIM\_JobDestination**</span></span>
</dt> <dt>

<span data-ttu-id="51f5a-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="51f5a-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="51f5a-127">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente"), [**debole**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="51f5a-127">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="51f5a-128">Un [**\_ JobDestination CIM**](cim-jobdestination.md) che descrive la destinazione del processo ospitata nel sistema.</span><span class="sxs-lookup"><span data-stu-id="51f5a-128">A [**CIM\_JobDestination**](cim-jobdestination.md) describing the job destination hosted on the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="51f5a-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="51f5a-129">Remarks</span></span>

<span data-ttu-id="51f5a-130">**CIM \_ HostedJobDestination** è derivato dalla [**\_ dipendenza CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="51f5a-130">**CIM\_HostedJobDestination** is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="51f5a-131">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="51f5a-131">WMI does not implement this class.</span></span>

<span data-ttu-id="51f5a-132">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="51f5a-132">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="51f5a-133">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="51f5a-133">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="51f5a-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="51f5a-134">Requirements</span></span>



| <span data-ttu-id="51f5a-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="51f5a-135">Requirement</span></span> | <span data-ttu-id="51f5a-136">Valore</span><span class="sxs-lookup"><span data-stu-id="51f5a-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="51f5a-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="51f5a-137">Minimum supported client</span></span><br/> | <span data-ttu-id="51f5a-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="51f5a-138">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="51f5a-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="51f5a-139">Minimum supported server</span></span><br/> | <span data-ttu-id="51f5a-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="51f5a-140">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="51f5a-141">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="51f5a-141">Namespace</span></span><br/>                | <span data-ttu-id="51f5a-142">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="51f5a-142">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="51f5a-143">MOF</span><span class="sxs-lookup"><span data-stu-id="51f5a-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="51f5a-144"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="51f5a-144"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="51f5a-145">DLL</span><span class="sxs-lookup"><span data-stu-id="51f5a-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="51f5a-146"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="51f5a-146"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51f5a-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="51f5a-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51f5a-148">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="51f5a-148">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

