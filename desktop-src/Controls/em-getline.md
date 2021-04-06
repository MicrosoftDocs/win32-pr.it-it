---
title: Messaggio EM_GETLINE (winuser. h)
description: Copia una riga di testo da un controllo di modifica e la inserisce in un buffer specificato. Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.
ms.assetid: ff56d2c6-5013-46c6-90d8-ee2bdc9074b1
keywords:
- Controlli di Windows Message EM_GETLINE
topic_type:
- apiref
api_name:
- EM_GETLINE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e014eaccba65b4ea1fc96e26872954a9cfc06e1e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963837"
---
# <a name="em_getline-message-winuserh"></a><span data-ttu-id="ec635-105">Messaggio EM_GETLINE (winuser. h)</span><span class="sxs-lookup"><span data-stu-id="ec635-105">EM_GETLINE message (Winuser.h)</span></span>

<span data-ttu-id="ec635-106">Copia una riga di testo da un controllo di modifica e la inserisce in un buffer specificato.</span><span class="sxs-lookup"><span data-stu-id="ec635-106">Copies a line of text from an edit control and places it in a specified buffer.</span></span> <span data-ttu-id="ec635-107">Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="ec635-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="ec635-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ec635-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec635-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ec635-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ec635-110">Indice in base zero della riga da recuperare da un controllo di modifica su più righe.</span><span class="sxs-lookup"><span data-stu-id="ec635-110">The zero-based index of the line to retrieve from a multiline edit control.</span></span> <span data-ttu-id="ec635-111">Un valore pari a zero specifica la riga più in alto.</span><span class="sxs-lookup"><span data-stu-id="ec635-111">A value of zero specifies the topmost line.</span></span> <span data-ttu-id="ec635-112">Questo parametro viene ignorato da un controllo di modifica a riga singola.</span><span class="sxs-lookup"><span data-stu-id="ec635-112">This parameter is ignored by a single-line edit control.</span></span>

</dd> <dt>

<span data-ttu-id="ec635-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ec635-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ec635-114">Puntatore al buffer che riceve una copia della riga.</span><span class="sxs-lookup"><span data-stu-id="ec635-114">A pointer to the buffer that receives a copy of the line.</span></span> <span data-ttu-id="ec635-115">Prima di inviare il messaggio, impostare la prima parola di questo buffer sulle dimensioni, in **TCHAR** s, del buffer.</span><span class="sxs-lookup"><span data-stu-id="ec635-115">Before sending the message, set the first word of this buffer to the size, in **TCHAR** s, of the buffer.</span></span> <span data-ttu-id="ec635-116">Per testo ANSI, indica il numero di byte; per il testo Unicode, indica il numero di caratteri.</span><span class="sxs-lookup"><span data-stu-id="ec635-116">For ANSI text, this is the number of bytes; for Unicode text, this is the number of characters.</span></span> <span data-ttu-id="ec635-117">La dimensione nella prima parola viene sovrascritta dalla riga copiata.</span><span class="sxs-lookup"><span data-stu-id="ec635-117">The size in the first word is overwritten by the copied line.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec635-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ec635-118">Return value</span></span>

<span data-ttu-id="ec635-119">Il valore restituito è il numero di **TCHAR** copiate.</span><span class="sxs-lookup"><span data-stu-id="ec635-119">The return value is the number of **TCHAR** s copied.</span></span> <span data-ttu-id="ec635-120">Il valore restituito è zero se il numero di riga specificato dal parametro *wParam* è maggiore del numero di righe nel controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="ec635-120">The return value is zero if the line number specified by the *wParam* parameter is greater than the number of lines in the edit control.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec635-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="ec635-121">Remarks</span></span>

<span data-ttu-id="ec635-122">**Controlli di modifica:** La riga copiata non contiene un carattere null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="ec635-122">**Edit controls:** The copied line does not contain a terminating null character.</span></span>

<span data-ttu-id="ec635-123">**Controlli Rich Edit:** Supportato in Microsoft Rich Edit 1,0 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="ec635-123">**Rich edit controls:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="ec635-124">La riga copiata non contiene un carattere null di terminazione, a meno che non sia stato copiato alcun testo.</span><span class="sxs-lookup"><span data-stu-id="ec635-124">The copied line does not contain a terminating null character, unless no text was copied.</span></span> <span data-ttu-id="ec635-125">Se non è stato copiato alcun testo, il messaggio inserisce un carattere null all'inizio del buffer.</span><span class="sxs-lookup"><span data-stu-id="ec635-125">If no text was copied, the message places a null character at the beginning of the buffer.</span></span> <span data-ttu-id="ec635-126">Per informazioni sulla compatibilità delle versioni Rich Edit con le varie versioni di sistema, vedere [informazioni sui controlli Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="ec635-126">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ec635-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ec635-127">Requirements</span></span>



| <span data-ttu-id="ec635-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec635-128">Requirement</span></span> | <span data-ttu-id="ec635-129">Valore</span><span class="sxs-lookup"><span data-stu-id="ec635-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec635-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ec635-130">Minimum supported client</span></span><br/> | <span data-ttu-id="ec635-131">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ec635-131">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ec635-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ec635-132">Minimum supported server</span></span><br/> | <span data-ttu-id="ec635-133">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ec635-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ec635-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ec635-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec635-135"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ec635-135"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec635-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ec635-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="ec635-137">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="ec635-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ec635-138">**\_LINELENGTH em**</span><span class="sxs-lookup"><span data-stu-id="ec635-138">**EM\_LINELENGTH**</span></span>](em-linelength.md)
</dt> <dt>

[<span data-ttu-id="ec635-139">**Modifica \_ getline**</span><span class="sxs-lookup"><span data-stu-id="ec635-139">**Edit\_GetLine**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_getline)
</dt> <dt>

<span data-ttu-id="ec635-140">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="ec635-140">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="ec635-141">**WM \_ GETtext**</span><span class="sxs-lookup"><span data-stu-id="ec635-141">**WM\_GETTEXT**</span></span>](/windows/desktop/winmsg/wm-gettext)
</dt> </dl>

 

