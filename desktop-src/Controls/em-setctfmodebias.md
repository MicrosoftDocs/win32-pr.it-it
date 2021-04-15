---
title: Messaggio di EM_SETCTFMODEBIAS (RichEdit. h)
description: Imposta la distorsione della modalità TSF (Text Services Framework) per un controllo Rich Edit.
ms.assetid: 17e3aac8-2ba8-4c06-bfd6-e118cfb82529
keywords:
- Controlli di Windows Message EM_SETCTFMODEBIAS
topic_type:
- apiref
api_name:
- EM_SETCTFMODEBIAS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b872fa5489c898ec4482ecdc094de7df6e3180be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518675"
---
# <a name="em_setctfmodebias-message"></a><span data-ttu-id="315b8-104">\_Messaggio SETCTFMODEBIAS em</span><span class="sxs-lookup"><span data-stu-id="315b8-104">EM\_SETCTFMODEBIAS message</span></span>

<span data-ttu-id="315b8-105">Imposta la distorsione della modalità TSF (Text Services Framework) per un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="315b8-105">Sets the Text Services Framework (TSF) mode bias for a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="315b8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="315b8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="315b8-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="315b8-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="315b8-108">Valore di distorsione della modalità.</span><span class="sxs-lookup"><span data-stu-id="315b8-108">Mode bias value.</span></span> <span data-ttu-id="315b8-109">Può corrispondere a uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="315b8-109">This can be one of the following values.</span></span>



