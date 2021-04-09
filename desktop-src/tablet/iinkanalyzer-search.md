---
description: Fornisce una ricerca basata su frasi fuzzy senza distinzione tra maiuscole e minuscole per i tratti di scrittura analizzati e i tratti di disegno analizzati con tipi riconosciuti.
ms.assetid: 5b5ce4b5-45ef-42ef-866b-2f38c32d8c86
title: 'Metodo IInkAnalyzer:: Search (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.Search
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ea9755c0f2836b363b967a3d6bfdc5d64a1305b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129442"
---
# <a name="iinkanalyzersearch-method"></a><span data-ttu-id="b1a00-103">Metodo IInkAnalyzer:: search</span><span class="sxs-lookup"><span data-stu-id="b1a00-103">IInkAnalyzer::Search method</span></span>

<span data-ttu-id="b1a00-104">Fornisce una ricerca basata su frasi fuzzy senza distinzione tra maiuscole e minuscole per i tratti di scrittura analizzati e i tratti di disegno analizzati con tipi riconosciuti.</span><span class="sxs-lookup"><span data-stu-id="b1a00-104">Provides a fuzzy, case-insensitive phrase based search for analyzed writing strokes and analyzed drawing strokes that have recognized types.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1a00-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b1a00-105">Syntax</span></span>


```C++
HRESULT Search(
  [in]      BSTR  bstrPhraseToMatch,
  [in, out] ULONG *pulSearchResultCount,
  [out]     ULONG **ppulStrokeCountPerResult,
  [in, out] ULONG *pulStrokeIdsCount,
  [out]     ULONG **ppulStrokeIds
);
```



## <a name="parameters"></a><span data-ttu-id="b1a00-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b1a00-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1a00-107">*bstrPhraseToMatch* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b1a00-107">*bstrPhraseToMatch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1a00-108">Frase che verrà trovata nelle alternative per i tratti attualmente analizzati.</span><span class="sxs-lookup"><span data-stu-id="b1a00-108">The phrase that will be found in the alternates for the currently analyzed strokes.</span></span>

</dd> <dt>

<span data-ttu-id="b1a00-109">*pulSearchResultCount* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="b1a00-109">*pulSearchResultCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b1a00-110">Numero massimo di risultati restituiti dalla ricerca.</span><span class="sxs-lookup"><span data-stu-id="b1a00-110">The maximum number of results returned from the search.</span></span>

</dd> <dt>

<span data-ttu-id="b1a00-111">*ppulStrokeCountPerResult* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b1a00-111">*ppulStrokeCountPerResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b1a00-112">Puntatore a una matrice del numero di tratti in ogni risultato della ricerca.</span><span class="sxs-lookup"><span data-stu-id="b1a00-112">Pointer to an array of the number of strokes in each search result.</span></span>

</dd> <dt>

<span data-ttu-id="b1a00-113">*pulStrokeIdsCount* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="b1a00-113">*pulStrokeIdsCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b1a00-114">Numero di ID tratto in *ppulStrokeIds*.</span><span class="sxs-lookup"><span data-stu-id="b1a00-114">The number of stroke IDs in *ppulStrokeIds*.</span></span>

</dd> <dt>

<span data-ttu-id="b1a00-115">*ppulStrokeIds* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="b1a00-115">*ppulStrokeIds* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b1a00-116">Puntatore a una matrice di ID tratto che rappresenta un set di set di tratti.</span><span class="sxs-lookup"><span data-stu-id="b1a00-116">Pointer to an array of stroke IDs representing a set of sets of strokes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1a00-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b1a00-117">Return value</span></span>

<span data-ttu-id="b1a00-118">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="b1a00-118">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b1a00-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="b1a00-119">Remarks</span></span>

<span data-ttu-id="b1a00-120">Questa ricerca trova le sottostringhe con più parole e singole parole.</span><span class="sxs-lookup"><span data-stu-id="b1a00-120">This search finds multi-word and single word substrings.</span></span> <span data-ttu-id="b1a00-121">Viene eseguita la ricerca sia di risultati di riconoscimento alternativi che di segmentazioni alternative.</span><span class="sxs-lookup"><span data-stu-id="b1a00-121">Both alternate recognition results and alternate segmentations are searched.</span></span>

