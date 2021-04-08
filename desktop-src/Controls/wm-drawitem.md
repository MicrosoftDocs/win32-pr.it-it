---
title: Messaggio WM_DRAWITEM (winuser. h)
description: Inviato alla finestra padre di un pulsante creato dal proprietario, una casella combinata, una casella di riepilogo o un menu quando viene modificato un aspetto visivo del pulsante, della casella combinata, della casella di riepilogo o del menu.
ms.assetid: e54bae5e-10d6-43b0-a766-1b270c8873a9
keywords:
- Controlli di Windows Message WM_DRAWITEM
topic_type:
- apiref
api_name:
- WM_DRAWITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5bd6465a560a0590ed9f5b483afae4c0d72d637
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741362"
---
# <a name="wm_drawitem-message"></a><span data-ttu-id="81886-104">Messaggio di WM \_ DrawItem</span><span class="sxs-lookup"><span data-stu-id="81886-104">WM\_DRAWITEM message</span></span>

<span data-ttu-id="81886-105">Inviato alla finestra padre di un pulsante creato dal proprietario, una casella combinata, una casella di riepilogo o un menu quando viene modificato un aspetto visivo del pulsante, della casella combinata, della casella di riepilogo o del menu.</span><span class="sxs-lookup"><span data-stu-id="81886-105">Sent to the parent window of an owner-drawn button, combo box, list box, or menu when a visual aspect of the button, combo box, list box, or menu has changed.</span></span>

<span data-ttu-id="81886-106">Una finestra riceve questo messaggio tramite la funzione [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="81886-106">A window receives this message through its [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
WM_DRAWITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="81886-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="81886-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81886-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="81886-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="81886-109">Specifica l'identificatore del controllo che ha inviato il messaggio **WM \_ DrawItem** .</span><span class="sxs-lookup"><span data-stu-id="81886-109">Specifies the identifier of the control that sent the **WM\_DRAWITEM** message.</span></span> <span data-ttu-id="81886-110">Se il messaggio è stato inviato da un menu, questo parametro è zero.</span><span class="sxs-lookup"><span data-stu-id="81886-110">If the message was sent by a menu, this parameter is zero.</span></span>

</dd> <dt>

<span data-ttu-id="81886-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="81886-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="81886-112">Puntatore a una struttura [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) contenente le informazioni sull'elemento da disegnare e il tipo di disegno necessario.</span><span class="sxs-lookup"><span data-stu-id="81886-112">Pointer to a [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure containing information about the item to be drawn and the type of drawing required.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81886-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="81886-113">Return value</span></span>

<span data-ttu-id="81886-114">Se un'applicazione elabora il messaggio, deve restituire **true**.</span><span class="sxs-lookup"><span data-stu-id="81886-114">If an application processes this message, it should return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="81886-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="81886-115">Remarks</span></span>

<span data-ttu-id="81886-116">Per impostazione predefinita, la funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) disegna il rettangolo di attivazione per un elemento della casella di riepilogo creato dal proprietario.</span><span class="sxs-lookup"><span data-stu-id="81886-116">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function draws the focus rectangle for an owner-drawn list box item.</span></span>

<span data-ttu-id="81886-117">Il membro *itemAction* della struttura [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) specifica l'operazione di disegno che deve essere eseguita da un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="81886-117">The *itemAction* member of the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure specifies the drawing operation that an application should perform.</span></span>

<span data-ttu-id="81886-118">Prima di restituire l'elaborazione di questo messaggio, un'applicazione deve garantire che il contesto di dispositivo identificato dal membro *HDC* della struttura [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) sia nello stato predefinito.</span><span class="sxs-lookup"><span data-stu-id="81886-118">Before returning from processing this message, an application should ensure that the device context identified by the *hDC* member of the [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) structure is in the default state.</span></span>

## <a name="requirements"></a><span data-ttu-id="81886-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="81886-119">Requirements</span></span>



| <span data-ttu-id="81886-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="81886-120">Requirement</span></span> | <span data-ttu-id="81886-121">Valore</span><span class="sxs-lookup"><span data-stu-id="81886-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81886-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="81886-122">Minimum supported client</span></span><br/> | <span data-ttu-id="81886-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="81886-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="81886-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="81886-124">Minimum supported server</span></span><br/> | <span data-ttu-id="81886-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="81886-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="81886-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="81886-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="81886-127"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="81886-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81886-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="81886-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="81886-129">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="81886-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="81886-130">**DRAWITEMSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="81886-130">**DRAWITEMSTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-drawitemstruct)
</dt> <dt>

<span data-ttu-id="81886-131">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="81886-131">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="81886-132">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="81886-132">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> </dl>

 

