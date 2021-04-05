---
title: Messaggio EM_SETLIMITTEXT (winuser. h)
description: Imposta il limite di testo di un controllo di modifica.
ms.assetid: e2be7814-435b-495f-982a-32247fbc0165
keywords:
- Controlli di Windows Message EM_SETLIMITTEXT
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
ms.openlocfilehash: 5c138e6d7fed75fa8da2e7a6b93308632c250e7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742007"
---
# <a name="em_setlimittext-message"></a><span data-ttu-id="fcfdc-104">\_Messaggio SETLIMITTEXT em</span><span class="sxs-lookup"><span data-stu-id="fcfdc-104">EM\_SETLIMITTEXT message</span></span>

<span data-ttu-id="fcfdc-105">Imposta il limite di testo di un controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="fcfdc-105">Sets the text limit of an edit control.</span></span> <span data-ttu-id="fcfdc-106">Il limite di testo è la quantità massima di testo, in **TCHAR** s, che l'utente può digitare nel controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="fcfdc-106">The text limit is the maximum amount of text, in **TCHAR** s, that the user can type into the edit control.</span></span> <span data-ttu-id="fcfdc-107">Questo messaggio può essere inviato a un controllo di modifica o a un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="fcfdc-107">You can send this message to either an edit control or a rich edit control.</span></span>

<span data-ttu-id="fcfdc-108">Per i controlli di modifica e Microsoft Rich Edit 1,0, vengono usati i byte.</span><span class="sxs-lookup"><span data-stu-id="fcfdc-108">For edit controls and Microsoft Rich Edit 1.0, bytes are used.</span></span> <span data-ttu-id="fcfdc-109">Per Microsoft Rich Edit 2,0 e versioni successive, vengono utilizzati i caratteri.</span><span class="sxs-lookup"><span data-stu-id="fcfdc-109">For Microsoft Rich Edit 2.0 and later, characters are used.</span></span>

<span data-ttu-id="fcfdc-110">Il **messaggio \_ SETLIMITTEXT em** è identico al [**messaggio \_ LIMITTEXT em**](em-limittext.md) .</span><span class="sxs-lookup"><span data-stu-id="fcfdc-110">The **EM\_SETLIMITTEXT** message is identical to the [**EM\_LIMITTEXT**](em-limittext.md) message.</span></span>

## <a name="parameters"></a><span data-ttu-id="fcfdc-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="fcfdc-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fcfdc-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fcfdc-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fcfdc-113">Il numero massimo di **TCHAR** che l'utente può immettere.</span><span class="sxs-lookup"><span data-stu-id="fcfdc-113">The maximum number of **TCHAR** s the user can enter.</span></span> <span data-ttu-id="fcfdc-114">Per testo ANSI, indica il numero di byte; per il testo Unicode, indica il numero di caratteri.</span><span class="sxs-lookup"><span data-stu-id="fcfdc-114">For ANSI text, this is the number of bytes; for Unicode text, this is the number of characters.</span></span> <span data-ttu-id="fcfdc-115">Questo numero non include il carattere null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="fcfdc-115">This number does not include the terminating null character.</span></span>

<span data-ttu-id="fcfdc-116">**Controlli Rich Edit:** Se questo parametro è zero, la lunghezza del testo viene impostata su 64.000 caratteri.</span><span class="sxs-lookup"><span data-stu-id="fcfdc-116">**Rich edit controls:** If this parameter is zero, the text length is set to 64,000 characters.</span></span>

<span data-ttu-id="fcfdc-117">Se questo parametro è zero, la lunghezza del testo viene impostata su 0x7FFFFFFE caratteri per i controlli di modifica a riga singola o 1 per i controlli di modifica su più righe.</span><span class="sxs-lookup"><span data-stu-id="fcfdc-117">If this parameter is zero, the text length is set to 0x7FFFFFFE characters for single-line edit controls or  1 for multiline edit controls.</span></span>

</dd> <dt>

<span data-ttu-id="fcfdc-118">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fcfdc-118">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fcfdc-119">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="fcfdc-119">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fcfdc-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fcfdc-120">Return value</span></span>

<span data-ttu-id="fcfdc-121">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="fcfdc-121">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fcfdc-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="fcfdc-122">Remarks</span></span>

