---
description: Rappresenta gli aspetti della definizione di una metrica.
ms.assetid: 861a69f6-a3bf-4e18-a9c2-931632e3cccc
title: Classe Msvm_BaseMetricDefinition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BaseMetricDefinition
- Msvm_BaseMetricDefinition.InstanceID
- Msvm_BaseMetricDefinition.Caption
- Msvm_BaseMetricDefinition.Description
- Msvm_BaseMetricDefinition.ElementName
- Msvm_BaseMetricDefinition.Id
- Msvm_BaseMetricDefinition.Name
- Msvm_BaseMetricDefinition.DataType
- Msvm_BaseMetricDefinition.Calculable
- Msvm_BaseMetricDefinition.Units
- Msvm_BaseMetricDefinition.BreakdownDimensions
- Msvm_BaseMetricDefinition.IsContinuous
- Msvm_BaseMetricDefinition.ChangeType
- Msvm_BaseMetricDefinition.TimeScope
- Msvm_BaseMetricDefinition.GatheringType
- Msvm_BaseMetricDefinition.ProgrammaticUnits
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8d1edbd722e3bf87631371b5650576917a7cfb39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319520"
---
# <a name="msvm_basemetricdefinition-class"></a><span data-ttu-id="9dea1-103">\_Classe MSVM BaseMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="9dea1-103">Msvm\_BaseMetricDefinition class</span></span>

<span data-ttu-id="9dea1-104">Rappresenta gli aspetti della definizione di una metrica.</span><span class="sxs-lookup"><span data-stu-id="9dea1-104">Represents the definition aspects of a metric.</span></span> <span data-ttu-id="9dea1-105">La **classe \_ BaseMetricDefinition di MSVM** deve essere associata al [**\_ ManagedElements CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) a cui si applica.</span><span class="sxs-lookup"><span data-stu-id="9dea1-105">The **Msvm\_BaseMetricDefinition** class should be associated with the [**CIM\_ManagedElements**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) to which it applies.</span></span>

