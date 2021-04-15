---
title: Messaggio di EM_FINDWORDBREAK (RichEdit. h)
description: Trova la parola successiva break prima o dopo la posizione del carattere specificata o recupera le informazioni sul carattere in quella posizione.
ms.assetid: b5df1365-4672-4c82-8ae4-ebf8b60bf871
keywords:
- Controlli di Windows Message EM_FINDWORDBREAK
topic_type:
- apiref
api_name:
- EM_FINDWORDBREAK
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6533358c0f4f521bc7021e290dfe11d66d4499e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477122"
---
# <a name="em_findwordbreak-message"></a><span data-ttu-id="b1138-104">\_Messaggio FINDWORDBREAK em</span><span class="sxs-lookup"><span data-stu-id="b1138-104">EM\_FINDWORDBREAK message</span></span>

<span data-ttu-id="b1138-105">Trova la parola successiva break prima o dopo la posizione del carattere specificata o recupera le informazioni sul carattere in quella posizione.</span><span class="sxs-lookup"><span data-stu-id="b1138-105">Finds the next word break before or after the specified character position or retrieves information about the character at that position.</span></span>

## <a name="parameters"></a><span data-ttu-id="b1138-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b1138-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1138-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b1138-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b1138-108">Specifica l'operazione di ricerca.</span><span class="sxs-lookup"><span data-stu-id="b1138-108">Specifies the find operation.</span></span> <span data-ttu-id="b1138-109">Questo parametro può avere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="b1138-109">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="b1138-110">Valore</span><span class="sxs-lookup"><span data-stu-id="b1138-110">Value</span></span>                                                                                                                                                                  | <span data-ttu-id="b1138-111">Significato</span><span class="sxs-lookup"><span data-stu-id="b1138-111">Meaning</span></span>                                                                                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WB_CLASSIFY"></span><span id="wb_classify"></span><dl> <span data-ttu-id="b1138-112"><dt>**\_classificazione WB**</dt></span><span class="sxs-lookup"><span data-stu-id="b1138-112"><dt>**WB\_CLASSIFY**</dt></span></span> </dl>                | <span data-ttu-id="b1138-113">Restituisce la classe di caratteri e i flag di interruzioni di parola del carattere in corrispondenza della posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="b1138-113">Returns the character class and word-break flags of the character at the specified position.</span></span><br/>                                                                                                                          |
| <span id="WB_ISDELIMITER"></span><span id="wb_isdelimiter"></span><dl> <span data-ttu-id="b1138-114"><dt>**delimitatore \_ WB**</dt></span><span class="sxs-lookup"><span data-stu-id="b1138-114"><dt>**WB\_ISDELIMITER**</dt></span></span> </dl>       | <span data-ttu-id="b1138-115">Restituisce **true** se il carattere in corrispondenza della posizione specificata è un delimitatore o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="b1138-115">Returns **TRUE** if the character at the specified position is a delimiter, or **FALSE** otherwise.</span></span><br/>                                                                                                                   |
| <span id="WB_LEFT"></span><span id="wb_left"></span><dl> <span data-ttu-id="b1138-116"><dt>**WB a \_ sinistra**</dt></span><span class="sxs-lookup"><span data-stu-id="b1138-116"><dt>**WB\_LEFT**</dt></span></span> </dl>                            | <span data-ttu-id="b1138-117">Trova il carattere più vicino prima della posizione specificata che inizia con una parola.</span><span class="sxs-lookup"><span data-stu-id="b1138-117">Finds the nearest character before the specified position that begins a word.</span></span><br/>                                                                                                                                         |
| <span id="WB_LEFTBREAK"></span><span id="wb_leftbreak"></span><dl> <span data-ttu-id="b1138-118"><dt>**\_LEFTBREAK WB**</dt></span><span class="sxs-lookup"><span data-stu-id="b1138-118"><dt>**WB\_LEFTBREAK**</dt></span></span> </dl>             | <span data-ttu-id="b1138-119">Trova la parola finale successiva prima della posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="b1138-119">Finds the next word end before the specified position.</span></span> <span data-ttu-id="b1138-120">Questo valore è uguale a WB \_ PREVBREAK.</span><span class="sxs-lookup"><span data-stu-id="b1138-120">This value is the same as WB\_PREVBREAK.</span></span><br/>                                                                                                                       |
| <span id="WB_MOVEWORDLEFT"></span><span id="wb_movewordleft"></span><dl> <span data-ttu-id="b1138-121"><dt>**\_MOVEWORDLEFT WB**</dt></span><span class="sxs-lookup"><span data-stu-id="b1138-121"><dt>**WB\_MOVEWORDLEFT**</dt></span></span> </dl>    | <span data-ttu-id="b1138-122">Trova il carattere successivo che inizia una parola prima della posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="b1138-122">Finds the next character that begins a word before the specified position.</span></span> <span data-ttu-id="b1138-123">Questo valore viene usato durante l'elaborazione del tasto CTRL + freccia sinistra.</span><span class="sxs-lookup"><span data-stu-id="b1138-123">This value is used during CTRL+LEFT ARROW key processing.</span></span> <span data-ttu-id="b1138-124">Questo valore è simile a WB \_ MOVEWORDPREV.</span><span class="sxs-lookup"><span data-stu-id="b1138-124">This value is the similar to WB\_MOVEWORDPREV.</span></span> <span data-ttu-id="b1138-125">Per ulteriori informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="b1138-125">See Remarks for more information.</span></span><br/> |
| <span id="WB_MOVEWORDRIGHT"></span><span id="wb_movewordright"></span><dl> <span data-ttu-id="b1138-126"><dt>**\_MOVEWORDRIGHT WB**</dt></span><span class="sxs-lookup"><span data-stu-id="b1138-126"><dt>**WB\_MOVEWORDRIGHT**</dt></span></span> </dl> | <span data-ttu-id="b1138-127">Trova il carattere successivo che inizia una parola dopo la posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="b1138-127">Finds the next character that begins a word after the specified position.</span></span> <span data-ttu-id="b1138-128">Questo valore viene usato durante l'elaborazione della chiave CTRL + right.</span><span class="sxs-lookup"><span data-stu-id="b1138-128">This value is used during CTRL+right key processing.</span></span> <span data-ttu-id="b1138-129">Questo valore è simile a WB \_ MOVEWORDNEXT.</span><span class="sxs-lookup"><span data-stu-id="b1138-129">This value is similar to WB\_MOVEWORDNEXT.</span></span> <span data-ttu-id="b1138-130">Per ulteriori informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="b1138-130">See Remarks for more information.</span></span><br/>           |
| <span id="WB_RIGHT"></span><span id="wb_right"></span><dl> <span data-ttu-id="b1138-131"><dt>**WB a \_ destra**</dt></span><span class="sxs-lookup"><span data-stu-id="b1138-131"><dt>**WB\_RIGHT**</dt></span></span> </dl>                         | <span data-ttu-id="b1138-132">Trova il carattere successivo che inizia una parola dopo la posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="b1138-132">Finds the next character that begins a word after the specified position.</span></span><br/>                                                                                                                                             |
| <span id="WB_RIGHTBREAK"></span><span id="wb_rightbreak"></span><dl> <span data-ttu-id="b1138-133"><dt>**\_RIGHTBREAK WB**</dt></span><span class="sxs-lookup"><span data-stu-id="b1138-133"><dt>**WB\_RIGHTBREAK**</dt></span></span> </dl>          | <span data-ttu-id="b1138-134">Trova il successivo delimitatore di fine parola dopo la posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="b1138-134">Finds the next end-of-word delimiter after the specified position.</span></span> <span data-ttu-id="b1138-135">Questo valore è uguale a WB \_ NEXTBREAK.</span><span class="sxs-lookup"><span data-stu-id="b1138-135">This value is the same as WB\_NEXTBREAK.</span></span><br/>                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="b1138-136">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b1138-136">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b1138-137">Posizione iniziale del carattere in base zero.</span><span class="sxs-lookup"><span data-stu-id="b1138-137">Zero-based character starting position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1138-138">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b1138-138">Return value</span></span>

