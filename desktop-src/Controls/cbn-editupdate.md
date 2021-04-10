---
title: Codice di notifica CBN_EDITUPDATE (winuser. h)
description: Inviato quando la parte del controllo di modifica di una casella combinata sta per visualizzare il testo modificato.
ms.assetid: cae9cbf5-d420-4dfb-a46f-8c1a77de6ecf
keywords:
- Controlli di Windows per il codice di notifica CBN_EDITUPDATE
topic_type:
- apiref
api_name:
- CBN_EDITUPDATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ef56b97bf8f4c4aebb4a11383be1b5a1941167b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121507"
---
# <a name="cbn_editupdate-notification-code"></a><span data-ttu-id="6e8f2-104">\_Codice di notifica EDITUPDATE CBN</span><span class="sxs-lookup"><span data-stu-id="6e8f2-104">CBN\_EDITUPDATE notification code</span></span>

<span data-ttu-id="6e8f2-105">Inviato quando la parte del controllo di modifica di una casella combinata sta per visualizzare il testo modificato.</span><span class="sxs-lookup"><span data-stu-id="6e8f2-105">Sent when the edit control portion of a combo box is about to display altered text.</span></span> <span data-ttu-id="6e8f2-106">Questo codice di notifica viene inviato dopo che il controllo ha formattato il testo, ma prima di visualizzare il testo.</span><span class="sxs-lookup"><span data-stu-id="6e8f2-106">This notification code is sent after the control has formatted the text, but before it displays the text.</span></span> <span data-ttu-id="6e8f2-107">La finestra padre della casella combinata riceve questo codice di notifica tramite il messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="6e8f2-107">The parent window of the combo box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
CBN_EDITUPDATE

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="6e8f2-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="6e8f2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e8f2-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6e8f2-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6e8f2-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene l'identificatore di controllo della casella combinata.</span><span class="sxs-lookup"><span data-stu-id="6e8f2-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the control identifier of the combo box.</span></span> <span data-ttu-id="6e8f2-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica il codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="6e8f2-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="6e8f2-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6e8f2-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6e8f2-113">Handle per la casella combinata.</span><span class="sxs-lookup"><span data-stu-id="6e8f2-113">Handle to the combo box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6e8f2-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="6e8f2-114">Remarks</span></span>

<span data-ttu-id="6e8f2-115">Se la casella combinata ha lo stile di [**\_ DropDownList CBS**](combo-box-styles.md) , questo codice di notifica non viene inviato.</span><span class="sxs-lookup"><span data-stu-id="6e8f2-115">If the combo box has the [**CBS\_DROPDOWNLIST**](combo-box-styles.md) style, this notification code is not sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e8f2-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6e8f2-116">Requirements</span></span>



| <span data-ttu-id="6e8f2-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e8f2-117">Requirement</span></span> | <span data-ttu-id="6e8f2-118">Valore</span><span class="sxs-lookup"><span data-stu-id="6e8f2-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e8f2-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6e8f2-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6e8f2-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6e8f2-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6e8f2-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6e8f2-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6e8f2-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6e8f2-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6e8f2-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6e8f2-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e8f2-124"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6e8f2-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e8f2-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6e8f2-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="6e8f2-126">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="6e8f2-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6e8f2-127">\_EDITCHANGE CBN</span><span class="sxs-lookup"><span data-stu-id="6e8f2-127">CBN\_EDITCHANGE</span></span>](cbn-editchange.md)
</dt> <dt>

<span data-ttu-id="6e8f2-128">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="6e8f2-128">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="6e8f2-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6e8f2-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="6e8f2-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6e8f2-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="6e8f2-131">**\_comando WM**</span><span class="sxs-lookup"><span data-stu-id="6e8f2-131">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

