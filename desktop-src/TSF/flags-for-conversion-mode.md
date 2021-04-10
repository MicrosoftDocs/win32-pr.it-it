---
title: Flag per la modalità di conversione (Ctffunc. h)
description: I flag seguenti vengono usati come valore della \_ conversione INPUTMODE della tastiera del raggruppamento GUID \_ \_ \_ . Equivale ai \_ valori cmode IME per imm32.
ms.assetid: 6e545af5-5fdb-49de-b24e-aaee82b51326
keywords:
- Flag per la modalità di conversione Framework servizi di testo
topic_type:
- apiref
api_name:
- Flags for Conversion Mode
api_location:
- Ctffunc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 022712ff45f213992bf3d40bd0149959e4864faa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120066"
---
# <a name="flags-for-conversion-mode"></a><span data-ttu-id="7dc75-105">Flag per la modalità di conversione</span><span class="sxs-lookup"><span data-stu-id="7dc75-105">Flags for Conversion Mode</span></span>

<span data-ttu-id="7dc75-106">I flag seguenti vengono usati come valore della [ \_ \_ \_ \_ conversione INPUTMODE della tastiera del raggruppamento GUID](predefined-compartments.md).</span><span class="sxs-lookup"><span data-stu-id="7dc75-106">The following flags are used as a value of [GUID\_COMPARTMENT\_KEYBOARD\_INPUTMODE\_CONVERSION](predefined-compartments.md).</span></span> <span data-ttu-id="7dc75-107">Equivale ai valori [ \_ cmode IME](../intl/ime-conversion-mode-values.md) per imm32.</span><span class="sxs-lookup"><span data-stu-id="7dc75-107">This is equivalent with [IME\_CMODE](../intl/ime-conversion-mode-values.md) values for IMM32.</span></span>



