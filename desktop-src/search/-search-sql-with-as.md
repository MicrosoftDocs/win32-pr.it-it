---
description: Gli alias dei gruppi di colonne consentono di utilizzare nomi più brevi al posto del nome di una colonna o di un gruppo di colonne. Il predicato alias del gruppo facoltativo fa parte della clausola WHERE.
ms.assetid: 7782ac24-ea6c-4a97-b1b6-982f276fcefc
title: CON il predicato alias gruppo AS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29218e11fbffe5f47128eeefba3a7fe847a5b21d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750367"
---
# <a name="with----as-group-alias-predicate"></a><span data-ttu-id="f8c5b-104">CON il predicato alias gruppo AS</span><span class="sxs-lookup"><span data-stu-id="f8c5b-104">WITH -- AS Group Alias Predicate</span></span>

<span data-ttu-id="f8c5b-105">Gli alias dei gruppi di colonne consentono di utilizzare nomi più brevi al posto del nome di una colonna o di un gruppo di colonne.</span><span class="sxs-lookup"><span data-stu-id="f8c5b-105">Column group aliases provide a way to use shorter names in place of the name of a column or a group of columns.</span></span> <span data-ttu-id="f8c5b-106">Il predicato alias del gruppo facoltativo fa parte della clausola WHERE.</span><span class="sxs-lookup"><span data-stu-id="f8c5b-106">The optional group alias predicate is part of the WHERE clause.</span></span> <span data-ttu-id="f8c5b-107">La sintassi è la seguente:</span><span class="sxs-lookup"><span data-stu-id="f8c5b-107">Its syntax follows:</span></span>


```
...WHERE[ WITH(<columns>) AS #<alias_name>]
[,WITH(<columns>) AS #<alias_name>]
```



<span data-ttu-id="f8c5b-108">È possibile specificare più di un alias di gruppo, separando con... COME predicati per virgole.</span><span class="sxs-lookup"><span data-stu-id="f8c5b-108">You can specify more than one group alias, separating the WITH...AS predicates by commas.</span></span>

<span data-ttu-id="f8c5b-109">Quando si fa riferimento a un alias di gruppo in un predicato della clausola WHERE, la condizione viene applicata a ogni colonna del gruppo.</span><span class="sxs-lookup"><span data-stu-id="f8c5b-109">When a group alias is referred to in a WHERE clause predicate, the condition is applied to each column in the group.</span></span> <span data-ttu-id="f8c5b-110">I valori logici risultanti dalla corrispondenza di ogni colonna vengono combinati utilizzando l'operatore logico **or** .</span><span class="sxs-lookup"><span data-stu-id="f8c5b-110">The logical values resulting from matching each column are combined by using the logical **OR** operator.</span></span>