<span data-ttu-id="fcfdc-123">Il **messaggio \_ SETLIMITTEXT em** limita solo il testo che l'utente può immettere.</span><span class="sxs-lookup"><span data-stu-id="fcfdc-123">The **EM\_SETLIMITTEXT** message limits only the text the user can enter.</span></span> <span data-ttu-id="fcfdc-124">Non influisce sul testo già presente nel controllo di modifica quando il messaggio viene inviato, né sulla lunghezza del testo copiato nel controllo di modifica da parte del messaggio [**WM \_**](/windows/desktop/winmsg/wm-settext) .</span><span class="sxs-lookup"><span data-stu-id="fcfdc-124">It does not affect any text already in the edit control when the message is sent, nor does it affect the length of the text copied to the edit control by the [**WM\_SETTEXT**](/windows/desktop/winmsg/wm-settext) message.</span></span> <span data-ttu-id="fcfdc-125">Se un'applicazione usa il messaggio di **\_ testo WM** per inserire più testo in un controllo di modifica rispetto a quanto specificato nel messaggio **\_ SETLIMITTEXT em** , l'utente può modificare l'intero contenuto del controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="fcfdc-125">If an application uses the **WM\_SETTEXT** message to place more text into an edit control than is specified in the **EM\_SETLIMITTEXT** message, the user can edit the entire contents of the edit control.</span></span>

<span data-ttu-id="fcfdc-126">Prima di chiamare **em \_ SETLIMITTEXT** , il limite predefinito per la quantità di testo che un utente può immettere in un controllo di modifica è di 32.767 caratteri.</span><span class="sxs-lookup"><span data-stu-id="fcfdc-126">Before **EM\_SETLIMITTEXT** is called, the default limit for the amount of text a user can enter in an edit control is 32,767 characters.</span></span>

<span data-ttu-id="fcfdc-127">Per i controlli di modifica a riga singola, il limite di testo è 0x7FFFFFFE byte o il valore del parametro *wParam* , a seconda del valore minore.</span><span class="sxs-lookup"><span data-stu-id="fcfdc-127">For single-line edit controls, the text limit is either 0x7FFFFFFE bytes or the value of the *wParam* parameter, whichever is smaller.</span></span> <span data-ttu-id="fcfdc-128">Per i controlli di modifica su più righe, questo valore è pari a 1 byte o al valore del parametro *wParam* , a seconda del valore minore.</span><span class="sxs-lookup"><span data-stu-id="fcfdc-128">For multiline edit controls, this value is either  1 bytes or the value of the *wParam* parameter, whichever is smaller.</span></span>

<span data-ttu-id="fcfdc-129">**Modifica avanzata:** Supportato in Microsoft Rich Edit 1,0 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="fcfdc-129">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="fcfdc-130">Usare il messaggio [**em \_ EXLIMITTEXT**](em-exlimittext.md) per i valori di lunghezza del testo maggiori di 64.000.</span><span class="sxs-lookup"><span data-stu-id="fcfdc-130">Use the message [**EM\_EXLIMITTEXT**](em-exlimittext.md) for text length values greater than 64,000.</span></span> <span data-ttu-id="fcfdc-131">Per informazioni sulla compatibilità delle versioni Rich Edit con le varie versioni di sistema, vedere [informazioni sui controlli Rich Edit](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="fcfdc-131">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fcfdc-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fcfdc-132">Requirements</span></span>



| <span data-ttu-id="fcfdc-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="fcfdc-133">Requirement</span></span> | <span data-ttu-id="fcfdc-134">Valore</span><span class="sxs-lookup"><span data-stu-id="fcfdc-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fcfdc-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fcfdc-135">Minimum supported client</span></span><br/> | <span data-ttu-id="fcfdc-136">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fcfdc-136">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="fcfdc-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fcfdc-137">Minimum supported server</span></span><br/> | <span data-ttu-id="fcfdc-138">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fcfdc-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fcfdc-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fcfdc-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="fcfdc-140"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fcfdc-140"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fcfdc-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fcfdc-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcfdc-142">**\_GETLIMITTEXT em**</span><span class="sxs-lookup"><span data-stu-id="fcfdc-142">**EM\_GETLIMITTEXT**</span></span>](em-getlimittext.md)
</dt> </dl>

 

