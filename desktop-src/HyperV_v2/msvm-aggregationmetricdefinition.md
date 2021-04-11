---
description: Rappresenta gli aspetti della definizione di una metrica derivata da un altro valore della metrica.
ms.assetid: 642f53fe-e51c-4c73-babf-19adb2cf55f4
title: Classe Msvm_AggregationMetricDefinition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AggregationMetricDefinition
- Msvm_AggregationMetricDefinition.InstanceID
- Msvm_AggregationMetricDefinition.Caption
- Msvm_AggregationMetricDefinition.Description
- Msvm_AggregationMetricDefinition.ElementName
- Msvm_AggregationMetricDefinition.Id
- Msvm_AggregationMetricDefinition.Name
- Msvm_AggregationMetricDefinition.DataType
- Msvm_AggregationMetricDefinition.Calculable
- Msvm_AggregationMetricDefinition.Units
- Msvm_AggregationMetricDefinition.BreakdownDimensions
- Msvm_AggregationMetricDefinition.IsContinuous
- Msvm_AggregationMetricDefinition.ChangeType
- Msvm_AggregationMetricDefinition.TimeScope
- Msvm_AggregationMetricDefinition.GatheringType
- Msvm_AggregationMetricDefinition.ProgrammaticUnits
- Msvm_AggregationMetricDefinition.SimpleFunction
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: da52c154c90b58fc147a52268025887d2dfa8f10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232687"
---
# <a name="msvm_aggregationmetricdefinition-class"></a><span data-ttu-id="2a695-103">\_Classe MSVM AggregationMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="2a695-103">Msvm\_AggregationMetricDefinition class</span></span>

<span data-ttu-id="2a695-104">Rappresenta gli aspetti della definizione di una metrica derivata da un altro valore della metrica.</span><span class="sxs-lookup"><span data-stu-id="2a695-104">Represents the definition aspects of a metric that is derived from another metric value.</span></span> <span data-ttu-id="2a695-105">L' **oggetto \_ AggregationMetricDefinition di MSVM** deve essere associato agli elementi gestiti a cui si applica.</span><span class="sxs-lookup"><span data-stu-id="2a695-105">The **Msvm\_AggregationMetricDefinition** object should be associated with the managed elements to which it applies.</span></span>

