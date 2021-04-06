---
title: Codice di notifica EN_SAVECLIPBOARD (RichEdit. h)
description: Notifica alla finestra padre del controllo Rich Edit che il controllo viene chiuso e gli Appunti contengono informazioni. Un controllo Rich Edit invia questo codice di notifica sotto forma di un \_ messaggio di notifica WM.
ms.assetid: e8b95e80-6494-4153-8e78-ede9ed17c66f
keywords:
- Controlli di Windows per il codice di notifica EN_SAVECLIPBOARD
topic_type:
- apiref
api_name:
- EN_SAVECLIPBOARD
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a1fd7c6e11ed82a7f77483c692dd68f860395c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873665"
---
# <a name="en_saveclipboard-notification-code"></a><span data-ttu-id="5ac07-105">\_Codice di notifica en SAVECLIPBOARD</span><span class="sxs-lookup"><span data-stu-id="5ac07-105">EN\_SAVECLIPBOARD notification code</span></span>

<span data-ttu-id="5ac07-106">Notifica alla finestra padre del controllo Rich Edit che il controllo viene chiuso e gli Appunti contengono informazioni.</span><span class="sxs-lookup"><span data-stu-id="5ac07-106">Notifies the rich edit control's parent window that the control is closing and the clipboard contains information.</span></span> <span data-ttu-id="5ac07-107">Un controllo Rich Edit invia questo codice di notifica sotto forma di un messaggio di [**\_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="5ac07-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_SAVECLIPBOARD

    penSaveClipboard = (ENSAVECLIPBOARD *) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="5ac07-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="5ac07-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ac07-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5ac07-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5ac07-110">Struttura [**ENSAVECLIPBOARD**](/windows/desktop/api/Richedit/ns-richedit-ensaveclipboard) che contiene informazioni sulle informazioni sugli Appunti.</span><span class="sxs-lookup"><span data-stu-id="5ac07-110">An [**ENSAVECLIPBOARD**](/windows/desktop/api/Richedit/ns-richedit-ensaveclipboard) structure that contains information about clipboard information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ac07-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5ac07-111">Return value</span></span>

<span data-ttu-id="5ac07-112">Restituisce zero se gli Appunti devono essere resi disponibili ad altre applicazioni.</span><span class="sxs-lookup"><span data-stu-id="5ac07-112">Return zero if the clipboard should be made available to other applications.</span></span>

<span data-ttu-id="5ac07-113">Restituisce un valore diverso da zero se gli Appunti non devono essere salvati.</span><span class="sxs-lookup"><span data-stu-id="5ac07-113">Return a nonzero value if the clipboard should not be saved.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ac07-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="5ac07-114">Remarks</span></span>

<span data-ttu-id="5ac07-115">La finestra padre otterrà sempre un messaggio [**di \_ notifica WM**](wm-notify.md) per questo evento, ma non richiede una maschera di notifica inviata con [**em \_ SETEVENTMASK**](em-seteventmask.md).</span><span class="sxs-lookup"><span data-stu-id="5ac07-115">The parent window will always get a [**WM\_NOTIFY**](wm-notify.md) message for this event, it does not require a notification mask sent with [**EM\_SETEVENTMASK**](em-seteventmask.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5ac07-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5ac07-116">Requirements</span></span>



| <span data-ttu-id="5ac07-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ac07-117">Requirement</span></span> | <span data-ttu-id="5ac07-118">Valore</span><span class="sxs-lookup"><span data-stu-id="5ac07-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5ac07-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5ac07-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5ac07-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5ac07-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5ac07-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5ac07-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5ac07-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5ac07-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5ac07-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5ac07-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ac07-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ac07-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ac07-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5ac07-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="5ac07-126">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="5ac07-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5ac07-127">**ENSAVECLIPBOARD**</span><span class="sxs-lookup"><span data-stu-id="5ac07-127">**ENSAVECLIPBOARD**</span></span>](/windows/desktop/api/Richedit/ns-richedit-ensaveclipboard)
</dt> </dl>

 

 