| <span data-ttu-id="315b8-110">Valore</span><span class="sxs-lookup"><span data-stu-id="315b8-110">Value</span></span>                                                                                                                                                                                                                     | <span data-ttu-id="315b8-111">Significato</span><span class="sxs-lookup"><span data-stu-id="315b8-111">Meaning</span></span>                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="CTFMODEBIAS_DEFAULT"></span><span id="ctfmodebias_default"></span><dl> <span data-ttu-id="315b8-112"><dt>**\_impostazione predefinita CTFMODEBIAS**</dt></span><span class="sxs-lookup"><span data-stu-id="315b8-112"><dt>**CTFMODEBIAS\_DEFAULT**</dt></span></span> </dl>                                           | <span data-ttu-id="315b8-113">Non esiste alcuna distorsione in modalità.</span><span class="sxs-lookup"><span data-stu-id="315b8-113">There is no mode bias.</span></span><br/>                             |
| <span id="CTFMODEBIAS_FILENAME"></span><span id="ctfmodebias_filename"></span><dl> <span data-ttu-id="315b8-114"><dt>**\_nome file CTFMODEBIAS**</dt></span><span class="sxs-lookup"><span data-stu-id="315b8-114"><dt>**CTFMODEBIAS\_FILENAME**</dt></span></span> </dl>                                        | <span data-ttu-id="315b8-115">La distorsione è a un nome di file.</span><span class="sxs-lookup"><span data-stu-id="315b8-115">The bias is to a filename.</span></span><br/>                         |
| <span id="CTFMODEBIAS_NAME"></span><span id="ctfmodebias_name"></span><dl> <span data-ttu-id="315b8-116"><dt>**\_nome CTFMODEBIAS**</dt></span><span class="sxs-lookup"><span data-stu-id="315b8-116"><dt>**CTFMODEBIAS\_NAME**</dt></span></span> </dl>                                                    | <span data-ttu-id="315b8-117">La distorsione è un nome.</span><span class="sxs-lookup"><span data-stu-id="315b8-117">The bias is to a name.</span></span><br/>                             |
| <span id="CTFMODEBIAS_READING"></span><span id="ctfmodebias_reading"></span><dl> <span data-ttu-id="315b8-118"><dt>**lettura di CTFMODEBIAS \_**</dt></span><span class="sxs-lookup"><span data-stu-id="315b8-118"><dt>**CTFMODEBIAS\_READING**</dt></span></span> </dl>                                           | <span data-ttu-id="315b8-119">La distorsione è la lettura.</span><span class="sxs-lookup"><span data-stu-id="315b8-119">The bias is to the reading.</span></span><br/>                        |
| <span id="CTFMODEBIAS_DATETIME"></span><span id="ctfmodebias_datetime"></span><dl> <span data-ttu-id="315b8-120"><dt>**CTFMODEBIAS \_ DateTime**</dt></span><span class="sxs-lookup"><span data-stu-id="315b8-120"><dt>**CTFMODEBIAS\_DATETIME**</dt></span></span> </dl>                                        | <span data-ttu-id="315b8-121">La distorsione è a una data o un'ora.</span><span class="sxs-lookup"><span data-stu-id="315b8-121">The bias is to a date or time.</span></span><br/>                     |
| <span id="CTFMODEBIAS_CONVERSATION"></span><span id="ctfmodebias_conversation"></span><dl> <span data-ttu-id="315b8-122"><dt>**\_conversazione CTFMODEBIAS**</dt></span><span class="sxs-lookup"><span data-stu-id="315b8-122"><dt>**CTFMODEBIAS\_CONVERSATION**</dt></span></span> </dl>                            | <span data-ttu-id="315b8-123">La distorsione è a una conversazione.</span><span class="sxs-lookup"><span data-stu-id="315b8-123">The bias is to a conversation.</span></span><br/>                     |
| <span id="CTFMODEBIAS_NUMERIC"></span><span id="ctfmodebias_numeric"></span><dl> <span data-ttu-id="315b8-124"><dt>**CTFMODEBIAS \_ numerico**</dt></span><span class="sxs-lookup"><span data-stu-id="315b8-124"><dt>**CTFMODEBIAS\_NUMERIC**</dt></span></span> </dl>                                           | <span data-ttu-id="315b8-125">La distorsione è un numero.</span><span class="sxs-lookup"><span data-stu-id="315b8-125">The bias is to a number.</span></span><br/>                           |
| <span id="CTFMODEBIAS_HIRAGANA"></span><span id="ctfmodebias_hiragana"></span><dl> <span data-ttu-id="315b8-126"><dt>**\_Hiragana CTFMODEBIAS**</dt></span><span class="sxs-lookup"><span data-stu-id="315b8-126"><dt>**CTFMODEBIAS\_HIRAGANA**</dt></span></span> </dl>                                        | <span data-ttu-id="315b8-127">La distorsione è per le stringhe hiragana.</span><span class="sxs-lookup"><span data-stu-id="315b8-127">The bias is to hiragana strings.</span></span><br/>                   |
| <span id="CTFMODEBIAS_KATAKANA"></span><span id="ctfmodebias_katakana"></span><dl> <span data-ttu-id="315b8-128"><dt>**\_katakana CTFMODEBIAS**</dt></span><span class="sxs-lookup"><span data-stu-id="315b8-128"><dt>**CTFMODEBIAS\_KATAKANA**</dt></span></span> </dl>                                        | <span data-ttu-id="315b8-129">La distorsione è per le stringhe katakana.</span><span class="sxs-lookup"><span data-stu-id="315b8-129">The bias is to katakana strings.</span></span><br/>                   |
| <span id="CTFMODEBIAS_HANGUL"></span><span id="ctfmodebias_hangul"></span><dl> <span data-ttu-id="315b8-130"><dt>**CTFMODEBIAS \_ hangul**</dt></span><span class="sxs-lookup"><span data-stu-id="315b8-130"><dt>**CTFMODEBIAS\_HANGUL**</dt></span></span> </dl>                                              | <span data-ttu-id="315b8-131">La distorsione è di caratteri Hangul.</span><span class="sxs-lookup"><span data-stu-id="315b8-131">The bias is to Hangul characters.</span></span><br/>                  |
| <span id="CTFMODEBIAS_HALFWIDTHKATAKANA"></span><span id="ctfmodebias_halfwidthkatakana"></span><dl> <span data-ttu-id="315b8-132"><dt>**\_HALFWIDTHKATAKANA CTFMODEBIAS**</dt></span><span class="sxs-lookup"><span data-stu-id="315b8-132"><dt>**CTFMODEBIAS\_HALFWIDTHKATAKANA**</dt></span></span> </dl>             | <span data-ttu-id="315b8-133">La distorsione è per le stringhe katakana a metà larghezza.</span><span class="sxs-lookup"><span data-stu-id="315b8-133">The bias is to half-width katakana strings.</span></span><br/>        |
| <span id="CTFMODEBIAS_FULLWIDTHALPHANUMERIC"></span><span id="ctfmodebias_fullwidthalphanumeric"></span><dl> <span data-ttu-id="315b8-134"><dt>**\_FULLWIDTHALPHANUMERIC CTFMODEBIAS**</dt></span><span class="sxs-lookup"><span data-stu-id="315b8-134"><dt>**CTFMODEBIAS\_FULLWIDTHALPHANUMERIC**</dt></span></span> </dl> | <span data-ttu-id="315b8-135">La distorsione è a caratteri alfanumerici a larghezza intera.</span><span class="sxs-lookup"><span data-stu-id="315b8-135">The bias is to full-width alphanumeric characters.</span></span><br/> |
| <span id="CTFMODEBIAS_HALFWIDTHALPHANUMERIC"></span><span id="ctfmodebias_halfwidthalphanumeric"></span><dl> <span data-ttu-id="315b8-136"><dt>**\_HALFWIDTHALPHANUMERIC CTFMODEBIAS**</dt></span><span class="sxs-lookup"><span data-stu-id="315b8-136"><dt>**CTFMODEBIAS\_HALFWIDTHALPHANUMERIC**</dt></span></span> </dl> | <span data-ttu-id="315b8-137">La distorsione è costituita da caratteri alfanumerici a metà larghezza.</span><span class="sxs-lookup"><span data-stu-id="315b8-137">The bias is to half-width alphanumeric characters.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="315b8-138">*lParam*</span><span class="sxs-lookup"><span data-stu-id="315b8-138">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="315b8-139">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="315b8-139">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="315b8-140">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="315b8-140">Return value</span></span>

