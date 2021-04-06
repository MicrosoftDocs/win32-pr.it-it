---
description: Imposta il testo di una finestra.
ms.assetid: 1b48c309-6903-4139-bf42-e8526963e681
title: Messaggio WM_SETTEXT (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3284855d817d5207b0d7572a41774e961c0113f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759494"
---
# <a name="wm_settext-message"></a><span data-ttu-id="80090-103">\_Messaggio di testo WM</span><span class="sxs-lookup"><span data-stu-id="80090-103">WM\_SETTEXT message</span></span>

<span data-ttu-id="80090-104">Imposta il testo di una finestra.</span><span class="sxs-lookup"><span data-stu-id="80090-104">Sets the text of a window.</span></span>


```C++
#define WM_SETTEXT                      0x000C
```



## <a name="parameters"></a><span data-ttu-id="80090-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="80090-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80090-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="80090-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="80090-107">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="80090-107">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="80090-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="80090-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="80090-109">Puntatore a una stringa con terminazione null che rappresenta il testo della finestra.</span><span class="sxs-lookup"><span data-stu-id="80090-109">A pointer to a null-terminated string that is the window text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80090-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="80090-110">Return value</span></span>

<span data-ttu-id="80090-111">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="80090-111">Type: **LRESULT**</span></span>

<span data-ttu-id="80090-112">Il valore restituito è **true** se il testo è impostato.</span><span class="sxs-lookup"><span data-stu-id="80090-112">The return value is **TRUE** if the text is set.</span></span> <span data-ttu-id="80090-113">È **false** (per un controllo di modifica), **lb \_ ERRSPACE** (per una casella di riepilogo) o **CB \_ ERRSPACE** (per una casella combinata) se è disponibile spazio insufficiente per impostare il testo nel controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="80090-113">It is **FALSE** (for an edit control), **LB\_ERRSPACE** (for a list box), or **CB\_ERRSPACE** (for a combo box) if insufficient space is available to set the text in the edit control.</span></span> <span data-ttu-id="80090-114">È **CB \_ Err** se questo messaggio viene inviato a una casella combinata senza un controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="80090-114">It is **CB\_ERR** if this message is sent to a combo box without an edit control.</span></span>

## <a name="remarks"></a><span data-ttu-id="80090-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="80090-115">Remarks</span></span>

<span data-ttu-id="80090-116">La funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) imposta e visualizza il testo della finestra.</span><span class="sxs-lookup"><span data-stu-id="80090-116">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function sets and displays the window text.</span></span> <span data-ttu-id="80090-117">Per un controllo di modifica, il testo è il contenuto del controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="80090-117">For an edit control, the text is the contents of the edit control.</span></span> <span data-ttu-id="80090-118">Per una casella combinata, il testo è il contenuto della parte relativa al controllo di modifica della casella combinata.</span><span class="sxs-lookup"><span data-stu-id="80090-118">For a combo box, the text is the contents of the edit-control portion of the combo box.</span></span> <span data-ttu-id="80090-119">Per un pulsante, il testo è il nome del pulsante.</span><span class="sxs-lookup"><span data-stu-id="80090-119">For a button, the text is the button name.</span></span> <span data-ttu-id="80090-120">Per le altre finestre, il testo è il titolo della finestra.</span><span class="sxs-lookup"><span data-stu-id="80090-120">For other windows, the text is the window title.</span></span>

<span data-ttu-id="80090-121">Questo messaggio non modifica la selezione corrente nella casella di riepilogo di una casella combinata.</span><span class="sxs-lookup"><span data-stu-id="80090-121">This message does not change the current selection in the list box of a combo box.</span></span> <span data-ttu-id="80090-122">Un'applicazione deve usare il messaggio [**CB \_ SELECTSTRING**](../controls/cb-selectstring.md) per selezionare l'elemento in una casella di riepilogo che corrisponde al testo nel controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="80090-122">An application should use the [**CB\_SELECTSTRING**](../controls/cb-selectstring.md) message to select the item in a list box that matches the text in the edit control.</span></span>

## <a name="requirements"></a><span data-ttu-id="80090-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="80090-123">Requirements</span></span>



| <span data-ttu-id="80090-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="80090-124">Requirement</span></span> | <span data-ttu-id="80090-125">Valore</span><span class="sxs-lookup"><span data-stu-id="80090-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80090-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="80090-126">Minimum supported client</span></span><br/> | <span data-ttu-id="80090-127">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="80090-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="80090-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="80090-128">Minimum supported server</span></span><br/> | <span data-ttu-id="80090-129">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="80090-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="80090-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="80090-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="80090-131"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="80090-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80090-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="80090-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="80090-133">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="80090-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="80090-134">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="80090-134">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="80090-135">**WM \_ GETtext**</span><span class="sxs-lookup"><span data-stu-id="80090-135">**WM\_GETTEXT**</span></span>](wm-gettext.md)
</dt> <dt>

<span data-ttu-id="80090-136">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="80090-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="80090-137">Windows</span><span class="sxs-lookup"><span data-stu-id="80090-137">Windows</span></span>](windows.md)
</dt> <dt>

<span data-ttu-id="80090-138">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="80090-138">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="80090-139">**CB \_ SELECTSTRING**</span><span class="sxs-lookup"><span data-stu-id="80090-139">**CB\_SELECTSTRING**</span></span>](../controls/cb-selectstring.md)
</dt> </dl>

 

 
