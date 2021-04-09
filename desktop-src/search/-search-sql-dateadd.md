---
description: La funzione DATEADD esegue calcoli di data e ora per le proprietà corrispondenti con tipi di dati. Utilizzare la funzione DATEADD per ottenere le date e le ore in un intervallo di tempo specificato prima del presente.
ms.assetid: 83ef098d-85ef-4883-a1e1-9229e050247f
title: Funzione DATEADD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c0b193e75ec644eb3312a61c723edeac43ee264
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128550"
---
# <a name="dateadd-function"></a><span data-ttu-id="c58dc-104">Funzione DATEADD</span><span class="sxs-lookup"><span data-stu-id="c58dc-104">DATEADD Function</span></span>

<span data-ttu-id="c58dc-105">La funzione DATEADD esegue calcoli di data e ora per le proprietà corrispondenti con tipi di dati.</span><span class="sxs-lookup"><span data-stu-id="c58dc-105">The DATEADD function performs time and date calculations for matching properties having date types.</span></span> <span data-ttu-id="c58dc-106">Utilizzare la funzione DATEADD per ottenere le date e le ore in un intervallo di tempo specificato prima del presente.</span><span class="sxs-lookup"><span data-stu-id="c58dc-106">Use the DATEADD function to obtain dates and times in a specified amount of time before the present.</span></span>

## <a name="syntax"></a><span data-ttu-id="c58dc-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c58dc-107">Syntax</span></span>


```
DATEADD (DateTimeUnits, OffsetValue, DateTime)
```



## <a name="arguments"></a><span data-ttu-id="c58dc-108">Argomenti</span><span class="sxs-lookup"><span data-stu-id="c58dc-108">Arguments</span></span>

<span data-ttu-id="c58dc-109">*DateTimeUnits*</span><span class="sxs-lookup"><span data-stu-id="c58dc-109">*DateTimeUnits*</span></span>

<span data-ttu-id="c58dc-110">Specifica le unità del parametro *DateTime* : anno, trimestre, mese, settimana, giorno, ora, minuto o secondo.</span><span class="sxs-lookup"><span data-stu-id="c58dc-110">Specifies the units of the *DateTime* parameter: YEAR, QUARTER, MONTH, WEEK, DAY, HOUR, MINUTE, or SECOND.</span></span> <span data-ttu-id="c58dc-111">Questo valore fa distinzione tra maiuscole e minuscole e le virgolette non sono necessarie intorno al parametro.</span><span class="sxs-lookup"><span data-stu-id="c58dc-111">This value is case-sensitive, and quotation marks are not required around the parameter.</span></span>

<span data-ttu-id="c58dc-112">*OffsetValue*</span><span class="sxs-lookup"><span data-stu-id="c58dc-112">*OffsetValue*</span></span>

<span data-ttu-id="c58dc-113">Specifica l'offset dell'ora, nelle unità specificate dal parametro *DateTimeUnits* .</span><span class="sxs-lookup"><span data-stu-id="c58dc-113">Specifies the time offset, in the units specified by the *DateTimeUnits* parameter.</span></span> <span data-ttu-id="c58dc-114">**OffsetValue** deve essere un numero intero negativo.</span><span class="sxs-lookup"><span data-stu-id="c58dc-114">**OffsetValue** must be a negative integer.</span></span> <span data-ttu-id="c58dc-115">I valori positivi non sono supportati.</span><span class="sxs-lookup"><span data-stu-id="c58dc-115">Positive values are not supported.</span></span>

<span data-ttu-id="c58dc-116">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="c58dc-116">*DateTime*</span></span>

<span data-ttu-id="c58dc-117">Specifica un timestamp da cui calcolare l'offset.</span><span class="sxs-lookup"><span data-stu-id="c58dc-117">Specifies a time stamp from which to calculate the offset.</span></span> <span data-ttu-id="c58dc-118">Non può essere un valore letterale di data.</span><span class="sxs-lookup"><span data-stu-id="c58dc-118">This cannot be a date literal.</span></span> <span data-ttu-id="c58dc-119">Deve essere GETGMTDATE o il risultato di un'altra funzione DATEADD.</span><span class="sxs-lookup"><span data-stu-id="c58dc-119">It must be either GETGMTDATE or the result of another DATEADD function.</span></span>

