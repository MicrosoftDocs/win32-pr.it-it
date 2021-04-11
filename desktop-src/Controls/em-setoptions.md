---
title: Messaggio di EM_SETOPTIONS (RichEdit. h)
description: Imposta le opzioni per un controllo Rich Edit.
ms.assetid: 98ef2de9-4c34-45ba-8e8a-eaf505f97f56
keywords:
- Controlli di Windows Message EM_SETOPTIONS
topic_type:
- apiref
api_name:
- EM_SETOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c43dda8268b42dc264a86600826d2a6b550e35c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119598"
---
# <a name="em_setoptions-message"></a><span data-ttu-id="a3aee-104">\_Messaggio SEoptions em</span><span class="sxs-lookup"><span data-stu-id="a3aee-104">EM\_SETOPTIONS message</span></span>

<span data-ttu-id="a3aee-105">Imposta le opzioni per un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="a3aee-105">Sets the options for a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="a3aee-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a3aee-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3aee-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a3aee-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a3aee-108">Specifica l'operazione. i possibili valori sono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="a3aee-108">Specifies the operation, which can be one of these values.</span></span>



| <span data-ttu-id="a3aee-109">Valore</span><span class="sxs-lookup"><span data-stu-id="a3aee-109">Value</span></span>                                                                                                                                             | <span data-ttu-id="a3aee-110">Significato</span><span class="sxs-lookup"><span data-stu-id="a3aee-110">Meaning</span></span>                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="ECOOP_SET"></span><span id="ecoop_set"></span><dl> <span data-ttu-id="a3aee-111"><dt>**SET di ECOOP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a3aee-111"><dt>**ECOOP\_SET**</dt></span></span> </dl> | <span data-ttu-id="a3aee-112">Imposta le opzioni su quelle specificate da *lParam*.</span><span class="sxs-lookup"><span data-stu-id="a3aee-112">Sets the options to those specified by *lParam*.</span></span><br/>                             |
| <span id="ECOOP_OR"></span><span id="ecoop_or"></span><dl> <span data-ttu-id="a3aee-113"><dt>**ECOOP \_ o**</dt></span><span class="sxs-lookup"><span data-stu-id="a3aee-113"><dt>**ECOOP\_OR**</dt></span></span> </dl>    | <span data-ttu-id="a3aee-114">Combina le opzioni specificate con le opzioni correnti.</span><span class="sxs-lookup"><span data-stu-id="a3aee-114">Combines the specified options with the current options.</span></span><br/>                     |
| <span id="ECOOP_AND"></span><span id="ecoop_and"></span><dl> <span data-ttu-id="a3aee-115"><dt>**ECOOP \_ e**</dt></span><span class="sxs-lookup"><span data-stu-id="a3aee-115"><dt>**ECOOP\_AND**</dt></span></span> </dl> | <span data-ttu-id="a3aee-116">Mantiene solo le opzioni correnti specificate anche da *lParam*.</span><span class="sxs-lookup"><span data-stu-id="a3aee-116">Retains only those current options that are also specified by *lParam*.</span></span><br/>      |
| <span id="ECOOP_XOR"></span><span id="ecoop_xor"></span><dl> <span data-ttu-id="a3aee-117"><dt>**\_Xor ECOOP**</dt></span><span class="sxs-lookup"><span data-stu-id="a3aee-117"><dt>**ECOOP\_XOR**</dt></span></span> </dl> | <span data-ttu-id="a3aee-118">Logicamente esclusivo o opzioni correnti con quelle specificate da *lParam*.</span><span class="sxs-lookup"><span data-stu-id="a3aee-118">Logically exclusive OR the current options with those specified by *lParam*.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a3aee-119">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a3aee-119">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a3aee-120">Specifica uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="a3aee-120">Specifies one or more of the following values.</span></span>



