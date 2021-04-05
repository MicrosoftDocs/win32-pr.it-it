---
title: Messaggio di EM_SETIMEOPTIONS (RichEdit. h)
description: Imposta le opzioni IME (Input Method Editor).
ms.assetid: 8a72ee1c-f6b8-44eb-b8df-57cd834db326
keywords:
- Controlli di Windows Message EM_SETIMEOPTIONS
topic_type:
- apiref
api_name:
- EM_SETIMEOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59be3148bd00abd998af200368f2ed77ad3ff911
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874038"
---
# <a name="em_setimeoptions-message"></a><span data-ttu-id="25b39-104">\_Messaggio SETIMEOPTIONS em</span><span class="sxs-lookup"><span data-stu-id="25b39-104">EM\_SETIMEOPTIONS message</span></span>

<span data-ttu-id="25b39-105">Imposta le opzioni IME (Input Method Editor).</span><span class="sxs-lookup"><span data-stu-id="25b39-105">Sets the Input Method Editor (IME) options.</span></span>

> [!Note]  
> <span data-ttu-id="25b39-106">Questo messaggio è supportato solo nelle versioni in lingua asiatica di Microsoft Rich Edit 1,0.</span><span class="sxs-lookup"><span data-stu-id="25b39-106">This message is supported only in Asian-language versions of Microsoft Rich Edit 1.0.</span></span> <span data-ttu-id="25b39-107">Non è supportata nelle versioni successive.</span><span class="sxs-lookup"><span data-stu-id="25b39-107">It is not supported in any later versions.</span></span>

 

## <a name="parameters"></a><span data-ttu-id="25b39-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="25b39-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25b39-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="25b39-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="25b39-110">Specifica uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="25b39-110">Specifies one of the following values.</span></span>



| <span data-ttu-id="25b39-111">Valore</span><span class="sxs-lookup"><span data-stu-id="25b39-111">Value</span></span>                                                                                                                                             | <span data-ttu-id="25b39-112">Significato</span><span class="sxs-lookup"><span data-stu-id="25b39-112">Meaning</span></span>                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="ECOOP_SET"></span><span id="ecoop_set"></span><dl> <span data-ttu-id="25b39-113"><dt>**SET di ECOOP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="25b39-113"><dt>**ECOOP\_SET**</dt></span></span> </dl> | <span data-ttu-id="25b39-114">Imposta le opzioni su quelle specificate da *lParam*.</span><span class="sxs-lookup"><span data-stu-id="25b39-114">Sets the options to those specified by *lParam*.</span></span><br/>                             |
| <span id="ECOOP_OR"></span><span id="ecoop_or"></span><dl> <span data-ttu-id="25b39-115"><dt>**ECOOP \_ o**</dt></span><span class="sxs-lookup"><span data-stu-id="25b39-115"><dt>**ECOOP\_OR**</dt></span></span> </dl>    | <span data-ttu-id="25b39-116">Combina le opzioni specificate con le opzioni correnti.</span><span class="sxs-lookup"><span data-stu-id="25b39-116">Combines the specified options with the current options.</span></span><br/>                     |
| <span id="ECOOP_AND"></span><span id="ecoop_and"></span><dl> <span data-ttu-id="25b39-117"><dt>**ECOOP \_ e**</dt></span><span class="sxs-lookup"><span data-stu-id="25b39-117"><dt>**ECOOP\_AND**</dt></span></span> </dl> | <span data-ttu-id="25b39-118">Mantiene solo le opzioni correnti specificate anche da *lParam*.</span><span class="sxs-lookup"><span data-stu-id="25b39-118">Retains only those current options that are also specified by *lParam*.</span></span><br/>      |
| <span id="ECOOP_XOR"></span><span id="ecoop_xor"></span><dl> <span data-ttu-id="25b39-119"><dt>**\_Xor ECOOP**</dt></span><span class="sxs-lookup"><span data-stu-id="25b39-119"><dt>**ECOOP\_XOR**</dt></span></span> </dl> | <span data-ttu-id="25b39-120">Logicamente esclusivo o opzioni correnti con quelle specificate da *lParam.*</span><span class="sxs-lookup"><span data-stu-id="25b39-120">Logically exclusive OR the current options with those specified by *lParam.*</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="25b39-121">*lParam*</span><span class="sxs-lookup"><span data-stu-id="25b39-121">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="25b39-122">Specifica uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="25b39-122">Specifies one of more of the following values.</span></span>



