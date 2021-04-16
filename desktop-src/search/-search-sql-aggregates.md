---
description: Una funzione di aggregazione esegue un calcolo su un set di valori e restituisce un valore. In questo modo è possibile generare statistiche di riepilogo per i gruppi a più livelli con un sovraccarico ridotto.
ms.assetid: 82a93f57-8273-45bf-81d7-50a673845ae1
title: Funzioni di aggregazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da68ad1104c93e8ae04f7ec37cbbde5020109336
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104562917"
---
# <a name="aggregate-functions"></a><span data-ttu-id="bef78-104">Funzioni di aggregazione</span><span class="sxs-lookup"><span data-stu-id="bef78-104">Aggregate Functions</span></span>

<span data-ttu-id="bef78-105">Una funzione di aggregazione esegue un calcolo su un set di valori e restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="bef78-105">An aggregate function performs a calculation on a set of values and returns a value.</span></span> <span data-ttu-id="bef78-106">In questo modo è possibile generare statistiche di riepilogo per i gruppi a più livelli con un sovraccarico ridotto.</span><span class="sxs-lookup"><span data-stu-id="bef78-106">Doing so makes it possible to generate summary statistics for multi-level groups with little overhead.</span></span>

## <a name="about-aggregate-functions"></a><span data-ttu-id="bef78-107">Informazioni sulle funzioni di aggregazione</span><span class="sxs-lookup"><span data-stu-id="bef78-107">About Aggregate Functions</span></span>

<span data-ttu-id="bef78-108">Le funzioni di aggregazione in Windows Search Structured Query Language (SQL) hanno la sintassi seguente:</span><span class="sxs-lookup"><span data-stu-id="bef78-108">Aggregate functions in Windows Search Structured Query Language (SQL) have the following syntax:</span></span>


```
AGGREGATE <function> [AS <label>] [,<function> [AS <label>]]*
```



<span data-ttu-id="bef78-109">La parte della funzione può includere le funzioni e la sintassi seguenti:</span><span class="sxs-lookup"><span data-stu-id="bef78-109">The function portion can include any of the following functions and syntax:</span></span>



