---
title: Codice di notifica CBN_SELENDOK (winuser. h)
description: Inviato quando l'utente seleziona una voce di elenco o seleziona un elemento e quindi lo chiude. Indica che la selezione dell'utente deve essere elaborata. La finestra padre della casella combinata riceve questo codice di notifica tramite il \_ messaggio di comando WM.
ms.assetid: ef0ac46f-2db9-40d6-ba82-7e90d71fdd37
keywords:
- Controlli di Windows per il codice di notifica CBN_SELENDOK
topic_type:
- apiref
api_name:
- CBN_SELENDOK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a0b04fcce0ec2b3f6a2bf5b5e04fa4110ad6ceb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301672"
---
# <a name="cbn_selendok-notification-code"></a><span data-ttu-id="e6286-106">\_Codice di notifica SELENDOK CBN</span><span class="sxs-lookup"><span data-stu-id="e6286-106">CBN\_SELENDOK notification code</span></span>

<span data-ttu-id="e6286-107">Inviato quando l'utente seleziona una voce di elenco o seleziona un elemento e quindi lo chiude.</span><span class="sxs-lookup"><span data-stu-id="e6286-107">Sent when the user selects a list item, or selects an item and then closes the list.</span></span> <span data-ttu-id="e6286-108">Indica che la selezione dell'utente deve essere elaborata.</span><span class="sxs-lookup"><span data-stu-id="e6286-108">It indicates that the user's selection is to be processed.</span></span> <span data-ttu-id="e6286-109">La finestra padre della casella combinata riceve questo codice di notifica tramite il messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="e6286-109">The parent window of the combo box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
CBN_SELENDOK

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="e6286-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="e6286-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6286-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e6286-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e6286-112">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene l'identificatore di controllo della casella combinata.</span><span class="sxs-lookup"><span data-stu-id="e6286-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the control identifier of the combo box.</span></span> <span data-ttu-id="e6286-113">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica il codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="e6286-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="e6286-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e6286-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e6286-115">Handle per la casella combinata.</span><span class="sxs-lookup"><span data-stu-id="e6286-115">Handle to the combo box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e6286-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="e6286-116">Remarks</span></span>

<span data-ttu-id="e6286-117">In una casella combinata con lo [**stile \_ semplice CBS**](combo-box-styles.md) , il codice di notifica di CBN \_ SELENDOK viene inviato immediatamente prima di ogni codice di notifica [ \_ selChange CBN](cbn-selchange.md) .</span><span class="sxs-lookup"><span data-stu-id="e6286-117">In a combo box with the [**CBS\_SIMPLE**](combo-box-styles.md) style, the CBN\_SELENDOK notification code is sent immediately before every [CBN\_SELCHANGE](cbn-selchange.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6286-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e6286-118">Requirements</span></span>



| <span data-ttu-id="e6286-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6286-119">Requirement</span></span> | <span data-ttu-id="e6286-120">Valore</span><span class="sxs-lookup"><span data-stu-id="e6286-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6286-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e6286-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e6286-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e6286-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e6286-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e6286-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e6286-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e6286-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e6286-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e6286-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6286-126"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e6286-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6286-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e6286-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="e6286-128">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="e6286-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e6286-129">\_selChange CBN</span><span class="sxs-lookup"><span data-stu-id="e6286-129">CBN\_SELCHANGE</span></span>](cbn-selchange.md)
</dt> <dt>

[<span data-ttu-id="e6286-130">\_SELENDCANCEL CBN</span><span class="sxs-lookup"><span data-stu-id="e6286-130">CBN\_SELENDCANCEL</span></span>](cbn-selendcancel.md)
</dt> <dt>

<span data-ttu-id="e6286-131">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="e6286-131">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="e6286-132">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e6286-132">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="e6286-133">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e6286-133">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="e6286-134">**\_comando WM**</span><span class="sxs-lookup"><span data-stu-id="e6286-134">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

