---
title: EM_FINDTEXT messaggio (Richedit.h)
description: "EM_FINDTEXT messaggio: trova il testo all'interno di un controllo Rich Edit."
ms.assetid: f19e19a0-d8dd-4d31-b76d-f1f09577dd2d
keywords:
- EM_FINDTEXT messaggio controlli Windows
topic_type:
- apiref
api_name:
- EM_FINDTEXT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 452d4e2534fb05cbbbf4c02ac4146f2f8914c9bb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109849"
---
# <a name="em_findtext-message"></a><span data-ttu-id="391ec-104">Messaggio \_ EM FINDTEXT</span><span class="sxs-lookup"><span data-stu-id="391ec-104">EM\_FINDTEXT message</span></span>

<span data-ttu-id="391ec-105">Trova il testo all'interno di un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="391ec-105">Finds text within a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="391ec-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="391ec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="391ec-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="391ec-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="391ec-108">Specificare i parametri dell'operazione di ricerca.</span><span class="sxs-lookup"><span data-stu-id="391ec-108">Specify the parameters of the search operation.</span></span> <span data-ttu-id="391ec-109">Questo parametro può essere uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="391ec-109">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="391ec-110">Valore</span><span class="sxs-lookup"><span data-stu-id="391ec-110">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="391ec-111">Significato</span><span class="sxs-lookup"><span data-stu-id="391ec-111">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FR_DOWN"></span><span id="fr_down"></span><dl> <span data-ttu-id="391ec-112"><dt>**FR \_ DOWN**</dt></span><span class="sxs-lookup"><span data-stu-id="391ec-112"><dt>**FR\_DOWN**</dt></span></span> </dl>                               | <span data-ttu-id="391ec-113">Microsoft Rich Edit 2.0 e versioni successive: se impostato, la ricerca viene effettuata dalla fine della selezione corrente alla fine del documento.</span><span class="sxs-lookup"><span data-stu-id="391ec-113">Microsoft Rich Edit 2.0 and later: If set, the search is from the end of the current selection to the end of the document.</span></span> <span data-ttu-id="391ec-114">Se non è impostata, la ricerca viene effettuata dalla fine della selezione corrente all'inizio del documento.</span><span class="sxs-lookup"><span data-stu-id="391ec-114">If not set, the search is from the end of the current selection to the beginning of the document.</span></span> <br/> <span data-ttu-id="391ec-115">Microsoft Rich Edit 1.0: il flag FR \_ DOWN viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="391ec-115">Microsoft Rich Edit 1.0: The FR\_DOWN flag is ignored.</span></span> <span data-ttu-id="391ec-116">La ricerca viene sempre effettuata dalla fine della selezione corrente alla fine del documento.</span><span class="sxs-lookup"><span data-stu-id="391ec-116">The search is always from the end of the current selection to the end of the document.</span></span><br/> |
| <span id="FR_MATCHALEFHAMZA"></span><span id="fr_matchalefhamza"></span><dl> <span data-ttu-id="391ec-117"><dt>**FR \_ MATCHALEFHAMZA**</dt></span><span class="sxs-lookup"><span data-stu-id="391ec-117"><dt>**FR\_MATCHALEFHAMZA**</dt></span></span> </dl> | <span data-ttu-id="391ec-118">Microsoft Rich Edit 3.0 e versioni successive: se impostata, la ricerca distingue tra alefs arabi con accenti diversi.</span><span class="sxs-lookup"><span data-stu-id="391ec-118">Microsoft Rich Edit 3.0 and later: If set, the search differentiates between Arabic alefs with different accents.</span></span> <span data-ttu-id="391ec-119">Se non è impostato, tutte le alef vengono abbinate solo dal carattere alef.</span><span class="sxs-lookup"><span data-stu-id="391ec-119">If not set, all alefs are matched by the alef character alone.</span></span> <br/>                                                                                                                                                                                                      |
| <span id="FR_MATCHDIAC"></span><span id="fr_matchdiac"></span><dl> <span data-ttu-id="391ec-120"><dt>**FR \_ MATCHDIAC**</dt></span><span class="sxs-lookup"><span data-stu-id="391ec-120"><dt>**FR\_MATCHDIAC**</dt></span></span> </dl>                | <span data-ttu-id="391ec-121">Microsoft Rich Edit 3.0 e versioni successive: se impostato, l'operazione di ricerca considera i segni diacritici arabo ed ebraico.</span><span class="sxs-lookup"><span data-stu-id="391ec-121">Microsoft Rich Edit 3.0 and later: If set, the search operation considers Arabic and Hebrew diacritical marks.</span></span> <span data-ttu-id="391ec-122">Se non è impostato, i segni diacritici vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="391ec-122">If not set, diacritical marks are ignored.</span></span> <br/>                                                                                                                                                                                                                             |
| <span id="FR_MATCHKASHIDA"></span><span id="fr_matchkashida"></span><dl> <span data-ttu-id="391ec-123"><dt>**FR \_ MATCHKASHIDA**</dt></span><span class="sxs-lookup"><span data-stu-id="391ec-123"><dt>**FR\_MATCHKASHIDA**</dt></span></span> </dl>       | <span data-ttu-id="391ec-124">Microsoft Rich Edit 3.0 e versioni successive: se impostato, l'operazione di ricerca considera i kashida arabi.</span><span class="sxs-lookup"><span data-stu-id="391ec-124">Microsoft Rich Edit 3.0 and later: If set, the search operation considers Arabic kashidas.</span></span> <span data-ttu-id="391ec-125">Se non impostato, i kashida vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="391ec-125">If not set, kashidas are ignored.</span></span> <br/>                                                                                                                                                                                                                                                          |
| <span id="FR_MATCHWIDTH"></span><span id="fr_matchwidth"></span><dl> <span data-ttu-id="391ec-126"><dt>**FR \_ MATCHWIDTH**</dt></span><span class="sxs-lookup"><span data-stu-id="391ec-126"><dt>**FR\_MATCHWIDTH**</dt></span></span> </dl>             | <span data-ttu-id="391ec-127">Windows 8: se impostata, le versioni a byte singolo e a byte doppio dello stesso carattere vengono considerate non uguali.</span><span class="sxs-lookup"><span data-stu-id="391ec-127">Windows 8: If set, single-byte and double-byte versions of the same character are considered to be not equal.</span></span><br/>                                                                                                                                                                                                                                                                          |
| <span id="FR_WHOLEWORD"></span><span id="fr_wholeword"></span><dl> <span data-ttu-id="391ec-128"><dt>**FR \_ WHOLEWORD**</dt></span><span class="sxs-lookup"><span data-stu-id="391ec-128"><dt>**FR\_WHOLEWORD**</dt></span></span> </dl>                | <span data-ttu-id="391ec-129">Se impostata, l'operazione cerca solo parole intere che corrispondono alla stringa di ricerca.</span><span class="sxs-lookup"><span data-stu-id="391ec-129">If set, the operation searches only for whole words that match the search string.</span></span> <span data-ttu-id="391ec-130">Se non impostata, l'operazione cerca anche i frammenti di parole che corrispondono alla stringa di ricerca.</span><span class="sxs-lookup"><span data-stu-id="391ec-130">If not set, the operation also searches for word fragments that match the search string.</span></span><br/>                                                                                                                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="391ec-131">*lParam*</span><span class="sxs-lookup"><span data-stu-id="391ec-131">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="391ec-132">Struttura [**FINDTEXT**](/windows/win32/api/richedit/ns-richedit-findtexta) contenente informazioni sull'operazione di ricerca.</span><span class="sxs-lookup"><span data-stu-id="391ec-132">A [**FINDTEXT**](/windows/win32/api/richedit/ns-richedit-findtexta) structure containing information about the find operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="391ec-133">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="391ec-133">Return value</span></span>

