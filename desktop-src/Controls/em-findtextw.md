---
title: Messaggio di EM_FINDTEXTW (RichEdit. h)
description: Trova il testo Unicode in un controllo Rich Edit.
ms.assetid: 0c1579f5-3b37-4e28-86a2-f4e03e195f38
keywords:
- Controlli di Windows Message EM_FINDTEXTW
topic_type:
- apiref
api_name:
- EM_FINDTEXTW
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73e8bae60269ab3ddb84a17c285c243e00d8117c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742826"
---
# <a name="em_findtextw-message"></a><span data-ttu-id="c6a78-104">\_Messaggio FINDTEXTW em</span><span class="sxs-lookup"><span data-stu-id="c6a78-104">EM\_FINDTEXTW message</span></span>

<span data-ttu-id="c6a78-105">Trova il testo Unicode in un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="c6a78-105">Finds Unicode text within a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="c6a78-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c6a78-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6a78-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c6a78-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c6a78-108">Specifica i parametri dell'operazione di ricerca.</span><span class="sxs-lookup"><span data-stu-id="c6a78-108">Specifies the parameters of the search operation.</span></span> <span data-ttu-id="c6a78-109">Il parametro può essere costituito da uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="c6a78-109">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="c6a78-110">Valore</span><span class="sxs-lookup"><span data-stu-id="c6a78-110">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="c6a78-111">Significato</span><span class="sxs-lookup"><span data-stu-id="c6a78-111">Meaning</span></span>                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FR_DOWN"></span><span id="fr_down"></span><dl> <span data-ttu-id="c6a78-112"><dt>**FR \_ giù**</dt></span><span class="sxs-lookup"><span data-stu-id="c6a78-112"><dt>**FR\_DOWN**</dt></span></span> </dl>                               | <span data-ttu-id="c6a78-113">Se impostato, l'operazione esegue la ricerca dalla fine della selezione corrente fino alla fine del documento.</span><span class="sxs-lookup"><span data-stu-id="c6a78-113">If set, the operation searches from the end of the current selection to the end of the document.</span></span> <span data-ttu-id="c6a78-114">Se non impostato, l'operazione esegue la ricerca dalla fine della selezione corrente fino all'inizio del documento.</span><span class="sxs-lookup"><span data-stu-id="c6a78-114">If not set, the operation searches from the end of the current selection to the beginning of the document.</span></span><br/> |
| <span id="FR_MATCHALEFHAMZA"></span><span id="fr_matchalefhamza"></span><dl> <span data-ttu-id="c6a78-115"><dt>**FR \_ MATCHALEFHAMZA**</dt></span><span class="sxs-lookup"><span data-stu-id="c6a78-115"><dt>**FR\_MATCHALEFHAMZA**</dt></span></span> </dl> | <span data-ttu-id="c6a78-116">Per impostazione predefinita, tutti i Alef arabi e ebraici con accenti diversi corrispondono al carattere Alef.</span><span class="sxs-lookup"><span data-stu-id="c6a78-116">By default, Arabic and Hebrew alefs with different accents are all matched by the alef character.</span></span> <span data-ttu-id="c6a78-117">Impostare questo flag se si desidera che la ricerca differenzi tra alef con accenti diversi.</span><span class="sxs-lookup"><span data-stu-id="c6a78-117">Set this flag if you want the search to differentiate between alefs with different accents.</span></span><br/>               |
| <span id="FR_MATCHCASE"></span><span id="fr_matchcase"></span><dl> <span data-ttu-id="c6a78-118"><dt>**FR \_ MATCHCASE**</dt></span><span class="sxs-lookup"><span data-stu-id="c6a78-118"><dt>**FR\_MATCHCASE**</dt></span></span> </dl>                | <span data-ttu-id="c6a78-119">Se impostato, l'operazione di ricerca fa distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="c6a78-119">If set, the search operation is case-sensitive.</span></span> <span data-ttu-id="c6a78-120">Se non è impostato, l'operazione di ricerca non fa distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="c6a78-120">If not set, the search operation is case-insensitive.</span></span><br/>                                                                                                       |
| <span id="FR_MATCHDIAC"></span><span id="fr_matchdiac"></span><dl> <span data-ttu-id="c6a78-121"><dt>**FR \_ MATCHDIAC**</dt></span><span class="sxs-lookup"><span data-stu-id="c6a78-121"><dt>**FR\_MATCHDIAC**</dt></span></span> </dl>                | <span data-ttu-id="c6a78-122">Per impostazione predefinita, i contrassegni diacritici arabi e ebraici vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="c6a78-122">By default, Arabic and Hebrew diacritical marks are ignored.</span></span> <span data-ttu-id="c6a78-123">Impostare questo flag se si desidera che l'operazione di ricerca consideri segni diacritici.</span><span class="sxs-lookup"><span data-stu-id="c6a78-123">Set this flag if you want the search operation to consider diacritical marks.</span></span><br/>                                                                  |
| <span id="FR_MATCHKASHIDA"></span><span id="fr_matchkashida"></span><dl> <span data-ttu-id="c6a78-124"><dt>**FR \_ MATCHKASHIDA**</dt></span><span class="sxs-lookup"><span data-stu-id="c6a78-124"><dt>**FR\_MATCHKASHIDA**</dt></span></span> </dl>       | <span data-ttu-id="c6a78-125">Per impostazione predefinita, i Kashida arabi e ebraici vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="c6a78-125">By default, Arabic and Hebrew kashidas are ignored.</span></span> <span data-ttu-id="c6a78-126">Impostare questo flag se si desidera che l'operazione di ricerca consideri Kashida.</span><span class="sxs-lookup"><span data-stu-id="c6a78-126">Set this flag if you want the search operation to consider kashidas.</span></span><br/>                                                                                    |
| <span id="FR_WHOLEWORD"></span><span id="fr_wholeword"></span><dl> <span data-ttu-id="c6a78-127"><dt>**FR \_ WHOLEWORD**</dt></span><span class="sxs-lookup"><span data-stu-id="c6a78-127"><dt>**FR\_WHOLEWORD**</dt></span></span> </dl>                | <span data-ttu-id="c6a78-128">Se impostato, l'operazione cerca solo le parole intere che corrispondono alla stringa di ricerca.</span><span class="sxs-lookup"><span data-stu-id="c6a78-128">If set, the operation searches only for whole words that match the search string.</span></span> <span data-ttu-id="c6a78-129">Se non impostato, l'operazione Cerca anche frammenti di parola che corrispondono alla stringa di ricerca.</span><span class="sxs-lookup"><span data-stu-id="c6a78-129">If not set, the operation also searches for word fragments that match the search string.</span></span><br/>                                  |



 