<span data-ttu-id="f8c5b-111">È necessario definire un alias per poterlo utilizzare e utilizzarlo solo all'interno della clausola WHERE.</span><span class="sxs-lookup"><span data-stu-id="f8c5b-111">An alias must be defined before it can be used, and it can be used only within the WHERE clause.</span></span> <span data-ttu-id="f8c5b-112">Il nome dell'alias deve essere un identificatore regolare preceduto da un simbolo di cancelletto obbligatorio ( \# ).</span><span class="sxs-lookup"><span data-stu-id="f8c5b-112">The alias name must be a regular identifier preceded by a required pound sign (\#).</span></span>

<span data-ttu-id="f8c5b-113">L'identificatore di colonna può contenere uno o più identificatori di colonna separati da virgole.</span><span class="sxs-lookup"><span data-stu-id="f8c5b-113">The column specifier can contain one or more column specifiers, separated by commas.</span></span> <span data-ttu-id="f8c5b-114">L'elenco di colonne deve essere racchiuso tra parentesi e la ponderazione può essere assegnata a ciascuna.</span><span class="sxs-lookup"><span data-stu-id="f8c5b-114">The list of columns must be enclosed in parentheses and weighting can be assigned to each.</span></span> <span data-ttu-id="f8c5b-115">Ogni colonna presenta la sintassi seguente:</span><span class="sxs-lookup"><span data-stu-id="f8c5b-115">Each column has the following syntax:</span></span>


```
<column_identifier> [<weight_assignment>]
```



<span data-ttu-id="f8c5b-116">Per informazioni su come specificare i pesi delle colonne, vedere [predicato FREETEXT](-search-sql-freetext.md) e [predicato CONTAINS](-search-sql-contains.md).</span><span class="sxs-lookup"><span data-stu-id="f8c5b-116">For information on specifying column weights, see [FREETEXT Predicate](-search-sql-freetext.md) and [CONTAINS Predicate](-search-sql-contains.md).</span></span>

<span data-ttu-id="f8c5b-117">L'identificatore di colonna può essere regolare o delimitato.</span><span class="sxs-lookup"><span data-stu-id="f8c5b-117">The column identifier can be regular or delimited.</span></span>

## <a name="examples"></a><span data-ttu-id="f8c5b-118">Esempio</span><span class="sxs-lookup"><span data-stu-id="f8c5b-118">Examples</span></span>

<span data-ttu-id="f8c5b-119">Negli esempi di clausole WHERE seguenti viene illustrato quando e come è possibile utilizzare il predicato alias di gruppo.</span><span class="sxs-lookup"><span data-stu-id="f8c5b-119">The following WHERE clause examples demonstrate when and how you can use the group alias predicate.</span></span> <span data-ttu-id="f8c5b-120">Nel primo esempio viene illustrata una clausola WHERE più ripetitiva che non utilizza l'aliasing del gruppo.</span><span class="sxs-lookup"><span data-stu-id="f8c5b-120">The first example shows a more repetitive WHERE clause that does not use group aliasing.</span></span>


```
...WHERE
    FREETEXT("System.ItemNameDisplay",'"computer software"')
    OR
    FREETEXT("System.Title",'"computer software"')
    OR 
    FREETEXT("System.Keywords",'"computer software"')
```



<span data-ttu-id="f8c5b-121">L'esempio precedente può essere semplificato usando un alias di gruppo, come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="f8c5b-121">The preceding example can be simplified by using a group alias, as shown in the following example.</span></span>


```
...WHERE
    WITH("System.ItemNameDisplay","System.Title","System.Keywords")
    AS #Doc-Descriptions
    FREETEXT(#Doc-Descriptions,'"computer software"')
```



<span data-ttu-id="f8c5b-122">Di seguito è riportato un esempio di ponderazione positiva, in cui la proprietà **title** viene assegnata più peso alla determinazione della classificazione relativa.</span><span class="sxs-lookup"><span data-stu-id="f8c5b-122">The following is an example of positive weighting where the **Title** property is given more weight in determining the relative rank.</span></span>


```
...WHERE
    WITH("System.Title":0.8,*:0.5,
         "System.Keywords")
    AS #Doc-Descriptions
    FREETEXT(#Doc-Descriptions,'"computer software"')
```



<span data-ttu-id="f8c5b-123">Di seguito è riportato un esempio di ponderazione negativa in cui la proprietà **title** con peso 0 non viene considerata.</span><span class="sxs-lookup"><span data-stu-id="f8c5b-123">The following is an example of negative weighting where the **Title** property with weight of 0 is not considered.</span></span>


```
...WHERE
    WITH("System.Title":0,*:1.0,
         "System.Keywords")
    AS #Doc-Descriptions
    FREETEXT(#Doc-Descriptions,'"computer software"')
```



## <a name="related-topics"></a><span data-ttu-id="f8c5b-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f8c5b-124">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="f8c5b-125">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="f8c5b-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f8c5b-126">Predicato FREETEXT</span><span class="sxs-lookup"><span data-stu-id="f8c5b-126">FREETEXT Predicate</span></span>](-search-sql-freetext.md)
</dt> <dt>

<span data-ttu-id="f8c5b-127">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="f8c5b-127">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f8c5b-128">Predicati full-text</span><span class="sxs-lookup"><span data-stu-id="f8c5b-128">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)
</dt> <dt>

[<span data-ttu-id="f8c5b-129">Predicati non full-text</span><span class="sxs-lookup"><span data-stu-id="f8c5b-129">Non-Full-Text Predicates</span></span>](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