<span data-ttu-id="391ec-134">Se viene trovata la stringa di destinazione, il valore restituito è la posizione in base zero del primo carattere della corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="391ec-134">If the target string is found, the return value is the zero-based position of the first character of the match.</span></span> <span data-ttu-id="391ec-135">Se la destinazione non viene trovata, il valore restituito è -1.</span><span class="sxs-lookup"><span data-stu-id="391ec-135">If the target is not found, the return value is -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="391ec-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="391ec-136">Remarks</span></span>

<span data-ttu-id="391ec-137">Il **membro cpMin** di **FINDTEXT.chrg** specifica sempre il punto iniziale della ricerca e **cpMax** specifica il punto finale.</span><span class="sxs-lookup"><span data-stu-id="391ec-137">The **cpMin** member of **FINDTEXT.chrg** always specifies the starting-point of the search, and **cpMax** specifies the end point.</span></span> <span data-ttu-id="391ec-138">Quando si esegue una ricerca **all'indietro, cpMin** deve essere uguale o maggiore di **cpMax**.</span><span class="sxs-lookup"><span data-stu-id="391ec-138">When searching backward, **cpMin** must be equal to or greater than **cpMax**.</span></span> <span data-ttu-id="391ec-139">Durante la ricerca in avanti, il valore -1 in **cpMax** estende l'intervallo di ricerca alla fine del testo.</span><span class="sxs-lookup"><span data-stu-id="391ec-139">When searching forward, a value of -1 in **cpMax** extends the search range to the end of the text.</span></span>

## <a name="requirements"></a><span data-ttu-id="391ec-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="391ec-140">Requirements</span></span>



| <span data-ttu-id="391ec-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="391ec-141">Requirement</span></span> | <span data-ttu-id="391ec-142">Valore</span><span class="sxs-lookup"><span data-stu-id="391ec-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="391ec-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="391ec-143">Minimum supported client</span></span><br/> | <span data-ttu-id="391ec-144">Solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="391ec-144">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="391ec-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="391ec-145">Minimum supported server</span></span><br/> | <span data-ttu-id="391ec-146">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="391ec-146">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="391ec-147">Intestazione</span><span class="sxs-lookup"><span data-stu-id="391ec-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="391ec-148"><dt>Richedit.h</dt></span><span class="sxs-lookup"><span data-stu-id="391ec-148"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="391ec-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="391ec-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="391ec-150">**Findtext**</span><span class="sxs-lookup"><span data-stu-id="391ec-150">**FINDTEXT**</span></span>](/windows/win32/api/richedit/ns-richedit-findtexta)
</dt> </dl>

 

 





