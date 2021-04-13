---
title: Messaggio EM_SETWORDBREAKPROC (winuser. h)
description: Sostituisce la funzione WordWrap predefinita di un controllo di modifica con una funzione WordWrap definita dall'applicazione. Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.
ms.assetid: e5029b75-5f35-43a5-876d-24e81605bb49
keywords:
- Controlli di Windows Message EM_SETWORDBREAKPROC
topic_type:
- apiref
api_name:
- EM_SETWORDBREAKPROC
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e85335562c9e9881093d89293e7e2ace9cf43b0a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517974"
---
# <a name="em_setwordbreakproc-message"></a><span data-ttu-id="fc6d4-105">\_Messaggio SETWORDBREAKPROC em</span><span class="sxs-lookup"><span data-stu-id="fc6d4-105">EM\_SETWORDBREAKPROC message</span></span>

<span data-ttu-id="fc6d4-106">Sostituisce la funzione WordWrap predefinita di un controllo di modifica con una funzione WordWrap definita dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="fc6d4-106">Replaces an edit control's default Wordwrap function with an application-defined Wordwrap function.</span></span> <span data-ttu-id="fc6d4-107">Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="fc6d4-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="fc6d4-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="fc6d4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc6d4-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fc6d4-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fc6d4-110">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="fc6d4-110">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="fc6d4-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fc6d4-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fc6d4-112">Indirizzo della funzione WordWrap definita dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="fc6d4-112">The address of the application-defined Wordwrap function.</span></span> <span data-ttu-id="fc6d4-113">Per ulteriori informazioni sulle interruzioni delle righe, vedere la descrizione della funzione di callback [*EditWordBreakProc*](/windows/win32/api/winuser/nc-winuser-editwordbreakproca) .</span><span class="sxs-lookup"><span data-stu-id="fc6d4-113">For more information about breaking lines, see the description of the [*EditWordBreakProc*](/windows/win32/api/winuser/nc-winuser-editwordbreakproca) callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc6d4-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fc6d4-114">Return value</span></span>

<span data-ttu-id="fc6d4-115">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="fc6d4-115">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc6d4-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="fc6d4-116">Remarks</span></span>

<span data-ttu-id="fc6d4-117">Una funzione WordWrap analizza un buffer di testo contenente il testo da inviare allo schermo, cercando la prima parola che non rientra nella riga della schermata corrente.</span><span class="sxs-lookup"><span data-stu-id="fc6d4-117">A Wordwrap function scans a text buffer that contains text to be sent to the screen, looking for the first word that does not fit on the current screen line.</span></span> <span data-ttu-id="fc6d4-118">La funzione WordWrap posiziona questa parola all'inizio della riga successiva sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="fc6d4-118">The Wordwrap function places this word at the beginning of the next line on the screen.</span></span>

<span data-ttu-id="fc6d4-119">Una funzione WordWrap definisce il punto in cui il sistema deve suddividere una riga di testo per i controlli di modifica su più righe, in genere in un carattere spazio che separa due parole.</span><span class="sxs-lookup"><span data-stu-id="fc6d4-119">A Wordwrap function defines the point at which the system should break a line of text for multiline edit controls, usually at a space character that separates two words.</span></span> <span data-ttu-id="fc6d4-120">Un controllo di modifica su più righe o su una sola riga potrebbe chiamare questa funzione quando l'utente preme i tasti di direzione in combinazione con il tasto CTRL per spostare il punto di inserimento alla parola successiva o alla parola precedente.</span><span class="sxs-lookup"><span data-stu-id="fc6d4-120">Either a multiline or a single-line edit control might call this function when the user presses arrow keys in combination with the CTRL key to move the caret to the next word or previous word.</span></span> <span data-ttu-id="fc6d4-121">La funzione WordWrap predefinita interrompe una riga di testo in un carattere spazio.</span><span class="sxs-lookup"><span data-stu-id="fc6d4-121">The default Wordwrap function breaks a line of text at a space character.</span></span> <span data-ttu-id="fc6d4-122">La funzione definita dall'applicazione può definire WordWrap in modo che si verifichino a un trattino o a un carattere diverso dal carattere spazio.</span><span class="sxs-lookup"><span data-stu-id="fc6d4-122">The application-defined function may define the Wordwrap to occur at a hyphen or a character other than the space character.</span></span>

<span data-ttu-id="fc6d4-123">**Modifica avanzata:** Supportato in Microsoft Rich Edit 1,0 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="fc6d4-123">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="fc6d4-124">Per informazioni sulla compatibilità delle versioni Rich Edit con le varie versioni di sistema, vedere [informazioni sui controlli Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="fc6d4-124">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fc6d4-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fc6d4-125">Requirements</span></span>



| <span data-ttu-id="fc6d4-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc6d4-126">Requirement</span></span> | <span data-ttu-id="fc6d4-127">Valore</span><span class="sxs-lookup"><span data-stu-id="fc6d4-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc6d4-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fc6d4-128">Minimum supported client</span></span><br/> | <span data-ttu-id="fc6d4-129">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fc6d4-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="fc6d4-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fc6d4-130">Minimum supported server</span></span><br/> | <span data-ttu-id="fc6d4-131">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fc6d4-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fc6d4-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fc6d4-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc6d4-133"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fc6d4-133"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc6d4-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fc6d4-134">See also</span></span>

<dl> <dt>

<span data-ttu-id="fc6d4-135">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="fc6d4-135">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="fc6d4-136">*EditWordBreakProc*</span><span class="sxs-lookup"><span data-stu-id="fc6d4-136">*EditWordBreakProc*</span></span>](/windows/win32/api/winuser/nc-winuser-editwordbreakproca)
</dt> <dt>

[<span data-ttu-id="fc6d4-137">**\_FMTLINES em**</span><span class="sxs-lookup"><span data-stu-id="fc6d4-137">**EM\_FMTLINES**</span></span>](em-fmtlines.md)
</dt> <dt>

[<span data-ttu-id="fc6d4-138">**\_GETWORDBREAKPROC em**</span><span class="sxs-lookup"><span data-stu-id="fc6d4-138">**EM\_GETWORDBREAKPROC**</span></span>](em-getwordbreakproc.md)
</dt> </dl>

 