## <a name="remarks"></a><span data-ttu-id="c58dc-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="c58dc-120">Remarks</span></span>

<span data-ttu-id="c58dc-121">La funzione DATEADD può essere utilizzata solo nei confronti di valori letterali e solo sul lato destro dell'operatore di confronto.</span><span class="sxs-lookup"><span data-stu-id="c58dc-121">The DATEADD function can be used only in literal value comparisons and only on the right side of the comparison operator.</span></span>

<span data-ttu-id="c58dc-122">La funzione GETGMTDATE restituisce la data e l'ora correnti nell'ora di Greenwich (GMT).</span><span class="sxs-lookup"><span data-stu-id="c58dc-122">The GETGMTDATE function returns the current date and time in Greenwich Mean Time (GMT).</span></span> <span data-ttu-id="c58dc-123">Tenere presente che questo valore potrebbe non corrispondere all'ora locale del computer.</span><span class="sxs-lookup"><span data-stu-id="c58dc-123">Remember that this value may not be the same as the local time of your computer.</span></span>

<span data-ttu-id="c58dc-124">Non usare l'operatore di confronto uguale a (=) perché la rappresentazione temporale interna può produrre errori di arrotondamento che generano risultati di corrispondenza imprevisti.</span><span class="sxs-lookup"><span data-stu-id="c58dc-124">Do not use the equals (=) comparison operator because the internal time representation can produce rounding errors that result in unexpected matching results.</span></span>

<span data-ttu-id="c58dc-125">È possibile utilizzare più funzioni DATEADD per combinare unità di offset.</span><span class="sxs-lookup"><span data-stu-id="c58dc-125">You can use multiple DATEADD functions to combine offset units.</span></span>

### <a name="examples"></a><span data-ttu-id="c58dc-126">Esempio</span><span class="sxs-lookup"><span data-stu-id="c58dc-126">Examples</span></span>

<span data-ttu-id="c58dc-127">La clausola WHERE di esempio seguente corrisponde ai documenti modificati negli ultimi cinque giorni:</span><span class="sxs-lookup"><span data-stu-id="c58dc-127">The following example WHERE clause matches documents that were modified within the last five days:</span></span>


```
...WHERE System.DateModified <=DATEADD (DAY, -5, GETGMTDATE())
```



<span data-ttu-id="c58dc-128">La clausola WHERE di esempio seguente corrisponde ai documenti modificati negli ultimi due giorni e quattro ore:</span><span class="sxs-lookup"><span data-stu-id="c58dc-128">The following example WHERE clause matches documents that were modified within the last two days and four hours:</span></span>


```
...WHERE System.DateModified <=DATEADD (DAY, -2, DATEADD (HOUR, -4, GETGMTDATE()))
```



## <a name="related-topics"></a><span data-ttu-id="c58dc-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c58dc-129">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="c58dc-130">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="c58dc-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c58dc-131">Confronto di valori letterali</span><span class="sxs-lookup"><span data-stu-id="c58dc-131">Literal Value Comparison</span></span>](-search-sql-literalvaluecomparison.md)
</dt> <dt>

[<span data-ttu-id="c58dc-132">Confronti multivalore (matrice)</span><span class="sxs-lookup"><span data-stu-id="c58dc-132">Multi-Valued (ARRAY) Comparisons</span></span>](-search-sql-multivaluedcomparisons.md)
</dt> <dt>

<span data-ttu-id="c58dc-133">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="c58dc-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c58dc-134">Predicati full-text</span><span class="sxs-lookup"><span data-stu-id="c58dc-134">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)
</dt> <dt>

[<span data-ttu-id="c58dc-135">Predicati non full-text</span><span class="sxs-lookup"><span data-stu-id="c58dc-135">Non-Full-Text Predicates</span></span>](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



