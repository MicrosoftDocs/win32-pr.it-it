---
title: Codice di notifica CBN_ERRSPACE (winuser. h)
description: Inviato quando una casella combinata non è in grado di allocare memoria sufficiente per soddisfare una richiesta specifica. La finestra padre della casella combinata riceve questo codice di notifica tramite il \_ messaggio di comando WM.
ms.assetid: c1c19c40-fc88-47d0-9676-7a267a48ae98
keywords:
- Controlli di Windows per il codice di notifica CBN_ERRSPACE
topic_type:
- apiref
api_name:
- CBN_ERRSPACE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d74e46e4435a03a0233ce6591d3c36cefb4d880a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121506"
---
# <a name="cbn_errspace-notification-code"></a><span data-ttu-id="513f1-105">\_Codice di notifica ERRSPACE CBN</span><span class="sxs-lookup"><span data-stu-id="513f1-105">CBN\_ERRSPACE notification code</span></span>

<span data-ttu-id="513f1-106">Inviato quando una casella combinata non è in grado di allocare memoria sufficiente per soddisfare una richiesta specifica.</span><span class="sxs-lookup"><span data-stu-id="513f1-106">Sent when a combo box cannot allocate enough memory to meet a specific request.</span></span> <span data-ttu-id="513f1-107">La finestra padre della casella combinata riceve questo codice di notifica tramite il messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="513f1-107">The parent window of the combo box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
CBN_ERRSPACE

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="513f1-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="513f1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="513f1-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="513f1-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="513f1-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene l'identificatore di controllo della casella combinata.</span><span class="sxs-lookup"><span data-stu-id="513f1-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the control identifier of the combo box.</span></span> <span data-ttu-id="513f1-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica il codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="513f1-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="513f1-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="513f1-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="513f1-113">Handle per la casella combinata.</span><span class="sxs-lookup"><span data-stu-id="513f1-113">Handle to the combo box.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="513f1-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="513f1-114">Requirements</span></span>



| <span data-ttu-id="513f1-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="513f1-115">Requirement</span></span> | <span data-ttu-id="513f1-116">Valore</span><span class="sxs-lookup"><span data-stu-id="513f1-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="513f1-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="513f1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="513f1-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="513f1-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="513f1-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="513f1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="513f1-120">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="513f1-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="513f1-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="513f1-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="513f1-122"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="513f1-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="513f1-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="513f1-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="513f1-124">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="513f1-124">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="513f1-125">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="513f1-125">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="513f1-126">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="513f1-126">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="513f1-127">**\_comando WM**</span><span class="sxs-lookup"><span data-stu-id="513f1-127">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

