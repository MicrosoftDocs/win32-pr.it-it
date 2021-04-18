---
description: La sintassi di query avanzata (AQS) è la sintassi di query predefinita utilizzata da Windows Search per eseguire una query sull'indice e per perfezionare e restringere i parametri di ricerca.
ms.assetid: 76e33903-d063-48c0-9afe-912c3daa8237
title: Uso della sintassi avanzata delle query a livello di codice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc8fa69a5a5ccaa37b84a10abd367e5a29656455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306194"
---
# <a name="using-advanced-query-syntax-programmatically"></a><span data-ttu-id="66001-103">Uso della sintassi avanzata delle query a livello di codice</span><span class="sxs-lookup"><span data-stu-id="66001-103">Using Advanced Query Syntax Programmatically</span></span>

<span data-ttu-id="66001-104">La sintassi di query avanzata (AQS) è la sintassi di query predefinita utilizzata da Windows Search per eseguire una query sull'indice e per perfezionare e restringere i parametri di ricerca.</span><span class="sxs-lookup"><span data-stu-id="66001-104">Advanced Query Syntax (AQS) is the default query syntax used by Windows Search to query the index and to refine and narrow search parameters.</span></span> <span data-ttu-id="66001-105">AQS viene usato dagli sviluppatori per compilare query a livello di codice (e dagli utenti per restringere i parametri di ricerca).</span><span class="sxs-lookup"><span data-stu-id="66001-105">AQS is employed by developers to build queries programmatically (and by users to narrow their search parameters).</span></span> <span data-ttu-id="66001-106">AQS canonico è stato introdotto in Windows 7 e deve essere usato in Windows 7 e versioni successive per generare query AQS a livello di codice.</span><span class="sxs-lookup"><span data-stu-id="66001-106">Canonical AQS was introduced in Windows 7 and must be used in Windows 7 and later to programmatically generate AQS queries.</span></span>