</dd> <dt>

<span data-ttu-id="c6a78-130">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c6a78-130">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c6a78-131">Struttura [**FINDTEXTW**](/windows/win32/api/richedit/ns-richedit-findtexta) che contiene informazioni sull'operazione di ricerca.</span><span class="sxs-lookup"><span data-stu-id="c6a78-131">A [**FINDTEXTW**](/windows/win32/api/richedit/ns-richedit-findtexta) structure containing information about the find operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6a78-132">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c6a78-132">Return value</span></span>

<span data-ttu-id="c6a78-133">Se viene trovata la stringa di destinazione, il valore restituito è la posizione in base zero del primo carattere della corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="c6a78-133">If the target string is found, the return value is the zero-based position of the first character of the match.</span></span> <span data-ttu-id="c6a78-134">Se la destinazione non viene trovata, il valore restituito è-1.</span><span class="sxs-lookup"><span data-stu-id="c6a78-134">If the target is not found, the return value is -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6a78-135">Commenti</span><span class="sxs-lookup"><span data-stu-id="c6a78-135">Remarks</span></span>

<span data-ttu-id="c6a78-136">**Em \_ FINDTEXTW** usa la struttura [**FINDTEXTW**](/windows/win32/api/richedit/ns-richedit-findtexta) , mentre [**em \_ FINDTEXTEXW**](em-findtextexw.md) usa la struttura [**FINDTEXTEXW**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) .</span><span class="sxs-lookup"><span data-stu-id="c6a78-136">**EM\_FINDTEXTW** uses the [**FINDTEXTW**](/windows/win32/api/richedit/ns-richedit-findtexta) structure, while [**EM\_FINDTEXTEXW**](em-findtextexw.md) uses the [**FINDTEXTEXW**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) structure.</span></span> <span data-ttu-id="c6a78-137">La differenza consiste nel fatto che **FINDTEXTEXW** restituisce l'intervallo di testo trovato.</span><span class="sxs-lookup"><span data-stu-id="c6a78-137">The difference is that **FINDTEXTEXW** reports back the range of text that was found.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6a78-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c6a78-138">Requirements</span></span>



| <span data-ttu-id="c6a78-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6a78-139">Requirement</span></span> | <span data-ttu-id="c6a78-140">Valore</span><span class="sxs-lookup"><span data-stu-id="c6a78-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c6a78-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c6a78-141">Minimum supported client</span></span><br/> | <span data-ttu-id="c6a78-142">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c6a78-142">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c6a78-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c6a78-143">Minimum supported server</span></span><br/> | <span data-ttu-id="c6a78-144">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c6a78-144">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c6a78-145">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c6a78-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6a78-146"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6a78-146"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6a78-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c6a78-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6a78-148">**\_FINDTEXTEXW em**</span><span class="sxs-lookup"><span data-stu-id="c6a78-148">**EM\_FINDTEXTEXW**</span></span>](em-findtextexw.md)
</dt> </dl>

 

 





