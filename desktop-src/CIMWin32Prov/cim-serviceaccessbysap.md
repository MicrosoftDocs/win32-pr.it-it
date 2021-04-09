---
description: La \_ classe di associazione CIM ServiceAccessBySAP rappresenta i punti di accesso per un servizio. Ad esempio, è possibile accedere a una stampante mediante i punti di accesso (SAP) di NetWare, Macintosh o Windows, che sono potenzialmente ospitati in sistemi diversi.
ms.assetid: 68311a56-b034-4a30-a885-74a745a738d8
ms.tgt_platform: multiple
title: Classe CIM_ServiceAccessBySAP
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ServiceAccessBySAP
- CIM_ServiceAccessBySAP.Dependent
- CIM_ServiceAccessBySAP.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e34b2af50a6475461ae4d39d156d26143fcb75f5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966094"
---
# <a name="cim_serviceaccessbysap-class"></a><span data-ttu-id="78109-104">CIM \_ ServiceAccessBySAP (classe)</span><span class="sxs-lookup"><span data-stu-id="78109-104">CIM\_ServiceAccessBySAP class</span></span>

<span data-ttu-id="78109-105">La classe di associazione **CIM \_ ServiceAccessBySAP** rappresenta i punti di accesso per un servizio.</span><span class="sxs-lookup"><span data-stu-id="78109-105">The **CIM\_ServiceAccessBySAP** association class represents the access points for a service.</span></span> <span data-ttu-id="78109-106">Ad esempio, è possibile accedere a una stampante mediante i punti di accesso (SAP) di NetWare, Macintosh o Windows, che sono potenzialmente ospitati in sistemi diversi.</span><span class="sxs-lookup"><span data-stu-id="78109-106">For example, a printer can be accessed by NetWare, Macintosh, or Windows service access points (SAPs), which are potentially hosted on different systems.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="78109-107">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="78109-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="78109-108">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="78109-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="78109-109">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="78109-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="78109-110">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="78109-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="78109-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="78109-111">Syntax</span></span>

``` syntax
[UUID("{714C00BA-DB37-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_ServiceAccessBySAP : CIM_Dependency
{
  CIM_ServiceAccessPoint REF Dependent;
  CIM_Service            REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="78109-112">Members</span><span class="sxs-lookup"><span data-stu-id="78109-112">Members</span></span>

<span data-ttu-id="78109-113">La classe **CIM \_ ServiceAccessBySAP** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="78109-113">The **CIM\_ServiceAccessBySAP** class has these types of members:</span></span>

-   [<span data-ttu-id="78109-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="78109-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="78109-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="78109-115">Properties</span></span>

<span data-ttu-id="78109-116">La classe **CIM \_ ServiceAccessBySAP** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="78109-116">The **CIM\_ServiceAccessBySAP** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="78109-117">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="78109-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78109-118">Tipo di dati **: \_ servizio CIM**</span><span class="sxs-lookup"><span data-stu-id="78109-118">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="78109-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="78109-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78109-120">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="78109-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="78109-121">[**\_ Servizio CIM**](cim-service.md) che descrive il servizio.</span><span class="sxs-lookup"><span data-stu-id="78109-121">A [**CIM\_Service**](cim-service.md) that describes the service.</span></span>

</dd> <dt>

<span data-ttu-id="78109-122">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="78109-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78109-123">Tipo di dati: **CIM \_ serviceAccessPoint**</span><span class="sxs-lookup"><span data-stu-id="78109-123">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="78109-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="78109-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78109-125">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="78109-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="78109-126">Un [**\_ serviceAccessPoint CIM**](cim-serviceaccesspoint.md) che descrive un punto di accesso per un servizio.</span><span class="sxs-lookup"><span data-stu-id="78109-126">A [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) that describes an access point for a service.</span></span> <span data-ttu-id="78109-127">I punti di accesso dipendono da questa relazione poiché non dispongono di funzioni senza un servizio corrispondente.</span><span class="sxs-lookup"><span data-stu-id="78109-127">Access points are dependent in this relationship since they have no function without a corresponding service.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="78109-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="78109-128">Remarks</span></span>

<span data-ttu-id="78109-129">La classe **CIM \_ ServiceAccessBySAP** è derivata dalla [**\_ dipendenza CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="78109-129">The **CIM\_ServiceAccessBySAP** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="78109-130">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="78109-130">WMI does not implement this class.</span></span> <span data-ttu-id="78109-131">Per le classi WMI derivate da **CIM \_ ServiceAccessBySAP**, vedere [Win32 Classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="78109-131">For WMI classes that are derived from **CIM\_ServiceAccessBySAP**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="78109-132">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="78109-132">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="78109-133">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="78109-133">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="78109-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="78109-134">Requirements</span></span>



| <span data-ttu-id="78109-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="78109-135">Requirement</span></span> | <span data-ttu-id="78109-136">Valore</span><span class="sxs-lookup"><span data-stu-id="78109-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="78109-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="78109-137">Minimum supported client</span></span><br/> | <span data-ttu-id="78109-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="78109-138">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="78109-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="78109-139">Minimum supported server</span></span><br/> | <span data-ttu-id="78109-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="78109-140">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="78109-141">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="78109-141">Namespace</span></span><br/>                | <span data-ttu-id="78109-142">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="78109-142">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="78109-143">MOF</span><span class="sxs-lookup"><span data-stu-id="78109-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="78109-144"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="78109-144"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="78109-145">DLL</span><span class="sxs-lookup"><span data-stu-id="78109-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="78109-146"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78109-146"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78109-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="78109-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78109-148">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="78109-148">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

