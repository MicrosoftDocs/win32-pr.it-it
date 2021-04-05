---
description: Determina la lunghezza, in caratteri, del testo associato a una finestra.
ms.assetid: 9e185435-a624-4380-adfd-be4f3645ee5d
title: Messaggio WM_GETTEXTLENGTH (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0efc058033f9c4939137414d305d0717b54bef54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967923"
---
# <a name="wm_gettextlength-message"></a><span data-ttu-id="da577-103">\_Messaggio GETTEXTLENGTH WM</span><span class="sxs-lookup"><span data-stu-id="da577-103">WM\_GETTEXTLENGTH message</span></span>

<span data-ttu-id="da577-104">Determina la lunghezza, in caratteri, del testo associato a una finestra.</span><span class="sxs-lookup"><span data-stu-id="da577-104">Determines the length, in characters, of the text associated with a window.</span></span>


```C++
#define WM_GETTEXTLENGTH                0x000E
```



## <a name="parameters"></a><span data-ttu-id="da577-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="da577-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da577-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="da577-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="da577-107">Questo parametro non viene utilizzato e deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="da577-107">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="da577-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="da577-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="da577-109">Questo parametro non viene utilizzato e deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="da577-109">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da577-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="da577-110">Return value</span></span>

<span data-ttu-id="da577-111">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="da577-111">Type: **LRESULT**</span></span>

<span data-ttu-id="da577-112">Il valore restituito è la lunghezza del testo in caratteri, escluso il carattere null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="da577-112">The return value is the length of the text in characters, not including the terminating null character.</span></span>

## <a name="remarks"></a><span data-ttu-id="da577-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="da577-113">Remarks</span></span>

<span data-ttu-id="da577-114">Per un controllo di modifica, il testo da copiare è il contenuto del controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="da577-114">For an edit control, the text to be copied is the content of the edit control.</span></span> <span data-ttu-id="da577-115">Per una casella combinata, il testo è il contenuto della parte del controllo di modifica (o del testo statico) della casella combinata.</span><span class="sxs-lookup"><span data-stu-id="da577-115">For a combo box, the text is the content of the edit control (or static-text) portion of the combo box.</span></span> <span data-ttu-id="da577-116">Per un pulsante, il testo è il nome del pulsante.</span><span class="sxs-lookup"><span data-stu-id="da577-116">For a button, the text is the button name.</span></span> <span data-ttu-id="da577-117">Per le altre finestre, il testo è il titolo della finestra.</span><span class="sxs-lookup"><span data-stu-id="da577-117">For other windows, the text is the window title.</span></span> <span data-ttu-id="da577-118">Per determinare la lunghezza di un elemento in una casella di riepilogo, un'applicazione può usare il messaggio [**\_ GETTEXTLEN lb**](../controls/lb-gettextlen.md) .</span><span class="sxs-lookup"><span data-stu-id="da577-118">To determine the length of an item in a list box, an application can use the [**LB\_GETTEXTLEN**](../controls/lb-gettextlen.md) message.</span></span>

<span data-ttu-id="da577-119">Quando viene inviato il messaggio **WM \_ GETTEXTLENGTH** , la funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) restituisce la lunghezza, in caratteri, del testo.</span><span class="sxs-lookup"><span data-stu-id="da577-119">When the **WM\_GETTEXTLENGTH** message is sent, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function returns the length, in characters, of the text.</span></span> <span data-ttu-id="da577-120">In determinate condizioni, la funzione **DefWindowProc** restituisce un valore maggiore della lunghezza effettiva del testo.</span><span class="sxs-lookup"><span data-stu-id="da577-120">Under certain conditions, the **DefWindowProc** function returns a value that is larger than the actual length of the text.</span></span> <span data-ttu-id="da577-121">Questa situazione si verifica con determinate combinazioni di ANSI e Unicode ed è causata dal sistema che consente la presenza di caratteri DBCS (Double-byte character set) all'interno del testo.</span><span class="sxs-lookup"><span data-stu-id="da577-121">This occurs with certain mixtures of ANSI and Unicode, and is due to the system allowing for the possible existence of double-byte character set (DBCS) characters within the text.</span></span> <span data-ttu-id="da577-122">Il valore restituito, tuttavia, sarà sempre almeno uguale alla lunghezza effettiva del testo; è pertanto possibile utilizzarlo sempre per guidare l'allocazione del buffer.</span><span class="sxs-lookup"><span data-stu-id="da577-122">The return value, however, will always be at least as large as the actual length of the text; you can thus always use it to guide buffer allocation.</span></span> <span data-ttu-id="da577-123">Questo comportamento può verificarsi quando un'applicazione utilizza funzioni ANSI e finestre di dialogo comuni che utilizzano Unicode.</span><span class="sxs-lookup"><span data-stu-id="da577-123">This behavior can occur when an application uses both ANSI functions and common dialogs, which use Unicode.</span></span>

