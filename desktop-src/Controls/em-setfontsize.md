---
title: Messaggio di EM_SETFONTSIZE (RichEdit. h)
description: Imposta la dimensione del carattere per il testo selezionato in un controllo Rich Edit.
ms.assetid: 18d91370-12c0-4e5f-a0e9-ffde02abc966
keywords:
- Controlli di Windows Message EM_SETFONTSIZE
topic_type:
- apiref
api_name:
- EM_SETFONTSIZE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8eb75276acbb86cbd452a8ad97698f1cd7382bd2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476829"
---
# <a name="em_setfontsize-message"></a><span data-ttu-id="7c602-104">\_Messaggio DIFONTSIZE em</span><span class="sxs-lookup"><span data-stu-id="7c602-104">EM\_SETFONTSIZE message</span></span>

<span data-ttu-id="7c602-105">Imposta la dimensione del carattere per il testo selezionato in un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="7c602-105">Sets the font size for the selected text in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="7c602-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7c602-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c602-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7c602-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7c602-108">Modifica le dimensioni in punti del testo selezionato.</span><span class="sxs-lookup"><span data-stu-id="7c602-108">Change in point size of the selected text.</span></span> <span data-ttu-id="7c602-109">Il risultato verrà arrotondato in base ai valori indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="7c602-109">The result will be rounded according to values shown in the following table.</span></span> <span data-ttu-id="7c602-110">Questo parametro deve essere compreso nell'intervallo da-1637 a 1638.</span><span class="sxs-lookup"><span data-stu-id="7c602-110">This parameter should be in the range of -1637 to 1638.</span></span> <span data-ttu-id="7c602-111">Le dimensioni del carattere risultante saranno comprese nell'intervallo da 1 a 1638.</span><span class="sxs-lookup"><span data-stu-id="7c602-111">The resulting font size will be within the range of 1 to 1638.</span></span>

</dd> <dt>

<span data-ttu-id="7c602-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7c602-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7c602-113">Questo parametro non viene utilizzato. deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="7c602-113">This parameter is not used; it must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c602-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7c602-114">Return value</span></span>

<span data-ttu-id="7c602-115">Se non si è verificato alcun errore, il valore restituito è **true**.</span><span class="sxs-lookup"><span data-stu-id="7c602-115">If no error occurred, the return value is **TRUE**.</span></span>

<span data-ttu-id="7c602-116">Se si è verificato un errore, il valore restituito è **false**.</span><span class="sxs-lookup"><span data-stu-id="7c602-116">If an error occurred, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c602-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="7c602-117">Remarks</span></span>

<span data-ttu-id="7c602-118">È possibile ottenere facilmente le dimensioni del carattere inviando il messaggio [**\_ GETCHARFORMAT em**](em-getcharformat.md) .</span><span class="sxs-lookup"><span data-stu-id="7c602-118">You can easily get the font size by sending the [**EM\_GETCHARFORMAT**](em-getcharformat.md) message.</span></span>

<span data-ttu-id="7c602-119">Rich Edit aggiunge innanzitutto *wParam* alla dimensione corrente del carattere e quindi usa le dimensioni risultanti e la tabella seguente per determinare il valore di arrotondamento.</span><span class="sxs-lookup"><span data-stu-id="7c602-119">Rich Edit first adds *wParam* to the current font size and then uses the resulting size and the following table to determine the rounding value.</span></span>



