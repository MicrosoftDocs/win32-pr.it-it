---
title: Codice di notifica CBN_DROPDOWN (winuser. h)
description: Inviato quando la casella di riepilogo di una casella combinata sta per essere resa visibile. La finestra padre della casella combinata riceve questo codice di notifica tramite il \_ messaggio di comando WM.
ms.assetid: 2ee9bb19-951b-46bb-a90d-1ade92c2d76c
keywords:
- Controlli di Windows per il codice di notifica CBN_DROPDOWN
topic_type:
- apiref
api_name:
- CBN_DROPDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 018dac2a17a656c11ac697836390ee64e55875db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301942"
---
# <a name="cbn_dropdown-notification-code"></a><span data-ttu-id="367eb-105">\_Codice di notifica a discesa CBN</span><span class="sxs-lookup"><span data-stu-id="367eb-105">CBN\_DROPDOWN notification code</span></span>

<span data-ttu-id="367eb-106">Inviato quando la casella di riepilogo di una casella combinata sta per essere resa visibile.</span><span class="sxs-lookup"><span data-stu-id="367eb-106">Sent when the list box of a combo box is about to be made visible.</span></span> <span data-ttu-id="367eb-107">La finestra padre della casella combinata riceve questo codice di notifica tramite il messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="367eb-107">The parent window of the combo box receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
CBN_DROPDOWN

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="367eb-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="367eb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="367eb-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="367eb-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="367eb-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene l'identificatore di controllo della casella combinata.</span><span class="sxs-lookup"><span data-stu-id="367eb-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the control identifier of the combo box.</span></span> <span data-ttu-id="367eb-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica il codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="367eb-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="367eb-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="367eb-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="367eb-113">Handle per la casella combinata.</span><span class="sxs-lookup"><span data-stu-id="367eb-113">Handle to the combo box.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="367eb-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="367eb-114">Remarks</span></span>

<span data-ttu-id="367eb-115">Questo codice di notifica viene inviato solo se la casella combinata include [**l' \_ elenco a discesa CBS**](combo-box-styles.md) o lo stile [**\_ DropDownList CBS**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="367eb-115">This notification code is only sent if the combo box has the [**CBS\_DROPDOWN**](combo-box-styles.md) or [**CBS\_DROPDOWNLIST**](combo-box-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="367eb-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="367eb-116">Requirements</span></span>



| <span data-ttu-id="367eb-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="367eb-117">Requirement</span></span> | <span data-ttu-id="367eb-118">Valore</span><span class="sxs-lookup"><span data-stu-id="367eb-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="367eb-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="367eb-119">Minimum supported client</span></span><br/> | <span data-ttu-id="367eb-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="367eb-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="367eb-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="367eb-121">Minimum supported server</span></span><br/> | <span data-ttu-id="367eb-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="367eb-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="367eb-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="367eb-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="367eb-124"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="367eb-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="367eb-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="367eb-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="367eb-126">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="367eb-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="367eb-127">primo piano CBN \_</span><span class="sxs-lookup"><span data-stu-id="367eb-127">CBN\_CLOSEUP</span></span>](cbn-closeup.md)
</dt> <dt>

<span data-ttu-id="367eb-128">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="367eb-128">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="367eb-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="367eb-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="367eb-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="367eb-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="367eb-131">**\_comando WM**</span><span class="sxs-lookup"><span data-stu-id="367eb-131">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

