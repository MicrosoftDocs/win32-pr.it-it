---
title: EM_SETLIMITTEXT messaggio (Winuser.h)
description: 'EM_SETLIMITTEXT messaggio: imposta il limite di testo di un controllo di modifica.'
ms.assetid: e2be7814-435b-495f-982a-32247fbc0165
keywords:
- EM_SETLIMITTEXT di windows del messaggio
topic_type:
- apiref
api_name:
- EM_SETLIMITTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b66d4e03b5c1824ab501226482fcf51fb9121cba
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109749"
---
# <a name="em_setlimittext-message"></a><span data-ttu-id="9870f-104">Messaggio EM \_ SETLIMITTEXT</span><span class="sxs-lookup"><span data-stu-id="9870f-104">EM\_SETLIMITTEXT message</span></span>

<span data-ttu-id="9870f-105">Imposta il limite di testo di un controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="9870f-105">Sets the text limit of an edit control.</span></span> <span data-ttu-id="9870f-106">Il limite di testo è la quantità massima di testo, in **TCHAR** s, che l'utente può digitare nel controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="9870f-106">The text limit is the maximum amount of text, in **TCHAR** s, that the user can type into the edit control.</span></span> <span data-ttu-id="9870f-107">È possibile inviare questo messaggio a un controllo di modifica o a un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="9870f-107">You can send this message to either an edit control or a rich edit control.</span></span>

<span data-ttu-id="9870f-108">Per i controlli di modifica e Microsoft Rich Edit 1.0, vengono usati i byte.</span><span class="sxs-lookup"><span data-stu-id="9870f-108">For edit controls and Microsoft Rich Edit 1.0, bytes are used.</span></span> <span data-ttu-id="9870f-109">Per Microsoft Rich Edit 2.0 e versioni successive, vengono usati caratteri.</span><span class="sxs-lookup"><span data-stu-id="9870f-109">For Microsoft Rich Edit 2.0 and later, characters are used.</span></span>

<span data-ttu-id="9870f-110">Il **messaggio EM \_ SETLIMITTEXT** è identico al [**messaggio EM \_ LIMITTEXT.**](em-limittext.md)</span><span class="sxs-lookup"><span data-stu-id="9870f-110">The **EM\_SETLIMITTEXT** message is identical to the [**EM\_LIMITTEXT**](em-limittext.md) message.</span></span>

## <a name="parameters"></a><span data-ttu-id="9870f-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="9870f-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9870f-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9870f-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9870f-113">Numero massimo di **TCHAR che** l'utente può immettere.</span><span class="sxs-lookup"><span data-stu-id="9870f-113">The maximum number of **TCHAR** s the user can enter.</span></span> <span data-ttu-id="9870f-114">Per il testo ANSI, questo è il numero di byte. per il testo Unicode, questo è il numero di caratteri.</span><span class="sxs-lookup"><span data-stu-id="9870f-114">For ANSI text, this is the number of bytes; for Unicode text, this is the number of characters.</span></span> <span data-ttu-id="9870f-115">Questo numero non include il carattere Null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="9870f-115">This number does not include the terminating null character.</span></span>

<span data-ttu-id="9870f-116">**Controlli Rich Edit:** Se questo parametro è zero, la lunghezza del testo viene impostata su 64.000 caratteri.</span><span class="sxs-lookup"><span data-stu-id="9870f-116">**Rich edit controls:** If this parameter is zero, the text length is set to 64,000 characters.</span></span>

<span data-ttu-id="9870f-117">Se questo parametro è zero, la lunghezza del testo viene impostata su 0x7FFFFFFE caratteri per i controlli di modifica a riga singola o su 1 per i controlli di modifica su più righe.</span><span class="sxs-lookup"><span data-stu-id="9870f-117">If this parameter is zero, the text length is set to 0x7FFFFFFE characters for single-line edit controls or  1 for multiline edit controls.</span></span>

</dd> <dt>

<span data-ttu-id="9870f-118">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9870f-118">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9870f-119">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="9870f-119">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9870f-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9870f-120">Return value</span></span>

<span data-ttu-id="9870f-121">Questo messaggio non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="9870f-121">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9870f-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="9870f-122">Remarks</span></span>

