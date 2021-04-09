---
title: Codice di notifica LBN_KILLFOCUS (winuser. h)
description: Notifica all'applicazione che la casella di riepilogo ha perso lo stato attivo della tastiera. La finestra padre della casella di riepilogo riceve questo codice di notifica tramite il \_ messaggio di comando WM.
ms.assetid: ef927b56-3c46-4ae7-87df-13295cf175a8
keywords:
- Controlli di Windows per il codice di notifica LBN_KILLFOCUS
topic_type:
- apiref
api_name:
- LBN_KILLFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba424efc2518d359c3d031561aeafee8c0348b65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120995"
---
# <a name="lbn_killfocus-notification-code"></a><span data-ttu-id="c6d57-105">\_Codice di notifica KILLFOCUS di LBN</span><span class="sxs-lookup"><span data-stu-id="c6d57-105">LBN\_KILLFOCUS notification code</span></span>

<span data-ttu-id="c6d57-106">Notifica all'applicazione che la casella di riepilogo ha perso lo stato attivo della tastiera.</span><span class="sxs-lookup"><span data-stu-id="c6d57-106">Notifies the application that the list box has lost the keyboard focus.</span></span> <span data-ttu-id="c6d57-107">La finestra padre della casella di riepilogo riceve questo codice di notifica tramite il messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="c6d57-107">The parent window of the list box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
LBN_KILLFOCUS

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="c6d57-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="c6d57-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6d57-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c6d57-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c6d57-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene l'identificatore della casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="c6d57-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the list box.</span></span> <span data-ttu-id="c6d57-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica il codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="c6d57-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="c6d57-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c6d57-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c6d57-113">Handle per la casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="c6d57-113">Handle to the list box.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c6d57-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c6d57-114">Requirements</span></span>



| <span data-ttu-id="c6d57-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6d57-115">Requirement</span></span> | <span data-ttu-id="c6d57-116">Valore</span><span class="sxs-lookup"><span data-stu-id="c6d57-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6d57-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c6d57-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c6d57-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c6d57-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c6d57-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c6d57-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c6d57-120">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c6d57-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c6d57-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c6d57-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6d57-122"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c6d57-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6d57-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c6d57-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="c6d57-124">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="c6d57-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c6d57-125">LBN \_ SetFocus</span><span class="sxs-lookup"><span data-stu-id="c6d57-125">LBN\_SETFOCUS</span></span>](lbn-setfocus.md)
</dt> <dt>

<span data-ttu-id="c6d57-126">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="c6d57-126">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="c6d57-127">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c6d57-127">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="c6d57-128">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c6d57-128">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="c6d57-129">**\_comando WM**</span><span class="sxs-lookup"><span data-stu-id="c6d57-129">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

