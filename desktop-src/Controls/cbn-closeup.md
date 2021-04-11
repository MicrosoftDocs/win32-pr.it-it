---
title: Codice di notifica CBN_CLOSEUP (winuser. h)
description: Inviato quando la casella di riepilogo di una casella combinata è stata chiusa. La finestra padre della casella combinata riceve questo codice di notifica tramite il \_ messaggio di comando WM.
ms.assetid: 79b2108e-1ef3-433d-a0b0-ac9ad1a93905
keywords:
- Controlli di Windows per il codice di notifica CBN_CLOSEUP
topic_type:
- apiref
api_name:
- CBN_CLOSEUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec67cf68109d32d6e1ad714f91a97987f9a3734d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121614"
---
# <a name="cbn_closeup-notification-code"></a><span data-ttu-id="d3cef-105">\_Codice di notifica primo piano CBN</span><span class="sxs-lookup"><span data-stu-id="d3cef-105">CBN\_CLOSEUP notification code</span></span>

<span data-ttu-id="d3cef-106">Inviato quando la casella di riepilogo di una casella combinata è stata chiusa.</span><span class="sxs-lookup"><span data-stu-id="d3cef-106">Sent when the list box of a combo box has been closed.</span></span> <span data-ttu-id="d3cef-107">La finestra padre della casella combinata riceve questo codice di notifica tramite il messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="d3cef-107">The parent window of the combo box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
CBN_CLOSEUP

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="d3cef-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d3cef-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3cef-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d3cef-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d3cef-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene l'identificatore di controllo della casella combinata.</span><span class="sxs-lookup"><span data-stu-id="d3cef-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the control identifier of the combo box.</span></span> <span data-ttu-id="d3cef-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica il codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="d3cef-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="d3cef-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d3cef-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d3cef-113">Handle per la casella combinata.</span><span class="sxs-lookup"><span data-stu-id="d3cef-113">Handle to the combo box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d3cef-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="d3cef-114">Remarks</span></span>

<span data-ttu-id="d3cef-115">Se l'utente ha modificato la selezione corrente, la casella combinata invia anche il codice di notifica di [CBN \_ selChange](cbn-selchange.md) quando l'elenco a discesa viene chiuso.</span><span class="sxs-lookup"><span data-stu-id="d3cef-115">If the user changed the current selection, the combo box also sends the [CBN\_SELCHANGE](cbn-selchange.md) notification code when the drop-down list closes.</span></span> <span data-ttu-id="d3cef-116">In generale, non è possibile prevedere l'ordine in cui verranno inviati i codici di notifica.</span><span class="sxs-lookup"><span data-stu-id="d3cef-116">In general, you cannot predict the order in which notification codes will be sent.</span></span> <span data-ttu-id="d3cef-117">In particolare, un \_ codice di notifica SelChange CBN può verificarsi prima o dopo un \_ codice di notifica primo piano CBN.</span><span class="sxs-lookup"><span data-stu-id="d3cef-117">In particular, a CBN\_SELCHANGE notification code may occur either before or after a CBN\_CLOSEUP notification code.</span></span>

<span data-ttu-id="d3cef-118">Per eseguire un processo specifico ogni volta che l'utente seleziona una voce di elenco, è possibile gestire il codice di notifica di [CBN \_ selChange](cbn-selchange.md) o CBN \_ closeup.</span><span class="sxs-lookup"><span data-stu-id="d3cef-118">To execute a specific process each time the user selects a list item, you can handle either the [CBN\_SELCHANGE](cbn-selchange.md) or CBN\_CLOSEUP notification code.</span></span> <span data-ttu-id="d3cef-119">In genere, è possibile attendere il \_ codice di notifica primo piano CBN prima di elaborare una modifica nella selezione corrente.</span><span class="sxs-lookup"><span data-stu-id="d3cef-119">Typically, you would wait for the CBN\_CLOSEUP notification code before processing a change in the current selection.</span></span> <span data-ttu-id="d3cef-120">Questo può essere particolarmente importante se è necessaria una quantità significativa di elaborazione.</span><span class="sxs-lookup"><span data-stu-id="d3cef-120">This can be particularly important if a significant amount of processing is required.</span></span>

<span data-ttu-id="d3cef-121">Questo codice di notifica non viene inviato a una casella combinata con stile [**\_ semplice CBS**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="d3cef-121">This notification code is not sent to a combo box that has the [**CBS\_SIMPLE**](combo-box-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3cef-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d3cef-122">Requirements</span></span>



| <span data-ttu-id="d3cef-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3cef-123">Requirement</span></span> | <span data-ttu-id="d3cef-124">Valore</span><span class="sxs-lookup"><span data-stu-id="d3cef-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3cef-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d3cef-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d3cef-126">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d3cef-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d3cef-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d3cef-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d3cef-128">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d3cef-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d3cef-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d3cef-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3cef-130"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d3cef-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3cef-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d3cef-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="d3cef-132">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="d3cef-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d3cef-133">\_elenco a discesa CBN</span><span class="sxs-lookup"><span data-stu-id="d3cef-133">CBN\_DROPDOWN</span></span>](cbn-dropdown.md)
</dt> <dt>

[<span data-ttu-id="d3cef-134">\_selChange CBN</span><span class="sxs-lookup"><span data-stu-id="d3cef-134">CBN\_SELCHANGE</span></span>](cbn-selchange.md)
</dt> <dt>

<span data-ttu-id="d3cef-135">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="d3cef-135">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="d3cef-136">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d3cef-136">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="d3cef-137">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d3cef-137">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="d3cef-138">**\_comando WM**</span><span class="sxs-lookup"><span data-stu-id="d3cef-138">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

