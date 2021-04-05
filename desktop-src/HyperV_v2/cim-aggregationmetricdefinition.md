---
description: Rappresenta la definizione di una metrica derivata da un altro valore della metrica. Un \_ oggetto AGGREGATIONMETRICDEFINITION CIM deve essere associato agli \_ oggetti gestiti di CIM a cui si applica.
ms.assetid: 0059bfd6-ecf3-41f0-be6b-0ce46dfbbb18
title: Classe CIM_AggregationMetricDefinition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AggregationMetricDefinition
- CIM_AggregationMetricDefinition.ChangeType
- CIM_AggregationMetricDefinition.SimpleFunction
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9a84eed5a725ebff3b39ca92bab530ef90cfca58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755447"
---
# <a name="cim_aggregationmetricdefinition-class"></a><span data-ttu-id="0b2b2-104">CIM \_ AggregationMetricDefinition (classe)</span><span class="sxs-lookup"><span data-stu-id="0b2b2-104">CIM\_AggregationMetricDefinition class</span></span>

<span data-ttu-id="0b2b2-105">Rappresenta la definizione di una metrica derivata da un altro valore della metrica.</span><span class="sxs-lookup"><span data-stu-id="0b2b2-105">Represents the definition of a metric that is derived from another metric value.</span></span> <span data-ttu-id="0b2b2-106">Un **oggetto \_ AggregationMetricDefinition CIM** deve essere associato agli oggetti **\_ gestiti di CIM** a cui si applica.</span><span class="sxs-lookup"><span data-stu-id="0b2b2-106">A **CIM\_AggregationMetricDefinition** object should be associated with the **CIM\_ManagedElement** objects to which it applies.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b2b2-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0b2b2-107">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_AggregationMetricDefinition : CIM_BaseMetricDefinition
{
  uint16 ChangeType = 5;
  uint16 SimpleFunction;
};
```

## <a name="members"></a><span data-ttu-id="0b2b2-108">Members</span><span class="sxs-lookup"><span data-stu-id="0b2b2-108">Members</span></span>

<span data-ttu-id="0b2b2-109">La classe **CIM \_ AggregationMetricDefinition** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="0b2b2-109">The **CIM\_AggregationMetricDefinition** class has these types of members:</span></span>

-   [<span data-ttu-id="0b2b2-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0b2b2-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0b2b2-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0b2b2-111">Properties</span></span>

<span data-ttu-id="0b2b2-112">La classe **CIM \_ AggregationMetricDefinition** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="0b2b2-112">The **CIM\_AggregationMetricDefinition** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0b2b2-113">**ChangeType**</span><span class="sxs-lookup"><span data-stu-id="0b2b2-113">**ChangeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b2b2-114">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0b2b2-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0b2b2-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b2b2-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b2b2-116">Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ChangeType"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AggregationMetricDefinition**.**Uncontinuous**")</span><span class="sxs-lookup"><span data-stu-id="0b2b2-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ChangeType"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AggregationMetricDefinition**.**IsContinuous**")</span></span>
</dt> </dl>

<span data-ttu-id="0b2b2-117">Indica il modo in cui il valore della metrica cambia usando gli attributi comuni, ad esempio la modifica della direzione, i valori minimo e massimo e la semantica di wrapping.</span><span class="sxs-lookup"><span data-stu-id="0b2b2-117">Indicates how the metric value changes using common attributes such as direction change, minimum and maximum values, and wrapping semantics.</span></span>

<dt>

<span id="Simple_Function"></span><span id="simple_function"></span><span id="SIMPLE_FUNCTION"></span>

<span data-ttu-id="0b2b2-118">**Funzione Simple** (5)</span><span class="sxs-lookup"><span data-stu-id="0b2b2-118">**Simple Function** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="0b2b2-119">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="0b2b2-119">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="0b2b2-120">**Fornitore riservato** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="0b2b2-120">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0b2b2-121">**SimpleFunction**</span><span class="sxs-lookup"><span data-stu-id="0b2b2-121">**SimpleFunction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b2b2-122">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0b2b2-122">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0b2b2-123">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="0b2b2-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0b2b2-124">Calcolo di base eseguito su una metrica sottostante per giungere al valore di questa metrica derivata.</span><span class="sxs-lookup"><span data-stu-id="0b2b2-124">The basic computation performed on an underlying metric to arrive at the value of this derived metric.</span></span> <span data-ttu-id="0b2b2-125">Questa proprietà è **null** se la proprietà **ChangeType** ha un valore diverso da "5" (funzione semplice).</span><span class="sxs-lookup"><span data-stu-id="0b2b2-125">This property is **NULL** when the **ChangeType** property has a value other than "5" (Simple Function).</span></span>

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="0b2b2-126"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="0b2b2-126"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>

<span data-ttu-id="0b2b2-127"><span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>**Minimo** (2)</span><span class="sxs-lookup"><span data-stu-id="0b2b2-127"><span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>**Minimum** (2)</span></span>


</dt> <dd>

<span data-ttu-id="0b2b2-128">La metrica indica il valore più basso rilevato per l'entità monitorata associata.</span><span class="sxs-lookup"><span data-stu-id="0b2b2-128">The metric reports the lowest value detected for the associated monitored entity.</span></span> <span data-ttu-id="0b2b2-129">Questa operazione è nota anche come limite minimo.</span><span class="sxs-lookup"><span data-stu-id="0b2b2-129">This is also known as a low watermark.</span></span>

</dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

<span data-ttu-id="0b2b2-130"><span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Massimo** (3)</span><span class="sxs-lookup"><span data-stu-id="0b2b2-130"><span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Maximum** (3)</span></span>


</dt> <dd>

<span data-ttu-id="0b2b2-131">La metrica indica il valore massimo rilevato per l'entità monitorata associata.</span><span class="sxs-lookup"><span data-stu-id="0b2b2-131">The metric reports the maximum value detected for the associated monitored entity.</span></span> <span data-ttu-id="0b2b2-132">Questa operazione è nota anche come limite massimo.</span><span class="sxs-lookup"><span data-stu-id="0b2b2-132">This is also known as a high watermark.</span></span>

</dd> <dt>

<span id="Average"></span><span id="average"></span><span id="AVERAGE"></span>

<span data-ttu-id="0b2b2-133"><span id="Average"></span><span id="average"></span><span id="AVERAGE"></span>**Media** (4)</span><span class="sxs-lookup"><span data-stu-id="0b2b2-133"><span id="Average"></span><span id="average"></span><span id="AVERAGE"></span>**Average** (4)</span></span>


</dt> <dd>

<span data-ttu-id="0b2b2-134">La metrica indica il valore medio dei valori delle metriche sottostanti.</span><span class="sxs-lookup"><span data-stu-id="0b2b2-134">The metric reports the average value of the underlying metric values.</span></span>

</dd> <dt>

<span id="Median"></span><span id="median"></span><span id="MEDIAN"></span>

<span data-ttu-id="0b2b2-135"><span id="Median"></span><span id="median"></span><span id="MEDIAN"></span>**Mediana** (5)</span><span class="sxs-lookup"><span data-stu-id="0b2b2-135"><span id="Median"></span><span id="median"></span><span id="MEDIAN"></span>**Median** (5)</span></span>


</dt> <dd>

<span data-ttu-id="0b2b2-136">La metrica indica il valore mediano dei valori delle metriche sottostanti.</span><span class="sxs-lookup"><span data-stu-id="0b2b2-136">The metric reports the median value of the underlying metric values.</span></span>

</dd> <dt>

<span id="Mode"></span><span id="mode"></span><span id="MODE"></span>

<span data-ttu-id="0b2b2-137"><span id="Mode"></span><span id="mode"></span><span id="MODE"></span>**Modalità** (6)</span><span class="sxs-lookup"><span data-stu-id="0b2b2-137"><span id="Mode"></span><span id="mode"></span><span id="MODE"></span>**Mode** (6)</span></span>


</dt> <dd>

<span data-ttu-id="0b2b2-138">la metrica indica il valore modale dei valori delle metriche sottostanti.</span><span class="sxs-lookup"><span data-stu-id="0b2b2-138">the metric reports the modal value of the underlying metric values.</span></span>

</dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="0b2b2-139"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornitore riservato** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="0b2b2-139"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="0b2b2-140"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="0b2b2-140"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="0b2b2-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0b2b2-141">Requirements</span></span>



| <span data-ttu-id="0b2b2-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b2b2-142">Requirement</span></span> | <span data-ttu-id="0b2b2-143">Valore</span><span class="sxs-lookup"><span data-stu-id="0b2b2-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b2b2-144">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0b2b2-144">Minimum supported client</span></span><br/> | <span data-ttu-id="0b2b2-145">Windows 8</span><span class="sxs-lookup"><span data-stu-id="0b2b2-145">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="0b2b2-146">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0b2b2-146">Minimum supported server</span></span><br/> | <span data-ttu-id="0b2b2-147">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0b2b2-147">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="0b2b2-148">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0b2b2-148">Namespace</span></span><br/>                | <span data-ttu-id="0b2b2-149">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="0b2b2-149">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="0b2b2-150">MOF</span><span class="sxs-lookup"><span data-stu-id="0b2b2-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0b2b2-151"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0b2b2-151"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0b2b2-152">DLL</span><span class="sxs-lookup"><span data-stu-id="0b2b2-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b2b2-153"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0b2b2-153"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0b2b2-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0b2b2-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b2b2-155">**\_BASEMETRICDEFINITION CIM**</span><span class="sxs-lookup"><span data-stu-id="0b2b2-155">**CIM\_BaseMetricDefinition**</span></span>](cim-basemetricdefinition.md)
</dt> </dl>

 

