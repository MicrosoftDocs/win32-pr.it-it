---
description: Rappresenta il valore dell'istanza di una metrica definita da un'istanza della \_ classe MSVM AggregationMetricDefinition.
ms.assetid: 6dfcb711-6137-492a-aff4-82facbd11949
title: Classe Msvm_AggregationMetricValue
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AggregationMetricValue
- Msvm_AggregationMetricValue.InstanceID
- Msvm_AggregationMetricValue.Caption
- Msvm_AggregationMetricValue.Description
- Msvm_AggregationMetricValue.ElementName
- Msvm_AggregationMetricValue.MetricDefinitionId
- Msvm_AggregationMetricValue.MeasuredElementName
- Msvm_AggregationMetricValue.TimeStamp
- Msvm_AggregationMetricValue.Duration
- Msvm_AggregationMetricValue.MetricValue
- Msvm_AggregationMetricValue.BreakdownDimension
- Msvm_AggregationMetricValue.BreakdownValue
- Msvm_AggregationMetricValue.Volatile
- Msvm_AggregationMetricValue.AggregationTimeStamp
- Msvm_AggregationMetricValue.AggregationDuration
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f6842e5a23fbbf7cf1d639862cf5b9737bc1ff96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104057981"
---
# <a name="msvm_aggregationmetricvalue-class"></a><span data-ttu-id="868a9-103">\_Classe MSVM AggregationMetricValue</span><span class="sxs-lookup"><span data-stu-id="868a9-103">Msvm\_AggregationMetricValue class</span></span>