<span data-ttu-id="9870f-123">Il **messaggio EM \_ SETLIMITTEXT** limita solo il testo che l'utente può immettere.</span><span class="sxs-lookup"><span data-stu-id="9870f-123">The **EM\_SETLIMITTEXT** message limits only the text the user can enter.</span></span> <span data-ttu-id="9870f-124">Non influisce sul testo già presente nel controllo di modifica quando viene inviato il messaggio, né sulla lunghezza del testo copiato nel controllo di modifica dal messaggio [**\_ WM SETTEXT.**](/windows/desktop/winmsg/wm-settext)</span><span class="sxs-lookup"><span data-stu-id="9870f-124">It does not affect any text already in the edit control when the message is sent, nor does it affect the length of the text copied to the edit control by the [**WM\_SETTEXT**](/windows/desktop/winmsg/wm-settext) message.</span></span> <span data-ttu-id="9870f-125">Se un'applicazione usa il messaggio **WM \_ SETTEXT** per inserire più testo in un controllo di modifica rispetto a quello specificato nel messaggio **EM \_ SETLIMITTEXT,** l'utente può modificare l'intero contenuto del controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="9870f-125">If an application uses the **WM\_SETTEXT** message to place more text into an edit control than is specified in the **EM\_SETLIMITTEXT** message, the user can edit the entire contents of the edit control.</span></span>

<span data-ttu-id="9870f-126">Prima della chiamata a **EM \_ SETLIMITTEXT,** il limite predefinito per la quantità di testo che un utente può immettere in un controllo di modifica è di 32.767 caratteri.</span><span class="sxs-lookup"><span data-stu-id="9870f-126">Before **EM\_SETLIMITTEXT** is called, the default limit for the amount of text a user can enter in an edit control is 32,767 characters.</span></span>

<span data-ttu-id="9870f-127">Per i controlli di modifica a riga singola, il limite di testo è 0x7FFFFFFE byte o il valore del *parametro wParam,* a seconda del valore minore.</span><span class="sxs-lookup"><span data-stu-id="9870f-127">For single-line edit controls, the text limit is either 0x7FFFFFFE bytes or the value of the *wParam* parameter, whichever is smaller.</span></span> <span data-ttu-id="9870f-128">Per i controlli di modifica su più righe, questo valore è pari a 1 byte o al valore del *parametro wParam,* a seconda del valore minore.</span><span class="sxs-lookup"><span data-stu-id="9870f-128">For multiline edit controls, this value is either  1 bytes or the value of the *wParam* parameter, whichever is smaller.</span></span>

<span data-ttu-id="9870f-129">**Rich Edit:** Supportato in Microsoft Rich Edit 1.0 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="9870f-129">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="9870f-130">Usare il messaggio [**EM \_ EXLIMITTEXT per**](em-exlimittext.md) i valori di lunghezza del testo maggiori di 64.000.</span><span class="sxs-lookup"><span data-stu-id="9870f-130">Use the message [**EM\_EXLIMITTEXT**](em-exlimittext.md) for text length values greater than 64,000.</span></span> <span data-ttu-id="9870f-131">Per informazioni sulla compatibilità delle versioni rich edit con le varie versioni di sistema, vedere [Informazioni sui controlli Rich Edit.](about-rich-edit-controls.md)</span><span class="sxs-lookup"><span data-stu-id="9870f-131">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9870f-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9870f-132">Requirements</span></span>



| <span data-ttu-id="9870f-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="9870f-133">Requirement</span></span> | <span data-ttu-id="9870f-134">Valore</span><span class="sxs-lookup"><span data-stu-id="9870f-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9870f-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9870f-135">Minimum supported client</span></span><br/> | <span data-ttu-id="9870f-136">Solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="9870f-136">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="9870f-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9870f-137">Minimum supported server</span></span><br/> | <span data-ttu-id="9870f-138">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="9870f-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9870f-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9870f-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="9870f-140"><dt>Winuser.h (includere Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="9870f-140"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9870f-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9870f-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9870f-142">**EM \_ GETLIMITTEXT**</span><span class="sxs-lookup"><span data-stu-id="9870f-142">**EM\_GETLIMITTEXT**</span></span>](em-getlimittext.md)
</dt> </dl>

 

