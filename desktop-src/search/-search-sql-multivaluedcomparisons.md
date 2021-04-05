---
description: Le colonne archiviate nell'indice di contenuto possono avere più valori e le colonne multivalore possono essere confrontate tramite il predicato di confronto della matrice.
ms.assetid: bc3de1bd-b833-459d-81a3-c6b08314e26f
title: Confronti multivalore (matrice)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77710ecdddcf289c9a5c64d0c5f57ca449311097
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750375"
---
# <a name="multi-valued-array-comparisons"></a><span data-ttu-id="8d8d2-103">Confronti multivalore (matrice)</span><span class="sxs-lookup"><span data-stu-id="8d8d2-103">Multi-Valued (ARRAY) Comparisons</span></span>

<span data-ttu-id="8d8d2-104">Le colonne archiviate nell'indice di contenuto possono avere più valori e le colonne multivalore possono essere confrontate tramite il predicato di confronto della matrice.</span><span class="sxs-lookup"><span data-stu-id="8d8d2-104">Columns stored in the content index can have multiple values, and those multivalued columns can be compared by using the ARRAY comparison predicate.</span></span>

<span data-ttu-id="8d8d2-105">Il predicato di confronto della matrice presenta la sintassi seguente:</span><span class="sxs-lookup"><span data-stu-id="8d8d2-105">The ARRAY comparison predicate has the following syntax:</span></span>


```
...WHERE <column> <comp_op> [<quantifier>] <comparison_list>
                
...WHERE <column> <comp_op> <value>
```



<span data-ttu-id="8d8d2-106">Se il riferimento alla colonna non è una colonna multivalore, viene restituito un errore.</span><span class="sxs-lookup"><span data-stu-id="8d8d2-106">An error is returned if the column reference is not a multivalued column.</span></span> <span data-ttu-id="8d8d2-107">Il tipo di dati della colonna deve essere compatibile con gli elementi dell'elenco di confronto.</span><span class="sxs-lookup"><span data-stu-id="8d8d2-107">The column data type must be compatible with the elements of the comparison list.</span></span> <span data-ttu-id="8d8d2-108">Se necessario, è possibile [eseguire il cast](-search-sql-castingdatacolumntype.md) del riferimento di colonna come un altro tipo di dati.</span><span class="sxs-lookup"><span data-stu-id="8d8d2-108">If necessary, the column reference can be [cast](-search-sql-castingdatacolumntype.md) as another data type.</span></span>

<span data-ttu-id="8d8d2-109">L'operatore di confronto (comp \_ op) può essere uno qualsiasi degli operatori di confronto normali.</span><span class="sxs-lookup"><span data-stu-id="8d8d2-109">The comparison operator (comp\_op) can be any of the normal comparison operators.</span></span> <span data-ttu-id="8d8d2-110">In un confronto multivalore, gli operatori di confronto hanno significati leggermente diversi a seconda che si utilizzi un quantificatore.</span><span class="sxs-lookup"><span data-stu-id="8d8d2-110">In a multivalued comparison, the comparison operators have slightly different meanings depending on whether a quantifier is used.</span></span> <span data-ttu-id="8d8d2-111">I quantificatori identificano se è necessario eseguire un confronto in base a tutti o solo alcuni dei valori nell'elenco di confronto.</span><span class="sxs-lookup"><span data-stu-id="8d8d2-111">Quantifiers identify whether a comparison should be made against all or some of the values in the comparison list.</span></span> <span data-ttu-id="8d8d2-112">Le funzioni degli operatori di confronto sono fornite nelle tabelle che descrivono ogni quantificatore (tutti e alcuni) più avanti in questo documento.</span><span class="sxs-lookup"><span data-stu-id="8d8d2-112">The functions of the comparison operators are given in the tables describing each quantifier (ALL and SOME) later in this document.</span></span>

<span data-ttu-id="8d8d2-113">Il valore dopo l'operatore specifica un singolo valore letterale che viene confrontato con tutti gli elementi della colonna multivalore.</span><span class="sxs-lookup"><span data-stu-id="8d8d2-113">The value after the operator specifies a single literal value that is compared against all elements of the multivalued column.</span></span> <span data-ttu-id="8d8d2-114">Se un elemento corrisponde al valore, il predicato è true.</span><span class="sxs-lookup"><span data-stu-id="8d8d2-114">If any element matches the value, the predicate is true.</span></span>

