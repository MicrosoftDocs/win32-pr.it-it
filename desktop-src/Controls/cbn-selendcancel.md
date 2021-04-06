---
title: Codice di notifica CBN_SELENDCANCEL (winuser. h)
description: Inviato quando l'utente seleziona un elemento, ma seleziona un altro controllo o chiude la finestra di dialogo. Indica che la selezione iniziale dell'utente deve essere ignorata. La finestra padre della casella combinata riceve questo codice di notifica tramite il \_ messaggio di comando WM.
ms.assetid: ac8d6d9f-4455-42d6-b0f1-5aaa55b8ee42
keywords:
- Controlli di Windows per il codice di notifica CBN_SELENDCANCEL
topic_type:
- apiref
api_name:
- CBN_SELENDCANCEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da5b588fbd55af9dfa66a03c7912d4918821168b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743047"
---
# <a name="cbn_selendcancel-notification-code"></a><span data-ttu-id="3f0ed-106">\_Codice di notifica SELENDCANCEL CBN</span><span class="sxs-lookup"><span data-stu-id="3f0ed-106">CBN\_SELENDCANCEL notification code</span></span>

<span data-ttu-id="3f0ed-107">Inviato quando l'utente seleziona un elemento, ma seleziona un altro controllo o chiude la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="3f0ed-107">Sent when the user selects an item, but then selects another control or closes the dialog box.</span></span> <span data-ttu-id="3f0ed-108">Indica che la selezione iniziale dell'utente deve essere ignorata.</span><span class="sxs-lookup"><span data-stu-id="3f0ed-108">It indicates the user's initial selection is to be ignored.</span></span> <span data-ttu-id="3f0ed-109">La finestra padre della casella combinata riceve questo codice di notifica tramite il messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="3f0ed-109">The parent window of the combo box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
CBN_SELENDCANCEL

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="3f0ed-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="3f0ed-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f0ed-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3f0ed-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3f0ed-112">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene l'identificatore di controllo della casella combinata.</span><span class="sxs-lookup"><span data-stu-id="3f0ed-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the control identifier of the combo box.</span></span> <span data-ttu-id="3f0ed-113">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica il codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="3f0ed-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="3f0ed-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3f0ed-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3f0ed-115">Handle per la casella combinata.</span><span class="sxs-lookup"><span data-stu-id="3f0ed-115">Handle to the combo box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3f0ed-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="3f0ed-116">Remarks</span></span>

<span data-ttu-id="3f0ed-117">In una casella combinata con lo [**stile \_ semplice CBS**](combo-box-styles.md) , il codice di notifica di CBN \_ SELENDCANCEL non viene inviato.</span><span class="sxs-lookup"><span data-stu-id="3f0ed-117">In a combo box with the [**CBS\_SIMPLE**](combo-box-styles.md) style, the CBN\_SELENDCANCEL notification code is not sent.</span></span> <span data-ttu-id="3f0ed-118">Il codice di notifica di [CBN \_ SELENDOK](cbn-selendok.md) viene inviato immediatamente prima di ogni codice di notifica [ \_ selChange CBN](cbn-selchange.md) .</span><span class="sxs-lookup"><span data-stu-id="3f0ed-118">The [CBN\_SELENDOK](cbn-selendok.md) notification code is sent immediately before every [CBN\_SELCHANGE](cbn-selchange.md) notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f0ed-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3f0ed-119">Requirements</span></span>



| <span data-ttu-id="3f0ed-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f0ed-120">Requirement</span></span> | <span data-ttu-id="3f0ed-121">Valore</span><span class="sxs-lookup"><span data-stu-id="3f0ed-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f0ed-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3f0ed-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3f0ed-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3f0ed-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3f0ed-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3f0ed-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3f0ed-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3f0ed-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3f0ed-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3f0ed-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="3f0ed-127"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3f0ed-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f0ed-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3f0ed-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="3f0ed-129">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="3f0ed-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3f0ed-130">\_selChange CBN</span><span class="sxs-lookup"><span data-stu-id="3f0ed-130">CBN\_SELCHANGE</span></span>](cbn-selchange.md)
</dt> <dt>

[<span data-ttu-id="3f0ed-131">\_SELENDOK CBN</span><span class="sxs-lookup"><span data-stu-id="3f0ed-131">CBN\_SELENDOK</span></span>](cbn-selendok.md)
</dt> <dt>

<span data-ttu-id="3f0ed-132">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="3f0ed-132">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="3f0ed-133">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3f0ed-133">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="3f0ed-134">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3f0ed-134">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="3f0ed-135">**\_comando WM**</span><span class="sxs-lookup"><span data-stu-id="3f0ed-135">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

