---
title: Codice di notifica EN_STOPNOUNDO (RichEdit. h)
description: Notifica alla finestra padre di un controllo Rich Edit che si è verificata un'azione per la quale il controllo non è in grado di allocare memoria sufficiente per mantenere lo stato di annullamento. Un controllo Rich Edit invia questo codice di notifica sotto forma di un \_ messaggio di notifica WM.
ms.assetid: 5608f6dd-83dc-4712-b485-dd9bc17dea24
keywords:
- Controlli di Windows per il codice di notifica EN_STOPNOUNDO
topic_type:
- apiref
api_name:
- EN_STOPNOUNDO
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ab71e6e1a78c468e6349fc1f42d03e9b68fb043
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121015"
---
# <a name="en_stopnoundo-notification-code"></a><span data-ttu-id="0e194-105">\_Codice di notifica en STOPNOUNDO</span><span class="sxs-lookup"><span data-stu-id="0e194-105">EN\_STOPNOUNDO notification code</span></span>

<span data-ttu-id="0e194-106">Notifica alla finestra padre di un controllo Rich Edit che si è verificata un'azione per la quale il controllo non è in grado di allocare memoria sufficiente per mantenere lo stato di annullamento.</span><span class="sxs-lookup"><span data-stu-id="0e194-106">Notifies a rich edit control's parent window that an action occurred for which the control cannot allocate enough memory to maintain the undo state.</span></span> <span data-ttu-id="0e194-107">Un controllo Rich Edit invia questo codice di notifica sotto forma di un messaggio di [**\_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="0e194-107">A rich edit control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
EN_STOPNOUNDO

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="0e194-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="0e194-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e194-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0e194-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0e194-110">Struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) .</span><span class="sxs-lookup"><span data-stu-id="0e194-110">An [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e194-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0e194-111">Return value</span></span>

<span data-ttu-id="0e194-112">Restituisce zero per continuare l'operazione di **annullamento** .</span><span class="sxs-lookup"><span data-stu-id="0e194-112">Return zero to continue the **Undo** operation.</span></span>

<span data-ttu-id="0e194-113">Restituisce un valore diverso da zero per arrestare l'operazione di **annullamento** .</span><span class="sxs-lookup"><span data-stu-id="0e194-113">Return a nonzero value to stop the **Undo** operation.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e194-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="0e194-114">Remarks</span></span>

<span data-ttu-id="0e194-115">La finestra padre otterrà sempre un messaggio [**di \_ notifica WM**](wm-notify.md) per questo evento, ma non richiede una maschera di notifica inviata con [**em \_ SETEVENTMASK**](em-seteventmask.md).</span><span class="sxs-lookup"><span data-stu-id="0e194-115">The parent window will always get a [**WM\_NOTIFY**](wm-notify.md) message for this event, it does not require a notification mask sent with [**EM\_SETEVENTMASK**](em-seteventmask.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0e194-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0e194-116">Requirements</span></span>



| <span data-ttu-id="0e194-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e194-117">Requirement</span></span> | <span data-ttu-id="0e194-118">Valore</span><span class="sxs-lookup"><span data-stu-id="0e194-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0e194-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0e194-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0e194-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0e194-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0e194-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0e194-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0e194-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0e194-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0e194-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0e194-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e194-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e194-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e194-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0e194-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="0e194-126">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="0e194-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0e194-127">**NMHDR**</span><span class="sxs-lookup"><span data-stu-id="0e194-127">**NMHDR**</span></span>](/windows/desktop/api/richedit/ns-richedit-nmhdr)
</dt> <dt>

[<span data-ttu-id="0e194-128">**\_notifica WM**</span><span class="sxs-lookup"><span data-stu-id="0e194-128">**WM\_NOTIFY**</span></span>](wm-notify.md)
</dt> </dl>

 

 