<span data-ttu-id="8d8d2-115">Nell'elenco di confronto viene specificata una matrice di valori letterali confrontati con la colonna multivalore.</span><span class="sxs-lookup"><span data-stu-id="8d8d2-115">The comparison list specifies an array of literal values that are compared against the multivalued column.</span></span> <span data-ttu-id="8d8d2-116">Di seguito è riportata la sintassi per l'elenco di confronto:</span><span class="sxs-lookup"><span data-stu-id="8d8d2-116">The syntax for the comparison list follows:</span></span>


```
ARRAY '['<literal> [,<literal>]']'
```



> [!IMPORTANT]
> <span data-ttu-id="8d8d2-117">Tenere presente la sintassi dell'elenco di confronto.</span><span class="sxs-lookup"><span data-stu-id="8d8d2-117">Be aware of the comparison list syntax.</span></span> <span data-ttu-id="8d8d2-118">Il gruppo di valori letterali che costituiscono l'elenco di confronto deve essere racchiuso tra parentesi quadre.</span><span class="sxs-lookup"><span data-stu-id="8d8d2-118">The group of literals that make up the comparison list must be surrounded by square brackets.</span></span> <span data-ttu-id="8d8d2-119">Non racchiudere i singoli elementi dell'elenco di confronto tra parentesi quadre.</span><span class="sxs-lookup"><span data-stu-id="8d8d2-119">Do not surround individual elements of the comparison list by square brackets.</span></span> <span data-ttu-id="8d8d2-120">Pertanto, ARRAY \[ 1 \] e Array 1 \[ , 2, 3 \] sono validi, ma \[ la matrice 1 \[ , 2 \] \[ , 3 non lo \] \] è.</span><span class="sxs-lookup"><span data-stu-id="8d8d2-120">Therefore, ARRAY \[1\] and ARRAY \[1,2,3\] are valid, but ARRAY \[1\[,2\]\[,3\]\] is not.</span></span>

 

<span data-ttu-id="8d8d2-121">Il metodo utilizzato per determinare se il confronto multivalore restituisce true o false viene specificato dal quantificatore facoltativo.</span><span class="sxs-lookup"><span data-stu-id="8d8d2-121">The method used to determine whether the multivalued comparison returns true or false is specified by the optional quantifier.</span></span> <span data-ttu-id="8d8d2-122">Le sezioni seguenti descrivono ogni quantificatore e come funziona ogni operatore di confronto quando viene usato il quantificatore.</span><span class="sxs-lookup"><span data-stu-id="8d8d2-122">The following sections describe each quantifier, and how each comparison operator works when the quantifier is used.</span></span>

## <a name="absent-quantifier"></a><span data-ttu-id="8d8d2-123">Quantificatore assente</span><span class="sxs-lookup"><span data-stu-id="8d8d2-123">Absent Quantifier</span></span>

<span data-ttu-id="8d8d2-124">Se non viene specificato alcun quantificatore, ogni elemento sul lato sinistro del confronto viene confrontato con l'elemento nella stessa posizione sul lato destro.</span><span class="sxs-lookup"><span data-stu-id="8d8d2-124">If no quantifier is specified, each element on the left side of the comparison is compared to the element in the same position on the right side.</span></span> <span data-ttu-id="8d8d2-125">Il confronto inizia con il primo elemento nelle matrici e avanza nell'ultimo elemento.</span><span class="sxs-lookup"><span data-stu-id="8d8d2-125">The comparison begins with the first element in the arrays, and progresses through the last element.</span></span> <span data-ttu-id="8d8d2-126">Se tutti gli elementi sul lato sinistro sono equivalenti agli elementi corrispondenti sul lato destro, il numero di elementi della matrice viene usato per determinare quale matrice è maggiore.</span><span class="sxs-lookup"><span data-stu-id="8d8d2-126">If all the elements on the left side are equivalent to the corresponding elements on the right side, the number of array elements is used to determine which array is greater.</span></span>