| <span data-ttu-id="7dc75-108">Flag</span><span class="sxs-lookup"><span data-stu-id="7dc75-108">Flag</span></span>                             | <span data-ttu-id="7dc75-109">valore</span><span class="sxs-lookup"><span data-stu-id="7dc75-109">Value</span></span>  | <span data-ttu-id="7dc75-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7dc75-110">Description</span></span>                                                     |
|----------------------------------|--------|-----------------------------------------------------------------|
| <span data-ttu-id="7dc75-111">\_CONVERSIONMODE \_ ALFANUMERICo TF</span><span class="sxs-lookup"><span data-stu-id="7dc75-111">TF\_CONVERSIONMODE\_ALPHANUMERIC</span></span> | <span data-ttu-id="7dc75-112">0x0000</span><span class="sxs-lookup"><span data-stu-id="7dc75-112">0x0000</span></span> | <span data-ttu-id="7dc75-113">Impostare su 1 se la modalità ALFANUMERICa.</span><span class="sxs-lookup"><span data-stu-id="7dc75-113">Set to 1 if ALPHANUMERIC mode.</span></span>                                  |
| <span data-ttu-id="7dc75-114">TF \_ CONVERSIONMODE \_ nativo</span><span class="sxs-lookup"><span data-stu-id="7dc75-114">TF\_CONVERSIONMODE\_NATIVE</span></span>       | <span data-ttu-id="7dc75-115">0x0001</span><span class="sxs-lookup"><span data-stu-id="7dc75-115">0x0001</span></span> | <span data-ttu-id="7dc75-116">Impostare su 1 se la modalità nativa; 0 se la modalità ALFANUMERICa.</span><span class="sxs-lookup"><span data-stu-id="7dc75-116">Set to 1 if NATIVE mode; 0 if ALPHANUMERIC mode.</span></span>                |
| <span data-ttu-id="7dc75-117">\_CONVERSIONMODE \_ katakana</span><span class="sxs-lookup"><span data-stu-id="7dc75-117">TF\_CONVERSIONMODE\_KATAKANA</span></span>     | <span data-ttu-id="7dc75-118">0x0002</span><span class="sxs-lookup"><span data-stu-id="7dc75-118">0x0002</span></span> | <span data-ttu-id="7dc75-119">Impostare su 1 se la modalità KATAKANA; 0 se la modalità HIRAGANA.</span><span class="sxs-lookup"><span data-stu-id="7dc75-119">Set to 1 if KATAKANA mode; 0 if HIRAGANA mode.</span></span>                  |
| <span data-ttu-id="7dc75-120">TF \_ CONVERSIONMODE \_ FULLSHAPE</span><span class="sxs-lookup"><span data-stu-id="7dc75-120">TF\_CONVERSIONMODE\_FULLSHAPE</span></span>    | <span data-ttu-id="7dc75-121">0x0008</span><span class="sxs-lookup"><span data-stu-id="7dc75-121">0x0008</span></span> | <span data-ttu-id="7dc75-122">Impostare su 1 se la modalità di forma completa; 0 se la modalità a metà forma.</span><span class="sxs-lookup"><span data-stu-id="7dc75-122">Set to 1 if full shape mode; 0 if half shape mode.</span></span>              |
| <span data-ttu-id="7dc75-123">TF \_ CONVERSIONMODE \_ Roman</span><span class="sxs-lookup"><span data-stu-id="7dc75-123">TF\_CONVERSIONMODE\_ROMAN</span></span>        | <span data-ttu-id="7dc75-124">0x0010</span><span class="sxs-lookup"><span data-stu-id="7dc75-124">0x0010</span></span> | <span data-ttu-id="7dc75-125">Impostare su 1 per impedire l'elaborazione di conversioni da IME; 0 in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="7dc75-125">Set to 1 to prevent processing of conversions by IME; 0 if not.</span></span> |
| <span data-ttu-id="7dc75-126">TF \_ CONVERSIONMODE \_ CHARCODE</span><span class="sxs-lookup"><span data-stu-id="7dc75-126">TF\_CONVERSIONMODE\_CHARCODE</span></span>     | <span data-ttu-id="7dc75-127">0x0020</span><span class="sxs-lookup"><span data-stu-id="7dc75-127">0x0020</span></span> | <span data-ttu-id="7dc75-128">Impostare su 1 se la modalità di input del codice carattere; 0 in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="7dc75-128">Set to 1 if character code input mode; 0 if not.</span></span>                |
| <span data-ttu-id="7dc75-129">TF \_ CONVERSIONMODE \_ SOFTKEYBOARD</span><span class="sxs-lookup"><span data-stu-id="7dc75-129">TF\_CONVERSIONMODE\_SOFTKEYBOARD</span></span> | <span data-ttu-id="7dc75-130">0x0080</span><span class="sxs-lookup"><span data-stu-id="7dc75-130">0x0080</span></span> | <span data-ttu-id="7dc75-131">Impostare su 1 se la modalità tastiera soft; 0 in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="7dc75-131">Set to 1 if Soft Keyboard mode; 0 if not.</span></span>                       |
| <span data-ttu-id="7dc75-132">TF \_ CONVERSIONMODE \_ noconversione</span><span class="sxs-lookup"><span data-stu-id="7dc75-132">TF\_CONVERSIONMODE\_NOCONVERSION</span></span> | <span data-ttu-id="7dc75-133">0x0100</span><span class="sxs-lookup"><span data-stu-id="7dc75-133">0x0100</span></span> | <span data-ttu-id="7dc75-134">Impostare su 1 per impedire l'elaborazione di conversioni da IME; 0 in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="7dc75-134">Set to 1 to prevent processing of conversions by IME; 0 if not.</span></span> |
| <span data-ttu-id="7dc75-135">\_simbolo TF CONVERSIONMODE \_</span><span class="sxs-lookup"><span data-stu-id="7dc75-135">TF\_CONVERSIONMODE\_SYMBOL</span></span>       | <span data-ttu-id="7dc75-136">0x0400</span><span class="sxs-lookup"><span data-stu-id="7dc75-136">0x0400</span></span> | <span data-ttu-id="7dc75-137">Impostare su 1 se la modalità di conversione del simbolo. 0 in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="7dc75-137">Set to 1 if SYMBOL conversion mode; 0 if not.</span></span>                   |
| <span data-ttu-id="7dc75-138">\_CONVERSIONMODE TF \_ fisso</span><span class="sxs-lookup"><span data-stu-id="7dc75-138">TF\_CONVERSIONMODE\_FIXED</span></span>        | <span data-ttu-id="7dc75-139">0x0800</span><span class="sxs-lookup"><span data-stu-id="7dc75-139">0x0800</span></span> | <span data-ttu-id="7dc75-140">Impostare su 1 se la modalità di conversione è fissa; 0 in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="7dc75-140">Set to 1 if fixed conversion mode; 0 if not.</span></span>                    |



 

