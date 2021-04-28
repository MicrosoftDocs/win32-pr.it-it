---
title: EM_FINDTEXTW messaggio (Richedit.h)
description: "EM_FINDTEXTW messaggio: trova testo Unicode all'interno di un controllo Rich Edit."
ms.assetid: 0c1579f5-3b37-4e28-86a2-f4e03e195f38
keywords:
- EM_FINDTEXTW messaggio Controlli Windows
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
ms.openlocfilehash: 325ff948c4c8f03e8051248f15928d8e8c56e52f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109799"
---
# <a name="em_findtextw-message"></a><span data-ttu-id="34b46-104">Messaggio \_ EM FINDTEXTW</span><span class="sxs-lookup"><span data-stu-id="34b46-104">EM\_FINDTEXTW message</span></span>

<span data-ttu-id="34b46-105">Trova testo Unicode all'interno di un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="34b46-105">Finds Unicode text within a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="34b46-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="34b46-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34b46-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="34b46-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="34b46-108">Specifica i parametri dell'operazione di ricerca.</span><span class="sxs-lookup"><span data-stu-id="34b46-108">Specifies the parameters of the search operation.</span></span> <span data-ttu-id="34b46-109">Questo parametro può essere uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="34b46-109">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="34b46-110">Valore</span><span class="sxs-lookup"><span data-stu-id="34b46-110">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="34b46-111">Significato</span><span class="sxs-lookup"><span data-stu-id="34b46-111">Meaning</span></span>                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FR_DOWN"></span><span id="fr_down"></span><dl> <span data-ttu-id="34b46-112"><dt>**FR \_ DOWN**</dt></span><span class="sxs-lookup"><span data-stu-id="34b46-112"><dt>**FR\_DOWN**</dt></span></span> </dl>                               | <span data-ttu-id="34b46-113">Se impostata, l'operazione cerca dalla fine della selezione corrente alla fine del documento.</span><span class="sxs-lookup"><span data-stu-id="34b46-113">If set, the operation searches from the end of the current selection to the end of the document.</span></span> <span data-ttu-id="34b46-114">Se non è impostata, l'operazione cerca dalla fine della selezione corrente all'inizio del documento.</span><span class="sxs-lookup"><span data-stu-id="34b46-114">If not set, the operation searches from the end of the current selection to the beginning of the document.</span></span><br/> |
| <span id="FR_MATCHALEFHAMZA"></span><span id="fr_matchalefhamza"></span><dl> <span data-ttu-id="34b46-115"><dt>**FR \_ MATCHALEFHAMZA**</dt></span><span class="sxs-lookup"><span data-stu-id="34b46-115"><dt>**FR\_MATCHALEFHAMZA**</dt></span></span> </dl> | <span data-ttu-id="34b46-116">Per impostazione predefinita, le alef arabo ed ebraico con accenti diversi vengono tutte abbinate dal carattere alef.</span><span class="sxs-lookup"><span data-stu-id="34b46-116">By default, Arabic and Hebrew alefs with different accents are all matched by the alef character.</span></span> <span data-ttu-id="34b46-117">Impostare questo flag se si vuole che la ricerca distinzioni tra alefs con accenti diversi.</span><span class="sxs-lookup"><span data-stu-id="34b46-117">Set this flag if you want the search to differentiate between alefs with different accents.</span></span><br/>               |
| <span id="FR_MATCHCASE"></span><span id="fr_matchcase"></span><dl> <span data-ttu-id="34b46-118"><dt>**FR \_ MATCHCASE**</dt></span><span class="sxs-lookup"><span data-stu-id="34b46-118"><dt>**FR\_MATCHCASE**</dt></span></span> </dl>                | <span data-ttu-id="34b46-119">Se impostata, l'operazione di ricerca fa distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="34b46-119">If set, the search operation is case-sensitive.</span></span> <span data-ttu-id="34b46-120">Se non è impostata, l'operazione di ricerca non fa distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="34b46-120">If not set, the search operation is case-insensitive.</span></span><br/>                                                                                                       |
| <span id="FR_MATCHDIAC"></span><span id="fr_matchdiac"></span><dl> <span data-ttu-id="34b46-121"><dt>**FR \_ MATCHDIAC**</dt></span><span class="sxs-lookup"><span data-stu-id="34b46-121"><dt>**FR\_MATCHDIAC**</dt></span></span> </dl>                | <span data-ttu-id="34b46-122">Per impostazione predefinita, i segni diacritici arabo ed ebraico vengono ignorati.</span><span class="sxs-lookup"><span data-stu-id="34b46-122">By default, Arabic and Hebrew diacritical marks are ignored.</span></span> <span data-ttu-id="34b46-123">Impostare questo flag se si vuole che l'operazione di ricerca consideri i segni diacritici.</span><span class="sxs-lookup"><span data-stu-id="34b46-123">Set this flag if you want the search operation to consider diacritical marks.</span></span><br/>                                                                  |
| <span id="FR_MATCHKASHIDA"></span><span id="fr_matchkashida"></span><dl> <span data-ttu-id="34b46-124"><dt>**FR \_ MATCHKASHIDA**</dt></span><span class="sxs-lookup"><span data-stu-id="34b46-124"><dt>**FR\_MATCHKASHIDA**</dt></span></span> </dl>       | <span data-ttu-id="34b46-125">Per impostazione predefinita, le kashida in arabo ed ebraico vengono ignorate.</span><span class="sxs-lookup"><span data-stu-id="34b46-125">By default, Arabic and Hebrew kashidas are ignored.</span></span> <span data-ttu-id="34b46-126">Impostare questo flag se si vuole che l'operazione di ricerca consideri i kashida.</span><span class="sxs-lookup"><span data-stu-id="34b46-126">Set this flag if you want the search operation to consider kashidas.</span></span><br/>                                                                                    |
| <span id="FR_WHOLEWORD"></span><span id="fr_wholeword"></span><dl> <span data-ttu-id="34b46-127"><dt>**FR \_ WHOLEWORD**</dt></span><span class="sxs-lookup"><span data-stu-id="34b46-127"><dt>**FR\_WHOLEWORD**</dt></span></span> </dl>                | <span data-ttu-id="34b46-128">Se impostata, l'operazione cerca solo parole intere che corrispondono alla stringa di ricerca.</span><span class="sxs-lookup"><span data-stu-id="34b46-128">If set, the operation searches only for whole words that match the search string.</span></span> <span data-ttu-id="34b46-129">Se non impostata, l'operazione cerca anche i frammenti di parole che corrispondono alla stringa di ricerca.</span><span class="sxs-lookup"><span data-stu-id="34b46-129">If not set, the operation also searches for word fragments that match the search string.</span></span><br/>                                  |



 

