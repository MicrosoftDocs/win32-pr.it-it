---
description: La \_ classe CIM ClusterServiceAccessBySAP rappresenta la relazione tra un servizio di clustering e i relativi punti di accesso.
ms.assetid: b1e03ef1-909c-4836-a75f-c8d88a4d0087
ms.tgt_platform: multiple
title: Classe CIM_ClusterServiceAccessBySAP
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ClusterServiceAccessBySAP
- CIM_ClusterServiceAccessBySAP.Dependent
- CIM_ClusterServiceAccessBySAP.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9b6e6f0df20f182be392de3fbb0cb13068cbeffc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966206"
---
# <a name="cim_clusterserviceaccessbysap-class"></a><span data-ttu-id="40f25-103">CIM \_ ClusterServiceAccessBySAP (classe)</span><span class="sxs-lookup"><span data-stu-id="40f25-103">CIM\_ClusterServiceAccessBySAP class</span></span>

<span data-ttu-id="40f25-104">La classe **CIM \_ ClusterServiceAccessBySAP** rappresenta la relazione tra un servizio di clustering e i relativi punti di accesso.</span><span class="sxs-lookup"><span data-stu-id="40f25-104">The **CIM\_ClusterServiceAccessBySAP** class represents the relationship between a clustering service and its access points.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="40f25-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="40f25-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="40f25-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="40f25-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="40f25-107">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="40f25-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="40f25-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="40f25-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="40f25-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="40f25-109">Syntax</span></span>

``` syntax
[UUID("{88F073D8-DB35-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_ClusterServiceAccessBySAP : CIM_ServiceAccessBySAP
{
  CIM_ClusteringSAP     REF Dependent;
  CIM_ClusteringService REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="40f25-110">Members</span><span class="sxs-lookup"><span data-stu-id="40f25-110">Members</span></span>

<span data-ttu-id="40f25-111">La classe **CIM \_ ClusterServiceAccessBySAP** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="40f25-111">The **CIM\_ClusterServiceAccessBySAP** class has these types of members:</span></span>

-   [<span data-ttu-id="40f25-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="40f25-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="40f25-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="40f25-113">Properties</span></span>

<span data-ttu-id="40f25-114">La classe **CIM \_ ClusterServiceAccessBySAP** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="40f25-114">The **CIM\_ClusterServiceAccessBySAP** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="40f25-115">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="40f25-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40f25-116">Tipo di dati: **CIM \_ ClusteringService**</span><span class="sxs-lookup"><span data-stu-id="40f25-116">Data type: **CIM\_ClusteringService**</span></span>
</dt> <dt>

<span data-ttu-id="40f25-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="40f25-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40f25-118">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="40f25-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="40f25-119">Un [**\_ ClusteringService CIM**](cim-clusteringservice.md) che descrive il servizio di clustering.</span><span class="sxs-lookup"><span data-stu-id="40f25-119">A [**CIM\_ClusteringService**](cim-clusteringservice.md) that describes the clustering service.</span></span>

</dd> <dt>

<span data-ttu-id="40f25-120">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="40f25-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40f25-121">Tipo di dati: **CIM \_ ClusteringSAP**</span><span class="sxs-lookup"><span data-stu-id="40f25-121">Data type: **CIM\_ClusteringSAP**</span></span>
</dt> <dt>

<span data-ttu-id="40f25-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="40f25-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40f25-123">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="40f25-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="40f25-124">Un [**\_ ClusteringSAP CIM**](cim-clusteringsap.md) che descrive un punto di accesso per il servizio di clustering.</span><span class="sxs-lookup"><span data-stu-id="40f25-124">A [**CIM\_ClusteringSAP**](cim-clusteringsap.md) that describes an access point for the clustering service.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="40f25-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="40f25-125">Remarks</span></span>

<span data-ttu-id="40f25-126">La classe **CIM \_ ClusterServiceAccessBySAP** è derivata da [**CIM \_ ServiceAccessBySAP**](cim-serviceaccessbysap.md).</span><span class="sxs-lookup"><span data-stu-id="40f25-126">The **CIM\_ClusterServiceAccessBySAP** class is derived from [**CIM\_ServiceAccessBySAP**](cim-serviceaccessbysap.md).</span></span>

<span data-ttu-id="40f25-127">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="40f25-127">WMI does not implement this class.</span></span>

<span data-ttu-id="40f25-128">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="40f25-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="40f25-129">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="40f25-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="40f25-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="40f25-130">Requirements</span></span>



| <span data-ttu-id="40f25-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="40f25-131">Requirement</span></span> | <span data-ttu-id="40f25-132">Valore</span><span class="sxs-lookup"><span data-stu-id="40f25-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="40f25-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="40f25-133">Minimum supported client</span></span><br/> | <span data-ttu-id="40f25-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="40f25-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="40f25-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="40f25-135">Minimum supported server</span></span><br/> | <span data-ttu-id="40f25-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="40f25-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="40f25-137">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="40f25-137">Namespace</span></span><br/>                | <span data-ttu-id="40f25-138">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="40f25-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="40f25-139">MOF</span><span class="sxs-lookup"><span data-stu-id="40f25-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="40f25-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="40f25-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="40f25-141">DLL</span><span class="sxs-lookup"><span data-stu-id="40f25-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="40f25-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40f25-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40f25-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="40f25-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40f25-144">**\_SERVICEACCESSBYSAP CIM**</span><span class="sxs-lookup"><span data-stu-id="40f25-144">**CIM\_ServiceAccessBySAP**</span></span>](cim-serviceaccessbysap.md)
</dt> </dl>

 

