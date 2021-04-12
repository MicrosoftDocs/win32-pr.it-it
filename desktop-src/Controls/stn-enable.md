---
title: Codice di notifica STN_ENABLE (winuser. h)
description: L' \_ Abilitazione del codice di notifica di STN viene inviata quando un controllo statico è abilitato.
ms.assetid: daac2ed3-c7cd-46f8-abfa-78754b277ef4
keywords:
- Controlli di Windows per il codice di notifica STN_ENABLE
topic_type:
- apiref
api_name:
- STN_ENABLE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfc9cc21e884a8a7e907054daa48a21678efa65e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475328"
---
# <a name="stn_enable-notification-code"></a><span data-ttu-id="6113c-104">STN \_ Abilita il codice di notifica</span><span class="sxs-lookup"><span data-stu-id="6113c-104">STN\_ENABLE notification code</span></span>

<span data-ttu-id="6113c-105">L' \_ Abilitazione del codice di notifica di STN viene inviata quando un controllo statico è abilitato.</span><span class="sxs-lookup"><span data-stu-id="6113c-105">The STN\_ENABLE notification code is sent when a static control is enabled.</span></span> <span data-ttu-id="6113c-106">Il controllo statico deve avere lo stile di [**\_ notifica SS**](static-control-styles.md) per ricevere il codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="6113c-106">The static control must have the [**SS\_NOTIFY**](static-control-styles.md) style to receive this notification code.</span></span> <span data-ttu-id="6113c-107">La finestra padre del controllo riceve questo codice di notifica tramite il messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="6113c-107">The parent window of the control receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
STN_ENABLE

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="6113c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="6113c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6113c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6113c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6113c-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene l'identificatore del controllo statico.</span><span class="sxs-lookup"><span data-stu-id="6113c-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the static control.</span></span> <span data-ttu-id="6113c-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica il codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="6113c-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="6113c-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6113c-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6113c-113">Handle per il controllo statico.</span><span class="sxs-lookup"><span data-stu-id="6113c-113">Handle to the static control.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6113c-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6113c-114">Requirements</span></span>



| <span data-ttu-id="6113c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="6113c-115">Requirement</span></span> | <span data-ttu-id="6113c-116">Valore</span><span class="sxs-lookup"><span data-stu-id="6113c-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6113c-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6113c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6113c-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6113c-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6113c-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6113c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6113c-120">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6113c-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6113c-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6113c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="6113c-122"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6113c-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6113c-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6113c-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="6113c-124">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="6113c-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6113c-125">STN \_ disabilitato</span><span class="sxs-lookup"><span data-stu-id="6113c-125">STN\_DISABLE</span></span>](stn-disable.md)
</dt> <dt>

<span data-ttu-id="6113c-126">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="6113c-126">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="6113c-127">Controlli statici</span><span class="sxs-lookup"><span data-stu-id="6113c-127">Static Controls</span></span>](static-controls.md)
</dt> <dt>

<span data-ttu-id="6113c-128">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="6113c-128">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="6113c-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6113c-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="6113c-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6113c-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="6113c-131">**\_comando WM**</span><span class="sxs-lookup"><span data-stu-id="6113c-131">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

