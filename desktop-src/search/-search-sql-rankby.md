---
description: I risultati di una query includono sia le righe restituite dalla query sia un valore di pertinenza per ogni riga se la colonna Rank è inclusa nella clausola SELECT.
ms.assetid: 8655eec4-5151-4f82-b485-4dbef947df0d
title: RANGO per clausola
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5de7f7a63e33f43ba6387cbcea44a5f5b5ae8f99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225951"
---
# <a name="rank-by-clause"></a><span data-ttu-id="e0c66-103">RANGO per clausola</span><span class="sxs-lookup"><span data-stu-id="e0c66-103">RANK BY Clause</span></span>

<span data-ttu-id="e0c66-104">I risultati di una query includono sia le righe restituite dalla query sia un valore di pertinenza per ogni riga se la colonna Rank è inclusa nella clausola SELECT.</span><span class="sxs-lookup"><span data-stu-id="e0c66-104">The results from a query include both the rows returned by the query and a rank value for each row if the rank column is included in the SELECT clause.</span></span> <span data-ttu-id="e0c66-105">I valori di pertinenza vengono calcolati dal motore di ricerca e vengono restituiti come numeri interi compresi tra 0 e 1000.</span><span class="sxs-lookup"><span data-stu-id="e0c66-105">The rank values are calculated by the Search engine and are returned as integers in the range zero to 1000.</span></span> <span data-ttu-id="e0c66-106">Per rendere più significativi i risultati della classificazione, la query può controllare il modo in cui i valori di classificazione non elaborati vengono calcolati nella clausola RANK BY.</span><span class="sxs-lookup"><span data-stu-id="e0c66-106">To make the rank results more meaningful, the query can control how raw rank values are calculated in the RANK BY clause.</span></span>