| <span data-ttu-id="bef78-110">Funzione</span><span class="sxs-lookup"><span data-stu-id="bef78-110">Function</span></span>                                                              | <span data-ttu-id="bef78-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bef78-111">Description</span></span>                                                                                                                                                                                                 |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bef78-112">AVG ( <column> )</span><span class="sxs-lookup"><span data-stu-id="bef78-112">AVG(<column>)</span></span>                                                   | <span data-ttu-id="bef78-113">Restituisce la media dei valori in un gruppo.</span><span class="sxs-lookup"><span data-stu-id="bef78-113">Returns the average of the values in a group.</span></span> <span data-ttu-id="bef78-114">Si applica solo ai numeri.</span><span class="sxs-lookup"><span data-stu-id="bef78-114">Applies only to numbers.</span></span>                                                                                                                                      |
| <span data-ttu-id="bef78-115">BYFREQUENCY ( <column> , <N> )</span><span class="sxs-lookup"><span data-stu-id="bef78-115">BYFREQUENCY(<column>, <N>)</span></span>                                | <span data-ttu-id="bef78-116">Restituisce i valori di colonna N più frequenti dai risultati nel gruppo.</span><span class="sxs-lookup"><span data-stu-id="bef78-116">Returns the most frequent N column values from the results in the group.</span></span> <span data-ttu-id="bef78-117">Include inoltre un conteggio del numero di volte in cui ogni valore si è verificato e degli identificatori del documento per i risultati che contengono ogni valore restituito.</span><span class="sxs-lookup"><span data-stu-id="bef78-117">Also includes a count of how many times each value occurred and document identifiers for results that contain each returned value.</span></span> |
| <span data-ttu-id="bef78-118">CHILDCOUNT ()</span><span class="sxs-lookup"><span data-stu-id="bef78-118">CHILDCOUNT()</span></span>                                                          | <span data-ttu-id="bef78-119">Restituisce il numero di elementi in un gruppo (esclusi i sottogruppi).</span><span class="sxs-lookup"><span data-stu-id="bef78-119">Returns the number of items in a group (excluding subgroups).</span></span> <span data-ttu-id="bef78-120">Se sono presenti più livelli di raggruppamento, restituisce il numero di gruppi figlio immediati.</span><span class="sxs-lookup"><span data-stu-id="bef78-120">If there are multiple levels of grouping, this returns the number of immediate child groups.</span></span>                                                  |
| <span data-ttu-id="bef78-121">CONTEGGIO ()</span><span class="sxs-lookup"><span data-stu-id="bef78-121">COUNT()</span></span>                                                               | <span data-ttu-id="bef78-122">Restituisce il numero di elementi in un gruppo e in tutti i sottogruppi.</span><span class="sxs-lookup"><span data-stu-id="bef78-122">Returns the number of items in a group and all subgroups.</span></span>                                                                                                                                                   |
| <span data-ttu-id="bef78-123">DATERANGE ( <column> )</span><span class="sxs-lookup"><span data-stu-id="bef78-123">DATERANGE(<column>)</span></span>                                             | <span data-ttu-id="bef78-124">Restituisce i limiti inferiore e superiore dei valori di colonna trovati nel gruppo di risultati del gruppo.</span><span class="sxs-lookup"><span data-stu-id="bef78-124">Returns the lower and upper bounds of the column values found in the group results group.</span></span> <span data-ttu-id="bef78-125">Valido solo per le proprietà FILETIME.</span><span class="sxs-lookup"><span data-stu-id="bef78-125">Valid only for filetime properties.</span></span>                                                                               |
| <span data-ttu-id="bef78-126">PRIMO ( <column> , <N> )</span><span class="sxs-lookup"><span data-stu-id="bef78-126">FIRST(<column>, <N>)</span></span>                                      | <span data-ttu-id="bef78-127">Restituisce i primi valori di colonna N dai risultati foglia trovati in un gruppo.</span><span class="sxs-lookup"><span data-stu-id="bef78-127">Returns the first N column values from leaf results found in a group.</span></span>                                                                                                                                       |
| <span data-ttu-id="bef78-128">MAX ( <column> )</span><span class="sxs-lookup"><span data-stu-id="bef78-128">MAX(<column>)</span></span>                                                   | <span data-ttu-id="bef78-129">Restituisce il valore massimo dell'espressione.</span><span class="sxs-lookup"><span data-stu-id="bef78-129">Returns the maximum value in the expression.</span></span> <span data-ttu-id="bef78-130">Si applica solo a numeri o date.</span><span class="sxs-lookup"><span data-stu-id="bef78-130">Applies only to numbers or dates.</span></span>                                                                                                                              |
| <span data-ttu-id="bef78-131">MIN ( <column> )</span><span class="sxs-lookup"><span data-stu-id="bef78-131">MIN(<column>)</span></span>                                                   | <span data-ttu-id="bef78-132">Restituisce il valore minimo nell'espressione.</span><span class="sxs-lookup"><span data-stu-id="bef78-132">Returns the minimum value in the expression.</span></span> <span data-ttu-id="bef78-133">Si applica solo a numeri o date.</span><span class="sxs-lookup"><span data-stu-id="bef78-133">Applies only to numbers or dates.</span></span>                                                                                                                              |
| <span data-ttu-id="bef78-134">REPRESENTATIVEOF ( <column> , <idRepresentative> , <N> )</span><span class="sxs-lookup"><span data-stu-id="bef78-134">REPRESENTATIVEOF(<column>, <idRepresentative>, <N>)</span></span> | <span data-ttu-id="bef78-135">Restituisce N valori idRepresentative, ognuno selezionato da uno dei subset di risultati con un valore di colonna univoco.</span><span class="sxs-lookup"><span data-stu-id="bef78-135">Returns N idRepresentative values, each selected from one of the result subsets that has a unique column value.</span></span> <span data-ttu-id="bef78-136">Ogni valore viene restituito anche con un identificatore del documento con il valore idRepresentative.</span><span class="sxs-lookup"><span data-stu-id="bef78-136">Each value is also returned with a document identifier that has the idRepresentative value.</span></span> |
| <span data-ttu-id="bef78-137">SUM ( <column> )</span><span class="sxs-lookup"><span data-stu-id="bef78-137">SUM(<column>)</span></span>                                                   | <span data-ttu-id="bef78-138">Restituisce la somma dei valori in un gruppo.</span><span class="sxs-lookup"><span data-stu-id="bef78-138">Returns the sum of the values in a group.</span></span> <span data-ttu-id="bef78-139">Si applica solo ai numeri.</span><span class="sxs-lookup"><span data-stu-id="bef78-139">Applies only to numbers.</span></span>                                                                                                                                          |



 

 

