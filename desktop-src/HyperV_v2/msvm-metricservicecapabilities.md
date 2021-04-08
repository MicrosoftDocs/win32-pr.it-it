---
description: Descrive le funzionalità dell'istanza MetricService di MSVM associata \_ .
ms.assetid: 4E24D675-8265-4B5E-9551-550510B138FE
title: Classe Msvm_MetricServiceCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricServiceCapabilities
- Msvm_MetricServiceCapabilities.InstanceID
- Msvm_MetricServiceCapabilities.Caption
- Msvm_MetricServiceCapabilities.Description
- Msvm_MetricServiceCapabilities.ElementName
- Msvm_MetricServiceCapabilities.ElementNameEditSupported
- Msvm_MetricServiceCapabilities.MaxElementNameLen
- Msvm_MetricServiceCapabilities.RequestedStatesSupported
- Msvm_MetricServiceCapabilities.ElementNameMask
- Msvm_MetricServiceCapabilities.ControllableMetrics
- Msvm_MetricServiceCapabilities.MetricsControlTypes
- Msvm_MetricServiceCapabilities.ControllableManagedElements
- Msvm_MetricServiceCapabilities.ManagedElementControlTypes
- Msvm_MetricServiceCapabilities.SupportedMethods
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 635e153d3184e74ea581a045e3d6d54a5fea199f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885145"
---
# <a name="msvm_metricservicecapabilities-class"></a><span data-ttu-id="03a98-103">\_Classe MSVM MetricServiceCapabilities</span><span class="sxs-lookup"><span data-stu-id="03a98-103">Msvm\_MetricServiceCapabilities class</span></span>

<span data-ttu-id="03a98-104">Descrive le funzionalità dell'istanza [**\_ MetricService di MSVM**](msvm-metricservice.md) associata.</span><span class="sxs-lookup"><span data-stu-id="03a98-104">Describes the capabilities of the associated [**Msvm\_MetricService**](msvm-metricservice.md) instance.</span></span>

