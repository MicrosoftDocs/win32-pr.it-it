---
title: Codice di notifica CBN_KILLFOCUS (winuser. h)
description: Inviato quando una casella combinata perde lo stato attivo della tastiera. La finestra padre della casella combinata riceve questo codice di notifica tramite il \_ messaggio di comando WM.
ms.assetid: 0118a2ff-9811-4bf1-b3f6-1d00ca5c8dbe
keywords:
- Controlli di Windows per il codice di notifica CBN_KILLFOCUS
topic_type:
- apiref
api_name:
- CBN_KILLFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e266824bf8bcdac1fb901d40ca2b15406fc79660
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302644"
---
# <a name="cbn_killfocus-notification-code"></a><span data-ttu-id="010dd-105">\_Codice di notifica KILLFOCUS CBN</span><span class="sxs-lookup"><span data-stu-id="010dd-105">CBN\_KILLFOCUS notification code</span></span>

<span data-ttu-id="010dd-106">Inviato quando una casella combinata perde lo stato attivo della tastiera.</span><span class="sxs-lookup"><span data-stu-id="010dd-106">Sent when a combo box loses the keyboard focus.</span></span> <span data-ttu-id="010dd-107">La finestra padre della casella combinata riceve questo codice di notifica tramite il messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="010dd-107">The parent window of the combo box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
CBN_KILLFOCUS

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="010dd-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="010dd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="010dd-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="010dd-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="010dd-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene l'identificatore di controllo della casella combinata.</span><span class="sxs-lookup"><span data-stu-id="010dd-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the control identifier of the combo box.</span></span> <span data-ttu-id="010dd-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica il codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="010dd-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="010dd-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="010dd-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="010dd-113">Handle per la casella combinata.</span><span class="sxs-lookup"><span data-stu-id="010dd-113">Handle to the combo box.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="010dd-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="010dd-114">Requirements</span></span>



| <span data-ttu-id="010dd-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="010dd-115">Requirement</span></span> | <span data-ttu-id="010dd-116">Valore</span><span class="sxs-lookup"><span data-stu-id="010dd-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="010dd-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="010dd-117">Minimum supported client</span></span><br/> | <span data-ttu-id="010dd-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="010dd-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="010dd-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="010dd-119">Minimum supported server</span></span><br/> | <span data-ttu-id="010dd-120">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="010dd-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="010dd-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="010dd-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="010dd-122"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="010dd-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="010dd-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="010dd-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="010dd-124">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="010dd-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="010dd-125">\_stato attivo CBN</span><span class="sxs-lookup"><span data-stu-id="010dd-125">CBN\_SETFOCUS</span></span>](cbn-setfocus.md)
</dt> <dt>

<span data-ttu-id="010dd-126">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="010dd-126">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="010dd-127">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="010dd-127">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="010dd-128">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="010dd-128">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="010dd-129">**\_comando WM**</span><span class="sxs-lookup"><span data-stu-id="010dd-129">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

