---
description: Microsoft Windows Search USA i gestori delle proprietà per estrarre i valori delle proprietà dagli elementi e usa lo schema del sistema di proprietà per determinare la modalità di indicizzazione di una proprietà specifica.
ms.assetid: b475329a-1ed7-43a4-8e11-3700889a4ce9
title: Sviluppo di gestori di proprietà per Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ac96e47738040321025b7f600e2c91109b08d51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225959"
---
# <a name="developing-property-handlers-for-windows-search"></a><span data-ttu-id="bb5f9-103">Sviluppo di gestori di proprietà per Windows Search</span><span class="sxs-lookup"><span data-stu-id="bb5f9-103">Developing Property Handlers for Windows Search</span></span>

<span data-ttu-id="bb5f9-104">Microsoft Windows Search USA i gestori delle proprietà per estrarre i valori delle proprietà dagli elementi e usa lo schema del sistema di proprietà per determinare la modalità di indicizzazione di una proprietà specifica.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-104">Microsoft Windows Search uses property handlers to extract the values of properties from items and uses the property system schema to determine how a specific property should be indexed.</span></span> <span data-ttu-id="bb5f9-105">Per leggere e indicizzare i valori delle proprietà, i gestori delle proprietà vengono richiamati out-of-process da Windows Search per migliorare la sicurezza e l'affidabilità.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-105">To read and index property values, property handlers are invoked out-of-process by Windows Search to improve security and robustness.</span></span> <span data-ttu-id="bb5f9-106">Al contrario, i gestori delle proprietà vengono richiamati in-process da Esplora risorse per leggere e scrivere i valori delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-106">In contrast, property handlers are invoked in-process by Windows Explorer to read and write property values.</span></span>

<span data-ttu-id="bb5f9-107">Questo argomento integra l'argomento del [sistema di proprietà](../properties/building-property-handlers.md) con informazioni specifiche di Windows Search e contiene le sezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="bb5f9-107">This topic supplements the [Property System](../properties/building-property-handlers.md) topic with information specific to Windows Search and contains the following sections:</span></span>

