---
title: Codice di notifica BN_CLICKED (winuser. h)
description: Inviato quando l'utente fa clic su un pulsante. La finestra padre del pulsante riceve questo codice di notifica tramite il \_ messaggio di comando WM.
ms.assetid: 74847549-b92f-4981-a979-d0b2a8a5539a
keywords:
- Controlli di Windows per il codice di notifica BN_CLICKED
topic_type:
- apiref
api_name:
- BN_CLICKED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 894837c9a930c6a5f6d124b6b9e983465ef3beac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119339"
---
# <a name="bn_clicked-notification-code"></a><span data-ttu-id="d6f53-105">\_Codice di notifica fatto clic su BN</span><span class="sxs-lookup"><span data-stu-id="d6f53-105">BN\_CLICKED notification code</span></span>

<span data-ttu-id="d6f53-106">Inviato quando l'utente fa clic su un pulsante.</span><span class="sxs-lookup"><span data-stu-id="d6f53-106">Sent when the user clicks a button.</span></span>

<span data-ttu-id="d6f53-107">La finestra padre del pulsante riceve questo codice di notifica tramite il messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="d6f53-107">The parent window of the button receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
BN_CLICKED

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="d6f53-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d6f53-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6f53-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d6f53-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d6f53-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene l'identificatore di controllo del pulsante.</span><span class="sxs-lookup"><span data-stu-id="d6f53-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the button's control identifier.</span></span> <span data-ttu-id="d6f53-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica il codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="d6f53-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="d6f53-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d6f53-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d6f53-113">Handle per il pulsante.</span><span class="sxs-lookup"><span data-stu-id="d6f53-113">A handle to the button.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d6f53-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="d6f53-114">Remarks</span></span>

<span data-ttu-id="d6f53-115">Un pulsante disabilitato non invia un \_ codice di notifica fatto clic su BN alla finestra padre.</span><span class="sxs-lookup"><span data-stu-id="d6f53-115">A disabled button does not send a BN\_CLICKED notification code to its parent window.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6f53-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d6f53-116">Requirements</span></span>



| <span data-ttu-id="d6f53-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6f53-117">Requirement</span></span> | <span data-ttu-id="d6f53-118">Valore</span><span class="sxs-lookup"><span data-stu-id="d6f53-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6f53-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d6f53-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d6f53-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d6f53-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d6f53-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d6f53-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d6f53-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d6f53-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d6f53-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d6f53-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6f53-124"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d6f53-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6f53-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d6f53-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="d6f53-126">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="d6f53-126">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="d6f53-127">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d6f53-127">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="d6f53-128">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d6f53-128">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="d6f53-129">**\_comando WM**</span><span class="sxs-lookup"><span data-stu-id="d6f53-129">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

