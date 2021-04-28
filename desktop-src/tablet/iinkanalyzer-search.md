---
description: 'Metodo IInkAnalyzer::Search: fornisce una ricerca fuzzy basata su frasi senza distinzione tra maiuscole e minuscole per i tratti di scrittura analizzati e i tratti di disegno analizzati con tipi riconosciuti.'
ms.assetid: 5b5ce4b5-45ef-42ef-866b-2f38c32d8c86
title: Metodo IInkAnalyzer::Search (IACom.h)
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
ms.openlocfilehash: 94ccdebf8c8a134a845ff3df3017d710d1da93f1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113729"
---
# <a name="iinkanalyzersearch-method"></a><span data-ttu-id="6c907-103">Metodo IInkAnalyzer::Search</span><span class="sxs-lookup"><span data-stu-id="6c907-103">IInkAnalyzer::Search method</span></span>

<span data-ttu-id="6c907-104">Fornisce una ricerca fuzzy basata su frasi senza distinzione tra maiuscole e minuscole per tratti di scrittura analizzati e tratti di disegno analizzati con tipi riconosciuti.</span><span class="sxs-lookup"><span data-stu-id="6c907-104">Provides a fuzzy, case-insensitive phrase based search for analyzed writing strokes and analyzed drawing strokes that have recognized types.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c907-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6c907-105">Syntax</span></span>


```C++
HRESULT Search(
  [in]      BSTR  bstrPhraseToMatch,
  [in, out] ULONG *pulSearchResultCount,
  [out]     ULONG **ppulStrokeCountPerResult,
  [in, out] ULONG *pulStrokeIdsCount,
  [out]     ULONG **ppulStrokeIds
);
```



## <a name="parameters"></a><span data-ttu-id="6c907-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6c907-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c907-107">*bstrPhraseToMatch* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="6c907-107">*bstrPhraseToMatch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c907-108">Frase che verrà trovata nelle alternative per i tratti attualmente analizzati.</span><span class="sxs-lookup"><span data-stu-id="6c907-108">The phrase that will be found in the alternates for the currently analyzed strokes.</span></span>

</dd> <dt>

<span data-ttu-id="6c907-109">*pulSearchResultCount* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="6c907-109">*pulSearchResultCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c907-110">Numero massimo di risultati restituiti dalla ricerca.</span><span class="sxs-lookup"><span data-stu-id="6c907-110">The maximum number of results returned from the search.</span></span>

</dd> <dt>

<span data-ttu-id="6c907-111">*ppulStrokeCountPerResult* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="6c907-111">*ppulStrokeCountPerResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c907-112">Puntatore a una matrice del numero di tratti in ogni risultato della ricerca.</span><span class="sxs-lookup"><span data-stu-id="6c907-112">Pointer to an array of the number of strokes in each search result.</span></span>

</dd> <dt>

<span data-ttu-id="6c907-113">*pulStrokeIdsCount* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="6c907-113">*pulStrokeIdsCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c907-114">Numero di ID di tratto in *ppulStrokeIds.*</span><span class="sxs-lookup"><span data-stu-id="6c907-114">The number of stroke IDs in *ppulStrokeIds*.</span></span>

</dd> <dt>

<span data-ttu-id="6c907-115">*ppulStrokeIds* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="6c907-115">*ppulStrokeIds* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c907-116">Puntatore a una matrice di ID tratto che rappresenta un set di tratti.</span><span class="sxs-lookup"><span data-stu-id="6c907-116">Pointer to an array of stroke IDs representing a set of sets of strokes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c907-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6c907-117">Return value</span></span>

<span data-ttu-id="6c907-118">Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna.](classes-and-interfaces---ink-analysis.md)</span><span class="sxs-lookup"><span data-stu-id="6c907-118">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6c907-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="6c907-119">Remarks</span></span>

<span data-ttu-id="6c907-120">Questa ricerca trova sottostringhe di più parole e singole parole.</span><span class="sxs-lookup"><span data-stu-id="6c907-120">This search finds multi-word and single word substrings.</span></span> <span data-ttu-id="6c907-121">Vengono cercati sia i risultati del riconoscimento alternativo che le segmentazioni alternative.</span><span class="sxs-lookup"><span data-stu-id="6c907-121">Both alternate recognition results and alternate segmentations are searched.</span></span>

