---
title: EM_FINDTEXTEX messaggio (Richedit.h)
description: "EM_FINDTEXTEX messaggio: trova testo all'interno di un controllo Rich Edit."
ms.assetid: f1bf925b-2776-40b8-9d05-8484daf8d989
keywords:
- EM_FINDTEXTEX messaggio Controlli Windows
topic_type:
- apiref
api_name:
- EM_FINDTEXTEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2158dabf9ea17d1bd4cac48454bdbb4056765752
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109839"
---
# <a name="em_findtextex-message"></a><span data-ttu-id="b864f-104">Messaggio \_ EM FINDTEXTEX</span><span class="sxs-lookup"><span data-stu-id="b864f-104">EM\_FINDTEXTEX message</span></span>

<span data-ttu-id="b864f-105">Trova il testo all'interno di un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="b864f-105">Finds text within a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="b864f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b864f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b864f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b864f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b864f-108">Specifica il comportamento dell'operazione di ricerca.</span><span class="sxs-lookup"><span data-stu-id="b864f-108">Specifies the behavior of the search operation.</span></span> <span data-ttu-id="b864f-109">Questo parametro può essere uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="b864f-109">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="b864f-110">Valore</span><span class="sxs-lookup"><span data-stu-id="b864f-110">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="b864f-111">Significato</span><span class="sxs-lookup"><span data-stu-id="b864f-111">Meaning</span></span>                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FR_DOWN"></span><span id="fr_down"></span><dl> <span data-ttu-id="b864f-112"><dt>**FR \_ DOWN**</dt></span><span class="sxs-lookup"><span data-stu-id="b864f-112"><dt>**FR\_DOWN**</dt></span></span> </dl>                               | <span data-ttu-id="b864f-113">Microsoft Rich Edit 2.0 e versioni successive: se impostato, la ricerca viene inoltrata da **FINDTEXTEX.chrg.cpMin**; se non è impostata, la ricerca è all'indietro rispetto **a FINDTEXTEX.chrg.cpMin**.</span><span class="sxs-lookup"><span data-stu-id="b864f-113">Microsoft Rich Edit 2.0 and later: If set, the search is forward from **FINDTEXTEX.chrg.cpMin**; if not set, the search is backward from **FINDTEXTEX.chrg.cpMin**.</span></span> <br/> <span data-ttu-id="b864f-114">Microsoft Rich Edit 1.0: il flag FR \_ DOWN viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="b864f-114">Microsoft Rich Edit 1.0: The FR\_DOWN flag is ignored.</span></span> <span data-ttu-id="b864f-115">La ricerca è sempre in avanti.</span><span class="sxs-lookup"><span data-stu-id="b864f-115">The search is always forward.</span></span><br/> |
| <span id="FR_MATCHALEFHAMZA"></span><span id="fr_matchalefhamza"></span><dl> <span data-ttu-id="b864f-116"><dt>**FR \_ MATCHALEFHAMZA**</dt></span><span class="sxs-lookup"><span data-stu-id="b864f-116"><dt>**FR\_MATCHALEFHAMZA**</dt></span></span> </dl> | <span data-ttu-id="b864f-117">Microsoft Rich Edit 3.0 e versioni successive: se impostata, la ricerca distingue tra alefs arabo ed ebraico con accenti diversi.</span><span class="sxs-lookup"><span data-stu-id="b864f-117">Microsoft Rich Edit 3.0 and later: If set, the search differentiates between Arabic and Hebrew alefs with different accents.</span></span> <span data-ttu-id="b864f-118">Se non è impostato, tutte le alef vengono abbinate solo dal carattere alef.</span><span class="sxs-lookup"><span data-stu-id="b864f-118">If not set, all alefs are matched by the alef character alone.</span></span> <br/>                                                                         |
| <span id="FR_MATCHCASE"></span><span id="fr_matchcase"></span><dl> <span data-ttu-id="b864f-119"><dt>**FR \_ MATCHCASE**</dt></span><span class="sxs-lookup"><span data-stu-id="b864f-119"><dt>**FR\_MATCHCASE**</dt></span></span> </dl>                | <span data-ttu-id="b864f-120">Se impostata, l'operazione di ricerca fa distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="b864f-120">If set, the search operation is case-sensitive.</span></span> <span data-ttu-id="b864f-121">Se non è impostata, l'operazione di ricerca non fa distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="b864f-121">If not set, the search operation is case-insensitive.</span></span> <br/>                                                                                                                                                               |
| <span id="FR_MATCHDIAC"></span><span id="fr_matchdiac"></span><dl> <span data-ttu-id="b864f-122"><dt>**FR \_ MATCHDIAC**</dt></span><span class="sxs-lookup"><span data-stu-id="b864f-122"><dt>**FR\_MATCHDIAC**</dt></span></span> </dl>                | <span data-ttu-id="b864f-123">Microsoft Rich Edit 3.0 e versioni successive: se impostato, l'operazione di ricerca considera i segni diacritici arabo ed ebraico.</span><span class="sxs-lookup"><span data-stu-id="b864f-123">Microsoft Rich Edit 3.0 and later: If set, the search operation considers Arabic and Hebrew diacritical marks.</span></span> <span data-ttu-id="b864f-124">Se non è impostato, i segni diacritici vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="b864f-124">If not set, diacritical marks are ignored.</span></span> <br/>                                                                                                           |
| <span id="FR_MATCHKASHIDA"></span><span id="fr_matchkashida"></span><dl> <span data-ttu-id="b864f-125"><dt>**FR \_ MATCHKASHIDA**</dt></span><span class="sxs-lookup"><span data-stu-id="b864f-125"><dt>**FR\_MATCHKASHIDA**</dt></span></span> </dl>       | <span data-ttu-id="b864f-126">Microsoft Rich Edit 3.0 e versioni successive: se impostato, l'operazione di ricerca considera le kashida arabo ed ebraico.</span><span class="sxs-lookup"><span data-stu-id="b864f-126">Microsoft Rich Edit 3.0 and later: If set, the search operation considers Arabic and Hebrew kashidas.</span></span> <span data-ttu-id="b864f-127">Se non impostato, i kashida vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="b864f-127">If not set, kashidas are ignored.</span></span> <br/>                                                                                                                             |
| <span id="FR_WHOLEWORD"></span><span id="fr_wholeword"></span><dl> <span data-ttu-id="b864f-128"><dt>**FR \_ WHOLEWORD**</dt></span><span class="sxs-lookup"><span data-stu-id="b864f-128"><dt>**FR\_WHOLEWORD**</dt></span></span> </dl>                | <span data-ttu-id="b864f-129">Se impostata, l'operazione cerca solo parole intere che corrispondono alla stringa di ricerca.</span><span class="sxs-lookup"><span data-stu-id="b864f-129">If set, the operation searches only for whole words that match the search string.</span></span> <span data-ttu-id="b864f-130">Se non è impostata, l'operazione cerca anche frammenti di parole che corrispondono alla stringa di ricerca.</span><span class="sxs-lookup"><span data-stu-id="b864f-130">If not set, the operation also searches for word fragments that match the search string.</span></span><br/>                                                                                           |



 

