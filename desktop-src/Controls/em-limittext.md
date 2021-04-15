---
title: Messaggio EM_LIMITTEXT (winuser. h)
description: Imposta il limite di testo di un controllo di modifica.
ms.assetid: 5a605de7-8dc7-4c54-8f18-e0b08c720856
keywords:
- Controlli di Windows Message EM_LIMITTEXT
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
ms.openlocfilehash: bf45f7ee9cfd88a25b78f0bd58911e516c146096
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476108"
---
# <a name="em_limittext-message"></a><span data-ttu-id="cfbc3-104">\_Messaggio LIMITTEXT em</span><span class="sxs-lookup"><span data-stu-id="cfbc3-104">EM\_LIMITTEXT message</span></span>

<span data-ttu-id="cfbc3-105">Imposta il limite di testo di un controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="cfbc3-105">Sets the text limit of an edit control.</span></span> <span data-ttu-id="cfbc3-106">Il limite di testo è la quantità massima di testo, in **TCHAR** s, che l'utente può digitare nel controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="cfbc3-106">The text limit is the maximum amount of text, in **TCHAR** s, that the user can type into the edit control.</span></span> <span data-ttu-id="cfbc3-107">Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="cfbc3-107">You can send this message to either an edit control or a rich edit control.</span></span>

<span data-ttu-id="cfbc3-108">Per i controlli di modifica e Microsoft Rich Edit 1,0, vengono usati i byte.</span><span class="sxs-lookup"><span data-stu-id="cfbc3-108">For edit controls and Microsoft Rich Edit 1.0, bytes are used.</span></span> <span data-ttu-id="cfbc3-109">Per Microsoft Rich Edit 2,0 e versioni successive, vengono utilizzati i caratteri.</span><span class="sxs-lookup"><span data-stu-id="cfbc3-109">For Microsoft Rich Edit 2.0 and later, characters are used.</span></span>

## <a name="parameters"></a><span data-ttu-id="cfbc3-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="cfbc3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfbc3-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cfbc3-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cfbc3-112">Il numero massimo di **TCHAR** che l'utente può immettere.</span><span class="sxs-lookup"><span data-stu-id="cfbc3-112">The maximum number of **TCHAR** s the user can enter.</span></span> <span data-ttu-id="cfbc3-113">Per testo ANSI, indica il numero di byte; per il testo Unicode, indica il numero di caratteri.</span><span class="sxs-lookup"><span data-stu-id="cfbc3-113">For ANSI text, this is the number of bytes; for Unicode text, this is the number of characters.</span></span> <span data-ttu-id="cfbc3-114">Questo numero non include il carattere null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="cfbc3-114">This number does not include the terminating null character.</span></span>

<span data-ttu-id="cfbc3-115">**Controlli Rich Edit:** Se questo parametro è zero, la lunghezza del testo viene impostata su 64.000 caratteri.</span><span class="sxs-lookup"><span data-stu-id="cfbc3-115">**Rich edit controls:** If this parameter is zero, the text length is set to 64,000 characters.</span></span>

<span data-ttu-id="cfbc3-116">Se questo parametro è zero, la lunghezza del testo viene impostata su 0x7FFFFFFE caratteri per i controlli di modifica a riga singola o-1 per i controlli di modifica su più righe.</span><span class="sxs-lookup"><span data-stu-id="cfbc3-116">If this parameter is zero, the text length is set to 0x7FFFFFFE characters for single-line edit controls or -1 for multiline edit controls.</span></span>

</dd> <dt>

<span data-ttu-id="cfbc3-117">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cfbc3-117">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cfbc3-118">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="cfbc3-118">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfbc3-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cfbc3-119">Return value</span></span>

<span data-ttu-id="cfbc3-120">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="cfbc3-120">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cfbc3-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="cfbc3-121">Remarks</span></span>

