---
title: Messaggio di EM_FINDTEXT (RichEdit. h)
description: Trova il testo in un controllo Rich Edit.
ms.assetid: f19e19a0-d8dd-4d31-b76d-f1f09577dd2d
keywords:
- Controlli di Windows Message EM_FINDTEXT
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
ms.openlocfilehash: 9e50034337f05d2df17af777986136881c503d05
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964396"
---
# <a name="em_findtext-message"></a><span data-ttu-id="d84b9-104">\_Messaggio FindText em</span><span class="sxs-lookup"><span data-stu-id="d84b9-104">EM\_FINDTEXT message</span></span>

<span data-ttu-id="d84b9-105">Trova il testo in un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="d84b9-105">Finds text within a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="d84b9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d84b9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d84b9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d84b9-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d84b9-108">Specificare i parametri dell'operazione di ricerca.</span><span class="sxs-lookup"><span data-stu-id="d84b9-108">Specify the parameters of the search operation.</span></span> <span data-ttu-id="d84b9-109">Il parametro può essere costituito da uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="d84b9-109">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="d84b9-110">Valore</span><span class="sxs-lookup"><span data-stu-id="d84b9-110">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="d84b9-111">Significato</span><span class="sxs-lookup"><span data-stu-id="d84b9-111">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FR_DOWN"></span><span id="fr_down"></span><dl> <span data-ttu-id="d84b9-112"><dt>**FR \_ giù**</dt></span><span class="sxs-lookup"><span data-stu-id="d84b9-112"><dt>**FR\_DOWN**</dt></span></span> </dl>                               | <span data-ttu-id="d84b9-113">Microsoft Rich Edit 2,0 e versioni successive: se impostato, la ricerca viene effettuata dalla fine della selezione corrente fino alla fine del documento.</span><span class="sxs-lookup"><span data-stu-id="d84b9-113">Microsoft Rich Edit 2.0 and later: If set, the search is from the end of the current selection to the end of the document.</span></span> <span data-ttu-id="d84b9-114">Se non è impostato, la ricerca viene effettuata dalla fine della selezione corrente fino all'inizio del documento.</span><span class="sxs-lookup"><span data-stu-id="d84b9-114">If not set, the search is from the end of the current selection to the beginning of the document.</span></span> <br/> <span data-ttu-id="d84b9-115">Microsoft Rich Edit 1,0: il \_ flag fr down viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="d84b9-115">Microsoft Rich Edit 1.0: The FR\_DOWN flag is ignored.</span></span> <span data-ttu-id="d84b9-116">La ricerca è sempre dalla fine della selezione corrente fino alla fine del documento.</span><span class="sxs-lookup"><span data-stu-id="d84b9-116">The search is always from the end of the current selection to the end of the document.</span></span><br/> |
| <span id="FR_MATCHALEFHAMZA"></span><span id="fr_matchalefhamza"></span><dl> <span data-ttu-id="d84b9-117"><dt>**FR \_ MATCHALEFHAMZA**</dt></span><span class="sxs-lookup"><span data-stu-id="d84b9-117"><dt>**FR\_MATCHALEFHAMZA**</dt></span></span> </dl> | <span data-ttu-id="d84b9-118">Microsoft Rich Edit 3,0 e versioni successive: se impostato, la ricerca distingue tra Alef arabi con accenti diversi.</span><span class="sxs-lookup"><span data-stu-id="d84b9-118">Microsoft Rich Edit 3.0 and later: If set, the search differentiates between Arabic alefs with different accents.</span></span> <span data-ttu-id="d84b9-119">Se non è impostato, tutti i Alef vengono confrontati solo con il carattere Alef.</span><span class="sxs-lookup"><span data-stu-id="d84b9-119">If not set, all alefs are matched by the alef character alone.</span></span> <br/>                                                                                                                                                                                                      |
| <span id="FR_MATCHDIAC"></span><span id="fr_matchdiac"></span><dl> <span data-ttu-id="d84b9-120"><dt>**FR \_ MATCHDIAC**</dt></span><span class="sxs-lookup"><span data-stu-id="d84b9-120"><dt>**FR\_MATCHDIAC**</dt></span></span> </dl>                | <span data-ttu-id="d84b9-121">Microsoft Rich Edit 3,0 e versioni successive: se impostato, l'operazione di ricerca considera i segni diacritici arabi e ebraici.</span><span class="sxs-lookup"><span data-stu-id="d84b9-121">Microsoft Rich Edit 3.0 and later: If set, the search operation considers Arabic and Hebrew diacritical marks.</span></span> <span data-ttu-id="d84b9-122">Se non è impostato, i segni diacritici vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="d84b9-122">If not set, diacritical marks are ignored.</span></span> <br/>                                                                                                                                                                                                                             |
| <span id="FR_MATCHKASHIDA"></span><span id="fr_matchkashida"></span><dl> <span data-ttu-id="d84b9-123"><dt>**FR \_ MATCHKASHIDA**</dt></span><span class="sxs-lookup"><span data-stu-id="d84b9-123"><dt>**FR\_MATCHKASHIDA**</dt></span></span> </dl>       | <span data-ttu-id="d84b9-124">Microsoft Rich Edit 3,0 e versioni successive: se impostato, l'operazione di ricerca considera i Kashida Arabi.</span><span class="sxs-lookup"><span data-stu-id="d84b9-124">Microsoft Rich Edit 3.0 and later: If set, the search operation considers Arabic kashidas.</span></span> <span data-ttu-id="d84b9-125">Se non è impostato, Kashida vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="d84b9-125">If not set, kashidas are ignored.</span></span> <br/>                                                                                                                                                                                                                                                          |
| <span id="FR_MATCHWIDTH"></span><span id="fr_matchwidth"></span><dl> <span data-ttu-id="d84b9-126"><dt>**FR \_ MATCHWIDTH**</dt></span><span class="sxs-lookup"><span data-stu-id="d84b9-126"><dt>**FR\_MATCHWIDTH**</dt></span></span> </dl>             | <span data-ttu-id="d84b9-127">Windows 8: se impostato, le versioni a byte singolo e a byte doppio dello stesso carattere sono considerate non uguali.</span><span class="sxs-lookup"><span data-stu-id="d84b9-127">Windows 8: If set, single-byte and double-byte versions of the same character are considered to be not equal.</span></span><br/>                                                                                                                                                                                                                                                                          |
| <span id="FR_WHOLEWORD"></span><span id="fr_wholeword"></span><dl> <span data-ttu-id="d84b9-128"><dt>**FR \_ WHOLEWORD**</dt></span><span class="sxs-lookup"><span data-stu-id="d84b9-128"><dt>**FR\_WHOLEWORD**</dt></span></span> </dl>                | <span data-ttu-id="d84b9-129">Se impostato, l'operazione cerca solo le parole intere che corrispondono alla stringa di ricerca.</span><span class="sxs-lookup"><span data-stu-id="d84b9-129">If set, the operation searches only for whole words that match the search string.</span></span> <span data-ttu-id="d84b9-130">Se non impostato, l'operazione Cerca anche frammenti di parola che corrispondono alla stringa di ricerca.</span><span class="sxs-lookup"><span data-stu-id="d84b9-130">If not set, the operation also searches for word fragments that match the search string.</span></span><br/>                                                                                                                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="d84b9-131">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d84b9-131">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d84b9-132">Struttura [**FindText**](/windows/win32/api/richedit/ns-richedit-findtexta) che contiene informazioni sull'operazione di ricerca.</span><span class="sxs-lookup"><span data-stu-id="d84b9-132">A [**FINDTEXT**](/windows/win32/api/richedit/ns-richedit-findtexta) structure containing information about the find operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d84b9-133">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d84b9-133">Return value</span></span>