<span data-ttu-id="e0c66-107">Questo argomento è organizzato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="e0c66-107">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="e0c66-108">RANGO per clausola</span><span class="sxs-lookup"><span data-stu-id="e0c66-108">RANK BY Clause</span></span>](#rank-by-clause)
-   [<span data-ttu-id="e0c66-109">WEIGHT (funzione)</span><span class="sxs-lookup"><span data-stu-id="e0c66-109">WEIGHT Function</span></span>](#weight-function)
-   [<span data-ttu-id="e0c66-110">Funzione di COERCIZIONe</span><span class="sxs-lookup"><span data-stu-id="e0c66-110">COERCION Function</span></span>](#coercion-function)

## <a name="rank-by-clause"></a><span data-ttu-id="e0c66-111">RANGO per clausola</span><span class="sxs-lookup"><span data-stu-id="e0c66-111">RANK BY Clause</span></span>

<span data-ttu-id="e0c66-112">La sintassi per la clausola RANK BY è la seguente:</span><span class="sxs-lookup"><span data-stu-id="e0c66-112">The syntax for the RANK BY clause is as follows:</span></span>


```
WHERE ( <search_condition> ) 
RANK BY [ ( ] <rank_specification> [ ) ]
```



<span data-ttu-id="e0c66-113">La clausola RANK BY viene applicata alla condizione di ricerca \_ immediatamente precedente, specificando in modo efficace un rango inferiore o superiore per le righe restituite dalla condizione di ricerca rispetto alle righe restituite da un'altra condizione di ricerca.</span><span class="sxs-lookup"><span data-stu-id="e0c66-113">The RANK BY clause is applied to the search\_condition immediately preceding it, effectively specifying a lower or higher rank for rows returned by that search condition than rows returned by another search condition.</span></span> <span data-ttu-id="e0c66-114">Sono necessarie le parentesi che racchiudono la condizione di ricerca \_ .</span><span class="sxs-lookup"><span data-stu-id="e0c66-114">The parentheses surrounding the search\_condition are required.</span></span> <span data-ttu-id="e0c66-115">Le parentesi che racchiudono la specifica di rango sono facoltative.</span><span class="sxs-lookup"><span data-stu-id="e0c66-115">The parentheses surrounding the rank specification are optional.</span></span>

<span data-ttu-id="e0c66-116">È possibile applicare più di una clausola RANK BY a una singola condizione.</span><span class="sxs-lookup"><span data-stu-id="e0c66-116">More than one RANK BY clause can be applied to a single condition.</span></span> <span data-ttu-id="e0c66-117">È possibile includere clausole ORDER BY aggiuntive una dopo l'altra usando le parentesi.</span><span class="sxs-lookup"><span data-stu-id="e0c66-117">You can include additional RANK BY clauses one after the other using parentheses.</span></span>

> [!Note]  
> <span data-ttu-id="e0c66-118">I predicati full-text restituiscono valori di rango nell'intervallo compreso tra 0 e 1000.</span><span class="sxs-lookup"><span data-stu-id="e0c66-118">Full-text predicates return rank values in the range 0 to 1000.</span></span> <span data-ttu-id="e0c66-119">I valori di pertinenza per tutti i documenti corrispondenti a un predicato non full-text sono 1000.</span><span class="sxs-lookup"><span data-stu-id="e0c66-119">Rank values for all documents matched by a non-full-text predicate are 1000.</span></span> <span data-ttu-id="e0c66-120">Le modifiche ai valori di pertinenza dovrebbero prendere in considerazione queste informazioni.</span><span class="sxs-lookup"><span data-stu-id="e0c66-120">Modifications to the rank values should take this information into account.</span></span>

 

<span data-ttu-id="e0c66-121">La \_ parte relativa alla specifica di rango della clausola RANKBY identifica una o più funzioni da applicare ai valori di rango.</span><span class="sxs-lookup"><span data-stu-id="e0c66-121">The rank\_specification portion of the RANKBY clause identifies one or more functions to apply to the rank values.</span></span> <span data-ttu-id="e0c66-122">La funzione WEIGHT applica un moltiplicatore al valore di classificazione RAW per una riga restituita.</span><span class="sxs-lookup"><span data-stu-id="e0c66-122">The WEIGHT function applies a multiplier to the raw rank value for a returned row.</span></span> <span data-ttu-id="e0c66-123">Minore è il moltiplicatore, minore è il valore di pertinenza risultante.</span><span class="sxs-lookup"><span data-stu-id="e0c66-123">The smaller the multiplier, the lower the resulting rank value.</span></span> <span data-ttu-id="e0c66-124">La funzione di COERCIZIONe può essere utilizzata per moltiplicare, aggiungere o impostare un valore di pertinenza specifico per una riga restituita.</span><span class="sxs-lookup"><span data-stu-id="e0c66-124">The COERCION function can be used to multiply, add to, or set a specific rank value for a returned row.</span></span> <span data-ttu-id="e0c66-125">Ogni specifica di rango può includere una funzione di peso zero o una e zero o più funzioni di COERCIZIONe.</span><span class="sxs-lookup"><span data-stu-id="e0c66-125">Each rank specification can include either zero or one WEIGHT function and zero or more COERCION functions.</span></span> <span data-ttu-id="e0c66-126">Se in una clausola RANK BY sono incluse sia funzioni di PONDERAzione che di COERCIZIONe, la funzione WEIGHT deve essere prima.</span><span class="sxs-lookup"><span data-stu-id="e0c66-126">If both WEIGHT and COERCION functions are included in a RANK BY clause, the WEIGHT function must be first.</span></span>

## <a name="weight-function"></a><span data-ttu-id="e0c66-127">WEIGHT (funzione)</span><span class="sxs-lookup"><span data-stu-id="e0c66-127">WEIGHT Function</span></span>

<span data-ttu-id="e0c66-128">La sintassi della funzione WEIGHT è la seguente:</span><span class="sxs-lookup"><span data-stu-id="e0c66-128">The syntax of the WEIGHT function is:</span></span>


```
WEIGHT ( <weight_multipler> ) 
```



<span data-ttu-id="e0c66-129">Il moltiplicatore deve essere un numero decimale compreso tra 0,001 e 1,000.</span><span class="sxs-lookup"><span data-stu-id="e0c66-129">The multiplier must be a decimal from 0.001 to 1.000.</span></span> <span data-ttu-id="e0c66-130">Il valore di rango non elaborato restituito dal predicato della condizione di ricerca viene moltiplicato per il moltiplicatore di peso per impostare un nuovo valore di pertinenza.</span><span class="sxs-lookup"><span data-stu-id="e0c66-130">The raw rank value returned by the search condition predicate is multiplied by the weight multiplier to set a new rank value.</span></span>

<span data-ttu-id="e0c66-131">Nell'esempio seguente la funzione WEIGHT assegna ai documenti la parola "Theresa" nel System.Document. Campo LastAuthor metà del valore di pertinenza dei documenti con "Theresa" nel campo System. Author:</span><span class="sxs-lookup"><span data-stu-id="e0c66-131">In the following example, the WEIGHT function gives documents with the word "Theresa" in the System.Document.LastAuthor field half the rank value of documents with "Theresa" in the System.Author field:</span></span>


```
WHERE CONTAINS ( System.Author,'"Theresa"' ) 
         RANK BY WEIGHT ( 1.000 )
      OR
      CONTAINS ( System.Document.LastAuthor,'"Theresa"' ) 
         RANK BY WEIGHT ( 0.500 ) 
```



 

> [!Note]  
> <span data-ttu-id="e0c66-132">Le funzionalità di ponderazione delle colonne dei predicati CONTAINs e FREETEXT supportano un formato abbreviato utilizzando i due punti tra il termine di ricerca e il moltiplicatore ("software": 0,25).</span><span class="sxs-lookup"><span data-stu-id="e0c66-132">The CONTAINS and FREETEXT predicate column weighting features support a shorthand format using a colon between the search term and the multiplier ("software":0.25).</span></span> <span data-ttu-id="e0c66-133">La clausola RANK BY non supporta il formato abbreviato.</span><span class="sxs-lookup"><span data-stu-id="e0c66-133">The RANK BY clause does not support the shortened form.</span></span>

 

<span data-ttu-id="e0c66-134">Esiste una limitazione quando si usa RANK BY WEIGHT: non funziona con le clausole CONTAINs che usano condizioni booleane; ad esempio, l'esempio seguente non è consentito:</span><span class="sxs-lookup"><span data-stu-id="e0c66-134">There is a limitation when using RANK BY WEIGHT: it does not work with CONTAINS clauses that use Boolean conditions; for example, the following example is not permitted:</span></span>


```
CONTAINS ( System.Author,'"Theresa" OR "Teresa"' ) RANK BY WEIGHT ( 0.400 )
```



## <a name="coercion-function"></a><span data-ttu-id="e0c66-135">Funzione di COERCIZIONe</span><span class="sxs-lookup"><span data-stu-id="e0c66-135">COERCION Function</span></span>

<span data-ttu-id="e0c66-136">La funzione di coercizione Rank può essere usata per modificare il valore di pertinenza restituito per addizione o moltiplicazione oppure assegnando un valore specifico.</span><span class="sxs-lookup"><span data-stu-id="e0c66-136">The rank coercion function can be used to change the returned rank value by addition or multiplication or by assigning it a specific value.</span></span>

<span data-ttu-id="e0c66-137">La sintassi della funzione di COERCIZIONe è la seguente:</span><span class="sxs-lookup"><span data-stu-id="e0c66-137">The syntax of the COERCION function is:</span></span>


```
COERCION ( <coercion_operation> , <coercion_value> )
```



<span data-ttu-id="e0c66-138">Il valore di coercizione è un valore intero.</span><span class="sxs-lookup"><span data-stu-id="e0c66-138">The coercion value is an integer value.</span></span>

<span data-ttu-id="e0c66-139">Nella tabella seguente vengono descritte le impostazioni dell'operazione di coercizione disponibili.</span><span class="sxs-lookup"><span data-stu-id="e0c66-139">The following table describes the available coercion operation settings.</span></span>



| <span data-ttu-id="e0c66-140">Operazione di coercizione</span><span class="sxs-lookup"><span data-stu-id="e0c66-140">Coercion operation</span></span> | <span data-ttu-id="e0c66-141">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e0c66-141">Description</span></span>                                                                                    | <span data-ttu-id="e0c66-142">Intervallo di valori</span><span class="sxs-lookup"><span data-stu-id="e0c66-142">Value range</span></span>  |
|--------------------|------------------------------------------------------------------------------------------------|--------------|
| <span data-ttu-id="e0c66-143">ABSOLUTE</span><span class="sxs-lookup"><span data-stu-id="e0c66-143">ABSOLUTE</span></span>           | <span data-ttu-id="e0c66-144">Il valore di pertinenza restituito è il valore specificato nel valore di coercizione.</span><span class="sxs-lookup"><span data-stu-id="e0c66-144">The rank value returned is the value specified in the coercion value.</span></span>                          | <span data-ttu-id="e0c66-145">da 0 a 1000</span><span class="sxs-lookup"><span data-stu-id="e0c66-145">0 to 1000</span></span>    |
| <span data-ttu-id="e0c66-146">ADD</span><span class="sxs-lookup"><span data-stu-id="e0c66-146">ADD</span></span>                | <span data-ttu-id="e0c66-147">Il valore di pertinenza restituito è la somma del valore di rango non elaborato e del valore di coercizione specificato.</span><span class="sxs-lookup"><span data-stu-id="e0c66-147">The rank value returned is the sum of the raw rank value and the specified coercion value.</span></span>     | <span data-ttu-id="e0c66-148">da 0,001 a 1,0</span><span class="sxs-lookup"><span data-stu-id="e0c66-148">0.001 to 1.0</span></span> |
| <span data-ttu-id="e0c66-149">Moltiplicazione</span><span class="sxs-lookup"><span data-stu-id="e0c66-149">MULTIPLY</span></span>           | <span data-ttu-id="e0c66-150">Il valore di pertinenza restituito è il prodotto del valore di classificazione non elaborato e il valore di coercizione specificato.</span><span class="sxs-lookup"><span data-stu-id="e0c66-150">The rank value returned is the product of the raw rank value and the specified coercion value.</span></span> | <span data-ttu-id="e0c66-151">da 0,001 a 1,0</span><span class="sxs-lookup"><span data-stu-id="e0c66-151">0.001 to 1.0</span></span> |



 

 

> [!IMPORTANT]
> <span data-ttu-id="e0c66-152">La ricerca può restituire valori di rango solo nell'intervallo compreso tra 0 e 1000.</span><span class="sxs-lookup"><span data-stu-id="e0c66-152">Search can return rank values only in the range of 0 to 1000.</span></span>

 

 

<span data-ttu-id="e0c66-153">Nell'esempio seguente viene usata la funzione di COERCIZIONe per impostare tutti i documenti con "computer" nel titolo per avere un rango di 1000, riducendo di un trimestre il rango dei documenti che contengono sia "computer" che "software" nel titolo.</span><span class="sxs-lookup"><span data-stu-id="e0c66-153">The following example uses the COERCION function to set all documents with "computer" in the title to have a rank of 1000, while reducing by one-quarter the rank of documents containing both "computer" and "software" in the title.</span></span>


```
WHERE CONTAINS ( System.Title, 'computer' )
        RANK BY COERCION ( ABSOLUTE , 1000 )
        OR 
       CONTAINS ( System.Title, '"computer" AND "software"' )
        RANK BY COERCION ( MULTIPLY, 0.750 ) 
```



 

 



