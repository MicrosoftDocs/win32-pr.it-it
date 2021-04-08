---
title: Codice di notifica STN_CLICKED (winuser. h)
description: "\\_Quando l'utente fa clic su un controllo statico con stile di notifica SS, viene inviato il codice di notifica con clic su STN \\_ . La finestra padre del controllo riceve questo codice di notifica tramite il \\_ messaggio di comando WM."
ms.assetid: deeac9e9-c23e-4ffb-a1d7-18782efb7a5c
keywords:
- Controlli di Windows per il codice di notifica STN_CLICKED
topic_type:
- apiref
api_name:
- STN_CLICKED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91f63bc496469f6edc26b4f9176f3f9157464bdd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873365"
---
# <a name="stn_clicked-notification-code"></a><span data-ttu-id="03ea8-105">\_Codice di notifica fatto clic su STN</span><span class="sxs-lookup"><span data-stu-id="03ea8-105">STN\_CLICKED notification code</span></span>

<span data-ttu-id="03ea8-106">\_Quando l'utente fa clic su un controllo statico con stile di [**\_ notifica SS**](static-control-styles.md) , viene inviato il codice di notifica con clic su STN.</span><span class="sxs-lookup"><span data-stu-id="03ea8-106">The STN\_CLICKED notification code is sent when the user clicks a static control that has the [**SS\_NOTIFY**](static-control-styles.md) style.</span></span> <span data-ttu-id="03ea8-107">La finestra padre del controllo riceve questo codice di notifica tramite il messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="03ea8-107">The parent window of the control receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
STN_CLICKED

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="03ea8-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="03ea8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03ea8-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="03ea8-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="03ea8-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene l'identificatore del controllo statico.</span><span class="sxs-lookup"><span data-stu-id="03ea8-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the static control.</span></span> <span data-ttu-id="03ea8-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica il codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="03ea8-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="03ea8-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="03ea8-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="03ea8-113">Handle per il controllo statico.</span><span class="sxs-lookup"><span data-stu-id="03ea8-113">Handle to the static control.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="03ea8-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="03ea8-114">Requirements</span></span>



| <span data-ttu-id="03ea8-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="03ea8-115">Requirement</span></span> | <span data-ttu-id="03ea8-116">Valore</span><span class="sxs-lookup"><span data-stu-id="03ea8-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03ea8-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="03ea8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="03ea8-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="03ea8-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="03ea8-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="03ea8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="03ea8-120">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="03ea8-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="03ea8-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="03ea8-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="03ea8-122"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="03ea8-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03ea8-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="03ea8-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="03ea8-124">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="03ea8-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="03ea8-125">\_DBLCLK STN</span><span class="sxs-lookup"><span data-stu-id="03ea8-125">STN\_DBLCLK</span></span>](stn-dblclk.md)
</dt> <dt>

<span data-ttu-id="03ea8-126">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="03ea8-126">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="03ea8-127">Controlli statici</span><span class="sxs-lookup"><span data-stu-id="03ea8-127">Static Controls</span></span>](static-controls.md)
</dt> <dt>

<span data-ttu-id="03ea8-128">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="03ea8-128">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="03ea8-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="03ea8-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="03ea8-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="03ea8-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="03ea8-131">**\_comando WM**</span><span class="sxs-lookup"><span data-stu-id="03ea8-131">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

