---
description: La \_ classe CIM SAPSAPDependency è un'associazione tra due punti di accesso al servizio (SAP), che indica che il secondo SAP è necessario affinché il primo SAP si connetta con il servizio.
ms.assetid: ba5f47d9-ebe5-4dcb-8a6d-0974acf67385
ms.tgt_platform: multiple
title: Classe CIM_SAPSAPDependency (provider WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SAPSAPDependency
- CIM_SAPSAPDependency.Dependent
- CIM_SAPSAPDependency.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b75cb397120ac2d4af041187f38f826e6b56be11
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966022"
---
# <a name="cim_sapsapdependency-class-cimwin32-wmi-providers"></a><span data-ttu-id="3bd87-103">Classe CIM_SAPSAPDependency (provider WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="3bd87-103">CIM_SAPSAPDependency class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="3bd87-104">La classe **CIM \_ SAPSAPDependency** è un'associazione tra due punti di accesso al servizio (SAP), che indica che il secondo SAP è necessario affinché il primo SAP si connetta con il servizio.</span><span class="sxs-lookup"><span data-stu-id="3bd87-104">The **CIM\_SAPSAPDependency** class is an association between two service access points (SAPs), which indicates that the second SAP is required for the first SAP to connect with its service.</span></span> <span data-ttu-id="3bd87-105">Ad esempio, per stampare su una stampante di rete, i punti di accesso alla stampante locale devono usare i succhi di rete sottostanti o gli endpoint del protocollo per inviare la richiesta di stampa.</span><span class="sxs-lookup"><span data-stu-id="3bd87-105">For example, to print on a network printer, local printer access points must use underlying network-related SAPs, or protocol endpoints, to send the print request.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3bd87-106">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="3bd87-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="3bd87-107">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="3bd87-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="3bd87-108">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="3bd87-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="3bd87-109">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="3bd87-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3bd87-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3bd87-110">Syntax</span></span>

``` syntax
[UUID("{422D175A-E3D5-11d2-8601-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_SAPSAPDependency : CIM_Dependency
{
  CIM_ServiceAccessPoint REF Dependent;
  CIM_ServiceAccessPoint REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="3bd87-111">Members</span><span class="sxs-lookup"><span data-stu-id="3bd87-111">Members</span></span>

<span data-ttu-id="3bd87-112">La classe **CIM \_ SAPSAPDependency** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="3bd87-112">The **CIM\_SAPSAPDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="3bd87-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3bd87-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3bd87-114">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3bd87-114">Properties</span></span>

<span data-ttu-id="3bd87-115">La classe **CIM \_ SAPSAPDependency** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="3bd87-115">The **CIM\_SAPSAPDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3bd87-116">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="3bd87-116">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3bd87-117">Tipo di dati: **CIM \_ serviceAccessPoint**</span><span class="sxs-lookup"><span data-stu-id="3bd87-117">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="3bd87-118">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3bd87-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3bd87-119">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="3bd87-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="3bd87-120">Un [**\_ serviceAccessPoint CIM**](cim-serviceaccesspoint.md) che descrive il punto di accesso al servizio richiesto.</span><span class="sxs-lookup"><span data-stu-id="3bd87-120">A [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) that describes the required service access point.</span></span>

</dd> <dt>

<span data-ttu-id="3bd87-121">**Dipendente**</span><span class="sxs-lookup"><span data-stu-id="3bd87-121">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3bd87-122">Tipo di dati: **CIM \_ serviceAccessPoint**</span><span class="sxs-lookup"><span data-stu-id="3bd87-122">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="3bd87-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="3bd87-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3bd87-124">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")</span><span class="sxs-lookup"><span data-stu-id="3bd87-124">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="3bd87-125">Un [**\_ serviceAccessPoint CIM**](cim-serviceaccesspoint.md) che descrive il punto di accesso del servizio che dipende da un SAP sottostante.</span><span class="sxs-lookup"><span data-stu-id="3bd87-125">A [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) that describes the service access point that is dependent on an underlying SAP.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3bd87-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="3bd87-126">Remarks</span></span>

<span data-ttu-id="3bd87-127">La classe **CIM \_ SAPSAPDependency** è derivata dalla [**\_ dipendenza CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="3bd87-127">The **CIM\_SAPSAPDependency** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="3bd87-128">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="3bd87-128">WMI does not implement this class.</span></span>

<span data-ttu-id="3bd87-129">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="3bd87-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="3bd87-130">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="3bd87-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="3bd87-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3bd87-131">Requirements</span></span>



| <span data-ttu-id="3bd87-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="3bd87-132">Requirement</span></span> | <span data-ttu-id="3bd87-133">Valore</span><span class="sxs-lookup"><span data-stu-id="3bd87-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3bd87-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3bd87-134">Minimum supported client</span></span><br/> | <span data-ttu-id="3bd87-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3bd87-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3bd87-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3bd87-136">Minimum supported server</span></span><br/> | <span data-ttu-id="3bd87-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3bd87-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3bd87-138">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="3bd87-138">Namespace</span></span><br/>                | <span data-ttu-id="3bd87-139">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="3bd87-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3bd87-140">MOF</span><span class="sxs-lookup"><span data-stu-id="3bd87-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3bd87-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3bd87-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3bd87-142">DLL</span><span class="sxs-lookup"><span data-stu-id="3bd87-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3bd87-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3bd87-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3bd87-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3bd87-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bd87-145">**\_Dipendenza CIM**</span><span class="sxs-lookup"><span data-stu-id="3bd87-145">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

