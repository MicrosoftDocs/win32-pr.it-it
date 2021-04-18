---
description: Il confronto dei valori letterali usa gli operatori di confronto standard per la corrispondenza di una colonna a valore singolo con un valore letterale.
ms.assetid: 941298b4-d703-4b3f-8bde-0e6e158560df
title: Confronto di valori letterali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d8577e5a97dcc92131658c325f175efa1d0c3fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306120"
---
# <a name="literal-value-comparison"></a><span data-ttu-id="aec09-103">Confronto di valori letterali</span><span class="sxs-lookup"><span data-stu-id="aec09-103">Literal Value Comparison</span></span>

<span data-ttu-id="aec09-104">Il confronto dei valori letterali usa gli operatori di confronto standard per la corrispondenza di una colonna a valore singolo con un valore [letterale](-search-sql-literals.md) .</span><span class="sxs-lookup"><span data-stu-id="aec09-104">The literal value comparison uses standard comparison operators for matching a single-valued column to a [literal](-search-sql-literals.md) value.</span></span> <span data-ttu-id="aec09-105">Per informazioni sul confronto tra colonne multivalore, vedere [confronti con più valori (Array)](-search-sql-multivaluedcomparisons.md).</span><span class="sxs-lookup"><span data-stu-id="aec09-105">For information about comparing multivalued columns, see [Multi-Valued (ARRAY) Comparisons](-search-sql-multivaluedcomparisons.md).</span></span>

<span data-ttu-id="aec09-106">Il predicato di confronto dei valori letterali presenta la sintassi seguente:</span><span class="sxs-lookup"><span data-stu-id="aec09-106">The literal value comparison predicate has the following syntax:</span></span>


```
...WHERE <column> <comparison operator> <literal>
```



> [!Note]  
> <span data-ttu-id="aec09-107">Il lato destro del confronto deve essere un valore letterale.</span><span class="sxs-lookup"><span data-stu-id="aec09-107">The right side of the comparison must be a literal.</span></span> <span data-ttu-id="aec09-108">Non è possibile confrontare una colonna con un valore calcolato e non è possibile confrontare una colonna con un'altra colonna.</span><span class="sxs-lookup"><span data-stu-id="aec09-108">You cannot compare a column against a computed value, and you cannot compare a column against another column.</span></span>

 

<span data-ttu-id="aec09-109">La parte colonna è qualsiasi colonna di proprietà valida ed è possibile eseguirne il cast a un altro tipo, se necessario.</span><span class="sxs-lookup"><span data-stu-id="aec09-109">The column part is any valid property column and can be cast to another type if necessary.</span></span> <span data-ttu-id="aec09-110">Facoltativamente, è possibile racchiudere il nome della colonna tra virgolette doppie per migliorare la leggibilità senza influire sulle funzionalità.</span><span class="sxs-lookup"><span data-stu-id="aec09-110">Optionally, you can enclose the column name in double quotes for readability without affecting functionality.</span></span> <span data-ttu-id="aec09-111">Per ulteriori informazioni, vedere [cast del tipo di dati di una colonna](-search-sql-castingdatacolumntype.md).</span><span class="sxs-lookup"><span data-stu-id="aec09-111">For more information, see [Casting the Data Type of a Column](-search-sql-castingdatacolumntype.md).</span></span>

<span data-ttu-id="aec09-112">Il valore letterale può essere qualsiasi valore letterale stringa, numerico, esadecimale, booleano o data, racchiuso tra virgolette singole.</span><span class="sxs-lookup"><span data-stu-id="aec09-112">The literal can be any string, numeric, hexadecimal, Boolean, or date literal, enclosed in single quotation marks.</span></span> <span data-ttu-id="aec09-113">Vengono riconosciute solo le corrispondenze esatte e i caratteri jolly vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="aec09-113">Only exact matches are recognized, and wildcard characters are ignored.</span></span> <span data-ttu-id="aec09-114">È anche possibile eseguire il cast del valore letterale a un altro tipo.</span><span class="sxs-lookup"><span data-stu-id="aec09-114">The literal can also be cast to another type.</span></span>

## <a name="comparison-operators"></a><span data-ttu-id="aec09-115">Operatori di confronto</span><span class="sxs-lookup"><span data-stu-id="aec09-115">Comparison Operators</span></span>

<span data-ttu-id="aec09-116">Nella tabella seguente vengono descritti gli operatori di confronto supportati.</span><span class="sxs-lookup"><span data-stu-id="aec09-116">The following table describes the supported comparison operators.</span></span>



