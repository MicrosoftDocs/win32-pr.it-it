---
description: La \_ classe CIM BootServiceAccessBySAP associa un servizio di avvio e i relativi punti di accesso.
ms.assetid: 993469dd-fb9c-4d21-99e0-03c4b19eb7fd
ms.tgt_platform: multiple
title: Classe CIM_BootServiceAccessBySAP
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BootServiceAccessBySAP
- CIM_BootServiceAccessBySAP.Dependent
- CIM_BootServiceAccessBySAP.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 90548be52defbcf3419d6c7defc21395da5cfbfe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748618"
---
# <a name="cim_bootserviceaccessbysap-class"></a><span data-ttu-id="7b0a6-103">CIM \_ BootServiceAccessBySAP (classe)</span><span class="sxs-lookup"><span data-stu-id="7b0a6-103">CIM\_BootServiceAccessBySAP class</span></span>

<span data-ttu-id="7b0a6-104">La classe **CIM \_ BootServiceAccessBySAP** associa un servizio di avvio e i relativi punti di accesso.</span><span class="sxs-lookup"><span data-stu-id="7b0a6-104">The **CIM\_BootServiceAccessBySAP** class associates a boot service and its access points.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7b0a6-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="7b0a6-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="7b0a6-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="7b0a6-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="7b0a6-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="7b0a6-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="7b0a6-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="7b0a6-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b0a6-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7b0a6-109">Syntax</span></span>

``` syntax
[UUID("{6EDF1DD2-DB35-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_BootServiceAccessBySAP : CIM_ServiceAccessBySAP
{
  CIM_BootSAP     REF Dependent;
  CIM_BootService REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="7b0a6-110">Members</span><span class="sxs-lookup"><span data-stu-id="7b0a6-110">Members</span></span>

<span data-ttu-id="7b0a6-111">La classe **CIM \_ BootServiceAccessBySAP** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="7b0a6-111">The **CIM\_BootServiceAccessBySAP** class has these types of members:</span></span>

-   [<span data-ttu-id="7b0a6-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7b0a6-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7b0a6-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7b0a6-113">Properties</span></span>

<span data-ttu-id="7b0a6-114">La classe **CIM \_ BootServiceAccessBySAP** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="7b0a6-114">The **CIM\_BootServiceAccessBySAP** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7b0a6-115">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="7b0a6-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b0a6-116">Tipo di dati: **CIM \_ BOOTSERVICE**</span><span class="sxs-lookup"><span data-stu-id="7b0a6-116">Data type: **CIM\_BootService**</span></span>
</dt> <dt>

<span data-ttu-id="7b0a6-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7b0a6-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b0a6-118">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="7b0a6-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="7b0a6-119">Un [**\_ BOOTSERVICE CIM**](cim-bootservice.md) che descrive il servizio di avvio.</span><span class="sxs-lookup"><span data-stu-id="7b0a6-119">A [**CIM\_BootService**](cim-bootservice.md) that describes the boot service.</span></span>

</dd> <dt>

<span data-ttu-id="7b0a6-120">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="7b0a6-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b0a6-121">Tipo di dati: **CIM \_ BootSAP**</span><span class="sxs-lookup"><span data-stu-id="7b0a6-121">Data type: **CIM\_BootSAP**</span></span>
</dt> <dt>

<span data-ttu-id="7b0a6-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="7b0a6-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b0a6-123">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="7b0a6-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="7b0a6-124">Un [**\_ BootSAP CIM**](cim-bootsap.md) che descrive un punto di accesso per il servizio di avvio.</span><span class="sxs-lookup"><span data-stu-id="7b0a6-124">A [**CIM\_BootSAP**](cim-bootsap.md) that describes an access point for the boot service.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7b0a6-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="7b0a6-125">Remarks</span></span>

<span data-ttu-id="7b0a6-126">La classe **CIM \_ BootServiceAccessBySAP** è derivata da [**CIM \_ ServiceAccessBySAP**](cim-serviceaccessbysap.md).</span><span class="sxs-lookup"><span data-stu-id="7b0a6-126">The **CIM\_BootServiceAccessBySAP** class is derived from [**CIM\_ServiceAccessBySAP**](cim-serviceaccessbysap.md).</span></span>

<span data-ttu-id="7b0a6-127">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="7b0a6-127">WMI does not implement this class.</span></span>

<span data-ttu-id="7b0a6-128">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="7b0a6-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="7b0a6-129">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="7b0a6-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b0a6-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7b0a6-130">Requirements</span></span>



| <span data-ttu-id="7b0a6-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b0a6-131">Requirement</span></span> | <span data-ttu-id="7b0a6-132">Valore</span><span class="sxs-lookup"><span data-stu-id="7b0a6-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7b0a6-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7b0a6-133">Minimum supported client</span></span><br/> | <span data-ttu-id="7b0a6-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7b0a6-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7b0a6-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7b0a6-135">Minimum supported server</span></span><br/> | <span data-ttu-id="7b0a6-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7b0a6-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7b0a6-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="7b0a6-137">Namespace</span></span><br/>                | <span data-ttu-id="7b0a6-138">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="7b0a6-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7b0a6-139">MOF</span><span class="sxs-lookup"><span data-stu-id="7b0a6-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7b0a6-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7b0a6-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7b0a6-141">DLL</span><span class="sxs-lookup"><span data-stu-id="7b0a6-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b0a6-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b0a6-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b0a6-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7b0a6-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b0a6-144">**\_SERVICEACCESSBYSAP CIM**</span><span class="sxs-lookup"><span data-stu-id="7b0a6-144">**CIM\_ServiceAccessBySAP**</span></span>](cim-serviceaccessbysap.md)
</dt> </dl>

 

