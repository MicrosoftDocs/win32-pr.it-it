---
description: Copia il testo che corrisponde a una finestra in un buffer fornito dal chiamante.
ms.assetid: 117c3d6d-24cd-462f-bdb0-b65d8914273a
title: Messaggio WM_GETTEXT (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47f8e2268c1d0ec043e24a001f16abae357bdbdc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757823"
---
# <a name="wm_gettext-message"></a><span data-ttu-id="29426-103">\_Messaggio WM GETtext</span><span class="sxs-lookup"><span data-stu-id="29426-103">WM\_GETTEXT message</span></span>

<span data-ttu-id="29426-104">Copia il testo che corrisponde a una finestra in un buffer fornito dal chiamante.</span><span class="sxs-lookup"><span data-stu-id="29426-104">Copies the text that corresponds to a window into a buffer provided by the caller.</span></span>


```C++
#define WM_GETTEXT                      0x000D
```



## <a name="parameters"></a><span data-ttu-id="29426-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="29426-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29426-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="29426-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="29426-107">Numero massimo di caratteri da copiare, incluso il carattere null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="29426-107">The maximum number of characters to be copied, including the terminating null character.</span></span>

<span data-ttu-id="29426-108">Le applicazioni ANSI possono avere una dimensione del buffer ridotta (almeno metà del valore *wParam* ) a causa della conversione da ANSI a Unicode.</span><span class="sxs-lookup"><span data-stu-id="29426-108">ANSI applications may have the string in the buffer reduced in size (to a minimum of half that of the *wParam* value) due to conversion from ANSI to Unicode.</span></span>

</dd> <dt>

<span data-ttu-id="29426-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="29426-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="29426-110">Puntatore al buffer che deve ricevere il testo.</span><span class="sxs-lookup"><span data-stu-id="29426-110">A pointer to the buffer that is to receive the text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29426-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="29426-111">Return value</span></span>

<span data-ttu-id="29426-112">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="29426-112">Type: **LRESULT**</span></span>

<span data-ttu-id="29426-113">Il valore restituito è il numero di caratteri copiati, escluso il carattere null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="29426-113">The return value is the number of characters copied, not including the terminating null character.</span></span>

## <a name="remarks"></a><span data-ttu-id="29426-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="29426-114">Remarks</span></span>

<span data-ttu-id="29426-115">La funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) copia il testo associato alla finestra nel buffer specificato e restituisce il numero di caratteri copiati.</span><span class="sxs-lookup"><span data-stu-id="29426-115">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function copies the text associated with the window into the specified buffer and returns the number of characters copied.</span></span> <span data-ttu-id="29426-116">Si noti che, per i controlli statici non di testo, questo fornisce il testo con cui è stato originariamente creato il controllo, ovvero il numero ID.</span><span class="sxs-lookup"><span data-stu-id="29426-116">Note, for non-text static controls this gives you the text with which the control was originally created, that is, the ID number.</span></span> <span data-ttu-id="29426-117">Tuttavia, fornisce l'ID del controllo statico non di testo creato in origine.</span><span class="sxs-lookup"><span data-stu-id="29426-117">However, it gives you the ID of the non-text static control as originally created.</span></span> <span data-ttu-id="29426-118">Ovvero, se in seguito si utilizza un' **\_ Immagine STM** per modificarla, verrà comunque restituito l'ID originale.</span><span class="sxs-lookup"><span data-stu-id="29426-118">That is, if you subsequently used a **STM\_SETIMAGE** to change it the original ID would still be returned.</span></span>

<span data-ttu-id="29426-119">Per un controllo di modifica, il testo da copiare è il contenuto del controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="29426-119">For an edit control, the text to be copied is the content of the edit control.</span></span> <span data-ttu-id="29426-120">Per una casella combinata, il testo è il contenuto della parte del controllo di modifica (o del testo statico) della casella combinata.</span><span class="sxs-lookup"><span data-stu-id="29426-120">For a combo box, the text is the content of the edit control (or static-text) portion of the combo box.</span></span> <span data-ttu-id="29426-121">Per un pulsante, il testo è il nome del pulsante.</span><span class="sxs-lookup"><span data-stu-id="29426-121">For a button, the text is the button name.</span></span> <span data-ttu-id="29426-122">Per le altre finestre, il testo è il titolo della finestra.</span><span class="sxs-lookup"><span data-stu-id="29426-122">For other windows, the text is the window title.</span></span> <span data-ttu-id="29426-123">Per copiare il testo di un elemento in una casella di riepilogo, un'applicazione può usare il messaggio [**lb \_ gettext**](../controls/lb-gettext.md) .</span><span class="sxs-lookup"><span data-stu-id="29426-123">To copy the text of an item in a list box, an application can use the [**LB\_GETTEXT**](../controls/lb-gettext.md) message.</span></span>

<span data-ttu-id="29426-124">Quando il messaggio **WM \_ gettext** viene inviato a un controllo statico con lo stile dell' **\_ icona SS** , viene restituito un handle per l'icona nei primi quattro byte del buffer a cui punta *lParam*.</span><span class="sxs-lookup"><span data-stu-id="29426-124">When the **WM\_GETTEXT** message is sent to a static control with the **SS\_ICON** style, a handle to the icon will be returned in the first four bytes of the buffer pointed to by *lParam*.</span></span> <span data-ttu-id="29426-125">Questo vale solo se è stato usato il messaggio [**WM \_ SetText**](wm-settext.md) per impostare l'icona.</span><span class="sxs-lookup"><span data-stu-id="29426-125">This is true only if the [**WM\_SETTEXT**](wm-settext.md) message has been used to set the icon.</span></span>

