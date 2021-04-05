---
description: Il predicato FREETEXT fa parte della clausola WHERE e supporta la ricerca di parole e frasi nelle colonne di testo.
ms.assetid: 8afc95d1-25cd-4448-8bee-d132c2da22b3
title: Predicato FREETEXT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc78be4d5ac75f892c82c6dad390e4583876856f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750386"
---
# <a name="freetext-predicate"></a><span data-ttu-id="b0c7a-103">Predicato FREETEXT</span><span class="sxs-lookup"><span data-stu-id="b0c7a-103">FREETEXT Predicate</span></span>

<span data-ttu-id="b0c7a-104">Il predicato FREETEXT fa parte della clausola [where](-search-sql-where.md) e supporta la ricerca di parole e frasi nelle colonne di testo.</span><span class="sxs-lookup"><span data-stu-id="b0c7a-104">The FREETEXT predicate is part of the [WHERE](-search-sql-where.md) clause and supports searching for words and phrases in text columns.</span></span> <span data-ttu-id="b0c7a-105">Usare il predicato FREETEXT per trovare documenti contenenti combinazioni di parole di ricerca distribuite in tutto il contenuto o le colonne specificate.</span><span class="sxs-lookup"><span data-stu-id="b0c7a-105">Use the FREETEXT predicate to find documents containing combinations of the search words spread throughout the content or columns specified.</span></span> <span data-ttu-id="b0c7a-106">Per ottenere il valore di pertinenza, includere System. search. Rank, che è un rango di rilevanza, come colonna nell'istruzione SELECT.</span><span class="sxs-lookup"><span data-stu-id="b0c7a-106">To get the rank value, include System.Search.Rank, which is a ranking of relevence, as a column in the SELECT statment.</span></span>

<span data-ttu-id="b0c7a-107">Il predicato FREETEXT presenta la sintassi seguente:</span><span class="sxs-lookup"><span data-stu-id="b0c7a-107">The FREETEXT predicate has the following syntax:</span></span>


```
FREETEXT
(["<fulltext_column>",]'<freetext_condition>'[,<LCID>])...
```



<span data-ttu-id="b0c7a-108">Il riferimento alla colonna full-text è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="b0c7a-108">The fulltext column reference is optional.</span></span> <span data-ttu-id="b0c7a-109">Con esso, è possibile specificare una singola colonna o un [alias di raggruppamento di colonne](-search-sql-with-as.md) su cui viene testato il predicato FREETEXT.</span><span class="sxs-lookup"><span data-stu-id="b0c7a-109">With it, you can specify a single column, or a [column grouping alias](-search-sql-with-as.md) against which the FREETEXT predicate is tested.</span></span> <span data-ttu-id="b0c7a-110">Quando la colonna full-text viene specificata come "ALL" o " \* ", viene eseguita la ricerca di tutte le proprietà di testo indicizzato.</span><span class="sxs-lookup"><span data-stu-id="b0c7a-110">When the fulltext column is specified as "ALL" or "\*", all indexed text properties are searched.</span></span> <span data-ttu-id="b0c7a-111">Sebbene non sia necessario che la colonna sia una proprietà di testo, i risultati potrebbero non essere significativi se la colonna è un altro tipo di dati.</span><span class="sxs-lookup"><span data-stu-id="b0c7a-111">Although the column is not required to be a text property, the results might be meaningless if the column is some other data type.</span></span> <span data-ttu-id="b0c7a-112">Il nome della colonna può essere un [identificatore](-search-sql-identifiers.md)regolare o delimitato ed è necessario separarlo dalla condizione con una virgola.</span><span class="sxs-lookup"><span data-stu-id="b0c7a-112">The column name can be either a regular or delimited [identifier](-search-sql-identifiers.md), and you must separate it from the condition by a comma.</span></span> <span data-ttu-id="b0c7a-113">Se non viene specificata alcuna condizione full-text, viene usata la colonna Contents, che è il corpo del documento.</span><span class="sxs-lookup"><span data-stu-id="b0c7a-113">If no fulltext condition is supplied, the Contents column, which is the body of the document, is used.</span></span>

<span data-ttu-id="b0c7a-114">È possibile specificare le impostazioni locali di ricerca per identificare il Word breaker e i moduli flessivi appropriati per la query di ricerca.</span><span class="sxs-lookup"><span data-stu-id="b0c7a-114">You can specify a search locale to identify the appropriate word breaker and inflectional forms for the search query.</span></span> <span data-ttu-id="b0c7a-115">I valori delle impostazioni locali validi sono un identificatore del codice lingua (LCID) di Windows standard.</span><span class="sxs-lookup"><span data-stu-id="b0c7a-115">Valid locale values are a Windows standard language code identifier (LCID).</span></span> <span data-ttu-id="b0c7a-116">Ad esempio, 1033 è il LCID per Stati Uniti-English.</span><span class="sxs-lookup"><span data-stu-id="b0c7a-116">For example, 1033 is the LCID for United States-English.</span></span> <span data-ttu-id="b0c7a-117">Posizionare il LCID come ultimo elemento all'interno delle parentesi della clausola FREETEXT.</span><span class="sxs-lookup"><span data-stu-id="b0c7a-117">Place the LCID as the last item inside the parentheses of the FREETEXT clause.</span></span> <span data-ttu-id="b0c7a-118">Per informazioni importanti sulla ricerca e sui linguaggi, vedere [uso delle ricerche localizzate](-search-sql-usinglocsearches.md).</span><span class="sxs-lookup"><span data-stu-id="b0c7a-118">For important information about searching and languages, see [Using Localized Searches](-search-sql-usinglocsearches.md).</span></span>

