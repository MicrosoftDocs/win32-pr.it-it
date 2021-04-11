---
title: Codice di notifica STN_DISABLE (winuser. h)
description: Il \_ codice di notifica di disabilitazione di STN viene inviato quando un controllo statico è disabilitato.
ms.assetid: 7ff0c191-4ff3-4a11-a418-8f45e16d0318
keywords:
- Controlli di Windows per il codice di notifica STN_DISABLE
topic_type:
- apiref
api_name:
- STN_DISABLE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2763fce96b043ec6aebf5339a9f93d6fdf4a8abb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119163"
---
# <a name="stn_disable-notification-code"></a><span data-ttu-id="1db52-104">STN \_ disabilitare il codice di notifica</span><span class="sxs-lookup"><span data-stu-id="1db52-104">STN\_DISABLE notification code</span></span>

<span data-ttu-id="1db52-105">Il \_ codice di notifica di disabilitazione di STN viene inviato quando un controllo statico è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="1db52-105">The STN\_DISABLE notification code is sent when a static control is disabled.</span></span> <span data-ttu-id="1db52-106">Il controllo statico deve avere lo stile di [**\_ notifica SS**](static-control-styles.md) per ricevere il codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="1db52-106">The static control must have the [**SS\_NOTIFY**](static-control-styles.md) style to receive this notification code.</span></span> <span data-ttu-id="1db52-107">La finestra padre del controllo riceve questo codice di notifica tramite il messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="1db52-107">The parent window of the control receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
STN_DISABLE

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="1db52-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="1db52-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1db52-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1db52-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1db52-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene l'identificatore del controllo statico.</span><span class="sxs-lookup"><span data-stu-id="1db52-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the static control.</span></span> <span data-ttu-id="1db52-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica il codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="1db52-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="1db52-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1db52-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1db52-113">Handle per il controllo statico.</span><span class="sxs-lookup"><span data-stu-id="1db52-113">Handle to the static control.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1db52-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1db52-114">Requirements</span></span>



| <span data-ttu-id="1db52-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="1db52-115">Requirement</span></span> | <span data-ttu-id="1db52-116">Valore</span><span class="sxs-lookup"><span data-stu-id="1db52-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1db52-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1db52-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1db52-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1db52-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1db52-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1db52-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1db52-120">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1db52-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1db52-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1db52-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="1db52-122"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1db52-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1db52-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1db52-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="1db52-124">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="1db52-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1db52-125">\_Abilitazione di STN</span><span class="sxs-lookup"><span data-stu-id="1db52-125">STN\_ENABLE</span></span>](stn-enable.md)
</dt> <dt>

<span data-ttu-id="1db52-126">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="1db52-126">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="1db52-127">Controlli statici</span><span class="sxs-lookup"><span data-stu-id="1db52-127">Static Controls</span></span>](static-controls.md)
</dt> <dt>

<span data-ttu-id="1db52-128">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="1db52-128">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="1db52-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1db52-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="1db52-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1db52-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="1db52-131">**\_comando WM**</span><span class="sxs-lookup"><span data-stu-id="1db52-131">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

