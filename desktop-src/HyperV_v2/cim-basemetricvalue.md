---
description: Rappresenta il valore dell'istanza di una metrica.
ms.assetid: 6b272ae8-7684-45bb-bff8-6559680cc8b6
title: Classe CIM_BaseMetricValue
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BaseMetricValue
- CIM_BaseMetricValue.InstanceID
- CIM_BaseMetricValue.MetricDefinitionId
- CIM_BaseMetricValue.MeasuredElementName
- CIM_BaseMetricValue.TimeStamp
- CIM_BaseMetricValue.Duration
- CIM_BaseMetricValue.MetricValue
- CIM_BaseMetricValue.BreakdownDimension
- CIM_BaseMetricValue.BreakdownValue
- CIM_BaseMetricValue.Volatile
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ca6c90a4b6b3ef3e690c13612f69480ec5f008be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968109"
---
# <a name="cim_basemetricvalue-class"></a><span data-ttu-id="20cf7-103">CIM \_ BaseMetricValue (classe)</span><span class="sxs-lookup"><span data-stu-id="20cf7-103">CIM\_BaseMetricValue class</span></span>

<span data-ttu-id="20cf7-104">Rappresenta il valore dell'istanza di una metrica.</span><span class="sxs-lookup"><span data-stu-id="20cf7-104">Represents the instance value of a metric.</span></span>