<span data-ttu-id="315b8-141">Se ha esito positivo, il valore restituito è il nuovo valore di distorsione della modalità TSF.</span><span class="sxs-lookup"><span data-stu-id="315b8-141">If successful, the return value is the new TSF mode bias value.</span></span> <span data-ttu-id="315b8-142">Se ha esito negativo, il valore restituito è il valore di distorsione della modalità TSF precedente.</span><span class="sxs-lookup"><span data-stu-id="315b8-142">If unsuccessful, the return value is the old TSF mode bias value.</span></span>

## <a name="remarks"></a><span data-ttu-id="315b8-143">Commenti</span><span class="sxs-lookup"><span data-stu-id="315b8-143">Remarks</span></span>

<span data-ttu-id="315b8-144">Quando un'applicazione Microsoft Rich Edit USA TSF, può selezionare la distorsione della modalità TSF.</span><span class="sxs-lookup"><span data-stu-id="315b8-144">When a Microsoft Rich Edit application uses TSF, it can select the TSF mode bias.</span></span> <span data-ttu-id="315b8-145">Questo messaggio imposta i criteri in base ai quali una scelta alternativa viene visualizzata nella parte superiore dell'elenco per la selezione.</span><span class="sxs-lookup"><span data-stu-id="315b8-145">This message sets the criteria by which an alternative choice appears at the top of the list for selection.</span></span>

<span data-ttu-id="315b8-146">Per impostare la distorsione della modalità per input Method Editor (IME), usare [**em \_ SETIMEMODEBIAS**](em-setimemodebias.md).</span><span class="sxs-lookup"><span data-stu-id="315b8-146">To set the mode bias for the Input Method Editor (IME), use [**EM\_SETIMEMODEBIAS**](em-setimemodebias.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="315b8-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="315b8-147">Requirements</span></span>



| <span data-ttu-id="315b8-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="315b8-148">Requirement</span></span> | <span data-ttu-id="315b8-149">Valore</span><span class="sxs-lookup"><span data-stu-id="315b8-149">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="315b8-150">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="315b8-150">Minimum supported client</span></span><br/> | <span data-ttu-id="315b8-151">Solo app desktop Windows XP con SP1 \[\]</span><span class="sxs-lookup"><span data-stu-id="315b8-151">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="315b8-152">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="315b8-152">Minimum supported server</span></span><br/> | <span data-ttu-id="315b8-153">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="315b8-153">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="315b8-154">Intestazione</span><span class="sxs-lookup"><span data-stu-id="315b8-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="315b8-155"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="315b8-155"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="315b8-156">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="315b8-156">See also</span></span>

<dl> <dt>

<span data-ttu-id="315b8-157">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="315b8-157">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="315b8-158">**\_GETCTFMODEBIAS em**</span><span class="sxs-lookup"><span data-stu-id="315b8-158">**EM\_GETCTFMODEBIAS**</span></span>](em-getctfmodebias.md)
</dt> <dt>

[<span data-ttu-id="315b8-159">**\_SETIMEMODEBIAS em**</span><span class="sxs-lookup"><span data-stu-id="315b8-159">**EM\_SETIMEMODEBIAS**</span></span>](em-setimemodebias.md)
</dt> </dl>

 

 





