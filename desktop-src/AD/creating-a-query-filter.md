---
title: Creazione di un filtro query
description: Un filtro di query indica Active Directory Domain Services per trovare i dati in una sintassi di query LDAP. Tutte le tecnologie di accesso ai dati specificate elencate nell'argomento scelta della tecnologia di ricerca supportano la sintassi delle query LDAP.
ms.assetid: 0bd652f0-41a6-4a0d-8742-9d6a2a7f168a
ms.tgt_platform: multiple
keywords:
- Esempi di Active Directory Active Directory, creazione di un filtro di query
- filtri query
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc2e0a4e4a02312fcc9affb681407044ba0d8e18
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855202"
---
# <a name="creating-a-query-filter"></a><span data-ttu-id="3ef7b-106">Creazione di un filtro query</span><span class="sxs-lookup"><span data-stu-id="3ef7b-106">Creating a Query Filter</span></span>

<span data-ttu-id="3ef7b-107">Un filtro di query indica Active Directory Domain Services per trovare i dati in una sintassi di query LDAP.</span><span class="sxs-lookup"><span data-stu-id="3ef7b-107">A query filter instructs Active Directory Domain Services to find data in an LDAP query syntax.</span></span> <span data-ttu-id="3ef7b-108">Tutte le tecnologie di accesso ai dati specificate elencate nell'argomento [scelta della tecnologia di ricerca](choosing-the-search-technology.md) supportano la sintassi delle query LDAP.</span><span class="sxs-lookup"><span data-stu-id="3ef7b-108">All the specified data access technologies listed in the [Choosing the Search Technology](choosing-the-search-technology.md) topic support LDAP query syntax.</span></span>

<span data-ttu-id="3ef7b-109">La sintassi della query LDAP è la seguente:</span><span class="sxs-lookup"><span data-stu-id="3ef7b-109">The LDAP query syntax is as follows:</span></span>


```C++
<expression><expression>...
```



<span data-ttu-id="3ef7b-110">Un filtro può contenere una o più espressioni.</span><span class="sxs-lookup"><span data-stu-id="3ef7b-110">A filter can contain one, or more, expressions.</span></span> <span data-ttu-id="3ef7b-111">Un'espressione ha il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="3ef7b-111">An expression has the following form:</span></span>


```C++
(<logicaloperator><comparison><comparison...>)
```



<span data-ttu-id="3ef7b-112">dove " &lt; LogicalOperator &gt; " è uno dei seguenti.</span><span class="sxs-lookup"><span data-stu-id="3ef7b-112">where "&lt;logicaloperator&gt;" is one of the following.</span></span>



| <span data-ttu-id="3ef7b-113">Operatore</span><span class="sxs-lookup"><span data-stu-id="3ef7b-113">Operator</span></span>        | <span data-ttu-id="3ef7b-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3ef7b-114">Description</span></span>                |
|-----------------|----------------------------|
| <span data-ttu-id="3ef7b-115">"\|"</span><span class="sxs-lookup"><span data-stu-id="3ef7b-115">"\|"</span></span><br/> | <span data-ttu-id="3ef7b-116">**Or** logico</span><span class="sxs-lookup"><span data-stu-id="3ef7b-116">Logical **OR**</span></span><br/>  |
| <span data-ttu-id="3ef7b-117">"&"</span><span class="sxs-lookup"><span data-stu-id="3ef7b-117">"&"</span></span><br/>  | <span data-ttu-id="3ef7b-118">**And** logico</span><span class="sxs-lookup"><span data-stu-id="3ef7b-118">Logical **AND**</span></span><br/> |
| <span data-ttu-id="3ef7b-119">"!"</span><span class="sxs-lookup"><span data-stu-id="3ef7b-119">"!"</span></span><br/>  | <span data-ttu-id="3ef7b-120">**Not** logico</span><span class="sxs-lookup"><span data-stu-id="3ef7b-120">Logical **NOT**</span></span><br/> |



 

<span data-ttu-id="3ef7b-121">e &lt; il "confronto &gt; " è il seguente:</span><span class="sxs-lookup"><span data-stu-id="3ef7b-121">and "&lt;comparison&gt;" is the following:</span></span>


```C++
(<attribute><operator><value>)
```



<span data-ttu-id="3ef7b-122">dove " &lt; Attribute &gt; " è l' **ldapDisplayName** dell'attributo da valutare, " &lt; value &gt; " è il valore da confrontare e " &lt; Operator &gt; " è uno degli operatori di confronto seguenti.</span><span class="sxs-lookup"><span data-stu-id="3ef7b-122">where "&lt;attribute&gt;" is the **lDAPDisplayName** of the attribute to evaluate, "&lt;value&gt;" is the value to compare against, and "&lt;operator&gt;" is one of the following comparison operators.</span></span>