<span data-ttu-id="8d8d2-127">Nella tabella seguente viene illustrato il funzionamento degli operatori di confronto quando non è specificato alcun quantificatore e viene fornita una breve descrizione di ciascuno di essi.</span><span class="sxs-lookup"><span data-stu-id="8d8d2-127">The following table shows the operation of the comparison operators when no quantifier is specified and provides a brief description of each.</span></span>



| <span data-ttu-id="8d8d2-128">Operatore</span><span class="sxs-lookup"><span data-stu-id="8d8d2-128">Operator</span></span>       | <span data-ttu-id="8d8d2-129">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8d8d2-129">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| =              | <span data-ttu-id="8d8d2-130">' Equal to ' restituisce true quando ogni elemento di sinistra ha lo stesso valore dell'elemento a destra corrispondente e entrambe le matrici hanno lo stesso numero di elementi.</span><span class="sxs-lookup"><span data-stu-id="8d8d2-130">'Equal to' returns true when each left-side element has the same value as the corresponding right-side element, and both arrays have the same number of elements.</span></span>                                                                                                                                                                                                                     |
| <span data-ttu-id="8d8d2-131">! = o <></span><span class="sxs-lookup"><span data-stu-id="8d8d2-131">!= or <></span></span> | <span data-ttu-id="8d8d2-132">' Diverso da' restituisce true quando uno o più elementi di sinistra hanno valori diversi dagli elementi a destra corrispondenti o quando le matrici di sinistra e di destra non hanno lo stesso numero di elementi.</span><span class="sxs-lookup"><span data-stu-id="8d8d2-132">'Not equal to' returns true when one or more left-side elements have values that differ from the corresponding right-side elements, or when the left-side and right-side arrays do not have the same number of elements.</span></span>                                                                                                                                                              |
| >           | <span data-ttu-id="8d8d2-133">' Maggiore di ' restituisce true quando il valore di ogni elemento di sinistra è maggiore del valore dell'elemento a destra corrispondente.</span><span class="sxs-lookup"><span data-stu-id="8d8d2-133">'Greater than' returns true when the value of each left-side element is greater than the value of the corresponding right-side element.</span></span> <span data-ttu-id="8d8d2-134">Se tutti i valori degli elementi a sinistra corrispondono esattamente ai corrispondenti elementi a destra e la matrice di sinistra contiene più elementi rispetto alla matrice di destra,' maggiore di ' restituisce true.</span><span class="sxs-lookup"><span data-stu-id="8d8d2-134">If all the left-side element values exactly match the corresponding right-side elements and the left-side array has more elements than the right-side array, 'greater than' returns true.</span></span>                                                     |
| >=          | <span data-ttu-id="8d8d2-135">' Maggiore o uguale a' restituisce true quando il valore di ogni elemento di sinistra è maggiore o uguale al valore dell'elemento a destra corrispondente.</span><span class="sxs-lookup"><span data-stu-id="8d8d2-135">'Greater than or equal to' returns true when the value of every left-side element is greater than or equal to the value of the corresponding right-side element.</span></span> <span data-ttu-id="8d8d2-136">Se tutti i valori degli elementi a sinistra sono uguali o maggiori dei corrispondenti elementi a destra e la matrice di sinistra ha gli stessi o più elementi della matrice di destra,' maggiore di ' restituisce true.</span><span class="sxs-lookup"><span data-stu-id="8d8d2-136">If all the left-side element values are equal to or greater than the corresponding right-side elements and the left-side array has the same or more elements than the right-side array, 'greater than' returns true.</span></span> |
| <           | <span data-ttu-id="8d8d2-137">' Less than ' restituisce true quando il valore di ogni elemento di sinistra è minore del valore dell'elemento a destra corrispondente.</span><span class="sxs-lookup"><span data-stu-id="8d8d2-137">'Less than' returns true when the value of each left-side element is less than the value of the corresponding right-side element.</span></span> <span data-ttu-id="8d8d2-138">' Minor di ' restituisce anche true quando il lato sinistro ha meno elementi del lato destro.</span><span class="sxs-lookup"><span data-stu-id="8d8d2-138">'Less than' also returns true when the left-side side has fewer elements than the right-side side.</span></span>                                                                                                                                                  |
| <=          | <span data-ttu-id="8d8d2-139">' Minore o uguale a' restituisce true quando il valore di ogni elemento di sinistra è minore o uguale al valore dell'elemento a destra corrispondente.</span><span class="sxs-lookup"><span data-stu-id="8d8d2-139">'Less than or equal to' returns true when the value of every left-side element is less than or equal to the value of the corresponding right-side element.</span></span> <span data-ttu-id="8d8d2-140">Se tutti i valori degli elementi a sinistra sono uguali o minori degli elementi di destra corrispondenti e la matrice di sinistra ha lo stesso o meno elementi della matrice di destra,' maggiore di ' restituisce true.</span><span class="sxs-lookup"><span data-stu-id="8d8d2-140">If all the left-side element values are equal to or less than the corresponding right-side elements and the left-side array has the same or fewer elements than the right-side array, 'greater than' returns true.</span></span>         |



 

