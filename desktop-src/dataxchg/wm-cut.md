---
title: Messaggio WM_CUT (winuser. h)
description: Un'applicazione invia un \_ messaggio WM Cut a un controllo di modifica o a una casella combinata per eliminare (tagliare) la selezione corrente, se presente, nel controllo di modifica e copiare il testo eliminato negli Appunti nel \_ formato di testo CF.
ms.assetid: 6ac45589-3e34-491c-9562-e072ddc478f9
keywords:
- Scambio di dati del messaggio WM_CUT
topic_type:
- apiref
api_name:
- WM_CUT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a63dfe85fb637636fbabbce5fa139699fd09a65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301494"
---
# <a name="wm_cut-message"></a><span data-ttu-id="4ab11-104">\_Messaggio WM Cut</span><span class="sxs-lookup"><span data-stu-id="4ab11-104">WM\_CUT message</span></span>

<span data-ttu-id="4ab11-105">Un'applicazione invia un messaggio **WM \_ Cut** a un controllo di modifica o a una casella combinata per eliminare (tagliare) la selezione corrente, se presente, nel controllo di modifica e copiare il testo eliminato negli Appunti nel formato di [**\_ testo CF**](standard-clipboard-formats.md) .</span><span class="sxs-lookup"><span data-stu-id="4ab11-105">An application sends a **WM\_CUT** message to an edit control or combo box to delete (cut) the current selection, if any, in the edit control and copy the deleted text to the clipboard in [**CF\_TEXT**](standard-clipboard-formats.md) format.</span></span>


```C++
#define WM_CUT                          0x0300
```



## <a name="parameters"></a><span data-ttu-id="4ab11-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4ab11-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ab11-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4ab11-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4ab11-108">Questo parametro non viene utilizzato e deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="4ab11-108">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="4ab11-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4ab11-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4ab11-110">Questo parametro non viene utilizzato e deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="4ab11-110">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ab11-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4ab11-111">Return value</span></span>

<span data-ttu-id="4ab11-112">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="4ab11-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ab11-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="4ab11-113">Remarks</span></span>

<span data-ttu-id="4ab11-114">L'eliminazione eseguita dal messaggio **WM \_ Cut** può essere annullata inviando il controllo di modifica un messaggio di [**\_ annullamento em**](../controls/em-undo.md) .</span><span class="sxs-lookup"><span data-stu-id="4ab11-114">The deletion performed by the **WM\_CUT** message can be undone by sending the edit control an [**EM\_UNDO**](../controls/em-undo.md) message.</span></span>

<span data-ttu-id="4ab11-115">Per eliminare la selezione corrente senza inserire il testo eliminato negli Appunti, usare il messaggio [**\_ Clear di WM**](wm-clear.md) .</span><span class="sxs-lookup"><span data-stu-id="4ab11-115">To delete the current selection without placing the deleted text on the clipboard, use the [**WM\_CLEAR**](wm-clear.md) message.</span></span>

<span data-ttu-id="4ab11-116">Quando viene inviato a una casella combinata, il messaggio **WM \_ Cut** viene gestito dal controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="4ab11-116">When sent to a combo box, the **WM\_CUT** message is handled by its edit control.</span></span> <span data-ttu-id="4ab11-117">Questo messaggio non ha alcun effetto quando viene inviato a una casella combinata con lo stile [**\_ DropDownList CBS**](../controls/combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="4ab11-117">This message has no effect when sent to a combo box with the [**CBS\_DROPDOWNLIST**](../controls/combo-box-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ab11-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4ab11-118">Requirements</span></span>



| <span data-ttu-id="4ab11-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ab11-119">Requirement</span></span> | <span data-ttu-id="4ab11-120">Valore</span><span class="sxs-lookup"><span data-stu-id="4ab11-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ab11-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4ab11-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4ab11-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4ab11-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="4ab11-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4ab11-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4ab11-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4ab11-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4ab11-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4ab11-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ab11-126"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4ab11-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ab11-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4ab11-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="4ab11-128">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="4ab11-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4ab11-129">**chiaro di WM \_**</span><span class="sxs-lookup"><span data-stu-id="4ab11-129">**WM\_CLEAR**</span></span>](wm-clear.md)
</dt> <dt>

[<span data-ttu-id="4ab11-130">**\_copia WM**</span><span class="sxs-lookup"><span data-stu-id="4ab11-130">**WM\_COPY**</span></span>](wm-copy.md)
</dt> <dt>

[<span data-ttu-id="4ab11-131">**\_Incolla WM**</span><span class="sxs-lookup"><span data-stu-id="4ab11-131">**WM\_PASTE**</span></span>](wm-paste.md)
</dt> <dt>

[<span data-ttu-id="4ab11-132">**\_annullamento WM**</span><span class="sxs-lookup"><span data-stu-id="4ab11-132">**WM\_UNDO**</span></span>](/windows/desktop/Controls/wm-undo)
</dt> <dt>

<span data-ttu-id="4ab11-133">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="4ab11-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="4ab11-134">Appunti</span><span class="sxs-lookup"><span data-stu-id="4ab11-134">Clipboard</span></span>](clipboard.md)
</dt> <dt>

<span data-ttu-id="4ab11-135">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="4ab11-135">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="4ab11-136">**\_Annulla**</span><span class="sxs-lookup"><span data-stu-id="4ab11-136">**EM\_UNDO**</span></span>](../controls/em-undo.md)
</dt> </dl>

 