<span data-ttu-id="7dc75-141">I valori seguenti vengono usati come valore della [ \_ \_ \_ \_ frase INPUTMODE della tastiera del raggruppamento GUID](predefined-compartments.md).</span><span class="sxs-lookup"><span data-stu-id="7dc75-141">The following values are used as a value of [GUID\_COMPARTMENT\_KEYBOARD\_INPUTMODE\_SENTENCE](predefined-compartments.md).</span></span> <span data-ttu-id="7dc75-142">Equivale ai valori [ \_ SMODE IME](../intl/ime-composition-string-values.md) per imm32.</span><span class="sxs-lookup"><span data-stu-id="7dc75-142">This is equivalent with [IME\_SMODE](../intl/ime-composition-string-values.md) values for IMM32.</span></span>



| <span data-ttu-id="7dc75-143">Flag</span><span class="sxs-lookup"><span data-stu-id="7dc75-143">Flag</span></span>                            | <span data-ttu-id="7dc75-144">valore</span><span class="sxs-lookup"><span data-stu-id="7dc75-144">Value</span></span>  | <span data-ttu-id="7dc75-145">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7dc75-145">Description</span></span>                                                                |
|---------------------------------|--------|----------------------------------------------------------------------------|
| <span data-ttu-id="7dc75-146">TF \_ SENTENCEMODE \_ None</span><span class="sxs-lookup"><span data-stu-id="7dc75-146">TF\_SENTENCEMODE\_NONE</span></span>          | <span data-ttu-id="7dc75-147">0x0000</span><span class="sxs-lookup"><span data-stu-id="7dc75-147">0x0000</span></span> | <span data-ttu-id="7dc75-148">Nessuna informazione per la frase.</span><span class="sxs-lookup"><span data-stu-id="7dc75-148">No information for sentence.</span></span>                                               |
| <span data-ttu-id="7dc75-149">TF \_ SENTENCEMODE \_ PLAURALCLAUSE</span><span class="sxs-lookup"><span data-stu-id="7dc75-149">TF\_SENTENCEMODE\_PLAURALCLAUSE</span></span> | <span data-ttu-id="7dc75-150">0x0001</span><span class="sxs-lookup"><span data-stu-id="7dc75-150">0x0001</span></span> | <span data-ttu-id="7dc75-151">L'IME utilizza le informazioni sulla clausola plurale per eseguire l'elaborazione della conversione.</span><span class="sxs-lookup"><span data-stu-id="7dc75-151">The IME uses plural clause information to carry out conversion processing.</span></span> |
| <span data-ttu-id="7dc75-152">TF \_ SENTENCEMODE \_ SINGLECONVERT</span><span class="sxs-lookup"><span data-stu-id="7dc75-152">TF\_SENTENCEMODE\_SINGLECONVERT</span></span> | <span data-ttu-id="7dc75-153">0x0002</span><span class="sxs-lookup"><span data-stu-id="7dc75-153">0x0002</span></span> | <span data-ttu-id="7dc75-154">L'IME esegue l'elaborazione della conversione in modalità a carattere singolo.</span><span class="sxs-lookup"><span data-stu-id="7dc75-154">The IME carries out conversion processing in single-character mode.</span></span>        |
| <span data-ttu-id="7dc75-155">TF \_ SENTENCEMODE \_ automatico</span><span class="sxs-lookup"><span data-stu-id="7dc75-155">TF\_SENTENCEMODE\_AUTOMATIC</span></span>     | <span data-ttu-id="7dc75-156">0x0004</span><span class="sxs-lookup"><span data-stu-id="7dc75-156">0x0004</span></span> | <span data-ttu-id="7dc75-157">L'IME esegue l'elaborazione della conversione in modalità automatica.</span><span class="sxs-lookup"><span data-stu-id="7dc75-157">The IME carries out conversion processing in automatic mode.</span></span>               |
| <span data-ttu-id="7dc75-158">TF \_ SENTENCEMODE \_ PHRASEPREDICT</span><span class="sxs-lookup"><span data-stu-id="7dc75-158">TF\_SENTENCEMODE\_PHRASEPREDICT</span></span> | <span data-ttu-id="7dc75-159">0x0008</span><span class="sxs-lookup"><span data-stu-id="7dc75-159">0x0008</span></span> | <span data-ttu-id="7dc75-160">L'IME utilizza le informazioni sulla frase per stimare il carattere successivo.</span><span class="sxs-lookup"><span data-stu-id="7dc75-160">The IME uses phrase information to predict the next character.</span></span>             |
| <span data-ttu-id="7dc75-161">\_conversazione TF SENTENCEMODE \_</span><span class="sxs-lookup"><span data-stu-id="7dc75-161">TF\_SENTENCEMODE\_CONVERSATION</span></span>  | <span data-ttu-id="7dc75-162">0x0010</span><span class="sxs-lookup"><span data-stu-id="7dc75-162">0x0010</span></span> | <span data-ttu-id="7dc75-163">L'IME utilizza la modalità conversazione.</span><span class="sxs-lookup"><span data-stu-id="7dc75-163">The IME uses conversation mode.</span></span> <span data-ttu-id="7dc75-164">Questa operazione è utile per le applicazioni di chat.</span><span class="sxs-lookup"><span data-stu-id="7dc75-164">This is useful for chat applications.</span></span>      |



 

