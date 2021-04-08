---
title: Codice di notifica STN_DBLCLK (winuser. h)
description: Il codice di notifica di STN \_ DBLCLK viene inviato quando l'utente fa doppio clic su un controllo statico con \_ stile di notifica SS. La finestra padre del controllo riceve questo codice di notifica tramite il \_ messaggio di comando WM.
ms.assetid: e3203309-87ea-46f4-9269-7e68c6fa0e4a
keywords:
- Controlli di Windows per il codice di notifica STN_DBLCLK
topic_type:
- apiref
api_name:
- STN_DBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 853ed5142de99dc85b729b4c4ea208273d4ace1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048065"
---
# <a name="stn_dblclk-notification-code"></a><span data-ttu-id="14684-105">Codice di notifica di STN \_ DBLCLK</span><span class="sxs-lookup"><span data-stu-id="14684-105">STN\_DBLCLK notification code</span></span>

<span data-ttu-id="14684-106">Il codice di notifica di STN \_ DBLCLK viene inviato quando l'utente fa doppio clic su un controllo statico con stile di [**\_ notifica SS**](static-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="14684-106">The STN\_DBLCLK notification code is sent when the user double-clicks a static control that has the [**SS\_NOTIFY**](static-control-styles.md) style.</span></span> <span data-ttu-id="14684-107">La finestra padre del controllo riceve questo codice di notifica tramite il messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="14684-107">The parent window of the control receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
STN_DBLCLK

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="14684-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="14684-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14684-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="14684-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="14684-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene l'identificatore del controllo statico.</span><span class="sxs-lookup"><span data-stu-id="14684-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the static control.</span></span> <span data-ttu-id="14684-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica il codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="14684-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="14684-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="14684-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="14684-113">Handle per il controllo statico.</span><span class="sxs-lookup"><span data-stu-id="14684-113">Handle to the static control.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="14684-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="14684-114">Requirements</span></span>



| <span data-ttu-id="14684-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="14684-115">Requirement</span></span> | <span data-ttu-id="14684-116">Valore</span><span class="sxs-lookup"><span data-stu-id="14684-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14684-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="14684-117">Minimum supported client</span></span><br/> | <span data-ttu-id="14684-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="14684-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="14684-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="14684-119">Minimum supported server</span></span><br/> | <span data-ttu-id="14684-120">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="14684-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="14684-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="14684-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="14684-122"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="14684-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14684-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="14684-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="14684-124">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="14684-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="14684-125">STN \_ selezionato</span><span class="sxs-lookup"><span data-stu-id="14684-125">STN\_CLICKED</span></span>](stn-clicked.md)
</dt> <dt>

<span data-ttu-id="14684-126">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="14684-126">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="14684-127">Controlli statici</span><span class="sxs-lookup"><span data-stu-id="14684-127">Static Controls</span></span>](static-controls.md)
</dt> <dt>

<span data-ttu-id="14684-128">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="14684-128">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="14684-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="14684-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="14684-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="14684-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="14684-131">**\_comando WM**</span><span class="sxs-lookup"><span data-stu-id="14684-131">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