> [!Note]  
> <span data-ttu-id="b0c7a-119">Le impostazioni locali di ricerca predefinite sono le impostazioni locali predefinite del sistema.</span><span class="sxs-lookup"><span data-stu-id="b0c7a-119">The default search locale is the system default locale.</span></span>

 

<span data-ttu-id="b0c7a-120">È necessario racchiudere la parte della condizione FREETEXT tra virgolette singole e deve essere costituita da uno o più termini di ricerca.</span><span class="sxs-lookup"><span data-stu-id="b0c7a-120">You must enclose the freetext condition portion in single quotation marks, and it must consist of one or more search terms.</span></span> <span data-ttu-id="b0c7a-121">Il predicato FREETEXT non supporta le operazioni logiche.</span><span class="sxs-lookup"><span data-stu-id="b0c7a-121">The FREETEXT predicate does not support logical operations.</span></span> <span data-ttu-id="b0c7a-122">Per cercare una frase come se fosse una singola parola, racchiudere la frase tra virgolette doppie.</span><span class="sxs-lookup"><span data-stu-id="b0c7a-122">To search for a phrase as if it were a single word, enclose the phrase in double quotation marks.</span></span>

<span data-ttu-id="b0c7a-123">Quando si usa il predicato FREETEXT, i risultati della query di ricerca restituiscono documenti contenenti tutti i termini di ricerca.</span><span class="sxs-lookup"><span data-stu-id="b0c7a-123">When you use the FREETEXT predicate, the search query results return documents containing all of the search terms.</span></span> <span data-ttu-id="b0c7a-124">I termini non devono essere visualizzati in un ordine particolare.</span><span class="sxs-lookup"><span data-stu-id="b0c7a-124">The terms do not need to appear in any particular order.</span></span> <span data-ttu-id="b0c7a-125">I documenti che contengono più termini di ricerca hanno valori di colonna di rango superiore.</span><span class="sxs-lookup"><span data-stu-id="b0c7a-125">Documents that contain more of the search terms have higher rank column values.</span></span>

## <a name="examples"></a><span data-ttu-id="b0c7a-126">Esempio</span><span class="sxs-lookup"><span data-stu-id="b0c7a-126">Examples</span></span>

<span data-ttu-id="b0c7a-127">Nell'esempio seguente viene eseguita la ricerca di documenti contenenti "computer", "software", "hardware" o combinazioni di queste parole:</span><span class="sxs-lookup"><span data-stu-id="b0c7a-127">The following example searches for documents containing "computer", "software", "hardware", or combinations of those words:</span></span>


```
WHERE FREETEXT('computer software hardware')
```



> [!Note]  
> <span data-ttu-id="b0c7a-128">Non è possibile usare la corrispondenza con una sola parola e la corrispondenza di frasi nello stesso predicato FREETEXT.</span><span class="sxs-lookup"><span data-stu-id="b0c7a-128">You cannot use both single-word matching and phrase matching in the same FREETEXT predicate.</span></span>

 

<span data-ttu-id="b0c7a-129">Quando si eseguono query con contrazioni, è necessario utilizzare caratteri di escape per le virgolette durante la contrazione quando si utilizza FREETEXT, ma non quando si utilizza CONTAINs.</span><span class="sxs-lookup"><span data-stu-id="b0c7a-129">When performing queries with contractions, you must escape the quotation mark in the contraction when using FREETEXT, but not when using CONTAINS.</span></span>

<span data-ttu-id="b0c7a-130">La sintassi seguente, ad esempio, ha esito negativo:</span><span class="sxs-lookup"><span data-stu-id="b0c7a-130">For example, the following syntax fails:</span></span>


```
WHERE FREETEXT(*,'"We'll meet next week"')
```



<span data-ttu-id="b0c7a-131">La sintassi corretta include due virgolette singole, non le virgolette doppie.</span><span class="sxs-lookup"><span data-stu-id="b0c7a-131">The correct syntax includes two single quotation marks, not a double quotation mark.</span></span>

<span data-ttu-id="b0c7a-132">La sintassi seguente ha esito positivo:</span><span class="sxs-lookup"><span data-stu-id="b0c7a-132">The following syntax succeeds:</span></span>


```
WHERE FREETEXT(*,'"We''ll meet next week"')
```



## <a name="related-topics"></a><span data-ttu-id="b0c7a-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b0c7a-133">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="b0c7a-134">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="b0c7a-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b0c7a-135">CONTIENE predicato</span><span class="sxs-lookup"><span data-stu-id="b0c7a-135">CONTAINS Predicate</span></span>](-search-sql-contains.md)
</dt> <dt>

[<span data-ttu-id="b0c7a-136">Clausola WHERE</span><span class="sxs-lookup"><span data-stu-id="b0c7a-136">WHERE Clause</span></span>](-search-sql-where.md)
</dt> <dt>

<span data-ttu-id="b0c7a-137">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="b0c7a-137">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b0c7a-138">Predicati non full-text</span><span class="sxs-lookup"><span data-stu-id="b0c7a-138">Non-Full-Text Predicates</span></span>](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



