---
description: 'Metodo IInkAnalyzer::SearchWithLanguageId: fornisce una ricerca fuzzy basata su frasi senza distinzione tra maiuscole e minuscole per i tratti di scrittura analizzati e i tratti di disegno analizzati con tipi riconosciuti.'
ms.assetid: dfd481f9-38fd-433f-b1fc-697c735c13da
title: Metodo IInkAnalyzer::SearchWithLanguageId (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SearchWithLanguageId
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 201469933da10b0d68a4d3a50e63c42f8d01d2dd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083659"
---
# <a name="iinkanalyzersearchwithlanguageid-method"></a><span data-ttu-id="1ac4c-103">Metodo IInkAnalyzer::SearchWithLanguageId</span><span class="sxs-lookup"><span data-stu-id="1ac4c-103">IInkAnalyzer::SearchWithLanguageId method</span></span>

<span data-ttu-id="1ac4c-104">Fornisce una ricerca fuzzy basata su frasi senza distinzione tra maiuscole e minuscole per i tratti di scrittura analizzati e i tratti di disegno analizzati con tipi riconosciuti.</span><span class="sxs-lookup"><span data-stu-id="1ac4c-104">Provides a fuzzy, case-insensitive phrase based search for analyzed writing strokes and analyzed drawing strokes that have recognized types.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ac4c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1ac4c-105">Syntax</span></span>


```C++
HRESULT SearchWithLanguageId(
  [in]      BSTR  bstrPhraseToMatch,
  [in]      LONG  lSearchStringLanguageId,
  [in, out] ULONG *pulSearchResultCount,
  [out]     ULONG **ppulStrokeCountPerResult,
  [in, out] ULONG *pulStrokeIdsCount,
  [out]     ULONG **ppulStrokeIds
);
```



## <a name="parameters"></a><span data-ttu-id="1ac4c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1ac4c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ac4c-107">*bstrPhraseToMatch* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="1ac4c-107">*bstrPhraseToMatch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ac4c-108">Frase che verrà trovata nelle alternative per i tratti attualmente analizzati.</span><span class="sxs-lookup"><span data-stu-id="1ac4c-108">The phrase that will be found in the alternates for the currently analyzed strokes.</span></span>

</dd> <dt>

<span data-ttu-id="1ac4c-109">*lSearchStringLanguageId* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="1ac4c-109">*lSearchStringLanguageId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ac4c-110">LCID associato alla stringa passata.</span><span class="sxs-lookup"><span data-stu-id="1ac4c-110">The LCID associated with the string that is passed.</span></span> <span data-ttu-id="1ac4c-111">Utilizzato per convertire internamente la distinzione tra maiuscole e minuscole per supportare confronti senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="1ac4c-111">Used to convert the case internally to support case insensitive comparisons.</span></span>

</dd> <dt>

<span data-ttu-id="1ac4c-112">*pulSearchResultCount* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="1ac4c-112">*pulSearchResultCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1ac4c-113">Numero massimo di risultati restituiti dalla ricerca.</span><span class="sxs-lookup"><span data-stu-id="1ac4c-113">The maximum number of results returned from the search.</span></span>

</dd> <dt>

<span data-ttu-id="1ac4c-114">*ppulStrokeCountPerResult* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="1ac4c-114">*ppulStrokeCountPerResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1ac4c-115">Puntatore a una matrice del numero di tratti in ogni risultato della ricerca.</span><span class="sxs-lookup"><span data-stu-id="1ac4c-115">Pointer to an array of the number of strokes in each search result.</span></span>

</dd> <dt>

<span data-ttu-id="1ac4c-116">*pulStrokeIdsCount* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="1ac4c-116">*pulStrokeIdsCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1ac4c-117">Numero di ID tratto in *ppulStrokeIds.*</span><span class="sxs-lookup"><span data-stu-id="1ac4c-117">The number of stroke IDs in *ppulStrokeIds*.</span></span>

</dd> <dt>

<span data-ttu-id="1ac4c-118">*ppulStrokeIds* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="1ac4c-118">*ppulStrokeIds* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1ac4c-119">Puntatore a una matrice di ID tratto che rappresenta un set di tratti.</span><span class="sxs-lookup"><span data-stu-id="1ac4c-119">Pointer to an array of stroke IDs representing a set of sets of strokes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ac4c-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1ac4c-120">Return value</span></span>

<span data-ttu-id="1ac4c-121">Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="1ac4c-121">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1ac4c-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="1ac4c-122">Remarks</span></span>

<span data-ttu-id="1ac4c-123">Questa ricerca trova sottostringhe di più parole e singole parole.</span><span class="sxs-lookup"><span data-stu-id="1ac4c-123">This search finds multi-word and single word substrings.</span></span> <span data-ttu-id="1ac4c-124">Vengono cercati sia i risultati di riconoscimento alternativi che le segmentazioni alternative.</span><span class="sxs-lookup"><span data-stu-id="1ac4c-124">Both alternate recognition results and alternate segmentations are searched.</span></span>

<span data-ttu-id="1ac4c-125">Tutte le stringhe in ingresso verranno convertite in un'unica distinzione tra maiuscole e minuscole per il confronto utilizzando l'LCID del thread corrente per eseguire questa conversione per rispettare le convenzioni relative alle maiuscole e minuscole relative alle impostazioni cultura.</span><span class="sxs-lookup"><span data-stu-id="1ac4c-125">All incoming strings will be converted to a single casing for comparison utilizing the LCID of the current thread to do this conversion to respect cultural case conventions.</span></span>

<span data-ttu-id="1ac4c-126">La stringa passata viene considerata come una frase.</span><span class="sxs-lookup"><span data-stu-id="1ac4c-126">The string passed is treated as a phrase.</span></span> <span data-ttu-id="1ac4c-127">Le parole e i caratteri devono essere visualizzati negli alterante per i tratti nell'ordine specificato.</span><span class="sxs-lookup"><span data-stu-id="1ac4c-127">Words and characters must appear in the alterantes for the strokes in the order specified.</span></span> <span data-ttu-id="1ac4c-128">La prima e l'ultima parola della frase possono essere abbinate come sottostringhe (la prima parola visualizzata alla fine di un'alternativa e l'ultima parola visualizzata all'inizio di una frase), ma qualsiasi altra parola (quelle all'interno della frase) deve essere visualizzata come parole intere.</span><span class="sxs-lookup"><span data-stu-id="1ac4c-128">The first and last words of the phrase may be matched as substrings (the first word appearing at the end of an alternate and the last word appearing at the begginging of one), but any other words (those inside of the phrase) must appear as whole words.</span></span>

<span data-ttu-id="1ac4c-129">Se la stringa passata non contiene spazi vuoti tra i caratteri, la sottostringa può essere trovata in qualsiasi punto all'interno di una singola parola in un'alternativa.</span><span class="sxs-lookup"><span data-stu-id="1ac4c-129">If the string passed in has no whitespace in between characters, the substring may be found anywhere inside of a single word in an alternate.</span></span>

<span data-ttu-id="1ac4c-130">Solo la presenza o l'assenza di spazi vuoti tra i caratteri modifica i risultati della ricerca.</span><span class="sxs-lookup"><span data-stu-id="1ac4c-130">Only the presence or absence of whitespace between characters changes the results of search.</span></span> <span data-ttu-id="1ac4c-131">Gli spazi vuoti non racchiusi tra caratteri vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="1ac4c-131">Whitespace that is not surrounded by characters is ignored.</span></span> <span data-ttu-id="1ac4c-132">Il tipo di spazio vuoto viene ignorato (una tabulazione o uno spazio tra i caratteri offrirà lo stesso risultato).</span><span class="sxs-lookup"><span data-stu-id="1ac4c-132">The type of the whitespace is ignored (a tab or a space between characters will give the same result).</span></span> <span data-ttu-id="1ac4c-133">La quantità di spazi vuoti non è importante: uno o due spazi tra i caratteri offriranno lo stesso risultato.</span><span class="sxs-lookup"><span data-stu-id="1ac4c-133">The amount of whitespace does not matter - one space or two spaces in between characters will give the same result.</span></span>

<span data-ttu-id="1ac4c-134">La ricerca non genera eventi PopulateContextNode.</span><span class="sxs-lookup"><span data-stu-id="1ac4c-134">Search does not generate PopulateContextNode events.</span></span> <span data-ttu-id="1ac4c-135">Verranno cercati solo i tratti già popolati.</span><span class="sxs-lookup"><span data-stu-id="1ac4c-135">Only the strokes that have already been populated will be searched.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ac4c-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1ac4c-136">Requirements</span></span>



| <span data-ttu-id="1ac4c-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ac4c-137">Requirement</span></span> | <span data-ttu-id="1ac4c-138">Valore</span><span class="sxs-lookup"><span data-stu-id="1ac4c-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ac4c-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1ac4c-139">Minimum supported client</span></span><br/> | <span data-ttu-id="1ac4c-140">Solo app desktop Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="1ac4c-140">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="1ac4c-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1ac4c-141">Minimum supported server</span></span><br/> | <span data-ttu-id="1ac4c-142">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="1ac4c-142">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="1ac4c-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1ac4c-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ac4c-144"><dt>IACom.h (richiede anche IACom \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="1ac4c-144"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="1ac4c-145">DLL</span><span class="sxs-lookup"><span data-stu-id="1ac4c-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1ac4c-146"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1ac4c-146"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="1ac4c-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1ac4c-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ac4c-148">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="1ac4c-148">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> </dl>

 

 