<span data-ttu-id="b1138-139">Il messaggio restituisce un valore basato sul parametro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="b1138-139">The message returns a value based on the *wParam* parameter.</span></span>



| <span data-ttu-id="b1138-140">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="b1138-140">Return code</span></span>                                                                                    | <span data-ttu-id="b1138-141">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b1138-141">Description</span></span>                                                                                                            |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b1138-142"><dt>**wParam**</dt></span><span class="sxs-lookup"><span data-stu-id="b1138-142"><dt>**wParam**</dt></span></span> </dl>          | <span data-ttu-id="b1138-143">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b1138-143">Return Value</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="b1138-144"><dt>**\_classificazione WB**</dt></span><span class="sxs-lookup"><span data-stu-id="b1138-144"><dt>**WB\_CLASSIFY**</dt></span></span> </dl>    | <span data-ttu-id="b1138-145">Restituisce la classe di caratteri e i flag di interruzioni di parola del carattere in corrispondenza della posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="b1138-145">Returns the character class and word-break flags of the character at the specified position.</span></span><br/>                |
| <dl> <span data-ttu-id="b1138-146"><dt>**delimitatore \_ WB**</dt></span><span class="sxs-lookup"><span data-stu-id="b1138-146"><dt>**WB\_ISDELIMITER**</dt></span></span> </dl> | <span data-ttu-id="b1138-147">Restituisce **true** se il carattere in corrispondenza della posizione specificata è un delimitatore; in caso contrario, restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="b1138-147">Returns **TRUE** if the character at the specified position is a delimiter; otherwise it returns **FALSE**.</span></span><br/> |
| <dl> <span data-ttu-id="b1138-148"><dt>**Altro**</dt></span><span class="sxs-lookup"><span data-stu-id="b1138-148"><dt>**Others**</dt></span></span> </dl>          | <span data-ttu-id="b1138-149">Restituisce l'indice dei caratteri della parola break.</span><span class="sxs-lookup"><span data-stu-id="b1138-149">Returns the character index of the word break.</span></span><br/>                                                              |



 