<span data-ttu-id="da577-124">Per ottenere la lunghezza esatta del testo, usare i messaggi [**WM \_ gettext**](wm-gettext.md), [**lb \_ gettext**](../controls/lb-gettext.md)o [**CB \_ GETLBTEXT**](../controls/cb-getlbtext.md) oppure la funzione [**GetWindowText**](/windows/win32/api/winuser/nf-winuser-getwindowtexta) .</span><span class="sxs-lookup"><span data-stu-id="da577-124">To obtain the exact length of the text, use the [**WM\_GETTEXT**](wm-gettext.md), [**LB\_GETTEXT**](../controls/lb-gettext.md), or [**CB\_GETLBTEXT**](../controls/cb-getlbtext.md) messages, or the [**GetWindowText**](/windows/win32/api/winuser/nf-winuser-getwindowtexta) function.</span></span>

<span data-ttu-id="da577-125">L'invio di un messaggio **WM \_ GETTEXTLENGTH** a un controllo statico non di testo, ad esempio una bitmap statica o un'icona statica controlc, non restituisce un valore stringa.</span><span class="sxs-lookup"><span data-stu-id="da577-125">Sending a **WM\_GETTEXTLENGTH** message to a non-text static control, such as a static bitmap or static icon controlc, does not return a string value.</span></span> <span data-ttu-id="da577-126">Viene invece restituito zero.</span><span class="sxs-lookup"><span data-stu-id="da577-126">Instead, it returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="da577-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="da577-127">Requirements</span></span>



| <span data-ttu-id="da577-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="da577-128">Requirement</span></span> | <span data-ttu-id="da577-129">Valore</span><span class="sxs-lookup"><span data-stu-id="da577-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da577-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="da577-130">Minimum supported client</span></span><br/> | <span data-ttu-id="da577-131">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="da577-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="da577-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="da577-132">Minimum supported server</span></span><br/> | <span data-ttu-id="da577-133">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="da577-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="da577-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="da577-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="da577-135"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="da577-135"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da577-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="da577-136">See also</span></span>

<dl> <dt>

<span data-ttu-id="da577-137">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="da577-137">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="da577-138">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="da577-138">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="da577-139">**GetWindowText**</span><span class="sxs-lookup"><span data-stu-id="da577-139">**GetWindowText**</span></span>](/windows/win32/api/winuser/nf-winuser-getwindowtexta)
</dt> <dt>

[<span data-ttu-id="da577-140">**GetWindowTextLength**</span><span class="sxs-lookup"><span data-stu-id="da577-140">**GetWindowTextLength**</span></span>](/windows/win32/api/winuser/nf-winuser-getwindowtextlengtha)
</dt> <dt>

[<span data-ttu-id="da577-141">**WM \_ GETtext**</span><span class="sxs-lookup"><span data-stu-id="da577-141">**WM\_GETTEXT**</span></span>](wm-gettext.md)
</dt> <dt>

<span data-ttu-id="da577-142">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="da577-142">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="da577-143">Windows</span><span class="sxs-lookup"><span data-stu-id="da577-143">Windows</span></span>](windows.md)
</dt> <dt>

<span data-ttu-id="da577-144">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="da577-144">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="da577-145">**CB \_ GETLBTEXT**</span><span class="sxs-lookup"><span data-stu-id="da577-145">**CB\_GETLBTEXT**</span></span>](../controls/cb-getlbtext.md)
</dt> <dt>

[<span data-ttu-id="da577-146">**GetText LB \_**</span><span class="sxs-lookup"><span data-stu-id="da577-146">**LB\_GETTEXT**</span></span>](../controls/lb-gettext.md)
</dt> <dt>

[<span data-ttu-id="da577-147">**\_GETTEXTLEN lb**</span><span class="sxs-lookup"><span data-stu-id="da577-147">**LB\_GETTEXTLEN**</span></span>](../controls/lb-gettextlen.md)
</dt> </dl>

 

 