| <span data-ttu-id="a3aee-121">Valore</span><span class="sxs-lookup"><span data-stu-id="a3aee-121">Value</span></span>                                                                                                                                                                                 | <span data-ttu-id="a3aee-122">Significato</span><span class="sxs-lookup"><span data-stu-id="a3aee-122">Meaning</span></span>                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="ECO_AUTOWORDSELECTION"></span><span id="eco_autowordselection"></span><dl> <span data-ttu-id="a3aee-123"><dt>**\_AUTOWORDSELECTION eco**</dt></span><span class="sxs-lookup"><span data-stu-id="a3aee-123"><dt>**ECO\_AUTOWORDSELECTION**</dt></span></span> </dl> | <span data-ttu-id="a3aee-124">Selezione automatica di Word con doppio clic.</span><span class="sxs-lookup"><span data-stu-id="a3aee-124">Automatic selection of word on double-click.</span></span><br/>                                                                           |
| <span id="ECO_AUTOVSCROLL"></span><span id="eco_autovscroll"></span><dl> <span data-ttu-id="a3aee-125"><dt>**\_AUTOVSCROLL eco**</dt></span><span class="sxs-lookup"><span data-stu-id="a3aee-125"><dt>**ECO\_AUTOVSCROLL**</dt></span></span> </dl>                   | <span data-ttu-id="a3aee-126">Uguale allo stile [**es \_ AUTOVSCROLL**](rich-edit-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="a3aee-126">Same as [**ES\_AUTOVSCROLL**](rich-edit-control-styles.md) style.</span></span><br/>                                      |
| <span id="ECO_AUTOHSCROLL"></span><span id="eco_autohscroll"></span><dl> <span data-ttu-id="a3aee-127"><dt>**\_AUTOHSCROLL eco**</dt></span><span class="sxs-lookup"><span data-stu-id="a3aee-127"><dt>**ECO\_AUTOHSCROLL**</dt></span></span> </dl>                   | <span data-ttu-id="a3aee-128">Uguale allo stile [**es \_ AUTOHSCROLL**](rich-edit-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="a3aee-128">Same as [**ES\_AUTOHSCROLL**](rich-edit-control-styles.md) style.</span></span><br/>                                      |
| <span id="ECO_NOHIDESEL"></span><span id="eco_nohidesel"></span><dl> <span data-ttu-id="a3aee-129"><dt>**\_NOHIDESEL eco**</dt></span><span class="sxs-lookup"><span data-stu-id="a3aee-129"><dt>**ECO\_NOHIDESEL**</dt></span></span> </dl>                         | <span data-ttu-id="a3aee-130">Uguale allo stile [**es \_ NOHIDESEL**](rich-edit-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="a3aee-130">Same as [**ES\_NOHIDESEL**](rich-edit-control-styles.md) style.</span></span><br/>                                          |
| <span id="ECO_READONLY"></span><span id="eco_readonly"></span><dl> <span data-ttu-id="a3aee-131"><dt>**ECO \_ ReadOnly**</dt></span><span class="sxs-lookup"><span data-stu-id="a3aee-131"><dt>**ECO\_READONLY**</dt></span></span> </dl>                            | <span data-ttu-id="a3aee-132">Uguale allo stile di sola [**\_ lettura di es**](rich-edit-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="a3aee-132">Same as [**ES\_READONLY**](rich-edit-control-styles.md) style.</span></span><br/>                                            |
| <span id="ECO_WANTRETURN"></span><span id="eco_wantreturn"></span><dl> <span data-ttu-id="a3aee-133"><dt>**\_WANTRETURN eco**</dt></span><span class="sxs-lookup"><span data-stu-id="a3aee-133"><dt>**ECO\_WANTRETURN**</dt></span></span> </dl>                      | <span data-ttu-id="a3aee-134">Uguale allo stile [**es \_ WANTRETURN**](rich-edit-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="a3aee-134">Same as [**ES\_WANTRETURN**](rich-edit-control-styles.md) style.</span></span><br/>                                        |
| <span id="ECO_SELECTIONBAR"></span><span id="eco_selectionbar"></span><dl> <span data-ttu-id="a3aee-135"><dt>**\_SELECTIONBAR eco**</dt></span><span class="sxs-lookup"><span data-stu-id="a3aee-135"><dt>**ECO\_SELECTIONBAR**</dt></span></span> </dl>                | <span data-ttu-id="a3aee-136">Uguale allo stile [**es \_ SELECTIONBAR**](rich-edit-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="a3aee-136">Same as [**ES\_SELECTIONBAR**](rich-edit-control-styles.md) style.</span></span><br/>                                    |
| <span id="ECO_VERTICAL"></span><span id="eco_vertical"></span><dl> <span data-ttu-id="a3aee-137"><dt>**ECO \_ verticale**</dt></span><span class="sxs-lookup"><span data-stu-id="a3aee-137"><dt>**ECO\_VERTICAL**</dt></span></span> </dl>                            | <span data-ttu-id="a3aee-138">Uguale allo [**stile \_ verticale es**](rich-edit-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="a3aee-138">Same as [**ES\_VERTICAL**](rich-edit-control-styles.md) style.</span></span> <span data-ttu-id="a3aee-139">Disponibile solo nelle versioni in lingua asiatica.</span><span class="sxs-lookup"><span data-stu-id="a3aee-139">Available in Asian-language versions only.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3aee-140">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a3aee-140">Return value</span></span>

<span data-ttu-id="a3aee-141">Questo messaggio restituisce le opzioni correnti del controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="a3aee-141">This message returns the current options of the edit control.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3aee-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a3aee-142">Requirements</span></span>



| <span data-ttu-id="a3aee-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3aee-143">Requirement</span></span> | <span data-ttu-id="a3aee-144">Valore</span><span class="sxs-lookup"><span data-stu-id="a3aee-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a3aee-145">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a3aee-145">Minimum supported client</span></span><br/> | <span data-ttu-id="a3aee-146">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a3aee-146">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a3aee-147">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a3aee-147">Minimum supported server</span></span><br/> | <span data-ttu-id="a3aee-148">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a3aee-148">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a3aee-149">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a3aee-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3aee-150"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3aee-150"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3aee-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a3aee-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3aee-152">**Stili del controllo Rich Edit**</span><span class="sxs-lookup"><span data-stu-id="a3aee-152">**Rich Edit Control Styles**</span></span>](rich-edit-control-styles.md)
</dt> </dl>

 

 





