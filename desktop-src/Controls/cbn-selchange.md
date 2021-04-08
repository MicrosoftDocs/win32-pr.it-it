---
title: Codice di notifica CBN_SELCHANGE (winuser. h)
description: Inviato quando l'utente modifica la selezione corrente nella casella di riepilogo di una casella combinata.
ms.assetid: 2d0d711c-dfc4-485b-97bb-9ccfa7c5864b
keywords:
- Controlli di Windows per il codice di notifica CBN_SELCHANGE
topic_type:
- apiref
api_name:
- CBN_SELCHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e921b7856780763923a448e42de072476cc02f6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964942"
---
# <a name="cbn_selchange-notification-code"></a><span data-ttu-id="7d2ed-104">\_Codice di notifica SelChange CBN</span><span class="sxs-lookup"><span data-stu-id="7d2ed-104">CBN\_SELCHANGE notification code</span></span>

<span data-ttu-id="7d2ed-105">Inviato quando l'utente modifica la selezione corrente nella casella di riepilogo di una casella combinata.</span><span class="sxs-lookup"><span data-stu-id="7d2ed-105">Sent when the user changes the current selection in the list box of a combo box.</span></span> <span data-ttu-id="7d2ed-106">L'utente può modificare la selezione facendo clic nella casella di riepilogo o usando i tasti di direzione.</span><span class="sxs-lookup"><span data-stu-id="7d2ed-106">The user can change the selection by clicking in the list box or by using the arrow keys.</span></span> <span data-ttu-id="7d2ed-107">La finestra padre della casella combinata riceve questo codice di notifica sotto forma di un messaggio [**di \_ comando WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="7d2ed-107">The parent window of the combo box receives this notification code in the form of a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
CBN_SELCHANGE

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="7d2ed-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7d2ed-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d2ed-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7d2ed-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7d2ed-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene l'identificatore di controllo della casella combinata.</span><span class="sxs-lookup"><span data-stu-id="7d2ed-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the control identifier of the combo box.</span></span> <span data-ttu-id="7d2ed-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica il codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="7d2ed-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="7d2ed-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7d2ed-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7d2ed-113">Handle per la casella combinata.</span><span class="sxs-lookup"><span data-stu-id="7d2ed-113">Handle to the combo box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7d2ed-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="7d2ed-114">Remarks</span></span>

<span data-ttu-id="7d2ed-115">Per ottenere l'indice della selezione corrente, inviare il messaggio del [**CB \_ GetCurSel**](cb-getcursel.md) al controllo.</span><span class="sxs-lookup"><span data-stu-id="7d2ed-115">To get the index of the current selection, send the [**CB\_GETCURSEL**](cb-getcursel.md) message to the control.</span></span>

<span data-ttu-id="7d2ed-116">Il codice di notifica di CBN \_ selChange non viene inviato quando la selezione corrente viene impostata usando il messaggio di [**\_ malmaledizione CB**](cb-setcursel.md) .</span><span class="sxs-lookup"><span data-stu-id="7d2ed-116">The CBN\_SELCHANGE notification code is not sent when the current selection is set using the [**CB\_SETCURSEL**](cb-setcursel.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d2ed-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7d2ed-117">Requirements</span></span>



| <span data-ttu-id="7d2ed-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d2ed-118">Requirement</span></span> | <span data-ttu-id="7d2ed-119">Valore</span><span class="sxs-lookup"><span data-stu-id="7d2ed-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d2ed-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7d2ed-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7d2ed-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7d2ed-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7d2ed-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7d2ed-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7d2ed-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7d2ed-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7d2ed-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7d2ed-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d2ed-125"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7d2ed-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d2ed-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7d2ed-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="7d2ed-127">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="7d2ed-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7d2ed-128">primo piano CBN \_</span><span class="sxs-lookup"><span data-stu-id="7d2ed-128">CBN\_CLOSEUP</span></span>](cbn-closeup.md)
</dt> <dt>

[<span data-ttu-id="7d2ed-129">\_DBLCLK CBN</span><span class="sxs-lookup"><span data-stu-id="7d2ed-129">CBN\_DBLCLK</span></span>](cbn-dblclk.md)
</dt> <dt>

[<span data-ttu-id="7d2ed-130">**CB \_ GETcursel**</span><span class="sxs-lookup"><span data-stu-id="7d2ed-130">**CB\_GETCURSEL**</span></span>](cb-getcursel.md)
</dt> <dt>

[<span data-ttu-id="7d2ed-131">**\_CAcursel CB**</span><span class="sxs-lookup"><span data-stu-id="7d2ed-131">**CB\_SETCURSEL**</span></span>](cb-setcursel.md)
</dt> <dt>

<span data-ttu-id="7d2ed-132">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="7d2ed-132">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="7d2ed-133">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7d2ed-133">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="7d2ed-134">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7d2ed-134">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="7d2ed-135">**\_comando WM**</span><span class="sxs-lookup"><span data-stu-id="7d2ed-135">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