</dd> <dt>

<span data-ttu-id="34b46-130">*lParam*</span><span class="sxs-lookup"><span data-stu-id="34b46-130">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="34b46-131">Struttura [**FINDTEXTW**](/windows/win32/api/richedit/ns-richedit-findtexta) contenente informazioni sull'operazione di ricerca.</span><span class="sxs-lookup"><span data-stu-id="34b46-131">A [**FINDTEXTW**](/windows/win32/api/richedit/ns-richedit-findtexta) structure containing information about the find operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34b46-132">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="34b46-132">Return value</span></span>

<span data-ttu-id="34b46-133">Se viene trovata la stringa di destinazione, il valore restituito è la posizione in base zero del primo carattere della corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="34b46-133">If the target string is found, the return value is the zero-based position of the first character of the match.</span></span> <span data-ttu-id="34b46-134">Se la destinazione non viene trovata, il valore restituito è -1.</span><span class="sxs-lookup"><span data-stu-id="34b46-134">If the target is not found, the return value is -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="34b46-135">Commenti</span><span class="sxs-lookup"><span data-stu-id="34b46-135">Remarks</span></span>

<span data-ttu-id="34b46-136">**EM \_ FINDTEXTW** usa la [**struttura FINDTEXTW,**](/windows/win32/api/richedit/ns-richedit-findtexta) mentre [**EM \_ FINDTEXTEXW**](em-findtextexw.md) usa la [**struttura FINDTEXTEXW.**](/windows/desktop/api/Richedit/ns-richedit-findtextexa)</span><span class="sxs-lookup"><span data-stu-id="34b46-136">**EM\_FINDTEXTW** uses the [**FINDTEXTW**](/windows/win32/api/richedit/ns-richedit-findtexta) structure, while [**EM\_FINDTEXTEXW**](em-findtextexw.md) uses the [**FINDTEXTEXW**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) structure.</span></span> <span data-ttu-id="34b46-137">La differenza è che **FINDTEXTEXW riporta** l'intervallo di testo trovato.</span><span class="sxs-lookup"><span data-stu-id="34b46-137">The difference is that **FINDTEXTEXW** reports back the range of text that was found.</span></span>

## <a name="requirements"></a><span data-ttu-id="34b46-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="34b46-138">Requirements</span></span>



| <span data-ttu-id="34b46-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="34b46-139">Requirement</span></span> | <span data-ttu-id="34b46-140">Valore</span><span class="sxs-lookup"><span data-stu-id="34b46-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="34b46-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="34b46-141">Minimum supported client</span></span><br/> | <span data-ttu-id="34b46-142">Solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="34b46-142">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="34b46-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="34b46-143">Minimum supported server</span></span><br/> | <span data-ttu-id="34b46-144">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="34b46-144">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="34b46-145">Intestazione</span><span class="sxs-lookup"><span data-stu-id="34b46-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="34b46-146"><dt>Richedit.h</dt></span><span class="sxs-lookup"><span data-stu-id="34b46-146"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34b46-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="34b46-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34b46-148">**EM \_ FINDTEXTEXW**</span><span class="sxs-lookup"><span data-stu-id="34b46-148">**EM\_FINDTEXTEXW**</span></span>](em-findtextexw.md)
</dt> </dl>

 

 





