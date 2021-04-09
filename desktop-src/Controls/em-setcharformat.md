---
title: Messaggio di EM_SETCHARFORMAT (RichEdit. h)
description: Imposta la formattazione carattere in un controllo Rich Edit.
ms.assetid: 5e7a545d-4ca4-4dc6-badb-584c11194982
keywords:
- Controlli di Windows Message EM_SETCHARFORMAT
topic_type:
- apiref
api_name:
- EM_SETCHARFORMAT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba8f37960659f29dd33d5b8f27f0b5a2e3d35eb0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121042"
---
# <a name="em_setcharformat-message"></a><span data-ttu-id="2ad43-104">\_Messaggio SETCHARFORMAT em</span><span class="sxs-lookup"><span data-stu-id="2ad43-104">EM\_SETCHARFORMAT message</span></span>

<span data-ttu-id="2ad43-105">Imposta la formattazione carattere in un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="2ad43-105">Sets character formatting in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="2ad43-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2ad43-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ad43-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2ad43-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2ad43-108">Formattazione dei caratteri applicata al controllo.</span><span class="sxs-lookup"><span data-stu-id="2ad43-108">Character formatting that applies to the control.</span></span> <span data-ttu-id="2ad43-109">Se questo parametro è zero, viene impostato il formato carattere predefinito.</span><span class="sxs-lookup"><span data-stu-id="2ad43-109">If this parameter is zero, the default character format is set.</span></span> <span data-ttu-id="2ad43-110">In caso contrario, può essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="2ad43-110">Otherwise, it can be one of the following values.</span></span>