<span data-ttu-id="6c907-122">Tutte le stringhe in ingresso verranno convertite in una singola distinzione tra maiuscole e minuscole per il confronto utilizzando l'LCID del thread corrente per eseguire questa conversione per rispettare le convenzioni relative alle maiuscole e minuscole relative alle impostazioni cultura.</span><span class="sxs-lookup"><span data-stu-id="6c907-122">All incoming strings will be converted to a single casing for comparison utilizing the LCID of the current thread to do this conversion to respect cultural case conventions.</span></span>

<span data-ttu-id="6c907-123">La stringa passata viene considerata come una frase.</span><span class="sxs-lookup"><span data-stu-id="6c907-123">The string passed is treated as a phrase.</span></span> <span data-ttu-id="6c907-124">Le parole e i caratteri devono essere visualizzati negli alterante per i tratti nell'ordine specificato.</span><span class="sxs-lookup"><span data-stu-id="6c907-124">Words and characters must appear in the alterantes for the strokes in the order specified.</span></span> <span data-ttu-id="6c907-125">La prima e l'ultima parola della frase possono essere abbinate come sottostringhe (la prima parola visualizzata alla fine di un'alternativa e l'ultima parola visualizzata all'inizio della frase), ma tutte le altre parole (quelle all'interno della frase) devono essere visualizzate come parole intere.</span><span class="sxs-lookup"><span data-stu-id="6c907-125">The first and last words of the phrase may be matched as substrings (the first word appearing at the end of an alternate and the last word appearing at the begginging of one), but any other words (those inside of the phrase) must appear as whole words.</span></span>

<span data-ttu-id="6c907-126">Se la stringa passata non contiene spazi vuoti tra i caratteri, la sottostringa può essere trovata in qualsiasi punto all'interno di una singola parola in un'alternativa.</span><span class="sxs-lookup"><span data-stu-id="6c907-126">If the string passed in has no whitespace in between characters, the substring may be found anywhere inside of a single word in an alternate.</span></span>

<span data-ttu-id="6c907-127">Solo la presenza o l'assenza di spazi vuoti tra i caratteri modifica i risultati della ricerca.</span><span class="sxs-lookup"><span data-stu-id="6c907-127">Only the presence or absence of whitespace between characters changes the results of search.</span></span> <span data-ttu-id="6c907-128">Gli spazi vuoti non racchiusi tra caratteri vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="6c907-128">Whitespace that is not surrounded by characters is ignored.</span></span> <span data-ttu-id="6c907-129">Il tipo di spazio vuoto viene ignorato (una tabulazione o uno spazio tra i caratteri offrirà lo stesso risultato).</span><span class="sxs-lookup"><span data-stu-id="6c907-129">The type of the whitespace is ignored (a tab or a space between characters will give the same result).</span></span> <span data-ttu-id="6c907-130">La quantità di spazi vuoti non è importante: uno o due spazi tra i caratteri offriranno lo stesso risultato.</span><span class="sxs-lookup"><span data-stu-id="6c907-130">The amount of whitespace does not matter - one space or two spaces in between characters will give the same result.</span></span>

<span data-ttu-id="6c907-131">La ricerca non genera eventi PopulateContextNode.</span><span class="sxs-lookup"><span data-stu-id="6c907-131">Search does not generate PopulateContextNode events.</span></span> <span data-ttu-id="6c907-132">Verranno cercati solo i tratti già popolati.</span><span class="sxs-lookup"><span data-stu-id="6c907-132">Only the strokes that have already been populated will be searched.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c907-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6c907-133">Requirements</span></span>



| <span data-ttu-id="6c907-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c907-134">Requirement</span></span> | <span data-ttu-id="6c907-135">Valore</span><span class="sxs-lookup"><span data-stu-id="6c907-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c907-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6c907-136">Minimum supported client</span></span><br/> | <span data-ttu-id="6c907-137">Solo app desktop Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="6c907-137">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="6c907-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6c907-138">Minimum supported server</span></span><br/> | <span data-ttu-id="6c907-139">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="6c907-139">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="6c907-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6c907-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c907-141"><dt>IACom.h (richiede anche IACom \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="6c907-141"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="6c907-142">DLL</span><span class="sxs-lookup"><span data-stu-id="6c907-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c907-143"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c907-143"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="6c907-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6c907-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c907-145">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="6c907-145">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> </dl>

 

 