<span data-ttu-id="03a98-105">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="03a98-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="03a98-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="03a98-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MetricServiceCapabilities : CIM_MetricServiceCapabilities
{
  string  InstanceID;
  string  Caption = "Hyper-V Metric Service Capabilities";
  string  Description = "Defines Hyper-V Metric Service Capabilities";
  string  ElementName = "Hyper-V Metric Service Capabilities";
  boolean ElementNameEditSupported;
  unit16  MaxElementNameLen;
  unit16  RequestedStatesSupported[];
  string  ElementNameMask;
  string  ControllableMetrics[];
  uint16  MetricsControlTypes[];
  string  ControllableManagedElements[];
  uint16  ManagedElementControlTypes[];
  uint16  SupportedMethods[];
};
```

## <a name="members"></a><span data-ttu-id="03a98-107">Members</span><span class="sxs-lookup"><span data-stu-id="03a98-107">Members</span></span>

<span data-ttu-id="03a98-108">La **classe \_ MetricServiceCapabilities di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="03a98-108">The **Msvm\_MetricServiceCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="03a98-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="03a98-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="03a98-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="03a98-110">Properties</span></span>

<span data-ttu-id="03a98-111">La **classe \_ MetricServiceCapabilities di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="03a98-111">The **Msvm\_MetricServiceCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="03a98-112">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="03a98-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03a98-113">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="03a98-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03a98-114">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="03a98-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03a98-115">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="03a98-115">A short description of the object.</span></span> <span data-ttu-id="03a98-116">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "funzionalità del servizio metrica Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="03a98-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Metric Service Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="03a98-117">**ControllableManagedElements**</span><span class="sxs-lookup"><span data-stu-id="03a98-117">**ControllableManagedElements**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03a98-118">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="03a98-118">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="03a98-119">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="03a98-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03a98-120">Qualificatori: **arrayType** ("indicizzato")</span><span class="sxs-lookup"><span data-stu-id="03a98-120">Qualifiers: **ArrayType** ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="03a98-121">Identifica le istanze di [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) che possono essere controllate dall'istanza **\_ MetricService CIM** associata.</span><span class="sxs-lookup"><span data-stu-id="03a98-121">Identifies the instances of [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) that can be controlled by the associated **CIM\_MetricService** instance.</span></span> <span data-ttu-id="03a98-122">Se questa proprietà è **null**, è possibile controllare tutti gli elementi.</span><span class="sxs-lookup"><span data-stu-id="03a98-122">If this property is **Null**, all elements can be controlled.</span></span> <span data-ttu-id="03a98-123">Questa proprietà viene ereditata da **CIM \_ MetricServiceCapabilities**.</span><span class="sxs-lookup"><span data-stu-id="03a98-123">This property is inherited from **CIM\_MetricServiceCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="03a98-124">**ControllableMetrics**</span><span class="sxs-lookup"><span data-stu-id="03a98-124">**ControllableMetrics**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03a98-125">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="03a98-125">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="03a98-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="03a98-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03a98-127">Qualificatori: **arrayType** ("indicizzato")</span><span class="sxs-lookup"><span data-stu-id="03a98-127">Qualifiers: **ArrayType** ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="03a98-128">Identifica le istanze di **\_ BaseMetricDefinition CIM** che possono essere controllate dall'istanza **\_ MetricService CIM** associata.</span><span class="sxs-lookup"><span data-stu-id="03a98-128">Identifies the instances of **CIM\_BaseMetricDefinition** that can be controlled by the associated **CIM\_MetricService** instance.</span></span> <span data-ttu-id="03a98-129">Se questa proprietà è **null**, è possibile controllare tutte le metriche.</span><span class="sxs-lookup"><span data-stu-id="03a98-129">If this property is **Null**, all metrics can be controlled.</span></span> <span data-ttu-id="03a98-130">Questa proprietà viene ereditata da **CIM \_ MetricServiceCapabilities**.</span><span class="sxs-lookup"><span data-stu-id="03a98-130">This property is inherited from **CIM\_MetricServiceCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="03a98-131">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="03a98-131">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03a98-132">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="03a98-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03a98-133">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="03a98-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03a98-134">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="03a98-134">A description of the object.</span></span> <span data-ttu-id="03a98-135">Questa proprietà viene ereditata da [**CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "definisce le funzionalità del servizio metrica Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="03a98-135">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Defines Hyper-V Metric Service Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="03a98-136">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="03a98-136">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03a98-137">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="03a98-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03a98-138">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="03a98-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03a98-139">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="03a98-139">A display name for the object.</span></span> <span data-ttu-id="03a98-140">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "funzionalità del servizio metrica Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="03a98-140">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Metric Service Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="03a98-141">**ElementNameEditSupported**</span><span class="sxs-lookup"><span data-stu-id="03a98-141">**ElementNameEditSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03a98-142">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="03a98-142">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="03a98-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="03a98-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03a98-144">Indica se la proprietà **ElementName** può essere modificata.</span><span class="sxs-lookup"><span data-stu-id="03a98-144">Indicates whether the **ElementName** property can be modified.</span></span> <span data-ttu-id="03a98-145">Questa proprietà viene ereditata da **CIM \_ EnabledLogicalElementCapabilities**.</span><span class="sxs-lookup"><span data-stu-id="03a98-145">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="03a98-146">**ElementNameMask**</span><span class="sxs-lookup"><span data-stu-id="03a98-146">**ElementNameMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03a98-147">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="03a98-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03a98-148">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="03a98-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03a98-149">Specifica le restrizioni per **ElementName**, espresse come espressione regolare.</span><span class="sxs-lookup"><span data-stu-id="03a98-149">Specifies the restrictions on **ElementName**, expressed as a regular expression.</span></span> <span data-ttu-id="03a98-150">Questa proprietà viene ereditata da **CIM \_ EnabledLogicalElementCapabilities**.</span><span class="sxs-lookup"><span data-stu-id="03a98-150">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="03a98-151">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="03a98-151">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03a98-152">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="03a98-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03a98-153">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="03a98-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03a98-154">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="03a98-154">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="03a98-155">Identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="03a98-155">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="03a98-156">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="03a98-156">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="03a98-157">**ManagedElementControlTypes**</span><span class="sxs-lookup"><span data-stu-id="03a98-157">**ManagedElementControlTypes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03a98-158">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="03a98-158">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="03a98-159">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="03a98-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03a98-160">Qualificatori: **arrayType** ("indicizzato")</span><span class="sxs-lookup"><span data-stu-id="03a98-160">Qualifiers: **ArrayType** ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="03a98-161">Identifica il tipo di controllo supportato dall'istanza del **\_ MetricService CIM** associata per l'oggetto [**CIM \_ gestitoelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) identificato dal valore in corrispondenza dello stesso indice di matrice nella proprietà **ControllableManagedElements** .</span><span class="sxs-lookup"><span data-stu-id="03a98-161">Identifies the type of control supported by the associated **CIM\_MetricService** instance for the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) object identified by the value at the same array index in the **ControllableManagedElements** property.</span></span> <span data-ttu-id="03a98-162">Se questa proprietà è **null**, sono supportati tutti i tipi di controllo.</span><span class="sxs-lookup"><span data-stu-id="03a98-162">If this property is **Null**, all control types are supported.</span></span> <span data-ttu-id="03a98-163">Questa proprietà viene ereditata da **CIM \_ MetricServiceCapabilities**.</span><span class="sxs-lookup"><span data-stu-id="03a98-163">This property is inherited from **CIM\_MetricServiceCapabilities**.</span></span>



| <span data-ttu-id="03a98-164">Valore</span><span class="sxs-lookup"><span data-stu-id="03a98-164">Value</span></span>                                                                                   | <span data-ttu-id="03a98-165">Significato</span><span class="sxs-lookup"><span data-stu-id="03a98-165">Meaning</span></span>                    |
|-----------------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="03a98-166"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="03a98-166"><dt>0</dt></span></span> </dl>            | <span data-ttu-id="03a98-167">Sconosciuto</span><span class="sxs-lookup"><span data-stu-id="03a98-167">Unknown</span></span><br/>         |
| <dl> <span data-ttu-id="03a98-168"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="03a98-168"><dt>2</dt></span></span> </dl>            | <span data-ttu-id="03a98-169">Discrete</span><span class="sxs-lookup"><span data-stu-id="03a98-169">Discrete</span></span><br/>        |
| <dl> <span data-ttu-id="03a98-170"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="03a98-170"><dt>3</dt></span></span> </dl>            | <span data-ttu-id="03a98-171">In blocco</span><span class="sxs-lookup"><span data-stu-id="03a98-171">Bulk</span></span><br/>            |
| <dl> <span data-ttu-id="03a98-172"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="03a98-172"><dt>4</dt></span></span> </dl>            | <span data-ttu-id="03a98-173">Entrambi</span><span class="sxs-lookup"><span data-stu-id="03a98-173">Both</span></span><br/>            |
| <dl> <span data-ttu-id="03a98-174"><dt>5.. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="03a98-174"><dt>5..32767</dt></span></span> </dl>     | <span data-ttu-id="03a98-175">DMTF riservato</span><span class="sxs-lookup"><span data-stu-id="03a98-175">DMTF reserved</span></span><br/>   |
| <dl> <span data-ttu-id="03a98-176"><dt>32768.. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="03a98-176"><dt>32768..65535</dt></span></span> </dl> | <span data-ttu-id="03a98-177">Specifico del fornitore</span><span class="sxs-lookup"><span data-stu-id="03a98-177">Vendor specific</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="03a98-178">**MaxElementNameLen**</span><span class="sxs-lookup"><span data-stu-id="03a98-178">**MaxElementNameLen**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03a98-179">Tipo di dati: **unit16**</span><span class="sxs-lookup"><span data-stu-id="03a98-179">Data type: **unit16**</span></span>
</dt> <dt>

<span data-ttu-id="03a98-180">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="03a98-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03a98-181">Qualificatori: **MaxValue** (256)</span><span class="sxs-lookup"><span data-stu-id="03a98-181">Qualifiers: **MaxValue** (256)</span></span>
</dt> </dl>

<span data-ttu-id="03a98-182">Specifica la lunghezza massima supportata della proprietà **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="03a98-182">Specifies the maximum supported length of the **ElementName** property.</span></span> <span data-ttu-id="03a98-183">Questa proprietà viene ereditata da **CIM \_ EnabledLogicalElementCapabilities**.</span><span class="sxs-lookup"><span data-stu-id="03a98-183">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="03a98-184">**MetricsControlTypes**</span><span class="sxs-lookup"><span data-stu-id="03a98-184">**MetricsControlTypes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03a98-185">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="03a98-185">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="03a98-186">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="03a98-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03a98-187">Qualificatori: **arrayType** ("indicizzato")</span><span class="sxs-lookup"><span data-stu-id="03a98-187">Qualifiers: **ArrayType** ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="03a98-188">Identifica il tipo di controllo supportato dall'istanza **\_ MetricService CIM** associata per il **\_ BaseMetricDefinition CIM** identificato dal valore in corrispondenza dello stesso indice di matrice nella proprietà **ControllableMetrics** .</span><span class="sxs-lookup"><span data-stu-id="03a98-188">Identifies the type of control supported by the associated **CIM\_MetricService** instance for the **CIM\_BaseMetricDefinition** identified by the value at the same array index in the **ControllableMetrics** property.</span></span> <span data-ttu-id="03a98-189">Se questa proprietà è **null**, sono supportati tutti i tipi di controllo.</span><span class="sxs-lookup"><span data-stu-id="03a98-189">If this property is **Null**, all control types are supported.</span></span> <span data-ttu-id="03a98-190">Questa proprietà viene ereditata da **CIM \_ MetricServiceCapabilities**.</span><span class="sxs-lookup"><span data-stu-id="03a98-190">This property is inherited from **CIM\_MetricServiceCapabilities**.</span></span>



| <span data-ttu-id="03a98-191">Valore</span><span class="sxs-lookup"><span data-stu-id="03a98-191">Value</span></span>                                                                                   | <span data-ttu-id="03a98-192">Significato</span><span class="sxs-lookup"><span data-stu-id="03a98-192">Meaning</span></span>                    |
|-----------------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="03a98-193"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="03a98-193"><dt>0</dt></span></span> </dl>            | <span data-ttu-id="03a98-194">Sconosciuto</span><span class="sxs-lookup"><span data-stu-id="03a98-194">Unknown</span></span><br/>         |
| <dl> <span data-ttu-id="03a98-195"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="03a98-195"><dt>2</dt></span></span> </dl>            | <span data-ttu-id="03a98-196">Discrete</span><span class="sxs-lookup"><span data-stu-id="03a98-196">Discrete</span></span><br/>        |
| <dl> <span data-ttu-id="03a98-197"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="03a98-197"><dt>3</dt></span></span> </dl>            | <span data-ttu-id="03a98-198">In blocco</span><span class="sxs-lookup"><span data-stu-id="03a98-198">Bulk</span></span><br/>            |
| <dl> <span data-ttu-id="03a98-199"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="03a98-199"><dt>4</dt></span></span> </dl>            | <span data-ttu-id="03a98-200">Entrambi</span><span class="sxs-lookup"><span data-stu-id="03a98-200">Both</span></span><br/>            |
| <dl> <span data-ttu-id="03a98-201"><dt>5.. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="03a98-201"><dt>5..32767</dt></span></span> </dl>     | <span data-ttu-id="03a98-202">DMTF riservato</span><span class="sxs-lookup"><span data-stu-id="03a98-202">DMTF reserved</span></span><br/>   |
| <dl> <span data-ttu-id="03a98-203"><dt>32768.. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="03a98-203"><dt>32768..65535</dt></span></span> </dl> | <span data-ttu-id="03a98-204">Specifico del fornitore</span><span class="sxs-lookup"><span data-stu-id="03a98-204">Vendor specific</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="03a98-205">**RequestedStatesSupported**</span><span class="sxs-lookup"><span data-stu-id="03a98-205">**RequestedStatesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03a98-206">Tipo di dati: matrice **unit16**</span><span class="sxs-lookup"><span data-stu-id="03a98-206">Data type: **unit16** array</span></span>
</dt> <dt>

<span data-ttu-id="03a98-207">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="03a98-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03a98-208">Indica gli stati possibili che è possibile richiedere quando si utilizza il metodo **RequestStateChange** sull'elemento logico Enabled.</span><span class="sxs-lookup"><span data-stu-id="03a98-208">Indicates the possible states that can be requested when using the **RequestStateChange** method on the enabled logical element.</span></span> <span data-ttu-id="03a98-209">Questa proprietà viene ereditata da **CIM \_ EnabledLogicalElementCapabilities**.</span><span class="sxs-lookup"><span data-stu-id="03a98-209">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>



| <span data-ttu-id="03a98-210">Valore</span><span class="sxs-lookup"><span data-stu-id="03a98-210">Value</span></span>                                                                         | <span data-ttu-id="03a98-211">Significato</span><span class="sxs-lookup"><span data-stu-id="03a98-211">Meaning</span></span>              |
|-------------------------------------------------------------------------------|----------------------|
| <dl> <span data-ttu-id="03a98-212"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="03a98-212"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="03a98-213">Abilitato</span><span class="sxs-lookup"><span data-stu-id="03a98-213">Enabled</span></span><br/>   |
| <dl> <span data-ttu-id="03a98-214"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="03a98-214"><dt>3</dt></span></span> </dl>  | <span data-ttu-id="03a98-215">Disabilita</span><span class="sxs-lookup"><span data-stu-id="03a98-215">Disables</span></span><br/>  |
| <dl> <span data-ttu-id="03a98-216"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="03a98-216"><dt>4</dt></span></span> </dl>  | <span data-ttu-id="03a98-217">Arresta</span><span class="sxs-lookup"><span data-stu-id="03a98-217">Shut Down</span></span><br/> |
| <dl> <span data-ttu-id="03a98-218"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="03a98-218"><dt>6</dt></span></span> </dl>  | <span data-ttu-id="03a98-219">Offline</span><span class="sxs-lookup"><span data-stu-id="03a98-219">Offline</span></span><br/>   |
| <dl> <span data-ttu-id="03a98-220"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="03a98-220"><dt>7</dt></span></span> </dl>  | <span data-ttu-id="03a98-221">Test</span><span class="sxs-lookup"><span data-stu-id="03a98-221">Test</span></span><br/>      |
| <dl> <span data-ttu-id="03a98-222"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="03a98-222"><dt>8</dt></span></span> </dl>  | <span data-ttu-id="03a98-223">Rinviare</span><span class="sxs-lookup"><span data-stu-id="03a98-223">Defer</span></span><br/>     |
| <dl> <span data-ttu-id="03a98-224"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="03a98-224"><dt>9</dt></span></span> </dl>  | <span data-ttu-id="03a98-225">Disattivazione</span><span class="sxs-lookup"><span data-stu-id="03a98-225">Quiesce</span></span><br/>   |
| <dl> <span data-ttu-id="03a98-226"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="03a98-226"><dt>10</dt></span></span> </dl> | <span data-ttu-id="03a98-227">Riavvio</span><span class="sxs-lookup"><span data-stu-id="03a98-227">Reboot</span></span><br/>    |
| <dl> <span data-ttu-id="03a98-228"><dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="03a98-228"><dt>11</dt></span></span> </dl> | <span data-ttu-id="03a98-229">Reset</span><span class="sxs-lookup"><span data-stu-id="03a98-229">Reset</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="03a98-230">**SupportedMethods**</span><span class="sxs-lookup"><span data-stu-id="03a98-230">**SupportedMethods**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03a98-231">Tipo di dati: matrice **UInt16**</span><span class="sxs-lookup"><span data-stu-id="03a98-231">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="03a98-232">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="03a98-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03a98-233">Specifica i metodi supportati dal servizio metrico.</span><span class="sxs-lookup"><span data-stu-id="03a98-233">Specifies the methods supported by the metric service.</span></span> <span data-ttu-id="03a98-234">Questa proprietà viene ereditata da **CIM \_ MetricServiceCapabilities**.</span><span class="sxs-lookup"><span data-stu-id="03a98-234">This property is inherited from **CIM\_MetricServiceCapabilities**.</span></span>



| <span data-ttu-id="03a98-235">Valore</span><span class="sxs-lookup"><span data-stu-id="03a98-235">Value</span></span>                                                                                   | <span data-ttu-id="03a98-236">Significato</span><span class="sxs-lookup"><span data-stu-id="03a98-236">Meaning</span></span>                                                                                         |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="03a98-237"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="03a98-237"><dt>2</dt></span></span> </dl>            | <span data-ttu-id="03a98-238">Il metodo [**ControlMetrics**](controlmetrics-msvm-metricservice.md) è supportato.</span><span class="sxs-lookup"><span data-stu-id="03a98-238">The [**ControlMetrics**](controlmetrics-msvm-metricservice.md) method is supported.</span></span><br/> |
| <dl> <span data-ttu-id="03a98-239"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="03a98-239"><dt>3</dt></span></span> </dl>            | <span data-ttu-id="03a98-240">Il metodo **ControlMetricsByClass** è supportato.</span><span class="sxs-lookup"><span data-stu-id="03a98-240">The **ControlMetricsByClass** method is supported.</span></span><br/>                                   |
| <dl> <span data-ttu-id="03a98-241"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="03a98-241"><dt>4</dt></span></span> </dl>            | <span data-ttu-id="03a98-242">Il metodo **ShowMetrics** è supportato.</span><span class="sxs-lookup"><span data-stu-id="03a98-242">The **ShowMetrics** method is supported.</span></span><br/>                                             |
| <dl> <span data-ttu-id="03a98-243"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="03a98-243"><dt>5</dt></span></span> </dl>            | <span data-ttu-id="03a98-244">Il metodo **ShowMetricsByClass** è supportato.</span><span class="sxs-lookup"><span data-stu-id="03a98-244">The **ShowMetricsByClass** method is supported.</span></span><br/>                                      |
| <dl> <span data-ttu-id="03a98-245"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="03a98-245"><dt>6</dt></span></span> </dl>            | <span data-ttu-id="03a98-246">Il metodo **GetMetricValues** è supportato.</span><span class="sxs-lookup"><span data-stu-id="03a98-246">The **GetMetricValues** method is supported.</span></span><br/>                                         |
| <dl> <span data-ttu-id="03a98-247"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="03a98-247"><dt>7</dt></span></span> </dl>            | <span data-ttu-id="03a98-248">Il metodo **ControlSampleTimes** è supportato.</span><span class="sxs-lookup"><span data-stu-id="03a98-248">The **ControlSampleTimes** method is supported.</span></span><br/>                                      |
| <dl> <span data-ttu-id="03a98-249"><dt>8.. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="03a98-249"><dt>8..32767</dt></span></span> </dl>     | <span data-ttu-id="03a98-250">DMTF riservato</span><span class="sxs-lookup"><span data-stu-id="03a98-250">DMTF reserved</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="03a98-251"><dt>32768.. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="03a98-251"><dt>32768..65535</dt></span></span> </dl> | <span data-ttu-id="03a98-252">Specifico del fornitore</span><span class="sxs-lookup"><span data-stu-id="03a98-252">Vendor specific</span></span><br/>                                                                      |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="03a98-253">Requisiti</span><span class="sxs-lookup"><span data-stu-id="03a98-253">Requirements</span></span>



| <span data-ttu-id="03a98-254">Requisito</span><span class="sxs-lookup"><span data-stu-id="03a98-254">Requirement</span></span> | <span data-ttu-id="03a98-255">Valore</span><span class="sxs-lookup"><span data-stu-id="03a98-255">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03a98-256">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="03a98-256">Minimum supported client</span></span><br/> | <span data-ttu-id="03a98-257">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="03a98-257">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="03a98-258">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="03a98-258">Minimum supported server</span></span><br/> | <span data-ttu-id="03a98-259">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="03a98-259">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="03a98-260">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="03a98-260">Namespace</span></span><br/>                | <span data-ttu-id="03a98-261">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="03a98-261">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="03a98-262">MOF</span><span class="sxs-lookup"><span data-stu-id="03a98-262">MOF</span></span><br/>                      | <dl> <span data-ttu-id="03a98-263"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="03a98-263"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="03a98-264">DLL</span><span class="sxs-lookup"><span data-stu-id="03a98-264">DLL</span></span><br/>                      | <dl> <span data-ttu-id="03a98-265"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="03a98-265"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="03a98-266">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="03a98-266">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03a98-267">**\_METRICSERVICECAPABILITIES CIM**</span><span class="sxs-lookup"><span data-stu-id="03a98-267">**CIM\_MetricServiceCapabilities**</span></span>](cim-metricservicecapabilities.md)
</dt> <dt>

[<span data-ttu-id="03a98-268">**\_MetricService MSVM**</span><span class="sxs-lookup"><span data-stu-id="03a98-268">**Msvm\_MetricService**</span></span>](msvm-metricservice.md)
</dt> </dl>

 

