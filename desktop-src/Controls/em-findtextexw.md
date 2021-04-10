---
title: Messaggio di EM_FINDTEXTEXW (RichEdit. h)
description: Trova il testo Unicode in un controllo Rich Edit.
ms.assetid: 7b90ef06-0395-430e-8b5d-b392481a5f70
keywords:
- Controlli di Windows Message EM_FINDTEXTEXW
topic_type:
- apiref
api_name:
- EM_FINDTEXTEXW
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aaf0857e47c6e98f4be6867ca66baef3472766a2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964758"
---
# <a name="em_findtextexw-message"></a><span data-ttu-id="eeab2-104">\_Messaggio FINDTEXTEXW em</span><span class="sxs-lookup"><span data-stu-id="eeab2-104">EM\_FINDTEXTEXW message</span></span>

<span data-ttu-id="eeab2-105">Trova il testo Unicode in un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="eeab2-105">Finds Unicode text within a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="eeab2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="eeab2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eeab2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="eeab2-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eeab2-108">Specifica il comportamento dell'operazione di ricerca.</span><span class="sxs-lookup"><span data-stu-id="eeab2-108">Specifies the behavior of the search operation.</span></span> <span data-ttu-id="eeab2-109">Il parametro può essere costituito da uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="eeab2-109">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="eeab2-110">Valore</span><span class="sxs-lookup"><span data-stu-id="eeab2-110">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="eeab2-111">Significato</span><span class="sxs-lookup"><span data-stu-id="eeab2-111">Meaning</span></span>                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FR_DOWN"></span><span id="fr_down"></span><dl> <span data-ttu-id="eeab2-112"><dt>**FR \_ giù**</dt></span><span class="sxs-lookup"><span data-stu-id="eeab2-112"><dt>**FR\_DOWN**</dt></span></span> </dl>                               | <span data-ttu-id="eeab2-113">Microsoft Rich Edit 2,0 e versioni successive: se impostato, la ricerca è diretta da **FINDTEXTEX. CTO Intrac. cpMin**; Se non è impostato, la ricerca è indietro rispetto a **FINDTEXTEX. CTO Intrac. cpMin**.</span><span class="sxs-lookup"><span data-stu-id="eeab2-113">Microsoft Rich Edit 2.0 and later: If set, the search is forward from **FINDTEXTEX.chrg.cpMin**; if not set, the search is backward from **FINDTEXTEX.chrg.cpMin**.</span></span> <br/> <span data-ttu-id="eeab2-114">Microsoft Rich Edit 1,0: il \_ flag fr down viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="eeab2-114">Microsoft Rich Edit 1.0: The FR\_DOWN flag is ignored.</span></span> <span data-ttu-id="eeab2-115">La ricerca è sempre in futuro.</span><span class="sxs-lookup"><span data-stu-id="eeab2-115">The search is always forward.</span></span><br/> |
| <span id="FR_MATCHALEFHAMZA"></span><span id="fr_matchalefhamza"></span><dl> <span data-ttu-id="eeab2-116"><dt>**FR \_ MATCHALEFHAMZA**</dt></span><span class="sxs-lookup"><span data-stu-id="eeab2-116"><dt>**FR\_MATCHALEFHAMZA**</dt></span></span> </dl> | <span data-ttu-id="eeab2-117">Se impostata, la ricerca distingue tra alef con accenti diversi.</span><span class="sxs-lookup"><span data-stu-id="eeab2-117">If set, the search differentiates between alefs with different accents.</span></span> <span data-ttu-id="eeab2-118">Se non è impostato, le corrispondenze in arabo ed ebraico alef con accenti diversi corrispondono al carattere Alef.</span><span class="sxs-lookup"><span data-stu-id="eeab2-118">If not set, Arabic and Hebrew alefs with different accents are all matched by the alef character.</span></span> <br/>                                                                                           |
| <span id="FR_MATCHCASE"></span><span id="fr_matchcase"></span><dl> <span data-ttu-id="eeab2-119"><dt>**FR \_ MATCHCASE**</dt></span><span class="sxs-lookup"><span data-stu-id="eeab2-119"><dt>**FR\_MATCHCASE**</dt></span></span> </dl>                | <span data-ttu-id="eeab2-120">Se impostato, l'operazione di ricerca fa distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="eeab2-120">If set, the search operation is case-sensitive.</span></span> <span data-ttu-id="eeab2-121">Se non è impostato, l'operazione di ricerca non fa distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="eeab2-121">If not set, the search operation is case-insensitive.</span></span><br/>                                                                                                                                                                |
| <span id="FR_MATCHDIAC"></span><span id="fr_matchdiac"></span><dl> <span data-ttu-id="eeab2-122"><dt>**FR \_ MATCHDIAC**</dt></span><span class="sxs-lookup"><span data-stu-id="eeab2-122"><dt>**FR\_MATCHDIAC**</dt></span></span> </dl>                | <span data-ttu-id="eeab2-123">Se impostato, l'operazione di ricerca considera i segni diacritici.</span><span class="sxs-lookup"><span data-stu-id="eeab2-123">If set, the search operation considers diacritical marks.</span></span> <span data-ttu-id="eeab2-124">Se non impostato, i segni diacritici arabi e ebraici vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="eeab2-124">If not set, Arabic and Hebrew diacritical marks are ignored.</span></span> <br/>                                                                                                                                              |
| <span id="FR_MATCHKASHIDA"></span><span id="fr_matchkashida"></span><dl> <span data-ttu-id="eeab2-125"><dt>**FR \_ MATCHKASHIDA**</dt></span><span class="sxs-lookup"><span data-stu-id="eeab2-125"><dt>**FR\_MATCHKASHIDA**</dt></span></span> </dl>       | <span data-ttu-id="eeab2-126">Se impostato, l'operazione di ricerca prende in considerazione Kashida.</span><span class="sxs-lookup"><span data-stu-id="eeab2-126">If set, the search operation considers kashidas.</span></span> <span data-ttu-id="eeab2-127">Se non impostato, i Kashida arabi e ebraici vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="eeab2-127">If not set, Arabic and Hebrew kashidas are ignored.</span></span> <br/>                                                                                                                                                                |
| <span id="FR_WHOLEWORD"></span><span id="fr_wholeword"></span><dl> <span data-ttu-id="eeab2-128"><dt>**FR \_ WHOLEWORD**</dt></span><span class="sxs-lookup"><span data-stu-id="eeab2-128"><dt>**FR\_WHOLEWORD**</dt></span></span> </dl>                | <span data-ttu-id="eeab2-129">Se impostato, l'operazione cerca solo le parole intere che corrispondono alla stringa di ricerca.</span><span class="sxs-lookup"><span data-stu-id="eeab2-129">If set, the operation searches only for whole words that match the search string.</span></span> <span data-ttu-id="eeab2-130">Se non impostato, l'operazione Cerca anche frammenti di parola che corrispondono alla stringa di ricerca.</span><span class="sxs-lookup"><span data-stu-id="eeab2-130">If not set, the operation also searches for word fragments that match the search string.</span></span><br/>                                                                                           |



 

