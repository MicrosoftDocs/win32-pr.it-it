---
title: Codice di notifica EN_LINK (RichEdit. h)
description: Un controllo Rich Edit invia \_ i codici di notifica dei collegamenti it quando riceve diversi messaggi, ad esempio quando l'utente fa clic sul mouse o quando il puntatore del mouse è posizionato su un testo con l' \_ effetto del collegamento CFE.
ms.assetid: 67f02908-957e-4d91-8a70-70399ce9cf2e
keywords:
- Controlli di Windows per il codice di notifica EN_LINK
topic_type:
- apiref
api_name:
- EN_LINK
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec0eeb134804f671502d4cd3abbe2cb6995194af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478556"
---
# <a name="en_link-notification-code"></a><span data-ttu-id="bd29f-104">\_Codice di notifica del collegamento it</span><span class="sxs-lookup"><span data-stu-id="bd29f-104">EN\_LINK notification code</span></span>

<span data-ttu-id="bd29f-105">Un controllo Rich Edit invia \_ i codici di notifica dei collegamenti it quando riceve diversi messaggi, ad esempio quando l'utente fa clic sul mouse o quando il puntatore del mouse è posizionato su un testo con l'effetto del **\_ collegamento CFE** .</span><span class="sxs-lookup"><span data-stu-id="bd29f-105">A rich edit control sends EN\_LINK notification codes when it receives various messages, for example, when the user clicks the mouse or when the mouse pointer is over text that has the **CFE\_LINK** effect.</span></span> <span data-ttu-id="bd29f-106">Un controllo Rich Edit senza finestra Invia questa notifica tramite il metodo [**ITextHost:: TxNotify**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify) .</span><span class="sxs-lookup"><span data-stu-id="bd29f-106">A windowless rich edit control sends this notification by using the [**ITextHost::TxNotify**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify) method.</span></span> <span data-ttu-id="bd29f-107">La finestra padre del controllo riceve questo codice di notifica tramite un messaggio di [**\_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="bd29f-107">The parent window of the control receives this notification code through a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_LINK

    penLink = (ENLINK *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="bd29f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="bd29f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd29f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bd29f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bd29f-110">ID della finestra recuperato chiamando la funzione [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) con il \_ valore ID GWL.</span><span class="sxs-lookup"><span data-stu-id="bd29f-110">The window ID retrieved by calling the [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) function with the GWL\_ID value.</span></span>

</dd> <dt>

<span data-ttu-id="bd29f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bd29f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bd29f-112">Puntatore a una struttura di [**collegamento**](/windows/desktop/api/Richedit/ns-richedit-enlink) .</span><span class="sxs-lookup"><span data-stu-id="bd29f-112">Pointer to an [**ENLINK**](/windows/desktop/api/Richedit/ns-richedit-enlink) structure.</span></span> <span data-ttu-id="bd29f-113">La struttura contiene una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , informazioni sul codice di notifica e una struttura [**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange) che indica l'intervallo di caratteri con effetto di **\_ collegamento CFE** .</span><span class="sxs-lookup"><span data-stu-id="bd29f-113">The structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure, information about the notification code, and a [**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange) structure that indicates the range of characters that have the **CFE\_LINK** effect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd29f-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bd29f-114">Return value</span></span>

<span data-ttu-id="bd29f-115">Restituisce zero per consentire al controllo di procedere con la normale gestione del messaggio.</span><span class="sxs-lookup"><span data-stu-id="bd29f-115">Return zero to allow the control to proceed with its normal handling of the message.</span></span>

<span data-ttu-id="bd29f-116">Restituisce un valore diverso da zero per impedire che il controllo gestisca il messaggio.</span><span class="sxs-lookup"><span data-stu-id="bd29f-116">Return a nonzero value to prevent the control from handling the message.</span></span>

<span data-ttu-id="bd29f-117">**Windows 8**: Return **en \_ link \_ ( \_ impostazione predefinita** ) per indirizzare il controllo Rich Edit per eseguire l'azione predefinita.</span><span class="sxs-lookup"><span data-stu-id="bd29f-117">**Windows 8**: Return **EN\_LINK\_DO\_DEFAULT** to direct the rich edit control to perform the default action.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd29f-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="bd29f-118">Remarks</span></span>

<span data-ttu-id="bd29f-119">Per ricevere i codici di notifica dei **\_ collegamenti** in quando il collegamento ha lo stato attivo, specificare il flag di [**\_ collegamento ENM**](rich-edit-control-event-mask-flags.md) nella maschera inviata con il messaggio [**\_ SETEVENTMASK em**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="bd29f-119">To receive **EN\_LINK** notification codes when the link has focus, specify the [**ENM\_LINK**](rich-edit-control-event-mask-flags.md) flag in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

<span data-ttu-id="bd29f-120">Se il collegamento non ha lo stato attivo, per ricevere i codici di notifica dei **\_ collegamenti it** specificare il flag **ses \_ NOFOCUSLINKNOTIFY** nella maschera inviata con il messaggio [**\_ SETEDITSTYLE em**](em-seteditstyle.md) .</span><span class="sxs-lookup"><span data-stu-id="bd29f-120">If the link has no focus, to receive **EN\_LINK** notification codes specify the **SES\_NOFOCUSLINKNOTIFY** flag in the mask sent with the [**EM\_SETEDITSTYLE**](em-seteditstyle.md) message.</span></span>

<span data-ttu-id="bd29f-121">Un controllo Rich Edit invia i codici di notifica di **\_ collegamento it** quando riceve i messaggi seguenti mentre il puntatore del mouse è sopra il testo con l'effetto del **\_ collegamento CFE** :</span><span class="sxs-lookup"><span data-stu-id="bd29f-121">A rich edit control sends **EN\_LINK** notification codes when it receives the following messages while the mouse pointer is over text that has the **CFE\_LINK** effect:</span></span>

-   [<span data-ttu-id="bd29f-122">**\_LBUTTONDBLCLK WM**</span><span class="sxs-lookup"><span data-stu-id="bd29f-122">**WM\_LBUTTONDBLCLK**</span></span>](/windows/desktop/inputdev/wm-lbuttondblclk)
-   [<span data-ttu-id="bd29f-123">**\_LBUTTONDOWN WM**</span><span class="sxs-lookup"><span data-stu-id="bd29f-123">**WM\_LBUTTONDOWN**</span></span>](/windows/desktop/inputdev/wm-lbuttondown)
-   [<span data-ttu-id="bd29f-124">**\_LBUTTONUP WM**</span><span class="sxs-lookup"><span data-stu-id="bd29f-124">**WM\_LBUTTONUP**</span></span>](/windows/desktop/inputdev/wm-lbuttonup)
-   [<span data-ttu-id="bd29f-125">**MOUSEMOVE di WM \_**</span><span class="sxs-lookup"><span data-stu-id="bd29f-125">**WM\_MOUSEMOVE**</span></span>](/windows/desktop/inputdev/wm-mousemove)
-   [<span data-ttu-id="bd29f-126">**\_RBUTTONDBLCLK WM**</span><span class="sxs-lookup"><span data-stu-id="bd29f-126">**WM\_RBUTTONDBLCLK**</span></span>](/windows/desktop/inputdev/wm-rbuttondblclk)
-   [<span data-ttu-id="bd29f-127">**\_RBUTTONDOWN WM**</span><span class="sxs-lookup"><span data-stu-id="bd29f-127">**WM\_RBUTTONDOWN**</span></span>](/windows/desktop/inputdev/wm-rbuttondown)
-   [<span data-ttu-id="bd29f-128">**\_RBUTTONUP WM**</span><span class="sxs-lookup"><span data-stu-id="bd29f-128">**WM\_RBUTTONUP**</span></span>](/windows/desktop/inputdev/wm-rbuttonup)
-   [<span data-ttu-id="bd29f-129">**\_cursore WM**</span><span class="sxs-lookup"><span data-stu-id="bd29f-129">**WM\_SETCURSOR**</span></span>](/windows/desktop/menurc/wm-setcursor)

<span data-ttu-id="bd29f-130">L'effetto del **\_ collegamento CFE** in genere identifica un intervallo di testo che contiene un URL.</span><span class="sxs-lookup"><span data-stu-id="bd29f-130">The **CFE\_LINK** effect typically identifies a range of text that contains an URL.</span></span> <span data-ttu-id="bd29f-131">Le applicazioni possono gestire il \_ codice di notifica del collegamento it cambiando il puntatore del mouse quando è posizionato sull'URL oppure avviando un browser per visualizzare il percorso identificato dall'URL.</span><span class="sxs-lookup"><span data-stu-id="bd29f-131">Applications can handle the EN\_LINK notification code by changing the mouse pointer when it is over the URL, or by starting a browser to view the location identified by the URL.</span></span>

<span data-ttu-id="bd29f-132">Se si invia il [**messaggio \_ AUTOURLDETECT em**](em-autourldetect.md) per abilitare il rilevamento automatico degli URL, il controllo Rich Edit imposta automaticamente l'effetto del **\_ collegamento CFE** per il testo modificato che identifica come un URL.</span><span class="sxs-lookup"><span data-stu-id="bd29f-132">If you send the [**EM\_AUTOURLDETECT**](em-autourldetect.md) message to enable automatic URL detection, the rich edit control automatically sets the **CFE\_LINK** effect for modified text that it identifies as a URL.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd29f-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bd29f-133">Requirements</span></span>



| <span data-ttu-id="bd29f-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd29f-134">Requirement</span></span> | <span data-ttu-id="bd29f-135">Valore</span><span class="sxs-lookup"><span data-stu-id="bd29f-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bd29f-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bd29f-136">Minimum supported client</span></span><br/> | <span data-ttu-id="bd29f-137">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bd29f-137">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bd29f-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bd29f-138">Minimum supported server</span></span><br/> | <span data-ttu-id="bd29f-139">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bd29f-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bd29f-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bd29f-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd29f-141"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd29f-141"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd29f-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bd29f-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd29f-143">**CHARRANGE**</span><span class="sxs-lookup"><span data-stu-id="bd29f-143">**CHARRANGE**</span></span>](/windows/desktop/api/Richedit/ns-richedit-charrange)
</dt> <dt>

[<span data-ttu-id="bd29f-144">**\_AUTOURLDETECT em**</span><span class="sxs-lookup"><span data-stu-id="bd29f-144">**EM\_AUTOURLDETECT**</span></span>](em-autourldetect.md)
</dt> <dt>

[<span data-ttu-id="bd29f-145">**COLLEGAMENTO**</span><span class="sxs-lookup"><span data-stu-id="bd29f-145">**ENLINK**</span></span>](/windows/desktop/api/Richedit/ns-richedit-enlink)
</dt> <dt>

[<span data-ttu-id="bd29f-146">**ITextRange2:: SetURL**</span><span class="sxs-lookup"><span data-stu-id="bd29f-146">**ITextRange2::SetURL**</span></span>](/windows/desktop/api/Tom/nf-tom-itextrange2-seturl)
</dt> <dt>

[<span data-ttu-id="bd29f-147">**NMHDR**</span><span class="sxs-lookup"><span data-stu-id="bd29f-147">**NMHDR**</span></span>](/windows/desktop/api/richedit/ns-richedit-nmhdr)
</dt> </dl>

 