<span data-ttu-id="2a695-106">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="2a695-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a695-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2a695-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_AggregationMetricDefinition : CIM_AggregationMetricDefinition
{
  string  InstanceID;
  string  Caption;
  string  Description;
  string  ElementName;
  string  Id;
  string  Name;
  uint16  DataType;
  uint16  Calculable;
  string  Units;
  string  BreakdownDimensions[];
  boolean IsContinuous;
  uint16  ChangeType;
  uint16  TimeScope;
  uint16  GatheringType;
  string  ProgrammaticUnits;
  uint16  SimpleFunction;
};
```

## <a name="members"></a><span data-ttu-id="2a695-108">Members</span><span class="sxs-lookup"><span data-stu-id="2a695-108">Members</span></span>

<span data-ttu-id="2a695-109">La **classe \_ AggregationMetricDefinition di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="2a695-109">The **Msvm\_AggregationMetricDefinition** class has these types of members:</span></span>

-   [<span data-ttu-id="2a695-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2a695-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2a695-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2a695-111">Properties</span></span>

<span data-ttu-id="2a695-112">La **classe \_ AggregationMetricDefinition di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="2a695-112">The **Msvm\_AggregationMetricDefinition** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2a695-113">**BreakdownDimensions**</span><span class="sxs-lookup"><span data-stu-id="2a695-113">**BreakdownDimensions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a695-114">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="2a695-114">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2a695-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a695-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a695-116">Definisce una o più stringhe che possono essere utilizzate per perfezionare (suddividere) query sui valori della metrica lungo una determinata dimensione.</span><span class="sxs-lookup"><span data-stu-id="2a695-116">Defines one or more strings that can be used to refine (break down) queries against the metric values along a certain dimension.</span></span> <span data-ttu-id="2a695-117">Un esempio è un nome di transazione, che consente l'interruzione del valore totale di tutte le transazioni in un set di valori, uno per ogni nome di transazione.</span><span class="sxs-lookup"><span data-stu-id="2a695-117">An example is a transaction name, allowing the break down of the total value for all transactions into a set of values, one for each transaction name.</span></span> <span data-ttu-id="2a695-118">Altri esempi possono essere il nome del sistema dell'applicazione o del gruppo di utenti.</span><span class="sxs-lookup"><span data-stu-id="2a695-118">Other examples might be application system or user group name.</span></span> <span data-ttu-id="2a695-119">Le stringhe sono di formato libero e dovrebbero essere significative per gli utenti finali dei dati della metrica.</span><span class="sxs-lookup"><span data-stu-id="2a695-119">The strings are free format and should be meaningful to the end users of the metric data.</span></span> <span data-ttu-id="2a695-120">Le stringhe indicano quali dimensioni di suddivisione sono supportate per questa definizione di metrica dalla strumentazione sottostante.</span><span class="sxs-lookup"><span data-stu-id="2a695-120">The strings indicate which break down dimensions are supported for this metric definition by the underlying instrumentation.</span></span> <span data-ttu-id="2a695-121">Questa proprietà viene ereditata da **CIM \_ BaseMetricDefinition**.</span><span class="sxs-lookup"><span data-stu-id="2a695-121">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>

</dd> <dt>

<span data-ttu-id="2a695-122">**Calcolabile**</span><span class="sxs-lookup"><span data-stu-id="2a695-122">**Calculable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a695-123">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2a695-123">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2a695-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a695-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a695-125">Descrive le caratteristiche della metrica a scopo di esecuzione dei calcoli.</span><span class="sxs-lookup"><span data-stu-id="2a695-125">Describes the characteristics of the metric for purposes of performing calculations.</span></span> <span data-ttu-id="2a695-126">Questa proprietà viene ereditata da **CIM \_ BaseMetricDefinition**.</span><span class="sxs-lookup"><span data-stu-id="2a695-126">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span> <span data-ttu-id="2a695-127">Può essere **null** o uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="2a695-127">This may be **Null** or one of the following values.</span></span>



| <span data-ttu-id="2a695-128">Valore</span><span class="sxs-lookup"><span data-stu-id="2a695-128">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="2a695-129">Significato</span><span class="sxs-lookup"><span data-stu-id="2a695-129">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Non-calculable"></span><span id="non-calculable"></span><span id="NON-CALCULABLE"></span><dl> <span data-ttu-id="2a695-130"><dt>**Non calcolabile**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="2a695-130"><dt>**Non-calculable**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="2a695-131">Non è possibile calcolare il valore.</span><span class="sxs-lookup"><span data-stu-id="2a695-131">The value cannot be calculated.</span></span> <span data-ttu-id="2a695-132">Ad esempio, una stringa.</span><span class="sxs-lookup"><span data-stu-id="2a695-132">For example, a string.</span></span><br/>                                                                                                                                                                                                                                                                                                         |
| <span id="Summable"></span><span id="summable"></span><span id="SUMMABLE"></span><dl> <span data-ttu-id="2a695-133"><dt>**Sommabile**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="2a695-133"><dt>**Summable**</dt> <dt>2</dt></span></span> </dl>                         | <span data-ttu-id="2a695-134">Il valore può essere sommato in molte istanze.</span><span class="sxs-lookup"><span data-stu-id="2a695-134">The value can be summed over many instances.</span></span> <span data-ttu-id="2a695-135">Ad esempio, se ogni processo di backup è un'unità di lavoro e ogni processo esegue il backup di 27.000 file in media, 100 processi di backup elaborati 2,7 milioni file.</span><span class="sxs-lookup"><span data-stu-id="2a695-135">For example, if each backup job is a unit of work, and each job backs up 27,000 files on average, then 100 backup jobs processed 2,700,000 files.</span></span><br/>                                                                                                                                                                 |
| <span id="Non-summable_"></span><span id="non-summable_"></span><span id="NON-SUMMABLE_"></span><dl> <span data-ttu-id="2a695-136"><dt> **Non sommabile**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="2a695-136"><dt>**Non-summable** </dt> <dt>3 </dt></span></span> </dl>    | <span data-ttu-id="2a695-137">Questo valore non può essere sommato in molte istanze.</span><span class="sxs-lookup"><span data-stu-id="2a695-137">This value cannot be summed over many instances.</span></span> <span data-ttu-id="2a695-138">Un esempio è una metrica che misura la lunghezza della coda quando un processo arriva a un server.</span><span class="sxs-lookup"><span data-stu-id="2a695-138">An example would be a metric that measures the queue length when a job arrives at a server.</span></span> <span data-ttu-id="2a695-139">Se ogni processo è un'unità di lavoro e la lunghezza media della coda quando ogni processo arriva è 33, non è sensato dire che la lunghezza della coda per i processi 100 è 3300.</span><span class="sxs-lookup"><span data-stu-id="2a695-139">If each job is a unit of work, and the average queue length when each job arrives is 33, it does not make sense to say that the queue length for 100 jobs is 3300.</span></span> <span data-ttu-id="2a695-140">È sensato dire che la media è 33.</span><span class="sxs-lookup"><span data-stu-id="2a695-140">It does make sense to say that the mean is 33.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2a695-141">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="2a695-141">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a695-142">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2a695-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a695-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a695-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a695-144">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="2a695-144">A short description of the object.</span></span> <span data-ttu-id="2a695-145">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="2a695-145">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="2a695-146">**ChangeType**</span><span class="sxs-lookup"><span data-stu-id="2a695-146">**ChangeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a695-147">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2a695-147">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2a695-148">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a695-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a695-149">Indica il modo in cui viene modificato il valore della metrica, sotto forma di combinazioni tipiche di attributi di granularità più sottili, ad esempio la modifica della direzione, i valori minimo e massimo e la semantica di wrapping.</span><span class="sxs-lookup"><span data-stu-id="2a695-149">Indicates how the metric value changes, in the form of typical combinations of finer grain attributes such as direction change, minimum and maximum values, and wrapping semantics.</span></span> <span data-ttu-id="2a695-150">Questa proprietà viene ereditata da **CIM \_ BaseMetricDefinition**.</span><span class="sxs-lookup"><span data-stu-id="2a695-150">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>



| <span data-ttu-id="2a695-151">Valore</span><span class="sxs-lookup"><span data-stu-id="2a695-151">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="2a695-152">Significato</span><span class="sxs-lookup"><span data-stu-id="2a695-152">Meaning</span></span>                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="2a695-153"><dt>**Sconosciuto**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2a695-153"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="2a695-154">La finestra di progettazione metrica non ha qualificato l'oggetto **ChangeType**.</span><span class="sxs-lookup"><span data-stu-id="2a695-154">The metric designer did not qualify the **ChangeType**.</span></span><br/>                                                                                                                               |
| <span id="N_A"></span><span id="n_a"></span><dl> <span data-ttu-id="2a695-155"><dt>**N/A**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="2a695-155"><dt>**N/A**</dt> <dt>2</dt></span></span> </dl>                                                                                       | <span data-ttu-id="2a695-156">Se la proprietà di **discontinuità** è "false", **ChangeType** non ha senso e deve essere impostato su "N/A".</span><span class="sxs-lookup"><span data-stu-id="2a695-156">If the **IsContinuous** property is "false", **ChangeType** does not make sense and must be set to "N/A".</span></span><br/>                                                                             |
| <span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span><dl> <span data-ttu-id="2a695-157"><dt>**Contatore**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="2a695-157"><dt>**Counter**</dt> <dt>3</dt></span></span> </dl>                                                 | <span data-ttu-id="2a695-158">La metrica è una metrica del contatore.</span><span class="sxs-lookup"><span data-stu-id="2a695-158">The metric is a counter metric.</span></span> <span data-ttu-id="2a695-159">Questi includono valori interi non negativi che aumentano fino a raggiungere il numero massimo rappresentabile, quindi eseguire il wrapping e iniziare ad aumentare da 0.</span><span class="sxs-lookup"><span data-stu-id="2a695-159">These have nonnegative integer values that increase until reaching the maximum representable number and then wrap around and start increasing from 0.</span></span><br/> |
| <span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span><dl> <span data-ttu-id="2a695-160"><dt>**Misuratore**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="2a695-160"><dt>**Gauge**</dt> <dt>4</dt></span></span> </dl>                                                         | <span data-ttu-id="2a695-161">La metrica è una metrica del misuratore.</span><span class="sxs-lookup"><span data-stu-id="2a695-161">The metric is a gauge metric.</span></span> <span data-ttu-id="2a695-162">Hanno valori integer o float che possono aumentare e diminuire in modo arbitrario.</span><span class="sxs-lookup"><span data-stu-id="2a695-162">These have integer or float values that can increase and decrease arbitrarily.</span></span><br/>                                                                          |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="2a695-163"><dt>**DMTF riservato**</dt> <dt>5.. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="2a695-163"><dt>**DMTF Reserved**</dt> <dt>5..32767</dt></span></span> </dl>                  |                                                                                                                                                                                                  |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <span data-ttu-id="2a695-164">32768 <dt> **riservato al fornitore**</dt> <dt>.. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="2a695-164"><dt>**Vendor Reserved** </dt> <dt>32768..65535 </dt></span></span> </dl> | <span data-ttu-id="2a695-165">I fornitori possono estendere la proprietà **ChangeType** nell'intervallo riservato del fornitore.</span><span class="sxs-lookup"><span data-stu-id="2a695-165">Vendors may extend the **ChangeType** property in the vendor reserved range.</span></span><br/>                                                                                                          |



 

</dd> <dt>

<span data-ttu-id="2a695-166">**DataType**</span><span class="sxs-lookup"><span data-stu-id="2a695-166">**DataType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a695-167">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2a695-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2a695-168">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a695-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a695-169">Tipo di dati della metrica.</span><span class="sxs-lookup"><span data-stu-id="2a695-169">The data type of the metric.</span></span> <span data-ttu-id="2a695-170">Questa proprietà viene ereditata da **CIM \_ BaseMetricDefinition**.</span><span class="sxs-lookup"><span data-stu-id="2a695-170">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>

<dl> <dt>

<span data-ttu-id="2a695-171"><span id="boolean"></span><span id="BOOLEAN"></span>**valore booleano** (1)</span><span class="sxs-lookup"><span data-stu-id="2a695-171"><span id="boolean"></span><span id="BOOLEAN"></span>**boolean** (1)</span></span>
</dt> <dt>

<span data-ttu-id="2a695-172"><span id="char16"></span><span id="CHAR16"></span>**Char16** (2)</span><span class="sxs-lookup"><span data-stu-id="2a695-172"><span id="char16"></span><span id="CHAR16"></span>**char16** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2a695-173"><span id="datetime"></span><span id="DATETIME"></span>**DateTime** (3)</span><span class="sxs-lookup"><span data-stu-id="2a695-173"><span id="datetime"></span><span id="DATETIME"></span>**datetime** (3)</span></span>
</dt> <dt>

<span data-ttu-id="2a695-174"><span id="real32"></span><span id="REAL32"></span>**real32** (4)</span><span class="sxs-lookup"><span data-stu-id="2a695-174"><span id="real32"></span><span id="REAL32"></span>**real32** (4)</span></span>
</dt> <dt>

<span data-ttu-id="2a695-175"><span id="real64"></span><span id="REAL64"></span>**real64** (5)</span><span class="sxs-lookup"><span data-stu-id="2a695-175"><span id="real64"></span><span id="REAL64"></span>**real64** (5)</span></span>
</dt> <dt>

<span data-ttu-id="2a695-176"><span id="sint16"></span><span id="SINT16"></span>**sint16** (6)</span><span class="sxs-lookup"><span data-stu-id="2a695-176"><span id="sint16"></span><span id="SINT16"></span>**sint16** (6)</span></span>
</dt> <dt>

<span data-ttu-id="2a695-177"><span id="sint32"></span><span id="SINT32"></span>**sint32** (7)</span><span class="sxs-lookup"><span data-stu-id="2a695-177"><span id="sint32"></span><span id="SINT32"></span>**sint32** (7)</span></span>
</dt> <dt>

<span data-ttu-id="2a695-178"><span id="sint64"></span><span id="SINT64"></span>**sint64** (8)</span><span class="sxs-lookup"><span data-stu-id="2a695-178"><span id="sint64"></span><span id="SINT64"></span>**sint64** (8)</span></span>
</dt> <dt>

<span data-ttu-id="2a695-179"><span id="sint8"></span><span id="SINT8"></span>**sint8** (9)</span><span class="sxs-lookup"><span data-stu-id="2a695-179"><span id="sint8"></span><span id="SINT8"></span>**sint8** (9)</span></span>
</dt> <dt>

<span data-ttu-id="2a695-180"><span id="string"></span><span id="STRING"></span>**stringa** (10)</span><span class="sxs-lookup"><span data-stu-id="2a695-180"><span id="string"></span><span id="STRING"></span>**string** (10)</span></span>
</dt> <dt>

<span data-ttu-id="2a695-181"><span id="uint16"></span><span id="UINT16"></span>**UInt16** (11)</span><span class="sxs-lookup"><span data-stu-id="2a695-181"><span id="uint16"></span><span id="UINT16"></span>**uint16** (11)</span></span>
</dt> <dt>

<span data-ttu-id="2a695-182"><span id="uint32"></span><span id="UINT32"></span>**UInt32** (12)</span><span class="sxs-lookup"><span data-stu-id="2a695-182"><span id="uint32"></span><span id="UINT32"></span>**uint32** (12)</span></span>
</dt> <dt>

<span data-ttu-id="2a695-183"><span id="uint64"></span><span id="UINT64"></span>**UInt64** (13)</span><span class="sxs-lookup"><span data-stu-id="2a695-183"><span id="uint64"></span><span id="UINT64"></span>**uint64** (13)</span></span>
</dt> <dt>

<span data-ttu-id="2a695-184"><span id="uint8_"></span><span id="UINT8_"></span>**Uint8** (14)</span><span class="sxs-lookup"><span data-stu-id="2a695-184"><span id="uint8_"></span><span id="UINT8_"></span>**uint8** (14 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2a695-185">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="2a695-185">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a695-186">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2a695-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a695-187">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a695-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a695-188">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="2a695-188">A description of the object.</span></span> <span data-ttu-id="2a695-189">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="2a695-189">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="2a695-190">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="2a695-190">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a695-191">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2a695-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a695-192">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a695-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a695-193">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="2a695-193">A display name for the object.</span></span> <span data-ttu-id="2a695-194">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="2a695-194">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="2a695-195">**GatheringType**</span><span class="sxs-lookup"><span data-stu-id="2a695-195">**GatheringType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a695-196">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2a695-196">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2a695-197">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a695-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a695-198">Indica il modo in cui i valori delle metriche vengono raccolti dalla strumentazione sottostante.</span><span class="sxs-lookup"><span data-stu-id="2a695-198">Indicates how the metric values are gathered by the underlying instrumentation.</span></span> <span data-ttu-id="2a695-199">Ciò consente all'applicazione client di scegliere la metrica corretta per lo scopo.</span><span class="sxs-lookup"><span data-stu-id="2a695-199">This allows the client application to choose the right metric for the purpose.</span></span> <span data-ttu-id="2a695-200">Questa proprietà viene ereditata da **CIM \_ BaseMetricDefinition**.</span><span class="sxs-lookup"><span data-stu-id="2a695-200">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span> <span data-ttu-id="2a695-201">Può essere **null** o uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="2a695-201">This may be **Null** or one of the following values.</span></span>



| <span data-ttu-id="2a695-202">Valore</span><span class="sxs-lookup"><span data-stu-id="2a695-202">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="2a695-203">Significato</span><span class="sxs-lookup"><span data-stu-id="2a695-203">Meaning</span></span>                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="2a695-204"><dt>**Sconosciuto**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2a695-204"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="2a695-205">Il tipo di raccolta non è noto.</span><span class="sxs-lookup"><span data-stu-id="2a695-205">The gathering type is not known.</span></span><br/>                                                                                                                                                                                                                               |
| <span id="OnChange"></span><span id="onchange"></span><span id="ONCHANGE"></span><dl> <span data-ttu-id="2a695-206"><dt>**OnChange**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="2a695-206"><dt>**OnChange**</dt> <dt>2</dt></span></span> </dl>                                             | <span data-ttu-id="2a695-207">I valori delle metriche vengono aggiornati immediatamente quando i valori all'interno della risorsa misurata cambiano.</span><span class="sxs-lookup"><span data-stu-id="2a695-207">The metric values get updated immediately when the values inside of the measured resource change.</span></span><br/>                                                                                                                                                              |
| <span id="Periodic"></span><span id="periodic"></span><span id="PERIODIC"></span><dl> <span data-ttu-id="2a695-208"><dt>3</dt> <dt>**periodici**</dt></span><span class="sxs-lookup"><span data-stu-id="2a695-208"><dt>**Periodic**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="2a695-209">I valori delle metriche vengono aggiornati periodicamente.</span><span class="sxs-lookup"><span data-stu-id="2a695-209">The metric values get updated periodically.</span></span> <span data-ttu-id="2a695-210">Ad esempio, per un'applicazione client, un valore della metrica che si applica all'ora corrente apparirà costante durante ogni intervallo di raccolta, quindi passa al nuovo valore alla fine di ogni intervallo di raccolta.</span><span class="sxs-lookup"><span data-stu-id="2a695-210">For instance, to a client application, a metric value that applies to the current time will appear constant during each gathering interval, and then jumps to the new value at the end of each gathering interval.</span></span><br/> |
| <span id="OnRequest"></span><span id="onrequest"></span><span id="ONREQUEST"></span><dl> <span data-ttu-id="2a695-211"><dt>**OnRequest**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="2a695-211"><dt>**OnRequest**</dt> <dt>4</dt></span></span> </dl>                                         | <span data-ttu-id="2a695-212">Il valore della metrica viene determinato ogni volta che viene letto da un'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="2a695-212">The metric value is determined each time a client application reads it.</span></span><br/>                                                                                                                                                                                        |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="2a695-213"><dt>**DMTF riservato**</dt> <dt>5.. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="2a695-213"><dt>**DMTF Reserved**</dt> <dt>5..32767</dt></span></span> </dl>                  |                                                                                                                                                                                                                                                                           |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <span data-ttu-id="2a695-214">32768 <dt> **riservato al fornitore**</dt> <dt>.. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="2a695-214"><dt>**Vendor Reserved** </dt> <dt>32768..65535 </dt></span></span> </dl> |                                                                                                                                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="2a695-215">**Id**</span><span class="sxs-lookup"><span data-stu-id="2a695-215">**Id**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a695-216">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2a695-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a695-217">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a695-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a695-218">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="2a695-218">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="2a695-219">Stringa che identifica in modo univoco la definizione della metrica.</span><span class="sxs-lookup"><span data-stu-id="2a695-219">A string that uniquely identifies the metric definition.</span></span> <span data-ttu-id="2a695-220">Questa proprietà viene ereditata da **CIM \_ BaseMetricDefinition**.</span><span class="sxs-lookup"><span data-stu-id="2a695-220">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>

</dd> <dt>

<span data-ttu-id="2a695-221">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2a695-221">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a695-222">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2a695-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a695-223">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a695-223">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a695-224">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="2a695-224">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="2a695-225">Stringa che identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="2a695-225">A string that uniquely identifies an instance of this class.</span></span> <span data-ttu-id="2a695-226">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="2a695-226">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="2a695-227">**IsContinuous**</span><span class="sxs-lookup"><span data-stu-id="2a695-227">**IsContinuous**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a695-228">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="2a695-228">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2a695-229">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a695-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a695-230">Indica se il valore della metrica è continuo o scalare.</span><span class="sxs-lookup"><span data-stu-id="2a695-230">Indicates whether the metric value is continuous or scalar.</span></span> <span data-ttu-id="2a695-231">Le metriche delle prestazioni sono un esempio di metrica continua.</span><span class="sxs-lookup"><span data-stu-id="2a695-231">Performance metrics are an example of a continuous metric.</span></span> <span data-ttu-id="2a695-232">Esempi di metriche scalari includono codici di errore o stati operativi.</span><span class="sxs-lookup"><span data-stu-id="2a695-232">Examples of scalar metrics include error codes or operational states.</span></span> <span data-ttu-id="2a695-233">È possibile confrontare le metriche continue usando la relazione "maggiore di".</span><span class="sxs-lookup"><span data-stu-id="2a695-233">Continuous metrics can be compared by using the "greater than" relation.</span></span> <span data-ttu-id="2a695-234">Questa proprietà viene ereditata da **CIM \_ BaseMetricDefinition**.</span><span class="sxs-lookup"><span data-stu-id="2a695-234">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>

</dd> <dt>

<span data-ttu-id="2a695-235">**Nome**</span><span class="sxs-lookup"><span data-stu-id="2a695-235">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a695-236">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2a695-236">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a695-237">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a695-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a695-238">Nome della metrica.</span><span class="sxs-lookup"><span data-stu-id="2a695-238">The name of the metric.</span></span> <span data-ttu-id="2a695-239">Questa proprietà viene ereditata da **CIM \_ BaseMetricDefinition**.</span><span class="sxs-lookup"><span data-stu-id="2a695-239">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>

</dd> <dt>

<span data-ttu-id="2a695-240">**ProgrammaticUnits**</span><span class="sxs-lookup"><span data-stu-id="2a695-240">**ProgrammaticUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a695-241">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2a695-241">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a695-242">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a695-242">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a695-243">Identifica le unità specifiche di un valore.</span><span class="sxs-lookup"><span data-stu-id="2a695-243">Identifies the specific units of a value.</span></span> <span data-ttu-id="2a695-244">Il valore di questa proprietà sarà un valore valido del qualificatore unità programmatiche come definito nell'Appendice C. 1 di [DSP0004 v 2.4](https://www.dmtf.org/sites/default/files/standards/documents/DSP0004_2.5.0.pdf) o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="2a695-244">The value of this property will be a legal value of the Programmatic Units qualifier as defined in Appendix C.1 of [DSP0004 V2.4](https://www.dmtf.org/sites/default/files/standards/documents/DSP0004_2.5.0.pdf) or later.</span></span> <span data-ttu-id="2a695-245">Questa proprietà viene ereditata da **CIM \_ BaseMetricDefinition**.</span><span class="sxs-lookup"><span data-stu-id="2a695-245">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>

</dd> <dt>

<span data-ttu-id="2a695-246">**SimpleFunction**</span><span class="sxs-lookup"><span data-stu-id="2a695-246">**SimpleFunction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a695-247">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2a695-247">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2a695-248">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="2a695-248">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2a695-249">Identifica il calcolo di base eseguito su una metrica sottostante per giungere al valore di questa metrica derivata.</span><span class="sxs-lookup"><span data-stu-id="2a695-249">Identifies the basic computation performed on an underlying metric to arrive at the value of this derived metric.</span></span> <span data-ttu-id="2a695-250">Questa proprietà viene ereditata da **CIM \_ AggregationMetricDefinition** e sarà uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="2a695-250">This property is inherited from **CIM\_AggregationMetricDefinition** and will be one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="2a695-251"><span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>**Minimo** (2)</span><span class="sxs-lookup"><span data-stu-id="2a695-251"><span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>**Minimum** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2a695-252"><span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Massimo** (3)</span><span class="sxs-lookup"><span data-stu-id="2a695-252"><span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Maximum** (3)</span></span>
</dt> <dt>

<span data-ttu-id="2a695-253"><span id="Average"></span><span id="average"></span><span id="AVERAGE"></span>**Media** (4)</span><span class="sxs-lookup"><span data-stu-id="2a695-253"><span id="Average"></span><span id="average"></span><span id="AVERAGE"></span>**Average** (4)</span></span>
</dt> <dt>

<span data-ttu-id="2a695-254"><span id="Median"></span><span id="median"></span><span id="MEDIAN"></span>**Mediana** (5)</span><span class="sxs-lookup"><span data-stu-id="2a695-254"><span id="Median"></span><span id="median"></span><span id="MEDIAN"></span>**Median** (5)</span></span>
</dt> <dt>

<span data-ttu-id="2a695-255"><span id="Mode"></span><span id="mode"></span><span id="MODE"></span>**Modalità** (6)</span><span class="sxs-lookup"><span data-stu-id="2a695-255"><span id="Mode"></span><span id="mode"></span><span id="MODE"></span>**Mode** (6)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2a695-256">**TimeScope**</span><span class="sxs-lookup"><span data-stu-id="2a695-256">**TimeScope**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a695-257">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2a695-257">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2a695-258">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a695-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a695-259">Indica l'ambito temporale a cui si applica il valore della metrica.</span><span class="sxs-lookup"><span data-stu-id="2a695-259">Indicates the time scope to which the metric value applies.</span></span> <span data-ttu-id="2a695-260">Questa proprietà viene ereditata da **CIM \_ BaseMetricDefinition**.</span><span class="sxs-lookup"><span data-stu-id="2a695-260">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>



| <span data-ttu-id="2a695-261">Valore</span><span class="sxs-lookup"><span data-stu-id="2a695-261">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="2a695-262">Significato</span><span class="sxs-lookup"><span data-stu-id="2a695-262">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="2a695-263"><dt>**Sconosciuto**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2a695-263"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="2a695-264">L'ambito temporale non è stato qualificato dalla finestra di progettazione della metrica o è sconosciuto al provider.</span><span class="sxs-lookup"><span data-stu-id="2a695-264">The time scope was not qualified by the metric designer, or is unknown to the provider.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Point"></span><span id="point"></span><span id="POINT"></span><dl> <span data-ttu-id="2a695-265"><dt>**Punto**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="2a695-265"><dt>**Point**</dt> <dt>2</dt></span></span> </dl>                                                         | <span data-ttu-id="2a695-266">La metrica si applica a un punto nel tempo.</span><span class="sxs-lookup"><span data-stu-id="2a695-266">The metric applies to a point in time.</span></span> <span data-ttu-id="2a695-267">Nelle istanze [**MSVM \_ BaseMetricValue**](msvm-basemetricvalue.md) corrispondenti la proprietà **timestamp** specifica il punto nel tempo e la proprietà **Duration** è sempre 0.</span><span class="sxs-lookup"><span data-stu-id="2a695-267">On the corresponding [**Msvm\_BaseMetricValue**](msvm-basemetricvalue.md) instances, the **TimeStamp** property specifies the point in time, and the **Duration** property is always 0.</span></span><br/>                                                                                                                                                                                                                                                                                              |
| <span id="Interval"></span><span id="interval"></span><span id="INTERVAL"></span><dl> <span data-ttu-id="2a695-268"><dt>**Intervallo**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="2a695-268"><dt>**Interval**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="2a695-269">La metrica si applica a un intervallo di tempo.</span><span class="sxs-lookup"><span data-stu-id="2a695-269">The metric applies to a time interval.</span></span> <span data-ttu-id="2a695-270">Nelle istanze [**MSVM \_ BaseMetricValue**](msvm-basemetricvalue.md) corrispondenti la proprietà **timestamp** specifica la fine dell'intervallo di tempo e la proprietà **Duration** ne specifica la durata.</span><span class="sxs-lookup"><span data-stu-id="2a695-270">On the corresponding [**Msvm\_BaseMetricValue**](msvm-basemetricvalue.md) instances, the **TimeStamp** property specifies the end of the time interval, and the **Duration** property specifies its duration.</span></span><br/>                                                                                                                                                                                                                                                                        |
| <span id="StartupInterval"></span><span id="startupinterval"></span><span id="STARTUPINTERVAL"></span><dl> <span data-ttu-id="2a695-271"><dt>**StartupInterval**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="2a695-271"><dt>**StartupInterval**</dt> <dt>4</dt></span></span> </dl>                 | <span data-ttu-id="2a695-272">La metrica si applica a un intervallo di tempo che inizia all'avvio della risorsa misurata (ovvero l'oggetto gestito associato da MetricDefForMe).</span><span class="sxs-lookup"><span data-stu-id="2a695-272">The metric applies to a time interval that began at the startup of the measured resource (that is, the ManagedElement associated by MetricDefForMe).</span></span> <span data-ttu-id="2a695-273">Nelle istanze [**MSVM \_ BaseMetricValue**](msvm-basemetricvalue.md) corrispondenti la proprietà **timestamp** specifica la fine dell'intervallo di tempo.</span><span class="sxs-lookup"><span data-stu-id="2a695-273">On the corresponding [**Msvm\_BaseMetricValue**](msvm-basemetricvalue.md) instances, the **TimeStamp** property specifies the end of the time interval.</span></span> <span data-ttu-id="2a695-274">Se la proprietà **Duration** è 0, indica che il tempo di avvio della risorsa misurata è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="2a695-274">If the **Duration** property is 0, this indicates that the startup time of the measured resource is unknown.</span></span> <span data-ttu-id="2a695-275">In caso contrario, **Duration** specifica la durata tra l'avvio della risorsa e il **timestamp**.</span><span class="sxs-lookup"><span data-stu-id="2a695-275">Otherwise, **Duration** specifies the duration between startup of the resource and **TimeStamp**.</span></span><br/> |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="2a695-276"><dt>**DMTF riservato**</dt> <dt>5.. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="2a695-276"><dt>**DMTF Reserved**</dt> <dt>5..32767</dt></span></span> </dl>                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <span data-ttu-id="2a695-277">32768 <dt> **riservato al fornitore**</dt> <dt>.. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="2a695-277"><dt>**Vendor Reserved** </dt> <dt>32768..65535 </dt></span></span> </dl> |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

</dd> <dt>

<span data-ttu-id="2a695-278">**Unità**</span><span class="sxs-lookup"><span data-stu-id="2a695-278">**Units**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a695-279">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="2a695-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a695-280">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="2a695-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2a695-281">Identifica le unità di un valore, ad esempio "megabyte".</span><span class="sxs-lookup"><span data-stu-id="2a695-281">Identifies the units of a value, for example, "megabytes".</span></span> <span data-ttu-id="2a695-282">Questa proprietà viene ereditata da **CIM \_ BaseMetricDefinition**.</span><span class="sxs-lookup"><span data-stu-id="2a695-282">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2a695-283">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2a695-283">Requirements</span></span>



| <span data-ttu-id="2a695-284">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a695-284">Requirement</span></span> | <span data-ttu-id="2a695-285">Valore</span><span class="sxs-lookup"><span data-stu-id="2a695-285">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a695-286">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2a695-286">Minimum supported client</span></span><br/> | <span data-ttu-id="2a695-287">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="2a695-287">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="2a695-288">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2a695-288">Minimum supported server</span></span><br/> | <span data-ttu-id="2a695-289">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="2a695-289">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2a695-290">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2a695-290">Namespace</span></span><br/>                | <span data-ttu-id="2a695-291">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="2a695-291">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="2a695-292">MOF</span><span class="sxs-lookup"><span data-stu-id="2a695-292">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2a695-293"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2a695-293"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2a695-294">DLL</span><span class="sxs-lookup"><span data-stu-id="2a695-294">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2a695-295"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2a695-295"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