| <span data-ttu-id="2ad43-111">Valore</span><span class="sxs-lookup"><span data-stu-id="2ad43-111">Value</span></span>                                                                                                                                                                           | <span data-ttu-id="2ad43-112">Significato</span><span class="sxs-lookup"><span data-stu-id="2ad43-112">Meaning</span></span>                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SCF_ALL"></span><span id="scf_all"></span><dl> <span data-ttu-id="2ad43-113"><dt>**\_tutti gli SCF**</dt></span><span class="sxs-lookup"><span data-stu-id="2ad43-113"><dt>**SCF\_ALL**</dt></span></span> </dl>                                     | <span data-ttu-id="2ad43-114">Applica la formattazione a tutto il testo nel controllo.</span><span class="sxs-lookup"><span data-stu-id="2ad43-114">Applies the formatting to all text in the control.</span></span> <span data-ttu-id="2ad43-115">Non valido con **l' \_ opzione SCF Selection** o **SCF \_ Word**.</span><span class="sxs-lookup"><span data-stu-id="2ad43-115">Not valid with **SCF\_SELECTION** or **SCF\_WORD**.</span></span><br/>                                                                                                                                                                                         |
| <span id="SCF_ASSOCIATEFONT"></span><span id="scf_associatefont"></span><dl> <span data-ttu-id="2ad43-116"><dt>**\_ASSOCIATEFONT SCF**</dt></span><span class="sxs-lookup"><span data-stu-id="2ad43-116"><dt>**SCF\_ASSOCIATEFONT**</dt></span></span> </dl>       | <span data-ttu-id="2ad43-117">**Richedit 4,1:** Associa un tipo di carattere a uno script specificato, modificando in questo modo il tipo di carattere predefinito per lo script.</span><span class="sxs-lookup"><span data-stu-id="2ad43-117">**RichEdit 4.1:** Associates a font to a given script, thus changing the default font for that script.</span></span> <span data-ttu-id="2ad43-118">Per specificare il tipo di carattere, usare i membri seguenti di [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a): **yHeight**, **bCharSet**, **bPitchAndFamily**, **szFaceName** e **LCID**.</span><span class="sxs-lookup"><span data-stu-id="2ad43-118">To specify the font, use the following members of [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a): **yHeight**, **bCharSet**, **bPitchAndFamily**, **szFaceName**, and **lcid**.</span></span><br/>                     |
| <span id="SCF_ASSOCIATEFONT2"></span><span id="scf_associatefont2"></span><dl> <span data-ttu-id="2ad43-119"><dt>**\_ASSOCIATEFONT2 SCF**</dt></span><span class="sxs-lookup"><span data-stu-id="2ad43-119"><dt>**SCF\_ASSOCIATEFONT2**</dt></span></span> </dl>    | <span data-ttu-id="2ad43-120">**Richedit 4,1:** Associa un tipo di carattere surrogato (piano 2) a uno script specificato, modificando in tal modo il tipo di carattere predefinito per lo script.</span><span class="sxs-lookup"><span data-stu-id="2ad43-120">**RichEdit 4.1:** Associates a surrogate (plane-2) font to a given script, thus changing the default font for that script.</span></span> <span data-ttu-id="2ad43-121">Per specificare il tipo di carattere, usare i membri seguenti di [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a): **yHeight**, **bCharSet**, **bPitchAndFamily**, **szFaceName** e **LCID**.</span><span class="sxs-lookup"><span data-stu-id="2ad43-121">To specify the font, use the following members of [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a): **yHeight**, **bCharSet**, **bPitchAndFamily**, **szFaceName**, and **lcid**.</span></span><br/> |
| <span id="SCF_CHARREPFROMLCID"></span><span id="scf_charrepfromlcid"></span><dl> <span data-ttu-id="2ad43-122"><dt>**\_CHARREPFROMLCID SCF**</dt></span><span class="sxs-lookup"><span data-stu-id="2ad43-122"><dt>**SCF\_CHARREPFROMLCID**</dt></span></span> </dl> | <span data-ttu-id="2ad43-123">Ottiene il repertorio di caratteri dall'LCID.</span><span class="sxs-lookup"><span data-stu-id="2ad43-123">Gets the character repertoire from the LCID.</span></span><br/>                                                                                                                                                                                                                                                   |
| <span id="SCF_DEFAULT"></span><span id="scf_default"></span><dl> <span data-ttu-id="2ad43-124"><dt>**\_impostazione predefinita SCF**</dt></span><span class="sxs-lookup"><span data-stu-id="2ad43-124"><dt>**SCF\_DEFAULT**</dt></span></span> </dl>                         | <span data-ttu-id="2ad43-125">**Richedit 4,1:** Imposta il tipo di carattere predefinito per il controllo.</span><span class="sxs-lookup"><span data-stu-id="2ad43-125">**RichEdit 4.1:** Sets the default font for the control.</span></span> <br/>                                                                                                                                                                                                                                      |
| <span id="SPF_DONTSETDEFAULT"></span><span id="spf_dontsetdefault"></span><dl> <span data-ttu-id="2ad43-126"><dt>**\_DONTSETDEFAULT SPF**</dt></span><span class="sxs-lookup"><span data-stu-id="2ad43-126"><dt>**SPF\_DONTSETDEFAULT**</dt></span></span> </dl>    | <span data-ttu-id="2ad43-127">Impedisce l'impostazione del formato di paragrafo predefinito quando il controllo Rich Edit è vuoto.</span><span class="sxs-lookup"><span data-stu-id="2ad43-127">Prevents setting the default paragraph format when the rich edit control is empty.</span></span><br/>                                                                                                                                                                                                             |
| <span id="SCF_NOKBUPDATE"></span><span id="scf_nokbupdate"></span><dl> <span data-ttu-id="2ad43-128"><dt>**\_NOKBUPDATE SCF**</dt></span><span class="sxs-lookup"><span data-stu-id="2ad43-128"><dt>**SCF\_NOKBUPDATE**</dt></span></span> </dl>                | <span data-ttu-id="2ad43-129">**Richedit 4,1:** Impedisce il cambio di tastiera per la corrispondenza con il tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="2ad43-129">**RichEdit 4.1:** Prevents keyboard switching to match the font.</span></span> <span data-ttu-id="2ad43-130">Se, ad esempio, viene impostato un tipo di carattere arabo, in genere la funzione di tastiera automatica per i linguaggi BiDi modifica la tastiera in una tastiera araba.</span><span class="sxs-lookup"><span data-stu-id="2ad43-130">For example, if an Arabic font is set, normally the automatic keyboard feature for Bidi languages changes the keyboard to an Arabic keyboard.</span></span><br/>                                                                                 |
| <span id="SCF_SELECTION"></span><span id="scf_selection"></span><dl> <span data-ttu-id="2ad43-131"><dt>**\_selezione SCF**</dt></span><span class="sxs-lookup"><span data-stu-id="2ad43-131"><dt>**SCF\_SELECTION**</dt></span></span> </dl>                   | <span data-ttu-id="2ad43-132">Applica la formattazione alla selezione corrente.</span><span class="sxs-lookup"><span data-stu-id="2ad43-132">Applies the formatting to the current selection.</span></span> <span data-ttu-id="2ad43-133">Se la selezione è vuota, la formattazione dei caratteri viene applicata al punto di inserimento e il nuovo formato carattere è attivo solo fino a quando il punto di inserimento non viene modificato.</span><span class="sxs-lookup"><span data-stu-id="2ad43-133">If the selection is empty, the character formatting is applied to the insertion point, and the new character format is in effect only until the insertion point changes.</span></span><br/>                                                                      |
| <span id="SPF_SETDEFAULT"></span><span id="spf_setdefault"></span><dl> <span data-ttu-id="2ad43-134"><dt>**\_impostazione predefinita SPF**</dt></span><span class="sxs-lookup"><span data-stu-id="2ad43-134"><dt>**SPF\_SETDEFAULT**</dt></span></span> </dl>                | <span data-ttu-id="2ad43-135">Imposta gli attributi di formattazione dei paragrafi predefiniti.</span><span class="sxs-lookup"><span data-stu-id="2ad43-135">Sets the default paragraph formatting attributes.</span></span><br/>                                                                                                                                                                                                                                              |
| <span id="SCF_SMARTFONT"></span><span id="scf_smartfont"></span><dl> <span data-ttu-id="2ad43-136"><dt>**\_SMARTFONT SCF**</dt></span><span class="sxs-lookup"><span data-stu-id="2ad43-136"><dt>**SCF\_SMARTFONT**</dt></span></span> </dl>                   | <span data-ttu-id="2ad43-137">Applicare il tipo di carattere solo se è in grado di gestire lo script.</span><span class="sxs-lookup"><span data-stu-id="2ad43-137">Apply the font only if it can handle script.</span></span><br/>                                                                                                                                                                                                                                                   |
| <span id="SCF_USEUIRULES"></span><span id="scf_useuirules"></span><dl> <span data-ttu-id="2ad43-138"><dt>**\_USEUIRULES SCF**</dt></span><span class="sxs-lookup"><span data-stu-id="2ad43-138"><dt>**SCF\_USEUIRULES**</dt></span></span> </dl>                | <span data-ttu-id="2ad43-139">**Richedit 4,1:** Utilizzato con **la \_ selezione SCF**.</span><span class="sxs-lookup"><span data-stu-id="2ad43-139">**RichEdit 4.1:** Used with **SCF\_SELECTION**.</span></span> <span data-ttu-id="2ad43-140">Indica che il formato proviene da una barra degli strumenti o da un altro strumento dell'interfaccia utente, quindi è necessario utilizzare le regole di formattazione dell'interfaccia utente anziché la formattazione letterale</span><span class="sxs-lookup"><span data-stu-id="2ad43-140">Indicates that format came from a toolbar or other UI tool, so UI formatting rules should be used instead of literal formatting.</span></span><br/>                                                                                                               |
| <span id="SCF_WORD"></span><span id="scf_word"></span><dl> <span data-ttu-id="2ad43-141"><dt>**\_parola SCF**</dt></span><span class="sxs-lookup"><span data-stu-id="2ad43-141"><dt>**SCF\_WORD**</dt></span></span> </dl>                                  | <span data-ttu-id="2ad43-142">Applica la formattazione alla parola o alle parole selezionate.</span><span class="sxs-lookup"><span data-stu-id="2ad43-142">Applies the formatting to the selected word or words.</span></span> <span data-ttu-id="2ad43-143">Se la selezione è vuota ma il punto di inserimento si trova all'interno di una parola, la formattazione viene applicata alla parola.</span><span class="sxs-lookup"><span data-stu-id="2ad43-143">If the selection is empty but the insertion point is inside a word, the formatting is applied to the word.</span></span> <span data-ttu-id="2ad43-144">Il valore della **\_ parola SCF** deve essere utilizzato insieme al valore **di \_ selezione SCF** .</span><span class="sxs-lookup"><span data-stu-id="2ad43-144">The **SCF\_WORD** value must be used in conjunction with the **SCF\_SELECTION** value.</span></span><br/>                                        |



 