| <span data-ttu-id="aec09-117">Operatore di confronto</span><span class="sxs-lookup"><span data-stu-id="aec09-117">Comparison operator</span></span> | <span data-ttu-id="aec09-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aec09-118">Description</span></span>              |
|---------------------|--------------------------|
| =                   | <span data-ttu-id="aec09-119">Uguale a</span><span class="sxs-lookup"><span data-stu-id="aec09-119">Equal to</span></span>                 |
| <span data-ttu-id="aec09-120">! = o <></span><span class="sxs-lookup"><span data-stu-id="aec09-120">!= or <></span></span>      | <span data-ttu-id="aec09-121">Diverso da</span><span class="sxs-lookup"><span data-stu-id="aec09-121">Not equal to</span></span>             |
| >                | <span data-ttu-id="aec09-122">Maggiore di</span><span class="sxs-lookup"><span data-stu-id="aec09-122">Greater than</span></span>             |
| >=               | <span data-ttu-id="aec09-123">Maggiore o uguale a</span><span class="sxs-lookup"><span data-stu-id="aec09-123">Greater than or equal to</span></span> |
| <                | <span data-ttu-id="aec09-124">Minore di</span><span class="sxs-lookup"><span data-stu-id="aec09-124">Less than</span></span>                |
| <=               | <span data-ttu-id="aec09-125">Minore o uguale a</span><span class="sxs-lookup"><span data-stu-id="aec09-125">Less than or equal to</span></span>    |



 

 

<span data-ttu-id="aec09-126">In combinazione con l'operatore "=", Windows Search Structured Query Language (SQL) supporta l'utilizzo delle parole chiave BEFORe e AFTER, che specificano se la query deve confrontare i valori di colonna prima o dopo un valore specificato, nell'ordinamento del dizionario.</span><span class="sxs-lookup"><span data-stu-id="aec09-126">In conjunction with the "=" operator, Windows Search Structured Query Language (SQL) supports the use of BEFORE and AFTER keywords, which specify whether the query should compare column values before or after a specified value, in dictionary sort ordering.</span></span>


```
...WHERE <column> <comparison operator> [BEFORE | AFTER](<https://msdn.microsoft.com/library/Ff637626(v=MSDN.10).aspx>)
```



## <a name="examples"></a><span data-ttu-id="aec09-127">Esempio</span><span class="sxs-lookup"><span data-stu-id="aec09-127">Examples</span></span>

<span data-ttu-id="aec09-128">Di seguito sono riportati esempi del predicato di confronto dei valori letterali.</span><span class="sxs-lookup"><span data-stu-id="aec09-128">The following are examples of the literal value comparison predicate.</span></span>


```
SELECT System.ItemUrl,System.ItemNameDisplay FROM SystemIndex 
    WHERE System.Title = 'Accounting'

SELECT System.ItemUrl,System.ItemNameDisplay FROM SystemIndex 
    WHERE System.IsFlagged != TRUE

SELECT System.ItemUrl,System.ItemNameDisplay FROM SystemIndex 
    WHERE System.Size >= 10000

SELECT System.ItemUrl,System.ItemNameDisplay FROM SystemIndex 
    WHERE System.Author = BEFORE('m')
```



## <a name="related-topics"></a><span data-ttu-id="aec09-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="aec09-129">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="aec09-130">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="aec09-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="aec09-131">Predicato LIKE</span><span class="sxs-lookup"><span data-stu-id="aec09-131">LIKE Predicate</span></span>](-search-sql-like.md)
</dt> <dt>

[<span data-ttu-id="aec09-132">DATEADD (funzione)</span><span class="sxs-lookup"><span data-stu-id="aec09-132">DATEADD Function</span></span>](-search-sql-dateadd.md)
</dt> <dt>

[<span data-ttu-id="aec09-133">Confronti multivalore (matrice)</span><span class="sxs-lookup"><span data-stu-id="aec09-133">Multi-Valued (ARRAY) Comparisons</span></span>](-search-sql-multivaluedcomparisons.md)
</dt> <dt>

[<span data-ttu-id="aec09-134">Predicato NULL</span><span class="sxs-lookup"><span data-stu-id="aec09-134">NULL Predicate</span></span>](-search-sql-null.md)
</dt> <dt>

<span data-ttu-id="aec09-135">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="aec09-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="aec09-136">Predicati full-text</span><span class="sxs-lookup"><span data-stu-id="aec09-136">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)
</dt> <dt>

[<span data-ttu-id="aec09-137">Predicati non full-text</span><span class="sxs-lookup"><span data-stu-id="aec09-137">Non-Full-Text Predicates</span></span>](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