</dd> <dt>

<span data-ttu-id="eeab2-131">*lParam*</span><span class="sxs-lookup"><span data-stu-id="eeab2-131">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eeab2-132">Struttura [**FINDTEXTEXW**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) che contiene informazioni sull'operazione di ricerca.</span><span class="sxs-lookup"><span data-stu-id="eeab2-132">A [**FINDTEXTEXW**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) structure containing information about the find operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eeab2-133">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="eeab2-133">Return value</span></span>

<span data-ttu-id="eeab2-134">Se viene trovata la stringa di destinazione, il valore restituito è la posizione in base zero del primo carattere della corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="eeab2-134">If the target string is found, the return value is the zero-based position of the first character of the match.</span></span> <span data-ttu-id="eeab2-135">Se la destinazione non viene trovata, il valore restituito è-1.</span><span class="sxs-lookup"><span data-stu-id="eeab2-135">If the target is not found, the return value is -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="eeab2-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="eeab2-136">Remarks</span></span>

<span data-ttu-id="eeab2-137">Utilizzare questo messaggio per trovare stringhe Unicode.</span><span class="sxs-lookup"><span data-stu-id="eeab2-137">Use this message to find Unicode strings.</span></span> <span data-ttu-id="eeab2-138">Per ANSI;, usare [**em \_ FINDTEXTEX**](em-findtextex.md).</span><span class="sxs-lookup"><span data-stu-id="eeab2-138">For ANSI;, use [**EM\_FINDTEXTEX**](em-findtextex.md).</span></span>