<span data-ttu-id="29426-126">**Modifica avanzata:** Se il testo da copiare supera 64K, usare il messaggio em [**\_ Stream**](../controls/em-streamout.md) out o [**em \_ GETSELTEXT**](../controls/em-getseltext.md) .</span><span class="sxs-lookup"><span data-stu-id="29426-126">**Rich Edit:** If the text to be copied exceeds 64K, use either the [**EM\_STREAMOUT**](../controls/em-streamout.md) or [**EM\_GETSELTEXT**](../controls/em-getseltext.md) message.</span></span>

<span data-ttu-id="29426-127">L'invio di un messaggio **WM \_ gettext** a un controllo statico non di testo, ad esempio una bitmap statica o un controllo icona statica, non restituisce un valore stringa.</span><span class="sxs-lookup"><span data-stu-id="29426-127">Sending a **WM\_GETTEXT** message to a non-text static control, such as a static bitmap or static icon control, does not return a string value.</span></span> <span data-ttu-id="29426-128">Viene invece restituito zero.</span><span class="sxs-lookup"><span data-stu-id="29426-128">Instead, it returns zero.</span></span> <span data-ttu-id="29426-129">Inoltre, nelle prime versioni di Windows, le applicazioni potevano inviare un messaggio **WM \_ gettext** a un controllo statico non di testo per recuperare l'ID del controllo.</span><span class="sxs-lookup"><span data-stu-id="29426-129">In addition, in early versions of Windows, applications could send a **WM\_GETTEXT** message to a non-text static control to retrieve the control's ID.</span></span> <span data-ttu-id="29426-130">Per recuperare l'ID di un controllo, le applicazioni possono usare [**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga) passando l' **\_ ID GWL** come valore di indice o [**GetWindowLongPtr**](/windows/win32/api/winuser/nf-winuser-getwindowlongptra) usando l' **\_ ID GWLP**.</span><span class="sxs-lookup"><span data-stu-id="29426-130">To retrieve a control's ID, applications can use [**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga) passing **GWL\_ID** as the index value or [**GetWindowLongPtr**](/windows/win32/api/winuser/nf-winuser-getwindowlongptra) using **GWLP\_ID**.</span></span>

## <a name="requirements"></a><span data-ttu-id="29426-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="29426-131">Requirements</span></span>



| <span data-ttu-id="29426-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="29426-132">Requirement</span></span> | <span data-ttu-id="29426-133">Valore</span><span class="sxs-lookup"><span data-stu-id="29426-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29426-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="29426-134">Minimum supported client</span></span><br/> | <span data-ttu-id="29426-135">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="29426-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="29426-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="29426-136">Minimum supported server</span></span><br/> | <span data-ttu-id="29426-137">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="29426-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="29426-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="29426-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="29426-139"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="29426-139"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29426-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="29426-140">See also</span></span>

<dl> <dt>

<span data-ttu-id="29426-141">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="29426-141">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="29426-142">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="29426-142">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="29426-143">**GetWindowLong**</span><span class="sxs-lookup"><span data-stu-id="29426-143">**GetWindowLong**</span></span>](/windows/win32/api/winuser/nf-winuser-getwindowlonga)
</dt> <dt>

[<span data-ttu-id="29426-144">**GetWindowLongPtr**</span><span class="sxs-lookup"><span data-stu-id="29426-144">**GetWindowLongPtr**</span></span>](/windows/win32/api/winuser/nf-winuser-getwindowlongptra)
</dt> <dt>

[<span data-ttu-id="29426-145">**GetWindowText**</span><span class="sxs-lookup"><span data-stu-id="29426-145">**GetWindowText**</span></span>](/windows/win32/api/winuser/nf-winuser-getwindowtexta)
</dt> <dt>

[<span data-ttu-id="29426-146">**GetWindowTextLength**</span><span class="sxs-lookup"><span data-stu-id="29426-146">**GetWindowTextLength**</span></span>](/windows/win32/api/winuser/nf-winuser-getwindowtextlengtha)
</dt> <dt>

[<span data-ttu-id="29426-147">**\_GETTEXTLENGTH WM**</span><span class="sxs-lookup"><span data-stu-id="29426-147">**WM\_GETTEXTLENGTH**</span></span>](wm-gettextlength.md)
</dt> <dt>

[<span data-ttu-id="29426-148">**\_testo WM**</span><span class="sxs-lookup"><span data-stu-id="29426-148">**WM\_SETTEXT**</span></span>](wm-settext.md)
</dt> <dt>

<span data-ttu-id="29426-149">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="29426-149">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="29426-150">Windows</span><span class="sxs-lookup"><span data-stu-id="29426-150">Windows</span></span>](windows.md)
</dt> <dt>

<span data-ttu-id="29426-151">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="29426-151">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="29426-152">**\_GETSELTEXT em**</span><span class="sxs-lookup"><span data-stu-id="29426-152">**EM\_GETSELTEXT**</span></span>](../controls/em-getseltext.md)
</dt> <dt>

[<span data-ttu-id="29426-153">**\_flusso em**</span><span class="sxs-lookup"><span data-stu-id="29426-153">**EM\_STREAMOUT**</span></span>](../controls/em-streamout.md)
</dt> <dt>

[<span data-ttu-id="29426-154">**GetText LB \_**</span><span class="sxs-lookup"><span data-stu-id="29426-154">**LB\_GETTEXT**</span></span>](../controls/lb-gettext.md)
</dt> </dl>

 

 
