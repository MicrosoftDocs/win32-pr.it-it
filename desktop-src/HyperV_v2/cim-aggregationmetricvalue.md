---
description: Rappresenta il valore dell'istanza di una metrica definita da un'istanza di CIM \_ AggregationMetricDefinition.
ms.assetid: 663ef18a-0238-416f-9682-8809b271b4fc
title: Classe CIM_AggregationMetricValue
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AggregationMetricValue
- CIM_AggregationMetricValue.AggregationTimeStamp
- CIM_AggregationMetricValue.AggregationDuration
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0af264b66838e7c039ef3f99a4f365ebab55c293
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310587"
---
# <a name="cim_aggregationmetricvalue-class"></a><span data-ttu-id="f312f-103">CIM \_ AggregationMetricValue (classe)</span><span class="sxs-lookup"><span data-stu-id="f312f-103">CIM\_AggregationMetricValue class</span></span>

<span data-ttu-id="f312f-104">Rappresenta il valore dell'istanza di una metrica definita da un'istanza di **CIM \_ AggregationMetricDefinition**.</span><span class="sxs-lookup"><span data-stu-id="f312f-104">Represents the instance value of a metric defined by an instance of **CIM\_AggregationMetricDefinition**.</span></span>

## <a name="syntax"></a><span data-ttu-id="f312f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f312f-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_AggregationMetricValue : CIM_BaseMetricValue
{
  datetime AggregationTimeStamp;
  datetime AggregationDuration;
};
```

## <a name="members"></a><span data-ttu-id="f312f-106">Members</span><span class="sxs-lookup"><span data-stu-id="f312f-106">Members</span></span>

<span data-ttu-id="f312f-107">La classe **CIM \_ AggregationMetricValue** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="f312f-107">The **CIM\_AggregationMetricValue** class has these types of members:</span></span>

-   [<span data-ttu-id="f312f-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f312f-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f312f-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f312f-109">Properties</span></span>

<span data-ttu-id="f312f-110">La classe **CIM \_ AggregationMetricValue** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="f312f-110">The **CIM\_AggregationMetricValue** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f312f-111">**AggregationDuration**</span><span class="sxs-lookup"><span data-stu-id="f312f-111">**AggregationDuration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f312f-112">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f312f-112">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f312f-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f312f-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f312f-114">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AggregationMetricValue**.**AggregationTimeStamp**")</span><span class="sxs-lookup"><span data-stu-id="f312f-114">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AggregationMetricValue**.**AggregationTimeStamp**")</span></span>
</dt> </dl>

<span data-ttu-id="f312f-115">Rappresenta la durata dell'intervallo di tempo in cui è stata calcolata l'aggregazione.</span><span class="sxs-lookup"><span data-stu-id="f312f-115">Represents the time duration over which the aggregation was computed.</span></span> <span data-ttu-id="f312f-116">L'inizio di un intervallo di monitoraggio sul quale viene applicata la funzione di aggregazione viene determinato sottraendo il valore **AggregationDuration** dal valore di **AggregationTimestamp** .</span><span class="sxs-lookup"><span data-stu-id="f312f-116">The start of a monitoring interval over which the aggregation function is applied is determined by subtracting the **AggregationDuration** value from the **AggregationTimestamp** value.</span></span>

</dd> <dt>

<span data-ttu-id="f312f-117">**AggregationTimeStamp**</span><span class="sxs-lookup"><span data-stu-id="f312f-117">**AggregationTimeStamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f312f-118">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f312f-118">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f312f-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="f312f-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f312f-120">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AggregationMetricValue**.**Durata**")</span><span class="sxs-lookup"><span data-stu-id="f312f-120">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AggregationMetricValue**.**Duration**")</span></span>
</dt> </dl>

<span data-ttu-id="f312f-121">Ora di applicazione della funzione di aggregazione per determinare il valore dell'istanza della metrica.</span><span class="sxs-lookup"><span data-stu-id="f312f-121">The time when the aggregation function was applied to determine the value of the metric instance.</span></span> <span data-ttu-id="f312f-122">Questa operazione è diversa dal momento in cui viene creata l'istanza.</span><span class="sxs-lookup"><span data-stu-id="f312f-122">This is different from the time when the instance is created.</span></span> <span data-ttu-id="f312f-123">Il valore **AggregationTimeStamp** cambia ogni volta che viene applicata la funzione di aggregazione per calcolare il valore.</span><span class="sxs-lookup"><span data-stu-id="f312f-123">The **AggregationTimeStamp** value changes whenever the aggregation function is applied to calculate the value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f312f-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f312f-124">Requirements</span></span>



| <span data-ttu-id="f312f-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="f312f-125">Requirement</span></span> | <span data-ttu-id="f312f-126">Valore</span><span class="sxs-lookup"><span data-stu-id="f312f-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f312f-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f312f-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f312f-128">Windows 8</span><span class="sxs-lookup"><span data-stu-id="f312f-128">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="f312f-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f312f-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f312f-130">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f312f-130">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="f312f-131">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f312f-131">Namespace</span></span><br/>                | <span data-ttu-id="f312f-132">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="f312f-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f312f-133">MOF</span><span class="sxs-lookup"><span data-stu-id="f312f-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f312f-134"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f312f-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f312f-135">DLL</span><span class="sxs-lookup"><span data-stu-id="f312f-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f312f-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f312f-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f312f-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f312f-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f312f-138">**\_BASEMETRICVALUE CIM**</span><span class="sxs-lookup"><span data-stu-id="f312f-138">**CIM\_BaseMetricValue**</span></span>](cim-basemetricvalue.md)
</dt> </dl>

 

