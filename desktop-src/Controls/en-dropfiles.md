---
title: Codice di notifica EN_DROPFILES (RichEdit. h)
description: Notifica a una finestra padre del controllo Rich Edit che l'utente sta tentando di rilasciare i file nel controllo. Un controllo Rich Edit invia questo codice di notifica sotto forma di un \_ messaggio di notifica WM quando riceve il \_ messaggio WM DROPFILES.
ms.assetid: fcae0ff8-ce37-4c71-b14c-cbd6429b4ab3
keywords:
- Controlli di Windows per il codice di notifica EN_DROPFILES
topic_type:
- apiref
api_name:
- EN_DROPFILES
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72c0ed1a4a9b95348b1de20e54fcf3b167df19f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475394"
---
# <a name="en_dropfiles-notification-code"></a><span data-ttu-id="4eaaf-105">\_Codice di notifica en DropFiles</span><span class="sxs-lookup"><span data-stu-id="4eaaf-105">EN\_DROPFILES notification code</span></span>

<span data-ttu-id="4eaaf-106">Notifica a una finestra padre del controllo Rich Edit che l'utente sta tentando di rilasciare i file nel controllo.</span><span class="sxs-lookup"><span data-stu-id="4eaaf-106">Notifies a rich edit control parent window that the user is attempting to drop files into the control.</span></span> <span data-ttu-id="4eaaf-107">Un controllo Rich Edit invia questo codice di notifica sotto forma di un messaggio di [**\_ notifica WM**](wm-notify.md) quando riceve il messaggio [**WM \_ DropFiles**](/windows/desktop/shell/wm-dropfiles) .</span><span class="sxs-lookup"><span data-stu-id="4eaaf-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message when it receives the [**WM\_DROPFILES**](/windows/desktop/shell/wm-dropfiles) message.</span></span>


```C++
EN_DROPFILES

      penDropFiles = (ENDROPFILES *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="4eaaf-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="4eaaf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4eaaf-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4eaaf-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4eaaf-110">Struttura [**ENDROPFILES**](/windows/desktop/api/Richedit/ns-richedit-endropfiles) che riceve informazioni sui file eliminati.</span><span class="sxs-lookup"><span data-stu-id="4eaaf-110">An [**ENDROPFILES**](/windows/desktop/api/Richedit/ns-richedit-endropfiles) structure that receives dropped files information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4eaaf-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4eaaf-111">Return value</span></span>

<span data-ttu-id="4eaaf-112">Restituisce un valore diverso da zero per consentire l'operazione di rilascio.</span><span class="sxs-lookup"><span data-stu-id="4eaaf-112">Return a nonzero value to allow the drop operation.</span></span>

<span data-ttu-id="4eaaf-113">Restituisce zero per ignorare l'operazione DROP.</span><span class="sxs-lookup"><span data-stu-id="4eaaf-113">Return zero to ignore the drop operation.</span></span>

## <a name="remarks"></a><span data-ttu-id="4eaaf-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="4eaaf-114">Remarks</span></span>

<span data-ttu-id="4eaaf-115">Per un controllo Rich Edit per la ricezione di messaggi [**WM \_ DropFiles**](/windows/desktop/shell/wm-dropfiles) , è necessario che la finestra padre registri il controllo come destinazione di rilascio tramite la funzione [**DragAcceptFiles**](/windows/desktop/api/shellapi/nf-shellapi-dragacceptfiles) .</span><span class="sxs-lookup"><span data-stu-id="4eaaf-115">For a rich edit control to receive [**WM\_DROPFILES**](/windows/desktop/shell/wm-dropfiles) messages, the parent window must register the control as a drop target by using the [**DragAcceptFiles**](/windows/desktop/api/shellapi/nf-shellapi-dragacceptfiles) function.</span></span> <span data-ttu-id="4eaaf-116">Il controllo non registra se stesso.</span><span class="sxs-lookup"><span data-stu-id="4eaaf-116">The control does not register itself.</span></span>

<span data-ttu-id="4eaaf-117">Per ricevere \_ i codici di notifica en DropFiles, specificare [**ENM \_ DropFiles**](rich-edit-control-event-mask-flags.md) nella maschera inviata con il messaggio [**\_ SETEVENTMASK em**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="4eaaf-117">To receive EN\_DROPFILES notification codes, specify [**ENM\_DROPFILES**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="4eaaf-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4eaaf-118">Requirements</span></span>



| <span data-ttu-id="4eaaf-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="4eaaf-119">Requirement</span></span> | <span data-ttu-id="4eaaf-120">Valore</span><span class="sxs-lookup"><span data-stu-id="4eaaf-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4eaaf-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4eaaf-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4eaaf-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4eaaf-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4eaaf-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4eaaf-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4eaaf-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4eaaf-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4eaaf-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4eaaf-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="4eaaf-126"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="4eaaf-126"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4eaaf-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4eaaf-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="4eaaf-128">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="4eaaf-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4eaaf-129">**ENDROPFILES**</span><span class="sxs-lookup"><span data-stu-id="4eaaf-129">**ENDROPFILES**</span></span>](/windows/desktop/api/Richedit/ns-richedit-endropfiles)
</dt> </dl>

 