> [!Note]  
> <span data-ttu-id="bef78-140">Le aggregazioni vengono restituite come singole colonne.</span><span class="sxs-lookup"><span data-stu-id="bef78-140">Aggregates are returned as individual columns.</span></span> <span data-ttu-id="bef78-141">Sono principalmente tipi semplici, ad eccezione di ByFrequency, First, DateRange e RepresentativeOf, che vengono restituiti come tipi composti.</span><span class="sxs-lookup"><span data-stu-id="bef78-141">They are mostly simple types except for ByFrequency, First, DateRange, and RepresentativeOf which are returned as compound types.</span></span>

 

<span data-ttu-id="bef78-142">È possibile utilizzare qualsiasi colonna numerica o data per le aggregazioni e non solo quelle presenti nella clausola SELECT.</span><span class="sxs-lookup"><span data-stu-id="bef78-142">You can use any numeric or date column for aggregations, and not only those that are in the SELECT clause.</span></span> <span data-ttu-id="bef78-143">Tuttavia, non è possibile raggruppare le aggregazioni.</span><span class="sxs-lookup"><span data-stu-id="bef78-143">However, you cannot group on aggregates.</span></span> <span data-ttu-id="bef78-144">Se l'argomento della colonna passato non è un tipo numerico o di data, viene restituito un errore di sintassi.</span><span class="sxs-lookup"><span data-stu-id="bef78-144">A syntax error is returned if the column argument passed in is not either a numeric or date type.</span></span>

<span data-ttu-id="bef78-145">La parte dell'etichetta è facoltativa e fornisce un alias più leggibile per l'etichetta.</span><span class="sxs-lookup"><span data-stu-id="bef78-145">The label portion is optional and provides a more readable alias for the label.</span></span> <span data-ttu-id="bef78-146">Se non si include un'etichetta alias, Windows Search trasforma il nome della funzione e della colonna in un'etichetta.</span><span class="sxs-lookup"><span data-stu-id="bef78-146">If you do not include an alias label, then Windows Search transforms the function and column name into a label.</span></span> <span data-ttu-id="bef78-147">Ad esempio, MAX (System.Document. WordCount) diventa il numero massimo di \_ SystemDocumentWordCount.</span><span class="sxs-lookup"><span data-stu-id="bef78-147">For example, MAX(System.Document.WordCount) becomes MAX\_SystemDocumentWordCount.</span></span>

## <a name="multi-level-groups-and-counting"></a><span data-ttu-id="bef78-148">Gruppi e conteggio a più livelli</span><span class="sxs-lookup"><span data-stu-id="bef78-148">Multi-level Groups and Counting</span></span>