## <a name="remarks"></a><span data-ttu-id="b1138-150">Commenti</span><span class="sxs-lookup"><span data-stu-id="b1138-150">Remarks</span></span>

<span data-ttu-id="b1138-151">Se *wParam* è WB \_ Left e WB \_ right, la procedura di Word break trova le interruzioni di parola solo dopo i delimitatori.</span><span class="sxs-lookup"><span data-stu-id="b1138-151">If *wParam* is WB\_LEFT and WB\_RIGHT, the word-break procedure finds word breaks only after delimiters.</span></span> <span data-ttu-id="b1138-152">Corrisponde alla funzionalità di un controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="b1138-152">This matches the functionality of an edit control.</span></span> <span data-ttu-id="b1138-153">Se *wParam* è WB \_ MOVEWORDLEFT o WB \_ MOVEWORDRIGHT, la stored procedure di Word-break confronta anche le classi di caratteri e i flag di Word break.</span><span class="sxs-lookup"><span data-stu-id="b1138-153">If *wParam* is WB\_MOVEWORDLEFT or WB\_MOVEWORDRIGHT, the word-break procedure also compares character classes and word-break flags.</span></span>

<span data-ttu-id="b1138-154">Per informazioni sulle classi di caratteri e i flag di interruzione di parola, vedere [parole e interruzioni di riga](using-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="b1138-154">For information about character classes and word-break flags, see [Word and Line Breaks](using-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b1138-155">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b1138-155">Requirements</span></span>



| <span data-ttu-id="b1138-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1138-156">Requirement</span></span> | <span data-ttu-id="b1138-157">Valore</span><span class="sxs-lookup"><span data-stu-id="b1138-157">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b1138-158">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b1138-158">Minimum supported client</span></span><br/> | <span data-ttu-id="b1138-159">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b1138-159">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b1138-160">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b1138-160">Minimum supported server</span></span><br/> | <span data-ttu-id="b1138-161">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b1138-161">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b1138-162">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b1138-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1138-163"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1138-163"><dt>Richedit.h</dt></span></span> </dl> |



 

 





