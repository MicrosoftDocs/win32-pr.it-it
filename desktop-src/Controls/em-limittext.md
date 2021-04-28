---
title: EM_LIMITTEXT messaggio (Winuser.h)
description: 'EM_LIMITTEXT messaggio: imposta il limite di testo di un controllo di modifica.'
ms.assetid: 5a605de7-8dc7-4c54-8f18-e0b08c720856
keywords:
- EM_LIMITTEXT messaggio Controlli Windows
topic_type:
- apiref
api_name:
- EM_LIMITTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a80ce29d4ee5155f6b3c5c32609366982655a078
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109789"
---
# <a name="em_limittext-message"></a><span data-ttu-id="c40ac-104">Messaggio EM \_ LIMITTEXT</span><span class="sxs-lookup"><span data-stu-id="c40ac-104">EM\_LIMITTEXT message</span></span>

<span data-ttu-id="c40ac-105">Imposta il limite di testo di un controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="c40ac-105">Sets the text limit of an edit control.</span></span> <span data-ttu-id="c40ac-106">Il limite di testo è la quantità massima di testo, in **TCHAR,** che l'utente può digitare nel controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="c40ac-106">The text limit is the maximum amount of text, in **TCHAR** s, that the user can type into the edit control.</span></span> <span data-ttu-id="c40ac-107">È possibile inviare questo messaggio a un controllo di modifica o a un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="c40ac-107">You can send this message to either an edit control or a rich edit control.</span></span>

<span data-ttu-id="c40ac-108">Per i controlli di modifica e Microsoft Rich Edit 1.0, vengono usati i byte.</span><span class="sxs-lookup"><span data-stu-id="c40ac-108">For edit controls and Microsoft Rich Edit 1.0, bytes are used.</span></span> <span data-ttu-id="c40ac-109">Per Microsoft Rich Edit 2.0 e versioni successive vengono usati i caratteri.</span><span class="sxs-lookup"><span data-stu-id="c40ac-109">For Microsoft Rich Edit 2.0 and later, characters are used.</span></span>

## <a name="parameters"></a><span data-ttu-id="c40ac-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="c40ac-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c40ac-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c40ac-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c40ac-112">Numero massimo di **TCHAR che l'utente** può immettere.</span><span class="sxs-lookup"><span data-stu-id="c40ac-112">The maximum number of **TCHAR** s the user can enter.</span></span> <span data-ttu-id="c40ac-113">Per il testo ANSI, questo è il numero di byte. per il testo Unicode, questo è il numero di caratteri.</span><span class="sxs-lookup"><span data-stu-id="c40ac-113">For ANSI text, this is the number of bytes; for Unicode text, this is the number of characters.</span></span> <span data-ttu-id="c40ac-114">Questo numero non include il carattere Null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="c40ac-114">This number does not include the terminating null character.</span></span>

<span data-ttu-id="c40ac-115">**Controlli Rich Edit:** Se questo parametro è zero, la lunghezza del testo è impostata su 64.000 caratteri.</span><span class="sxs-lookup"><span data-stu-id="c40ac-115">**Rich edit controls:** If this parameter is zero, the text length is set to 64,000 characters.</span></span>

<span data-ttu-id="c40ac-116">Se questo parametro è zero, la lunghezza del testo viene impostata 0x7FFFFFFE caratteri per i controlli di modifica a riga singola o -1 per i controlli di modifica su più righe.</span><span class="sxs-lookup"><span data-stu-id="c40ac-116">If this parameter is zero, the text length is set to 0x7FFFFFFE characters for single-line edit controls or -1 for multiline edit controls.</span></span>

</dd> <dt>

<span data-ttu-id="c40ac-117">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c40ac-117">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c40ac-118">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="c40ac-118">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c40ac-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c40ac-119">Return value</span></span>

<span data-ttu-id="c40ac-120">Questo messaggio non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="c40ac-120">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c40ac-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="c40ac-121">Remarks</span></span>

