---
description: Descrive le funzionalità di un \_ oggetto METRICSERVICE CIM.
ms.assetid: 3b4da02f-5298-46d4-876c-404baca38c03
title: Classe CIM_MetricServiceCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricServiceCapabilities
- CIM_MetricServiceCapabilities.ControllableMetrics
- CIM_MetricServiceCapabilities.MetricsControlTypes
- CIM_MetricServiceCapabilities.ControllableManagedElements
- CIM_MetricServiceCapabilities.ManagedElementControlTypes
- CIM_MetricServiceCapabilities.SupportedMethods
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f878cb0e616cb710a33d350df866160fc0eebb83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313377"
---
# <a name="cim_metricservicecapabilities-class"></a><span data-ttu-id="fa543-103">CIM \_ MetricServiceCapabilities (classe)</span><span class="sxs-lookup"><span data-stu-id="fa543-103">CIM\_MetricServiceCapabilities class</span></span>

<span data-ttu-id="fa543-104">Descrive le funzionalità di un [**oggetto \_ MetricService CIM**](cim-metricservice.md) .</span><span class="sxs-lookup"><span data-stu-id="fa543-104">Describes the capabilities of a [**CIM\_MetricService**](cim-metricservice.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa543-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fa543-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Metrics::BaseMetrics"), AMENDMENT]
class CIM_MetricServiceCapabilities : CIM_EnabledLogicalElementCapabilities
{
  string ControllableMetrics[];
  uint16 MetricsControlTypes[];
  string ControllableManagedElements[];
  uint16 ManagedElementControlTypes[];
  uint16 SupportedMethods[];
};
```

## <a name="members"></a><span data-ttu-id="fa543-106">Members</span><span class="sxs-lookup"><span data-stu-id="fa543-106">Members</span></span>

<span data-ttu-id="fa543-107">La classe **CIM \_ MetricServiceCapabilities** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="fa543-107">The **CIM\_MetricServiceCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="fa543-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="fa543-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fa543-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="fa543-109">Properties</span></span>

<span data-ttu-id="fa543-110">La classe **CIM \_ MetricServiceCapabilities** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="fa543-110">The **CIM\_MetricServiceCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fa543-111">**ControllableManagedElements**</span><span class="sxs-lookup"><span data-stu-id="fa543-111">**ControllableManagedElements**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa543-112">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="fa543-112">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="fa543-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fa543-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa543-114">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ MetricServiceCapabilities**.**ManagedElementControlTypes**")</span><span class="sxs-lookup"><span data-stu-id="fa543-114">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_MetricServiceCapabilities**.**ManagedElementControlTypes**")</span></span>
</dt> </dl>

<span data-ttu-id="fa543-115">Matrice che contiene gli identificatori delle istanze di [**CIM \_ gestite**](cim-managedelement.md) che sono controllate dal servizio metrico.</span><span class="sxs-lookup"><span data-stu-id="fa543-115">An array that contains identifiers of the [**CIM\_ManagedElement**](cim-managedelement.md) instances that are controlled by the metric service.</span></span> <span data-ttu-id="fa543-116">Gli identificatori devono essere formattati come URI WBEM (Web-Based Enterprise Management).</span><span class="sxs-lookup"><span data-stu-id="fa543-116">The identifiers must be formatted as Web-Based Enterprise Management (WBEM) URIs.</span></span> <span data-ttu-id="fa543-117">Per usare questa proprietà, il servizio metrico deve supportare l'abilitazione o la disabilitazione di almeno una metrica definita per l'istanza **CIM \_ gestitaelement** .</span><span class="sxs-lookup"><span data-stu-id="fa543-117">In order to use this property, the metric service must support enabling or disabling at least one metric that is defined for the **CIM\_ManagedElement** instance.</span></span>

</dd> <dt>

<span data-ttu-id="fa543-118">**ControllableMetrics**</span><span class="sxs-lookup"><span data-stu-id="fa543-118">**ControllableMetrics**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa543-119">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="fa543-119">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="fa543-120">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fa543-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa543-121">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ MetricServiceCapabilities**.**MetricControlTypes**")</span><span class="sxs-lookup"><span data-stu-id="fa543-121">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_MetricServiceCapabilities**.**MetricControlTypes**")</span></span>
</dt> </dl>

<span data-ttu-id="fa543-122">Matrice contenente gli identificatori del [**\_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md) che definisce le metriche gestite dal servizio metrico.</span><span class="sxs-lookup"><span data-stu-id="fa543-122">An array that contains identifiers of the [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) that defines the metrics that are managed by the metric service.</span></span> <span data-ttu-id="fa543-123">Gli identificatori devono essere formattati come URI WBEM (Web-Based Enterprise Management).</span><span class="sxs-lookup"><span data-stu-id="fa543-123">The identifiers must be formatted as Web-Based Enterprise Management (WBEM) URIs.</span></span>

<span data-ttu-id="fa543-124">Per usare questa proprietà, un'istanza di [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) deve essere associata a un'istanza [**CIM \_ MetricService**](cim-metricservice.md) tramite la classe [**CIM \_ ServiceAffectsElement**](cim-serviceaffectselement.md) .</span><span class="sxs-lookup"><span data-stu-id="fa543-124">In order to use this property, a [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) instance must be associated with a [**CIM\_MetricService**](cim-metricservice.md) instance through the [**CIM\_ServiceAffectsElement**](cim-serviceaffectselement.md) class.</span></span> <span data-ttu-id="fa543-125">Il servizio metrico deve inoltre supportare l'abilitazione o la disabilitazione di almeno una metrica definita dall'istanza **CIM \_ BaseMetricDefinition** .</span><span class="sxs-lookup"><span data-stu-id="fa543-125">In addition the metric service must support enabling or disabling at least one metric that is defined by the **CIM\_BaseMetricDefinition** instance.</span></span>

</dd> <dt>

<span data-ttu-id="fa543-126">**ManagedElementControlTypes**</span><span class="sxs-lookup"><span data-stu-id="fa543-126">**ManagedElementControlTypes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa543-127">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fa543-127">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="fa543-128">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fa543-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa543-129">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ MetricServiceCapabilities**.**ControllableManagedElements**")</span><span class="sxs-lookup"><span data-stu-id="fa543-129">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_MetricServiceCapabilities**.**ControllableManagedElements**")</span></span>
</dt> </dl>

<span data-ttu-id="fa543-130">Matrice che indica i tipi di controllo supportati dal servizio metrico per gli elementi gestiti nella matrice **ControllableManagedElements** .</span><span class="sxs-lookup"><span data-stu-id="fa543-130">An array that indicates the control types that are supported by the metric service for the managed elements in the **ControllableManagedElements** array.</span></span> <span data-ttu-id="fa543-131">Questa matrice corrisponde alla matrice **ControllableManagedElements** .</span><span class="sxs-lookup"><span data-stu-id="fa543-131">This array corresponds to the **ControllableManagedElements** array.</span></span> <span data-ttu-id="fa543-132">I tipi di controllo in questa matrice sono associati alle metriche tramite la matrice **ControllableManagedElements** .</span><span class="sxs-lookup"><span data-stu-id="fa543-132">The control types in this array are associated with metrics through the **ControllableManagedElements** array.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fa543-133">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="fa543-133">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Discrete"></span><span id="discrete"></span><span id="DISCRETE"></span>

<span data-ttu-id="fa543-134">**Discreto** (2)</span><span class="sxs-lookup"><span data-stu-id="fa543-134">**Discrete** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Bulk"></span><span id="bulk"></span><span id="BULK"></span>

<span data-ttu-id="fa543-135">**Bulk** (3)</span><span class="sxs-lookup"><span data-stu-id="fa543-135">**Bulk** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Both"></span><span id="both"></span><span id="BOTH"></span>

<span data-ttu-id="fa543-136">**Entrambi** (4)</span><span class="sxs-lookup"><span data-stu-id="fa543-136">**Both** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="fa543-137">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="fa543-137">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span data-ttu-id="fa543-138">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="fa543-138">**Vendor Specific** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="fa543-139">**MetricsControlTypes**</span><span class="sxs-lookup"><span data-stu-id="fa543-139">**MetricsControlTypes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa543-140">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fa543-140">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="fa543-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fa543-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fa543-142">Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ MetricServiceCapabilities**.**ControllableMetrics**")</span><span class="sxs-lookup"><span data-stu-id="fa543-142">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_MetricServiceCapabilities**.**ControllableMetrics**")</span></span>
</dt> </dl>

<span data-ttu-id="fa543-143">Matrice che indica i tipi di controllo supportati dal servizio metrico.</span><span class="sxs-lookup"><span data-stu-id="fa543-143">An array that indicates the control types that are supported by the metric service.</span></span> <span data-ttu-id="fa543-144">Questa matrice corrisponde alla matrice **ControllableMetrics** .</span><span class="sxs-lookup"><span data-stu-id="fa543-144">This array corresponds to the **ControllableMetrics** array.</span></span> <span data-ttu-id="fa543-145">I tipi di controllo in questa matrice sono associati alle metriche tramite la matrice **ControllableMetrics** .</span><span class="sxs-lookup"><span data-stu-id="fa543-145">The control types in this array are associated with metrics through the **ControllableMetrics** array.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="fa543-146">**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="fa543-146">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Discrete"></span><span id="discrete"></span><span id="DISCRETE"></span>

<span data-ttu-id="fa543-147">**Discreto** (2)</span><span class="sxs-lookup"><span data-stu-id="fa543-147">**Discrete** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Bulk"></span><span id="bulk"></span><span id="BULK"></span>

<span data-ttu-id="fa543-148">**Bulk** (3)</span><span class="sxs-lookup"><span data-stu-id="fa543-148">**Bulk** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Both"></span><span id="both"></span><span id="BOTH"></span>

<span data-ttu-id="fa543-149">**Entrambi** (4)</span><span class="sxs-lookup"><span data-stu-id="fa543-149">**Both** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="fa543-150">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="fa543-150">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span data-ttu-id="fa543-151">**Specifico del fornitore** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="fa543-151">**Vendor Specific** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="fa543-152">**SupportedMethods**</span><span class="sxs-lookup"><span data-stu-id="fa543-152">**SupportedMethods**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fa543-153">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fa543-153">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="fa543-154">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="fa543-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fa543-155">Matrice che contiene i nomi dei metodi supportati dal servizio metrico.</span><span class="sxs-lookup"><span data-stu-id="fa543-155">An array that contains names of methods that are supported by the metric service.</span></span>

<dt>

<span id="ControlMetrics"></span><span id="controlmetrics"></span><span id="CONTROLMETRICS"></span>

<span data-ttu-id="fa543-156">**ControlMetrics** (2)</span><span class="sxs-lookup"><span data-stu-id="fa543-156">**ControlMetrics** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="ControlMetricsByClass"></span><span id="controlmetricsbyclass"></span><span id="CONTROLMETRICSBYCLASS"></span>

<span data-ttu-id="fa543-157">**ControlMetricsByClass** (3)</span><span class="sxs-lookup"><span data-stu-id="fa543-157">**ControlMetricsByClass** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ShowMetrics"></span><span id="showmetrics"></span><span id="SHOWMETRICS"></span>

<span data-ttu-id="fa543-158">**ShowMetrics** (4)</span><span class="sxs-lookup"><span data-stu-id="fa543-158">**ShowMetrics** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="ShowMetricsByClass"></span><span id="showmetricsbyclass"></span><span id="SHOWMETRICSBYCLASS"></span>

<span data-ttu-id="fa543-159">**ShowMetricsByClass** (5)</span><span class="sxs-lookup"><span data-stu-id="fa543-159">**ShowMetricsByClass** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="GetMetricValues"></span><span id="getmetricvalues"></span><span id="GETMETRICVALUES"></span>

<span data-ttu-id="fa543-160">**GetMetricValues** (6)</span><span class="sxs-lookup"><span data-stu-id="fa543-160">**GetMetricValues** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="ControlSampleTimes"></span><span id="controlsampletimes"></span><span id="CONTROLSAMPLETIMES"></span>

<span data-ttu-id="fa543-161">**ControlSampleTimes** (7)</span><span class="sxs-lookup"><span data-stu-id="fa543-161">**ControlSampleTimes** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="fa543-162">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="fa543-162">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span data-ttu-id="fa543-163">**Specifico del fornitore** (0x8000..)</span><span class="sxs-lookup"><span data-stu-id="fa543-163">**Vendor Specific** (0x8000..)</span></span>


<span data-ttu-id="fa543-164"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="fa543-164"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="fa543-165">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fa543-165">Requirements</span></span>



| <span data-ttu-id="fa543-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa543-166">Requirement</span></span> | <span data-ttu-id="fa543-167">Valore</span><span class="sxs-lookup"><span data-stu-id="fa543-167">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa543-168">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fa543-168">Minimum supported client</span></span><br/> | <span data-ttu-id="fa543-169">Windows 8</span><span class="sxs-lookup"><span data-stu-id="fa543-169">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="fa543-170">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fa543-170">Minimum supported server</span></span><br/> | <span data-ttu-id="fa543-171">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fa543-171">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="fa543-172">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="fa543-172">Namespace</span></span><br/>                | <span data-ttu-id="fa543-173">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="fa543-173">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="fa543-174">MOF</span><span class="sxs-lookup"><span data-stu-id="fa543-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fa543-175"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fa543-175"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fa543-176">DLL</span><span class="sxs-lookup"><span data-stu-id="fa543-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa543-177"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fa543-177"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fa543-178">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fa543-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa543-179">**\_ENABLEDLOGICALELEMENTCAPABILITIES CIM**</span><span class="sxs-lookup"><span data-stu-id="fa543-179">**CIM\_EnabledLogicalElementCapabilities**</span></span>](cim-enabledlogicalelementcapabilities.md)
</dt> </dl>

 