## <a name="requirements"></a><span data-ttu-id="7dc75-165">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7dc75-165">Requirements</span></span>



| <span data-ttu-id="7dc75-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="7dc75-166">Requirement</span></span> | <span data-ttu-id="7dc75-167">Valore</span><span class="sxs-lookup"><span data-stu-id="7dc75-167">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7dc75-168">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7dc75-168">Minimum supported client</span></span><br/> | <span data-ttu-id="7dc75-169">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7dc75-169">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="7dc75-170">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7dc75-170">Minimum supported server</span></span><br/> | <span data-ttu-id="7dc75-171">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7dc75-171">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="7dc75-172">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="7dc75-172">Redistributable</span></span><br/>          | <span data-ttu-id="7dc75-173">TSF 1,0 onWindows NT 4.0, Windows 2000 ProfessionalandWindows MeWindows 98</span><span class="sxs-lookup"><span data-stu-id="7dc75-173">TSF 1.0 onWindows NT 4.0,Windows 2000 ProfessionalandWindows MeWindows 98</span></span><br/>   |
| <span data-ttu-id="7dc75-174">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7dc75-174">Header</span></span><br/>                   | <dl> <span data-ttu-id="7dc75-175"><dt>Ctffunc. h</dt></span><span class="sxs-lookup"><span data-stu-id="7dc75-175"><dt>Ctffunc.h</dt></span></span> </dl>   |
| <span data-ttu-id="7dc75-176">IDL</span><span class="sxs-lookup"><span data-stu-id="7dc75-176">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7dc75-177"><dt>Ctffunc. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7dc75-177"><dt>Ctffunc.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7dc75-178">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7dc75-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7dc75-179">Raggruppamenti predefiniti</span><span class="sxs-lookup"><span data-stu-id="7dc75-179">Predefined Compartments</span></span>](predefined-compartments.md)
</dt> </dl>

 