</dd> <dt>

<span data-ttu-id="2ad43-145">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2ad43-145">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2ad43-146">Puntatore a una struttura [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) che specifica la formattazione dei caratteri da usare.</span><span class="sxs-lookup"><span data-stu-id="2ad43-146">Pointer to a [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) structure specifying the character formatting to use.</span></span> <span data-ttu-id="2ad43-147">Vengono modificati solo gli attributi di formattazione specificati dal membro **dwMask** .</span><span class="sxs-lookup"><span data-stu-id="2ad43-147">Only the formatting attributes specified by the **dwMask** member are changed.</span></span>

<span data-ttu-id="2ad43-148">Microsoft Rich Edit 2,0 e versioni successive: questo parametro può essere un puntatore a una struttura [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a) , che è un'estensione della struttura [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) .</span><span class="sxs-lookup"><span data-stu-id="2ad43-148">Microsoft Rich Edit 2.0 and later: This parameter can be a pointer to a [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a) structure, which is an extension of the [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) structure.</span></span> <span data-ttu-id="2ad43-149">Prima di inviare il messaggio **\_ SETCHARFORMAT em** , impostare il membro **cbSize** della struttura su `sizeof(CHARFORMAT)` o `sizeof(CHARFORMAT2)` indicare quale versione della struttura viene utilizzata.</span><span class="sxs-lookup"><span data-stu-id="2ad43-149">Before sending the **EM\_SETCHARFORMAT** message, set the structure's **cbSize** member to `sizeof(CHARFORMAT)` or `sizeof(CHARFORMAT2)` indicate which version of the structure is being used.</span></span>