</dd> <dt>

<span data-ttu-id="b864f-131">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b864f-131">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b864f-132">Struttura [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) contenente informazioni sull'operazione di ricerca.</span><span class="sxs-lookup"><span data-stu-id="b864f-132">A [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) structure containing information about the find operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b864f-133">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b864f-133">Return value</span></span>

<span data-ttu-id="b864f-134">Se viene trovata la stringa di destinazione, il valore restituito è la posizione in base zero del primo carattere della corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="b864f-134">If the target string is found, the return value is the zero-based position of the first character of the match.</span></span> <span data-ttu-id="b864f-135">Se la destinazione non viene trovata, il valore restituito è -1.</span><span class="sxs-lookup"><span data-stu-id="b864f-135">If the target is not found, the return value is -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="b864f-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="b864f-136">Remarks</span></span>

<span data-ttu-id="b864f-137">Usare questo messaggio per trovare stringhe ANSI.</span><span class="sxs-lookup"><span data-stu-id="b864f-137">Use this message to find ANSI strings.</span></span> <span data-ttu-id="b864f-138">Per Unicode, usare [**EM \_ FINDTEXTEXW**](em-findtextexw.md).</span><span class="sxs-lookup"><span data-stu-id="b864f-138">For Unicode, use [**EM\_FINDTEXTEXW**](em-findtextexw.md).</span></span>

<span data-ttu-id="b864f-139">Il **membro cpMin** di **FINDTEXTEX.chrg** specifica sempre il punto iniziale della ricerca e **cpMax** specifica il punto finale.</span><span class="sxs-lookup"><span data-stu-id="b864f-139">The **cpMin** member of **FINDTEXTEX.chrg** always specifies the starting-point of the search, and **cpMax** specifies the end point.</span></span> <span data-ttu-id="b864f-140">Quando si esegue la ricerca **all'indietro, cpMin** deve essere uguale o maggiore di **cpMax**.</span><span class="sxs-lookup"><span data-stu-id="b864f-140">When searching backward, **cpMin** must be equal to or greater than **cpMax**.</span></span> <span data-ttu-id="b864f-141">Durante la ricerca in avanti, il valore -1 in **cpMax** estende l'intervallo di ricerca alla fine del testo.</span><span class="sxs-lookup"><span data-stu-id="b864f-141">When searching forward, a value of -1 in **cpMax** extends the search range to the end of the text.</span></span>

<span data-ttu-id="b864f-142">Se l'operazione di ricerca trova una corrispondenza, il membro **chrgText** della struttura [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) restituisce l'intervallo di posizioni di caratteri che contiene il testo corrispondente.</span><span class="sxs-lookup"><span data-stu-id="b864f-142">If the search operation finds a match, the **chrgText** member of the [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) structure returns the range of character positions that contains the matching text.</span></span>

## <a name="requirements"></a><span data-ttu-id="b864f-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b864f-143">Requirements</span></span>



| <span data-ttu-id="b864f-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="b864f-144">Requirement</span></span> | <span data-ttu-id="b864f-145">Valore</span><span class="sxs-lookup"><span data-stu-id="b864f-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b864f-146">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b864f-146">Minimum supported client</span></span><br/> | <span data-ttu-id="b864f-147">Solo app desktop di Windows \[ Vista\]</span><span class="sxs-lookup"><span data-stu-id="b864f-147">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b864f-148">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b864f-148">Minimum supported server</span></span><br/> | <span data-ttu-id="b864f-149">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="b864f-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b864f-150">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b864f-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="b864f-151"><dt>Richedit.h</dt></span><span class="sxs-lookup"><span data-stu-id="b864f-151"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b864f-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b864f-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b864f-153">**EM \_ FINDTEXT**</span><span class="sxs-lookup"><span data-stu-id="b864f-153">**EM\_FINDTEXT**</span></span>](em-findtext.md)
</dt> </dl>

 

 