| <span data-ttu-id="7c602-120">Fuori banda</span><span class="sxs-lookup"><span data-stu-id="7c602-120">Band</span></span>    | <span data-ttu-id="7c602-121">Valore di arrotondamento</span><span class="sxs-lookup"><span data-stu-id="7c602-121">Rounding value</span></span> |
|---------|----------------|
| <span data-ttu-id="7c602-122"><= 12</span><span class="sxs-lookup"><span data-stu-id="7c602-122"><=12</span></span> | <span data-ttu-id="7c602-123">1</span><span class="sxs-lookup"><span data-stu-id="7c602-123">1</span></span>              |
| <span data-ttu-id="7c602-124">28</span><span class="sxs-lookup"><span data-stu-id="7c602-124">28</span></span>      | <span data-ttu-id="7c602-125">2</span><span class="sxs-lookup"><span data-stu-id="7c602-125">2</span></span>              |
| <span data-ttu-id="7c602-126">36</span><span class="sxs-lookup"><span data-stu-id="7c602-126">36</span></span>      | <span data-ttu-id="7c602-127">0</span><span class="sxs-lookup"><span data-stu-id="7c602-127">0</span></span>              |
| <span data-ttu-id="7c602-128">48</span><span class="sxs-lookup"><span data-stu-id="7c602-128">48</span></span>      | <span data-ttu-id="7c602-129">0</span><span class="sxs-lookup"><span data-stu-id="7c602-129">0</span></span>              |
| <span data-ttu-id="7c602-130">72</span><span class="sxs-lookup"><span data-stu-id="7c602-130">72</span></span>      | <span data-ttu-id="7c602-131">0</span><span class="sxs-lookup"><span data-stu-id="7c602-131">0</span></span>              |
| <span data-ttu-id="7c602-132">80</span><span class="sxs-lookup"><span data-stu-id="7c602-132">80</span></span>      | <span data-ttu-id="7c602-133">0</span><span class="sxs-lookup"><span data-stu-id="7c602-133">0</span></span>              |
| <span data-ttu-id="7c602-134">> 80</span><span class="sxs-lookup"><span data-stu-id="7c602-134">> 80</span></span> | <span data-ttu-id="7c602-135">10</span><span class="sxs-lookup"><span data-stu-id="7c602-135">10</span></span>             |



 

<span data-ttu-id="7c602-136">Se la dimensione del carattere risultante non è divisibile in modo uniforme per il valore di arrotondamento, le dimensioni del carattere vengono arrotondate a un numero equamente divisibile per il valore di arrotondamento.</span><span class="sxs-lookup"><span data-stu-id="7c602-136">If the resulting font size is not evenly divisible by the rounding value, the font size is then rounded to a number evenly divisible by the rounding value.</span></span> <span data-ttu-id="7c602-137">Quindi, se la dimensione del carattere è minore o uguale a 12, il valore di arrotondamento sarà 1.</span><span class="sxs-lookup"><span data-stu-id="7c602-137">So if the font size is less than or equal to 12, the rounding value will be 1.</span></span> <span data-ttu-id="7c602-138">Analogamente, se la dimensione del carattere è minore o uguale a 28, il valore di arrotondamento è 2.</span><span class="sxs-lookup"><span data-stu-id="7c602-138">Similarly, if the font size is less than or equal to 28, the rounding value is 2.</span></span> <span data-ttu-id="7c602-139">Per i valori maggiori di 28, le dimensioni del carattere vengono arrotondate alla banda successiva.</span><span class="sxs-lookup"><span data-stu-id="7c602-139">For values greater than 28, font sizes are rounded to the next band.</span></span> <span data-ttu-id="7c602-140">Quindi, la dimensione del carattere passa a 36, 48, 72, 80.</span><span class="sxs-lookup"><span data-stu-id="7c602-140">So, the font size jumps to 36, 48, 72, 80.</span></span> <span data-ttu-id="7c602-141">Dopo 80, l'arrotondamento viene eseguito in incrementi di dieci punti.</span><span class="sxs-lookup"><span data-stu-id="7c602-141">After 80, all rounding is done in increments of ten points.</span></span>