<span data-ttu-id="2ad43-150">I membri **szFaceName** e **bCharSet** possono essere sovraregolati quando non sono validi per i caratteri, ad esempio: Arial in caratteri kanji.</span><span class="sxs-lookup"><span data-stu-id="2ad43-150">The **szFaceName** and **bCharSet** members may be overruled when invalid for characters, for example: Arial on kanji characters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ad43-151">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2ad43-151">Return value</span></span>

<span data-ttu-id="2ad43-152">Se l'operazione ha esito positivo, il valore restituito è un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="2ad43-152">If the operation succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="2ad43-153">Se l'operazione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="2ad43-153">If the operation fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ad43-154">Commenti</span><span class="sxs-lookup"><span data-stu-id="2ad43-154">Remarks</span></span>

<span data-ttu-id="2ad43-155">Se questo messaggio viene inviato più di una volta con gli stessi parametri, l'effetto sul testo viene attivato o disattivato.</span><span class="sxs-lookup"><span data-stu-id="2ad43-155">If this message is sent more than once with the same parameters, the effect on the text is toggled.</span></span> <span data-ttu-id="2ad43-156">Ovvero inviando il messaggio una volta generato l'effetto, l'invio del messaggio due volte Annulla l'effetto e così via.</span><span class="sxs-lookup"><span data-stu-id="2ad43-156">That is, sending the message once produces the effect, sending the message twice cancels the effect, and so forth.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ad43-157">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2ad43-157">Requirements</span></span>



| <span data-ttu-id="2ad43-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ad43-158">Requirement</span></span> | <span data-ttu-id="2ad43-159">Valore</span><span class="sxs-lookup"><span data-stu-id="2ad43-159">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2ad43-160">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2ad43-160">Minimum supported client</span></span><br/> | <span data-ttu-id="2ad43-161">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2ad43-161">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2ad43-162">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2ad43-162">Minimum supported server</span></span><br/> | <span data-ttu-id="2ad43-163">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2ad43-163">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2ad43-164">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2ad43-164">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ad43-165"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ad43-165"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ad43-166">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2ad43-166">See also</span></span>

<dl> <dt>

<span data-ttu-id="2ad43-167">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="2ad43-167">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2ad43-168">**CHARFORMAT**</span><span class="sxs-lookup"><span data-stu-id="2ad43-168">**CHARFORMAT**</span></span>](/windows/win32/api/richedit/ns-richedit-charformata)
</dt> <dt>

[<span data-ttu-id="2ad43-169">**CHARFORMAT2**</span><span class="sxs-lookup"><span data-stu-id="2ad43-169">**CHARFORMAT2**</span></span>](/windows/desktop/api/Richedit/ns-richedit-charformat2a)
</dt> </dl>

 

 





