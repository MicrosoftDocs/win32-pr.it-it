---
title: Messaggio WM_COPY (winuser. h)
description: Un'applicazione invia il \_ messaggio di copia WM a una casella combinata o un controllo di modifica per copiare la selezione corrente negli Appunti nel \_ formato di testo CF.
ms.assetid: dcac3ad3-1e70-4b71-accd-261587224e60
keywords:
- Scambio di dati del messaggio WM_COPY
topic_type:
- apiref
api_name:
- WM_COPY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b298248d75b1d25d1bfef8347347fe2f1a6c7916
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "106320823"
---
# <a name="wm_copy-message"></a><span data-ttu-id="3e693-104">\_Messaggio copia WM</span><span class="sxs-lookup"><span data-stu-id="3e693-104">WM\_COPY message</span></span>

<span data-ttu-id="3e693-105">Un'applicazione invia il messaggio di **\_ copia WM** a una casella combinata o un controllo di modifica per copiare la selezione corrente negli Appunti nel formato di [**\_ testo CF**](standard-clipboard-formats.md) .</span><span class="sxs-lookup"><span data-stu-id="3e693-105">An application sends the **WM\_COPY** message to an edit control or combo box to copy the current selection to the clipboard in [**CF\_TEXT**](standard-clipboard-formats.md) format.</span></span>


```C++
#define WM_COPY                         0x0301
```



## <a name="parameters"></a><span data-ttu-id="3e693-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3e693-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e693-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3e693-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3e693-108">Questo parametro non viene utilizzato e deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="3e693-108">This parameter is not used and must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="3e693-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3e693-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3e693-110">Questo parametro non viene utilizzato e deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="3e693-110">This parameter is not used and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e693-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3e693-111">Return value</span></span>

<span data-ttu-id="3e693-112">Restituisce un valore diverso da zero in caso di esito positivo, altrimenti zero.</span><span class="sxs-lookup"><span data-stu-id="3e693-112">Returns nonzero value on success, else zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e693-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="3e693-113">Remarks</span></span>

<span data-ttu-id="3e693-114">Quando viene inviato a una casella combinata, il messaggio di **\_ copia WM** viene gestito dal controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="3e693-114">When sent to a combo box, the **WM\_COPY** message is handled by its edit control.</span></span> <span data-ttu-id="3e693-115">Questo messaggio non ha alcun effetto quando viene inviato a una casella combinata con lo stile [**\_ DropDownList CBS**](../controls/combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="3e693-115">This message has no effect when sent to a combo box with the [**CBS\_DROPDOWNLIST**](../controls/combo-box-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e693-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3e693-116">Requirements</span></span>



| <span data-ttu-id="3e693-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e693-117">Requirement</span></span> | <span data-ttu-id="3e693-118">Valore</span><span class="sxs-lookup"><span data-stu-id="3e693-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e693-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3e693-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3e693-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3e693-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="3e693-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3e693-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3e693-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3e693-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3e693-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3e693-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e693-124"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3e693-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e693-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3e693-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="3e693-126">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="3e693-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3e693-127">**chiaro di WM \_**</span><span class="sxs-lookup"><span data-stu-id="3e693-127">**WM\_CLEAR**</span></span>](wm-clear.md)
</dt> <dt>

[<span data-ttu-id="3e693-128">**\_taglia WM**</span><span class="sxs-lookup"><span data-stu-id="3e693-128">**WM\_CUT**</span></span>](wm-cut.md)
</dt> <dt>

[<span data-ttu-id="3e693-129">**\_Incolla WM**</span><span class="sxs-lookup"><span data-stu-id="3e693-129">**WM\_PASTE**</span></span>](wm-paste.md)
</dt> <dt>

[<span data-ttu-id="3e693-130">**\_annullamento WM**</span><span class="sxs-lookup"><span data-stu-id="3e693-130">**WM\_UNDO**</span></span>](/windows/desktop/Controls/wm-undo)
</dt> <dt>

<span data-ttu-id="3e693-131">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="3e693-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="3e693-132">Appunti</span><span class="sxs-lookup"><span data-stu-id="3e693-132">Clipboard</span></span>](clipboard.md)
</dt> </dl>

 