<span data-ttu-id="7c602-142">Le dimensioni del carattere vengono arrotondate per eccesso o per difetto a seconda del segno di *wParam*.</span><span class="sxs-lookup"><span data-stu-id="7c602-142">The font size is rounded up or down depending on the sign of *wParam*.</span></span> <span data-ttu-id="7c602-143">Se *wParam* è positivo, l'arrotondamento è sempre attivo.</span><span class="sxs-lookup"><span data-stu-id="7c602-143">If *wParam* is positive, the rounding is always up.</span></span> <span data-ttu-id="7c602-144">In caso contrario, l'arrotondamento è sempre inattivo.</span><span class="sxs-lookup"><span data-stu-id="7c602-144">Otherwise, rounding is always down.</span></span> <span data-ttu-id="7c602-145">Quindi, se la dimensione corrente del carattere è 10 e *wParam* è 3, le dimensioni del carattere risultante saranno 14 (10 + 3 = 13, che non è divisibile per 2, quindi la dimensione viene arrotondata a 14).</span><span class="sxs-lookup"><span data-stu-id="7c602-145">So, if the current font size is 10 and *wParam* is 3, the resulting font size would be 14 (10 + 3 = 13, which is not divisible by 2, so the size rounds up to 14).</span></span> <span data-ttu-id="7c602-146">Viceversa, se le dimensioni del carattere correnti sono 14 e *wParam* è-3, la dimensione del carattere risultante sarà 10 (14-3 = 11, che non è divisibile per 2, quindi la dimensione viene arrotondata a 10).</span><span class="sxs-lookup"><span data-stu-id="7c602-146">Conversely, if the current font size is 14 and *wParam* is -3, the resulting font size would be 10 (14 - 3 = 11, which is not divisible by 2, so the size rounds down to 10).</span></span>

<span data-ttu-id="7c602-147">La modifica viene applicata a ogni parte della selezione.</span><span class="sxs-lookup"><span data-stu-id="7c602-147">The change is applied to each part of the selection.</span></span> <span data-ttu-id="7c602-148">Quindi, se il testo è 10pt e alcuni 20pt, dopo una chiamata con *wParam* impostato su 1, le dimensioni del carattere diventano rispettivamente 11pt e 22pt.</span><span class="sxs-lookup"><span data-stu-id="7c602-148">So, if some of the text is 10pt and some 20pt, after a call with *wParam* set to 1, the font sizes become 11pt and 22pt, respectively.</span></span>

<span data-ttu-id="7c602-149">Nella tabella seguente sono illustrati altri esempi.</span><span class="sxs-lookup"><span data-stu-id="7c602-149">Additional examples are shown in the following table.</span></span>