| <span data-ttu-id="3ef7b-123">Operatore</span><span class="sxs-lookup"><span data-stu-id="3ef7b-123">Operator</span></span>           | <span data-ttu-id="3ef7b-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3ef7b-124">Description</span></span>                         |
|--------------------|-------------------------------------|
| <span data-ttu-id="3ef7b-125">"="</span><span class="sxs-lookup"><span data-stu-id="3ef7b-125">"="</span></span><br/>     | <span data-ttu-id="3ef7b-126">Uguale a</span><span class="sxs-lookup"><span data-stu-id="3ef7b-126">Equals</span></span><br/>                   |
| <span data-ttu-id="3ef7b-127">"~="</span><span class="sxs-lookup"><span data-stu-id="3ef7b-127">"~="</span></span><br/>    | <span data-ttu-id="3ef7b-128">Approssimativamente uguale a</span><span class="sxs-lookup"><span data-stu-id="3ef7b-128">Approximately equals</span></span><br/>     |
| <span data-ttu-id="3ef7b-129">"<="</span><span class="sxs-lookup"><span data-stu-id="3ef7b-129">"<="</span></span><br/> | <span data-ttu-id="3ef7b-130">Minore o uguale a</span><span class="sxs-lookup"><span data-stu-id="3ef7b-130">Less than or equal to</span></span><br/>    |
| <span data-ttu-id="3ef7b-131">">="</span><span class="sxs-lookup"><span data-stu-id="3ef7b-131">">="</span></span><br/> | <span data-ttu-id="3ef7b-132">Maggiore o uguale a</span><span class="sxs-lookup"><span data-stu-id="3ef7b-132">Greater than or equal to</span></span><br/> |



 

<span data-ttu-id="3ef7b-133">Inoltre, a seconda della sintassi dell'attributo, il " &lt; valore &gt; " può contenere il carattere jolly (" \* ").</span><span class="sxs-lookup"><span data-stu-id="3ef7b-133">In addition, depending on the attribute syntax, the "&lt;value&gt;" may contain the wildcard symbol ("\*").</span></span> <span data-ttu-id="3ef7b-134">Un " &lt; valore &gt; " che contiene solo un carattere jolly verificherà l'esistenza di qualsiasi valore in " &lt; Attribute &gt; ".</span><span class="sxs-lookup"><span data-stu-id="3ef7b-134">A "&lt;value&gt;" that contains only a wildcard will check for the existence of any value in "&lt;attribute&gt;".</span></span> <span data-ttu-id="3ef7b-135">Se non è impostato alcun valore per " &lt; Attribute &gt; ", il test avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="3ef7b-135">If no value is set for "&lt;attribute&gt;", the test will fail.</span></span>

<span data-ttu-id="3ef7b-136">Se uno dei seguenti caratteri speciali deve essere visualizzato nel filtro della query come valori letterali, è necessario sostituirli con la sequenza di escape elencata.</span><span class="sxs-lookup"><span data-stu-id="3ef7b-136">If any of the following special characters must appear in the query filter as literals, they must be replaced by the listed escape sequence.</span></span>



| <span data-ttu-id="3ef7b-137">Carattere ASCII</span><span class="sxs-lookup"><span data-stu-id="3ef7b-137">ASCII character</span></span>    | <span data-ttu-id="3ef7b-138">Sostituzione sequenza di escape</span><span class="sxs-lookup"><span data-stu-id="3ef7b-138">Escape sequence substitute</span></span> |
|--------------------|----------------------------|
| \*<br/>      | <span data-ttu-id="3ef7b-139">" \\ 2a"</span><span class="sxs-lookup"><span data-stu-id="3ef7b-139">"\\2a"</span></span><br/>          |
| <span data-ttu-id="3ef7b-140">(</span><span class="sxs-lookup"><span data-stu-id="3ef7b-140">(</span></span><br/>       | <span data-ttu-id="3ef7b-141">" \\ 28"</span><span class="sxs-lookup"><span data-stu-id="3ef7b-141">"\\28"</span></span><br/>          |
| <span data-ttu-id="3ef7b-142">)</span><span class="sxs-lookup"><span data-stu-id="3ef7b-142">)</span></span><br/>       | <span data-ttu-id="3ef7b-143">" \\ 29"</span><span class="sxs-lookup"><span data-stu-id="3ef7b-143">"\\29"</span></span><br/>          |
| \\<br/>      | <span data-ttu-id="3ef7b-144">" \\ 5C"</span><span class="sxs-lookup"><span data-stu-id="3ef7b-144">"\\5c"</span></span><br/>          |
| <span data-ttu-id="3ef7b-145">**NUL**</span><span class="sxs-lookup"><span data-stu-id="3ef7b-145">**NUL**</span></span><br/> | <span data-ttu-id="3ef7b-146">" \\ 00"</span><span class="sxs-lookup"><span data-stu-id="3ef7b-146">"\\00"</span></span><br/>          |



 

