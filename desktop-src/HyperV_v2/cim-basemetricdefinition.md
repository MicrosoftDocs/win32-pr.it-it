---
description: Rappresenta una definizione di metrica che contiene i metadati per un \_ oggetto METRICINSTANCE CIM.
ms.assetid: 6abfb0dc-e80b-4ca6-89d9-2e43283d0abe
title: Classe CIM_BaseMetricDefinition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BaseMetricDefinition
- CIM_BaseMetricDefinition.Id
- CIM_BaseMetricDefinition.Name
- CIM_BaseMetricDefinition.DataType
- CIM_BaseMetricDefinition.Calculable
- CIM_BaseMetricDefinition.Units
- CIM_BaseMetricDefinition.BreakdownDimensions
- CIM_BaseMetricDefinition.IsContinuous
- CIM_BaseMetricDefinition.ChangeType
- CIM_BaseMetricDefinition.TimeScope
- CIM_BaseMetricDefinition.GatheringType
- CIM_BaseMetricDefinition.ProgrammaticUnits
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cac965ed1eae59f1c269d897a12e9aa116183eb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319528"
---
# <a name="cim_basemetricdefinition-class"></a><span data-ttu-id="e3dac-103">CIM \_ BaseMetricDefinition (classe)</span><span class="sxs-lookup"><span data-stu-id="e3dac-103">CIM\_BaseMetricDefinition class</span></span>