<span data-ttu-id="9dea1-106">La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="9dea1-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9dea1-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9dea1-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BaseMetricDefinition : CIM_BaseMetricDefinition
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
};
```

## <a name="members"></a><span data-ttu-id="9dea1-108">Members</span><span class="sxs-lookup"><span data-stu-id="9dea1-108">Members</span></span>

<span data-ttu-id="9dea1-109">La **classe \_ BaseMetricDefinition di MSVM** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="9dea1-109">The **Msvm\_BaseMetricDefinition** class has these types of members:</span></span>

-   [<span data-ttu-id="9dea1-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9dea1-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9dea1-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="9dea1-111">Properties</span></span>

<span data-ttu-id="9dea1-112">La **classe \_ BaseMetricDefinition di MSVM** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="9dea1-112">The **Msvm\_BaseMetricDefinition** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9dea1-113">**BreakdownDimensions**</span><span class="sxs-lookup"><span data-stu-id="9dea1-113">**BreakdownDimensions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dea1-114">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="9dea1-114">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9dea1-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9dea1-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9dea1-116">Definisce una o più stringhe che possono essere utilizzate per perfezionare (suddividere) query sui valori della metrica lungo una determinata dimensione.</span><span class="sxs-lookup"><span data-stu-id="9dea1-116">Defines one or more strings that can be used to refine (break down) queries against the metric values along a certain dimension.</span></span> <span data-ttu-id="9dea1-117">Un esempio è un nome di transazione, che consente l'interruzione del valore totale di tutte le transazioni in un set di valori, uno per ogni nome di transazione.</span><span class="sxs-lookup"><span data-stu-id="9dea1-117">An example is a transaction name, allowing the break down of the total value for all transactions into a set of values, one for each transaction name.</span></span> <span data-ttu-id="9dea1-118">Altri esempi possono essere il nome del sistema dell'applicazione o del gruppo di utenti.</span><span class="sxs-lookup"><span data-stu-id="9dea1-118">Other examples might be application system or user group name.</span></span> <span data-ttu-id="9dea1-119">Le stringhe sono di formato libero e dovrebbero essere significative per gli utenti finali dei dati della metrica.</span><span class="sxs-lookup"><span data-stu-id="9dea1-119">The strings are free format and should be meaningful to the end users of the metric data.</span></span> <span data-ttu-id="9dea1-120">Le stringhe indicano quali dimensioni di suddivisione sono supportate per questa definizione di metrica, dalla strumentazione sottostante.</span><span class="sxs-lookup"><span data-stu-id="9dea1-120">The strings indicate which break down dimensions are supported for this metric definition, by the underlying instrumentation.</span></span> <span data-ttu-id="9dea1-121">Questa proprietà viene ereditata da **CIM \_ BaseMetricDefinition**.</span><span class="sxs-lookup"><span data-stu-id="9dea1-121">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>

</dd> <dt>

<span data-ttu-id="9dea1-122">**Calcolabile**</span><span class="sxs-lookup"><span data-stu-id="9dea1-122">**Calculable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dea1-123">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9dea1-123">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9dea1-124">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9dea1-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9dea1-125">Descrive le caratteristiche della metrica a scopo di esecuzione dei calcoli.</span><span class="sxs-lookup"><span data-stu-id="9dea1-125">Describes the characteristics of the metric for purposes of performing calculations.</span></span> <span data-ttu-id="9dea1-126">Questa proprietà viene ereditata da **CIM \_ BaseMetricDefinition**.</span><span class="sxs-lookup"><span data-stu-id="9dea1-126">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span> <span data-ttu-id="9dea1-127">Può essere **null** o uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="9dea1-127">This may be **Null** or one of the following values.</span></span>



| <span data-ttu-id="9dea1-128">Valore</span><span class="sxs-lookup"><span data-stu-id="9dea1-128">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="9dea1-129">Significato</span><span class="sxs-lookup"><span data-stu-id="9dea1-129">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Non-calculable"></span><span id="non-calculable"></span><span id="NON-CALCULABLE"></span><dl> <span data-ttu-id="9dea1-130"><dt>**Non calcolabile**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="9dea1-130"><dt>**Non-calculable**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="9dea1-131">Non è possibile calcolare il valore.</span><span class="sxs-lookup"><span data-stu-id="9dea1-131">The value cannot be calculated.</span></span> <span data-ttu-id="9dea1-132">Ad esempio, una stringa.</span><span class="sxs-lookup"><span data-stu-id="9dea1-132">For example, a string.</span></span><br/>                                                                                                                                                                                                                                                                                                         |
| <span id="Summable"></span><span id="summable"></span><span id="SUMMABLE"></span><dl> <span data-ttu-id="9dea1-133"><dt>**Sommabile**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="9dea1-133"><dt>**Summable**</dt> <dt>2</dt></span></span> </dl>                         | <span data-ttu-id="9dea1-134">Il valore può essere sommato in molte istanze.</span><span class="sxs-lookup"><span data-stu-id="9dea1-134">The value can be summed over many instances.</span></span> <span data-ttu-id="9dea1-135">Ad esempio, se ogni processo di backup è un'unità di lavoro e ogni processo esegue il backup di 27.000 file in media, 100 processi di backup elaborati 2,7 milioni file.</span><span class="sxs-lookup"><span data-stu-id="9dea1-135">For example, if each backup job is a unit of work, and each job backs up 27,000 files on average, then 100 backup jobs processed 2,700,000 files.</span></span><br/>                                                                                                                                                                 |
| <span id="Non-summable_"></span><span id="non-summable_"></span><span id="NON-SUMMABLE_"></span><dl> <span data-ttu-id="9dea1-136"><dt> **Non sommabile**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="9dea1-136"><dt>**Non-summable** </dt> <dt>3 </dt></span></span> </dl>    | <span data-ttu-id="9dea1-137">Questo valore non può essere sommato in molte istanze.</span><span class="sxs-lookup"><span data-stu-id="9dea1-137">This value cannot be summed over many instances.</span></span> <span data-ttu-id="9dea1-138">Un esempio è una metrica che misura la lunghezza della coda quando un processo arriva a un server.</span><span class="sxs-lookup"><span data-stu-id="9dea1-138">An example would be a metric that measures the queue length when a job arrives at a server.</span></span> <span data-ttu-id="9dea1-139">Se ogni processo è un'unità di lavoro e la lunghezza media della coda quando ogni processo arriva è 33, non è sensato dire che la lunghezza della coda per i processi 100 è 3300.</span><span class="sxs-lookup"><span data-stu-id="9dea1-139">If each job is a unit of work, and the average queue length when each job arrives is 33, it does not make sense to say that the queue length for 100 jobs is 3300.</span></span> <span data-ttu-id="9dea1-140">È sensato dire che la media è 33.</span><span class="sxs-lookup"><span data-stu-id="9dea1-140">It does make sense to say that the mean is 33.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9dea1-141">**Didascalia**</span><span class="sxs-lookup"><span data-stu-id="9dea1-141">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dea1-142">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9dea1-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9dea1-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9dea1-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9dea1-144">Breve descrizione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="9dea1-144">A short description of the object.</span></span> <span data-ttu-id="9dea1-145">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="9dea1-145">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9dea1-146">**ChangeType**</span><span class="sxs-lookup"><span data-stu-id="9dea1-146">**ChangeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dea1-147">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9dea1-147">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9dea1-148">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9dea1-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9dea1-149">Indica il modo in cui viene modificato il valore della metrica, sotto forma di combinazioni tipiche di attributi di granularità più sottili, ad esempio la modifica della direzione, i valori minimo e massimo e la semantica di wrapping.</span><span class="sxs-lookup"><span data-stu-id="9dea1-149">Indicates how the metric value changes, in the form of typical combinations of finer grain attributes such as direction change, minimum and maximum values, and wrapping semantics.</span></span> <span data-ttu-id="9dea1-150">Questa proprietà viene ereditata da **CIM \_ BaseMetricDefinition**.</span><span class="sxs-lookup"><span data-stu-id="9dea1-150">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>



| <span data-ttu-id="9dea1-151">Valore</span><span class="sxs-lookup"><span data-stu-id="9dea1-151">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="9dea1-152">Significato</span><span class="sxs-lookup"><span data-stu-id="9dea1-152">Meaning</span></span>                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="9dea1-153"><dt>**Sconosciuto**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="9dea1-153"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="9dea1-154">La finestra di progettazione metrica non ha qualificato il **ChangeType.**</span><span class="sxs-lookup"><span data-stu-id="9dea1-154">The metric designer did not qualify the **ChangeType.**.</span></span><br/>                                                                                                                              |
| <span id="N_A"></span><span id="n_a"></span><dl> <span data-ttu-id="9dea1-155"><dt>**N/A**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="9dea1-155"><dt>**N/A**</dt> <dt>2</dt></span></span> </dl>                                                                                       | <span data-ttu-id="9dea1-156">Se la proprietà di **discontinuità** è "false", **ChangeType** non ha senso e deve essere impostato su "N/A".</span><span class="sxs-lookup"><span data-stu-id="9dea1-156">If the **IsContinuous** property is "false", **ChangeType** does not make sense and must be set to "N/A".</span></span><br/>                                                                             |
| <span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span><dl> <span data-ttu-id="9dea1-157"><dt>**Contatore**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="9dea1-157"><dt>**Counter**</dt> <dt>3</dt></span></span> </dl>                                                 | <span data-ttu-id="9dea1-158">La metrica è una metrica del contatore.</span><span class="sxs-lookup"><span data-stu-id="9dea1-158">The metric is a counter metric.</span></span> <span data-ttu-id="9dea1-159">Questi includono valori interi non negativi che aumentano fino a raggiungere il numero massimo rappresentabile, quindi eseguire il wrapping e iniziare ad aumentare da 0.</span><span class="sxs-lookup"><span data-stu-id="9dea1-159">These have nonnegative integer values that increase until reaching the maximum representable number and then wrap around and start increasing from 0.</span></span><br/> |
| <span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span><dl> <span data-ttu-id="9dea1-160"><dt>**Misuratore**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="9dea1-160"><dt>**Gauge**</dt> <dt>4</dt></span></span> </dl>                                                         | <span data-ttu-id="9dea1-161">La metrica è una metrica del misuratore.</span><span class="sxs-lookup"><span data-stu-id="9dea1-161">The metric is a gauge metric.</span></span> <span data-ttu-id="9dea1-162">Hanno valori integer o float che possono aumentare e diminuire in modo arbitrario.</span><span class="sxs-lookup"><span data-stu-id="9dea1-162">These have integer or float values that can increase and decrease arbitrarily.</span></span><br/>                                                                          |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="9dea1-163"><dt>**DMTF riservato**</dt> <dt>5.. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="9dea1-163"><dt>**DMTF Reserved**</dt> <dt>5..32767</dt></span></span> </dl>                  |                                                                                                                                                                                                  |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <span data-ttu-id="9dea1-164">32768 <dt> **riservato al fornitore**</dt> <dt>.. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="9dea1-164"><dt>**Vendor Reserved** </dt> <dt>32768..65535 </dt></span></span> </dl> | <span data-ttu-id="9dea1-165">I fornitori possono estendere la proprietà **ChangeType** nell'intervallo riservato del fornitore.</span><span class="sxs-lookup"><span data-stu-id="9dea1-165">Vendors may extend the **ChangeType** property in the vendor reserved range.</span></span><br/>                                                                                                          |



 

</dd> <dt>

<span data-ttu-id="9dea1-166">**DataType**</span><span class="sxs-lookup"><span data-stu-id="9dea1-166">**DataType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dea1-167">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9dea1-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9dea1-168">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9dea1-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9dea1-169">Tipo di dati della metrica.</span><span class="sxs-lookup"><span data-stu-id="9dea1-169">The data type of the metric.</span></span> <span data-ttu-id="9dea1-170">Questa proprietà viene ereditata da **CIM \_ BaseMetricDefinition**.</span><span class="sxs-lookup"><span data-stu-id="9dea1-170">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>

<dl> <dt>

<span data-ttu-id="9dea1-171"><span id="boolean"></span><span id="BOOLEAN"></span>**valore booleano** (1)</span><span class="sxs-lookup"><span data-stu-id="9dea1-171"><span id="boolean"></span><span id="BOOLEAN"></span>**boolean** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9dea1-172"><span id="char16"></span><span id="CHAR16"></span>**Char16** (2)</span><span class="sxs-lookup"><span data-stu-id="9dea1-172"><span id="char16"></span><span id="CHAR16"></span>**char16** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9dea1-173"><span id="datetime"></span><span id="DATETIME"></span>**DateTime** (3)</span><span class="sxs-lookup"><span data-stu-id="9dea1-173"><span id="datetime"></span><span id="DATETIME"></span>**datetime** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9dea1-174"><span id="real32"></span><span id="REAL32"></span>**real32** (4)</span><span class="sxs-lookup"><span data-stu-id="9dea1-174"><span id="real32"></span><span id="REAL32"></span>**real32** (4)</span></span>
</dt> <dt>

<span data-ttu-id="9dea1-175"><span id="real64"></span><span id="REAL64"></span>**real64** (5)</span><span class="sxs-lookup"><span data-stu-id="9dea1-175"><span id="real64"></span><span id="REAL64"></span>**real64** (5)</span></span>
</dt> <dt>

<span data-ttu-id="9dea1-176"><span id="sint16"></span><span id="SINT16"></span>**sint16** (6)</span><span class="sxs-lookup"><span data-stu-id="9dea1-176"><span id="sint16"></span><span id="SINT16"></span>**sint16** (6)</span></span>
</dt> <dt>

<span data-ttu-id="9dea1-177"><span id="sint32"></span><span id="SINT32"></span>**sint32** (7)</span><span class="sxs-lookup"><span data-stu-id="9dea1-177"><span id="sint32"></span><span id="SINT32"></span>**sint32** (7)</span></span>
</dt> <dt>

<span data-ttu-id="9dea1-178"><span id="sint64"></span><span id="SINT64"></span>**sint64** (8)</span><span class="sxs-lookup"><span data-stu-id="9dea1-178"><span id="sint64"></span><span id="SINT64"></span>**sint64** (8)</span></span>
</dt> <dt>

<span data-ttu-id="9dea1-179"><span id="sint8"></span><span id="SINT8"></span>**sint8** (9)</span><span class="sxs-lookup"><span data-stu-id="9dea1-179"><span id="sint8"></span><span id="SINT8"></span>**sint8** (9)</span></span>
</dt> <dt>

<span data-ttu-id="9dea1-180"><span id="string"></span><span id="STRING"></span>**stringa** (10)</span><span class="sxs-lookup"><span data-stu-id="9dea1-180"><span id="string"></span><span id="STRING"></span>**string** (10)</span></span>
</dt> <dt>

<span data-ttu-id="9dea1-181"><span id="uint16"></span><span id="UINT16"></span>**UInt16** (11)</span><span class="sxs-lookup"><span data-stu-id="9dea1-181"><span id="uint16"></span><span id="UINT16"></span>**uint16** (11)</span></span>
</dt> <dt>

<span data-ttu-id="9dea1-182"><span id="uint32"></span><span id="UINT32"></span>**UInt32** (12)</span><span class="sxs-lookup"><span data-stu-id="9dea1-182"><span id="uint32"></span><span id="UINT32"></span>**uint32** (12)</span></span>
</dt> <dt>

<span data-ttu-id="9dea1-183"><span id="uint64"></span><span id="UINT64"></span>**UInt64** (13)</span><span class="sxs-lookup"><span data-stu-id="9dea1-183"><span id="uint64"></span><span id="UINT64"></span>**uint64** (13)</span></span>
</dt> <dt>

<span data-ttu-id="9dea1-184"><span id="uint8_"></span><span id="UINT8_"></span>**Uint8** (14)</span><span class="sxs-lookup"><span data-stu-id="9dea1-184"><span id="uint8_"></span><span id="UINT8_"></span>**uint8** (14 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9dea1-185">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="9dea1-185">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dea1-186">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9dea1-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9dea1-187">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9dea1-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9dea1-188">Descrizione dell'oggetto .</span><span class="sxs-lookup"><span data-stu-id="9dea1-188">A description of the object.</span></span> <span data-ttu-id="9dea1-189">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="9dea1-189">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9dea1-190">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="9dea1-190">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dea1-191">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9dea1-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9dea1-192">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9dea1-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9dea1-193">Nome visualizzato per l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="9dea1-193">A display name for the object.</span></span> <span data-ttu-id="9dea1-194">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="9dea1-194">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9dea1-195">**GatheringType**</span><span class="sxs-lookup"><span data-stu-id="9dea1-195">**GatheringType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dea1-196">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9dea1-196">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9dea1-197">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9dea1-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9dea1-198">Indica il modo in cui i valori delle metriche vengono raccolti dalla strumentazione sottostante.</span><span class="sxs-lookup"><span data-stu-id="9dea1-198">Indicates how the metric values are gathered by the underlying instrumentation.</span></span> <span data-ttu-id="9dea1-199">Ciò consente all'applicazione client di scegliere la metrica corretta per lo scopo.</span><span class="sxs-lookup"><span data-stu-id="9dea1-199">This allows the client application to choose the right metric for the purpose.</span></span> <span data-ttu-id="9dea1-200">Questa proprietà viene ereditata da **CIM \_ BaseMetricDefinition**.</span><span class="sxs-lookup"><span data-stu-id="9dea1-200">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span> <span data-ttu-id="9dea1-201">Può essere **null** o uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="9dea1-201">This may be **Null** or one of the following values.</span></span>



| <span data-ttu-id="9dea1-202">Valore</span><span class="sxs-lookup"><span data-stu-id="9dea1-202">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="9dea1-203">Significato</span><span class="sxs-lookup"><span data-stu-id="9dea1-203">Meaning</span></span>                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="9dea1-204"><dt>**Sconosciuto**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="9dea1-204"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="9dea1-205">Il tipo di raccolta non è noto.</span><span class="sxs-lookup"><span data-stu-id="9dea1-205">The gathering type is not known.</span></span><br/>                                                                                                                                                                                                                               |
| <span id="OnChange"></span><span id="onchange"></span><span id="ONCHANGE"></span><dl> <span data-ttu-id="9dea1-206"><dt>**OnChange**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="9dea1-206"><dt>**OnChange**</dt> <dt>2</dt></span></span> </dl>                                             | <span data-ttu-id="9dea1-207">I valori delle metriche vengono aggiornati immediatamente quando i valori all'interno della risorsa misurata cambiano.</span><span class="sxs-lookup"><span data-stu-id="9dea1-207">The metric values get updated immediately when the values inside of the measured resource change.</span></span><br/>                                                                                                                                                              |
| <span id="Periodic"></span><span id="periodic"></span><span id="PERIODIC"></span><dl> <span data-ttu-id="9dea1-208"><dt>3</dt> <dt>**periodici**</dt></span><span class="sxs-lookup"><span data-stu-id="9dea1-208"><dt>**Periodic**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="9dea1-209">I valori delle metriche vengono aggiornati periodicamente.</span><span class="sxs-lookup"><span data-stu-id="9dea1-209">The metric values get updated periodically.</span></span> <span data-ttu-id="9dea1-210">Ad esempio, per un'applicazione client, un valore della metrica che si applica all'ora corrente apparirà costante durante ogni intervallo di raccolta, quindi passa al nuovo valore alla fine di ogni intervallo di raccolta.</span><span class="sxs-lookup"><span data-stu-id="9dea1-210">For instance, to a client application, a metric value that applies to the current time will appear constant during each gathering interval, and then jumps to the new value at the end of each gathering interval.</span></span><br/> |
| <span id="OnRequest"></span><span id="onrequest"></span><span id="ONREQUEST"></span><dl> <span data-ttu-id="9dea1-211"><dt>**OnRequest**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="9dea1-211"><dt>**OnRequest**</dt> <dt>4</dt></span></span> </dl>                                         | <span data-ttu-id="9dea1-212">Il valore della metrica viene determinato ogni volta che viene letto da un'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="9dea1-212">The metric value is determined each time a client application reads it.</span></span><br/>                                                                                                                                                                                        |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="9dea1-213"><dt>**DMTF riservato**</dt> <dt>5.. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="9dea1-213"><dt>**DMTF Reserved**</dt> <dt>5..32767</dt></span></span> </dl>                  |                                                                                                                                                                                                                                                                           |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <span data-ttu-id="9dea1-214">32768 <dt> **riservato al fornitore**</dt> <dt>.. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="9dea1-214"><dt>**Vendor Reserved** </dt> <dt>32768..65535 </dt></span></span> </dl> |                                                                                                                                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="9dea1-215">**Id**</span><span class="sxs-lookup"><span data-stu-id="9dea1-215">**Id**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dea1-216">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9dea1-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9dea1-217">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9dea1-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9dea1-218">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="9dea1-218">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="9dea1-219">Stringa che identifica in modo univoco la definizione della metrica.</span><span class="sxs-lookup"><span data-stu-id="9dea1-219">A string that uniquely identifies the metric definition.</span></span> <span data-ttu-id="9dea1-220">Questa proprietà viene ereditata da **CIM \_ BaseMetricDefinition**.</span><span class="sxs-lookup"><span data-stu-id="9dea1-220">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>

</dd> <dt>

<span data-ttu-id="9dea1-221">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="9dea1-221">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dea1-222">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9dea1-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9dea1-223">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9dea1-223">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9dea1-224">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="9dea1-224">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="9dea1-225">Stringa che identifica in modo univoco un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="9dea1-225">A string that uniquely identifies an instance of this class.</span></span> <span data-ttu-id="9dea1-226">Questa proprietà viene ereditata da [**CIM \_ managementelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="9dea1-226">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9dea1-227">**IsContinuous**</span><span class="sxs-lookup"><span data-stu-id="9dea1-227">**IsContinuous**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dea1-228">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="9dea1-228">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9dea1-229">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9dea1-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9dea1-230">Indica se il valore della metrica è continuo o scalare.</span><span class="sxs-lookup"><span data-stu-id="9dea1-230">Indicates whether the metric value is continuous or scalar.</span></span> <span data-ttu-id="9dea1-231">Le metriche delle prestazioni sono un esempio di metrica continua.</span><span class="sxs-lookup"><span data-stu-id="9dea1-231">Performance metrics are an example of a continuous metric.</span></span> <span data-ttu-id="9dea1-232">Esempi di metriche scalari includono codici di errore o stati operativi.</span><span class="sxs-lookup"><span data-stu-id="9dea1-232">Examples of scalar metrics include error codes or operational states.</span></span> <span data-ttu-id="9dea1-233">È possibile confrontare le metriche continue usando la relazione "maggiore di".</span><span class="sxs-lookup"><span data-stu-id="9dea1-233">Continuous metrics can be compared by using the "greater than" relation.</span></span> <span data-ttu-id="9dea1-234">Questa proprietà viene ereditata da **CIM \_ BaseMetricDefinition**.</span><span class="sxs-lookup"><span data-stu-id="9dea1-234">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>

</dd> <dt>

<span data-ttu-id="9dea1-235">**Nome**</span><span class="sxs-lookup"><span data-stu-id="9dea1-235">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dea1-236">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9dea1-236">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9dea1-237">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9dea1-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9dea1-238">Nome della metrica.</span><span class="sxs-lookup"><span data-stu-id="9dea1-238">The name of the metric.</span></span> <span data-ttu-id="9dea1-239">Questa proprietà viene ereditata da **CIM \_ BaseMetricDefinition**.</span><span class="sxs-lookup"><span data-stu-id="9dea1-239">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>

</dd> <dt>

<span data-ttu-id="9dea1-240">**ProgrammaticUnits**</span><span class="sxs-lookup"><span data-stu-id="9dea1-240">**ProgrammaticUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dea1-241">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9dea1-241">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9dea1-242">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9dea1-242">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9dea1-243">Identifica le unità specifiche di un valore.</span><span class="sxs-lookup"><span data-stu-id="9dea1-243">Identifies the specific units of a value.</span></span> <span data-ttu-id="9dea1-244">Il valore di questa proprietà sarà un valore valido del qualificatore unità programmatiche come definito nell'Appendice C. 1 di [DSP0004 v 2.4](https://www.dmtf.org/sites/default/files/standards/documents/DSP0004_2.5.0.pdf) o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="9dea1-244">The value of this property will be a legal value of the Programmatic Units qualifier as defined in Appendix C.1 of [DSP0004 V2.4](https://www.dmtf.org/sites/default/files/standards/documents/DSP0004_2.5.0.pdf) or later.</span></span> <span data-ttu-id="9dea1-245">Questa proprietà viene ereditata da **CIM \_ BaseMetricDefinition**.</span><span class="sxs-lookup"><span data-stu-id="9dea1-245">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>

</dd> <dt>

<span data-ttu-id="9dea1-246">**TimeScope**</span><span class="sxs-lookup"><span data-stu-id="9dea1-246">**TimeScope**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dea1-247">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9dea1-247">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9dea1-248">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9dea1-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9dea1-249">Indica l'ambito temporale a cui si applica il valore della metrica.</span><span class="sxs-lookup"><span data-stu-id="9dea1-249">Indicates the time scope to which the metric value applies.</span></span> <span data-ttu-id="9dea1-250">Questa proprietà viene ereditata da **CIM \_ BaseMetricDefinition**.</span><span class="sxs-lookup"><span data-stu-id="9dea1-250">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>



| <span data-ttu-id="9dea1-251">Valore</span><span class="sxs-lookup"><span data-stu-id="9dea1-251">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="9dea1-252">Significato</span><span class="sxs-lookup"><span data-stu-id="9dea1-252">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="9dea1-253"><dt>**Sconosciuto**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="9dea1-253"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="9dea1-254">L'ambito temporale non è stato qualificato dalla finestra di progettazione della metrica o è sconosciuto al provider.</span><span class="sxs-lookup"><span data-stu-id="9dea1-254">The time scope was not qualified by the metric designer or is unknown to the provider.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="Point"></span><span id="point"></span><span id="POINT"></span><dl> <span data-ttu-id="9dea1-255"><dt>**Punto**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="9dea1-255"><dt>**Point**</dt> <dt>2</dt></span></span> </dl>                                                         | <span data-ttu-id="9dea1-256">La metrica si applica a un punto nel tempo.</span><span class="sxs-lookup"><span data-stu-id="9dea1-256">The metric applies to a point in time.</span></span> <span data-ttu-id="9dea1-257">Nelle istanze [**MSVM \_ BaseMetricValue**](msvm-basemetricvalue.md) corrispondenti la proprietà **timestamp** specifica il punto nel tempo e la proprietà **Duration** è sempre 0.</span><span class="sxs-lookup"><span data-stu-id="9dea1-257">On the corresponding [**Msvm\_BaseMetricValue**](msvm-basemetricvalue.md) instances, the **TimeStamp** property specifies the point in time, and the **Duration** property is always 0.</span></span><br/>                                                                                                                                                                                                                                                                                              |
| <span id="Interval"></span><span id="interval"></span><span id="INTERVAL"></span><dl> <span data-ttu-id="9dea1-258"><dt>**Intervallo**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="9dea1-258"><dt>**Interval**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="9dea1-259">La metrica si applica a un intervallo di tempo.</span><span class="sxs-lookup"><span data-stu-id="9dea1-259">The metric applies to a time interval.</span></span> <span data-ttu-id="9dea1-260">Nelle istanze [**MSVM \_ BaseMetricValue**](msvm-basemetricvalue.md) corrispondenti la proprietà **timestamp** specifica la fine dell'intervallo di tempo e la proprietà **Duration** ne specifica la durata.</span><span class="sxs-lookup"><span data-stu-id="9dea1-260">On the corresponding [**Msvm\_BaseMetricValue**](msvm-basemetricvalue.md) instances, the **TimeStamp** property specifies the end of the time interval, and the **Duration** property specifies its duration.</span></span><br/>                                                                                                                                                                                                                                                                        |
| <span id="StartupInterval"></span><span id="startupinterval"></span><span id="STARTUPINTERVAL"></span><dl> <span data-ttu-id="9dea1-261"><dt>**StartupInterval**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="9dea1-261"><dt>**StartupInterval**</dt> <dt>4</dt></span></span> </dl>                 | <span data-ttu-id="9dea1-262">La metrica si applica a un intervallo di tempo che inizia all'avvio della risorsa misurata (ovvero l'oggetto gestito associato da MetricDefForMe).</span><span class="sxs-lookup"><span data-stu-id="9dea1-262">The metric applies to a time interval that began at the startup of the measured resource (that is, the ManagedElement associated by MetricDefForMe).</span></span> <span data-ttu-id="9dea1-263">Nelle istanze [**MSVM \_ BaseMetricValue**](msvm-basemetricvalue.md) corrispondenti la proprietà **timestamp** specifica la fine dell'intervallo di tempo.</span><span class="sxs-lookup"><span data-stu-id="9dea1-263">On the corresponding [**Msvm\_BaseMetricValue**](msvm-basemetricvalue.md) instances, the **TimeStamp** property specifies the end of the time interval.</span></span> <span data-ttu-id="9dea1-264">Se la proprietà **Duration** è 0, indica che il tempo di avvio della risorsa misurata è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="9dea1-264">If the **Duration** property is 0, this indicates that the startup time of the measured resource is unknown.</span></span> <span data-ttu-id="9dea1-265">In caso contrario, **Duration** specifica la durata tra l'avvio della risorsa e il **timestamp**.</span><span class="sxs-lookup"><span data-stu-id="9dea1-265">Otherwise, **Duration** specifies the duration between startup of the resource and **TimeStamp**.</span></span><br/> |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="9dea1-266"><dt>**DMTF riservato**</dt> <dt>5.. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="9dea1-266"><dt>**DMTF Reserved**</dt> <dt>5..32767</dt></span></span> </dl>                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <span data-ttu-id="9dea1-267">32768 <dt> **riservato al fornitore**</dt> <dt>.. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="9dea1-267"><dt>**Vendor Reserved** </dt> <dt>32768..65535 </dt></span></span> </dl> |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

</dd> <dt>

<span data-ttu-id="9dea1-268">**Unità**</span><span class="sxs-lookup"><span data-stu-id="9dea1-268">**Units**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9dea1-269">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="9dea1-269">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9dea1-270">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="9dea1-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9dea1-271">Identifica le unità specifiche di un valore, ad esempio "megabyte".</span><span class="sxs-lookup"><span data-stu-id="9dea1-271">Identifies the specific units of a value, for example, "megabytes".</span></span> <span data-ttu-id="9dea1-272">Questa proprietà viene ereditata da **CIM \_ BaseMetricDefinition**.</span><span class="sxs-lookup"><span data-stu-id="9dea1-272">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9dea1-273">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9dea1-273">Requirements</span></span>



| <span data-ttu-id="9dea1-274">Requisito</span><span class="sxs-lookup"><span data-stu-id="9dea1-274">Requirement</span></span> | <span data-ttu-id="9dea1-275">Valore</span><span class="sxs-lookup"><span data-stu-id="9dea1-275">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9dea1-276">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9dea1-276">Minimum supported client</span></span><br/> | <span data-ttu-id="9dea1-277">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="9dea1-277">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="9dea1-278">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9dea1-278">Minimum supported server</span></span><br/> | <span data-ttu-id="9dea1-279">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="9dea1-279">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9dea1-280">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9dea1-280">Namespace</span></span><br/>                | <span data-ttu-id="9dea1-281">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="9dea1-281">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="9dea1-282">MOF</span><span class="sxs-lookup"><span data-stu-id="9dea1-282">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9dea1-283"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9dea1-283"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9dea1-284">DLL</span><span class="sxs-lookup"><span data-stu-id="9dea1-284">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9dea1-285"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9dea1-285"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