<span data-ttu-id="c40ac-122">Il **messaggio EM \_ LIMITTEXT** limita solo il testo che l'utente può immettere.</span><span class="sxs-lookup"><span data-stu-id="c40ac-122">The **EM\_LIMITTEXT** message limits only the text the user can enter.</span></span> <span data-ttu-id="c40ac-123">Non influisce sul testo già presente nel controllo di modifica quando viene inviato il messaggio, né sulla lunghezza del testo copiato nel controllo di modifica dal [**messaggio WM \_ SETTEXT.**](/windows/desktop/winmsg/wm-settext)</span><span class="sxs-lookup"><span data-stu-id="c40ac-123">It does not affect any text already in the edit control when the message is sent, nor does it affect the length of the text copied to the edit control by the [**WM\_SETTEXT**](/windows/desktop/winmsg/wm-settext) message.</span></span> <span data-ttu-id="c40ac-124">Se un'applicazione usa il messaggio **WM \_ SETTEXT** per inserire più testo in un controllo di modifica di quello specificato nel messaggio **EM \_ LIMITTEXT,** l'utente può modificare l'intero contenuto del controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="c40ac-124">If an application uses the **WM\_SETTEXT** message to place more text into an edit control than is specified in the **EM\_LIMITTEXT** message, the user can edit the entire contents of the edit control.</span></span>

<span data-ttu-id="c40ac-125">Prima **della chiamata a EM \_ LIMITTEXT,** il limite predefinito per la quantità di testo che un utente può immettere in un controllo di modifica è di 32.767 caratteri.</span><span class="sxs-lookup"><span data-stu-id="c40ac-125">Before **EM\_LIMITTEXT** is called, the default limit for the amount of text a user can enter in an edit control is 32,767 characters.</span></span>

<span data-ttu-id="c40ac-126">Per i controlli di modifica a riga singola, il limite di testo è 0x7FFFFFFE byte o il valore del *parametro wParam,* a seconda del valore più piccolo.</span><span class="sxs-lookup"><span data-stu-id="c40ac-126">For single-line edit controls, the text limit is either 0x7FFFFFFE bytes or the value of the *wParam* parameter, whichever is smaller.</span></span> <span data-ttu-id="c40ac-127">Per i controlli di modifica su più righe, questo valore è -1 byte o il valore del *parametro wParam,* a seconda del valore minore.</span><span class="sxs-lookup"><span data-stu-id="c40ac-127">For multiline edit controls, this value is either -1 byte or the value of the *wParam* parameter, whichever is smaller.</span></span>

<span data-ttu-id="c40ac-128">**Rich Edit:** Supportato in Microsoft Rich Edit 1.0 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="c40ac-128">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="c40ac-129">Usare il messaggio [**EM \_ EXLIMITTEXT per**](em-exlimittext.md) i valori di lunghezza del testo maggiori di 64.000.</span><span class="sxs-lookup"><span data-stu-id="c40ac-129">Use the message [**EM\_EXLIMITTEXT**](em-exlimittext.md) for text length values greater than 64,000.</span></span> <span data-ttu-id="c40ac-130">Per informazioni sulla compatibilità delle versioni rich edit con le varie versioni di sistema, vedere [Informazioni sui controlli Rich Edit.](about-rich-edit-controls.md)</span><span class="sxs-lookup"><span data-stu-id="c40ac-130">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c40ac-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c40ac-131">Requirements</span></span>



| <span data-ttu-id="c40ac-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="c40ac-132">Requirement</span></span> | <span data-ttu-id="c40ac-133">Valore</span><span class="sxs-lookup"><span data-stu-id="c40ac-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c40ac-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c40ac-134">Minimum supported client</span></span><br/> | <span data-ttu-id="c40ac-135">Solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c40ac-135">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c40ac-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c40ac-136">Minimum supported server</span></span><br/> | <span data-ttu-id="c40ac-137">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="c40ac-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c40ac-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c40ac-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="c40ac-139"><dt>Winuser.h (includere Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="c40ac-139"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c40ac-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c40ac-140">See also</span></span>

<dl> <dt>

<span data-ttu-id="c40ac-141">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="c40ac-141">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c40ac-142">**EM \_ EXLIMITTEXT**</span><span class="sxs-lookup"><span data-stu-id="c40ac-142">**EM\_EXLIMITTEXT**</span></span>](em-exlimittext.md)
</dt> <dt>

[<span data-ttu-id="c40ac-143">**Modifica \_ limitText**</span><span class="sxs-lookup"><span data-stu-id="c40ac-143">**Edit\_LimitText**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_limittext)
</dt> <dt>

<span data-ttu-id="c40ac-144">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="c40ac-144">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="c40ac-145">**WM \_ SETTEXT**</span><span class="sxs-lookup"><span data-stu-id="c40ac-145">**WM\_SETTEXT**</span></span>](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 

