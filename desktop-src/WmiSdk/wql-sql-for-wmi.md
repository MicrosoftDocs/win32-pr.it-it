---
description: Il WMI Query Language (WQL) è un subset del Structured Query Language di American National Standards Institute (ANSI SQL) &\# 8212; con modifiche semantiche secondarie. Nella tabella seguente sono elencate le parole chiave WQL.
ms.assetid: 72a7ec04-9af3-41ae-9189-6e1d46803fa9
ms.tgt_platform: multiple
title: WQL (SQL per WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87498b6e8e37ab900e21eedf2c15d5cdba9f9bd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226932"
---
# <a name="wql-sql-for-wmi"></a><span data-ttu-id="6089c-104">WQL (SQL per WMI)</span><span class="sxs-lookup"><span data-stu-id="6089c-104">WQL (SQL for WMI)</span></span>

<span data-ttu-id="6089c-105">Il WMI Query Language (WQL) è un subset del Structured Query Language di American National Standards Institute (ANSI SQL) con modifiche di semantica secondarie.</span><span class="sxs-lookup"><span data-stu-id="6089c-105">The WMI Query Language (WQL) is a subset of the American National Standards Institute Structured Query Language (ANSI SQL) with minor semantic changes.</span></span> <span data-ttu-id="6089c-106">Nella tabella seguente sono elencate le parole chiave WQL.</span><span class="sxs-lookup"><span data-stu-id="6089c-106">The following table lists the WQL keywords.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6089c-107">WQL (parola chiave)</span><span class="sxs-lookup"><span data-stu-id="6089c-107">WQL keyword</span></span></th>
<th><span data-ttu-id="6089c-108">Significato</span><span class="sxs-lookup"><span data-stu-id="6089c-108">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6089c-109">AND</span><span class="sxs-lookup"><span data-stu-id="6089c-109">AND</span></span><br/></td>
<td><span data-ttu-id="6089c-110">Combina due espressioni booleane e restituisce <strong>true</strong> quando entrambe le espressioni sono <strong>true</strong>.</span><span class="sxs-lookup"><span data-stu-id="6089c-110">Combines two Boolean expressions, and returns <strong>TRUE</strong> when both expressions are <strong>TRUE</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6089c-111"><a href="associators-of-statement.md">ASSOCIATORI DI</a></span><span class="sxs-lookup"><span data-stu-id="6089c-111"><a href="associators-of-statement.md">ASSOCIATORS OF</a></span></span></td>
<td><span data-ttu-id="6089c-112">Recupera tutte le istanze di associate a un'istanza di di origine.</span><span class="sxs-lookup"><span data-stu-id="6089c-112">Retrieves all instances that are associated with a source instance.</span></span><br/> <span data-ttu-id="6089c-113">Usare questa istruzione con query di schema e query di dati.</span><span class="sxs-lookup"><span data-stu-id="6089c-113">Use this statement with schema queries and data queries.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6089c-114"><a href="--class-identifier.md">__CLASS</a></span><span class="sxs-lookup"><span data-stu-id="6089c-114"><a href="--class-identifier.md">__CLASS</a></span></span></td>
<td><span data-ttu-id="6089c-115">Fa riferimento alla classe dell'oggetto in una query.</span><span class="sxs-lookup"><span data-stu-id="6089c-115">References the class of the object in a query.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6089c-116">FROM</span><span class="sxs-lookup"><span data-stu-id="6089c-116">FROM</span></span><br/></td>
<td><span data-ttu-id="6089c-117">Specifica la classe che contiene le proprietà elencate in un'istruzione SELECT.</span><span class="sxs-lookup"><span data-stu-id="6089c-117">Specifies the class that contains the properties listed in a SELECT statement.</span></span> <span data-ttu-id="6089c-118">Strumentazione gestione Windows (WMI) supporta le query di dati da una sola classe alla volta.</span><span class="sxs-lookup"><span data-stu-id="6089c-118">Windows Management Instrumentation (WMI) supports data queries from only one class at a time.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6089c-119"><a href="group-clause.md">Clausola GROUP</a></span><span class="sxs-lookup"><span data-stu-id="6089c-119"><a href="group-clause.md">GROUP Clause</a></span></span></td>
<td><span data-ttu-id="6089c-120">Causa la generazione di una notifica da parte di WMI per rappresentare un gruppo di eventi.</span><span class="sxs-lookup"><span data-stu-id="6089c-120">Causes WMI to generate one notification to represent a group of events.</span></span><br/> <span data-ttu-id="6089c-121">Usare questa clausola con le query di eventi.</span><span class="sxs-lookup"><span data-stu-id="6089c-121">Use this clause with event queries.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6089c-122"><a href="having-clause.md">HAVING</a></span><span class="sxs-lookup"><span data-stu-id="6089c-122"><a href="having-clause.md">HAVING</a></span></span></td>
<td><span data-ttu-id="6089c-123">Filtra gli eventi ricevuti durante l'intervallo di raggruppamento specificato nella <a href="within-clause.md">clausola all'interno</a>di.</span><span class="sxs-lookup"><span data-stu-id="6089c-123">Filters the events that are received during the grouping interval that is specified in the <a href="within-clause.md">WITHIN clause</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6089c-124"><a href="wql-operators.md">IS</a></span><span class="sxs-lookup"><span data-stu-id="6089c-124"><a href="wql-operators.md">IS</a></span></span></td>
<td><span data-ttu-id="6089c-125">Operatore di confronto utilizzato con NOT e <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="6089c-125">Comparison operator used with NOT and <strong>NULL</strong>.</span></span> <span data-ttu-id="6089c-126">La sintassi per questa istruzione è la seguente:</span><span class="sxs-lookup"><span data-stu-id="6089c-126">The syntax for this statement is the following:</span></span><br/> <span data-ttu-id="6089c-127">IS [NOT] <strong>null</strong></span><span class="sxs-lookup"><span data-stu-id="6089c-127">IS [NOT] <strong>NULL</strong></span></span><br/> <span data-ttu-id="6089c-128">(dove NOT è facoltativo)</span><span class="sxs-lookup"><span data-stu-id="6089c-128">(where NOT is optional)</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6089c-129"><a href="wql-operators.md">ISA</a></span><span class="sxs-lookup"><span data-stu-id="6089c-129"><a href="wql-operators.md">ISA</a></span></span></td>
<td><span data-ttu-id="6089c-130">Operatore che applica una query alle sottoclassi di una classe specificata.</span><span class="sxs-lookup"><span data-stu-id="6089c-130">Operator that applies a query to the subclasses of a specified class.</span></span> <span data-ttu-id="6089c-131">Per ulteriori informazioni, vedere <a href="isa-operator-for-event-queries.md">operatore ISA per query di evento</a>, <a href="isa-operator-for-data-queries.md">operatore ISA per query di dati</a>e <a href="isa-operator-for-schema-queries.md">operatore ISA per le query di schema</a>.</span><span class="sxs-lookup"><span data-stu-id="6089c-131">For more information, see <a href="isa-operator-for-event-queries.md">ISA Operator for Event Queries</a>, <a href="isa-operator-for-data-queries.md">ISA Operator for Data Queries</a>, and <a href="isa-operator-for-schema-queries.md">ISA Operator for Schema Queries</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6089c-132">KEYSONLY</span><span class="sxs-lookup"><span data-stu-id="6089c-132">KEYSONLY</span></span><br/></td>
<td><span data-ttu-id="6089c-133">Utilizzato nei <a href="references-of-statement.md">riferimenti di</a> e <a href="associators-of-statement.md">associatori di</a> query per garantire che le istanze risultanti vengano popolate solo con le chiavi delle istanze di, riducendo l'overhead della chiamata.</span><span class="sxs-lookup"><span data-stu-id="6089c-133">Used in <a href="references-of-statement.md">REFERENCES OF</a> and <a href="associators-of-statement.md">ASSOCIATORS OF</a> queries to ensure that the resulting instances are only populated with the keys of the instances, which reduces the overhead of the call.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6089c-134"><a href="wql-operators.md">LIKE</a></span><span class="sxs-lookup"><span data-stu-id="6089c-134"><a href="wql-operators.md">LIKE</a></span></span></td>
<td><span data-ttu-id="6089c-135">Operatore che determina se una determinata stringa di caratteri corrisponde a un criterio specificato.</span><span class="sxs-lookup"><span data-stu-id="6089c-135">Operator that determines whether or not a given character string matches a specified pattern.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6089c-136">NOT</span><span class="sxs-lookup"><span data-stu-id="6089c-136">NOT</span></span><br/></td>
<td><span data-ttu-id="6089c-137">Operatore di confronto che utilizza in una query di selezione WQL, ad esempio:</span><span class="sxs-lookup"><span data-stu-id="6089c-137">Comparison operator that use in a WQL SELECT query, for example:</span></span><br/>
<pre data-space="preserve"><code>SELECT * FROM meta_class WHERE NOT __class < &quot;Win32&quot; AND NOT __this ISA &quot;Win32_Account&quot;</code></pre></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6089c-138"><strong>NULL</strong></span><span class="sxs-lookup"><span data-stu-id="6089c-138"><strong>NULL</strong></span></span></td>
<td><span data-ttu-id="6089c-139">Indica che un oggetto non dispone di un valore assegnato in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="6089c-139">Indicates an object does not have an explicitly assigned value.</span></span> <span data-ttu-id="6089c-140"><strong>Null</strong> non è equivalente a zero (0) o vuoto.</span><span class="sxs-lookup"><span data-stu-id="6089c-140"><strong>NULL</strong> is not equivalent to zero (0) or blank.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6089c-141">OR</span><span class="sxs-lookup"><span data-stu-id="6089c-141">OR</span></span><br/></td>
<td><span data-ttu-id="6089c-142">Combina due condizioni.</span><span class="sxs-lookup"><span data-stu-id="6089c-142">Combines two conditions.</span></span><br/> <span data-ttu-id="6089c-143">Quando in un'istruzione viene usato più di un operatore logico, gli operatori OR vengono valutati dopo gli operatori e.</span><span class="sxs-lookup"><span data-stu-id="6089c-143">When more than one logical operator is used in a statement, the OR operators are evaluated after the AND operators.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6089c-144"><a href="references-of-statement.md">RIFERIMENTI DI</a></span><span class="sxs-lookup"><span data-stu-id="6089c-144"><a href="references-of-statement.md">REFERENCES OF</a></span></span></td>
<td><span data-ttu-id="6089c-145">Recupera tutte le istanze di associazione che fanno riferimento a un'istanza di origine specifica.</span><span class="sxs-lookup"><span data-stu-id="6089c-145">Retrieves all association instances that refer to a specific source instance.</span></span> <span data-ttu-id="6089c-146">Usare questa istruzione con le query di schema e dati.</span><span class="sxs-lookup"><span data-stu-id="6089c-146">Use this statement with schema and data queries.</span></span> <span data-ttu-id="6089c-147">I <a href="references-of-statement.md">riferimenti</a> <a href="associators-of-statement.md">all'istruzione sono simili a quelli dell'</a> istruzione.</span><span class="sxs-lookup"><span data-stu-id="6089c-147">The <a href="references-of-statement.md">REFERENCES OF</a> statement is similar to the <a href="associators-of-statement.md">ASSOCIATORS OF</a> statement.</span></span> <span data-ttu-id="6089c-148">Tuttavia, non recupera le istanze dell'endpoint. Recupera le istanze dell'associazione.</span><span class="sxs-lookup"><span data-stu-id="6089c-148">However, it does not retrieve endpoint instances; it retrieves the association instances.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6089c-149">SELECT</span><span class="sxs-lookup"><span data-stu-id="6089c-149">SELECT</span></span><br/></td>
<td><span data-ttu-id="6089c-150">Specifica le proprietà utilizzate in una query.</span><span class="sxs-lookup"><span data-stu-id="6089c-150">Specifies the properties that are used in a query.</span></span><br/> <span data-ttu-id="6089c-151">Per ulteriori informazioni, vedere istruzione <a href="select-statement-for-data-queries.md">Select per le query di dati</a>, <a href="select-statement-for-event-queries.md">istruzione SELECT per le query di evento</a>o <a href="select-statement-for-schema-queries.md">istruzione SELECT per le query dello schema</a>.</span><span class="sxs-lookup"><span data-stu-id="6089c-151">For more information, see <a href="select-statement-for-data-queries.md">SELECT Statement for Data Queries</a>, <a href="select-statement-for-event-queries.md">SELECT Statement for Event Queries</a>, or <a href="select-statement-for-schema-queries.md">SELECT Statement for Schema Queries</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6089c-152"><strong>TRUE</strong></span><span class="sxs-lookup"><span data-stu-id="6089c-152"><strong>TRUE</strong></span></span></td>
<td><span data-ttu-id="6089c-153">Operatore booleano che restituisce-1 (meno uno).</span><span class="sxs-lookup"><span data-stu-id="6089c-153">Boolean operator that evaluates to -1 (minus one).</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6089c-154"><a href="where-clause.md">WHERE</a></span><span class="sxs-lookup"><span data-stu-id="6089c-154"><a href="where-clause.md">WHERE</a></span></span></td>
<td><span data-ttu-id="6089c-155">Restringe l'ambito di una query di dati, eventi o schemi.</span><span class="sxs-lookup"><span data-stu-id="6089c-155">Narrows the scope of a data, event, or schema query.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6089c-156"><a href="within-clause.md">WITHIN</a></span><span class="sxs-lookup"><span data-stu-id="6089c-156"><a href="within-clause.md">WITHIN</a></span></span></td>
<td><span data-ttu-id="6089c-157">Specifica un intervallo di polling o di raggruppamento.</span><span class="sxs-lookup"><span data-stu-id="6089c-157">Specifies a polling or grouping interval.</span></span><br/> <span data-ttu-id="6089c-158">Usare questa clausola con le query di eventi.</span><span class="sxs-lookup"><span data-stu-id="6089c-158">Use this clause with event queries.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6089c-159">FALSE</span><span class="sxs-lookup"><span data-stu-id="6089c-159">FALSE</span></span><br/></td>
<td><span data-ttu-id="6089c-160">Operatore booleano che restituisce 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="6089c-160">Boolean operator that evaluates to 0 (zero).</span></span></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="6089c-161">L'utilizzo di una parola chiave WQL come nome di oggetto può generare una query che non può essere analizzata anche quando la query viene compilata senza errori.</span><span class="sxs-lookup"><span data-stu-id="6089c-161">Using a WQL key word as an object name can result in a query that cannot be parsed even when the query compiles without error.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="6089c-162">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6089c-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6089c-163">Operatori WQL</span><span class="sxs-lookup"><span data-stu-id="6089c-163">WQL Operators</span></span>](wql-operators.md)
</dt> <dt>

[<span data-ttu-id="6089c-164">Formati di data supportati da WQL</span><span class="sxs-lookup"><span data-stu-id="6089c-164">WQL-Supported Date Formats</span></span>](wql-supported-date-formats.md)
</dt> <dt>

[<span data-ttu-id="6089c-165">Formati di ora supportati da WQL</span><span class="sxs-lookup"><span data-stu-id="6089c-165">WQL-Supported Time Formats</span></span>](wql-supported-time-formats.md)
</dt> </dl>

 

 