<span data-ttu-id="e3dac-104">Rappresenta una definizione di metrica che contiene i metadati per un **oggetto \_ MetricInstance CIM** .</span><span class="sxs-lookup"><span data-stu-id="e3dac-104">Represents a metric definition that contains the meta data for a **CIM\_MetricInstance** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3dac-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e3dac-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_BaseMetricDefinition : CIM_ManagedElement
{
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

## <a name="members"></a><span data-ttu-id="e3dac-106">Members</span><span class="sxs-lookup"><span data-stu-id="e3dac-106">Members</span></span>

<span data-ttu-id="e3dac-107">La classe **CIM \_ BaseMetricDefinition** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="e3dac-107">The **CIM\_BaseMetricDefinition** class has these types of members:</span></span>

-   [<span data-ttu-id="e3dac-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e3dac-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e3dac-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e3dac-109">Properties</span></span>

<span data-ttu-id="e3dac-110">La classe **CIM \_ BaseMetricDefinition** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="e3dac-110">The **CIM\_BaseMetricDefinition** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e3dac-111">**BreakdownDimensions**</span><span class="sxs-lookup"><span data-stu-id="e3dac-111">**BreakdownDimensions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3dac-112">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="e3dac-112">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="e3dac-113">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e3dac-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e3dac-114">Matrice che contiene le stringhe di formato gratuite che possono essere utilizzate per suddividere le query di oggetti [**CIM \_ BaseMetricValue**](cim-basemetricvalue.md) lungo una determinata dimensione.</span><span class="sxs-lookup"><span data-stu-id="e3dac-114">An array that contains free format strings that can be used to break down queries of [**CIM\_BaseMetricValue**](cim-basemetricvalue.md) objects along a certain dimension.</span></span> <span data-ttu-id="e3dac-115">Le stringhe devono essere significative per gli utenti finali dei dati della metrica.</span><span class="sxs-lookup"><span data-stu-id="e3dac-115">The strings should be meaningful to the end users of the metric data.</span></span> <span data-ttu-id="e3dac-116">Inoltre, le stringhe devono indicare quali dimensioni di suddivisione sono supportate per la definizione della metrica, dalla strumentazione sottostante.</span><span class="sxs-lookup"><span data-stu-id="e3dac-116">In addition, the strings should indicate which break down dimensions are supported for the metric definition, by the underlying instrumentation.</span></span>

<span data-ttu-id="e3dac-117">Un esempio è un nome di transazione che consente di suddividere il valore totale di tutte le transazioni in un set di valori, uno per ogni nome di transazione.</span><span class="sxs-lookup"><span data-stu-id="e3dac-117">An example is a transaction name that allows the break down of the total value for all transactions into a set of values, one for each transaction name.</span></span> <span data-ttu-id="e3dac-118">Altri esempi sono un sistema applicativo o un nome di gruppo di utenti.</span><span class="sxs-lookup"><span data-stu-id="e3dac-118">Other examples are an application system, or a user group name.</span></span>

</dd> <dt>

<span data-ttu-id="e3dac-119">**Calcolabile**</span><span class="sxs-lookup"><span data-stu-id="e3dac-119">**Calculable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3dac-120">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e3dac-120">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e3dac-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e3dac-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e3dac-122">Caratteristiche della metrica utilizzata per eseguire i calcoli.</span><span class="sxs-lookup"><span data-stu-id="e3dac-122">The characteristics of the metric used to perform calculations.</span></span>

<dt>

<span id="Non-calculable"></span><span id="non-calculable"></span><span id="NON-CALCULABLE"></span>

<span data-ttu-id="e3dac-123"><span id="Non-calculable"></span><span id="non-calculable"></span><span id="NON-CALCULABLE"></span>**Non calcolabile** (1)</span><span class="sxs-lookup"><span data-stu-id="e3dac-123"><span id="Non-calculable"></span><span id="non-calculable"></span><span id="NON-CALCULABLE"></span>**Non-calculable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="e3dac-124">Stringa.</span><span class="sxs-lookup"><span data-stu-id="e3dac-124">A string.</span></span> <span data-ttu-id="e3dac-125">L'aritmetica non è sensata.</span><span class="sxs-lookup"><span data-stu-id="e3dac-125">Arithmetic makes no sense.</span></span>

</dd> <dt>

<span id="Summable"></span><span id="summable"></span><span id="SUMMABLE"></span>

<span data-ttu-id="e3dac-126"><span id="Summable"></span><span id="summable"></span><span id="SUMMABLE"></span>**Sommabile** (2)</span><span class="sxs-lookup"><span data-stu-id="e3dac-126"><span id="Summable"></span><span id="summable"></span><span id="SUMMABLE"></span>**Summable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="e3dac-127">È ragionevole sommare questo valore in molte istanze di, ad esempio, UnitOfWork, ad esempio il numero di file elaborati in un processo di backup.</span><span class="sxs-lookup"><span data-stu-id="e3dac-127">It is reasonable to sum this value over many instances of e.g., UnitOfWork, such as the number of files processed in a backup job.</span></span> <span data-ttu-id="e3dac-128">Se, ad esempio, ogni processo di backup è un UnitOfWork e ogni processo esegue il backup di 27.000 file in media, è opportuno indicare che i processi di backup 100 hanno elaborato 2,7 milioni file.</span><span class="sxs-lookup"><span data-stu-id="e3dac-128">For example, if each backup job is a UnitOfWork, and each job backs up 27,000 files on average, then it makes sense to say that 100 backup jobs processed 2,700,000 files.</span></span>

</dd> <dt>

<span id="Non-summable"></span><span id="non-summable"></span><span id="NON-SUMMABLE"></span>

<span data-ttu-id="e3dac-129"><span id="Non-summable"></span><span id="non-summable"></span><span id="NON-SUMMABLE"></span>**Non-sommabile** (3)</span><span class="sxs-lookup"><span data-stu-id="e3dac-129"><span id="Non-summable"></span><span id="non-summable"></span><span id="NON-SUMMABLE"></span>**Non-summable** (3)</span></span>


</dt> <dd>

<span data-ttu-id="e3dac-130">Non ha senso sommare questo valore in molte istanze di UnitOfWork.</span><span class="sxs-lookup"><span data-stu-id="e3dac-130">It does not make sense to sum this value over many instances of UnitOfWork.</span></span> <span data-ttu-id="e3dac-131">Un esempio è una metrica che misura la lunghezza della coda quando un processo arriva a un server.</span><span class="sxs-lookup"><span data-stu-id="e3dac-131">An example would be a metric that measures the queue length when a job arrives at a server.</span></span> <span data-ttu-id="e3dac-132">Se ogni processo è un UnitOfWork e la lunghezza media della coda quando ogni processo arriva è 33, non è sensato dire che la lunghezza della coda per i processi 100 è 3300.</span><span class="sxs-lookup"><span data-stu-id="e3dac-132">If each job is a UnitOfWork, and the average queue length when each job arrives is 33, it does not make sense to say that the queue length for 100 jobs is 3300.</span></span> <span data-ttu-id="e3dac-133">È sensato dire che la media è 33.</span><span class="sxs-lookup"><span data-stu-id="e3dac-133">It does make sense to say that the mean is 33.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e3dac-134">**ChangeType**</span><span class="sxs-lookup"><span data-stu-id="e3dac-134">**ChangeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3dac-135">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e3dac-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e3dac-136">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e3dac-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e3dac-137">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ BaseMetricDefinition**.**Uncontinuous**")</span><span class="sxs-lookup"><span data-stu-id="e3dac-137">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_BaseMetricDefinition**.**IsContinuous**")</span></span>
</dt> </dl>

<span data-ttu-id="e3dac-138">Indica il modo in cui il valore della metrica cambia usando gli attributi comuni, ad esempio la modifica della direzione, i valori minimo e massimo e la semantica di wrapping.</span><span class="sxs-lookup"><span data-stu-id="e3dac-138">Indicates how the metric value changes using common attributes such as direction change, minimum and maximum values, and wrapping semantics.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e3dac-139"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="e3dac-139"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="e3dac-140">La finestra di progettazione metrica non ha qualificato l'oggetto ChangeType.</span><span class="sxs-lookup"><span data-stu-id="e3dac-140">The metric designer did not qualify the ChangeType.</span></span>

</dd> <dt>

<span id="N_A"></span><span id="n_a"></span>

<span data-ttu-id="e3dac-141"><span id="N_A"></span><span id="n_a"></span>**N/** d (2)</span><span class="sxs-lookup"><span data-stu-id="e3dac-141"><span id="N_A"></span><span id="n_a"></span>**N/A** (2)</span></span>


</dt> <dd>

<span data-ttu-id="e3dac-142">Se la proprietà "sacontinuous" è "false", ChangeType non ha senso e deve essere impostato su "N/A".</span><span class="sxs-lookup"><span data-stu-id="e3dac-142">If the "IsContinuous" property is "false", ChangeType does not make sense and MUST be is set to "N/A".</span></span>

</dd> <dt>

<span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span>

<span data-ttu-id="e3dac-143"><span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span>**Contatore** (3)</span><span class="sxs-lookup"><span data-stu-id="e3dac-143"><span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span>**Counter** (3)</span></span>


</dt> <dd>

<span data-ttu-id="e3dac-144">La metrica è una metrica del contatore.</span><span class="sxs-lookup"><span data-stu-id="e3dac-144">The metric is a counter metric.</span></span> <span data-ttu-id="e3dac-145">Hanno valori interi non negativi che aumentano in modo progressivo fino a raggiungere il numero massimo rappresentabile, quindi eseguire il wrapping e iniziare ad aumentare da 0.</span><span class="sxs-lookup"><span data-stu-id="e3dac-145">These have non-negative integer values which increase monotonically until reaching the maximum representable number and then wrap around and start increasing from 0.</span></span> <span data-ttu-id="e3dac-146">Tali contatori, noti anche come contatori di rollover, possono essere usati ad esempio per conteggiare il numero di errori di rete o il numero di transazioni elaborate.</span><span class="sxs-lookup"><span data-stu-id="e3dac-146">Such counters, also known as rollover counters, can be used for instance to count the number of network errors or the number of transactions processed.</span></span> <span data-ttu-id="e3dac-147">L'unico modo in cui un'applicazione client tiene traccia degli incapsulamenti consiste nel recuperare il valore del contatore in intervalli opportunamente brevi.</span><span class="sxs-lookup"><span data-stu-id="e3dac-147">The only way for a client application to keep track of wrap arounds is to retrieve the value of the counter in appropriately short intervals.</span></span>

</dd> <dt>

<span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span>

<span data-ttu-id="e3dac-148"><span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span>**Misuratore** (4)</span><span class="sxs-lookup"><span data-stu-id="e3dac-148"><span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span>**Gauge** (4)</span></span>


</dt> <dd>

<span data-ttu-id="e3dac-149">La metrica è una metrica del misuratore.</span><span class="sxs-lookup"><span data-stu-id="e3dac-149">The metric is a gauge metric.</span></span> <span data-ttu-id="e3dac-150">Hanno valori integer o float che possono aumentare e diminuire in modo arbitrario.</span><span class="sxs-lookup"><span data-stu-id="e3dac-150">These have integer or float values that can increase and decrease arbitrarily.</span></span> <span data-ttu-id="e3dac-151">NON è necessario eseguire il wrapping di un misuratore quando si raggiunge il numero minimo o massimo rappresentabile, invece, il valore "bastoni" a tale numero.</span><span class="sxs-lookup"><span data-stu-id="e3dac-151">A gauge MUST NOT wrap when reaching the minimum or maximum representable number, instead, the value "sticks" at that number.</span></span> <span data-ttu-id="e3dac-152">Valori minimi o massimi all'interno dell'intervallo di valori rappresentabili in corrispondenza del quale il valore della metrica "bastoni", può o non essere definito.</span><span class="sxs-lookup"><span data-stu-id="e3dac-152">Minimum or maximum values inside of the representable value range at which the metric value "sticks", may or may not be defined.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="e3dac-153"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (5.. 32767)</span><span class="sxs-lookup"><span data-stu-id="e3dac-153"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (5..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="e3dac-154"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornitore riservato** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="e3dac-154"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e3dac-155">**DataType**</span><span class="sxs-lookup"><span data-stu-id="e3dac-155">**DataType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3dac-156">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e3dac-156">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e3dac-157">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e3dac-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e3dac-158">Tipo di dati della metrica.</span><span class="sxs-lookup"><span data-stu-id="e3dac-158">The data type of the metric.</span></span>

<dt>

<span id="boolean"></span><span id="BOOLEAN"></span>

<span data-ttu-id="e3dac-159">**valore booleano** (1)</span><span class="sxs-lookup"><span data-stu-id="e3dac-159">**boolean** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="char16"></span><span id="CHAR16"></span>

<span data-ttu-id="e3dac-160">**Char16** (2)</span><span class="sxs-lookup"><span data-stu-id="e3dac-160">**char16** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="datetime"></span><span id="DATETIME"></span>

<span data-ttu-id="e3dac-161">**DateTime** (3)</span><span class="sxs-lookup"><span data-stu-id="e3dac-161">**datetime** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="real32"></span><span id="REAL32"></span>

<span data-ttu-id="e3dac-162">**real32** (4)</span><span class="sxs-lookup"><span data-stu-id="e3dac-162">**real32** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="real64"></span><span id="REAL64"></span>

<span data-ttu-id="e3dac-163">**real64** (5)</span><span class="sxs-lookup"><span data-stu-id="e3dac-163">**real64** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="sint16"></span><span id="SINT16"></span>

<span data-ttu-id="e3dac-164">**sint16** (6)</span><span class="sxs-lookup"><span data-stu-id="e3dac-164">**sint16** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="sint32"></span><span id="SINT32"></span>

<span data-ttu-id="e3dac-165">**sint32** (7)</span><span class="sxs-lookup"><span data-stu-id="e3dac-165">**sint32** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="sint64"></span><span id="SINT64"></span>

<span data-ttu-id="e3dac-166">**sint64** (8)</span><span class="sxs-lookup"><span data-stu-id="e3dac-166">**sint64** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="sint8"></span><span id="SINT8"></span>

<span data-ttu-id="e3dac-167">**sint8** (9)</span><span class="sxs-lookup"><span data-stu-id="e3dac-167">**sint8** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="string"></span><span id="STRING"></span>

<span data-ttu-id="e3dac-168">**stringa** (10)</span><span class="sxs-lookup"><span data-stu-id="e3dac-168">**string** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="uint16"></span><span id="UINT16"></span>

<span data-ttu-id="e3dac-169">**UInt16** (11)</span><span class="sxs-lookup"><span data-stu-id="e3dac-169">**uint16** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="uint32"></span><span id="UINT32"></span>

<span data-ttu-id="e3dac-170">**UInt32** (12)</span><span class="sxs-lookup"><span data-stu-id="e3dac-170">**uint32** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="uint64"></span><span id="UINT64"></span>

<span data-ttu-id="e3dac-171">**UInt64** (13)</span><span class="sxs-lookup"><span data-stu-id="e3dac-171">**uint64** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="uint8"></span><span id="UINT8"></span>

<span data-ttu-id="e3dac-172">**Uint8** (14)</span><span class="sxs-lookup"><span data-stu-id="e3dac-172">**uint8** (14)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e3dac-173">**GatheringType**</span><span class="sxs-lookup"><span data-stu-id="e3dac-173">**GatheringType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3dac-174">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e3dac-174">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e3dac-175">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e3dac-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e3dac-176">Indica il modo in cui i valori delle metriche vengono raccolti dalla strumentazione sottostante.</span><span class="sxs-lookup"><span data-stu-id="e3dac-176">Indicates how the metric values are gathered by the underlying instrumentation.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e3dac-177"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="e3dac-177"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="e3dac-178">Indica che GatheringType non è noto.</span><span class="sxs-lookup"><span data-stu-id="e3dac-178">Indicates that the GatheringType is not known.</span></span>

</dd> <dt>

<span id="OnChange"></span><span id="onchange"></span><span id="ONCHANGE"></span>

<span data-ttu-id="e3dac-179"><span id="OnChange"></span><span id="onchange"></span><span id="ONCHANGE"></span>**OnChange** (2)</span><span class="sxs-lookup"><span data-stu-id="e3dac-179"><span id="OnChange"></span><span id="onchange"></span><span id="ONCHANGE"></span>**OnChange** (2)</span></span>


</dt> <dd>

<span data-ttu-id="e3dac-180">Indica che i valori della metrica CIM vengono aggiornati immediatamente quando i valori all'interno della risorsa misurata cambiano.</span><span class="sxs-lookup"><span data-stu-id="e3dac-180">Indicates that the CIM metric values get updated immediately when the values inside of the measured resource change.</span></span> <span data-ttu-id="e3dac-181">I valori delle metriche OnChange riflettono effettivamente la situazione corrente all'interno della risorsa in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="e3dac-181">The values of OnChange metrics truly reflect the current situation within the resource at any time.</span></span> <span data-ttu-id="e3dac-182">Un esempio è il numero di utenti connessi che vengono aggiornati immediatamente quando gli utenti accedono e si disconnettono.</span><span class="sxs-lookup"><span data-stu-id="e3dac-182">An example is the number of logged on users that gets updated immediately as users log on and off.</span></span>

</dd> <dt>

<span id="Periodic"></span><span id="periodic"></span><span id="PERIODIC"></span>

<span data-ttu-id="e3dac-183"><span id="Periodic"></span><span id="periodic"></span><span id="PERIODIC"></span>**Periodica** (3)</span><span class="sxs-lookup"><span data-stu-id="e3dac-183"><span id="Periodic"></span><span id="periodic"></span><span id="PERIODIC"></span>**Periodic** (3)</span></span>


</dt> <dd>

<span data-ttu-id="e3dac-184">": Indica che i valori della metrica CIM vengono aggiornati periodicamente.</span><span class="sxs-lookup"><span data-stu-id="e3dac-184">": Indicates that the CIM metric values get updated periodically.</span></span> <span data-ttu-id="e3dac-185">Ad esempio, per un'applicazione client, un valore della metrica che si applica all'ora corrente apparirà costante durante ogni intervallo di raccolta, quindi passa al nuovo valore alla fine di ogni intervallo di raccolta.</span><span class="sxs-lookup"><span data-stu-id="e3dac-185">For instance, to a client application, a metric value applying to the current time will appear constant during each gathering interval, and then jumps to the new value at the end of each gathering interval.</span></span>

</dd> <dt>

<span id="OnRequest"></span><span id="onrequest"></span><span id="ONREQUEST"></span>

<span data-ttu-id="e3dac-186"><span id="OnRequest"></span><span id="onrequest"></span><span id="ONREQUEST"></span>**OnRequest** (4)</span><span class="sxs-lookup"><span data-stu-id="e3dac-186"><span id="OnRequest"></span><span id="onrequest"></span><span id="ONREQUEST"></span>**OnRequest** (4)</span></span>


</dt> <dd>

<span data-ttu-id="e3dac-187">Indica che il valore della metrica CIM viene determinato ogni volta che viene letto da un'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="e3dac-187">Indicates that the CIM metric value is determined each time a client application reads it.</span></span> <span data-ttu-id="e3dac-188">I valori delle metriche OnRequest restituiscono effettivamente la situazione corrente all'interno della risorsa, se richiesto.</span><span class="sxs-lookup"><span data-stu-id="e3dac-188">The values of OnRequest metrics truly return the current situation within the resource if somebody asks for it.</span></span> <span data-ttu-id="e3dac-189">Tuttavia, non modificano "unosservato" e pertanto la sottoscrizione delle modifiche dei valori delle metriche OnRequest non è CONSIGLIata.</span><span class="sxs-lookup"><span data-stu-id="e3dac-189">However, they do not change "unobserved", and therefore subscribing for value changes of OnRequest metrics is NOT RECOMMENDED.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="e3dac-190"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (5.. 32767)</span><span class="sxs-lookup"><span data-stu-id="e3dac-190"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (5..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="e3dac-191"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornitore riservato** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="e3dac-191"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e3dac-192">**Id**</span><span class="sxs-lookup"><span data-stu-id="e3dac-192">**Id**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3dac-193">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e3dac-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e3dac-194">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e3dac-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e3dac-195">Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e3dac-195">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e3dac-196">ID univoco della definizione della metrica.</span><span class="sxs-lookup"><span data-stu-id="e3dac-196">The unique ID of the metric definition.</span></span> <span data-ttu-id="e3dac-197">Sono consigliati gli UUID/GUID Open Software Foundation (OSF).</span><span class="sxs-lookup"><span data-stu-id="e3dac-197">Open Software Foundation (OSF) UUID/GUIDs are recommended.</span></span>

</dd> <dt>

<span data-ttu-id="e3dac-198">**IsContinuous**</span><span class="sxs-lookup"><span data-stu-id="e3dac-198">**IsContinuous**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3dac-199">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="e3dac-199">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e3dac-200">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e3dac-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e3dac-201">True se il valore della metrica è continuo. in caso contrario, false.</span><span class="sxs-lookup"><span data-stu-id="e3dac-201">True if the metric value is continuous; otherwise, false.</span></span>

</dd> <dt>

<span data-ttu-id="e3dac-202">**Nome**</span><span class="sxs-lookup"><span data-stu-id="e3dac-202">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3dac-203">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e3dac-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e3dac-204">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e3dac-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e3dac-205">Nome della metrica.</span><span class="sxs-lookup"><span data-stu-id="e3dac-205">The name of the metric.</span></span> <span data-ttu-id="e3dac-206">Non è necessario che questo nome sia univoco, ma deve essere descrittivo e può contenere spazi vuoti.</span><span class="sxs-lookup"><span data-stu-id="e3dac-206">This name does not have to be unique, but should be descriptive and may contain blank spaces.</span></span>

</dd> <dt>

<span data-ttu-id="e3dac-207">**ProgrammaticUnits**</span><span class="sxs-lookup"><span data-stu-id="e3dac-207">**ProgrammaticUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3dac-208">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e3dac-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e3dac-209">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e3dac-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e3dac-210">Unità specifiche di un valore.</span><span class="sxs-lookup"><span data-stu-id="e3dac-210">The specific units of a value.</span></span> <span data-ttu-id="e3dac-211">Il valore di questa proprietà deve essere un valore valido del qualificatore unità programmatiche come definito nell'Appendice C. 1 di DSP0004 V 2.4 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="e3dac-211">The value of this property should be a legal value of the Programmatic Units qualifier as defined in Appendix C.1 of DSP0004 V2.4 or later.</span></span>

</dd> <dt>

<span data-ttu-id="e3dac-212">**TimeScope**</span><span class="sxs-lookup"><span data-stu-id="e3dac-212">**TimeScope**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3dac-213">Tipo di dati: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e3dac-213">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e3dac-214">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e3dac-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e3dac-215">Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ BaseMetricValue**](cim-basemetricvalue.md).**TimeStamp**","**CIM \_ BaseMetricValue**.**Durata**")</span><span class="sxs-lookup"><span data-stu-id="e3dac-215">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_BaseMetricValue**](cim-basemetricvalue.md).**TimeStamp**", "**CIM\_BaseMetricValue**.**Duration**")</span></span>
</dt> </dl>

<span data-ttu-id="e3dac-216">Ambito temporale che si applica alla finestra di progettazione della metrica.</span><span class="sxs-lookup"><span data-stu-id="e3dac-216">The time scope that applies to the metric designer.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e3dac-217"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)</span><span class="sxs-lookup"><span data-stu-id="e3dac-217"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="e3dac-218">Indica che l'ambito di tempo non è stato qualificato dalla finestra di progettazione della metrica o è sconosciuto al provider.</span><span class="sxs-lookup"><span data-stu-id="e3dac-218">Indicates the time scope was not qualified by the metric designer, or is unknown to the provider.</span></span>

</dd> <dt>

<span id="Point"></span><span id="point"></span><span id="POINT"></span>

<span data-ttu-id="e3dac-219"><span id="Point"></span><span id="point"></span><span id="POINT"></span>**Punto** (2)</span><span class="sxs-lookup"><span data-stu-id="e3dac-219"><span id="Point"></span><span id="point"></span><span id="POINT"></span>**Point** (2)</span></span>


</dt> <dd>

<span data-ttu-id="e3dac-220">Indica che la metrica si applica a un punto nel tempo.</span><span class="sxs-lookup"><span data-stu-id="e3dac-220">Indicates that the metric applies to a point in time.</span></span> <span data-ttu-id="e3dac-221">Nelle istanze BaseMetricValue corrispondenti, TimeStamp specifica il punto nel tempo e la durata è sempre 0.</span><span class="sxs-lookup"><span data-stu-id="e3dac-221">On the corresponding BaseMetricValue instances, TimeStamp specifies the point in time and Duration is always 0.</span></span>

</dd> <dt>

<span id="Interval"></span><span id="interval"></span><span id="INTERVAL"></span>

<span data-ttu-id="e3dac-222"><span id="Interval"></span><span id="interval"></span><span id="INTERVAL"></span>**Intervallo** (3)</span><span class="sxs-lookup"><span data-stu-id="e3dac-222"><span id="Interval"></span><span id="interval"></span><span id="INTERVAL"></span>**Interval** (3)</span></span>


</dt> <dd>

<span data-ttu-id="e3dac-223">Indica che la metrica si applica a un intervallo di tempo.</span><span class="sxs-lookup"><span data-stu-id="e3dac-223">Indicates that the metric applies to a time interval.</span></span> <span data-ttu-id="e3dac-224">Nelle istanze BaseMetricValue corrispondenti, TimeStamp specifica la fine dell'intervallo di tempo e Duration ne specifica la durata</span><span class="sxs-lookup"><span data-stu-id="e3dac-224">On the corresponding BaseMetricValue instances, TimeStamp specifies the end of the time interval and Duration specifies its duration</span></span>

</dd> <dt>

<span id="StartupInterval"></span><span id="startupinterval"></span><span id="STARTUPINTERVAL"></span>

<span data-ttu-id="e3dac-225"><span id="StartupInterval"></span><span id="startupinterval"></span><span id="STARTUPINTERVAL"></span>**StartupInterval** (4)</span><span class="sxs-lookup"><span data-stu-id="e3dac-225"><span id="StartupInterval"></span><span id="startupinterval"></span><span id="STARTUPINTERVAL"></span>**StartupInterval** (4)</span></span>


</dt> <dd>

<span data-ttu-id="e3dac-226">Indica che la metrica si applica a un intervallo di tempo che inizia all'avvio della risorsa misurata, ovvero l'oggetto gestito associato da MetricDefForMe.</span><span class="sxs-lookup"><span data-stu-id="e3dac-226">Indicates that the metric applies to a time interval that began at the startup of the measured resource (i.e. the ManagedElement associated by MetricDefForMe).</span></span> <span data-ttu-id="e3dac-227">Nelle istanze BaseMetricValue corrispondenti, TimeStamp specifica la fine dell'intervallo di tempo.</span><span class="sxs-lookup"><span data-stu-id="e3dac-227">On the corresponding BaseMetricValue instances, TimeStamp specifies the end of the time interval.</span></span> <span data-ttu-id="e3dac-228">Se Duration è 0, indica che il tempo di avvio della risorsa misurata è sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="e3dac-228">If Duration is 0, this indicates that the startup time of the measured resource is unknown.</span></span> <span data-ttu-id="e3dac-229">Else, Duration specifica la durata tra l'avvio della risorsa e il TimeStamp.</span><span class="sxs-lookup"><span data-stu-id="e3dac-229">Else, Duration specifies the duration between startup of the resource and TimeStamp.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="e3dac-230"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF riservato** (5.. 32767)</span><span class="sxs-lookup"><span data-stu-id="e3dac-230"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (5..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="e3dac-231"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornitore riservato** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="e3dac-231"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e3dac-232">**Unità**</span><span class="sxs-lookup"><span data-stu-id="e3dac-232">**Units**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e3dac-233">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="e3dac-233">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e3dac-234">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="e3dac-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e3dac-235">Unità della metrica.</span><span class="sxs-lookup"><span data-stu-id="e3dac-235">The units of the metric.</span></span> <span data-ttu-id="e3dac-236">Esempi sono i byte, i pacchetti, i processi, i file, i millisecondi e gli ampere.</span><span class="sxs-lookup"><span data-stu-id="e3dac-236">Examples are bytes, packets, jobs, files, milliseconds, and amps.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e3dac-237">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e3dac-237">Requirements</span></span>



| <span data-ttu-id="e3dac-238">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3dac-238">Requirement</span></span> | <span data-ttu-id="e3dac-239">Valore</span><span class="sxs-lookup"><span data-stu-id="e3dac-239">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3dac-240">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e3dac-240">Minimum supported client</span></span><br/> | <span data-ttu-id="e3dac-241">Windows 8</span><span class="sxs-lookup"><span data-stu-id="e3dac-241">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="e3dac-242">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e3dac-242">Minimum supported server</span></span><br/> | <span data-ttu-id="e3dac-243">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e3dac-243">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="e3dac-244">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e3dac-244">Namespace</span></span><br/>                | <span data-ttu-id="e3dac-245">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="e3dac-245">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e3dac-246">MOF</span><span class="sxs-lookup"><span data-stu-id="e3dac-246">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e3dac-247"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e3dac-247"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e3dac-248">DLL</span><span class="sxs-lookup"><span data-stu-id="e3dac-248">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e3dac-249"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e3dac-249"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e3dac-250">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e3dac-250">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3dac-251">**\_ManagementName CIM**</span><span class="sxs-lookup"><span data-stu-id="e3dac-251">**CIM\_ManagedElement**</span></span>](cim-managedelement.md)
</dt> </dl>

 

