---
description: La \_ classe CIM HostedBootService associa un sistema di hosting e un servizio di avvio. Poiché questa relazione è sottoclassata da CIM \_ servizio ospitato, eredita lo schema di ambito/denominazione definito per il servizio, dove un servizio rinvia al relativo sistema di hosting.
ms.assetid: 91621288-a231-4423-94df-7601bdf2ebe1
ms.tgt_platform: multiple
title: Classe CIM_HostedBootService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedBootService
- CIM_HostedBootService.Antecedent
- CIM_HostedBootService.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 12baa364653feda1400ad15d658e6739859b2521
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126970"
---
# <a name="cim_hostedbootservice-class"></a><span data-ttu-id="bd250-104">CIM \_ HostedBootService (classe)</span><span class="sxs-lookup"><span data-stu-id="bd250-104">CIM\_HostedBootService class</span></span>

<span data-ttu-id="bd250-105">La classe **CIM \_ HostedBootService** associa un sistema di hosting e un servizio di avvio.</span><span class="sxs-lookup"><span data-stu-id="bd250-105">The **CIM\_HostedBootService** class associates a hosting system and a boot service.</span></span> <span data-ttu-id="bd250-106">Poiché questa relazione è sottoclassata da [**CIM \_ servizio ospitato**](cim-hostedservice.md), eredita lo schema di ambito/denominazione definito per il servizio, dove un servizio rinvia al relativo sistema di hosting.</span><span class="sxs-lookup"><span data-stu-id="bd250-106">Since this relationship is subclassed from [**CIM\_HostedService**](cim-hostedservice.md), it inherits the scoping/naming scheme defined for service, where a service defers to its hosting system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bd250-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="bd250-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="bd250-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="bd250-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="bd250-109">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="bd250-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="bd250-110">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="bd250-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd250-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bd250-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{6DAE7092-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_HostedBootService : CIM_HostedService
{
  CIM_System      REF Antecedent;
  CIM_BootService REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="bd250-112">Members</span><span class="sxs-lookup"><span data-stu-id="bd250-112">Members</span></span>

<span data-ttu-id="bd250-113">La classe **CIM \_ HostedBootService** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="bd250-113">The **CIM\_HostedBootService** class has these types of members:</span></span>

-   [<span data-ttu-id="bd250-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bd250-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bd250-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="bd250-115">Properties</span></span>

<span data-ttu-id="bd250-116">La classe **CIM \_ HostedBootService** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="bd250-116">The **CIM\_HostedBootService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bd250-117">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="bd250-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd250-118">Tipo di dati **: \_ sistema CIM**</span><span class="sxs-lookup"><span data-stu-id="bd250-118">Data type: **CIM\_System**</span></span>
</dt> <dt>

<span data-ttu-id="bd250-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bd250-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd250-120">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (precedente)</span><span class="sxs-lookup"><span data-stu-id="bd250-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) (Antecedent)</span></span>
</dt> </dl>

<span data-ttu-id="bd250-121">[**\_ Sistema CIM**](cim-system.md) che descrive il sistema host.</span><span class="sxs-lookup"><span data-stu-id="bd250-121">A [**CIM\_System**](cim-system.md) that describes the hosting system.</span></span>

</dd> <dt>

<span data-ttu-id="bd250-122">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="bd250-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd250-123">Tipo di dati: **CIM \_ BOOTSERVICE**</span><span class="sxs-lookup"><span data-stu-id="bd250-123">Data type: **CIM\_BootService**</span></span>
</dt> <dt>

<span data-ttu-id="bd250-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="bd250-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd250-125">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="bd250-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="bd250-126">Un [**\_ BOOTSERVICE CIM**](cim-bootservice.md) che descrive il servizio di avvio ospitato nel sistema.</span><span class="sxs-lookup"><span data-stu-id="bd250-126">A [**CIM\_BootService**](cim-bootservice.md) that describes the boot service hosted on the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bd250-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="bd250-127">Remarks</span></span>

<span data-ttu-id="bd250-128">La classe **CIM \_ HostedBootService** è derivata da [**CIM \_ servizio ospitato**](cim-hostedservice.md).</span><span class="sxs-lookup"><span data-stu-id="bd250-128">The **CIM\_HostedBootService** class is derived from [**CIM\_HostedService**](cim-hostedservice.md).</span></span>

<span data-ttu-id="bd250-129">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="bd250-129">WMI does not implement this class.</span></span>

<span data-ttu-id="bd250-130">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="bd250-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="bd250-131">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="bd250-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd250-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bd250-132">Requirements</span></span>



| <span data-ttu-id="bd250-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd250-133">Requirement</span></span> | <span data-ttu-id="bd250-134">Valore</span><span class="sxs-lookup"><span data-stu-id="bd250-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bd250-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bd250-135">Minimum supported client</span></span><br/> | <span data-ttu-id="bd250-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bd250-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bd250-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bd250-137">Minimum supported server</span></span><br/> | <span data-ttu-id="bd250-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bd250-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bd250-139">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="bd250-139">Namespace</span></span><br/>                | <span data-ttu-id="bd250-140">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="bd250-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="bd250-141">MOF</span><span class="sxs-lookup"><span data-stu-id="bd250-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bd250-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bd250-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="bd250-143">DLL</span><span class="sxs-lookup"><span data-stu-id="bd250-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd250-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd250-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd250-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bd250-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd250-146">**\_Servizio ospitato CIM**</span><span class="sxs-lookup"><span data-stu-id="bd250-146">**CIM\_HostedService**</span></span>](cim-hostedservice.md)
</dt> </dl>

 