<span data-ttu-id="bef78-149">Le aggregazioni sono definite sulle foglie e vengono duplicate.</span><span class="sxs-lookup"><span data-stu-id="bef78-149">Aggregates are defined over leaves and are duplicated.</span></span> <span data-ttu-id="bef78-150">Un'aggregazione accetta come input le foglie del gruppo che lo definisce (Documents), anziché i sottogruppi dei relativi elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="bef78-150">An aggregate takes as input the leaves of the group that defines it (documents), rather than the subgroups of its children.</span></span> <span data-ttu-id="bef78-151">Questa funzionalità viene definita raggruppamento a più livelli.</span><span class="sxs-lookup"><span data-stu-id="bef78-151">This functionality is referred to as multi-level grouping.</span></span>

<span data-ttu-id="bef78-152">Oltre ad aggregazioni definite su foglie e duplicate, vengono conteggiate una sola volta.</span><span class="sxs-lookup"><span data-stu-id="bef78-152">In addition to aggregates being defined over leaves and duplicated, they are counted only once.</span></span> <span data-ttu-id="bef78-153">Sebbene lo stesso documento possa essere rappresentato più volte in un gruppo, le aggregazioni lo considerano una sola volta.</span><span class="sxs-lookup"><span data-stu-id="bef78-153">While the same document might be represented multiple times under one group, aggregates would only consider it once.</span></span> <span data-ttu-id="bef78-154">Questo concetto è illustrato nell'immagine seguente.</span><span class="sxs-lookup"><span data-stu-id="bef78-154">The following graphic illustrates this concept.</span></span>

![diagramma che mostra che le aggregazioni sono definite sulle foglie e duplicate e vengono conteggiate una sola volta](images/aggregates.png)

## <a name="aggregate-examples"></a><span data-ttu-id="bef78-156">Esempi di aggregazione</span><span class="sxs-lookup"><span data-stu-id="bef78-156">Aggregate Examples</span></span>

<span data-ttu-id="bef78-157">Di seguito sono riportati esempi di funzioni di aggregazione all'interno della clausola GROUP ON:</span><span class="sxs-lookup"><span data-stu-id="bef78-157">The following are examples of aggregate functions within the GROUP ON clause:</span></span>


```
GROUP ON System.Sender ['d','m','r'] 
    AGGREGATE COUNT() as 'Total',
              MAX(System.Size) as 'Max Size',
              MIN(System.Size) as 'Min Size'
    OVER (SELECT System.Subject FROM systemindex)
              
GROUP ON System.Sender ['d', 'm', 'r']
      AGGREGATE MAX(System.Search.Rank) as 'MaxRank', 
                MIN(System.Search.Rank) as 'MinRank'
      OVER (GROUP ON system.conversationID
                  OVER (SELECT workid, System.ItemUrl FROM systemindex
                        WHERE CONTAINS (*, 'sometext')
                        ORDER BY System.DateCreated))
               
GROUP ON System.FileName [before('a'),before('z')] 
      AGGREGATE MAX(System.Size) as 'maxsize', MIN(System.Size) as 'MinSize' 
      OVER (SELECT System.FileName FROM systemindex
            ORDER BY System.FileName)      
            
GROUP ON System.author 
      AGGREGATE MAX(System.size) as 'maxsize' 
      ORDER BY min(System.Size) 
      OVER (GROUP ON System.DateCreated 
                  AGGREGATE Count() 
                  ORDER BY MAX(System.size) 
                  OVER (SELECT filename, System.DateCreated, System.Size FROM systemindex
                        WHERE CONTAINS('text')))
```



## <a name="return-value"></a><span data-ttu-id="bef78-158">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bef78-158">Return Value</span></span>

<span data-ttu-id="bef78-159">Il valore restituito è un VARIANT trovato nel set di righe come proprietà personalizzata, come alias specificati o come "aggregazioni" se non è specificata alcuna etichetta alias.</span><span class="sxs-lookup"><span data-stu-id="bef78-159">The return value is a variant found on the rowset as a custom property, either as the specified aliases or as "Aggregates" if no alias label is specified.</span></span>

 

 



