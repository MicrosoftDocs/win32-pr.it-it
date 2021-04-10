---
title: Codice di notifica LBN_SELCANCEL (winuser. h)
description: Notifica all'applicazione che l'utente ha annullato la selezione in una casella di riepilogo. La finestra padre della casella di riepilogo riceve questo codice di notifica tramite il \_ messaggio di comando WM.
ms.assetid: 82e39f22-090e-4dda-8ddc-6a1fe4704fc7
keywords:
- Controlli di Windows per il codice di notifica LBN_SELCANCEL
topic_type:
- apiref
api_name:
- LBN_SELCANCEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c192fbdfdb7a351d51993bee89b9b6ec3dab387
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964747"
---
# <a name="lbn_selcancel-notification-code"></a><span data-ttu-id="9bd05-105">\_Codice di notifica SELCANCEL di LBN</span><span class="sxs-lookup"><span data-stu-id="9bd05-105">LBN\_SELCANCEL notification code</span></span>

<span data-ttu-id="9bd05-106">Notifica all'applicazione che l'utente ha annullato la selezione in una casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="9bd05-106">Notifies the application that the user has canceled the selection in a list box.</span></span> <span data-ttu-id="9bd05-107">La finestra padre della casella di riepilogo riceve questo codice di notifica tramite il messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="9bd05-107">The parent window of the list box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
LBN_SELCANCEL

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="9bd05-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="9bd05-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9bd05-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9bd05-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9bd05-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene l'identificatore della casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="9bd05-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the list box.</span></span> <span data-ttu-id="9bd05-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica il codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="9bd05-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="9bd05-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9bd05-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9bd05-113">Handle per la casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="9bd05-113">Handle to the list box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9bd05-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="9bd05-114">Remarks</span></span>

<span data-ttu-id="9bd05-115">Questo codice di notifica viene inviato solo da una casella di riepilogo con stile [**di \_ notifica L BS**](button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="9bd05-115">This notification code is sent only by a list box that has the L [**BS\_NOTIFY**](button-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="9bd05-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9bd05-116">Requirements</span></span>



| <span data-ttu-id="9bd05-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="9bd05-117">Requirement</span></span> | <span data-ttu-id="9bd05-118">Valore</span><span class="sxs-lookup"><span data-stu-id="9bd05-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9bd05-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9bd05-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9bd05-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9bd05-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="9bd05-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9bd05-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9bd05-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9bd05-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9bd05-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9bd05-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9bd05-124"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9bd05-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9bd05-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9bd05-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="9bd05-126">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="9bd05-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9bd05-127">**di \_ lb**</span><span class="sxs-lookup"><span data-stu-id="9bd05-127">**LB\_SETCURSEL**</span></span>](lb-setcursel.md)
</dt> <dt>

[<span data-ttu-id="9bd05-128">\_DBLCLK LBN</span><span class="sxs-lookup"><span data-stu-id="9bd05-128">LBN\_DBLCLK</span></span>](lbn-dblclk.md)
</dt> <dt>

[<span data-ttu-id="9bd05-129">\_selChange LBN</span><span class="sxs-lookup"><span data-stu-id="9bd05-129">LBN\_SELCHANGE</span></span>](lbn-selchange.md)
</dt> <dt>

<span data-ttu-id="9bd05-130">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="9bd05-130">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="9bd05-131">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9bd05-131">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="9bd05-132">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9bd05-132">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="9bd05-133">**\_comando WM**</span><span class="sxs-lookup"><span data-stu-id="9bd05-133">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

