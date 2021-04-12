---
title: Codice di notifica LBN_ERRSPACE (winuser. h)
description: Notifica all'applicazione che la casella di riepilogo non può allocare memoria sufficiente per soddisfare una richiesta specifica. La finestra padre della casella di riepilogo riceve questo codice di notifica tramite il \_ messaggio di comando WM.
ms.assetid: ff716ad0-cbd8-4ac3-bcaf-d5be81355eaa
keywords:
- Controlli di Windows per il codice di notifica LBN_ERRSPACE
topic_type:
- apiref
api_name:
- LBN_ERRSPACE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d324b17a83e38a9b3592be71720486910e88689d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104225225"
---
# <a name="lbn_errspace-notification-code"></a><span data-ttu-id="e8a6b-105">\_Codice di notifica ERRSPACE di LBN</span><span class="sxs-lookup"><span data-stu-id="e8a6b-105">LBN\_ERRSPACE notification code</span></span>

<span data-ttu-id="e8a6b-106">Notifica all'applicazione che la casella di riepilogo non può allocare memoria sufficiente per soddisfare una richiesta specifica.</span><span class="sxs-lookup"><span data-stu-id="e8a6b-106">Notifies the application that the list box cannot allocate enough memory to meet a specific request.</span></span> <span data-ttu-id="e8a6b-107">La finestra padre della casella di riepilogo riceve questo codice di notifica tramite il messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="e8a6b-107">The parent window of the list box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
LBN_ERRSPACE

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="e8a6b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e8a6b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8a6b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e8a6b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e8a6b-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene l'identificatore della casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="e8a6b-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the list box.</span></span> <span data-ttu-id="e8a6b-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica il codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="e8a6b-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="e8a6b-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e8a6b-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e8a6b-113">Handle per la casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="e8a6b-113">Handle to the list box.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e8a6b-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e8a6b-114">Requirements</span></span>



| <span data-ttu-id="e8a6b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8a6b-115">Requirement</span></span> | <span data-ttu-id="e8a6b-116">Valore</span><span class="sxs-lookup"><span data-stu-id="e8a6b-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8a6b-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e8a6b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e8a6b-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e8a6b-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e8a6b-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e8a6b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e8a6b-120">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e8a6b-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e8a6b-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e8a6b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8a6b-122"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e8a6b-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8a6b-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e8a6b-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="e8a6b-124">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="e8a6b-124">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="e8a6b-125">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e8a6b-125">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="e8a6b-126">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e8a6b-126">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="e8a6b-127">**\_comando WM**</span><span class="sxs-lookup"><span data-stu-id="e8a6b-127">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