## <a name="all-quantifier"></a><span data-ttu-id="8d8d2-141">TUTTI i quantificatori</span><span class="sxs-lookup"><span data-stu-id="8d8d2-141">ALL Quantifier</span></span>

<span data-ttu-id="8d8d2-142">Il quantificatore ALL specifica che ogni elemento sul lato sinistro viene confrontato con ogni elemento sul lato destro.</span><span class="sxs-lookup"><span data-stu-id="8d8d2-142">The ALL quantifier specifies that each element in the left side is compared against every element on the right side.</span></span> <span data-ttu-id="8d8d2-143">Per restituire true, il confronto deve essere true per ogni elemento sul lato sinistro rispetto a ogni elemento sul lato destro.</span><span class="sxs-lookup"><span data-stu-id="8d8d2-143">To return true, the comparison must be true for each element on the left side when compared to every element on the right side.</span></span> <span data-ttu-id="8d8d2-144">Il numero di elementi nei lati della matrice sinistra e destra non ha alcun effetto sul risultato.</span><span class="sxs-lookup"><span data-stu-id="8d8d2-144">The number of elements in the left and right array sides has no effect on the result.</span></span>

<span data-ttu-id="8d8d2-145">Nella tabella seguente viene illustrato il funzionamento di ogni operatore di confronto con il quantificatore ALL.</span><span class="sxs-lookup"><span data-stu-id="8d8d2-145">The following table shows how each comparison operator functions with the ALL quantifier.</span></span>



| <span data-ttu-id="8d8d2-146">Operatore</span><span class="sxs-lookup"><span data-stu-id="8d8d2-146">Operator</span></span>       | <span data-ttu-id="8d8d2-147">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8d8d2-147">Description</span></span>                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------|
| =              | <span data-ttu-id="8d8d2-148">' Equal to ' restituisce true quando ogni valore dell'elemento di sinistra è uguale a ogni valore di elemento a destra.</span><span class="sxs-lookup"><span data-stu-id="8d8d2-148">'Equal to' returns true when each left-side element value is the same as every right-side element value.</span></span>                              |
| <span data-ttu-id="8d8d2-149">! = o <></span><span class="sxs-lookup"><span data-stu-id="8d8d2-149">!= or <></span></span> | <span data-ttu-id="8d8d2-150">' Diverso da' restituisce true quando almeno uno dei valori degli elementi a sinistra è diverso da uno qualsiasi dei valori degli elementi a destra.</span><span class="sxs-lookup"><span data-stu-id="8d8d2-150">'Not equal to' returns true when at least one of the left-side element values is different from any of the right-side element values.</span></span> |
| >           | <span data-ttu-id="8d8d2-151">' Maggiore di ' restituisce true quando ogni valore dell'elemento di sinistra è maggiore di ogni valore di elemento a destra.</span><span class="sxs-lookup"><span data-stu-id="8d8d2-151">'Greater than' returns true when each left-side element value is greater than every right-side element value.</span></span>                         |
| >=          | <span data-ttu-id="8d8d2-152">' Maggiore o uguale a' restituisce true quando ogni valore dell'elemento di sinistra è maggiore o uguale a ogni valore di elemento a destra.</span><span class="sxs-lookup"><span data-stu-id="8d8d2-152">'Greater than or equal to' returns true when each left-side element value is greater than or equal to every right-side element value.</span></span> |
| <           | <span data-ttu-id="8d8d2-153">' Less than ' restituisce true quando ogni valore dell'elemento di sinistra è minore di ogni valore di elemento a destra.</span><span class="sxs-lookup"><span data-stu-id="8d8d2-153">'Less than' returns true when each left-side element value is less than every right-side element value.</span></span>                               |
| <=          | <span data-ttu-id="8d8d2-154">' Minore o uguale a' restituisce true quando ogni valore dell'elemento di sinistra è minore o uguale a ogni valore di elemento a destra.</span><span class="sxs-lookup"><span data-stu-id="8d8d2-154">'Less than or equal to' returns true when each left-side element value is less than or equal to every right-side element value.</span></span>       |



 

