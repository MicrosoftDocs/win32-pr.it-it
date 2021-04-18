---
title: Messaggio EM_GETWORDBREAKPROC (winuser. h)
description: Ottiene l'indirizzo della funzione WordWrap corrente. Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.
ms.assetid: 564b4b1b-913f-4040-bb28-eea50c0c3738
keywords:
- Controlli di Windows Message EM_GETWORDBREAKPROC
topic_type:
- apiref
api_name:
- EM_GETWORDBREAKPROC
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: feb9499492668abac24774b66304ae8a87a2d739
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478107"
---
# <a name="em_getwordbreakproc-message"></a><span data-ttu-id="6af00-105">\_Messaggio GETWORDBREAKPROC em</span><span class="sxs-lookup"><span data-stu-id="6af00-105">EM\_GETWORDBREAKPROC message</span></span>

<span data-ttu-id="6af00-106">Ottiene l'indirizzo della funzione WordWrap corrente.</span><span class="sxs-lookup"><span data-stu-id="6af00-106">Gets the address of the current Wordwrap function.</span></span> <span data-ttu-id="6af00-107">Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="6af00-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="6af00-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="6af00-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6af00-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6af00-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6af00-110">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="6af00-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="6af00-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6af00-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6af00-112">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="6af00-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6af00-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6af00-113">Return value</span></span>

<span data-ttu-id="6af00-114">Il valore restituito specifica l'indirizzo della funzione WordWrap definita dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6af00-114">The return value specifies the address of the application-defined Wordwrap function.</span></span> <span data-ttu-id="6af00-115">Il valore restituito è **null** se non esiste alcuna funzione WordWrap.</span><span class="sxs-lookup"><span data-stu-id="6af00-115">The return value is **NULL** if no Wordwrap function exists.</span></span>

## <a name="remarks"></a><span data-ttu-id="6af00-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="6af00-116">Remarks</span></span>

<span data-ttu-id="6af00-117">Una funzione WordWrap analizza un buffer di testo contenente il testo da inviare alla visualizzazione, cercando la prima parola che non rientra nella riga di visualizzazione corrente.</span><span class="sxs-lookup"><span data-stu-id="6af00-117">A Wordwrap function scans a text buffer that contains text to be sent to the display, looking for the first word that does not fit on the current display line.</span></span> <span data-ttu-id="6af00-118">La funzione WordWrap posiziona questa parola all'inizio della riga successiva sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="6af00-118">The wordwrap function places this word at the beginning of the next line on the display.</span></span> <span data-ttu-id="6af00-119">Una funzione WordWrap definisce il punto in cui il sistema deve suddividere una riga di testo per i controlli di modifica su più righe, in genere in un carattere spazio che separa due parole.</span><span class="sxs-lookup"><span data-stu-id="6af00-119">A Wordwrap function defines the point at which the system should break a line of text for multiline edit controls, usually at a space character that separates two words.</span></span>

<span data-ttu-id="6af00-120">**Modifica avanzata:** Supportato in Microsoft Rich Edit 1,0 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="6af00-120">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="6af00-121">Per informazioni sulla compatibilità delle versioni Rich Edit con le varie versioni di sistema, vedere [informazioni sui controlli Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="6af00-121">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6af00-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6af00-122">Requirements</span></span>



| <span data-ttu-id="6af00-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="6af00-123">Requirement</span></span> | <span data-ttu-id="6af00-124">Valore</span><span class="sxs-lookup"><span data-stu-id="6af00-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6af00-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6af00-125">Minimum supported client</span></span><br/> | <span data-ttu-id="6af00-126">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6af00-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6af00-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6af00-127">Minimum supported server</span></span><br/> | <span data-ttu-id="6af00-128">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6af00-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6af00-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6af00-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="6af00-130"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6af00-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6af00-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6af00-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="6af00-132">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="6af00-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6af00-133">*EditWordBreakProc*</span><span class="sxs-lookup"><span data-stu-id="6af00-133">*EditWordBreakProc*</span></span>](/windows/win32/api/winuser/nc-winuser-editwordbreakproca)
</dt> <dt>

[<span data-ttu-id="6af00-134">**\_FMTLINES em**</span><span class="sxs-lookup"><span data-stu-id="6af00-134">**EM\_FMTLINES**</span></span>](em-fmtlines.md)
</dt> <dt>

[<span data-ttu-id="6af00-135">**\_SETWORDBREAKPROC em**</span><span class="sxs-lookup"><span data-stu-id="6af00-135">**EM\_SETWORDBREAKPROC**</span></span>](em-setwordbreakproc.md)
</dt> </dl>

 

