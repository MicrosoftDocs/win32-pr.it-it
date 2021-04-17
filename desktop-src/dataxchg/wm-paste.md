---
title: Messaggio WM_PASTE (winuser. h)
description: Un'applicazione invia un messaggio di inserimento di WM \_ a un controllo di modifica o una casella combinata per copiare il contenuto corrente degli Appunti nel controllo di modifica in corrispondenza della posizione corrente del punto di inserimento. I dati vengono inseriti solo se gli Appunti contengono dati in \_ formato testo CF.
ms.assetid: 6830b511-986f-46ef-a977-7adedffe86ea
keywords:
- Scambio di dati del messaggio WM_PASTE
topic_type:
- apiref
api_name:
- WM_PASTE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86b723830ecdd0f8b7e3faa9da9adcb51161b297
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400842"
---
# <a name="wm_paste-message"></a><span data-ttu-id="1654c-105">\_Messaggio incolla WM</span><span class="sxs-lookup"><span data-stu-id="1654c-105">WM\_PASTE message</span></span>

<span data-ttu-id="1654c-106">Un'applicazione invia un messaggio di **\_ inserimento di WM** a un controllo di modifica o una casella combinata per copiare il contenuto corrente degli Appunti nel controllo di modifica in corrispondenza della posizione corrente del punto di inserimento.</span><span class="sxs-lookup"><span data-stu-id="1654c-106">An application sends a **WM\_PASTE** message to an edit control or combo box to copy the current content of the clipboard to the edit control at the current caret position.</span></span> <span data-ttu-id="1654c-107">I dati vengono inseriti solo se gli Appunti contengono dati in formato [**\_ testo CF**](standard-clipboard-formats.md) .</span><span class="sxs-lookup"><span data-stu-id="1654c-107">Data is inserted only if the clipboard contains data in [**CF\_TEXT**](standard-clipboard-formats.md) format.</span></span>


```C++
#define WM_PASTE                        0x0302
```



## <a name="parameters"></a><span data-ttu-id="1654c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="1654c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1654c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1654c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1654c-110">Questo parametro non viene utilizzato e deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="1654c-110">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="1654c-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1654c-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1654c-112">Questo parametro non viene utilizzato e deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="1654c-112">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1654c-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1654c-113">Return value</span></span>

<span data-ttu-id="1654c-114">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="1654c-114">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1654c-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="1654c-115">Remarks</span></span>

<span data-ttu-id="1654c-116">Quando viene inviato a una casella combinata, il messaggio di **\_ copia di WM** viene gestito dal controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="1654c-116">When sent to a combo box, the **WM\_PASTE** message is handled by its edit control.</span></span> <span data-ttu-id="1654c-117">Questo messaggio non ha alcun effetto quando viene inviato a una casella combinata con lo stile [**\_ DropDownList CBS**](../controls/combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="1654c-117">This message has no effect when sent to a combo box with the [**CBS\_DROPDOWNLIST**](../controls/combo-box-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="1654c-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1654c-118">Requirements</span></span>



| <span data-ttu-id="1654c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="1654c-119">Requirement</span></span> | <span data-ttu-id="1654c-120">Valore</span><span class="sxs-lookup"><span data-stu-id="1654c-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1654c-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1654c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1654c-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1654c-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="1654c-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1654c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1654c-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1654c-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1654c-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1654c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="1654c-126"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1654c-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1654c-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1654c-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="1654c-128">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="1654c-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1654c-129">**chiaro di WM \_**</span><span class="sxs-lookup"><span data-stu-id="1654c-129">**WM\_CLEAR**</span></span>](wm-clear.md)
</dt> <dt>

[<span data-ttu-id="1654c-130">**\_copia WM**</span><span class="sxs-lookup"><span data-stu-id="1654c-130">**WM\_COPY**</span></span>](wm-copy.md)
</dt> <dt>

[<span data-ttu-id="1654c-131">**\_taglia WM**</span><span class="sxs-lookup"><span data-stu-id="1654c-131">**WM\_CUT**</span></span>](wm-cut.md)
</dt> <dt>

[<span data-ttu-id="1654c-132">**\_annullamento WM**</span><span class="sxs-lookup"><span data-stu-id="1654c-132">**WM\_UNDO**</span></span>](/windows/desktop/Controls/wm-undo)
</dt> <dt>

<span data-ttu-id="1654c-133">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="1654c-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="1654c-134">Appunti</span><span class="sxs-lookup"><span data-stu-id="1654c-134">Clipboard</span></span>](clipboard.md)
</dt> </dl>

 