| <span data-ttu-id="25b39-123">Valore</span><span class="sxs-lookup"><span data-stu-id="25b39-123">Value</span></span>                                                                                                                                                                                 | <span data-ttu-id="25b39-124">Significato</span><span class="sxs-lookup"><span data-stu-id="25b39-124">Meaning</span></span>                                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="IMF_CLOSESTATUSWINDOW"></span><span id="imf_closestatuswindow"></span><dl> <span data-ttu-id="25b39-125"><dt>**\_CLOSESTATUSWINDOW FMI**</dt></span><span class="sxs-lookup"><span data-stu-id="25b39-125"><dt>**IMF\_CLOSESTATUSWINDOW**</dt></span></span> </dl> | <span data-ttu-id="25b39-126">Chiude la finestra di stato IME quando il controllo riceve lo stato attivo per l'input.</span><span class="sxs-lookup"><span data-stu-id="25b39-126">Closes the IME status window when the control receives the input focus.</span></span><br/>                                                                                                               |
| <span id="IMF_FORCEACTIVE"></span><span id="imf_forceactive"></span><dl> <span data-ttu-id="25b39-127"><dt>**\_FORCEACTIVE FMI**</dt></span><span class="sxs-lookup"><span data-stu-id="25b39-127"><dt>**IMF\_FORCEACTIVE**</dt></span></span> </dl>                   | <span data-ttu-id="25b39-128">Attiva l'IME quando il controllo riceve lo stato attivo per l'input.</span><span class="sxs-lookup"><span data-stu-id="25b39-128">Activates the IME when the control receives the input focus.</span></span><br/>                                                                                                                          |
| <span id="IMF_FORCEDISABLE"></span><span id="imf_forcedisable"></span><dl> <span data-ttu-id="25b39-129"><dt>**\_FORCEDISABLE FMI**</dt></span><span class="sxs-lookup"><span data-stu-id="25b39-129"><dt>**IMF\_FORCEDISABLE**</dt></span></span> </dl>                | <span data-ttu-id="25b39-130">Disabilita l'IME quando il controllo riceve lo stato attivo per l'input.</span><span class="sxs-lookup"><span data-stu-id="25b39-130">Disables the IME when the control receives the input focus.</span></span><br/>                                                                                                                           |
| <span id="IMF_FORCEENABLE"></span><span id="imf_forceenable"></span><dl> <span data-ttu-id="25b39-131"><dt>**\_FORCEENABLE FMI**</dt></span><span class="sxs-lookup"><span data-stu-id="25b39-131"><dt>**IMF\_FORCEENABLE**</dt></span></span> </dl>                   | <span data-ttu-id="25b39-132">Abilita l'IME quando il controllo riceve lo stato attivo per l'input.</span><span class="sxs-lookup"><span data-stu-id="25b39-132">Enables the IME when the control receives the input focus.</span></span><br/>                                                                                                                            |
| <span id="IMF_FORCEINACTIVE"></span><span id="imf_forceinactive"></span><dl> <span data-ttu-id="25b39-133"><dt>**\_FORCEINACTIVE FMI**</dt></span><span class="sxs-lookup"><span data-stu-id="25b39-133"><dt>**IMF\_FORCEINACTIVE**</dt></span></span> </dl>             | <span data-ttu-id="25b39-134">Disattiva l'IME quando il controllo riceve lo stato attivo per l'input.</span><span class="sxs-lookup"><span data-stu-id="25b39-134">Inactivates the IME when the control receives the input focus.</span></span><br/>                                                                                                                        |
| <span id="IMF_FORCENONE"></span><span id="imf_forcenone"></span><dl> <span data-ttu-id="25b39-135"><dt>**\_FORCENONE FMI**</dt></span><span class="sxs-lookup"><span data-stu-id="25b39-135"><dt>**IMF\_FORCENONE**</dt></span></span> </dl>                         | <span data-ttu-id="25b39-136">Disabilita la gestione IME.</span><span class="sxs-lookup"><span data-stu-id="25b39-136">Disables IME handling.</span></span><br/>                                                                                                                                                                |
| <span id="IMF_FORCEREMEMBER"></span><span id="imf_forceremember"></span><dl> <span data-ttu-id="25b39-137"><dt>**\_FORCEREMEMBER FMI**</dt></span><span class="sxs-lookup"><span data-stu-id="25b39-137"><dt>**IMF\_FORCEREMEMBER**</dt></span></span> </dl>             | <span data-ttu-id="25b39-138">Ripristina lo stato dell'IME precedente quando il controllo riceve lo stato attivo per l'input.</span><span class="sxs-lookup"><span data-stu-id="25b39-138">Restores the previous IME status when the control receives the input focus.</span></span><br/>                                                                                                           |
| <span id="IMF_MULTIPLEEDIT"></span><span id="imf_multipleedit"></span><dl> <span data-ttu-id="25b39-139"><dt>**\_MULTIPLEEDIT FMI**</dt></span><span class="sxs-lookup"><span data-stu-id="25b39-139"><dt>**IMF\_MULTIPLEEDIT**</dt></span></span> </dl>                | <span data-ttu-id="25b39-140">Specifica che la stringa di composizione non verrà annullata o determinata dalla modifica dello stato attivo.</span><span class="sxs-lookup"><span data-stu-id="25b39-140">Specifies that the composition string will not be canceled or determined by focus changes.</span></span> <span data-ttu-id="25b39-141">Questo consente a un'applicazione di avere stringhe di composizione separate in ogni controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="25b39-141">This allows an application to have separate composition strings on each rich edit control.</span></span><br/> |
| <span id="IMF_VERTICAL"></span><span id="imf_vertical"></span><dl> <span data-ttu-id="25b39-142"><dt>**FMI \_ verticale**</dt></span><span class="sxs-lookup"><span data-stu-id="25b39-142"><dt>**IMF\_VERTICAL**</dt></span></span> </dl>                            | <span data-ttu-id="25b39-143">Nota utilizzata in Rich Edit 2,0 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="25b39-143">Note used in Rich Edit 2.0 and later.</span></span> <br/>                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25b39-144">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="25b39-144">Return value</span></span>

<span data-ttu-id="25b39-145">Se l'operazione ha esito positivo, il valore restituito è un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="25b39-145">If the operation succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="25b39-146">Se l'operazione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="25b39-146">If the operation fails, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="25b39-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="25b39-147">Requirements</span></span>



| <span data-ttu-id="25b39-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="25b39-148">Requirement</span></span> | <span data-ttu-id="25b39-149">Valore</span><span class="sxs-lookup"><span data-stu-id="25b39-149">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="25b39-150">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="25b39-150">Minimum supported client</span></span><br/> | <span data-ttu-id="25b39-151">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="25b39-151">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="25b39-152">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="25b39-152">Minimum supported server</span></span><br/> | <span data-ttu-id="25b39-153">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="25b39-153">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="25b39-154">Intestazione</span><span class="sxs-lookup"><span data-stu-id="25b39-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="25b39-155"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="25b39-155"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25b39-156">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="25b39-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25b39-157">**\_GETIMEOPTIONS em**</span><span class="sxs-lookup"><span data-stu-id="25b39-157">**EM\_GETIMEOPTIONS**</span></span>](em-getimeoptions.md)
</dt> </dl>

 

 