<span data-ttu-id="66001-107">Questo argomento è organizzato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="66001-107">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="66001-108">Informazioni sulla sintassi avanzata delle query</span><span class="sxs-lookup"><span data-stu-id="66001-108">About Advanced Query Syntax</span></span>](#about-advanced-query-syntax)
    -   [<span data-ttu-id="66001-109">esempi</span><span class="sxs-lookup"><span data-stu-id="66001-109">Examples</span></span>](#examples)
    -   [<span data-ttu-id="66001-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="66001-110">Properties</span></span>](#properties)
-   [<span data-ttu-id="66001-111">Utilizzo delle parole chiave nelle lingue locali</span><span class="sxs-lookup"><span data-stu-id="66001-111">Keyword Use in Local Languages</span></span>](#keyword-use-in-local-languages)
-   [<span data-ttu-id="66001-112">Sintassi avanzata delle query canoniche in Windows 7</span><span class="sxs-lookup"><span data-stu-id="66001-112">Canonical Advanced Query Syntax in Windows 7</span></span>](#canonical-advanced-query-syntax-in-windows-7)
    -   [<span data-ttu-id="66001-113">esempi</span><span class="sxs-lookup"><span data-stu-id="66001-113">Examples</span></span>](#examples)
    -   [<span data-ttu-id="66001-114">Operatori di query</span><span class="sxs-lookup"><span data-stu-id="66001-114">Query Operators</span></span>](#query-operators)
    -   [<span data-ttu-id="66001-115">Valori di query</span><span class="sxs-lookup"><span data-stu-id="66001-115">Query Values</span></span>](#query-values)
-   [<span data-ttu-id="66001-116">Limitazioni dell'ambito</span><span class="sxs-lookup"><span data-stu-id="66001-116">Scope Restrictions</span></span>](#scope-restrictions)
-   [<span data-ttu-id="66001-117">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="66001-117">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="66001-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="66001-118">Related topics</span></span>](#related-topics)

## <a name="about-advanced-query-syntax"></a><span data-ttu-id="66001-119">Informazioni sulla sintassi avanzata delle query</span><span class="sxs-lookup"><span data-stu-id="66001-119">About Advanced Query Syntax</span></span>

<span data-ttu-id="66001-120">Una query è costituita da query di base connesse con AND, OR e NOT, come illustrato nella sintassi di esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="66001-120">A query consists of basic queries connected with AND, OR, and NOT, as shown in the following example syntax:</span></span>

``` syntax
<query> ::=
     <basic query>
| ( <query> )
| <query> AND <query>  
| <query> <query>    // Same as <query> AND <query>
| <query> OR <query> 
| NOT <query>
```

> [!Note]  
> <span data-ttu-id="66001-121">AQS non fa distinzione tra maiuscole e minuscole, ad eccezione di AND, OR e NOT, che deve essere in lettere maiuscole.</span><span class="sxs-lookup"><span data-stu-id="66001-121">AQS is not case sensitive, with the exception of AND, OR, and NOT, which must be in all uppercase.</span></span>

 

<span data-ttu-id="66001-122">Se una query ha due o più utilizzi di AND o OR, verranno associati da sinistra a destra, indipendentemente dal fatto che sia e o o.</span><span class="sxs-lookup"><span data-stu-id="66001-122">If a query has two or more uses of AND or OR, they will bind from left to right, regardless of whether it is AND or OR.</span></span> <span data-ttu-id="66001-123">Ovvero, la query "Apple, pera o prugna" verrà interpretata come se fosse scritta come "(Apple e pera) o prugna" e la query "Apple, pera e Plum" verrà interpretata come se fosse scritta come "(Apple o pera) e Plum".</span><span class="sxs-lookup"><span data-stu-id="66001-123">That is, the query, "apple AND pear OR plum" will be interpreted as if it were written as "(apple AND pear) OR plum", and the query, "apple OR pear AND plum", will be interpreted as if it were written as "(apple OR pear) AND plum".</span></span> <span data-ttu-id="66001-124">Quindi, se un documento contiene la parola prugna ma né Apple, né Pear, la prima query lo restituirà ma la seconda query non verrà eseguita.</span><span class="sxs-lookup"><span data-stu-id="66001-124">So if a document contains the word plum but neither apple, nor pear, the first query will return it but the second query will not.</span></span> <span data-ttu-id="66001-125">È quindi consigliabile usare le parentesi esplicite per qualsiasi query che mescoli AND e OR per evitare errori o interpretazioni errate.</span><span class="sxs-lookup"><span data-stu-id="66001-125">Hence, we recommend that you use explicit parentheses for any query that mixes AND and OR to avoid mistakes or misinterpretations.</span></span>

<span data-ttu-id="66001-126">Una query di base cerca gli elementi che soddisfano una restrizione su una proprietà.</span><span class="sxs-lookup"><span data-stu-id="66001-126">A basic query searches for items that satisfy a restriction over a property.</span></span> <span data-ttu-id="66001-127">L'unica parte obbligatoria di una query di base è la restrizione o il valore di ricerca.</span><span class="sxs-lookup"><span data-stu-id="66001-127">The only required portion of a basic query is the restriction or search value.</span></span> <span data-ttu-id="66001-128">Se non si specifica una proprietà, la ricerca di Windows Cerca tutte le proprietà.</span><span class="sxs-lookup"><span data-stu-id="66001-128">If you do not specify a property, Windows Search searches all properties.</span></span> <span data-ttu-id="66001-129"><restr> rappresenta la restrizione di ricerca.</span><span class="sxs-lookup"><span data-stu-id="66001-129"><restr> represents the search restriction.</span></span>

<span data-ttu-id="66001-130">I seguenti formati per una query di base sono validi:</span><span class="sxs-lookup"><span data-stu-id="66001-130">The following forms for a basic query are valid:</span></span>

``` syntax
<basic query> ::=
     <prop>:<basic restr>
| <restr>
```

<span data-ttu-id="66001-131">Una proprietà viene designata da una parola chiave, ad esempio Author o size, oppure da un nome di proprietà canonico, ad esempio [System. DateModified](../properties/props-system-datemodified.md).</span><span class="sxs-lookup"><span data-stu-id="66001-131">A property is designated by a keyword such as author or size, or by a canonical property name such as [System.DateModified](../properties/props-system-datemodified.md).</span></span> <span data-ttu-id="66001-132">I moduli validi per una proprietà sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="66001-132">Valid forms for a property are as follows:</span></span>

``` syntax
<prop> ::= 
     <canonical property name>
| <property label in UI language>
```

<span data-ttu-id="66001-133">Un operatore indica un'operazione come < o =.</span><span class="sxs-lookup"><span data-stu-id="66001-133">An operator indicates an operation such as < or =.</span></span> <span data-ttu-id="66001-134">Per un elenco degli operatori validi, vedere la sezione operatori di query più avanti in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="66001-134">For a list of valid operators, see the Query Operators section later in this topic.</span></span>

<span data-ttu-id="66001-135">Una restrizione di base è una restrizione semplice su una proprietà che può essere scritta senza parentesi:</span><span class="sxs-lookup"><span data-stu-id="66001-135">A basic restriction is a simple restriction on a property that can be written without parentheses:</span></span>

``` syntax
<basic restr> ::=
     <value>
| <op><value>
| NOT <basic restr>
| ( <restr> )
```

<span data-ttu-id="66001-136">Una restrizione è un valore di ricerca, ad esempio un valore numerico o un valore stringa, facoltativamente con un operatore.</span><span class="sxs-lookup"><span data-stu-id="66001-136">A restriction is a search value such as a number value or string value, optionally with an operator.</span></span> <span data-ttu-id="66001-137">I moduli validi per una restrizione sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="66001-137">Valid forms for a restriction are as follows:</span></span>

``` syntax
<restr> ::=
    <basic restr>
| <restr> AND <restr>
| <restr> <restr>      // Same as <restr> AND <restr>
| <restr> OR <restr>
```

<span data-ttu-id="66001-138">Se non si specifica un operatore, Windows Search sceglie l'operatore più appropriato per la query:</span><span class="sxs-lookup"><span data-stu-id="66001-138">If you do not specify an operator, Windows Search chooses the most appropriate operator for your query:</span></span>

-   <span data-ttu-id="66001-139">Per una proprietà di stringa, \_ \_ viene utilizzato l'operatore di Word STARTSWITH $<.</span><span class="sxs-lookup"><span data-stu-id="66001-139">For a string property, the COP\_WORD\_STARTSWITH $< operator is assumed.</span></span>
-   <span data-ttu-id="66001-140">Per tutte le altre proprietà, \_ viene utilizzato l'operatore COP EQUAL =.</span><span class="sxs-lookup"><span data-stu-id="66001-140">For all other properties, the COP\_EQUAL = operator is assumed.</span></span>

<span data-ttu-id="66001-141">Per l'uso a livello di codice di AQS, è consigliabile avere sempre un operatore esplicito.</span><span class="sxs-lookup"><span data-stu-id="66001-141">For the programmatic use of AQS, we recommend that you always have an explicit operator.</span></span> <span data-ttu-id="66001-142">Il formato valido per la ricerca di un valore semplice o di un intervallo di valori è il seguente:</span><span class="sxs-lookup"><span data-stu-id="66001-142">The valid form for searching a simple value or value range is as follows:</span></span>

``` syntax
<value> ::=
    <simplevalue>
| <simplevalue> .. <simplevalue>
```

<span data-ttu-id="66001-143">Un valore semplice può essere costituito da uno dei tipi seguenti:</span><span class="sxs-lookup"><span data-stu-id="66001-143">A simple value can consist of any of the following types:</span></span>

``` syntax
<simplevalue> ::=
  []         // No value, or a null value
| <word>     // A sequence of characters without whitespace
| <number>   // An integer or a floating point number
| <datetime> // A relative date, or an absolute date and/or time
| <Boolean>
| "..."      // A phrase
| <enumeration range>
```

### <a name="examples"></a><span data-ttu-id="66001-144">Esempio</span><span class="sxs-lookup"><span data-stu-id="66001-144">Examples</span></span>

<span data-ttu-id="66001-145">Una query che cerca un documento che contiene la fase "ultimo trimestre", creata da Theresa o Lee, e che è stata salvata nella cartella documenti, combina tre query di base come segue:</span><span class="sxs-lookup"><span data-stu-id="66001-145">A query that searches for a document containing the phase "last quarter," authored by Theresa or Lee, and that was saved to the folder MyDocs, combines three basic queries as follows:</span></span>

``` syntax
"last quarter" author:(theresa OR lee) folder:MyDocs
```

<span data-ttu-id="66001-146">Le tre query di base sono:</span><span class="sxs-lookup"><span data-stu-id="66001-146">The three basic queries are:</span></span>

-   <span data-ttu-id="66001-147">"ultimo trimestre"</span><span class="sxs-lookup"><span data-stu-id="66001-147">"last quarter"</span></span>
-   <span data-ttu-id="66001-148">autore: (Theresa o Lee)</span><span class="sxs-lookup"><span data-stu-id="66001-148">author:(theresa OR lee)</span></span>
-   <span data-ttu-id="66001-149">cartella: docs</span><span class="sxs-lookup"><span data-stu-id="66001-149">folder:MyDocs</span></span>

<span data-ttu-id="66001-150">Una query di base che usa la sintassi canonica è:</span><span class="sxs-lookup"><span data-stu-id="66001-150">A basic query that uses canonical syntax is:</span></span>

``` syntax
System.Size:>1kb
```

### <a name="properties"></a><span data-ttu-id="66001-151">Proprietà</span><span class="sxs-lookup"><span data-stu-id="66001-151">Properties</span></span>

<span data-ttu-id="66001-152">Le proprietà sono definite da una parola chiave, che può essere un nome di proprietà canonico in Windows 7 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="66001-152">Properties are referred to by a keyword, which can be a canonical property name in Windows 7 and later.</span></span> <span data-ttu-id="66001-153">AQS nell'interfaccia utente di Windows può usare l'etichetta anziché il nome della proprietà canonica, ad esempio Author anziché [System. Author](../properties/props-system-author.md).</span><span class="sxs-lookup"><span data-stu-id="66001-153">AQS in the Windows UI can use the label instead of the canonical property name, such as author instead of [System.Author](../properties/props-system-author.md).</span></span> <span data-ttu-id="66001-154">In Windows Vista e versioni precedenti era possibile usare le etichette inglesi indipendentemente dalla lingua dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="66001-154">In Windows Vista and earlier it was possible to use English labels regardless of the UI language.</span></span> <span data-ttu-id="66001-155">In Windows 7 e versioni successive, Windows Search riconosce le parole chiave solo nella lingua predefinita dell'interfaccia utente corrente.</span><span class="sxs-lookup"><span data-stu-id="66001-155">In Windows 7 and later, Windows Search recognizes keywords in the current default UI language only.</span></span>

### <a name="support-for-custom-properties"></a><span data-ttu-id="66001-156">Supporto per proprietà personalizzate</span><span class="sxs-lookup"><span data-stu-id="66001-156">Support for Custom Properties</span></span>

<span data-ttu-id="66001-157">In Windows Vista e versioni precedenti, le proprietà personalizzate non erano disponibili in AQS.</span><span class="sxs-lookup"><span data-stu-id="66001-157">In Windows Vista and earlier, custom properties were not available in AQS.</span></span> <span data-ttu-id="66001-158">In Windows 7 e versioni successive, AQS funziona con proprietà personalizzate registrate con il sistema di proprietà.</span><span class="sxs-lookup"><span data-stu-id="66001-158">In Windows 7 and later, AQS works with custom properties that are registered with the property system.</span></span> <span data-ttu-id="66001-159">Per ulteriori informazioni sulla creazione di proprietà personalizzate, vedere [System Property](../properties/building-property-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="66001-159">For more information on creating custom properties, see [Property System](../properties/building-property-handlers.md).</span></span>

### <a name="datetime-properties-in-windows-8"></a><span data-ttu-id="66001-160">Proprietà DateTime in Windows 8</span><span class="sxs-lookup"><span data-stu-id="66001-160">DateTime properties in Windows 8</span></span>

<span data-ttu-id="66001-161">A partire da Windows 8, le proprietà DateTime (ad esempio [System. DateModified](../properties/props-system-datemodified.md)) supportano il formato di data e ora canonico specificato da [ISO-8601](https://www.w3.org/TR/NOTE-datetime), includendo facoltativamente il fuso orario UTC.</span><span class="sxs-lookup"><span data-stu-id="66001-161">As of Windows 8, DateTime properties (like [System.DateModified](../properties/props-system-datemodified.md)) support the canonical date and time format specified by [ISO-8601](https://www.w3.org/TR/NOTE-datetime), optionally including the UTC time zone.</span></span>

-   <span data-ttu-id="66001-162">**Windows 8 e versioni precedenti, data e ora senza fuso orario UTC:** *aaaa* - *mm* - *GGThh*:*mm*:*SS*</span><span class="sxs-lookup"><span data-stu-id="66001-162">**Windows 8 and earlier, date-time without UTC time zone:** *YYYY*-*MM*-*DDThh*:*mm*:*ss*</span></span>

    <span data-ttu-id="66001-163">Questo formato specifica un'ora locale, indipendentemente dall'utente o dalle impostazioni locali del sistema.</span><span class="sxs-lookup"><span data-stu-id="66001-163">This format specifies a local time, regardless of the user or system locale.</span></span>

-   <span data-ttu-id="66001-164">**Windows 8, data/ora con fuso orario UTC:** *aaaa* - *mm* - *GGThh*:*mm*:*ssTZD*</span><span class="sxs-lookup"><span data-stu-id="66001-164">**Windows 8, date-time with UTC time zone:** *YYYY*-*MM*-*DDThh*:*mm*:*ssTZD*</span></span>

    <span data-ttu-id="66001-165">Questo formato specifica un'ora al fuso orario UTC specificato.</span><span class="sxs-lookup"><span data-stu-id="66001-165">This format specifies a time at the specified UTC time zone.</span></span>

## <a name="keyword-use-in-local-languages"></a><span data-ttu-id="66001-166">Utilizzo delle parole chiave nelle lingue locali</span><span class="sxs-lookup"><span data-stu-id="66001-166">Keyword Use in Local Languages</span></span>

<span data-ttu-id="66001-167">In Windows 7 e versioni successive, le parole chiave mnemonico funzionano solo nel linguaggio di sistema, ad esempio parole chiave tedesche solo in un sistema operativo tedesco e parole chiave inglesi solo in un sistema operativo in lingua inglese.</span><span class="sxs-lookup"><span data-stu-id="66001-167">In Windows 7 and later, mnemonic keywords work in the system language only, such as German keywords only on a German operating system, and English keywords only on an English operating system.</span></span> <span data-ttu-id="66001-168">[System. Author](../properties/props-system-author.md) è una parola chiave canonica e il valore mnemonico per la proprietà System. Author è, ad esempio, Author.</span><span class="sxs-lookup"><span data-stu-id="66001-168">[System.Author](../properties/props-system-author.md) is a canonical keyword, and the mnemonic value for the System.Author property is Author, for example.</span></span> <span data-ttu-id="66001-169">L'introduzione di parole chiave canoniche compensa il fatto che le parole chiave in lingua inglese non sono più universalmente riconosciute in tutti i sistemi operativi indipendentemente dalla lingua, come nel caso di Windows Vista e versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="66001-169">The introduction of canonical keywords compensates for the fact that English mnemonic keywords are no longer universally recognized on all operating systems regardless of language, as was the case in Windows Vista and earlier.</span></span>

> [!Note]  
> <span data-ttu-id="66001-170">In Windows 7 e versioni successive, Windows Search riconosce solo le parole chiave nella lingua predefinita corrente e non in inglese, a meno che l'inglese non sia l'impostazione predefinita corrente.</span><span class="sxs-lookup"><span data-stu-id="66001-170">In Windows 7 and later, Windows Search recognizes keywords in the current default language only, and not in English unless English is the current default.</span></span> <span data-ttu-id="66001-171">Si consiglia agli sviluppatori di usare sempre la sintassi canonica, in modo che l'applicazione non abbia problemi di lingua con le parole chiave.</span><span class="sxs-lookup"><span data-stu-id="66001-171">We recommend that developers always use canonical syntax so that their application won't have language problems with keywords.</span></span>

 

## <a name="canonical-advanced-query-syntax-in-windows-7"></a><span data-ttu-id="66001-172">Sintassi avanzata delle query canoniche in Windows 7</span><span class="sxs-lookup"><span data-stu-id="66001-172">Canonical Advanced Query Syntax in Windows 7</span></span>

<span data-ttu-id="66001-173">La sintassi canonica è stata introdotta per le parole chiave in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="66001-173">Canonical syntax was introduced for keywords in Windows 7.</span></span> <span data-ttu-id="66001-174">Un esempio di query con una proprietà canonica è `System.Message.FromAddress:=me@microsoft.com` .</span><span class="sxs-lookup"><span data-stu-id="66001-174">An example of a query with a canonical property is `System.Message.FromAddress:=me@microsoft.com`.</span></span> <span data-ttu-id="66001-175">Quando si codificano query in applicazioni in esecuzione in Windows 7 e versioni successive, è necessario usare la sintassi canonica per generare query AQS a livello di codice.</span><span class="sxs-lookup"><span data-stu-id="66001-175">When coding queries in applications running on Windows 7 and later, you must use canonical syntax to programmatically generate AQS queries.</span></span> <span data-ttu-id="66001-176">Se non si usa la sintassi canonica e l'applicazione viene distribuita in una lingua locale o dell'interfaccia utente diversa da quella del codice dell'applicazione, le query non verranno interpretate correttamente.</span><span class="sxs-lookup"><span data-stu-id="66001-176">If you do not use canonical syntax and your application is deployed in a locale or UI language different from the language in the application code, your queries will not be interpreted correctly.</span></span>

<span data-ttu-id="66001-177">Le convenzioni per la sintassi delle parole chiave canoniche sono le seguenti:</span><span class="sxs-lookup"><span data-stu-id="66001-177">The conventions for canonical keyword syntax are as follows:</span></span>

-   <span data-ttu-id="66001-178">La sintassi canonica per una proprietà è il nome canonico, ad esempio `System.Photo.LightSource` .</span><span class="sxs-lookup"><span data-stu-id="66001-178">The canonical syntax for a property is its canonical name, such as `System.Photo.LightSource`.</span></span> <span data-ttu-id="66001-179">I nomi canonico non fanno distinzione tra maiuscole e minuscole</span><span class="sxs-lookup"><span data-stu-id="66001-179">Canonical names are not case sensitive.</span></span>
-   <span data-ttu-id="66001-180">La sintassi canonica per gli operatori booleani è costituita dalle parole chiave AND, OR e NOT, in lettere maiuscole.</span><span class="sxs-lookup"><span data-stu-id="66001-180">The canonical syntax for the Boolean operators consists of the keywords AND, OR, and NOT, in all uppercase.</span></span>
-   <span data-ttu-id="66001-181">Gli operatori <, >, = e così via, non sono localizzati e quindi fanno anche parte della sintassi canonica.</span><span class="sxs-lookup"><span data-stu-id="66001-181">The operators <, >, =, and so forth, are not localized and are thus also part of the canonical syntax.</span></span>
-   <span data-ttu-id="66001-182">Se una proprietà `P` ha enumerato i valori o gli intervalli denominati N ₁ tramite NK, la sintassi canonica per il valore o l'intervallo di *i* TH è il nome canonico per P, seguito dal carattere \# , seguito da N <sub>i</sub>, come illustrato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="66001-182">If a property `P` has enumerated values or ranges named N₁ through Nₖ, the canonical syntax for the *I* th value or range is the canonical name for P, followed by the character \#, followed by N<sub>I</sub>, as illustrated in the following example:</span></span>
    -   <span data-ttu-id="66001-183">`System.Photo.LightSource#Daylight`, `System.Photo.LightSource#StandardA` e così via.</span><span class="sxs-lookup"><span data-stu-id="66001-183">`System.Photo.LightSource#Daylight`, `System.Photo.LightSource#StandardA`, and so forth.</span></span>
-   <span data-ttu-id="66001-184">Per un tipo semantico definito T con valori o intervalli denominati N ₁ tramite NK, la sintassi canonica per il valore o l'intervallo di *i* TH è il nome canonico per T, seguito dal carattere \# , seguito da N <sub>i</sub>, come illustrato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="66001-184">For a defined semantic type T with values or ranges named N₁ through Nₖ, the canonical syntax for the *I* th value or range is the canonical name for T, followed by the character \#, followed by N<sub>I</sub>, as illustrated in the following example:</span></span>
    -   `System.Devices.LaunchDeviceStageFromExplorer:=System.StructuredQueryType.Boolean#True`
-   <span data-ttu-id="66001-185">Per i valori letterali come parole o frasi, la sintassi canonica è identica a quella della normale sintassi.</span><span class="sxs-lookup"><span data-stu-id="66001-185">For literal values such as words or phrases, the canonical syntax is the same as the regular syntax.</span></span> <span data-ttu-id="66001-186">Esempi di query con valori letterali nella sintassi canonica sono:</span><span class="sxs-lookup"><span data-stu-id="66001-186">Examples of queries with literal values in canonical syntax are:</span></span>
    -   `System.Author:sanjay`
    -   `System.Keywords:"Animal"`
    -   `System.FileCount:>100`

> [!Note]  
> <span data-ttu-id="66001-187">Non esiste alcuna sintassi canonica per i numeri in Windows 7 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="66001-187">There is no canonical syntax for numbers in Windows 7 and later.</span></span> <span data-ttu-id="66001-188">Poiché i formati a virgola mobile variano tra le impostazioni locali, l'uso di una query canonica che prevede una costante a virgola mobile non è supportato.</span><span class="sxs-lookup"><span data-stu-id="66001-188">Because floating point formats vary among locales, the use of a canonical query that involves a floating point constant is not supported.</span></span> <span data-ttu-id="66001-189">Le costanti integer possono invece essere scritte usando solo cifre (nessun separatore per migliaia) e possono essere usate in modo sicuro nelle query canoniche in Windows 7 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="66001-189">Integer constants, in contrast, can be written using only digits (no separators for thousands) and can be safely used in canonical queries in Windows 7 and later.</span></span>

 

### <a name="examples"></a><span data-ttu-id="66001-190">Esempio</span><span class="sxs-lookup"><span data-stu-id="66001-190">Examples</span></span>

<span data-ttu-id="66001-191">Nella tabella seguente vengono illustrati alcuni esempi di proprietà canoniche e la sintassi per utilizzarli.</span><span class="sxs-lookup"><span data-stu-id="66001-191">The following table shows some examples of canonical properties and the syntax for using them.</span></span>



| <span data-ttu-id="66001-192">Tipo di proprietà canonica</span><span class="sxs-lookup"><span data-stu-id="66001-192">Type of canonical property</span></span> | <span data-ttu-id="66001-193">Esempio</span><span class="sxs-lookup"><span data-stu-id="66001-193">Example</span></span>                                                                                     | <span data-ttu-id="66001-194">Sintassi</span><span class="sxs-lookup"><span data-stu-id="66001-194">Syntax</span></span>                                                                                                                                                                                                                                                  |
|----------------------------|---------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66001-195">Valore stringa</span><span class="sxs-lookup"><span data-stu-id="66001-195">String value</span></span>               | [<span data-ttu-id="66001-196">System.Author</span><span class="sxs-lookup"><span data-stu-id="66001-196">System.Author</span></span>](../properties/props-system-author.md)<br/>    | <span data-ttu-id="66001-197">Il valore della stringa viene cercato nella proprietà Author:</span><span class="sxs-lookup"><span data-stu-id="66001-197">The string value is searched for in the author property:</span></span> <br/>`System.Author:Jacobs`                                                                                                                                                              |
| <span data-ttu-id="66001-198">Intervallo di enumerazione</span><span class="sxs-lookup"><span data-stu-id="66001-198">Enumeration range</span></span>          | [<span data-ttu-id="66001-199">System. Priority</span><span class="sxs-lookup"><span data-stu-id="66001-199">System.Priority</span></span>](../properties/props-system-priority.md)             | <span data-ttu-id="66001-200">La proprietà Priority può avere un intervallo di valori numerici:</span><span class="sxs-lookup"><span data-stu-id="66001-200">The priority property can have a numerical value range:</span></span><br/>`System.Priority:System.Priority#High`                                                                                                                                                |
| <span data-ttu-id="66001-201">Boolean</span><span class="sxs-lookup"><span data-stu-id="66001-201">Boolean</span></span>                    | [<span data-ttu-id="66001-202">System. undeleted</span><span class="sxs-lookup"><span data-stu-id="66001-202">System.IsDeleted</span></span>](../properties/props-system-isdeleted.md)<br/> | <span data-ttu-id="66001-203">I valori booleani possono essere usati con qualsiasi proprietà booleana:</span><span class="sxs-lookup"><span data-stu-id="66001-203">Boolean values can be used with any Boolean property:</span></span><br/><span data-ttu-id="66001-204">`System.IsDeleted:System.StructuredQueryType.Boolean#True`, e `System.IsDeleted:System.StructuredQueryType.Boolean#False`</span><span class="sxs-lookup"><span data-stu-id="66001-204">`System.IsDeleted:System.StructuredQueryType.Boolean#True`, and `System.IsDeleted:System.StructuredQueryType.Boolean#False`</span></span>                                                             |
| <span data-ttu-id="66001-205">Numerico</span><span class="sxs-lookup"><span data-stu-id="66001-205">Numerical</span></span>                  | [<span data-ttu-id="66001-206">System. size</span><span class="sxs-lookup"><span data-stu-id="66001-206">System.Size</span></span>](../properties/props-system-size.md)<br/>      | <span data-ttu-id="66001-207">Non è possibile scrivere in modo sicuro una query canonica che prevede una costante a virgola mobile, perché i formati a virgola mobile variano tra le impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="66001-207">It is not possible to write safely a canonical query that involves a floating point constant, because floating point formats vary among locales.</span></span> <span data-ttu-id="66001-208">I numeri interi devono essere scritti senza separatori per le migliaia.</span><span class="sxs-lookup"><span data-stu-id="66001-208">Integers must be written with no separators for thousands.</span></span> <span data-ttu-id="66001-209">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="66001-209">For example:</span></span><br/>`System.Size:<12345` |



 

<span data-ttu-id="66001-210">Per ulteriori informazioni sulle proprietà canoniche e sul sistema di proprietà in genere, vedere [proprietà di sistema](../properties/props.md).</span><span class="sxs-lookup"><span data-stu-id="66001-210">For more information about canonical properties and the property system generally, see [System Properties](../properties/props.md).</span></span> <span data-ttu-id="66001-211">In alternativa, fare riferimento ai file di intestazione pubblica.</span><span class="sxs-lookup"><span data-stu-id="66001-211">Alternatively, refer to the public header files.</span></span>

### <a name="query-operators"></a><span data-ttu-id="66001-212">Operatori di query</span><span class="sxs-lookup"><span data-stu-id="66001-212">Query Operators</span></span>

<span data-ttu-id="66001-213">Se una proprietà, p, ha più valori per un elemento, una query AQS per p: <restr> restituisce l'elemento se <restr> è **true** per almeno uno dei valori.</span><span class="sxs-lookup"><span data-stu-id="66001-213">If a property, p, has multiple values for some item, an AQS query for p:<restr> returns the item if <restr> is **true** for at least one of the values.</span></span> <span data-ttu-id="66001-214">( <restr> rappresenta una restrizione).</span><span class="sxs-lookup"><span data-stu-id="66001-214">(<restr> represents a restriction.)</span></span>

<span data-ttu-id="66001-215">La sintassi elencata nella tabella seguente è costituita da un operatore, un simbolo dell'operatore, un esempio e una descrizione di esempio.</span><span class="sxs-lookup"><span data-stu-id="66001-215">The syntax listed in the following table consists of an operator, operator symbol, example and example description.</span></span> <span data-ttu-id="66001-216">L'operatore e il simbolo possono essere utilizzati in qualsiasi linguaggio e inclusi in qualsiasi query.</span><span class="sxs-lookup"><span data-stu-id="66001-216">The operator and symbol can be used in any language and included in any query.</span></span> <span data-ttu-id="66001-217">Non usare gli \_ operatori specifici dell'applicazione COP o COP \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="66001-217">Do not use the COP\_IMPLICIT or COP\_APPLICATION\_SPECIFIC operators.</span></span> <span data-ttu-id="66001-218">Alcuni operatori hanno simboli intercambiabili.</span><span class="sxs-lookup"><span data-stu-id="66001-218">Some of the operators have interchangeable symbols.</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="66001-219">Operatore</span><span class="sxs-lookup"><span data-stu-id="66001-219">Operator</span></span></th>
<th><span data-ttu-id="66001-220">Simbolo</span><span class="sxs-lookup"><span data-stu-id="66001-220">Symbol</span></span></th>
<th><span data-ttu-id="66001-221">Esempio</span><span class="sxs-lookup"><span data-stu-id="66001-221">Example</span></span></th>
<th><span data-ttu-id="66001-222">Descrizione</span><span class="sxs-lookup"><span data-stu-id="66001-222">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="66001-223">COP_EQUAL</span><span class="sxs-lookup"><span data-stu-id="66001-223">COP_EQUAL</span></span></td>
<td>=<br/></td>
<td><span data-ttu-id="66001-224">System. FileExtension: = &quot; . txt&quot;</span><span class="sxs-lookup"><span data-stu-id="66001-224">System.FileExtension:=&quot;.txt&quot;</span></span><br/></td>
<td><span data-ttu-id="66001-225">Il valore è String &quot; <em>. txt</em> &quot; .</span><span class="sxs-lookup"><span data-stu-id="66001-225">The value is the string &quot;<em>.txt</em>&quot;.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66001-226">COP_NOTEQUAL</span><span class="sxs-lookup"><span data-stu-id="66001-226">COP_NOTEQUAL</span></span></td>
<td><span data-ttu-id="66001-227">≠</span><span class="sxs-lookup"><span data-stu-id="66001-227">≠</span></span><br/> -<br/> &lt;&gt;<br/> <span data-ttu-id="66001-228">NOT</span><span class="sxs-lookup"><span data-stu-id="66001-228">NOT</span></span><br/> - -<br/></td>
<td><span data-ttu-id="66001-229">System. Kind: immagine ≠</span><span class="sxs-lookup"><span data-stu-id="66001-229">System.Kind:≠picture</span></span><br/> <span data-ttu-id="66001-230">System. Photo. DateTaken:-[] ¹</span><span class="sxs-lookup"><span data-stu-id="66001-230">System.Photo.DateTaken:-[]¹</span></span><br/> <span data-ttu-id="66001-231">System. Kind: &lt; &gt; immagine</span><span class="sxs-lookup"><span data-stu-id="66001-231">System.Kind:&lt;&gt;picture</span></span><br/> <span data-ttu-id="66001-232">System. Kind: non immagine</span><span class="sxs-lookup"><span data-stu-id="66001-232">System.Kind:NOT picture</span></span><br/> <span data-ttu-id="66001-233">System. Kind:--immagine</span><span class="sxs-lookup"><span data-stu-id="66001-233">System.Kind:- -picture</span></span><br/></td>
<td><span data-ttu-id="66001-234">La proprietà <a href="/windows/desktop/properties/props-system-kind">System. Kind</a> non è un'immagine.</span><span class="sxs-lookup"><span data-stu-id="66001-234">The <a href="/windows/desktop/properties/props-system-kind">System.Kind</a> property is not a picture.</span></span><br/> <span data-ttu-id="66001-235">Il valore della proprietà <a href="/windows/desktop/properties/props-system-photo-datetaken">System. Photo. DateTaken</a> è.</span><span class="sxs-lookup"><span data-stu-id="66001-235">The <a href="/windows/desktop/properties/props-system-photo-datetaken">System.Photo.DateTaken</a> property has a value.</span></span><br/> <span data-ttu-id="66001-236">La proprietà <a href="/windows/desktop/properties/props-system-kind">System. Kind</a> non è un'immagine.</span><span class="sxs-lookup"><span data-stu-id="66001-236">The <a href="/windows/desktop/properties/props-system-kind">System.Kind</a> property is not a picture.</span></span> <br/> <span data-ttu-id="66001-237">La proprietà <a href="/windows/desktop/properties/props-system-kind">System. Kind</a> non è un'immagine.</span><span class="sxs-lookup"><span data-stu-id="66001-237">The <a href="/windows/desktop/properties/props-system-kind">System.Kind</a> property is not a picture.</span></span> <br/> <span data-ttu-id="66001-238">Gli operatori Double non applicati alla stessa proprietà non vengono annullati. System. Kind:--Picture, quindi, è equivalente a System. Kind:-Picture e System. Kind: NOT Picture.</span><span class="sxs-lookup"><span data-stu-id="66001-238">Double NOT operators applied to the same property do not cancel out. Hence, System.Kind:- -picture is equivalent to System.Kind:-picture and System.Kind:NOT picture.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66001-239">COP_LESSTHAN</span><span class="sxs-lookup"><span data-stu-id="66001-239">COP_LESSTHAN</span></span></td>
<td>&lt;<br/></td>
<td><span data-ttu-id="66001-240">System. Size: &lt; 1 KB</span><span class="sxs-lookup"><span data-stu-id="66001-240">System.Size:&lt;1kb</span></span><br/></td>
<td><span data-ttu-id="66001-241">Questo valore è minore di <em>1 KB</em>.</span><span class="sxs-lookup"><span data-stu-id="66001-241">This value is less than <em>1kb</em>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66001-242">COP_GREATERTHAN</span><span class="sxs-lookup"><span data-stu-id="66001-242">COP_GREATERTHAN</span></span></td>
<td>&gt;<br/></td>
<td><span data-ttu-id="66001-243">System. ItemDate: &gt; System. StructuredQueryType. DateTime # today</span><span class="sxs-lookup"><span data-stu-id="66001-243">System.ItemDate:&gt;System.StructuredQueryType.DateTime#Today</span></span><br/></td>
<td><span data-ttu-id="66001-244">Questo valore è maggiore di <em>oggi</em>.</span><span class="sxs-lookup"><span data-stu-id="66001-244">This value is greater than <em>today</em>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66001-245">COP_LESSTHANOREQUAL</span><span class="sxs-lookup"><span data-stu-id="66001-245">COP_LESSTHANOREQUAL</span></span></td>
<td>&lt;=<br/> <span data-ttu-id="66001-246">≤</span><span class="sxs-lookup"><span data-stu-id="66001-246">≤</span></span><br/></td>
<td><span data-ttu-id="66001-247">System. Size: &lt; = 1 KB</span><span class="sxs-lookup"><span data-stu-id="66001-247">System.Size:&lt;=1kb</span></span><br/></td>
<td><span data-ttu-id="66001-248">Questo valore è minore o uguale a <em>1 KB</em>.</span><span class="sxs-lookup"><span data-stu-id="66001-248">This value is less than or equal to <em>1kb</em>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66001-249">COP_GREATERTHANOREQUAL</span><span class="sxs-lookup"><span data-stu-id="66001-249">COP_GREATERTHANOREQUAL</span></span></td>
<td>&gt;=<br/> <span data-ttu-id="66001-250">≥</span><span class="sxs-lookup"><span data-stu-id="66001-250">≥</span></span><br/></td>
<td><span data-ttu-id="66001-251">System. Size: &gt; = 1 KB</span><span class="sxs-lookup"><span data-stu-id="66001-251">System.Size:&gt;=1kb</span></span><br/></td>
<td><span data-ttu-id="66001-252">Questo valore è uguale o maggiore di <em>1 KB</em>.</span><span class="sxs-lookup"><span data-stu-id="66001-252">This value is equal to or greater than <em>1kb</em>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66001-253">COP_VALUE_STARTSWITH</span><span class="sxs-lookup"><span data-stu-id="66001-253">COP_VALUE_STARTSWITH</span></span></td>
<td>~&lt;<br/></td>
<td><span data-ttu-id="66001-254">System. FileName: ~ Nozioni di &lt; &quot; primo in C++&quot;</span><span class="sxs-lookup"><span data-stu-id="66001-254">System.FileName:~&lt;&quot;C++ Primer&quot;</span></span><br/></td>
<td><span data-ttu-id="66001-255">Trova gli elementi in cui il nome del file inizia con i caratteri C++ nozioni di &quot; <em>fondo</em> &quot; .</span><span class="sxs-lookup"><span data-stu-id="66001-255">Finds items where the file name begins with the characters &quot;<em>C++ Primer</em>&quot;.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66001-256">COP_VALUE_ENDSWITH</span><span class="sxs-lookup"><span data-stu-id="66001-256">COP_VALUE_ENDSWITH</span></span></td>
<td>~&gt;<br/></td>
<td><span data-ttu-id="66001-257">System. Photo. CameraModel: ~ &gt; non</span><span class="sxs-lookup"><span data-stu-id="66001-257">System.Photo.CameraModel:~&gt;non</span></span><br/></td>
<td><span data-ttu-id="66001-258">Trova gli elementi in cui il valore della proprietà termina con i caratteri <em>non</em>.</span><span class="sxs-lookup"><span data-stu-id="66001-258">Finds items where the property value ends with the characters <em>non</em>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66001-259">COP_VALUE_CONTAINS</span><span class="sxs-lookup"><span data-stu-id="66001-259">COP_VALUE_CONTAINS</span></span></td>
<td>~=<br/> ~~<br/></td>
<td><span data-ttu-id="66001-260">System. Subject. ~ = Round</span><span class="sxs-lookup"><span data-stu-id="66001-260">System.Subject.~=round</span></span> <br/> <span data-ttu-id="66001-261">System. search. AutoSummary: ~ ~ Round</span><span class="sxs-lookup"><span data-stu-id="66001-261">System.Search.Autosummary:~~round</span></span><br/></td>
<td><span data-ttu-id="66001-262">Trova un messaggio con questa stringa nell'oggetto e corrisponde a &quot; g regole<em>arrotondate</em> , &quot; ad esempio.</span><span class="sxs-lookup"><span data-stu-id="66001-262">Finds a message that has this string in the subject, and will match &quot;g<em>round</em> rules&quot; for example.</span></span><br/> <span data-ttu-id="66001-263">Trova tutti gli elementi con un riepilogo che contiene i caratteri <em>arrotondati</em>.</span><span class="sxs-lookup"><span data-stu-id="66001-263">Finds all items with an Autosummary that contains the characters <em>round</em>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66001-264">COP_VALUE_NOTCONTAINS</span><span class="sxs-lookup"><span data-stu-id="66001-264">COP_VALUE_NOTCONTAINS</span></span></td>
<td><span data-ttu-id="66001-265">~!</span><span class="sxs-lookup"><span data-stu-id="66001-265">~!</span></span><br/></td>
<td><span data-ttu-id="66001-266">System. Author: ~! &quot; Sanjay&quot;</span><span class="sxs-lookup"><span data-stu-id="66001-266">System.Author:~!&quot;sanjay&quot;</span></span><br/></td>
<td><span data-ttu-id="66001-267">Trova gli autori che non hanno la sequenza di caratteri &quot; <em>Sanjay</em> &quot; .</span><span class="sxs-lookup"><span data-stu-id="66001-267">Finds authors that do not have the character sequence&quot;<em>sanjay</em>&quot; in them.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66001-268">COP_DOSWILDCARDS</span><span class="sxs-lookup"><span data-stu-id="66001-268">COP_DOSWILDCARDS</span></span></td>
<td>~ <br/></td>
<td><span data-ttu-id="66001-269">System. FileName: ~ &quot; MIC? osoft W \* d&quot;</span><span class="sxs-lookup"><span data-stu-id="66001-269">System.FileName:~&quot;Mic?osoft W\*d&quot;</span></span><br/></td>
<td><span data-ttu-id="66001-270">Trova i file in cui il nome del file inizia con <em>MIC</em>, seguito da un carattere, seguito da <em>osoft w</em>, seguito da tutti i caratteri che terminano con <em>d</em>.</span><span class="sxs-lookup"><span data-stu-id="66001-270">Finds files where the file name starts with <em>Mic</em>, followed by some character, followed by <em>osoft w</em>, followed by any characters ending with <em>d</em>.</span></span> <br/> <span data-ttu-id="66001-271">Il carattere ?</span><span class="sxs-lookup"><span data-stu-id="66001-271">The ?</span></span> <span data-ttu-id="66001-272">e \* i caratteri non vengono interpretati letteralmente e funzionano come i caratteri jolly di tipo DOS:</span><span class="sxs-lookup"><span data-stu-id="66001-272">and \* characters are not interpreted literally, and work like DOS-style wildcard characters:</span></span><br/>
<ul>
<li><span data-ttu-id="66001-273">?</span><span class="sxs-lookup"><span data-stu-id="66001-273">?</span></span> <span data-ttu-id="66001-274">corrisponde a un carattere arbitrario.</span><span class="sxs-lookup"><span data-stu-id="66001-274">matches one arbitrary character.</span></span></li>
<li><span data-ttu-id="66001-275">\* trova la corrispondenza di zero o più caratteri arbitrari.</span><span class="sxs-lookup"><span data-stu-id="66001-275">\* matches zero or more arbitrary characters.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66001-276">COP_WORD_EQUAL</span><span class="sxs-lookup"><span data-stu-id="66001-276">COP_WORD_EQUAL</span></span></td>
<td>$=<br/> $$<br/></td>
<td><span data-ttu-id="66001-277">System. StructuredQuery. Virtual. from: $ = &quot; Sanjay Jacobs&quot;</span><span class="sxs-lookup"><span data-stu-id="66001-277">System.StructuredQuery.Virtual.From:$=&quot;Sanjay Jacobs&quot;</span></span><br/></td>
<td><span data-ttu-id="66001-278">Per Windows 7 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="66001-278">For Windows 7 and later.</span></span> <span data-ttu-id="66001-279">Trova la frase &quot; <em>Sanjay Jacobs</em> &quot; in tutte le proprietà di.</span><span class="sxs-lookup"><span data-stu-id="66001-279">Finds the phrase &quot;<em>Sanjay Jacobs</em>&quot; in all From properties.</span></span> <span data-ttu-id="66001-280">La parola <em>Sanjay</em> deve essere seguita dalla parola <em>Jacobs</em>.</span><span class="sxs-lookup"><span data-stu-id="66001-280">The word <em>Sanjay</em> must be followed by the word <em>Jacobs</em>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66001-281">COP_WORD_STARTSWITH</span><span class="sxs-lookup"><span data-stu-id="66001-281">COP_WORD_STARTSWITH</span></span></td>
<td>$<<br/></td>
<td><span data-ttu-id="66001-282">System. Author: $</span><span class="sxs-lookup"><span data-stu-id="66001-282">System.Author:$</span></span><&quot;San&quot; System.Filename:$<&quot;Micro Exe&quot;<br/></td>
<td><span data-ttu-id="66001-283">Per Windows 7 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="66001-283">For Windows 7 and later.</span></span> <span data-ttu-id="66001-284">Trova un elemento in cui l'autore contiene una parola che inizia con i caratteri &quot; <em>San</em> &quot; .</span><span class="sxs-lookup"><span data-stu-id="66001-284">Finds any item where Author contains a word starting with the characters &quot;<em>San</em>&quot;.</span></span><br/> <span data-ttu-id="66001-285">Trova tutti i file in cui il nome file contiene una parola che inizia con <em>micro</em>, seguita da una parola che inizia con <em>exe</em>.</span><span class="sxs-lookup"><span data-stu-id="66001-285">Finds any file in which the file name contains a word starting with <em>micro</em>, followed by a word starting with <em>exe</em>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="66001-286">¹ parentesi quadre vuote ( \[ \] ) indica "nessun valore".</span><span class="sxs-lookup"><span data-stu-id="66001-286">¹ Empty square brackets (\[\]) denote "no value".</span></span>

<span data-ttu-id="66001-287">Per le proprietà di stringa l'operazione predefinita è COP \_ Word \_ inizia \_ con o COP \_ Word \_ Equal.</span><span class="sxs-lookup"><span data-stu-id="66001-287">For string properties the default operation is either COP\_WORD\_STARTS\_WITH or COP\_WORD\_EQUAL.</span></span>

### <a name="query-values"></a><span data-ttu-id="66001-288">Valori di query</span><span class="sxs-lookup"><span data-stu-id="66001-288">Query Values</span></span>

<span data-ttu-id="66001-289">Nella tabella seguente sono elencati alcuni esempi utili di come è possibile limitare i valori di query.</span><span class="sxs-lookup"><span data-stu-id="66001-289">Useful examples of how query values can be restricted are listed in the following table.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="66001-290">Valore/simbolo</span><span class="sxs-lookup"><span data-stu-id="66001-290">Value/symbol</span></span></th>
<th><span data-ttu-id="66001-291">Esempi</span><span class="sxs-lookup"><span data-stu-id="66001-291">Examples</span></span></th>
<th><span data-ttu-id="66001-292">Descrizione</span><span class="sxs-lookup"><span data-stu-id="66001-292">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="66001-293">string</span><span class="sxs-lookup"><span data-stu-id="66001-293">String</span></span></td>
<td><span data-ttu-id="66001-294">auto</span><span class="sxs-lookup"><span data-stu-id="66001-294">auto</span></span><br/></td>
<td><span data-ttu-id="66001-295">Qualsiasi sequenza di caratteri in cui è possibile cercare.</span><span class="sxs-lookup"><span data-stu-id="66001-295">Any sequence of characters that can be searched for.</span></span> <span data-ttu-id="66001-296">La stringa non deve contenere spazi vuoti o combinazioni di caratteri che fanno parte della sintassi.</span><span class="sxs-lookup"><span data-stu-id="66001-296">The string must not contain whitespace or character combinations that are part of the syntax.</span></span> <span data-ttu-id="66001-297">Questo esempio cerca una parola che inizia con <em>auto</em>.</span><span class="sxs-lookup"><span data-stu-id="66001-297">This example searches for a word beginning with <em>auto</em>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66001-298">Stringa tra virgolette &quot;&quot;</span><span class="sxs-lookup"><span data-stu-id="66001-298">Quoted string &quot;&quot;</span></span></td>
<td><span data-ttu-id="66001-299">&quot;CONCLUSIONI: valido &quot; &quot; il &quot; &quot; Blue &quot; &quot; Team&quot;</span><span class="sxs-lookup"><span data-stu-id="66001-299">&quot;Conclusions: valid&quot; &quot;The &quot;&quot;blue&quot;&quot; team&quot;</span></span><br/></td>
<td><span data-ttu-id="66001-300">Qualsiasi sequenza di caratteri.</span><span class="sxs-lookup"><span data-stu-id="66001-300">Any sequence of characters.</span></span> <span data-ttu-id="66001-301">La stringa non viene interpretata come parte della sintassi.</span><span class="sxs-lookup"><span data-stu-id="66001-301">The string is not interpreted as part of the syntax.</span></span><br/> <span data-ttu-id="66001-302">Le virgolette possono essere incluse in una query se sono raddoppiate.</span><span class="sxs-lookup"><span data-stu-id="66001-302">Quotation marks can be included in a query if they are doubled.</span></span> <span data-ttu-id="66001-303">In questo esempio viene eseguita <em>la ricerca del &quot; Blue &quot; Team</em>.</span><span class="sxs-lookup"><span data-stu-id="66001-303">This example searches for <em>The &quot;blue&quot; team</em>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66001-304">Integer</span><span class="sxs-lookup"><span data-stu-id="66001-304">Integer</span></span></td>
<td><span data-ttu-id="66001-305">5678</span><span class="sxs-lookup"><span data-stu-id="66001-305">5678</span></span><br/></td>
<td><span data-ttu-id="66001-306">Usare solo cifre per numeri interi.</span><span class="sxs-lookup"><span data-stu-id="66001-306">Use only digits for integers.</span></span> <span data-ttu-id="66001-307">Non usare alcun separatore per le migliaia.</span><span class="sxs-lookup"><span data-stu-id="66001-307">Do not use any separators for thousands.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66001-308">Numero a virgola mobile</span><span class="sxs-lookup"><span data-stu-id="66001-308">Floating point number</span></span></td>
<td><span data-ttu-id="66001-309">5678,1234</span><span class="sxs-lookup"><span data-stu-id="66001-309">5678.1234</span></span><br/></td>
<td><span data-ttu-id="66001-310">Poiché i formati a virgola mobile variano tra le impostazioni locali, una query canonica non può utilizzare una costante a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="66001-310">Because floating point formats vary among locales, a canonical query cannot use a floating point constant.</span></span> <span data-ttu-id="66001-311">L'uso della sintassi canonica con numeri a virgola mobile non è sicuro per la localizzazione.</span><span class="sxs-lookup"><span data-stu-id="66001-311">The use of canonical syntax with floating point numbers is not localization safe.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66001-312">Booleano <strong>true</strong> / <strong>false</strong></span><span class="sxs-lookup"><span data-stu-id="66001-312">Boolean <strong>true</strong>/<strong>false</strong></span></span></td>
<td><span data-ttu-id="66001-313">System. noread: = System. StructuredQueryType. Boolean # true</span><span class="sxs-lookup"><span data-stu-id="66001-313">System.IsRead:=System.StructuredQueryType.Boolean#True</span></span><br/> <span data-ttu-id="66001-314">System. IsEncrypted:-System. StructuredQueryType. Boolean # false</span><span class="sxs-lookup"><span data-stu-id="66001-314">System.IsEncrypted:-System.StructuredQueryType.Boolean#False</span></span><br/></td>
<td><span data-ttu-id="66001-315">Valore booleano <strong>true</strong> .</span><span class="sxs-lookup"><span data-stu-id="66001-315">The <strong>TRUE</strong> Boolean value.</span></span><br/> <span data-ttu-id="66001-316">Valore booleano <strong>false</strong> .</span><span class="sxs-lookup"><span data-stu-id="66001-316">The <strong>FALSE</strong> Boolean value.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66001-317">[]</span><span class="sxs-lookup"><span data-stu-id="66001-317">[]</span></span></td>
<td><span data-ttu-id="66001-318">System. Keywords: = []</span><span class="sxs-lookup"><span data-stu-id="66001-318">System.Keywords:=[]</span></span><br/></td>
<td><span data-ttu-id="66001-319">Le parentesi quadre vuote indicano che non esiste alcun valore.</span><span class="sxs-lookup"><span data-stu-id="66001-319">Empty square brackets denote that there is no value.</span></span> <span data-ttu-id="66001-320">In questo esempio vengono trovati tutti gli elementi che non sono stati contrassegnati.</span><span class="sxs-lookup"><span data-stu-id="66001-320">This example finds all items that have not been tagged.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66001-321">Date assolute</span><span class="sxs-lookup"><span data-stu-id="66001-321">Absolute dates</span></span></td>
<td><span data-ttu-id="66001-322">System. ItemDate: 1/26/2010</span><span class="sxs-lookup"><span data-stu-id="66001-322">System.ItemDate:1/26/2010</span></span><br/> <span data-ttu-id="66001-323">SystemDateModified 10/15/2002 19:00</span><span class="sxs-lookup"><span data-stu-id="66001-323">SystemDateModified 10/15/2002 19:00</span></span><br/></td>
<td><span data-ttu-id="66001-324">Trova gli elementi con una data di 26 gennaio 2010.</span><span class="sxs-lookup"><span data-stu-id="66001-324">Finds items with a date of 26 January 2010.</span></span><br/> <span data-ttu-id="66001-325">Trova gli elementi modificati il 15 ottobre 2002 tra le ore 19:00:00 e 19:00:59.</span><span class="sxs-lookup"><span data-stu-id="66001-325">Finds items that were modified on 15 October 2002 between the hours 19:00:00 and 19:00:59.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="66001-326">Poiché i formati di data, ad esempio i formati a virgola mobile, variano tra le impostazioni locali, l'uso della sintassi canonica con date assolute non è supportato e non è sicuro per la localizzazione.</span><span class="sxs-lookup"><span data-stu-id="66001-326">Because date formats (like floating point formats) vary among locales, the use of canonical syntax with absolute dates is not supported and is not localization safe.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66001-327">Date relative</span><span class="sxs-lookup"><span data-stu-id="66001-327">Relative dates</span></span></td>
<td><span data-ttu-id="66001-328">System. ItemDate: System. StructuredQueryType. DateTime # today</span><span class="sxs-lookup"><span data-stu-id="66001-328">System.ItemDate:System.StructuredQueryType.DateTime#Today</span></span><br/> <span data-ttu-id="66001-329">System. DateAcquired: System. StructuredQueryType. DateTime # NextMonth</span><span class="sxs-lookup"><span data-stu-id="66001-329">System.DateAcquired:System.StructuredQueryType.DateTime#NextMonth</span></span><br/> <span data-ttu-id="66001-330">System. Message. DateReceived: System. StructuredQueryType. DateTime # LastYear</span><span class="sxs-lookup"><span data-stu-id="66001-330">System.Message.DateReceived:System.StructuredQueryType.DateTime#LastYear</span></span><br/></td>
<td><span data-ttu-id="66001-331">Trova gli elementi con la data odierna.</span><span class="sxs-lookup"><span data-stu-id="66001-331">Finds items with today's date.</span></span><br/> <span data-ttu-id="66001-332">Trova gli elementi con una data nel mese successivo.</span><span class="sxs-lookup"><span data-stu-id="66001-332">Finds items with a date in the next month.</span></span><br/> <span data-ttu-id="66001-333">Trova gli elementi con una data nell'ultimo anno.</span><span class="sxs-lookup"><span data-stu-id="66001-333">Finds items with a date in the last year.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="66001-334">Oltre a eseguire ricerche in base a intervalli di date e date specifici, AQS riconosce i valori relativi alla data, ad esempio <em>Today</em>, <em>Tomorrow</em>, <em>NEXTWEEK</em>, <em>NEXTMONTH</em>, e Day, ad esempio <em>Tuesday</em> o <em>Monday. Mercoledì</em>) e mese (<em>febbraio</em>).</span><span class="sxs-lookup"><span data-stu-id="66001-334">In addition to searching on specific dates and date ranges, AQS recognizes relative date values (like <em>today</em>, <em>tomorrow</em>, <em>nextweek</em>, <em>nextmonth</em>), and day (like <em>Tuesday</em> or <em>Monday..Wednesday</em>), and month (<em>February</em>).</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66001-335">..</span><span class="sxs-lookup"><span data-stu-id="66001-335">..</span></span></td>
<td><span data-ttu-id="66001-336">System. ItemDate: 11/05/04.. 11/10/04 System. Size: 5 KB.. 10kb</span><span class="sxs-lookup"><span data-stu-id="66001-336">System.ItemDate:11/05/04..11/10/04 System.Size:5kb..10kb</span></span><br/></td>
<td><span data-ttu-id="66001-337">I punti doppi indicano un intervallo di valori.</span><span class="sxs-lookup"><span data-stu-id="66001-337">Double periods indicate a value range.</span></span> <span data-ttu-id="66001-338">Trova gli elementi con una data compresa tra 11/05/04 e 11/10/04 inclusi.</span><span class="sxs-lookup"><span data-stu-id="66001-338">Finds items with a date between 11/05/04 and 11/10/04, inclusive.</span></span><br/> <span data-ttu-id="66001-339">Trova gli elementi compresi tra 5 e 10KB.</span><span class="sxs-lookup"><span data-stu-id="66001-339">Finds items between 5 and 10kb in size.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="scope-restrictions"></a><span data-ttu-id="66001-340">Limitazioni dell'ambito</span><span class="sxs-lookup"><span data-stu-id="66001-340">Scope Restrictions</span></span>

<span data-ttu-id="66001-341">Gli utenti possono limitare l'ambito delle proprie ricerche a percorsi di cartelle o archivi dati specifici.</span><span class="sxs-lookup"><span data-stu-id="66001-341">Users can limit the scope of their searches to specific folder locations or data stores.</span></span> <span data-ttu-id="66001-342">Se, ad esempio, si utilizzano più account di posta elettronica e si desidera limitare una query a Microsoft Outlook o Microsoft Outlook Express, è possibile `System.Search.Store:mapi` utilizzare `System.Search.Store:oe` rispettivamente o.</span><span class="sxs-lookup"><span data-stu-id="66001-342">For example, if you use several email accounts and you want to limit a query to either Microsoft Outlook or Microsoft Outlook Express, you can use `System.Search.Store:mapi` or `System.Search.Store:oe` respectively.</span></span> <span data-ttu-id="66001-343">La tabella seguente illustra alcuni esempi di come limitare una ricerca in base all'archivio dati.</span><span class="sxs-lookup"><span data-stu-id="66001-343">The following table shows some examples of how to restrict a search by data store.</span></span>



| <span data-ttu-id="66001-344">Limita la ricerca per archivio dati</span><span class="sxs-lookup"><span data-stu-id="66001-344">Restrict search by data store</span></span>  | <span data-ttu-id="66001-345">Parola chiave</span><span class="sxs-lookup"><span data-stu-id="66001-345">Keyword</span></span> | <span data-ttu-id="66001-346">Esempio</span><span class="sxs-lookup"><span data-stu-id="66001-346">Example</span></span>                                     |
|--------------------------------|---------|---------------------------------------------|
| <span data-ttu-id="66001-347">File</span><span class="sxs-lookup"><span data-stu-id="66001-347">Files</span></span>                          | <span data-ttu-id="66001-348">file</span><span class="sxs-lookup"><span data-stu-id="66001-348">file</span></span>    | <span data-ttu-id="66001-349">System. search. Store: file</span><span class="sxs-lookup"><span data-stu-id="66001-349">System.Search.Store:file</span></span>                    |
| <span data-ttu-id="66001-350">Outlook</span><span class="sxs-lookup"><span data-stu-id="66001-350">Outlook</span></span>                        | <span data-ttu-id="66001-351">MAPI</span><span class="sxs-lookup"><span data-stu-id="66001-351">mapi</span></span>    | <span data-ttu-id="66001-352">System. search. Store: MAPI</span><span class="sxs-lookup"><span data-stu-id="66001-352">System.Search.Store:mapi</span></span>                    |
| <span data-ttu-id="66001-353">Outlook Express</span><span class="sxs-lookup"><span data-stu-id="66001-353">Outlook Express</span></span>                | <span data-ttu-id="66001-354">OE</span><span class="sxs-lookup"><span data-stu-id="66001-354">oe</span></span>      | <span data-ttu-id="66001-355">System. search. Store: OE</span><span class="sxs-lookup"><span data-stu-id="66001-355">System.Search.Store:oe</span></span>                      |
| <span data-ttu-id="66001-356">File offline</span><span class="sxs-lookup"><span data-stu-id="66001-356">Offline files</span></span>                  | <span data-ttu-id="66001-357">CSC</span><span class="sxs-lookup"><span data-stu-id="66001-357">csc</span></span>     | <span data-ttu-id="66001-358">System. search. Store: CSC</span><span class="sxs-lookup"><span data-stu-id="66001-358">System.Search.Store:csc</span></span>                     |
| <span data-ttu-id="66001-359">Cartella specifica nell'unità locale</span><span class="sxs-lookup"><span data-stu-id="66001-359">Specific folder on local drive</span></span> | <span data-ttu-id="66001-360">folder</span><span class="sxs-lookup"><span data-stu-id="66001-360">folder</span></span>  | <span data-ttu-id="66001-361">System. ItemFolderNameDisplay: C: " \\ cartella"</span><span class="sxs-lookup"><span data-stu-id="66001-361">System.ItemFolderNameDisplay:C:"\\MyFolder"</span></span> |



 

## <a name="additional-resources"></a><span data-ttu-id="66001-362">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="66001-362">Additional Resources</span></span>

-   <span data-ttu-id="66001-363">In Windows 7 e versioni successive, può essere disponibile un'opzione di menu di scelta rapida a seconda che venga soddisfatta una condizione AQS.</span><span class="sxs-lookup"><span data-stu-id="66001-363">In Windows 7 and later, a shortcut menu option can be available based on whether an AQS condition is met.</span></span> <span data-ttu-id="66001-364">Per ulteriori informazioni, vedere "recupero del comportamento dinamico per i verbi statici tramite la sintassi di query avanzata" nella sezione [creazione di gestori di menu di scelta rapida](../shell/context-menu-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="66001-364">For more information, see "Getting Dynamic Behavior for Static Verbs by Using Advanced Query Syntax" in [Creating Context Menu Handlers](../shell/context-menu-handlers.md).</span></span>
-   <span data-ttu-id="66001-365">Le query AQS possono essere limitate a specifici tipi di file, noti come tipi di file.</span><span class="sxs-lookup"><span data-stu-id="66001-365">AQS queries can be limited to specific types of files, which are known as file kinds.</span></span> <span data-ttu-id="66001-366">Per altre informazioni, vedere [tipi di file e associazioni](../shell/fa-intro.md).</span><span class="sxs-lookup"><span data-stu-id="66001-366">For more information, see [File Types and Associations](../shell/fa-intro.md).</span></span> <span data-ttu-id="66001-367">Per la documentazione di riferimento della proprietà, vedere [System. Kind](../properties/props-system-kind.md)e [System. KindText](../properties/props-system-kindtext.md).</span><span class="sxs-lookup"><span data-stu-id="66001-367">For property reference documentation, see [System.Kind](../properties/props-system-kind.md), and [System.KindText](../properties/props-system-kindtext.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="66001-368">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="66001-368">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="66001-369">Esecuzione di query sull'indice a livello di codice</span><span class="sxs-lookup"><span data-stu-id="66001-369">Querying the Index Programmatically</span></span>](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[<span data-ttu-id="66001-370">Utilizzo degli approcci SQL e AQS per eseguire una query sull'indice</span><span class="sxs-lookup"><span data-stu-id="66001-370">Using SQL and AQS Approaches to Query the Index</span></span>](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[<span data-ttu-id="66001-371">Esecuzione di query sull'indice con ISearchQueryHelper</span><span class="sxs-lookup"><span data-stu-id="66001-371">Querying the Index with ISearchQueryHelper</span></span>](-search-3x-wds-qryidx-searchqueryhelper.md)
</dt> <dt>

[<span data-ttu-id="66001-372">Esecuzione di query sull'indice con il protocollo search-ms</span><span class="sxs-lookup"><span data-stu-id="66001-372">Querying the Index with the search-ms Protocol</span></span>](-search-3x-wds-qryidx-searchms.md)
</dt> <dt>

[<span data-ttu-id="66001-373">Esecuzione di query sull'indice con la sintassi SQL di ricerca di Windows</span><span class="sxs-lookup"><span data-stu-id="66001-373">Querying the Index with Windows Search SQL Syntax</span></span>](-search-sql-windowssearch-entry.md)
</dt> </dl>

 

 
