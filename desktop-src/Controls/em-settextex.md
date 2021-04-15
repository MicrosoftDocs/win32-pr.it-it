---
title: Messaggio di EM_SETTEXTEX (RichEdit. h)
description: Combina la funzionalità dei messaggi WM \_ REPLACESEL e em e \_ consente di impostare il testo usando una tabella codici e di usare testo RTF o testo normale.
ms.assetid: 1ba9e4c0-7870-4057-8a8b-d0e6577349ac
keywords:
- Controlli di Windows Message EM_SETTEXTEX
topic_type:
- apiref
api_name:
- EM_SETTEXTEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfdd7dece965f70fe41d40edf44d365795d44fc4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477309"
---
# <a name="em_settextex-message"></a><span data-ttu-id="39aae-104">\_Messaggio SETTEXTEX em</span><span class="sxs-lookup"><span data-stu-id="39aae-104">EM\_SETTEXTEX message</span></span>

<span data-ttu-id="39aae-105">Combina la funzionalità dei messaggi [**WM \_**](/windows/desktop/winmsg/wm-settext) [**\_ REPLACESEL e em**](em-replacesel.md) e consente di impostare il testo usando una tabella codici e di usare testo RTF o testo normale.</span><span class="sxs-lookup"><span data-stu-id="39aae-105">Combines the functionality of the [**WM\_SETTEXT**](/windows/desktop/winmsg/wm-settext) and [**EM\_REPLACESEL**](em-replacesel.md) messages, and adds the ability to set text using a code page and to use either rich text or plain text.</span></span>

## <a name="parameters"></a><span data-ttu-id="39aae-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="39aae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39aae-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="39aae-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="39aae-108">Puntatore a una struttura [**SETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-settextex) che specifica i flag e una tabella codici facoltativa da usare per la conversione in Unicode.</span><span class="sxs-lookup"><span data-stu-id="39aae-108">Pointer to a [**SETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-settextex) structure that specifies flags and an optional code page to use in translating to Unicode.</span></span>

</dd> <dt>

<span data-ttu-id="39aae-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="39aae-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="39aae-110">Puntatore al testo con terminazione null da inserire.</span><span class="sxs-lookup"><span data-stu-id="39aae-110">Pointer to the null-terminated text to insert.</span></span> <span data-ttu-id="39aae-111">Questo testo è una stringa ANSI, a meno che la tabella codici non sia 1200 (Unicode).</span><span class="sxs-lookup"><span data-stu-id="39aae-111">This text is an ANSI string, unless the code page is 1200 (Unicode).</span></span> <span data-ttu-id="39aae-112">Se *lParam* inizia con una sequenza ASCII RTF valida, ad esempio "{ \\ RTF" o "{urtf", il testo viene letto usando il lettore RTF.</span><span class="sxs-lookup"><span data-stu-id="39aae-112">If *lParam* starts with a valid RTF ASCII sequence for example, "{\\rtf" or "{urtf" the text is read in using the RTF reader.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39aae-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="39aae-113">Return value</span></span>

<span data-ttu-id="39aae-114">Se l'operazione sta impostando tutto il testo e ha esito positivo, il valore restituito è 1.</span><span class="sxs-lookup"><span data-stu-id="39aae-114">If the operation is setting all of the text and succeeds, the return value is 1.</span></span>

<span data-ttu-id="39aae-115">Se l'operazione sta impostando la selezione e ha esito positivo, il valore restituito è il numero di byte o caratteri copiati.</span><span class="sxs-lookup"><span data-stu-id="39aae-115">If the operation is setting the selection and succeeds, the return value is the number of bytes or characters copied.</span></span>

<span data-ttu-id="39aae-116">Se l'operazione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="39aae-116">If the operation fails, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="39aae-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="39aae-117">Requirements</span></span>



| <span data-ttu-id="39aae-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="39aae-118">Requirement</span></span> | <span data-ttu-id="39aae-119">Valore</span><span class="sxs-lookup"><span data-stu-id="39aae-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="39aae-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="39aae-120">Minimum supported client</span></span><br/> | <span data-ttu-id="39aae-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="39aae-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="39aae-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="39aae-122">Minimum supported server</span></span><br/> | <span data-ttu-id="39aae-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="39aae-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="39aae-124">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="39aae-124">Redistributable</span></span><br/>          | <span data-ttu-id="39aae-125">Modifica avanzata 3,0</span><span class="sxs-lookup"><span data-stu-id="39aae-125">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="39aae-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="39aae-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="39aae-127"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="39aae-127"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39aae-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="39aae-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="39aae-129">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="39aae-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="39aae-130">**\_GETTEXTEX em**</span><span class="sxs-lookup"><span data-stu-id="39aae-130">**EM\_GETTEXTEX**</span></span>](em-gettextex.md)
</dt> <dt>

[<span data-ttu-id="39aae-131">**SETTEXTEX**</span><span class="sxs-lookup"><span data-stu-id="39aae-131">**SETTEXTEX**</span></span>](/windows/desktop/api/Richedit/ns-richedit-settextex)
</dt> </dl>

 