<span data-ttu-id="b1a00-122">Tutte le stringhe in ingresso verranno convertite in una singola combinazione di maiuscole e minuscole per il confronto utilizzando l'identificatore LCID del thread corrente per eseguire questa conversione per rispettare le convenzioni dei case culturali.</span><span class="sxs-lookup"><span data-stu-id="b1a00-122">All incoming strings will be converted to a single casing for comparison utilizing the LCID of the current thread to do this conversion to respect cultural case conventions.</span></span>

<span data-ttu-id="b1a00-123">La stringa passata viene considerata come una frase.</span><span class="sxs-lookup"><span data-stu-id="b1a00-123">The string passed is treated as a phrase.</span></span> <span data-ttu-id="b1a00-124">Le parole e i caratteri devono essere visualizzati in alterantes per i tratti nell'ordine specificato.</span><span class="sxs-lookup"><span data-stu-id="b1a00-124">Words and characters must appear in the alterantes for the strokes in the order specified.</span></span> <span data-ttu-id="b1a00-125">La prima e l'ultima parola della frase possono corrispondere a sottostringhe (la prima parola che viene visualizzata alla fine di un'alternativa e l'ultima parola in corrispondenza della begginging di uno), ma tutte le altre parole (quelle all'interno della frase) devono apparire come parole intere.</span><span class="sxs-lookup"><span data-stu-id="b1a00-125">The first and last words of the phrase may be matched as substrings (the first word appearing at the end of an alternate and the last word appearing at the begginging of one), but any other words (those inside of the phrase) must appear as whole words.</span></span>

<span data-ttu-id="b1a00-126">Se la stringa passata non ha spazi vuoti tra i caratteri, la sottostringa può trovarsi in qualsiasi punto all'interno di una singola parola in un'alternativa.</span><span class="sxs-lookup"><span data-stu-id="b1a00-126">If the string passed in has no whitespace in between characters, the substring may be found anywhere inside of a single word in an alternate.</span></span>

<span data-ttu-id="b1a00-127">Solo la presenza o l'assenza di spazi vuoti tra i caratteri modifica i risultati della ricerca.</span><span class="sxs-lookup"><span data-stu-id="b1a00-127">Only the presence or absence of whitespace between characters changes the results of search.</span></span> <span data-ttu-id="b1a00-128">Lo spazio vuoto non racchiuso tra caratteri viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="b1a00-128">Whitespace that is not surrounded by characters is ignored.</span></span> <span data-ttu-id="b1a00-129">Il tipo dello spazio vuoto viene ignorato (una scheda o uno spazio tra i caratteri fornirà lo stesso risultato).</span><span class="sxs-lookup"><span data-stu-id="b1a00-129">The type of the whitespace is ignored (a tab or a space between characters will give the same result).</span></span> <span data-ttu-id="b1a00-130">La quantità di spazio vuoto non è rilevante. uno spazio o due spazi tra i caratteri restituiranno lo stesso risultato.</span><span class="sxs-lookup"><span data-stu-id="b1a00-130">The amount of whitespace does not matter - one space or two spaces in between characters will give the same result.</span></span>

<span data-ttu-id="b1a00-131">La ricerca non genera eventi PopulateContextNode.</span><span class="sxs-lookup"><span data-stu-id="b1a00-131">Search does not generate PopulateContextNode events.</span></span> <span data-ttu-id="b1a00-132">Verranno cercati solo i tratti già popolati.</span><span class="sxs-lookup"><span data-stu-id="b1a00-132">Only the strokes that have already been populated will be searched.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1a00-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b1a00-133">Requirements</span></span>



| <span data-ttu-id="b1a00-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1a00-134">Requirement</span></span> | <span data-ttu-id="b1a00-135">Valore</span><span class="sxs-lookup"><span data-stu-id="b1a00-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1a00-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b1a00-136">Minimum supported client</span></span><br/> | <span data-ttu-id="b1a00-137">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="b1a00-137">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b1a00-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b1a00-138">Minimum supported server</span></span><br/> | <span data-ttu-id="b1a00-139">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="b1a00-139">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="b1a00-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b1a00-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1a00-141"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="b1a00-141"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b1a00-142">DLL</span><span class="sxs-lookup"><span data-stu-id="b1a00-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b1a00-143"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b1a00-143"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="b1a00-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b1a00-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1a00-145">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="b1a00-145">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> </dl>

 

 




