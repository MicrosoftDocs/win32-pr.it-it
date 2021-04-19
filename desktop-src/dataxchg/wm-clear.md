---
title: Messaggio WM_CLEAR (winuser. h)
description: Un'applicazione invia un \_ messaggio Clear WM a un controllo di modifica o a una casella combinata per eliminare (cancellare) la selezione corrente, se presente, dal controllo di modifica.
ms.assetid: 6730a725-01ec-4821-9ffc-1ea267d665b3
keywords:
- Scambio di dati del messaggio WM_CLEAR
topic_type:
- apiref
api_name:
- WM_CLEAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61a8e325704d1e8b953fe59bfaf4e8fcee62cf40
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301774"
---
# <a name="wm_clear-message"></a><span data-ttu-id="d2986-104">\_Messaggio Clear WM</span><span class="sxs-lookup"><span data-stu-id="d2986-104">WM\_CLEAR message</span></span>

<span data-ttu-id="d2986-105">Un'applicazione invia un **messaggio \_ Clear WM** a un controllo di modifica o a una casella combinata per eliminare (cancellare) la selezione corrente, se presente, dal controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="d2986-105">An application sends a **WM\_CLEAR** message to an edit control or combo box to delete (clear) the current selection, if any, from the edit control.</span></span>


```C++
#define WM_CLEAR                        0x0303
```



## <a name="parameters"></a><span data-ttu-id="d2986-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d2986-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2986-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d2986-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d2986-108">Questo parametro non viene utilizzato e deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="d2986-108">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="d2986-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d2986-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d2986-110">Questo parametro non viene utilizzato e deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="d2986-110">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2986-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d2986-111">Return value</span></span>

<span data-ttu-id="d2986-112">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="d2986-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2986-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="d2986-113">Remarks</span></span>

<span data-ttu-id="d2986-114">Per annullare l'operazione di eliminazione del messaggio **WM \_ Clear** , è possibile inviare il controllo di modifica un messaggio di [**\_ annullamento em**](../controls/em-undo.md) .</span><span class="sxs-lookup"><span data-stu-id="d2986-114">The deletion performed by the **WM\_CLEAR** message can be undone by sending the edit control an [**EM\_UNDO**](../controls/em-undo.md) message.</span></span>

<span data-ttu-id="d2986-115">Per eliminare la selezione corrente e inserire il contenuto eliminato negli Appunti, usare il messaggio [**WM \_ Cut**](wm-cut.md) .</span><span class="sxs-lookup"><span data-stu-id="d2986-115">To delete the current selection and place the deleted content on the clipboard, use the [**WM\_CUT**](wm-cut.md) message.</span></span>

<span data-ttu-id="d2986-116">Quando viene inviato a una casella combinata, il messaggio **WM \_ Clear** viene gestito dal relativo controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="d2986-116">When sent to a combo box, the **WM\_CLEAR** message is handled by its edit control.</span></span> <span data-ttu-id="d2986-117">Questo messaggio non ha alcun effetto quando viene inviato a una casella combinata con lo stile [**\_ DropDownList CBS**](../controls/combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="d2986-117">This message has no effect when sent to a combo box with the [**CBS\_DROPDOWNLIST**](../controls/combo-box-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2986-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d2986-118">Requirements</span></span>



| <span data-ttu-id="d2986-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2986-119">Requirement</span></span> | <span data-ttu-id="d2986-120">Valore</span><span class="sxs-lookup"><span data-stu-id="d2986-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2986-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d2986-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d2986-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d2986-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="d2986-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d2986-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d2986-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d2986-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d2986-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d2986-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2986-126"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d2986-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2986-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d2986-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="d2986-128">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="d2986-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d2986-129">**\_copia WM**</span><span class="sxs-lookup"><span data-stu-id="d2986-129">**WM\_COPY**</span></span>](wm-copy.md)
</dt> <dt>

[<span data-ttu-id="d2986-130">**\_taglia WM**</span><span class="sxs-lookup"><span data-stu-id="d2986-130">**WM\_CUT**</span></span>](wm-cut.md)
</dt> <dt>

[<span data-ttu-id="d2986-131">**\_Incolla WM**</span><span class="sxs-lookup"><span data-stu-id="d2986-131">**WM\_PASTE**</span></span>](wm-paste.md)
</dt> <dt>

[<span data-ttu-id="d2986-132">**\_annullamento WM**</span><span class="sxs-lookup"><span data-stu-id="d2986-132">**WM\_UNDO**</span></span>](/windows/desktop/Controls/wm-undo)
</dt> <dt>

<span data-ttu-id="d2986-133">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="d2986-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d2986-134">Appunti</span><span class="sxs-lookup"><span data-stu-id="d2986-134">Clipboard</span></span>](clipboard.md)
</dt> </dl>

 