| <span data-ttu-id="7c602-150">Dimensioni del carattere originale</span><span class="sxs-lookup"><span data-stu-id="7c602-150">Original font size</span></span> | <span data-ttu-id="7c602-151">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7c602-151">*wParam*</span></span> | <span data-ttu-id="7c602-152">Dimensioni del carattere risultanti</span><span class="sxs-lookup"><span data-stu-id="7c602-152">Resulting font size</span></span> |
|--------------------|----------|---------------------|
| <span data-ttu-id="7c602-153">7</span><span class="sxs-lookup"><span data-stu-id="7c602-153">7</span></span>                  | <span data-ttu-id="7c602-154">1</span><span class="sxs-lookup"><span data-stu-id="7c602-154">1</span></span>        | <span data-ttu-id="7c602-155">8</span><span class="sxs-lookup"><span data-stu-id="7c602-155">8</span></span>                   |
| <span data-ttu-id="7c602-156">7</span><span class="sxs-lookup"><span data-stu-id="7c602-156">7</span></span>                  | <span data-ttu-id="7c602-157">3</span><span class="sxs-lookup"><span data-stu-id="7c602-157">3</span></span>        | <span data-ttu-id="7c602-158">10</span><span class="sxs-lookup"><span data-stu-id="7c602-158">10</span></span>                  |
| <span data-ttu-id="7c602-159">10</span><span class="sxs-lookup"><span data-stu-id="7c602-159">10</span></span>                 | <span data-ttu-id="7c602-160">3</span><span class="sxs-lookup"><span data-stu-id="7c602-160">3</span></span>        | <span data-ttu-id="7c602-161">14</span><span class="sxs-lookup"><span data-stu-id="7c602-161">14</span></span>                  |
| <span data-ttu-id="7c602-162">14</span><span class="sxs-lookup"><span data-stu-id="7c602-162">14</span></span>                 | <span data-ttu-id="7c602-163">-3</span><span class="sxs-lookup"><span data-stu-id="7c602-163">-3</span></span>       | <span data-ttu-id="7c602-164">10</span><span class="sxs-lookup"><span data-stu-id="7c602-164">10</span></span>                  |
| <span data-ttu-id="7c602-165">28</span><span class="sxs-lookup"><span data-stu-id="7c602-165">28</span></span>                 | <span data-ttu-id="7c602-166">1</span><span class="sxs-lookup"><span data-stu-id="7c602-166">1</span></span>        | <span data-ttu-id="7c602-167">36</span><span class="sxs-lookup"><span data-stu-id="7c602-167">36</span></span>                  |
| <span data-ttu-id="7c602-168">28</span><span class="sxs-lookup"><span data-stu-id="7c602-168">28</span></span>                 | <span data-ttu-id="7c602-169">3</span><span class="sxs-lookup"><span data-stu-id="7c602-169">3</span></span>        | <span data-ttu-id="7c602-170">36</span><span class="sxs-lookup"><span data-stu-id="7c602-170">36</span></span>                  |
| <span data-ttu-id="7c602-171">80</span><span class="sxs-lookup"><span data-stu-id="7c602-171">80</span></span>                 | <span data-ttu-id="7c602-172">1</span><span class="sxs-lookup"><span data-stu-id="7c602-172">1</span></span>        | <span data-ttu-id="7c602-173">90</span><span class="sxs-lookup"><span data-stu-id="7c602-173">90</span></span>                  |
| <span data-ttu-id="7c602-174">80</span><span class="sxs-lookup"><span data-stu-id="7c602-174">80</span></span>                 | <span data-ttu-id="7c602-175">-1</span><span class="sxs-lookup"><span data-stu-id="7c602-175">-1</span></span>       | <span data-ttu-id="7c602-176">72</span><span class="sxs-lookup"><span data-stu-id="7c602-176">72</span></span>                  |



 

## <a name="requirements"></a><span data-ttu-id="7c602-177">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7c602-177">Requirements</span></span>



| <span data-ttu-id="7c602-178">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c602-178">Requirement</span></span> | <span data-ttu-id="7c602-179">Valore</span><span class="sxs-lookup"><span data-stu-id="7c602-179">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7c602-180">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7c602-180">Minimum supported client</span></span><br/> | <span data-ttu-id="7c602-181">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7c602-181">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7c602-182">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7c602-182">Minimum supported server</span></span><br/> | <span data-ttu-id="7c602-183">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7c602-183">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7c602-184">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="7c602-184">Redistributable</span></span><br/>          | <span data-ttu-id="7c602-185">Modifica avanzata 3,0</span><span class="sxs-lookup"><span data-stu-id="7c602-185">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="7c602-186">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7c602-186">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c602-187"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c602-187"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c602-188">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7c602-188">See also</span></span>

<dl> <dt>

<span data-ttu-id="7c602-189">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="7c602-189">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7c602-190">**\_GETCHARFORMAT em**</span><span class="sxs-lookup"><span data-stu-id="7c602-190">**EM\_GETCHARFORMAT**</span></span>](em-getcharformat.md)
</dt> <dt>

[<span data-ttu-id="7c602-191">**CHARFORMAT2**</span><span class="sxs-lookup"><span data-stu-id="7c602-191">**CHARFORMAT2**</span></span>](/windows/desktop/api/Richedit/ns-richedit-charformat2a)
</dt> <dt>

<span data-ttu-id="7c602-192">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="7c602-192">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="7c602-193">Informazioni sui controlli Rich Edit</span><span class="sxs-lookup"><span data-stu-id="7c602-193">About Rich Edit Controls</span></span>](about-rich-edit-controls.md)
</dt> </dl>

 

 