## <a name="syntax"></a><span data-ttu-id="20cf7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="20cf7-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.19.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_BaseMetricValue : CIM_ManagedElement
{
  string   InstanceID;
  string   MetricDefinitionId;
  string   MeasuredElementName;
  datetime TimeStamp;
  datetime Duration;
  string   MetricValue;
  string   BreakdownDimension;
  string   BreakdownValue;
  boolean  Volatile;
};
```

## <a name="members"></a><span data-ttu-id="20cf7-106">Members</span><span class="sxs-lookup"><span data-stu-id="20cf7-106">Members</span></span>

<span data-ttu-id="20cf7-107">La classe **CIM \_ BaseMetricValue** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="20cf7-107">The **CIM\_BaseMetricValue** class has these types of members:</span></span>

-   [<span data-ttu-id="20cf7-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="20cf7-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="20cf7-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="20cf7-109">Properties</span></span>

<span data-ttu-id="20cf7-110">La classe **CIM \_ BaseMetricValue** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="20cf7-110">The **CIM\_BaseMetricValue** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="20cf7-111">**BreakdownDimension**</span><span class="sxs-lookup"><span data-stu-id="20cf7-111">**BreakdownDimension**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20cf7-112">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="20cf7-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20cf7-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20cf7-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20cf7-114">Dimensione per la quale questo set di valori di metrica viene suddiviso in base alla proprietà **BreakdownDimensions** dell' [**oggetto \_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md) associato.</span><span class="sxs-lookup"><span data-stu-id="20cf7-114">The dimension for which this set of metric values is broken down based on **BreakdownDimensions** property of the associated [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="20cf7-115">**BreakdownValue**</span><span class="sxs-lookup"><span data-stu-id="20cf7-115">**BreakdownValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20cf7-116">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="20cf7-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20cf7-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20cf7-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20cf7-118">Valore della proprietà **BreakdownDimension** definita per questo valore dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="20cf7-118">The value of the **BreakdownDimension** property defined for this instance value.</span></span> <span data-ttu-id="20cf7-119">Se, ad esempio, **BreakdownDimension** contiene "transactionName", questa proprietà potrebbe assegnare un nome alla transazione effettiva a cui si applica questo particolare valore della metrica.</span><span class="sxs-lookup"><span data-stu-id="20cf7-119">For example, if **BreakdownDimension** contains "TransactionName", this property could name the actual transaction to which this particular metric value applies.</span></span>

</dd> <dt>

<span data-ttu-id="20cf7-120">**Duration**</span><span class="sxs-lookup"><span data-stu-id="20cf7-120">**Duration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20cf7-121">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="20cf7-121">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="20cf7-122">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20cf7-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20cf7-123">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md).**TimeScope**","**CIM \_ BaseMetricValue**.**TimeStamp**")</span><span class="sxs-lookup"><span data-stu-id="20cf7-123">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md).**TimeScope**", "**CIM\_BaseMetricValue**.**TimeStamp**")</span></span>
</dt> </dl>

<span data-ttu-id="20cf7-124">Durata del periodo di validità del valore della metrica.</span><span class="sxs-lookup"><span data-stu-id="20cf7-124">The time duration over which this metric value is valid.</span></span> <span data-ttu-id="20cf7-125">Questa proprietà non deve esistere per gli indicatori temporali che si applicano solo a un punto nel tempo, ma deve essere definito per i valori considerati validi per un determinato periodo di tempo (ad esempio,</span><span class="sxs-lookup"><span data-stu-id="20cf7-125">This property should not exist for time stamps that only apply to a point in time, but should be defined for values that are considered valid for a certain time period (ex.</span></span> <span data-ttu-id="20cf7-126">campionamento).</span><span class="sxs-lookup"><span data-stu-id="20cf7-126">sampling).</span></span> <span data-ttu-id="20cf7-127">Se la proprietà **Duration** esiste e è diversa da null, il valore di **timestamp** deve essere la fine dell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="20cf7-127">If the **Duration** property exists and is non-Null, the **TimeStamp** value should be the end of the interval.</span></span>

</dd> <dt>

<span data-ttu-id="20cf7-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="20cf7-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20cf7-129">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="20cf7-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20cf7-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20cf7-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20cf7-131">Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceId")</span><span class="sxs-lookup"><span data-stu-id="20cf7-131">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceID")</span></span>
</dt> </dl>

<span data-ttu-id="20cf7-132">Identifica in modo univoco un'istanza di questa classe nell'ambito dello spazio dei nomi che lo contiene.</span><span class="sxs-lookup"><span data-stu-id="20cf7-132">Uniquely identifies an instance of this class within the scope of the containing namespace.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="20cf7-133">Per garantire l'univocità all'interno dello spazio dei nomi, il valore della proprietà **InstanceID** deve essere costruito nel modello seguente: *OrgID*:*LocalId*</span><span class="sxs-lookup"><span data-stu-id="20cf7-133">In order to ensure uniqueness within the namespace, the value of the **InstanceID** property should be constructed in the following pattern: *OrgID*:*LocalID*</span></span>
>
> <span data-ttu-id="20cf7-134">*OrgID* deve includere un nome con copyright, marchio o in altro modo univoco, di proprietà dell'entità di business che definisce **InstanceID**, oppure essere un ID registrato assegnato da un'autorità globale riconosciuta.</span><span class="sxs-lookup"><span data-stu-id="20cf7-134">*OrgID* must include a copyrighted, trademarked or otherwise unique name that is owned by the business entity that defines the **InstanceID**, or be a registered ID that is assigned by a recognized global authority.</span></span> <span data-ttu-id="20cf7-135">Questo modello è simile alla struttura dei nomi delle classi dello schema.</span><span class="sxs-lookup"><span data-stu-id="20cf7-135">This pattern is similar to the structure of schema class names.</span></span> <span data-ttu-id="20cf7-136">Inoltre, per garantire l'univocità, i primi due punti in **InstanceID** devono essere compresi tra *OrgID* e *LocalId*.</span><span class="sxs-lookup"><span data-stu-id="20cf7-136">In addition, to ensure uniqueness, the first colon in **InstanceID** must be between the *OrgID* and *LocalID*.</span></span> <span data-ttu-id="20cf7-137">Pertanto *OrgID* non deve contenere i due punti (':').</span><span class="sxs-lookup"><span data-stu-id="20cf7-137">Therefore the *OrgID* must not contain a colon (':').</span></span>
>
> <span data-ttu-id="20cf7-138">Il *localizzato* viene scelto dall'entità di business e non deve essere riutilizzato per identificare diversi elementi reali sottostanti.</span><span class="sxs-lookup"><span data-stu-id="20cf7-138">*LocalID* is chosen by the business entity and should not be re-used to identify different underlying real-world elements.</span></span>
>
> <span data-ttu-id="20cf7-139">Se il criterio precedente non viene utilizzato, l'entità di definizione deve assicurare che il valore **InstanceID** risultante non venga riutilizzato nelle proprietà **InstanceID** generate dal provider o da altri provider per questo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="20cf7-139">If the above pattern is not used, the defining entity must assure that the resultant **InstanceID** value is not re-used across any **InstanceID** properties that are produced by this provider or other providers for this namespace.</span></span>
>
> <span data-ttu-id="20cf7-140">Per le istanze definite DMTF (Distributed Management Task Force), il modello deve essere usato con *OrgID* impostato su CIM.</span><span class="sxs-lookup"><span data-stu-id="20cf7-140">For Distributed Management Task Force (DMTF) defined instances, the pattern must be used with the *OrgID* set to CIM.</span></span>

 

</dd> <dt>

<span data-ttu-id="20cf7-141">**MeasuredElementName**</span><span class="sxs-lookup"><span data-stu-id="20cf7-141">**MeasuredElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20cf7-142">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="20cf7-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20cf7-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20cf7-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20cf7-144">Nome descrittivo per l'elemento misurato dalla metrica.</span><span class="sxs-lookup"><span data-stu-id="20cf7-144">A descriptive name for the element that is measure by the metric.</span></span>

<span data-ttu-id="20cf7-145">Questa proprietà è obbligatoria se la definizione della metrica non è associata a un oggetto [**\_ gestito CIM**](cim-managedelement.md) e può essere usata in altri casi per fornire informazioni aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="20cf7-145">This property is required if the metric definition is not associated with a [**CIM\_ManagedElement**](cim-managedelement.md) object, and may be used in other cases to provide supplemental information.</span></span> <span data-ttu-id="20cf7-146">Ciò consente di acquisire le metriche indipendentemente da qualsiasi oggetto **CIM \_ gestito** .</span><span class="sxs-lookup"><span data-stu-id="20cf7-146">This allows metrics to be captured independent of any **CIM\_ManagedElement** object.</span></span>

<span data-ttu-id="20cf7-147">Se sono presenti più oggetti [**CIM \_ gestitielement**](cim-managedelement.md) associati al valore della metrica, è possibile scegliere uno degli elementi gestiti per creare le informazioni aggiuntive per la metrica.</span><span class="sxs-lookup"><span data-stu-id="20cf7-147">If there are multiple [**CIM\_ManagedElement**](cim-managedelement.md) objects associated with the metric value, then you can choose one of the managed elements to create the supplemental information for the metric.</span></span> <span data-ttu-id="20cf7-148">La proprietà non deve essere utilizzata come chiave esterna per eseguire una query sull'elemento misurato.</span><span class="sxs-lookup"><span data-stu-id="20cf7-148">The property is not meant to be used as a foreign key to query the measured element.</span></span> <span data-ttu-id="20cf7-149">È invece consigliabile usare l'associazione a **CIM \_ Managed** .</span><span class="sxs-lookup"><span data-stu-id="20cf7-149">Instead, the association to the **CIM\_ManagedElement** should be used.</span></span>

</dd> <dt>

<span data-ttu-id="20cf7-150">**MetricDefinitionId**</span><span class="sxs-lookup"><span data-stu-id="20cf7-150">**MetricDefinitionId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20cf7-151">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="20cf7-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20cf7-152">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20cf7-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20cf7-153">Qualificatori: [**required**](/windows/desktop/WmiSdk/standard-qualifiers), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md).**ID**")</span><span class="sxs-lookup"><span data-stu-id="20cf7-153">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md).**Id**")</span></span>
</dt> </dl>

<span data-ttu-id="20cf7-154">Chiave dell'istanza di [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) associata a questo valore dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="20cf7-154">The key of the [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) instance that is associated with this instance value.</span></span>

</dd> <dt>

<span data-ttu-id="20cf7-155">**MetricValue**</span><span class="sxs-lookup"><span data-stu-id="20cf7-155">**MetricValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20cf7-156">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="20cf7-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20cf7-157">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20cf7-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20cf7-158">Qualificatori: [ **obbligatorio**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="20cf7-158">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="20cf7-159">Rappresentazione di stringa del valore della metrica.</span><span class="sxs-lookup"><span data-stu-id="20cf7-159">A string representation of the metric value.</span></span> <span data-ttu-id="20cf7-160">Il tipo di dati originale del valore della metrica viene specificato nell'oggetto [**\_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md) associato.</span><span class="sxs-lookup"><span data-stu-id="20cf7-160">The original data type of the metric value is specified in the associated [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="20cf7-161">**TimeStamp**</span><span class="sxs-lookup"><span data-stu-id="20cf7-161">**TimeStamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20cf7-162">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="20cf7-162">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="20cf7-163">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20cf7-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20cf7-164">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md).**TimeScope**","**CIM \_ BaseMetricValue**.**Durata**")</span><span class="sxs-lookup"><span data-stu-id="20cf7-164">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md).**TimeScope**", "**CIM\_BaseMetricValue**.**Duration**")</span></span>
</dt> </dl>

<span data-ttu-id="20cf7-165">Data e ora in cui viene calcolato il valore di un'istanza della metrica.</span><span class="sxs-lookup"><span data-stu-id="20cf7-165">The time when the value of a metric instance is computed.</span></span> <span data-ttu-id="20cf7-166">Questa operazione è diversa dal momento in cui viene creata l'istanza.</span><span class="sxs-lookup"><span data-stu-id="20cf7-166">This is different from the time when the instance is created.</span></span> <span data-ttu-id="20cf7-167">Se la proprietà **volatile** è true, questo valore cambia ogni volta che viene eseguito un nuovo snapshot di misurazione.</span><span class="sxs-lookup"><span data-stu-id="20cf7-167">If the **Volatile** property is true, this value changes whenever a new measurement snapshot is taken.</span></span>

<span data-ttu-id="20cf7-168">Un'applicazione di gestione può stabilire una serie temporale di dati di metrica recuperando le istanze di **CIM \_ BaseMetricValue** e ordinando le istanze in base al relativo valore di **timestamp** .</span><span class="sxs-lookup"><span data-stu-id="20cf7-168">A management application may establish a time series of metric data by retrieving the instances of **CIM\_BaseMetricValue** and sorting them according to their **TimeStamp** value.</span></span>

</dd> <dt>

<span data-ttu-id="20cf7-169">**Volatile**</span><span class="sxs-lookup"><span data-stu-id="20cf7-169">**Volatile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20cf7-170">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="20cf7-170">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="20cf7-171">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="20cf7-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20cf7-172">True se il valore di **timestamp** cambia ogni volta che viene modificato il valore dell'istanza della metrica.</span><span class="sxs-lookup"><span data-stu-id="20cf7-172">True if the **TimeStamp** value changes whenever the value of the metric instance changes.</span></span> <span data-ttu-id="20cf7-173">False se l'oggetto deve rimanere invariato e viene creato un nuovo oggetto per il nuovo valore di **timestamp** .</span><span class="sxs-lookup"><span data-stu-id="20cf7-173">False if this object must remain unchanged and a new object created for the new **TimeStamp** value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="20cf7-174">Requisiti</span><span class="sxs-lookup"><span data-stu-id="20cf7-174">Requirements</span></span>



| <span data-ttu-id="20cf7-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="20cf7-175">Requirement</span></span> | <span data-ttu-id="20cf7-176">Valore</span><span class="sxs-lookup"><span data-stu-id="20cf7-176">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20cf7-177">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="20cf7-177">Minimum supported client</span></span><br/> | <span data-ttu-id="20cf7-178">Windows 8</span><span class="sxs-lookup"><span data-stu-id="20cf7-178">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="20cf7-179">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="20cf7-179">Minimum supported server</span></span><br/> | <span data-ttu-id="20cf7-180">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="20cf7-180">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="20cf7-181">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="20cf7-181">Namespace</span></span><br/>                | <span data-ttu-id="20cf7-182">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="20cf7-182">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="20cf7-183">MOF</span><span class="sxs-lookup"><span data-stu-id="20cf7-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="20cf7-184"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="20cf7-184"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="20cf7-185">DLL</span><span class="sxs-lookup"><span data-stu-id="20cf7-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20cf7-186"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="20cf7-186"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="20cf7-187">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="20cf7-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20cf7-188">**\_ManagementName CIM**</span><span class="sxs-lookup"><span data-stu-id="20cf7-188">**CIM\_ManagedElement**</span></span>](cim-managedelement.md)
</dt> </dl>

 

