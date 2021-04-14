---
description: L' \_ associazione CIM RelatedStatistics rappresenta gerarchie e dipendenze di \_ classi CIM StatisticalInformation correlate.
ms.assetid: f5cea01d-7854-4ad4-a89e-db0ce9f4a83f
ms.tgt_platform: multiple
title: Classe CIM_RelatedStatistics
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RelatedStatistics
- CIM_RelatedStatistics.RelatedStats
- CIM_RelatedStatistics.Stats
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 01fb70535a4ae8f84d637cf92a06eee4fe318a49
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523114"
---
# <a name="cim_relatedstatistics-class"></a><span data-ttu-id="99532-103">CIM \_ RelatedStatistics (classe)</span><span class="sxs-lookup"><span data-stu-id="99532-103">CIM\_RelatedStatistics class</span></span>

<span data-ttu-id="99532-104">L'associazione **CIM \_ RelatedStatistics** rappresenta gerarchie e dipendenze di classi [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md) correlate.</span><span class="sxs-lookup"><span data-stu-id="99532-104">The **CIM\_RelatedStatistics** association represents hierarchies and dependencies of related [**CIM\_StatisticalInformation**](cim-statisticalinformation.md) classes.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="99532-105">Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI.</span><span class="sxs-lookup"><span data-stu-id="99532-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="99532-106">Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="99532-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="99532-107">La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="99532-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="99532-108">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="99532-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="99532-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="99532-109">Syntax</span></span>

``` syntax
[Abstract, Association, UUID("{956597A4-7D80-11D2-AAD3-006008C78BC7}"), AMENDMENT]
class CIM_RelatedStatistics
{
  CIM_StatisticalInformation REF RelatedStats;
  CIM_StatisticalInformation REF Stats;
};
```

## <a name="members"></a><span data-ttu-id="99532-110">Members</span><span class="sxs-lookup"><span data-stu-id="99532-110">Members</span></span>

<span data-ttu-id="99532-111">La classe **CIM \_ RelatedStatistics** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="99532-111">The **CIM\_RelatedStatistics** class has these types of members:</span></span>

-   [<span data-ttu-id="99532-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="99532-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="99532-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="99532-113">Properties</span></span>

<span data-ttu-id="99532-114">La classe **CIM \_ RelatedStatistics** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="99532-114">The **CIM\_RelatedStatistics** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="99532-115">**RelatedStats**</span><span class="sxs-lookup"><span data-stu-id="99532-115">**RelatedStats**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="99532-116">Tipo di dati: **CIM \_ StatisticalInformation**</span><span class="sxs-lookup"><span data-stu-id="99532-116">Data type: **CIM\_StatisticalInformation**</span></span>
</dt> <dt>

<span data-ttu-id="99532-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="99532-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="99532-118">Riferimento alle statistiche o alle metriche correlate.</span><span class="sxs-lookup"><span data-stu-id="99532-118">Reference to the related statistics or metrics.</span></span>

</dd> <dt>

<span data-ttu-id="99532-119">**Statistiche**</span><span class="sxs-lookup"><span data-stu-id="99532-119">**Stats**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="99532-120">Tipo di dati: **CIM \_ StatisticalInformation**</span><span class="sxs-lookup"><span data-stu-id="99532-120">Data type: **CIM\_StatisticalInformation**</span></span>
</dt> <dt>

<span data-ttu-id="99532-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="99532-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="99532-122">Riferimento all'oggetto o alle informazioni statistici.</span><span class="sxs-lookup"><span data-stu-id="99532-122">Reference to the statistic information or object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="99532-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="99532-123">Remarks</span></span>

<span data-ttu-id="99532-124">WMI non implementa questa classe.</span><span class="sxs-lookup"><span data-stu-id="99532-124">WMI does not implement this class.</span></span>

<span data-ttu-id="99532-125">Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF.</span><span class="sxs-lookup"><span data-stu-id="99532-125">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="99532-126">Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="99532-126">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="99532-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="99532-127">Requirements</span></span>



| <span data-ttu-id="99532-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="99532-128">Requirement</span></span> | <span data-ttu-id="99532-129">Valore</span><span class="sxs-lookup"><span data-stu-id="99532-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="99532-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="99532-130">Minimum supported client</span></span><br/> | <span data-ttu-id="99532-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="99532-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="99532-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="99532-132">Minimum supported server</span></span><br/> | <span data-ttu-id="99532-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="99532-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="99532-134">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="99532-134">Namespace</span></span><br/>                | <span data-ttu-id="99532-135">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="99532-135">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="99532-136">MOF</span><span class="sxs-lookup"><span data-stu-id="99532-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="99532-137"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="99532-137"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="99532-138">DLL</span><span class="sxs-lookup"><span data-stu-id="99532-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="99532-139"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="99532-139"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