<span data-ttu-id="3ef7b-147">Inoltre, i dati binari arbitrari possono essere rappresentati utilizzando la sintassi della sequenza di escape codificando ogni byte di dati binari con la barra rovesciata seguita da due cifre esadecimali.</span><span class="sxs-lookup"><span data-stu-id="3ef7b-147">In addition, arbitrary binary data may be represented using the escape sequence syntax by encoding each byte of binary data with the backslash followed by two hexadecimal digits.</span></span> <span data-ttu-id="3ef7b-148">Ad esempio, il valore a quattro byte 0x00000004 è codificato come " \\ 00 \\ 00 \\ 00 \\ 04" in una stringa di filtro.</span><span class="sxs-lookup"><span data-stu-id="3ef7b-148">For example, the four-byte value 0x00000004 is encoded as "\\00\\00\\00\\04" in a filter string.</span></span>

## <a name="examples"></a><span data-ttu-id="3ef7b-149">Esempio</span><span class="sxs-lookup"><span data-stu-id="3ef7b-149">Examples</span></span>

<span data-ttu-id="3ef7b-150">Nella stringa di query seguente vengono cercati tutti gli oggetti di tipo "computer".</span><span class="sxs-lookup"><span data-stu-id="3ef7b-150">The following query string will search for all objects of type "computer".</span></span>


```C++
(objectCategory=computer)
```



<span data-ttu-id="3ef7b-151">Nella stringa di query seguente vengono cercati tutti gli oggetti di tipo "computer" con un nome che inizia con "desktop".</span><span class="sxs-lookup"><span data-stu-id="3ef7b-151">The following query string will search for all objects of type "computer" with a name that begins with "desktop".</span></span>


```C++
(&(objectCategory=computer)(name=desktop*))
```



<span data-ttu-id="3ef7b-152">Nella stringa di query seguente vengono cercati tutti gli oggetti di tipo "computer" con un nome che inizia con "desktop" o un nome che inizia con "notebook".</span><span class="sxs-lookup"><span data-stu-id="3ef7b-152">The following query string will search for all objects of type "computer" with a name that begins with "desktop" or a name that begins with "notebook".</span></span>


```C++
(&(objectCategory=computer)(|(name=desktop*)(name=notebook*)))
```



<span data-ttu-id="3ef7b-153">La stringa di query seguente Cerca tutti gli oggetti di tipo "User" con un numero di telefono dell'abitazione.</span><span class="sxs-lookup"><span data-stu-id="3ef7b-153">The following query string will search for all objects of type "user" that have a home phone number.</span></span>


```C++
(&(objectCategory=user)(homePhone=*))
```



<span data-ttu-id="3ef7b-154">Per ulteriori informazioni sulle stringhe di filtro della query e sugli esempi di utilizzo, vedere:</span><span class="sxs-lookup"><span data-stu-id="3ef7b-154">For more information about query filter strings, and usage examples, see:</span></span>

-   [<span data-ttu-id="3ef7b-155">Ricerca di oggetti per classe</span><span class="sxs-lookup"><span data-stu-id="3ef7b-155">Finding Objects by Class</span></span>](finding-objects-by-class.md)
-   [<span data-ttu-id="3ef7b-156">Ricerca di oggetti in base al nome</span><span class="sxs-lookup"><span data-stu-id="3ef7b-156">Finding Objects by Name</span></span>](finding-objects-by-name.md)
-   [<span data-ttu-id="3ef7b-157">Ricerca di un elenco di attributi su cui eseguire una query</span><span class="sxs-lookup"><span data-stu-id="3ef7b-157">Finding a List of Attributes To Query</span></span>](finding-a-list-of-attributes-to-query.md)
-   [<span data-ttu-id="3ef7b-158">Verifica della sintassi del filtro query</span><span class="sxs-lookup"><span data-stu-id="3ef7b-158">Checking the Query Filter Syntax</span></span>](checking-the-query-filter-syntax.md)
-   [<span data-ttu-id="3ef7b-159">Come specificare i valori di confronto</span><span class="sxs-lookup"><span data-stu-id="3ef7b-159">How to Specify Comparison Values</span></span>](how-to-specify-comparison-values.md)

 

 