<span data-ttu-id="d84b9-134">Se viene trovata la stringa di destinazione, il valore restituito è la posizione in base zero del primo carattere della corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="d84b9-134">If the target string is found, the return value is the zero-based position of the first character of the match.</span></span> <span data-ttu-id="d84b9-135">Se la destinazione non viene trovata, il valore restituito è-1.</span><span class="sxs-lookup"><span data-stu-id="d84b9-135">If the target is not found, the return value is -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="d84b9-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="d84b9-136">Remarks</span></span>

<span data-ttu-id="d84b9-137">Il membro **cpMin** di **FindText. CTO Intrac** specifica sempre il punto iniziale della ricerca e **cpMax** specifica il punto finale.</span><span class="sxs-lookup"><span data-stu-id="d84b9-137">The **cpMin** member of **FINDTEXT.chrg** always specifies the starting-point of the search, and **cpMax** specifies the end point.</span></span> <span data-ttu-id="d84b9-138">Quando si esegue la ricerca indietro, **cpMin** deve essere uguale o maggiore di **cpMax**.</span><span class="sxs-lookup"><span data-stu-id="d84b9-138">When searching backward, **cpMin** must be equal to or greater than **cpMax**.</span></span> <span data-ttu-id="d84b9-139">Quando si esegue la ricerca in futuro, un valore pari a-1 in **cpMax** estende l'intervallo di ricerca alla fine del testo.</span><span class="sxs-lookup"><span data-stu-id="d84b9-139">When searching forward, a value of -1 in **cpMax** extends the search range to the end of the text.</span></span>

## <a name="requirements"></a><span data-ttu-id="d84b9-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d84b9-140">Requirements</span></span>



| <span data-ttu-id="d84b9-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="d84b9-141">Requirement</span></span> | <span data-ttu-id="d84b9-142">Valore</span><span class="sxs-lookup"><span data-stu-id="d84b9-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d84b9-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d84b9-143">Minimum supported client</span></span><br/> | <span data-ttu-id="d84b9-144">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d84b9-144">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d84b9-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d84b9-145">Minimum supported server</span></span><br/> | <span data-ttu-id="d84b9-146">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d84b9-146">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d84b9-147">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d84b9-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="d84b9-148"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="d84b9-148"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d84b9-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d84b9-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d84b9-150">**FINDTEXT**</span><span class="sxs-lookup"><span data-stu-id="d84b9-150">**FINDTEXT**</span></span>](/windows/win32/api/richedit/ns-richedit-findtexta)
</dt> </dl>

 

 





