---
title: Messaggio di EM_SETWORDWRAPMODE (RichEdit. h)
description: Imposta le opzioni di ritorno a capo automatico e di suddivisione in parole per un controllo Rich Edit.
ms.assetid: 43703ac8-6ae5-470b-9156-e60330ef97c4
keywords:
- Controlli di Windows Message EM_SETWORDWRAPMODE
topic_type:
- apiref
api_name:
- EM_SETWORDWRAPMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf1dc6f064f52bf2a5f58c71db099f38b9350e63
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048477"
---
# <a name="em_setwordwrapmode-message"></a><span data-ttu-id="b5258-104">\_Messaggio SETWORDWRAPMODE em</span><span class="sxs-lookup"><span data-stu-id="b5258-104">EM\_SETWORDWRAPMODE message</span></span>

<span data-ttu-id="b5258-105">Imposta le opzioni di ritorno a capo automatico e di suddivisione in parole per un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="b5258-105">Sets the word-wrapping and word-breaking options for a rich edit control.</span></span>

> [!Note]  
> <span data-ttu-id="b5258-106">Questo messaggio è supportato solo nelle versioni in lingua asiatica di Microsoft Rich Edit 1,0.</span><span class="sxs-lookup"><span data-stu-id="b5258-106">This message is supported only in Asian-language versions of Microsoft Rich Edit 1.0.</span></span> <span data-ttu-id="b5258-107">Non è supportata nelle versioni successive.</span><span class="sxs-lookup"><span data-stu-id="b5258-107">It is not supported in any later versions.</span></span>

 

## <a name="parameters"></a><span data-ttu-id="b5258-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b5258-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5258-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b5258-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b5258-110">Specifica uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="b5258-110">Specifies one or more of the following values.</span></span>



| <span data-ttu-id="b5258-111">Valore</span><span class="sxs-lookup"><span data-stu-id="b5258-111">Value</span></span>                                                                                                                                                         | <span data-ttu-id="b5258-112">Significato</span><span class="sxs-lookup"><span data-stu-id="b5258-112">Meaning</span></span>                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span id="WBF_WORDWRAP"></span><span id="wbf_wordwrap"></span><dl> <span data-ttu-id="b5258-113"><dt>**\_WORDWRAP WBF**</dt></span><span class="sxs-lookup"><span data-stu-id="b5258-113"><dt>**WBF\_WORDWRAP**</dt></span></span> </dl>    | <span data-ttu-id="b5258-114">Abilita le operazioni a capo automatico specifiche per le lingue asiatiche, ad esempio Kinsoku in giapponese.</span><span class="sxs-lookup"><span data-stu-id="b5258-114">Enables Asian-specific word wrap operations, such as kinsoku in Japanese.</span></span> <br/>                                 |
| <span id="WBF_WORDBREAK"></span><span id="wbf_wordbreak"></span><dl> <span data-ttu-id="b5258-115"><dt>**\_WordBreak WBF**</dt></span><span class="sxs-lookup"><span data-stu-id="b5258-115"><dt>**WBF\_WORDBREAK**</dt></span></span> </dl> | <span data-ttu-id="b5258-116">Abilita le operazioni di suddivisione in parole inglesi in giapponese e cinese.</span><span class="sxs-lookup"><span data-stu-id="b5258-116">Enables English word-breaking operations in Japanese and Chinese.</span></span> <span data-ttu-id="b5258-117">Abilita l'operazione di suddivisione in parole Hangeul.</span><span class="sxs-lookup"><span data-stu-id="b5258-117">Enables Hangeul word-breaking operation.</span></span><br/> |
| <span id="WBF_OVERFLOW"></span><span id="wbf_overflow"></span><dl> <span data-ttu-id="b5258-118"><dt>**\_overflow WBF**</dt></span><span class="sxs-lookup"><span data-stu-id="b5258-118"><dt>**WBF\_OVERFLOW**</dt></span></span> </dl>    | <span data-ttu-id="b5258-119">Riconosce la punteggiatura dell'overflow.</span><span class="sxs-lookup"><span data-stu-id="b5258-119">Recognizes overflow punctuation.</span></span> <span data-ttu-id="b5258-120">(Attualmente non supportata).</span><span class="sxs-lookup"><span data-stu-id="b5258-120">(Not currently supported.)</span></span><br/>                                                |
| <span id="WBF_LEVEL1"></span><span id="wbf_level1"></span><dl> <span data-ttu-id="b5258-121"><dt>**\_Level1 WBF**</dt></span><span class="sxs-lookup"><span data-stu-id="b5258-121"><dt>**WBF\_LEVEL1**</dt></span></span> </dl>          | <span data-ttu-id="b5258-122">Imposta come predefinita la tabella di punteggiatura di livello 1.</span><span class="sxs-lookup"><span data-stu-id="b5258-122">Sets the Level 1 punctuation table as the default.</span></span><br/>                                                         |
| <span id="WBF_LEVEL2"></span><span id="wbf_level2"></span><dl> <span data-ttu-id="b5258-123"><dt>**\_Level2 WBF**</dt></span><span class="sxs-lookup"><span data-stu-id="b5258-123"><dt>**WBF\_LEVEL2**</dt></span></span> </dl>          | <span data-ttu-id="b5258-124">Imposta la tabella di punteggiatura di livello 2 come valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="b5258-124">Sets the Level 2 punctuation table as the default.</span></span><br/>                                                         |
| <span id="WBF_CUSTOM"></span><span id="wbf_custom"></span><dl> <span data-ttu-id="b5258-125"><dt>**WBF \_ personalizzato**</dt></span><span class="sxs-lookup"><span data-stu-id="b5258-125"><dt>**WBF\_CUSTOM**</dt></span></span> </dl>          | <span data-ttu-id="b5258-126">Imposta la tabella di punteggiatura definita dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b5258-126">Sets the application-defined punctuation table.</span></span><br/>                                                            |



 

</dd> <dt>

<span data-ttu-id="b5258-127">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b5258-127">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b5258-128">Questo parametro non viene utilizzato. deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="b5258-128">This parameter is not used; it must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5258-129">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b5258-129">Return value</span></span>

<span data-ttu-id="b5258-130">Questo messaggio restituisce le opzioni di ritorno a capo e di suddivisione in parole correnti.</span><span class="sxs-lookup"><span data-stu-id="b5258-130">This message returns the current word-wrapping and word-breaking options.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5258-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="b5258-131">Remarks</span></span>

<span data-ttu-id="b5258-132">Questo messaggio non deve essere inviato dalla procedura di suddivisione delle parole definita dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b5258-132">This message must not be sent by the application defined word breaking procedure.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5258-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b5258-133">Requirements</span></span>



| <span data-ttu-id="b5258-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5258-134">Requirement</span></span> | <span data-ttu-id="b5258-135">Valore</span><span class="sxs-lookup"><span data-stu-id="b5258-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b5258-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b5258-136">Minimum supported client</span></span><br/> | <span data-ttu-id="b5258-137">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b5258-137">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b5258-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b5258-138">Minimum supported server</span></span><br/> | <span data-ttu-id="b5258-139">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b5258-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b5258-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b5258-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5258-141"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5258-141"><dt>Richedit.h</dt></span></span> </dl> |



 

 





