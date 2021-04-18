---
title: Codice di notifica CBN_DBLCLK (winuser. h)
description: Inviato quando l'utente fa doppio clic su una stringa nella casella di riepilogo di una casella combinata. La finestra padre della casella combinata riceve questo codice di notifica tramite il \_ messaggio di comando WM.
ms.assetid: 79ca3fd3-4a71-4bd5-be68-efc867a4ad22
keywords:
- Controlli di Windows per il codice di notifica CBN_DBLCLK
topic_type:
- apiref
api_name:
- CBN_DBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 841c68079572e1740f074034c1a8097ba6a86253
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302724"
---
# <a name="cbn_dblclk-notification-code"></a><span data-ttu-id="2f016-105">\_Codice di notifica DBLCLK CBN</span><span class="sxs-lookup"><span data-stu-id="2f016-105">CBN\_DBLCLK notification code</span></span>

<span data-ttu-id="2f016-106">Inviato quando l'utente fa doppio clic su una stringa nella casella di riepilogo di una casella combinata.</span><span class="sxs-lookup"><span data-stu-id="2f016-106">Sent when the user double-clicks a string in the list box of a combo box.</span></span> <span data-ttu-id="2f016-107">La finestra padre della casella combinata riceve questo codice di notifica tramite il messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="2f016-107">The parent window of the combo box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
CBN_DBLCLK

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="2f016-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="2f016-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f016-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2f016-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2f016-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene l'identificatore di controllo della casella combinata.</span><span class="sxs-lookup"><span data-stu-id="2f016-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the control identifier of the combo box.</span></span> <span data-ttu-id="2f016-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica il codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="2f016-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="2f016-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2f016-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2f016-113">Handle per la casella combinata.</span><span class="sxs-lookup"><span data-stu-id="2f016-113">Handle to the combo box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2f016-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="2f016-114">Remarks</span></span>

<span data-ttu-id="2f016-115">Questo codice di notifica si verifica solo per una casella combinata con stile [**\_ semplice CBS**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="2f016-115">This notification code occurs only for a combo box with the [**CBS\_SIMPLE**](combo-box-styles.md) style.</span></span> <span data-ttu-id="2f016-116">In una casella combinata con l'elenco a [**\_ discesa CBS**](combo-box-styles.md) o lo stile [**\_ DropDownList CBS**](combo-box-styles.md) , un doppio clic non può verificarsi perché un solo clic chiude la casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="2f016-116">In a combo box with the [**CBS\_DROPDOWN**](combo-box-styles.md) or [**CBS\_DROPDOWNLIST**](combo-box-styles.md) style, a double-click cannot occur because a single click closes the list box.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f016-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2f016-117">Requirements</span></span>



| <span data-ttu-id="2f016-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f016-118">Requirement</span></span> | <span data-ttu-id="2f016-119">Valore</span><span class="sxs-lookup"><span data-stu-id="2f016-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f016-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2f016-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2f016-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2f016-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2f016-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2f016-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2f016-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2f016-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2f016-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2f016-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f016-125"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2f016-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f016-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2f016-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="2f016-127">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="2f016-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2f016-128">\_selChange CBN</span><span class="sxs-lookup"><span data-stu-id="2f016-128">CBN\_SELCHANGE</span></span>](cbn-selchange.md)
</dt> <dt>

<span data-ttu-id="2f016-129">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="2f016-129">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="2f016-130">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2f016-130">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="2f016-131">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2f016-131">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="2f016-132">**\_comando WM**</span><span class="sxs-lookup"><span data-stu-id="2f016-132">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