<span data-ttu-id="cfbc3-122">Il **messaggio \_ LIMITTEXT em** limita solo il testo che l'utente può immettere.</span><span class="sxs-lookup"><span data-stu-id="cfbc3-122">The **EM\_LIMITTEXT** message limits only the text the user can enter.</span></span> <span data-ttu-id="cfbc3-123">Non influisce sul testo già presente nel controllo di modifica quando il messaggio viene inviato, né sulla lunghezza del testo copiato nel controllo di modifica da parte del messaggio [**WM \_**](/windows/desktop/winmsg/wm-settext) .</span><span class="sxs-lookup"><span data-stu-id="cfbc3-123">It does not affect any text already in the edit control when the message is sent, nor does it affect the length of the text copied to the edit control by the [**WM\_SETTEXT**](/windows/desktop/winmsg/wm-settext) message.</span></span> <span data-ttu-id="cfbc3-124">Se un'applicazione usa il messaggio di **\_ testo WM** per inserire più testo in un controllo di modifica rispetto a quanto specificato nel messaggio **\_ LIMITTEXT em** , l'utente può modificare l'intero contenuto del controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="cfbc3-124">If an application uses the **WM\_SETTEXT** message to place more text into an edit control than is specified in the **EM\_LIMITTEXT** message, the user can edit the entire contents of the edit control.</span></span>

<span data-ttu-id="cfbc3-125">Prima di chiamare **em \_ LIMITTEXT** , il limite predefinito per la quantità di testo che un utente può immettere in un controllo di modifica è di 32.767 caratteri.</span><span class="sxs-lookup"><span data-stu-id="cfbc3-125">Before **EM\_LIMITTEXT** is called, the default limit for the amount of text a user can enter in an edit control is 32,767 characters.</span></span>

<span data-ttu-id="cfbc3-126">Per i controlli di modifica a riga singola, il limite di testo è 0x7FFFFFFE byte o il valore del parametro *wParam* , a seconda del valore minore.</span><span class="sxs-lookup"><span data-stu-id="cfbc3-126">For single-line edit controls, the text limit is either 0x7FFFFFFE bytes or the value of the *wParam* parameter, whichever is smaller.</span></span> <span data-ttu-id="cfbc3-127">Per i controlli di modifica su più righe, questo valore è-1 byte oppure il valore del parametro *wParam* , a seconda del valore minore.</span><span class="sxs-lookup"><span data-stu-id="cfbc3-127">For multiline edit controls, this value is either -1 byte or the value of the *wParam* parameter, whichever is smaller.</span></span>

<span data-ttu-id="cfbc3-128">**Modifica avanzata:** Supportato in Microsoft Rich Edit 1,0 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="cfbc3-128">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="cfbc3-129">Usare il messaggio [**em \_ EXLIMITTEXT**](em-exlimittext.md) per i valori di lunghezza del testo maggiori di 64.000.</span><span class="sxs-lookup"><span data-stu-id="cfbc3-129">Use the message [**EM\_EXLIMITTEXT**](em-exlimittext.md) for text length values greater than 64,000.</span></span> <span data-ttu-id="cfbc3-130">Per informazioni sulla compatibilità delle versioni Rich Edit con le varie versioni di sistema, vedere [informazioni sui controlli Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="cfbc3-130">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cfbc3-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cfbc3-131">Requirements</span></span>



| <span data-ttu-id="cfbc3-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="cfbc3-132">Requirement</span></span> | <span data-ttu-id="cfbc3-133">Valore</span><span class="sxs-lookup"><span data-stu-id="cfbc3-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cfbc3-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cfbc3-134">Minimum supported client</span></span><br/> | <span data-ttu-id="cfbc3-135">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cfbc3-135">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="cfbc3-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cfbc3-136">Minimum supported server</span></span><br/> | <span data-ttu-id="cfbc3-137">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cfbc3-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="cfbc3-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cfbc3-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="cfbc3-139"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cfbc3-139"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfbc3-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cfbc3-140">See also</span></span>

<dl> <dt>

<span data-ttu-id="cfbc3-141">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="cfbc3-141">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="cfbc3-142">**\_EXLIMITTEXT em**</span><span class="sxs-lookup"><span data-stu-id="cfbc3-142">**EM\_EXLIMITTEXT**</span></span>](em-exlimittext.md)
</dt> <dt>

[<span data-ttu-id="cfbc3-143">**Modifica \_ LimitText**</span><span class="sxs-lookup"><span data-stu-id="cfbc3-143">**Edit\_LimitText**</span></span>](/windows/desktop/api/Windowsx/nf-windowsx-edit_limittext)
</dt> <dt>

<span data-ttu-id="cfbc3-144">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="cfbc3-144">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="cfbc3-145">**\_testo WM**</span><span class="sxs-lookup"><span data-stu-id="cfbc3-145">**WM\_SETTEXT**</span></span>](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 

