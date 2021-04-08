---
title: Codice di notifica EN_ALIGN_RTL_EC (winuser. h)
description: Inviato quando l'utente ha modificato la direzione del controllo di modifica da destra a sinistra. La finestra padre del controllo di modifica riceve questo codice di notifica tramite un \_ messaggio di comando WM.
ms.assetid: c53bc808-48c6-4a8f-ae5d-af2164fe419a
keywords:
- Controlli di Windows per il codice di notifica EN_ALIGN_RTL_EC
topic_type:
- apiref
api_name:
- EN_ALIGN_RTL_EC
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eca94073b86ea44b192360e593f4b76d4227cf82
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873586"
---
# <a name="en_align_rtl_ec-notification-code"></a><span data-ttu-id="42b10-105">\_Allinea il \_ codice di \_ notifica RTL EC</span><span class="sxs-lookup"><span data-stu-id="42b10-105">EN\_ALIGN\_RTL\_EC notification code</span></span>

<span data-ttu-id="42b10-106">Inviato quando l'utente ha modificato la direzione del controllo di modifica da destra a sinistra.</span><span class="sxs-lookup"><span data-stu-id="42b10-106">Sent when the user has changed the edit control direction to right-to-left.</span></span> <span data-ttu-id="42b10-107">La finestra padre del controllo di modifica riceve questo codice di notifica tramite un messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="42b10-107">The parent window of the edit control receives this notification code through a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
EN_ALIGN_RTL_EC

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="42b10-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="42b10-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42b10-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="42b10-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="42b10-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene l'identificatore del controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="42b10-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the edit control.</span></span> <span data-ttu-id="42b10-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica il codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="42b10-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="42b10-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="42b10-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="42b10-113">Handle per il controllo di modifica che invia il codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="42b10-113">A handle to the edit control sending the notification code.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="42b10-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="42b10-114">Remarks</span></span>

<span data-ttu-id="42b10-115">Se nel sistema è installata una lingua bidirezionale, ad esempio l'arabo o l'ebraico, è possibile modificare la direzione del controllo di modifica usando CTRL + LSHIFT (da sinistra a destra) e CTRL + RSHIFT (da destra a sinistra).</span><span class="sxs-lookup"><span data-stu-id="42b10-115">If there is a bidirectional language installed on your system, for example, Arabic or Hebrew, you can change the edit control direction using CTRL+LSHIFT (for left to right) and CTRL+RSHIFT (for right to left).</span></span>

<span data-ttu-id="42b10-116">**Modifica avanzata:** Questo codice di notifica non è supportato.</span><span class="sxs-lookup"><span data-stu-id="42b10-116">**Rich Edit:** This notification code is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="42b10-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="42b10-117">Requirements</span></span>



| <span data-ttu-id="42b10-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="42b10-118">Requirement</span></span> | <span data-ttu-id="42b10-119">Valore</span><span class="sxs-lookup"><span data-stu-id="42b10-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42b10-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="42b10-120">Minimum supported client</span></span><br/> | <span data-ttu-id="42b10-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="42b10-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="42b10-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="42b10-122">Minimum supported server</span></span><br/> | <span data-ttu-id="42b10-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="42b10-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="42b10-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="42b10-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="42b10-125"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="42b10-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42b10-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="42b10-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42b10-127">**\_comando WM**</span><span class="sxs-lookup"><span data-stu-id="42b10-127">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

