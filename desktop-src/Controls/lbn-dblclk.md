---
title: Codice di notifica LBN_DBLCLK (winuser. h)
description: Notifica all'applicazione che l'utente ha fatto doppio clic su un elemento in una casella di riepilogo. La finestra padre della casella di riepilogo riceve questo codice di notifica tramite il \_ messaggio di comando WM.
ms.assetid: 487282cb-833a-4123-987e-6a417fbd09d4
keywords:
- Controlli di Windows per il codice di notifica LBN_DBLCLK
topic_type:
- apiref
api_name:
- LBN_DBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a60623aafb287f2006d9e27da49d0df34c05b05
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743010"
---
# <a name="lbn_dblclk-notification-code"></a><span data-ttu-id="d2076-105">\_Codice di notifica DBLCLK di LBN</span><span class="sxs-lookup"><span data-stu-id="d2076-105">LBN\_DBLCLK notification code</span></span>

<span data-ttu-id="d2076-106">Notifica all'applicazione che l'utente ha fatto doppio clic su un elemento in una casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="d2076-106">Notifies the application that the user has double-clicked an item in a list box.</span></span> <span data-ttu-id="d2076-107">La finestra padre della casella di riepilogo riceve questo codice di notifica tramite il messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="d2076-107">The parent window of the list box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
LBN_DBLCLK

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="d2076-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d2076-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2076-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d2076-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d2076-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene l'identificatore della casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="d2076-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the list box.</span></span> <span data-ttu-id="d2076-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica il codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="d2076-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="d2076-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d2076-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d2076-113">Handle per la casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="d2076-113">Handle to the list box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d2076-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="d2076-114">Remarks</span></span>

<span data-ttu-id="d2076-115">Questo codice di notifica viene inviato solo da una casella di riepilogo con stile [**di \_ notifica L BS**](button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="d2076-115">This notification code is sent only by a list box that has the L [**BS\_NOTIFY**](button-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2076-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d2076-116">Requirements</span></span>



| <span data-ttu-id="d2076-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2076-117">Requirement</span></span> | <span data-ttu-id="d2076-118">Valore</span><span class="sxs-lookup"><span data-stu-id="d2076-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2076-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d2076-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d2076-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d2076-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d2076-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d2076-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d2076-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d2076-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d2076-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d2076-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2076-124"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d2076-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2076-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d2076-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="d2076-126">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="d2076-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d2076-127">\_selChange LBN</span><span class="sxs-lookup"><span data-stu-id="d2076-127">LBN\_SELCHANGE</span></span>](lbn-selchange.md)
</dt> <dt>

<span data-ttu-id="d2076-128">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="d2076-128">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="d2076-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d2076-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="d2076-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d2076-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="d2076-131">**\_comando WM**</span><span class="sxs-lookup"><span data-stu-id="d2076-131">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

