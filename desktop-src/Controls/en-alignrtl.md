---
title: Codice di notifica EN_ALIGNRTL (RichEdit. h)
description: Notifica alla finestra padre di un controllo Rich Edit che la direzione del paragrafo è stata modificata da destra a sinistra. Un controllo Rich Edit invia questo codice di notifica sotto forma di un \_ messaggio di comando WM.
ms.assetid: 2db5fd49-9ecd-49d7-8199-1706648255ca
keywords:
- Controlli di Windows per il codice di notifica EN_ALIGNRTL
topic_type:
- apiref
api_name:
- EN_ALIGNRTL
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fac2adaa629d00ef940f02f1ed69eb778cdc7813
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476096"
---
# <a name="en_alignrtl-notification-code"></a><span data-ttu-id="a84c6-105">\_Codice di notifica en ALIGNRTL</span><span class="sxs-lookup"><span data-stu-id="a84c6-105">EN\_ALIGNRTL notification code</span></span>

<span data-ttu-id="a84c6-106">Notifica alla finestra padre di un controllo Rich Edit che la direzione del paragrafo è stata modificata da destra a sinistra.</span><span class="sxs-lookup"><span data-stu-id="a84c6-106">Notifies a rich edit control's parent window that the paragraph direction changed to right-to-left.</span></span> <span data-ttu-id="a84c6-107">Un controllo Rich Edit invia questo codice di notifica sotto forma di un messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="a84c6-107">A rich edit control sends this notification code in the form of a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
EN_ALIGNRTL

    WPARAM wParam
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="a84c6-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a84c6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a84c6-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a84c6-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a84c6-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene l'identificatore del controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="a84c6-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the rich edit control.</span></span> <span data-ttu-id="a84c6-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica il codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="a84c6-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="a84c6-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a84c6-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a84c6-113">Handle per il controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="a84c6-113">Handle to the rich edit control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a84c6-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a84c6-114">Return value</span></span>

<span data-ttu-id="a84c6-115">Questo codice di notifica non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="a84c6-115">This notification code does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a84c6-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a84c6-116">Requirements</span></span>



| <span data-ttu-id="a84c6-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="a84c6-117">Requirement</span></span> | <span data-ttu-id="a84c6-118">Valore</span><span class="sxs-lookup"><span data-stu-id="a84c6-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a84c6-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a84c6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a84c6-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a84c6-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a84c6-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a84c6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a84c6-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a84c6-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a84c6-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a84c6-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="a84c6-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="a84c6-124"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a84c6-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a84c6-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="a84c6-126">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="a84c6-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a84c6-127">**EN \_ ALIGNLTR**</span><span class="sxs-lookup"><span data-stu-id="a84c6-127">**EN\_ALIGNLTR**</span></span>](en-alignltr.md)
</dt> <dt>

<span data-ttu-id="a84c6-128">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="a84c6-128">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="a84c6-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a84c6-129">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="a84c6-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a84c6-130">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="a84c6-131">**\_comando WM**</span><span class="sxs-lookup"><span data-stu-id="a84c6-131">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

