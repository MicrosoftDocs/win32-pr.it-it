---
title: Codice di notifica BN_SETFOCUS (winuser. h)
description: Inviato quando un pulsante riceve lo stato attivo della tastiera. Il pulsante deve avere lo \_ stile di notifica BS per inviare il codice di notifica. La finestra padre del pulsante riceve questo codice di notifica tramite il \_ messaggio di comando WM.
ms.assetid: 6b8d9bde-67f9-454f-ba2c-e5c8d9ff2709
keywords:
- Controlli di Windows per il codice di notifica BN_SETFOCUS
topic_type:
- apiref
api_name:
- BN_SETFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3eb9204f5b23b62b6cee9fb2652a16d546f6ef62
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301183"
---
# <a name="bn_setfocus-notification-code"></a><span data-ttu-id="5002e-106">Codice di notifica per la messa a fuoco di BN \_</span><span class="sxs-lookup"><span data-stu-id="5002e-106">BN\_SETFOCUS notification code</span></span>

<span data-ttu-id="5002e-107">Inviato quando un pulsante riceve lo stato attivo della tastiera.</span><span class="sxs-lookup"><span data-stu-id="5002e-107">Sent when a button receives the keyboard focus.</span></span> <span data-ttu-id="5002e-108">Il pulsante deve avere lo stile di [**\_ notifica BS**](button-styles.md) per inviare il codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="5002e-108">The button must have the [**BS\_NOTIFY**](button-styles.md) style to send this notification code.</span></span>

<span data-ttu-id="5002e-109">La finestra padre del pulsante riceve questo codice di notifica tramite il messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="5002e-109">The parent window of the button receives this notification code through the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
BN_SETFOCUS

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="5002e-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="5002e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5002e-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5002e-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5002e-112">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene l'identificatore di controllo del pulsante.</span><span class="sxs-lookup"><span data-stu-id="5002e-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the button's control identifier.</span></span> <span data-ttu-id="5002e-113">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica il codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="5002e-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="5002e-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5002e-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5002e-115">Handle per il pulsante.</span><span class="sxs-lookup"><span data-stu-id="5002e-115">A handle to the button.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5002e-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5002e-116">Requirements</span></span>



| <span data-ttu-id="5002e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="5002e-117">Requirement</span></span> | <span data-ttu-id="5002e-118">Valore</span><span class="sxs-lookup"><span data-stu-id="5002e-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5002e-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5002e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5002e-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5002e-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5002e-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5002e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5002e-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5002e-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5002e-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5002e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5002e-124"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5002e-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5002e-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5002e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5002e-126">BN \_ KILLFOCUS</span><span class="sxs-lookup"><span data-stu-id="5002e-126">BN\_KILLFOCUS</span></span>](bn-killfocus.md)
</dt> </dl>

 

