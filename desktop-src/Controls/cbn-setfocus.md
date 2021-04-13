---
title: Codice di notifica CBN_SETFOCUS (winuser. h)
description: Inviato quando una casella combinata riceve lo stato attivo della tastiera. La finestra padre della casella combinata riceve questo codice di notifica tramite il \_ messaggio di comando WM.
ms.assetid: 8072edc6-aedc-4daf-80df-d3acd82fcffa
keywords:
- Controlli di Windows per il codice di notifica CBN_SETFOCUS
topic_type:
- apiref
api_name:
- CBN_SETFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 885bbaebac0a79fc600cbcc2b7864cbdfd19ea93
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341382"
---
# <a name="cbn_setfocus-notification-code"></a><span data-ttu-id="9b446-105">Codice di notifica per la \_ messa a fuoco CBN</span><span class="sxs-lookup"><span data-stu-id="9b446-105">CBN\_SETFOCUS notification code</span></span>

<span data-ttu-id="9b446-106">Inviato quando una casella combinata riceve lo stato attivo della tastiera.</span><span class="sxs-lookup"><span data-stu-id="9b446-106">Sent when a combo box receives the keyboard focus.</span></span> <span data-ttu-id="9b446-107">La finestra padre della casella combinata riceve questo codice di notifica tramite il messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="9b446-107">The parent window of the combo box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
CBN_SETFOCUS

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="9b446-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="9b446-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b446-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9b446-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9b446-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene l'identificatore di controllo della casella combinata.</span><span class="sxs-lookup"><span data-stu-id="9b446-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the control identifier of the combo box.</span></span> <span data-ttu-id="9b446-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica il codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="9b446-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="9b446-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9b446-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9b446-113">Handle per la casella combinata.</span><span class="sxs-lookup"><span data-stu-id="9b446-113">Handle to the combo box.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9b446-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9b446-114">Requirements</span></span>



| <span data-ttu-id="9b446-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b446-115">Requirement</span></span> | <span data-ttu-id="9b446-116">Valore</span><span class="sxs-lookup"><span data-stu-id="9b446-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b446-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9b446-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9b446-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9b446-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="9b446-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9b446-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9b446-120">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9b446-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9b446-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9b446-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b446-122"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9b446-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b446-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9b446-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="9b446-124">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="9b446-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9b446-125">\_KILLFOCUS CBN</span><span class="sxs-lookup"><span data-stu-id="9b446-125">CBN\_KILLFOCUS</span></span>](cbn-killfocus.md)
</dt> <dt>

<span data-ttu-id="9b446-126">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="9b446-126">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="9b446-127">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9b446-127">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="9b446-128">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9b446-128">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="9b446-129">**\_comando WM**</span><span class="sxs-lookup"><span data-stu-id="9b446-129">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