## <a name="some-or-any-quantifier"></a><span data-ttu-id="8d8d2-155">UN quantificatore (o qualsiasi)</span><span class="sxs-lookup"><span data-stu-id="8d8d2-155">SOME (or ANY) Quantifier</span></span>

<span data-ttu-id="8d8d2-156">Il quantificatore SOME e il quantificatore ANY possono essere usati in modo interscambiabile.</span><span class="sxs-lookup"><span data-stu-id="8d8d2-156">The SOME quantifier and the ANY quantifier can be used interchangeably.</span></span> <span data-ttu-id="8d8d2-157">Come il quantificatore ALL, il quantificatore SOME specifica che ogni elemento sul lato sinistro viene confrontato con ogni elemento sul lato destro.</span><span class="sxs-lookup"><span data-stu-id="8d8d2-157">Like the ALL quantifier, the SOME quantifier specifies that each element in the left side is compared against every element on the right side.</span></span> <span data-ttu-id="8d8d2-158">Per restituire true, il confronto deve essere true per almeno uno degli elementi sul lato sinistro rispetto a qualsiasi elemento a destra.</span><span class="sxs-lookup"><span data-stu-id="8d8d2-158">To return true, the comparison must be true for at least one of the elements on the left side when compared to any element on the right side.</span></span> <span data-ttu-id="8d8d2-159">Il numero di elementi nelle matrici di sinistra e di destra non ha alcun effetto sul risultato.</span><span class="sxs-lookup"><span data-stu-id="8d8d2-159">The number of elements on the left and right side arrays has no effect on the result.</span></span>

<span data-ttu-id="8d8d2-160">Nella tabella seguente viene illustrato il funzionamento di ogni operatore di confronto con il quantificatore SOME.</span><span class="sxs-lookup"><span data-stu-id="8d8d2-160">The following table shows how each comparison operator functions with the SOME quantifier.</span></span>



| <span data-ttu-id="8d8d2-161">Operatore</span><span class="sxs-lookup"><span data-stu-id="8d8d2-161">Operator</span></span>       | <span data-ttu-id="8d8d2-162">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8d8d2-162">Description</span></span>                                                                                                                                                     |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| =              | <span data-ttu-id="8d8d2-163">' Equal to ' restituisce true quando almeno uno dei valori degli elementi a sinistra è uguale a uno dei valori degli elementi a destra.</span><span class="sxs-lookup"><span data-stu-id="8d8d2-163">'Equal to' returns true when at least one of the left-side element values is the same as any of the right-side element values.</span></span>                                  |
| <span data-ttu-id="8d8d2-164">! = o <></span><span class="sxs-lookup"><span data-stu-id="8d8d2-164">!= or <></span></span> | <span data-ttu-id="8d8d2-165">' Diverso da' restituisce true se nessuno dei valori degli elementi a sinistra è uguale a uno dei valori degli elementi a destra.</span><span class="sxs-lookup"><span data-stu-id="8d8d2-165">'Not equal to' returns true when none of the left-side element values is the same as any of the right-side element values.</span></span>                                      |
| >           | <span data-ttu-id="8d8d2-166">' Maggiore di ' restituisce true quando almeno uno dei valori degli elementi a sinistra è maggiore di uno dei valori degli elementi a destra.</span><span class="sxs-lookup"><span data-stu-id="8d8d2-166">'Greater than' returns true when at least one of the left-side element values is greater than any one of the right-side element values.</span></span>                         |
| >=          | <span data-ttu-id="8d8d2-167">' Maggiore o uguale a' restituisce true quando almeno uno dei valori degli elementi di sinistra è maggiore o uguale a uno dei valori degli elementi a destra.</span><span class="sxs-lookup"><span data-stu-id="8d8d2-167">'Greater than or equal to' returns true when at least one of the left-side element values is greater than or equal to any one of the right-side element values.</span></span> |
| <           | <span data-ttu-id="8d8d2-168">' Less of ' restituisce true quando almeno uno dei valori degli elementi a sinistra è minore di uno dei valori degli elementi a destra.</span><span class="sxs-lookup"><span data-stu-id="8d8d2-168">'Less than' returns true when at least one of the left-side element values is less than any one of the right-side element values.</span></span>                               |
| <=          | <span data-ttu-id="8d8d2-169">' Minore o uguale a' restituisce true quando almeno uno dei valori degli elementi di sinistra è minore o uguale a uno dei valori degli elementi a destra.</span><span class="sxs-lookup"><span data-stu-id="8d8d2-169">'Less than or equal to' returns true when at least one of the left-side element values is less than or equal to any one of the right-side element values.</span></span>       |



 

