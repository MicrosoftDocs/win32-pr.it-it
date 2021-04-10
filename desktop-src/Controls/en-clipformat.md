---
title: Codice di notifica EN_CLIPFORMAT (RichEdit. h)
description: Notifica alla finestra padre di un controllo Rich Edit che è stata eseguita una copia con un formato degli Appunti specifico. Un controllo Rich Edit senza finestra Invia questa notifica tramite il metodo ITextHost TxNotify.
ms.assetid: 79FE1350-4D45-447B-B705-63E966AC7F0E
keywords:
- Controlli di Windows per il codice di notifica EN_CLIPFORMAT
topic_type:
- apiref
api_name:
- EN_CLIPFORMAT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0430e8a4dba0b1a18f81f4e28ec67f2c93551cd5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964046"
---
# <a name="en_clipformat-notification-code"></a><span data-ttu-id="075e8-105">\_Codice di notifica en CLIPFORMAT</span><span class="sxs-lookup"><span data-stu-id="075e8-105">EN\_CLIPFORMAT notification code</span></span>

<span data-ttu-id="075e8-106">Notifica alla finestra padre di un controllo Rich Edit che è stata eseguita una copia con un formato degli Appunti specifico.</span><span class="sxs-lookup"><span data-stu-id="075e8-106">Notifies a rich edit control's parent window that a paste occurred with a particular clipboard format.</span></span> <span data-ttu-id="075e8-107">Un controllo Rich Edit senza finestra Invia questa notifica tramite il metodo [**ITextHost:: TxNotify**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify) .</span><span class="sxs-lookup"><span data-stu-id="075e8-107">A windowless rich edit control sends this notification by using the [**ITextHost::TxNotify**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txnotify) method.</span></span>


```C++
EN_CLIPFORMAT

      pClipboardFmt = (CLIPBOARDFORMAT *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="075e8-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="075e8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="075e8-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="075e8-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="075e8-110">ID della finestra recuperato chiamando la funzione [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) con il \_ valore ID GWL.</span><span class="sxs-lookup"><span data-stu-id="075e8-110">The window ID retrieved by calling the [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) function with the GWL\_ID value.</span></span>

</dd> <dt>

<span data-ttu-id="075e8-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="075e8-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="075e8-112">Puntatore a una struttura [**CLIPBOARDFORMAT**](/windows/desktop/api/Richedit/ns-richedit-clipboardformat) che contiene informazioni sul formato degli Appunti.</span><span class="sxs-lookup"><span data-stu-id="075e8-112">A pointer to a [**CLIPBOARDFORMAT**](/windows/desktop/api/Richedit/ns-richedit-clipboardformat) structure that contains information about the clipboard format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="075e8-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="075e8-113">Return value</span></span>

<span data-ttu-id="075e8-114">Il valore restituito viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="075e8-114">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="075e8-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="075e8-115">Remarks</span></span>

<span data-ttu-id="075e8-116">Per ricevere \_ i codici di notifica en CLIPFORMAT, specificare [**ENM \_ CLIPFORMAT**](rich-edit-control-event-mask-flags.md) nella maschera inviata con il messaggio [**\_ SETEVENTMASK em**](em-seteventmask.md) .</span><span class="sxs-lookup"><span data-stu-id="075e8-116">To receive EN\_CLIPFORMAT notification codes, specify [**ENM\_CLIPFORMAT**](rich-edit-control-event-mask-flags.md) in the mask sent with the [**EM\_SETEVENTMASK**](em-seteventmask.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="075e8-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="075e8-117">Requirements</span></span>



| <span data-ttu-id="075e8-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="075e8-118">Requirement</span></span> | <span data-ttu-id="075e8-119">Valore</span><span class="sxs-lookup"><span data-stu-id="075e8-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="075e8-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="075e8-120">Minimum supported client</span></span><br/> | <span data-ttu-id="075e8-121">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="075e8-121">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="075e8-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="075e8-122">Minimum supported server</span></span><br/> | <span data-ttu-id="075e8-123">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="075e8-123">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="075e8-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="075e8-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="075e8-125"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="075e8-125"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="075e8-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="075e8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="075e8-127">**CLIPBOARDFORMAT**</span><span class="sxs-lookup"><span data-stu-id="075e8-127">**CLIPBOARDFORMAT**</span></span>](/windows/desktop/api/Richedit/ns-richedit-clipboardformat)
</dt> </dl>

 

