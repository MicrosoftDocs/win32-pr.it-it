---
description: Gestisce la metrica per gli elementi gestiti.
ms.assetid: df249d0c-960b-47d6-9590-f0fd08ddec18
title: Classe CIM_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 41c4ab5e947fe22434e38006c5169711701915a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312920"
---
# <a name="cim_metricservice-class"></a><span data-ttu-id="93b6b-103">CIM \_ MetricService (classe)</span><span class="sxs-lookup"><span data-stu-id="93b6b-103">CIM\_MetricService class</span></span>

<span data-ttu-id="93b6b-104">Gestisce la metrica per gli elementi gestiti.</span><span class="sxs-lookup"><span data-stu-id="93b6b-104">Manages metrics for managed elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="93b6b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="93b6b-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.23.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_MetricService : CIM_Service
{
};
```

## <a name="members"></a><span data-ttu-id="93b6b-106">Members</span><span class="sxs-lookup"><span data-stu-id="93b6b-106">Members</span></span>

<span data-ttu-id="93b6b-107">La classe **CIM \_ MetricService** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="93b6b-107">The **CIM\_MetricService** class has these types of members:</span></span>

-   [<span data-ttu-id="93b6b-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="93b6b-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="93b6b-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="93b6b-109">Methods</span></span>

<span data-ttu-id="93b6b-110">La classe **CIM \_ MetricService** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="93b6b-110">The **CIM\_MetricService** class has these methods.</span></span>



| <span data-ttu-id="93b6b-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="93b6b-111">Method</span></span>                                                                   | <span data-ttu-id="93b6b-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="93b6b-112">Description</span></span>                                                                                                                                                                         |
|:-------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="93b6b-113">**ControlMetrics**</span><span class="sxs-lookup"><span data-stu-id="93b6b-113">**ControlMetrics**</span></span>](cim-metricservice-controlmetrics.md)               | <span data-ttu-id="93b6b-114">Abilita e Disabilita la raccolta di metriche.</span><span class="sxs-lookup"><span data-stu-id="93b6b-114">Enables and disables the collection of metrics.</span></span><br/>                                                                                                                          |
| [<span data-ttu-id="93b6b-115">**ControlMetricsByClass**</span><span class="sxs-lookup"><span data-stu-id="93b6b-115">**ControlMetricsByClass**</span></span>](cim-metricservice-controlmetricsbyclass.md) | <span data-ttu-id="93b6b-116">Abilita e Disabilita la raccolta di metriche per una classe.</span><span class="sxs-lookup"><span data-stu-id="93b6b-116">Enables and disables the collection of metrics for a class.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="93b6b-117">**ControlSampleTimes**</span><span class="sxs-lookup"><span data-stu-id="93b6b-117">**ControlSampleTimes**</span></span>](cim-metricservice-controlsampletimes.md)       | <span data-ttu-id="93b6b-118">Specifica quando le metriche vengono raccolte.</span><span class="sxs-lookup"><span data-stu-id="93b6b-118">Specifies when metrics are gathered.</span></span><br/>                                                                                                                                     |
| [<span data-ttu-id="93b6b-119">**GetMetricValues**</span><span class="sxs-lookup"><span data-stu-id="93b6b-119">**GetMetricValues**</span></span>](cim-metricservice-getmetricvalues.md)             | <span data-ttu-id="93b6b-120">Recupera un elenco filtrato di valori di metrica.</span><span class="sxs-lookup"><span data-stu-id="93b6b-120">Retrieves a filtered list of metric values.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="93b6b-121">**ShowMetrics**</span><span class="sxs-lookup"><span data-stu-id="93b6b-121">**ShowMetrics**</span></span>](cim-metricservice-showmetrics.md)                     | <span data-ttu-id="93b6b-122">Indica se la raccolta di metriche è abilitata per gli elementi gestiti specificati e indica le metriche disponibili per la raccolta per ogni elemento gestito.</span><span class="sxs-lookup"><span data-stu-id="93b6b-122">Indicates whether metric collection is enabled for the specified managed elements, and indicates the metrics that are available for collection for each managed element.</span></span><br/> |
| [<span data-ttu-id="93b6b-123">**ShowMetricsByClass**</span><span class="sxs-lookup"><span data-stu-id="93b6b-123">**ShowMetricsByClass**</span></span>](cim-metricservice-showmetricsbyclass.md)       | <span data-ttu-id="93b6b-124">Indica le metriche disponibili per la raccolta per tutte le istanze di una classe CIM.</span><span class="sxs-lookup"><span data-stu-id="93b6b-124">Indicates which metrics are available for collection for all instances of a CIM class.</span></span><br/>                                                                                   |



 

## <a name="requirements"></a><span data-ttu-id="93b6b-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="93b6b-125">Requirements</span></span>



| <span data-ttu-id="93b6b-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="93b6b-126">Requirement</span></span> | <span data-ttu-id="93b6b-127">Valore</span><span class="sxs-lookup"><span data-stu-id="93b6b-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93b6b-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="93b6b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="93b6b-129">Windows 8</span><span class="sxs-lookup"><span data-stu-id="93b6b-129">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="93b6b-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="93b6b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="93b6b-131">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="93b6b-131">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="93b6b-132">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="93b6b-132">Namespace</span></span><br/>                | <span data-ttu-id="93b6b-133">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="93b6b-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="93b6b-134">MOF</span><span class="sxs-lookup"><span data-stu-id="93b6b-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="93b6b-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="93b6b-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="93b6b-136">DLL</span><span class="sxs-lookup"><span data-stu-id="93b6b-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93b6b-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="93b6b-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="93b6b-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="93b6b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93b6b-139">**\_Servizio CIM**</span><span class="sxs-lookup"><span data-stu-id="93b6b-139">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