<span data-ttu-id="868a9-104">Rappresenta il valore dell'istanza di una metrica definita da un'istanza della classe [**MSVM \_ AggregationMetricDefinition**](msvm-aggregationmetricdefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="868a9-104">Represents the instance value of a metric defined by an instance of the [**Msvm\_AggregationMetricDefinition**](msvm-aggregationmetricdefinition.md) class.</span></span> <span data-ttu-id="868a9-105">Le proprietà ereditate da [**MSVM \_ BaseMetricValue**](msvm-basemetricvalue.md) forniscono il valore della metrica effettivo.</span><span class="sxs-lookup"><span data-stu-id="868a9-105">The properties inherited from [**Msvm\_BaseMetricValue**](msvm-basemetricvalue.md) provide the actual metric value.</span></span> <span data-ttu-id="868a9-106">Le proprietà definite da questa classe forniscono informazioni sull'intervallo in base al quale è stata applicata la funzione di aggregazione.</span><span class="sxs-lookup"><span data-stu-id="868a9-106">The properties defined by this class provide information about the interval over which the aggregation function was applied.</span></span>

<span data-ttu-id="868a9-107">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="868a9-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="868a9-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="868a9-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_AggregationMetricValue : CIM_AggregationMetricValue
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  string   MetricDefinitionId;
  string   MeasuredElementName;
  datetime TimeStamp;
  datetime Duration;
  string   MetricValue;
  string   BreakdownDimension;
  string   BreakdownValue;
  boolean  Volatile;
  datetime AggregationTimeStamp;
  datetime AggregationDuration;
};
```

## <a name="members"></a><span data-ttu-id="868a9-109">Members</span><span class="sxs-lookup"><span data-stu-id="868a9-109">Members</span></span>

<span data-ttu-id="868a9-110">La **classe \_ AggregationMetricValue di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="868a9-110">The **Msvm\_AggregationMetricValue** class has these types of members:</span></span>

-   [<span data-ttu-id="868a9-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="868a9-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="868a9-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="868a9-112">Properties</span></span>

<span data-ttu-id="868a9-113">La **classe \_ AggregationMetricValue di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="868a9-113">The **Msvm\_AggregationMetricValue** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="868a9-114">**AggregationDuration**</span><span class="sxs-lookup"><span data-stu-id="868a9-114">**AggregationDuration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="868a9-115">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="868a9-115">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="868a9-116">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="868a9-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="868a9-117">Rappresenta la durata dell'intervallo di tempo in cui è stata calcolata l'aggregazione.</span><span class="sxs-lookup"><span data-stu-id="868a9-117">Represents the time duration over which the aggregation was computed.</span></span> <span data-ttu-id="868a9-118">L'inizio di un intervallo di monitoraggio sul quale viene applicata la funzione di aggregazione viene determinato sottraendo **AggregationDuration** da **AggregationTimeStamp**.</span><span class="sxs-lookup"><span data-stu-id="868a9-118">The start of a monitoring interval over which the aggregation function is applied is determined by subtracting the **AggregationDuration** from the **AggregationTimeStamp**.</span></span> <span data-ttu-id="868a9-119">Questa proprietà viene ereditata da **CIM \_ AggregationMetricValue**.</span><span class="sxs-lookup"><span data-stu-id="868a9-119">This property is inherited from **CIM\_AggregationMetricValue**.</span></span>

</dd> <dt>

<span data-ttu-id="868a9-120">**AggregationTimeStamp**</span><span class="sxs-lookup"><span data-stu-id="868a9-120">**AggregationTimeStamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="868a9-121">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="868a9-121">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="868a9-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="868a9-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="868a9-123">Indica l'ora in cui è stata applicata la funzione di aggregazione per determinare il valore dell'istanza della metrica.</span><span class="sxs-lookup"><span data-stu-id="868a9-123">Identifies the time when the aggregation function was applied to determine the value of the metric instance.</span></span> <span data-ttu-id="868a9-124">Non corrisponde all'ora di creazione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="868a9-124">This is not the same as the time when the instance was created.</span></span> <span data-ttu-id="868a9-125">Per un'istanza **di \_ AggregationMetricValue CIM** specificata, **AggregationTimeStamp** cambia ogni volta che viene applicata la funzione di aggregazione per calcolare il valore.</span><span class="sxs-lookup"><span data-stu-id="868a9-125">For a given **CIM\_AggregationMetricValue** instance, the **AggregationTimeStamp** changes whenever the aggregation function is applied to calculate the value.</span></span> <span data-ttu-id="868a9-126">Questa proprietà viene ereditata da **CIM \_ AggregationMetricValue**.</span><span class="sxs-lookup"><span data-stu-id="868a9-126">This property is inherited from **CIM\_AggregationMetricValue**.</span></span>

</dd> <dt>

<span data-ttu-id="868a9-127">**BreakdownDimension**</span><span class="sxs-lookup"><span data-stu-id="868a9-127">**BreakdownDimension**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="868a9-128">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="868a9-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="868a9-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="868a9-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="868a9-130">Specifica una dimensione di suddivisione dalla matrice **BreakdownDimensions** definita nel [**\_ BaseMetricDefinition MSVM**](msvm-basemetricdefinition.md)associato.</span><span class="sxs-lookup"><span data-stu-id="868a9-130">Specifies one breakdown dimension from the **BreakdownDimensions** array defined in the associated [**Msvm\_BaseMetricDefinition**](msvm-basemetricdefinition.md).</span></span> <span data-ttu-id="868a9-131">Si tratta della dimensione in base alla quale questo set di valori di metrica viene suddiviso.</span><span class="sxs-lookup"><span data-stu-id="868a9-131">This is the dimension along which this set of metric values is broken down.</span></span> <span data-ttu-id="868a9-132">Questa proprietà viene ereditata da [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="868a9-132">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="868a9-133">**BreakdownValue**</span><span class="sxs-lookup"><span data-stu-id="868a9-133">**BreakdownValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="868a9-134">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="868a9-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="868a9-135">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="868a9-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="868a9-136">Definisce un valore della proprietà **BreakdownDimension** definita per questa istanza del valore della metrica.</span><span class="sxs-lookup"><span data-stu-id="868a9-136">Defines a value of the **BreakdownDimension** property defined for this metric value instance.</span></span> <span data-ttu-id="868a9-137">Ad esempio, se **BreakdownDimension** è "transactionName", questa proprietà può assegnare un nome alla transazione effettiva a cui si applica questo particolare valore della metrica.</span><span class="sxs-lookup"><span data-stu-id="868a9-137">For example, if the **BreakdownDimension** is "TransactionName", this property could name the actual transaction to which this particular metric value applies.</span></span> <span data-ttu-id="868a9-138">Questa proprietà viene ereditata da [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="868a9-138">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="868a9-139">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="868a9-139">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="868a9-140">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="868a9-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="868a9-141">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="868a9-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="868a9-142">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="868a9-142">A short description of the object.</span></span> <span data-ttu-id="868a9-143">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="868a9-143">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="868a9-144">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="868a9-144">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="868a9-145">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="868a9-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="868a9-146">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="868a9-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="868a9-147">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="868a9-147">A description of the object.</span></span> <span data-ttu-id="868a9-148">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="868a9-148">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="868a9-149">**Duration**</span><span class="sxs-lookup"><span data-stu-id="868a9-149">**Duration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="868a9-150">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="868a9-150">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="868a9-151">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="868a9-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="868a9-152">Specifica la durata del periodo di validità del valore della metrica.</span><span class="sxs-lookup"><span data-stu-id="868a9-152">Specifies the time duration over which this metric value is valid.</span></span> <span data-ttu-id="868a9-153">Questa proprietà non deve esistere per gli indicatori di tempo che si applicano solo a un punto nel tempo, ma deve essere specificata per i valori considerati validi per un determinato periodo di tempo, ad esempio il campionamento.</span><span class="sxs-lookup"><span data-stu-id="868a9-153">This property should not exist for time stamps that apply only to a point in time, but should be specified for values that are considered valid for a certain time period (for example, sampling).</span></span> <span data-ttu-id="868a9-154">Se la proprietà **Duration** esiste e non è **null**, la proprietà **timestamp** specifica la fine dell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="868a9-154">If the **Duration** property exists and is not **Null**, the **TimeStamp** property specifies the end of the interval.</span></span> <span data-ttu-id="868a9-155">Questa proprietà viene ereditata da [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="868a9-155">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="868a9-156">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="868a9-156">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="868a9-157">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="868a9-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="868a9-158">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="868a9-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="868a9-159">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="868a9-159">A display name for the object.</span></span> <span data-ttu-id="868a9-160">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="868a9-160">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="868a9-161">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="868a9-161">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="868a9-162">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="868a9-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="868a9-163">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="868a9-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="868a9-164">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="868a9-164">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="868a9-165">Stringa che identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="868a9-165">A string that uniquely identifies an instance of this class.</span></span> <span data-ttu-id="868a9-166">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="868a9-166">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="868a9-167">**MeasuredElementName**</span><span class="sxs-lookup"><span data-stu-id="868a9-167">**MeasuredElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="868a9-168">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="868a9-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="868a9-169">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="868a9-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="868a9-170">Nome descrittivo per l'elemento a cui appartiene il valore della metrica, ovvero l'elemento misurato.</span><span class="sxs-lookup"><span data-stu-id="868a9-170">A descriptive name for the element to which the metric value belongs (the measured element).</span></span> <span data-ttu-id="868a9-171">Questa proprietà viene ereditata da [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="868a9-171">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="868a9-172">**MetricDefinitionId**</span><span class="sxs-lookup"><span data-stu-id="868a9-172">**MetricDefinitionId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="868a9-173">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="868a9-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="868a9-174">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="868a9-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="868a9-175">Chiave dell'istanza di [**\_ BaseMetricDefinition MSVM**](msvm-basemetricdefinition.md) per questo valore.</span><span class="sxs-lookup"><span data-stu-id="868a9-175">The key of the [**Msvm\_BaseMetricDefinition**](msvm-basemetricdefinition.md) instance for this value.</span></span> <span data-ttu-id="868a9-176">Questa proprietà viene ereditata da [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="868a9-176">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="868a9-177">**MetricValue**</span><span class="sxs-lookup"><span data-stu-id="868a9-177">**MetricValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="868a9-178">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="868a9-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="868a9-179">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="868a9-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="868a9-180">Valore della metrica rappresentata come stringa.</span><span class="sxs-lookup"><span data-stu-id="868a9-180">The value of the metric that is represented as a string.</span></span> <span data-ttu-id="868a9-181">Questa proprietà viene ereditata da [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="868a9-181">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="868a9-182">**TimeStamp**</span><span class="sxs-lookup"><span data-stu-id="868a9-182">**TimeStamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="868a9-183">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="868a9-183">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="868a9-184">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="868a9-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="868a9-185">Specifica l'ora in cui il valore della metrica è stato acquisito o calcolato.</span><span class="sxs-lookup"><span data-stu-id="868a9-185">Specifies the time when the metric value was captured or computed.</span></span> <span data-ttu-id="868a9-186">Tenere presente che si tratta di una differenza rispetto all'ora di creazione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="868a9-186">Be aware that this is different from the time when the instance was created.</span></span> <span data-ttu-id="868a9-187">Questa proprietà viene ereditata da [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="868a9-187">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="868a9-188">**Volatile**</span><span class="sxs-lookup"><span data-stu-id="868a9-188">**Volatile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="868a9-189">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="868a9-189">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="868a9-190">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="868a9-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="868a9-191">**True** se il valore per il momento successivo utilizzerà la stessa istanza della classe e modificherà solo i valori delle proprietà, ad esempio il **valore** o il **timestamp**.</span><span class="sxs-lookup"><span data-stu-id="868a9-191">**True** if the value for the next point in time will use the same class instance and just change the property values (such as the **Value** or **TimeStamp**).</span></span> <span data-ttu-id="868a9-192">Se **true**, l'istanza viene riutilizzata.</span><span class="sxs-lookup"><span data-stu-id="868a9-192">If **True**, the instance is reused.</span></span> <span data-ttu-id="868a9-193">Se **false**, le istanze esistenti rimangono invariate e viene creata una nuova istanza per il nuovo punto nel tempo.</span><span class="sxs-lookup"><span data-stu-id="868a9-193">If **False**, the existing instances remain unchanged and a new instance is created for the new point in time.</span></span> <span data-ttu-id="868a9-194">Questa proprietà viene ereditata da [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="868a9-194">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="868a9-195">Requisiti</span><span class="sxs-lookup"><span data-stu-id="868a9-195">Requirements</span></span>



| <span data-ttu-id="868a9-196">Requisito</span><span class="sxs-lookup"><span data-stu-id="868a9-196">Requirement</span></span> | <span data-ttu-id="868a9-197">Valore</span><span class="sxs-lookup"><span data-stu-id="868a9-197">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="868a9-198">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="868a9-198">Minimum supported client</span></span><br/> | <span data-ttu-id="868a9-199">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="868a9-199">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="868a9-200">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="868a9-200">Minimum supported server</span></span><br/> | <span data-ttu-id="868a9-201">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="868a9-201">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="868a9-202">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="868a9-202">Namespace</span></span><br/>                | <span data-ttu-id="868a9-203">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="868a9-203">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="868a9-204">MOF</span><span class="sxs-lookup"><span data-stu-id="868a9-204">MOF</span></span><br/>                      | <dl> <span data-ttu-id="868a9-205"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="868a9-205"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="868a9-206">DLL</span><span class="sxs-lookup"><span data-stu-id="868a9-206">DLL</span></span><br/>                      | <dl> <span data-ttu-id="868a9-207"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="868a9-207"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