## <a name="examples"></a><span data-ttu-id="8d8d2-170">Esempio</span><span class="sxs-lookup"><span data-stu-id="8d8d2-170">Examples</span></span>

<span data-ttu-id="8d8d2-171">Nell'esempio seguente viene verificato se i documenti sono inclusi nelle categorie "Finance" o "Planning":</span><span class="sxs-lookup"><span data-stu-id="8d8d2-171">The following example checks whether documents are in the "Finance" or "Planning" categories:</span></span>


```
SELECT System.ItemUrl FROM SystemIndex WHERE System.Category =
SOME ARRAY['Finance','Planning']
```



<span data-ttu-id="8d8d2-172">Tutti i confronti seguenti restituiscono true.</span><span class="sxs-lookup"><span data-stu-id="8d8d2-172">The following comparisons all evaluate true.</span></span> <span data-ttu-id="8d8d2-173">Tenere presente che, nell'uso effettivo, la sintassi della query di ricerca richiede che il lato sinistro sia una proprietà, non un valore letterale.</span><span class="sxs-lookup"><span data-stu-id="8d8d2-173">Remember that in actual use, the search query syntax requires the left side to be a property, not a literal value.</span></span>


```
ARRAY [1,2] > ARRAY [1,1]
ARRAY [1,2] > ARRAY [1,1,2]
ARRAY [1,2] < ARRAY [1,2,3]
ARRAY [1,2] = SOME ARRAY [1,12,27,35,2]
ARRAY [1,1] != ALL ARRAY [1,2]
ARRAY [1,20,21,22] < SOME ARRAY [0,40]
ARRAY [1,20,21,22] < ANY ARRAY [0,40]
```



## <a name="related-topics"></a><span data-ttu-id="8d8d2-174">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8d8d2-174">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="8d8d2-175">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="8d8d2-175">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8d8d2-176">Predicato LIKE</span><span class="sxs-lookup"><span data-stu-id="8d8d2-176">LIKE Predicate</span></span>](-search-sql-like.md)
</dt> <dt>

[<span data-ttu-id="8d8d2-177">Confronto di valori letterali</span><span class="sxs-lookup"><span data-stu-id="8d8d2-177">Literal Value Comparison</span></span>](-search-sql-literalvaluecomparison.md)
</dt> <dt>

[<span data-ttu-id="8d8d2-178">Predicato NULL</span><span class="sxs-lookup"><span data-stu-id="8d8d2-178">NULL Predicate</span></span>](-search-sql-null.md)
</dt> <dt>

<span data-ttu-id="8d8d2-179">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="8d8d2-179">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="8d8d2-180">Predicati full-text</span><span class="sxs-lookup"><span data-stu-id="8d8d2-180">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)
</dt> <dt>

[<span data-ttu-id="8d8d2-181">Predicati non full-text</span><span class="sxs-lookup"><span data-stu-id="8d8d2-181">Non-Full-Text Predicates</span></span>](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



