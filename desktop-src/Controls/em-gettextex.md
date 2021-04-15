---
title: Messaggio di EM_GETTEXTEX (RichEdit. h)
description: Ottiene il testo da un controllo Rich Edit.
ms.assetid: 46431563-fde1-4407-ab7a-b2248c0e12b8
keywords:
- Controlli di Windows Message EM_GETTEXTEX
topic_type:
- apiref
api_name:
- EM_GETTEXTEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 357cfe37d3432b396183b500c945ad89397c0294
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476480"
---
# <a name="em_gettextex-message"></a><span data-ttu-id="8f673-104">\_Messaggio GETTEXTEX em</span><span class="sxs-lookup"><span data-stu-id="8f673-104">EM\_GETTEXTEX message</span></span>

<span data-ttu-id="8f673-105">Ottiene il testo da un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="8f673-105">Gets the text from a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="8f673-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8f673-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f673-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8f673-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8f673-108">Puntatore a una struttura [**GETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-gettextex) , che indica come tradurre il testo prima di inserirlo nel buffer di output.</span><span class="sxs-lookup"><span data-stu-id="8f673-108">Pointer to a [**GETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-gettextex) structure, which indicates how to translate the text before putting it into the output buffer.</span></span>

</dd> <dt>

<span data-ttu-id="8f673-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8f673-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8f673-110">Puntatore al buffer per ricevere il testo.</span><span class="sxs-lookup"><span data-stu-id="8f673-110">Pointer to the buffer to receive the text.</span></span> <span data-ttu-id="8f673-111">Le dimensioni del buffer, in byte, sono specificate dal membro **CB** della struttura [**GETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-gettextex) .</span><span class="sxs-lookup"><span data-stu-id="8f673-111">The size of this buffer, in bytes, is specified by the **cb** member of the [**GETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-gettextex) structure.</span></span> <span data-ttu-id="8f673-112">Usare il [**messaggio \_ GetTextLengthEx em**](em-gettextlengthex.md) per ottenere la dimensione richiesta del buffer.</span><span class="sxs-lookup"><span data-stu-id="8f673-112">Use the [**EM\_GETTEXTLENGTHEX**](em-gettextlengthex.md) message to get the required size of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f673-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8f673-113">Return value</span></span>

<span data-ttu-id="8f673-114">Il valore restituito è il numero di **TCHAR** copiate nel buffer di output, incluso il carattere di terminazione null.</span><span class="sxs-lookup"><span data-stu-id="8f673-114">The return value is the number of **TCHAR** s copied into the output buffer, including the null terminator.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f673-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="8f673-115">Remarks</span></span>

<span data-ttu-id="8f673-116">Se la dimensione del buffer di output è inferiore alla dimensione del testo nel controllo, il controllo di modifica copia il testo dall'inizio e lo inserisce nel buffer finché il buffer non è pieno.</span><span class="sxs-lookup"><span data-stu-id="8f673-116">If the size of the output buffer is less than the size of the text in the control, the edit control will copy text from its beginning and place it in the buffer until the buffer is full.</span></span> <span data-ttu-id="8f673-117">Un carattere di terminazione null verrà ancora inserito alla fine del buffer.</span><span class="sxs-lookup"><span data-stu-id="8f673-117">A terminating null character will still be placed at the end of the buffer.</span></span>

<span data-ttu-id="8f673-118">Se viene richiesto testo ANSI, **em \_ GETTEXTEX** usa la funzione [**WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) per convertire i caratteri Unicode in ANSI.</span><span class="sxs-lookup"><span data-stu-id="8f673-118">If ANSI text is requested, **EM\_GETTEXTEX** uses the [**WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) function to translate the Unicode characters to ANSI.</span></span> <span data-ttu-id="8f673-119">Consente di passare da Unicode a ANSI usando una determinata tabella codici.</span><span class="sxs-lookup"><span data-stu-id="8f673-119">It allows you to go from Unicode to ANSI using a particular code page.</span></span> <span data-ttu-id="8f673-120">La struttura [**GETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-gettextex) contiene i membri (**lpDefaultChar** e **lpUsedDefChar**) usati nella conversione da Unicode ad ANSI.</span><span class="sxs-lookup"><span data-stu-id="8f673-120">The [**GETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-gettextex) structure contains members (**lpDefaultChar** and **lpUsedDefChar**) that are used in the translation from Unicode to ANSI.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f673-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8f673-121">Requirements</span></span>



| <span data-ttu-id="8f673-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f673-122">Requirement</span></span> | <span data-ttu-id="8f673-123">Valore</span><span class="sxs-lookup"><span data-stu-id="8f673-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8f673-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8f673-124">Minimum supported client</span></span><br/> | <span data-ttu-id="8f673-125">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8f673-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8f673-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8f673-126">Minimum supported server</span></span><br/> | <span data-ttu-id="8f673-127">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8f673-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8f673-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8f673-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f673-129"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f673-129"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f673-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8f673-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="8f673-131">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="8f673-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8f673-132">**\_SETTEXTEX em**</span><span class="sxs-lookup"><span data-stu-id="8f673-132">**EM\_SETTEXTEX**</span></span>](em-settextex.md)
</dt> <dt>

[<span data-ttu-id="8f673-133">**GETTEXTEX**</span><span class="sxs-lookup"><span data-stu-id="8f673-133">**GETTEXTEX**</span></span>](/windows/desktop/api/Richedit/ns-richedit-gettextex)
</dt> <dt>

<span data-ttu-id="8f673-134">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="8f673-134">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="8f673-135">**WideCharToMultiByte**</span><span class="sxs-lookup"><span data-stu-id="8f673-135">**WideCharToMultiByte**</span></span>](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte)
</dt> <dt>

[<span data-ttu-id="8f673-136">**\_testo WM**</span><span class="sxs-lookup"><span data-stu-id="8f673-136">**WM\_SETTEXT**</span></span>](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 