-   [<span data-ttu-id="bb5f9-108">Decisioni di progettazione per i gestori di proprietà</span><span class="sxs-lookup"><span data-stu-id="bb5f9-108">Design Decisions for Property Handlers</span></span>](#design-decisions-for-property-handlers)
    -   [<span data-ttu-id="bb5f9-109">Decisioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="bb5f9-109">Property Decisions</span></span>](#property-decisions)
    -   [<span data-ttu-id="bb5f9-110">Supporto full-text</span><span class="sxs-lookup"><span data-stu-id="bb5f9-110">Full-Text Support</span></span>](#full-text-support)
    -   [<span data-ttu-id="bb5f9-111">Considerazioni sul Implementatation del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="bb5f9-111">Operating System Implementatation Considerations</span></span>](#operating-system-implementatation-considerations)
-   [<span data-ttu-id="bb5f9-112">Scrittura dei file di descrizione delle proprietà</span><span class="sxs-lookup"><span data-stu-id="bb5f9-112">Writing Property Description Files</span></span>](#writing-property-description-files)
-   [<span data-ttu-id="bb5f9-113">Implementazione di gestori di proprietà</span><span class="sxs-lookup"><span data-stu-id="bb5f9-113">Implementing Property Handlers</span></span>](#implementing-property-handlers)
    -   [<span data-ttu-id="bb5f9-114">IInitializeWithStream</span><span class="sxs-lookup"><span data-stu-id="bb5f9-114">IInitializeWithStream</span></span>](#iinitializewithstream)
    -   [<span data-ttu-id="bb5f9-115">IPropertyStore</span><span class="sxs-lookup"><span data-stu-id="bb5f9-115">IPropertyStore</span></span>](#ipropertystore)
    -   [<span data-ttu-id="bb5f9-116">IPropertyStoreCapabilities</span><span class="sxs-lookup"><span data-stu-id="bb5f9-116">IPropertyStoreCapabilities</span></span>](#ipropertystorecapabilities)
-   [<span data-ttu-id="bb5f9-117">Verifica dell'indicizzazione degli elementi</span><span class="sxs-lookup"><span data-stu-id="bb5f9-117">Ensuring Your Items Get Indexed</span></span>](#ensuring-your-items-get-indexed)
-   [<span data-ttu-id="bb5f9-118">Installazione e registrazione di gestori di proprietà</span><span class="sxs-lookup"><span data-stu-id="bb5f9-118">Installing and Registering Property Handlers</span></span>](#installing-and-registering-property-handlers)
-   [<span data-ttu-id="bb5f9-119">Test e risoluzione dei problemi relativi ai gestori di proprietà</span><span class="sxs-lookup"><span data-stu-id="bb5f9-119">Testing and Troubleshooting Property Handlers</span></span>](#testing-and-troubleshooting-property-handlers)
    -   [<span data-ttu-id="bb5f9-120">Test di installazione e configurazione</span><span class="sxs-lookup"><span data-stu-id="bb5f9-120">Installation and Setup Tests</span></span>](#installation-and-setup-tests)
    -   [<span data-ttu-id="bb5f9-121">Risoluzione dei problemi relativi ai gestori di proprietà</span><span class="sxs-lookup"><span data-stu-id="bb5f9-121">Troubleshooting Property Handlers</span></span>](#troubleshooting-property-handlers)
-   [<span data-ttu-id="bb5f9-122">Utilizzo di System-Supplied gestori di proprietà</span><span class="sxs-lookup"><span data-stu-id="bb5f9-122">Using System-Supplied Property Handlers</span></span>](#using-system-supplied-property-handlers)
-   [<span data-ttu-id="bb5f9-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bb5f9-123">Related topics</span></span>](#related-topics)

 

## <a name="design-decisions-for-property-handlers"></a><span data-ttu-id="bb5f9-124">Decisioni di progettazione per i gestori di proprietà</span><span class="sxs-lookup"><span data-stu-id="bb5f9-124">Design Decisions for Property Handlers</span></span>

<span data-ttu-id="bb5f9-125">L'implementazione dei gestori delle proprietà prevede i passaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="bb5f9-125">Implementing property handlers involves the following steps:</span></span>

1.  <span data-ttu-id="bb5f9-126">Prendere decisioni di progettazione relative alle proprietà che si desidera supportare.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-126">Making design decisions regarding the properties you want to support.</span></span>
2.  <span data-ttu-id="bb5f9-127">Creazione di un file di descrizione della proprietà (. propdesc) per le proprietà non già presenti nel sistema di proprietà.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-127">Creating a Property Description (.propdesc) file for properties not already in the property system.</span></span>
3.  <span data-ttu-id="bb5f9-128">Implementazione e test del gestore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-128">Implementing and testing the property handler.</span></span>
4.  <span data-ttu-id="bb5f9-129">Installazione e registrazione dei file di descrizione della proprietà e del gestore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-129">Installing and registering the property handler and property description files.</span></span>
5.  <span data-ttu-id="bb5f9-130">Test dell'installazione e della registrazione del gestore proprietà.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-130">Testing property handler installation and registration.</span></span>

<span data-ttu-id="bb5f9-131">Prima di iniziare, è necessario prendere in considerazione le seguenti domande di progettazione:</span><span class="sxs-lookup"><span data-stu-id="bb5f9-131">Before you begin, you need to consider the following design questions:</span></span>

-   <span data-ttu-id="bb5f9-132">Quali proprietà sono supportate dal formato di file?</span><span class="sxs-lookup"><span data-stu-id="bb5f9-132">What properties does/should the file format support?</span></span>
-   <span data-ttu-id="bb5f9-133">Queste proprietà sono già nello schema del sistema?</span><span class="sxs-lookup"><span data-stu-id="bb5f9-133">Are these properties already in the System schema?</span></span>
-   <span data-ttu-id="bb5f9-134">È possibile utilizzare un gestore di proprietà esistente fornito dal sistema?</span><span class="sxs-lookup"><span data-stu-id="bb5f9-134">Can I use an existing system-supplied property handler?</span></span>
-   <span data-ttu-id="bb5f9-135">Quali proprietà possono essere visualizzate agli utenti finali?</span><span class="sxs-lookup"><span data-stu-id="bb5f9-135">Which properties can be displayed to end users?</span></span>
-   <span data-ttu-id="bb5f9-136">Quali proprietà possono essere modificate dagli utenti?</span><span class="sxs-lookup"><span data-stu-id="bb5f9-136">Which properties can users edit?</span></span>
-   <span data-ttu-id="bb5f9-137">Il supporto per la ricerca full-text proviene da un gestore di proprietà o da un filtro?</span><span class="sxs-lookup"><span data-stu-id="bb5f9-137">Should support for full-text search come from a property handler or a filter?</span></span>
-   <span data-ttu-id="bb5f9-138">È necessario supportare le applicazioni legacy?</span><span class="sxs-lookup"><span data-stu-id="bb5f9-138">Do I need to support legacy applications?</span></span> <span data-ttu-id="bb5f9-139">In tal caso, cosa si implementa?</span><span class="sxs-lookup"><span data-stu-id="bb5f9-139">If so, what do I implement?</span></span>

> [!Note]  
> <span data-ttu-id="bb5f9-140">Prima di continuare, vedere [uso di System-Supplied gestori di proprietà](#using-system-supplied-property-handlers) per verificare se è possibile usare un gestore di proprietà fornito dal sistema, risparmiando tempo e risorse di sviluppo.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-140">Before continuing, see [Using System-Supplied Property Handlers](#using-system-supplied-property-handlers) to see if you can use a system-supplied property handler, saving you both time and development resources.</span></span>

 

<span data-ttu-id="bb5f9-141">Dopo aver preso queste decisioni, è possibile scrivere descrizioni formali delle proprietà personalizzate in modo che il motore di ricerca di Windows possa iniziare a indicizzare i file e le proprietà.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-141">After you have made these decisions, you can write formal descriptions of your custom properties so that the Windows Search engine can begin indexing your files and properties.</span></span> <span data-ttu-id="bb5f9-142">Queste descrizioni formali sono file XML, descritti nello [schema della descrizione della proprietà](/previous-versions//cc144127(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="bb5f9-142">These formal descriptions are XML files, described in [Property Description Schema](/previous-versions//cc144127(v=vs.85)).</span></span>

### <a name="property-decisions"></a><span data-ttu-id="bb5f9-143">Decisioni sulle proprietà</span><span class="sxs-lookup"><span data-stu-id="bb5f9-143">Property Decisions</span></span>

<span data-ttu-id="bb5f9-144">Quando si considerano le proprietà da supportare, è necessario identificare le esigenze di indicizzazione e ricerca degli utenti.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-144">When considering which properties to support, you should identify your users' indexing and searching needs.</span></span> <span data-ttu-id="bb5f9-145">Ad esempio, si potrebbe essere in grado di identificare 100 proprietà potenzialmente utili per il tipo di file, ma gli utenti potrebbero essere interessati alla ricerca solo in pochi.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-145">For example, you may be able to identify one hundred potentially useful properties for your file type, but users may be interested in searching on only a handful.</span></span> <span data-ttu-id="bb5f9-146">Inoltre, è possibile che si desideri visualizzare un gruppo diverso, più grande o più piccolo, di tali proprietà per gli utenti in Esplora risorse e consentire agli utenti di modificare solo un subset di tali proprietà visualizzate.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-146">Furthermore, you may want to display a different, larger or smaller, group of those properties to users in Windows Explorer, and allow users to edit only a subset of those properties displayed.</span></span>

<span data-ttu-id="bb5f9-147">Il tipo di file può supportare qualsiasi proprietà personalizzata definita dall'utente, oltre a un set di proprietà definite dal sistema.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-147">Your file type can support any custom properties you define, as well as a set of system-defined properties.</span></span> <span data-ttu-id="bb5f9-148">Prima di creare una proprietà personalizzata, verificare le [proprietà di sistema](https://msdn.microsoft.com/library/bb763010(VS.85).aspx) per verificare se la proprietà che si desidera supportare è già definita da una proprietà di sistema.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-148">Before you create a custom property, please review [System Properties](https://msdn.microsoft.com/library/bb763010(VS.85).aspx) to see if the property you want to support is already defined by a system property.</span></span> <span data-ttu-id="bb5f9-149">Assicurarsi sempre di supportare le proprietà più importanti definite dal sistema.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-149">Always be sure you support the most important system-defined properties.</span></span>

<span data-ttu-id="bb5f9-150">Per progettare le proprietà è consigliabile usare una matrice:</span><span class="sxs-lookup"><span data-stu-id="bb5f9-150">We recommend using a matrix to help you design your properties:</span></span>



| <span data-ttu-id="bb5f9-151">Nome proprietà</span><span class="sxs-lookup"><span data-stu-id="bb5f9-151">Property name</span></span> | <span data-ttu-id="bb5f9-152">È indicizzabile?</span><span class="sxs-lookup"><span data-stu-id="bb5f9-152">Is indexable?</span></span> | <span data-ttu-id="bb5f9-153">È visualizzabile?</span><span class="sxs-lookup"><span data-stu-id="bb5f9-153">Is displayable?</span></span> | <span data-ttu-id="bb5f9-154">È modificabile?</span><span class="sxs-lookup"><span data-stu-id="bb5f9-154">Is editable?</span></span> |
|---------------|---------------|-----------------|--------------|
| <span data-ttu-id="bb5f9-155">property1</span><span class="sxs-lookup"><span data-stu-id="bb5f9-155">property1</span></span>     | <span data-ttu-id="bb5f9-156">S</span><span class="sxs-lookup"><span data-stu-id="bb5f9-156">Y</span></span>             | <span data-ttu-id="bb5f9-157">S</span><span class="sxs-lookup"><span data-stu-id="bb5f9-157">Y</span></span>               | <span data-ttu-id="bb5f9-158">N</span><span class="sxs-lookup"><span data-stu-id="bb5f9-158">N</span></span>            |
| <span data-ttu-id="bb5f9-159">Proprietà...</span><span class="sxs-lookup"><span data-stu-id="bb5f9-159">property...</span></span>   | <span data-ttu-id="bb5f9-160">S</span><span class="sxs-lookup"><span data-stu-id="bb5f9-160">Y</span></span>             | <span data-ttu-id="bb5f9-161">S</span><span class="sxs-lookup"><span data-stu-id="bb5f9-161">Y</span></span>               | <span data-ttu-id="bb5f9-162">N</span><span class="sxs-lookup"><span data-stu-id="bb5f9-162">N</span></span>            |
| <span data-ttu-id="bb5f9-163">propertyN</span><span class="sxs-lookup"><span data-stu-id="bb5f9-163">propertyn</span></span>     | <span data-ttu-id="bb5f9-164">N</span><span class="sxs-lookup"><span data-stu-id="bb5f9-164">N</span></span>             | <span data-ttu-id="bb5f9-165">N</span><span class="sxs-lookup"><span data-stu-id="bb5f9-165">N</span></span>               | <span data-ttu-id="bb5f9-166">N</span><span class="sxs-lookup"><span data-stu-id="bb5f9-166">N</span></span>            |



 

<span data-ttu-id="bb5f9-167">Per ognuna di queste proprietà, è necessario determinare gli attributi che devono avere e quindi descriverli formalmente in file XML di descrizione della proprietà (. propdesc).</span><span class="sxs-lookup"><span data-stu-id="bb5f9-167">For each of these properties, you need to determine what attributes it should have and then describe them formally in Property Description XML files (.propdesc).</span></span> <span data-ttu-id="bb5f9-168">Gli attributi includono il tipo di dati della proprietà, l'etichetta, la stringa della guida e altro ancora.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-168">Attributes include the property's data type, label, help string and more.</span></span> <span data-ttu-id="bb5f9-169">Per le proprietà indicizzabili, è necessario prestare particolare attenzione ai seguenti attributi di proprietà trovati nell'elemento XML [searchInfo](../properties/propdesc-schema-searchinfo.md)   del file di descrizione della proprietà.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-169">For indexable properties, you should pay particular attention to the following property attributes found in the [searchInfo](../properties/propdesc-schema-searchinfo.md)   XML element of the Property Description file.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bb5f9-170">Attributo</span><span class="sxs-lookup"><span data-stu-id="bb5f9-170">Attribute</span></span></th>
<th><span data-ttu-id="bb5f9-171">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bb5f9-171">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bb5f9-172">inInvertedIndex</span><span class="sxs-lookup"><span data-stu-id="bb5f9-172">inInvertedIndex</span></span></td>
<td><span data-ttu-id="bb5f9-173">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-173">Optional.</span></span> <span data-ttu-id="bb5f9-174">Indica se il valore di una proprietà di stringa deve essere suddiviso in parole e ogni parola archiviata nell'indice invertito.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-174">Indicates whether a string property value should be broken into words and each word stored in the inverted index.</span></span> <span data-ttu-id="bb5f9-175">L'indice invertito consente una ricerca efficiente di parole e frasi sul valore della proprietà usando CONTAINs o FREETEXT (ad esempio, SELECT... DOVE contiene &quot; someText &quot; ).</span><span class="sxs-lookup"><span data-stu-id="bb5f9-175">The inverted index enables efficient searching for words and phrases over the property value using CONTAINS or FREETEXT (for example, SELECT ... WHERE CONTAINS &quot;sometext&quot;).</span></span> <span data-ttu-id="bb5f9-176">Se è impostato su <strong>false</strong>, le ricerche vengono eseguite sull'intera stringa.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-176">If set to <strong>FALSE</strong>, searches are done against the whole string.</span></span> <span data-ttu-id="bb5f9-177">La maggior parte delle proprietà di stringa deve avere questo valore impostato su <strong>true</strong>; per le proprietà non di stringa è necessario impostare questo valore su <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-177">Most string properties should have this set to <strong>TRUE</strong>; non-string properties should have this set to <strong>FALSE</strong>.</span></span> <span data-ttu-id="bb5f9-178">Il valore predefinito è <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-178">The default is <strong>FALSE</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bb5f9-179">isColumn</span><span class="sxs-lookup"><span data-stu-id="bb5f9-179">isColumn</span></span></td>
<td><span data-ttu-id="bb5f9-180">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-180">Optional.</span></span> <span data-ttu-id="bb5f9-181">Indica se la proprietà deve essere archiviata nel database di ricerca di Windows come colonna.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-181">Indicates whether the property should be stored in the Windows Search database as a column.</span></span> <span data-ttu-id="bb5f9-182">L'archiviazione della proprietà come colonna consente il recupero, l'ordinamento, il raggruppamento e il filtro, ovvero l'utilizzo di qualsiasi predicato eccetto CONTAINs o FREETEXT per l'intero valore della colonna.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-182">Storing the property as a column enables retrieving, sorting, grouping, and filtering (that is, using any predicate except CONTAINS or FREETEXT) on the whole column value.</span></span> <span data-ttu-id="bb5f9-183">Le proprietà visualizzate per l'utente devono essere impostate su <strong>true</strong> , a meno che non si tratti di una proprietà testuale molto grande, ad esempio il corpo di un documento, in cui verrebbe eseguita la ricerca nell'indice invertito.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-183">Properties displayed to the user should have this set to <strong>TRUE</strong> unless it is a very large textual property (like the body of a document) that would be searched in the inverted index.</span></span> <span data-ttu-id="bb5f9-184">Il valore predefinito è <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-184">The default is <strong>FALSE</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bb5f9-185">isColumnSparse</span><span class="sxs-lookup"><span data-stu-id="bb5f9-185">isColumnSparse</span></span></td>
<td><span data-ttu-id="bb5f9-186">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-186">Optional.</span></span> <span data-ttu-id="bb5f9-187">Indica se una proprietà non occupa alcuno spazio se il valore è <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-187">Indicates whether a property takes no space if the value is <strong>NULL</strong>.</span></span> <span data-ttu-id="bb5f9-188">Una proprietà non di tipo sparse occupa spazio per ogni elemento, anche se il valore è <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-188">A non-sparse property takes space for every item, even if the value is <strong>NULL</strong>.</span></span> <span data-ttu-id="bb5f9-189">Se la proprietà è multivalore, questo attributo è sempre <strong>true</strong>.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-189">If the property is multi-valued, this attribute is always <strong>TRUE</strong>.</span></span> <span data-ttu-id="bb5f9-190">Questo attributo deve essere <strong>false</strong> solo se è presente un valore per ogni elemento.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-190">This attribute should be <strong>FALSE</strong> only if a value is present for every item.</span></span> <span data-ttu-id="bb5f9-191">Il valore predefinito è <strong>true</strong>.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-191">The default is <strong>TRUE</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bb5f9-192">columnIndexType</span><span class="sxs-lookup"><span data-stu-id="bb5f9-192">columnIndexType</span></span></td>
<td><span data-ttu-id="bb5f9-193">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-193">Optional.</span></span> <span data-ttu-id="bb5f9-194">Per ottimizzare l'esecuzione di query, il motore di ricerca di Windows può creare indici secondari per le proprietà con la colonna =<strong>true</strong>.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-194">To optimize querying, the Windows Search engine can create secondary indices for properties that have isColumn=<strong>TRUE</strong>.</span></span> <span data-ttu-id="bb5f9-195">Questa operazione richiede più spazio di elaborazione e spazio su disco durante l'indicizzazione, ma migliora le prestazioni durante l'esecuzione di query.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-195">This requires more processing and disk space during indexing, but improves performance during querying.</span></span> <span data-ttu-id="bb5f9-196">Se la proprietà tende a essere ordinata, raggruppata o filtrata (ovvero usando =,! =, <, >, LIKE, corrisponde) spesso dagli utenti, questo attributo deve essere impostato su &quot; ondisk &quot; .</span><span class="sxs-lookup"><span data-stu-id="bb5f9-196">If the property tends to be sorted, grouped, or filtered (that is, using =, !=, <, >, LIKE, MATCHES) frequently by users, this attribute should be set to &quot;OnDisk&quot;.</span></span> <span data-ttu-id="bb5f9-197">Il valore predefinito è &quot; NotIndexed &quot; .</span><span class="sxs-lookup"><span data-stu-id="bb5f9-197">The default is &quot;NotIndexed&quot;.</span></span> <span data-ttu-id="bb5f9-198">I valori seguenti sono validi:</span><span class="sxs-lookup"><span data-stu-id="bb5f9-198">The following values are valid:</span></span>
<ul>
<li><span data-ttu-id="bb5f9-199">NotIndexed: non viene creato alcun indice secondario.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-199">NotIndexed: No secondary index is created.</span></span></li>
<li><span data-ttu-id="bb5f9-200">Ondisk: creare e archiviare un indice secondario sul disco.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-200">OnDisk: Create and store a secondary index on disk.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bb5f9-201">maxSize</span><span class="sxs-lookup"><span data-stu-id="bb5f9-201">maxSize</span></span></td>
<td><span data-ttu-id="bb5f9-202">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-202">Optional.</span></span> <span data-ttu-id="bb5f9-203">Indica la dimensione massima consentita per il valore della proprietà archiviato nel database di ricerca di Windows.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-203">Indicates the maximum size allowed for the property value stored in the Windows search database.</span></span> <span data-ttu-id="bb5f9-204">Questo limite si applica agli elementi ciascun indvidual di un vettore, non all'intero vettore.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-204">This limit applies to the indvidual elements of a vector, not the vector as a whole.</span></span> <span data-ttu-id="bb5f9-205">I valori che superano questa dimensione vengono troncati.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-205">Values beyond this size are truncated.</span></span> <span data-ttu-id="bb5f9-206">Il valore predefinito è &quot; 128 &quot; (byte).</span><span class="sxs-lookup"><span data-stu-id="bb5f9-206">The default is &quot;128&quot; (bytes).</span></span><br/> <span data-ttu-id="bb5f9-207">Attualmente, Windows Search non usa maxSize durante il calcolo della quantità di dati accettati da un file.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-207">Currently, Windows Search does not use the maxSize when calculating the amount of data it accepts from a file.</span></span> <span data-ttu-id="bb5f9-208">Al contrario, il limite usato da Windows Search è il prodotto delle dimensioni del file e il valore di MaxGrowFactor (file size N \* MaxGrowFactor) letto dal registro di sistema in HKEY_LOCAL_MACHINE->software->Microsoft->Windows Search->Gathering Manager->MaxGrowFactor.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-208">Instead, the limit Windows Search uses is the product of the size of the file and the MaxGrowFactor (file size N \* MaxGrowFactor) read from the registry at HKEY_LOCAL_MACHINE->Software->Microsoft->Windows Search->Gathering Manager->MaxGrowFactor.</span></span> <span data-ttu-id="bb5f9-209">Il valore predefinito di MaxGrowFactor è quattro (4).</span><span class="sxs-lookup"><span data-stu-id="bb5f9-209">The default MaxGrowFactor is four (4).</span></span> <span data-ttu-id="bb5f9-210">Di conseguenza, se il tipo di file tende a essere ridotto in dimensioni totali ma con proprietà più grandi, è possibile che Windows Search non accetti tutti i dati di proprietà che si desidera creare.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-210">Consequently, if your file type tends to be small in total size but have larger properties, Windows Search may not accept all the property data you want to emit.</span></span> <span data-ttu-id="bb5f9-211">Tuttavia, è possibile aumentare il MaxGrowFactor in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-211">However, you can increase the MaxGrowFactor to suit your needs.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="bb5f9-212">Per l'attributo columnIndexType, il vantaggio di una query più veloce deve essere ponderato rispetto al tempo di indicizzazione e ai costi di spazio maggiori che gli indici secondari possono sostenere.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-212">For the columnIndexType attribute, the benefit of faster queries needs to be weighed against the greater indexing time and space costs that the secondary indices can incur.</span></span> <span data-ttu-id="bb5f9-213">Questo costo viene tuttavia pagato solo per gli elementi con un valore non **null** , quindi per la maggior parte delle proprietà questo attributo può essere impostato su "ondisk".</span><span class="sxs-lookup"><span data-stu-id="bb5f9-213">However, this cost is only paid for items that have a non-**null** value, so for most properties can have this attribute set to "OnDisk".</span></span>

 

### <a name="full-text-support"></a><span data-ttu-id="bb5f9-214">Supporto full-text</span><span class="sxs-lookup"><span data-stu-id="bb5f9-214">Full-Text Support</span></span>

<span data-ttu-id="bb5f9-215">In generale, la ricerca full-text è supportata dai componenti chiamati [filtri](-search-3x-wds-extidx-filters.md); Tuttavia, per i tipi di file basati su testo con formati di file non complicati, i gestori di proprietà possono essere in grado di fornire questa funzionalità con un minor sforzo di sviluppo.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-215">Generally speaking, full-text search is supported by components called [filters](-search-3x-wds-extidx-filters.md); however, for text-based file types with uncomplicated file formats, property handlers may be able to provide this functionality with less development effort.</span></span> <span data-ttu-id="bb5f9-216">È consigliabile esaminare la sezione del [contenuto full-text](../properties/building-property-handlers-property-handlers.md) per un confronto tra le funzionalità di filtro e di gestione delle proprietà che consentono di decidere quale sia la soluzione migliore per il tipo di file.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-216">You should review the [Full-Text Contents](../properties/building-property-handlers-property-handlers.md) section for a comparison of filter and property handler functionality to help you decide what is best for your file type.</span></span> <span data-ttu-id="bb5f9-217">Di particolare importanza è il fatto che i filtri possono gestire gli identificatori di codice in più lingue (LCID) per ogni file, mentre i gestori di proprietà non possono.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-217">Of particular importance is the fact that filters can handle multiple language code identifiers (LCIDs) per file while property handlers cannot.</span></span>

> [!Note]  
> <span data-ttu-id="bb5f9-218">Poiché i gestori di proprietà non possono suddividere il contenuto nel modo in cui i filtri possono, i file di grandi dimensioni (anche se sono formati di file non complicati) devono essere completamente caricati in memoria.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-218">Because property handlers cannot chunk content the way filters can, large files (even if they are uncomplicated file formats) must be completely loaded into memory.</span></span>

 

### <a name="operating-system-implementatation-considerations"></a><span data-ttu-id="bb5f9-219">Considerazioni sul Implementatation del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="bb5f9-219">Operating System Implementatation Considerations</span></span>

### <a name="implementation-information-for-windows-7"></a><span data-ttu-id="bb5f9-220">Informazioni di implementazione per Windows 7</span><span class="sxs-lookup"><span data-stu-id="bb5f9-220">Implementation Information for Windows 7</span></span>

<span data-ttu-id="bb5f9-221">In Windows 7 e versioni successive, si verifica un nuovo comportamento quando si registra un gestore di proprietà, un [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)o una nuova estensione.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-221">In Windows 7 and later, there is new behavior when registering a property handler, [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter), or new extension.</span></span> <span data-ttu-id="bb5f9-222">Quando viene installato un nuovo gestore di proprietà e/o **IFilter** , i file con le estensioni corrispondenti vengono automaticamente reindicizzati.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-222">When a new property handler and/or **IFilter** is installed, files with the corresponding extensions are automatically reindexed.</span></span>

<span data-ttu-id="bb5f9-223">In Windows 7 è consigliabile installare un [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) insieme ai gestori di proprietà corrispondenti e che **IFilter** venga registrato prima del gestore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-223">In Windows 7 it is recommended that an [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) is installed in conjunction with its corresponding property handlers, and that the **IFilter** is registered before the property handler.</span></span> <span data-ttu-id="bb5f9-224">La registrazione del gestore delle proprietà avvia la reindicizzazione immediata dei file indicizzati in precedenza senza dover prima riavviare il computer e sfrutta tutti gli IFilter registrati in precedenza ai fini dell'indicizzazione del contenuto.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-224">The registration of the property handler initiates immediate re-indexing of previously indexed files without first requiring a reboot, and takes advantage of any previously registered IFilter(s) for the purpose of content indexing.</span></span>

<span data-ttu-id="bb5f9-225">Se è installato solo un [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) , senza un gestore proprietà corrispondente, la reindicizzazione automatica viene eseguita dopo il riavvio del servizio di indicizzazione o il riavvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-225">If only an [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) is installed, without a corresponding property handler, then automatic reindexing occurs either after a restart of the indexing service, or a reboot of the system.</span></span>

<span data-ttu-id="bb5f9-226">Per i flag di descrizione della proprietà specifici di Windows 7, vedere gli argomenti di riferimento seguenti:</span><span class="sxs-lookup"><span data-stu-id="bb5f9-226">For property description flags specific to Windows 7, see the following reference topics:</span></span>

-   [<span data-ttu-id="bb5f9-227">GETPROPERTYSTOREFLAGS</span><span class="sxs-lookup"><span data-stu-id="bb5f9-227">GETPROPERTYSTOREFLAGS</span></span>](/windows/win32/api/propsys/ne-propsys-getpropertystoreflags)
-   [<span data-ttu-id="bb5f9-228">tipo di PROPDESC \_ COLUMNINDEX \_</span><span class="sxs-lookup"><span data-stu-id="bb5f9-228">PROPDESC\_COLUMNINDEX\_TYPE</span></span>](/windows/win32/api/propsys/ne-propsys-propdesc_columnindex_type)
-   [<span data-ttu-id="bb5f9-229">\_flag SEARCHINFO \_ PROPDESC</span><span class="sxs-lookup"><span data-stu-id="bb5f9-229">PROPDESC\_SEARCHINFO\_FLAGS</span></span>](/windows/win32/api/propsys/ne-propsys-propdesc_searchinfo_flags)

### <a name="implementation-information-for-windows-vista-and-earlier"></a><span data-ttu-id="bb5f9-230">Informazioni di implementazione per Windows Vista e versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="bb5f9-230">Implementation Information for Windows Vista and Earlier</span></span>

<span data-ttu-id="bb5f9-231">Prima di Windows Vista, i filtri fornivano il supporto per l'analisi e l'enumerazione di contenuto e proprietà del file.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-231">Prior to Windows Vista, filters provided support for parsing and enumerating file content and properties.</span></span> <span data-ttu-id="bb5f9-232">Con l'introduzione del sistema di proprietà, i gestori delle proprietà gestiscono le proprietà dei file mentre i filtri gestiscono il contenuto del file.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-232">With the introduction of the property system, property handlers handle file properties while filters handle file content.</span></span> <span data-ttu-id="bb5f9-233">Per Windows Vista, è necessario sviluppare solo un'implementazione parziale dell'interfaccia [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)in coordinamento con un gestore di proprietà, come descritto in [procedure consigliate per la creazione di gestori di filtro in Windows Search](-search-3x-wds-extidx-filters.md).</span><span class="sxs-lookup"><span data-stu-id="bb5f9-233">For Windows Vista, you need develop only a partial implementation of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)interface in coordination with a property handler, as described in [Best Practices for Creating Filter Handlers in Windows Search](-search-3x-wds-extidx-filters.md).</span></span>

<span data-ttu-id="bb5f9-234">Sebbene il sistema di proprietà sia incluso anche nell'installazione di Windows Search per Windows XP, le applicazioni di terze parti e legacy possono richiedere che i filtri gestiscano sia il contenuto che le proprietà.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-234">While the property system is also included with the Windows Search installation for Windows XP, third-party and legacy applications may require that filters handle both content and properties.</span></span> <span data-ttu-id="bb5f9-235">Pertanto, se si sta sviluppando sulla piattaforma Windows XP, è necessario fornire un'implementazione di filtro completo e un gestore di proprietà per il tipo di file o la proprietà personalizzata.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-235">Therefore, if you are developing on the Windows XP platform, you should provide a full filter implementation as well as a property handler for your file type or custom property.</span></span>

 

## <a name="writing-property-description-files"></a><span data-ttu-id="bb5f9-236">Scrittura dei file di descrizione delle proprietà</span><span class="sxs-lookup"><span data-stu-id="bb5f9-236">Writing Property Description Files</span></span>

<span data-ttu-id="bb5f9-237">La struttura dei file XML di descrizione della proprietà (con estensione propdesc) è descritta nell'argomento [PropertyDescription](../properties/propdesc-schema-propertydescription.md) .</span><span class="sxs-lookup"><span data-stu-id="bb5f9-237">The structure of property description XML files (.propdesc) is described in the [propertyDescription](../properties/propdesc-schema-propertydescription.md) topic.</span></span> <span data-ttu-id="bb5f9-238">Di particolare interesse per la ricerca sono gli attributi dell'elemento [searchInfo](../properties/propdesc-schema-searchinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="bb5f9-238">Of particular interest for search are the attributes of the [searchInfo](../properties/propdesc-schema-searchinfo.md) element.</span></span> <span data-ttu-id="bb5f9-239">Dopo aver deciso quali proprietà supportare, è necessario creare e registrare i file di descrizione delle proprietà per ogni proprietà.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-239">Once you've decided which properties to support, you need to create and register property description files for each properties.</span></span> <span data-ttu-id="bb5f9-240">Quando si registrano i file con estensione propdesc, questi vengono inclusi nell'elenco di descrizioni delle proprietà dello schema e diventano nomi di colonna all'interno dell'archivio delle proprietà del motore di ricerca.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-240">When you register your .propdesc files, they are included in the schema's property description list and become column names within the Search engine's property store.</span></span>

<span data-ttu-id="bb5f9-241">È possibile registrare le descrizioni delle proprietà personalizzate utilizzando la funzione [PSRegisterPropertySchema](/windows/win32/api/propsys/nf-propsys-psregisterpropertyschema) , un'API wrapper che chiama IPropertySystem:: RegisterPropertySchema del sottosistema dello schema.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-241">You can register your custom property descriptions using the [PSRegisterPropertySchema](/windows/win32/api/propsys/nf-propsys-psregisterpropertyschema) function, a wrapper API that calls the schema subsystem's IPropertySystem::RegisterPropertySchema.</span></span> <span data-ttu-id="bb5f9-242">Questa funzione informa il sottosistema dello schema dell'aggiunta di file di schema di descrizione della proprietà (. propdesc), usando i percorsi di file nei file con estensione propdesc nel computer locale, in genere la directory di installazione dell'applicazione in "programmi".</span><span class="sxs-lookup"><span data-stu-id="bb5f9-242">This function informs the schema subsystem of the addition of property description schema (.propdesc) files, using file path(s) to the .propdesc file(s) on the local machine, usually the application's install directory under "Program Files".</span></span> <span data-ttu-id="bb5f9-243">In genere, un'installazione o un'applicazione (ad esempio, il programma di installazione del gestore di proprietà) chiamerà questo metodo dopo l'installazione dei file con estensione propdesc.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-243">Typically, a setup or application (for example, your property handler installer) will call this method after installing the .propdesc file(s).</span></span>

 

## <a name="implementing-property-handlers"></a><span data-ttu-id="bb5f9-244">Implementazione di gestori di proprietà</span><span class="sxs-lookup"><span data-stu-id="bb5f9-244">Implementing Property Handlers</span></span>

<span data-ttu-id="bb5f9-245">Lo sviluppo di un gestore di proprietà comporta l'implementazione delle interfacce seguenti:</span><span class="sxs-lookup"><span data-stu-id="bb5f9-245">Developing a property handler involves implementing the following interfaces:</span></span>

-   <span data-ttu-id="bb5f9-246">IInitialzeWithStream: fornisce l'inizializzazione basata sul flusso del gestore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-246">IInitialzeWithStream: Provides stream-based initialization of your property handler.</span></span>
-   <span data-ttu-id="bb5f9-247">IPropertyStore: enumera, ottiene e imposta i valori delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-247">IPropertyStore: Enumerates, gets, and sets property values.</span></span>
-   <span data-ttu-id="bb5f9-248">IPropertyStoreCapabilities: facoltativo.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-248">IPropertyStoreCapabilities: Optional.</span></span> <span data-ttu-id="bb5f9-249">Indica se gli utenti possono modificare una proprietà da un'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-249">Identifies whether users can edit a property from a user interface.</span></span>

### <a name="iinitializewithstream"></a><span data-ttu-id="bb5f9-250">IInitializeWithStream</span><span class="sxs-lookup"><span data-stu-id="bb5f9-250">IInitializeWithStream</span></span>

<span data-ttu-id="bb5f9-251">Come descritto nell'argomento relativo al [sistema di proprietà](../properties/building-property-handlers.md) , è consigliabile implementare i gestori di proprietà con **IInitializeWithStream** per eseguire l'inizializzazione basata sul flusso.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-251">As described in the [Property System](../properties/building-property-handlers.md) topic, we strongly recommend implementing property handlers with **IInitializeWithStream** to do stream-based initialization.</span></span> <span data-ttu-id="bb5f9-252">Se si sceglie di non implementare IInitializeWithStream, il gestore della proprietà deve rifiutare esplicitamente l'esecuzione nel processo di isolamento impostando il flag DisableProcessIsolation nella chiave del registro di sistema del gestore proprietà.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-252">If you chose not to implement IInitializeWithStream, the property handler must opt out of running in the isolation process by setting the DisableProcessIsolation flag on the property handler's registry key.</span></span> <span data-ttu-id="bb5f9-253">La disabilitazione dell'isolamento dei processi è in genere destinata solo ai gestori di proprietà legacy e deve essere evitata con qualsiasi nuovo codice.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-253">Disabling process isolation is generally intended only for legacy property handlers and should be strenuously avoided by any new code.</span></span>

### <a name="ipropertystore"></a><span data-ttu-id="bb5f9-254">IPropertyStore</span><span class="sxs-lookup"><span data-stu-id="bb5f9-254">IPropertyStore</span></span>

<span data-ttu-id="bb5f9-255">Per creare un gestore di proprietà, è necessario implementare l'interfaccia [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) con i metodi seguenti.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-255">To create a property handler, you must implement the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface with the following methods.</span></span>



| <span data-ttu-id="bb5f9-256">Metodo</span><span class="sxs-lookup"><span data-stu-id="bb5f9-256">Method</span></span>   | <span data-ttu-id="bb5f9-257">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bb5f9-257">Description</span></span>                                                         |
|----------|---------------------------------------------------------------------|
| <span data-ttu-id="bb5f9-258">Commit</span><span class="sxs-lookup"><span data-stu-id="bb5f9-258">Commit</span></span>   | <span data-ttu-id="bb5f9-259">Salva una modifica apportata a una proprietà nel file.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-259">Saves a property change to the file.</span></span>                                |
| <span data-ttu-id="bb5f9-260">GetAt</span><span class="sxs-lookup"><span data-stu-id="bb5f9-260">GetAt</span></span>    | <span data-ttu-id="bb5f9-261">Recupera una chiave di proprietà dalla matrice di proprietà di un elemento.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-261">Retrieves a property key from an item's array of properties.</span></span>        |
| <span data-ttu-id="bb5f9-262">GetCount</span><span class="sxs-lookup"><span data-stu-id="bb5f9-262">GetCount</span></span> | <span data-ttu-id="bb5f9-263">Ottiene il numero di proprietà associate al file.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-263">Gets the number of properties attached to the file.</span></span>                 |
| <span data-ttu-id="bb5f9-264">GetValue</span><span class="sxs-lookup"><span data-stu-id="bb5f9-264">GetValue</span></span> | <span data-ttu-id="bb5f9-265">Recupera i dati per una proprietà specifica.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-265">Retrieves data for a specific property.</span></span>                             |
| <span data-ttu-id="bb5f9-266">SetValue</span><span class="sxs-lookup"><span data-stu-id="bb5f9-266">SetValue</span></span> | <span data-ttu-id="bb5f9-267">Imposta un nuovo valore della proprietà o sostituisce o rimuove un valore esistente.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-267">Sets a new property value or replaces or removes an existing value.</span></span> |



 

 

 

<span data-ttu-id="bb5f9-268">Importanti considerazioni per l'implementazione di questa interfaccia sono incluse nella documentazione di [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) .</span><span class="sxs-lookup"><span data-stu-id="bb5f9-268">Important considerations for implementing this interface are included in the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) documentation.</span></span>

> [!Note]  
> <span data-ttu-id="bb5f9-269">Se il gestore delle proprietà emette più valori per la stessa proprietà per un determinato elemento, solo l'ultimo valore emesso viene archiviato nel catalogo.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-269">If your property handler emits multiple values for the same property for a given item, only the last value emitted is stored in the catalog.</span></span>

 

 

### <a name="ipropertystorecapabilities"></a><span data-ttu-id="bb5f9-270">IPropertyStoreCapabilities</span><span class="sxs-lookup"><span data-stu-id="bb5f9-270">IPropertyStoreCapabilities</span></span>

<span data-ttu-id="bb5f9-271">I gestori di proprietà possono implementare facoltativamente questa interfaccia per disabilitare la capacità di un utente di modificare proprietà specifiche.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-271">Property handlers can optionally implement this interface to disable a user's ability to edit specific properties.</span></span> <span data-ttu-id="bb5f9-272">Queste proprietà sono in genere modificabili nella pagina dei dettagli e nel riquadro, ma non sono consentite nel gestore delle proprietà di implementazione.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-272">These properties are normally editable in the Details page and pane but editing them is not allowed under the implementing property handler.</span></span> <span data-ttu-id="bb5f9-273">Implementare correttamente questa interfaccia offre un'esperienza utente migliore rispetto all'alternativa, ovvero un semplice errore di run-time dalla Shell.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-273">Implementing this interface correctly provides a better user experience than the alternative—a simple run-time error from the Shell.</span></span>

 

## <a name="ensuring-your-items-get-indexed"></a><span data-ttu-id="bb5f9-274">Verifica dell'indicizzazione degli elementi</span><span class="sxs-lookup"><span data-stu-id="bb5f9-274">Ensuring Your Items Get Indexed</span></span>

<span data-ttu-id="bb5f9-275">Ora che è stato implementato il gestore delle proprietà, è necessario assicurarsi che gli elementi per i quali viene registrato il gestore vengano indicizzati.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-275">Now that you've implemented your property handler, you want to make sure the items your handler is registered for get indexed.</span></span> <span data-ttu-id="bb5f9-276">È possibile utilizzare [gestione catalogo](-search-3x-wds-mngidx-catalog-manager.md) per avviare la reindicizzazione ed è inoltre possibile utilizzare il [gestore dell'ambito di ricerca per indicizzazione](-search-3x-wds-extidx-csm.md) per configurare le regole predefinite che indicano gli URL per cui l'indicizzatore deve eseguire la ricerca per indicizzazione.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-276">You can use the [Catalog Manager](-search-3x-wds-mngidx-catalog-manager.md) to initiate re-indexing, and you can also use the [Crawl Scope Manager](-search-3x-wds-extidx-csm.md) to set up default rules indicating the URLs you want the Indexer to crawl.</span></span> <span data-ttu-id="bb5f9-277">Un'altra opzione consiste nel seguire l'esempio di codice REINDEX negli [esempi di Windows Search SDK](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8).</span><span class="sxs-lookup"><span data-stu-id="bb5f9-277">Another option is to follow the ReIndex code sample in the [Windows Search SDK Samples](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8).</span></span>

<span data-ttu-id="bb5f9-278">Per ulteriori informazioni, vedere [utilizzo di gestione catalogo](-search-3x-wds-mngidx-catalog-manager.md) e [utilizzo di gestione ambito ricerca per indicizzazione](-search-3x-wds-extidx-csm.md).</span><span class="sxs-lookup"><span data-stu-id="bb5f9-278">For further information, refer to [Using the Catalog Manager](-search-3x-wds-mngidx-catalog-manager.md) and [Using the Crawl Scope Manager](-search-3x-wds-extidx-csm.md).</span></span>

 

## <a name="installing-and-registering-property-handlers"></a><span data-ttu-id="bb5f9-279">Installazione e registrazione di gestori di proprietà</span><span class="sxs-lookup"><span data-stu-id="bb5f9-279">Installing and Registering Property Handlers</span></span>

<span data-ttu-id="bb5f9-280">Con il gestore di proprietà implementato, deve essere registrato e la relativa estensione del nome file associata al gestore.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-280">With the property handler implemented, it must be registered and its file name extension associated with the handler.</span></span> <span data-ttu-id="bb5f9-281">Nell'esempio seguente vengono illustrate le chiavi del registro di sistema e i valori necessari per eseguire questa operazione.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-281">The following example shows the registry keys and values required to do this.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {<CLSID for property handler>}
         (Default) = <Property Handler Name>
         InProcServer32
            (Default) = <full path to property handler dll>
            ThreadingModel = <your threading model>
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               PropertySystem
                  PropertyHandlers
                     <.fileextention>
                        (Default) = {<CLSID for property handler>}
```

 

## <a name="testing-and-troubleshooting-property-handlers"></a><span data-ttu-id="bb5f9-282">Test e risoluzione dei problemi relativi ai gestori di proprietà</span><span class="sxs-lookup"><span data-stu-id="bb5f9-282">Testing and Troubleshooting Property Handlers</span></span>

<span data-ttu-id="bb5f9-283">Nell'elenco seguente vengono forniti consigli sui tipi di test da eseguire:</span><span class="sxs-lookup"><span data-stu-id="bb5f9-283">The following list provides advice on the kinds of tests you should perform:</span></span>

-   <span data-ttu-id="bb5f9-284">Testare il recupero dell'output da ogni singola proprietà supportata dal tipo di file.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-284">Test getting output from every single property supported by the file type.</span></span>
-   <span data-ttu-id="bb5f9-285">Usare i valori di proprietà Big, ad esempio, usare un metatag di grandi dimensioni nei documenti HTML.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-285">Use big property values, for example, use a large metatag in HTML documents.</span></span>
-   <span data-ttu-id="bb5f9-286">Verificare che il gestore delle proprietà non perda gli handle di file modificando l'output del gestore proprietà o utilizzando uno strumento come oh.exe prima e dopo l'enumerazione delle proprietà del file.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-286">Check that the property handler does not leak file handles by editing it after getting output from the property handler, or by using a tool like oh.exe before and after enumerating file properties.</span></span>
-   <span data-ttu-id="bb5f9-287">Testare tutti i tipi di file associati al gestore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-287">Test all file types associated with the property handler.</span></span> <span data-ttu-id="bb5f9-288">Verificare, ad esempio, che il filtro HTML funzioni con i tipi di file con estensione htm e HTML.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-288">For example, check that the HTML filter works with .htm and .html file types.</span></span>
-   <span data-ttu-id="bb5f9-289">Eseguire test con file danneggiati.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-289">Test with corrupted files.</span></span> <span data-ttu-id="bb5f9-290">Il gestore delle proprietà dovrebbe avere esito negativo normalmente.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-290">Property handler should fail gracefully.</span></span>
-   <span data-ttu-id="bb5f9-291">Se un'applicazione supporta la crittografia, verificare che il gestore della proprietà non restituisca il testo crittografato.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-291">If an application supports encryption, test that the property handler does not output encrypted text.</span></span>
-   <span data-ttu-id="bb5f9-292">Se il gestore delle proprietà supporta la ricerca full-text:</span><span class="sxs-lookup"><span data-stu-id="bb5f9-292">If your property handler supports full-text search:</span></span>
    -   <span data-ttu-id="bb5f9-293">Usare più caratteri Unicode speciali nel contenuto del file e testarne l'output.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-293">Use multiple special Unicode characters in the file contents and test for their output.</span></span>
    -   <span data-ttu-id="bb5f9-294">Testare la gestione di documenti di dimensioni molto grandi per assicurarsi che il gestore di proprietà funzioni come previsto.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-294">Test the handling of very large documents to ensure the property handler works as expected.</span></span>

### <a name="installation-and-setup-tests"></a><span data-ttu-id="bb5f9-295">Test di installazione e configurazione</span><span class="sxs-lookup"><span data-stu-id="bb5f9-295">Installation and Setup Tests</span></span>

<span data-ttu-id="bb5f9-296">Infine, è necessario testare le routine di installazione e disinstallazione.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-296">Lastly, you need to test your install and uninstall routines.</span></span>

-   <span data-ttu-id="bb5f9-297">L'installazione deve essere ripristinata da installazioni non riuscite, ad esempio dall'annullamento e dal riavvio del programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-297">Installation must recover from failed installations (for example, from canceling and then restarting setup).</span></span>
-   <span data-ttu-id="bb5f9-298">Uninstall deve eliminare tutti i file associati al gestore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-298">Uninstall must delete all files associated with the property handler.</span></span>
-   <span data-ttu-id="bb5f9-299">La disinstallazione non deve eliminare file diversi da quelli associati all'installazione del gestore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-299">Uninstall must not delete files other than the ones associated with the property handler installation.</span></span>
-   <span data-ttu-id="bb5f9-300">Le chiavi del registro di sistema associate al gestore proprietà devono essere rimosse quando viene disinstallato.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-300">Registry keys associated with the property handler must be removed when uninstalled.</span></span>
-   <span data-ttu-id="bb5f9-301">La disinstallazione deve funzionare anche se i file vengono eliminati dalla directory di installazione.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-301">Uninstall must work even if files are deleted from the installation directory.</span></span>

### <a name="troubleshooting-property-handlers"></a><span data-ttu-id="bb5f9-302">Risoluzione dei problemi relativi ai gestori di proprietà</span><span class="sxs-lookup"><span data-stu-id="bb5f9-302">Troubleshooting Property Handlers</span></span>

<span data-ttu-id="bb5f9-303">Di seguito sono riportati alcuni errori comuni eseguiti durante lo sviluppo dei gestori delle proprietà:</span><span class="sxs-lookup"><span data-stu-id="bb5f9-303">The following are some common errors made while developing property handlers:</span></span>

-   <span data-ttu-id="bb5f9-304">Installazione di file con estensione propdesc o dll in una directory utente.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-304">Installing .propdesc files or DLLs under a user directory.</span></span>
-   <span data-ttu-id="bb5f9-305">Registrazione dei componenti mediante percorsi relativi.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-305">Registering components using relative paths.</span></span>
-   <span data-ttu-id="bb5f9-306">Registrazione dei componenti in HKEY \_ Current \_ User anziché HKEY \_ Local \_ computer.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-306">Registering components under HKEY\_CURRENT\_USER instead of HKEY\_LOCAL\_MACHINE.</span></span>
-   <span data-ttu-id="bb5f9-307">Si dimentica di impostare DisableProcessIsolation per i gestori non di flusso.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-307">Forgetting to set DisableProcessIsolation for non-stream handlers.</span></span>
-   <span data-ttu-id="bb5f9-308">Posizionamento del file di test in una posizione non indicizzata.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-308">Placing the test file in an unindexed location.</span></span>

<span data-ttu-id="bb5f9-309">Se si verificano problemi durante l'utilizzo dell'indicizzatore da parte del gestore delle proprietà, di seguito sono riportati alcuni suggerimenti utili per risolvere i problemi:</span><span class="sxs-lookup"><span data-stu-id="bb5f9-309">If you're having trouble getting your property handler working with the indexer, here are some tips to help you troubleshoot:</span></span>

-   <span data-ttu-id="bb5f9-310">Verificare che le descrizioni delle proprietà (file con estensione propdesc) siano contrassegnate come colonna = "**true**", visualizzabile = "**true**" e Queryable = "**true**" nel modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-310">Verify that your property descriptions (.propdesc files) are marked isColumn="**true**", isViewable="**true**", and isQueryable="**true**" as appropriate.</span></span>
-   <span data-ttu-id="bb5f9-311">Verificare che i file con estensione propdesc si trovino in un percorso globale.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-311">Verify that your .propdesc files are in a global location.</span></span>
-   <span data-ttu-id="bb5f9-312">Verificare che i file con estensione propdesc siano stati registrati usando percorsi assoluti.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-312">Verify that you registered your .propdesc files using absolute paths.</span></span>
-   <span data-ttu-id="bb5f9-313">Verificare che nel registro eventi non siano stati registrati errori durante la registrazione del file con estensione propdesc.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-313">Verify that the event log did not record any failures from registering your .propdesc file.</span></span>
-   <span data-ttu-id="bb5f9-314">Verificare che le dll si trovino in un percorso globale (e non nel profilo utente).</span><span class="sxs-lookup"><span data-stu-id="bb5f9-314">Verify that your DLLs is in a global location (and not under your user profile).</span></span>
-   <span data-ttu-id="bb5f9-315">Verificare che le dll siano registrate in HKEY \_ Local \_ Machine \\ software \\ Classes.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-315">Verify that your DLLs is registered under HKEY\_LOCAL\_MACHINE\\Software\\Classes.</span></span>
-   <span data-ttu-id="bb5f9-316">Verificare che le dll siano registrate usando percorsi completi (o le \_ stringhe reg Expand \_ SZ che si espandono in percorsi assoluti usando le variabili di ambiente note dall'account di sistema).</span><span class="sxs-lookup"><span data-stu-id="bb5f9-316">Verify that your DLLs is registered using full paths (or REG\_EXPAND\_SZ strings that expand to absolute paths using environment variables known by the System account).</span></span>
-   <span data-ttu-id="bb5f9-317">Verificare che il gestore delle proprietà funzioni in Esplora risorse.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-317">Verify that your property handler works under Windows Explorer.</span></span>
-   <span data-ttu-id="bb5f9-318">Sebbene sia consigliabile usare IInitializeWithStream, se è necessario usare IInitializeWithFile o IInitializeWithItem, verificare di specificare DisableProcessIsolation.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-318">While we recommend using IInitializeWithStream, if you must use IInitializeWithFile or IInitializeWithItem, verify that you specify DisableProcessIsolation.</span></span>
-   <span data-ttu-id="bb5f9-319">Verificare che il pannello di controllo opzioni di indicizzazione elenchi il tipo di file come tipo di file indicizzato.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-319">Verify that the Indexing Options Control Panel lists your file type as an indexed file type.</span></span>
-   <span data-ttu-id="bb5f9-320">Verificare che il file di test si trovi in una posizione indicizzata.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-320">Verify that the test file is in an indexed location.</span></span>
-   <span data-ttu-id="bb5f9-321">Verificare che il file di test sia stato modificato dopo l'installazione del gestore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-321">Verify that the test file has been modified since you installed your property handler.</span></span>

<span data-ttu-id="bb5f9-322">Se il file di test si trova in una posizione indicizzata e l'indicizzatore ha già sottoposto a ricerca per indicizzazione, è necessario modificare il file in qualche modo per attivare una reindicizzazione del file.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-322">If your test file is in an indexed location and the indexer has already crawled that location, you need to modify the file in some way in order to trigger a reindexing of the file.</span></span>

 

## <a name="using-system-supplied-property-handlers"></a><span data-ttu-id="bb5f9-323">Utilizzo di System-Supplied gestori di proprietà</span><span class="sxs-lookup"><span data-stu-id="bb5f9-323">Using System-Supplied Property Handlers</span></span>

<span data-ttu-id="bb5f9-324">Windows include diversi gestori di proprietà forniti dal sistema che è possibile usare se il formato del tipo di file è compatibile.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-324">Windows includes a number of system-supplied property handlers that you can use if the format of your file type is compatible.</span></span> <span data-ttu-id="bb5f9-325">Se si definisce una nuova estensione di file che usa uno di questi formati, è possibile usare i gestori forniti dal sistema registrando l'identificatore di classe del gestore (CLSID) per l'estensione di file.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-325">If you define a new file extension that uses one of these formats you can use the system-provided handlers by registering the handler class identifier (CLSID) for your file extension.</span></span>

<span data-ttu-id="bb5f9-326">È possibile utilizzare il CLSID elencato nella tabella seguente per registrare i gestori di proprietà forniti dal sistema per il tipo di formato di file.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-326">You can use the CLSID listed in the following table to register the system-supplied property handlers for your file format type.</span></span>



| <span data-ttu-id="bb5f9-327">Formato</span><span class="sxs-lookup"><span data-stu-id="bb5f9-327">Format</span></span>          | <span data-ttu-id="bb5f9-328">CLSID</span><span class="sxs-lookup"><span data-stu-id="bb5f9-328">CLSID</span></span>                                  |
|-----------------|----------------------------------------|
| <span data-ttu-id="bb5f9-329">DocFile OLE</span><span class="sxs-lookup"><span data-stu-id="bb5f9-329">OLE DocFile</span></span>     | <span data-ttu-id="bb5f9-330">{8d80504a-0826-40c5-97e1-ebc68f953792}</span><span class="sxs-lookup"><span data-stu-id="bb5f9-330">{8d80504a-0826-40c5-97e1-ebc68f953792}</span></span> |
| <span data-ttu-id="bb5f9-331">Salva XML del gioco</span><span class="sxs-lookup"><span data-stu-id="bb5f9-331">Save Game XML</span></span>   | <span data-ttu-id="bb5f9-332">{ECDD6472-2B9B-4b4b-AE36-F316DF3C8D60}</span><span class="sxs-lookup"><span data-stu-id="bb5f9-332">{ECDD6472-2B9B-4b4b-AE36-F316DF3C8D60}</span></span> |
| <span data-ttu-id="bb5f9-333">Gestore XPS/OPC</span><span class="sxs-lookup"><span data-stu-id="bb5f9-333">XPS/OPC handler</span></span> | <span data-ttu-id="bb5f9-334">{45670FA8-ED97-4F44-BC93-305082590BFB}</span><span class="sxs-lookup"><span data-stu-id="bb5f9-334">{45670FA8-ED97-4F44-BC93-305082590BFB}</span></span> |
| <span data-ttu-id="bb5f9-335">XML</span><span class="sxs-lookup"><span data-stu-id="bb5f9-335">XML</span></span>             | <span data-ttu-id="bb5f9-336">{c73f6f30-97a0-4ad1-a08f-540d4e9bc7b9}</span><span class="sxs-lookup"><span data-stu-id="bb5f9-336">{c73f6f30-97a0-4ad1-a08f-540d4e9bc7b9}</span></span> |



 

<span data-ttu-id="bb5f9-337">Prima di creare una proprietà personalizzata, è necessario assicurarsi che non esista una proprietà definita dal sistema che è invece possibile usare.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-337">Before creating a custom property, you should be sure there isn't a system-defined property you can use instead.</span></span> <span data-ttu-id="bb5f9-338">È possibile enumerare le proprietà definite dal sistema chiamando [**PSEnumeratePropertyDescriptions**](/windows/win32/api/propsys/nf-propsys-psenumeratepropertydescriptions) o utilizzando lo strumento da riga di comando prop.exe.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-338">You can enumerate the system-defined properties by calling [**PSEnumeratePropertyDescriptions**](/windows/win32/api/propsys/nf-propsys-psenumeratepropertydescriptions) or using the prop.exe command line tool.</span></span>

<span data-ttu-id="bb5f9-339">Lo schema del sistema definisce il modo in cui queste proprietà interagiscono con l'indicizzatore e non è possibile modificarlo.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-339">The system schema defines how these properties interact with the indexer, and you cannot change that.</span></span> <span data-ttu-id="bb5f9-340">Inoltre, l'applicazione utilizzata per creare, modificare e salvare il tipo di file deve essere conforme anche a un determinato comportamento.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-340">Furthermore, the application you use to create, edit and save your file type needs to conform to certain behavior as well.</span></span> <span data-ttu-id="bb5f9-341">Se, ad esempio, l'applicazione implementa il salvataggio sicuro (in base al quale viene creato un file temporaneo durante la modifica e quindi ReplaceFile () viene usato per scambiare la nuova versione per il vecchio), deve trasferire tutte le proprietà dal file originale al nuovo file.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-341">For example, if the application implements safe save (whereby a temporary file is created during editing, and then ReplaceFile() is used to swap the new version for the old), it must transfer all of the properties from the original file to the new file.</span></span> <span data-ttu-id="bb5f9-342">In caso contrario, il file perde le proprietà aggiunte dagli utenti o da altre applicazioni.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-342">Failure to do means the file loses properties added by users or other applications.</span></span>

 

<span data-ttu-id="bb5f9-343">**Esempio**</span><span class="sxs-lookup"><span data-stu-id="bb5f9-343">**Example**</span></span>

<span data-ttu-id="bb5f9-344">Di seguito viene illustrata la registrazione del gestore DocFile OLE fornito dal sistema per un tipo di file con un oggetto. Estensione OLEDocFile.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-344">The following shows the registration of the system-supplied OLE DocFile handler for a file type with a .OLEDocFile extension.</span></span>

```
HKEY_CLASSES_ROOT
   SystemFileAssociations
      .OLEDocFile
         shellex
            {BB2E617C-0920-11d1-9A0B-00C04FC2D6C1}
               (Default) = {9DBD2C50-62AD-11d0-B806-00C04FD706EC}
```

<span data-ttu-id="bb5f9-345">Di seguito viene illustrata la registrazione delle informazioni sull'elenco di proprietà in modo che le proprietà di. I file OLEDocFile vengono visualizzati nel riquadro e nella scheda Dettagli.</span><span class="sxs-lookup"><span data-stu-id="bb5f9-345">The following shows the registration of the property list information so properties of .OLEDocFile files are displayed on the Details tab and pane.</span></span>

```
HKEY_CLASSES_ROOT
   SystemFileAssociations
      .OLEDocFile
         ExtendedTileInfo = prop:System.ItemType;System.Size;System.DateModified;System.Author;System.OfflineAvailability
         FullDetails = prop:System.PropGroup.Description;System.Title;System.Subject;
System.Keywords;System.Category;System.Comment;System.PropGroup.Origin;
System.Author;System.Document.LastAuthor;System.Document.RevisionNumber;
System.Document.Version;System.ApplicationName;System.Company;System.Document.Manager;
System.Document.DateCreated;System.Document.DateSaved;System.Document.DatePrinted;
System.Document.TotalEditingTime;System.PropGroup.Content;System.ContentStatus;
System.ContentType;System.Document.PageCount;System.Document.WordCount;
System.Document.CharacterCount;System.Document.LineCount;
System.Document.ParagraphCount;System.Document.Template;System.Document.Scale;
System.Document.LinksDirty;System.Language;System.PropGroup.FileSystem;
System.ItemNameDisplay;System.ItemType;System.ItemFolderPathDisplay;
System.DateCreated;System.DateModified;System.Size;System.FileAttributes;
System.OfflineAvailability;System.OfflineStatus;System.SharedWith;
System.FileOwner;System.ComputerName
         InfoTip = prop:System.ItemType;System.Size;System.DateModified;System.Document.PageCoun
         PerceivedType = document
         PreviewDetails = prop:*System.DateModified;System.Author;System.Keywords;
*System.Size;System.Title;System.Comment;System.Category;
*System.Document.PageCount;System.ContentStatus;System.ContentType;
*System.OfflineAvailability;*System.OfflineStatus;System.Subject;
*System.DateCreated;*System.SharedWith
```

 

## <a name="related-topics"></a><span data-ttu-id="bb5f9-346">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bb5f9-346">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="bb5f9-347">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="bb5f9-347">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="bb5f9-348">Mapping delle proprietà</span><span class="sxs-lookup"><span data-stu-id="bb5f9-348">Property Mappings</span></span>](-search-3x-wds-propertymappings.md)
</dt> <dt>

<span data-ttu-id="bb5f9-349">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="bb5f9-349">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="bb5f9-350">Procedure consigliate per la creazione di gestori di filtro in Windows Search</span><span class="sxs-lookup"><span data-stu-id="bb5f9-350">Best Practices for Creating Filter Handlers in Windows Search</span></span>](-search-3x-wds-extidx-filters.md)
</dt> <dt>

[<span data-ttu-id="bb5f9-351">Processo di indicizzazione</span><span class="sxs-lookup"><span data-stu-id="bb5f9-351">The Indexing Process</span></span>](-search-indexing-process-overview.md)
</dt> <dt>

[<span data-ttu-id="bb5f9-352">Sviluppo di gestori di protocollo</span><span class="sxs-lookup"><span data-stu-id="bb5f9-352">Developing Protocol Handlers</span></span>](-search-3x-wds-phaddins.md)
</dt> <dt>

[<span data-ttu-id="bb5f9-353">Proprietà definite dal sistema per formati di file personalizzati</span><span class="sxs-lookup"><span data-stu-id="bb5f9-353">System-Defined Properties for Custom File Formats</span></span>](-shell-systemdefinedpropertiesforfileformats.md)
</dt> <dt>

<span data-ttu-id="bb5f9-354">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="bb5f9-354">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="bb5f9-355">Sistema di proprietà</span><span class="sxs-lookup"><span data-stu-id="bb5f9-355">Property System</span></span>](../properties/building-property-handlers.md)
</dt> <dt>

<span data-ttu-id="bb5f9-356">[Proprietà di sistema](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="bb5f9-356">[System Properties](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)</span></span>
</dt> <dt>

[<span data-ttu-id="bb5f9-357">Esempi di Windows Search SDK</span><span class="sxs-lookup"><span data-stu-id="bb5f9-357">Windows Search SDK Samples</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8)
</dt> </dl>

 

 