<span data-ttu-id="eeab2-139">Il membro **cpMin** di **FINDTEXTEX. CTO Intrac** specifica sempre il punto iniziale della ricerca e **cpMax** specifica il punto finale.</span><span class="sxs-lookup"><span data-stu-id="eeab2-139">The **cpMin** member of **FINDTEXTEX.chrg** always specifies the starting-point of the search, and **cpMax** specifies the end point.</span></span> <span data-ttu-id="eeab2-140">Quando si esegue la ricerca indietro, **cpMin** deve essere uguale o maggiore di **cpMax**.</span><span class="sxs-lookup"><span data-stu-id="eeab2-140">When searching backward, **cpMin** must be equal to or greater than **cpMax**.</span></span> <span data-ttu-id="eeab2-141">Quando si esegue la ricerca in futuro, un valore pari a-1 in **cpMax** estende l'intervallo di ricerca alla fine del testo.</span><span class="sxs-lookup"><span data-stu-id="eeab2-141">When searching forward, a value of -1 in **cpMax** extends the search range to the end of the text.</span></span>

<span data-ttu-id="eeab2-142">Se l'operazione di ricerca trova una corrispondenza, il membro **chrgText** della struttura [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) restituisce l'intervallo di posizioni dei caratteri che contiene il testo corrispondente.</span><span class="sxs-lookup"><span data-stu-id="eeab2-142">If the search operation finds a match, the **chrgText** member of the [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) structure returns the range of character positions that contains the matching text.</span></span>

<span data-ttu-id="eeab2-143">**Em \_ FINDTEXTEXW** usa la struttura [**FINDTEXTEXW**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) , mentre [**em \_ FINDTEXTW**](em-findtextw.md) usa la struttura [**FINDTEXTW**](/windows/win32/api/richedit/ns-richedit-findtexta) .</span><span class="sxs-lookup"><span data-stu-id="eeab2-143">**EM\_FINDTEXTEXW** uses the [**FINDTEXTEXW**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) structure, while [**EM\_FINDTEXTW**](em-findtextw.md) uses the [**FINDTEXTW**](/windows/win32/api/richedit/ns-richedit-findtexta) structure.</span></span> <span data-ttu-id="eeab2-144">La differenza è che **em \_ FINDTEXTEXW** segnala l'intervallo di testo trovato.</span><span class="sxs-lookup"><span data-stu-id="eeab2-144">The difference is that **EM\_FINDTEXTEXW** reports the range of text that was found.</span></span>

## <a name="requirements"></a><span data-ttu-id="eeab2-145">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eeab2-145">Requirements</span></span>



| <span data-ttu-id="eeab2-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="eeab2-146">Requirement</span></span> | <span data-ttu-id="eeab2-147">Valore</span><span class="sxs-lookup"><span data-stu-id="eeab2-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="eeab2-148">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eeab2-148">Minimum supported client</span></span><br/> | <span data-ttu-id="eeab2-149">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="eeab2-149">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="eeab2-150">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eeab2-150">Minimum supported server</span></span><br/> | <span data-ttu-id="eeab2-151">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="eeab2-151">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="eeab2-152">Intestazione</span><span class="sxs-lookup"><span data-stu-id="eeab2-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="eeab2-153"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="eeab2-153"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eeab2-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eeab2-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eeab2-155">**\_FINDTEXTW em**</span><span class="sxs-lookup"><span data-stu-id="eeab2-155">**EM\_FINDTEXTW**</span></span>](em-findtextw.md)
</dt> </dl>

 

 





