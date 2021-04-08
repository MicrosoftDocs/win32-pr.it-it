---
title: Codice di notifica ACN_START (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di animazione che è iniziata la riproduzione del clip AVI associato. Questo codice di notifica viene inviato sotto forma di un \_ messaggio di comando WM.
ms.assetid: b4d12225-36f7-4f87-b58a-dac091d14e4c
keywords:
- Controlli di Windows per il codice di notifica ACN_START
topic_type:
- apiref
api_name:
- ACN_START
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b0354d8b2b41ea8690be47e70cbc577c064e579
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740519"
---
# <a name="acn_start-notification-code"></a><span data-ttu-id="1be8c-105">\_Codice di notifica di avvio ACN</span><span class="sxs-lookup"><span data-stu-id="1be8c-105">ACN\_START notification code</span></span>

<span data-ttu-id="1be8c-106">Notifica alla finestra padre di un controllo di animazione che è iniziata la riproduzione del clip AVI associato.</span><span class="sxs-lookup"><span data-stu-id="1be8c-106">Notifies an animation control's parent window that the associated AVI clip has started playing.</span></span> <span data-ttu-id="1be8c-107">Questo codice di notifica viene inviato sotto forma di un messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="1be8c-107">This notification code is sent in the form of a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
ACN_START 

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="1be8c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="1be8c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1be8c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1be8c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1be8c-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene l'identificatore del controllo dell'animazione.</span><span class="sxs-lookup"><span data-stu-id="1be8c-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the animation control's identifier.</span></span> <span data-ttu-id="1be8c-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica il codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="1be8c-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="1be8c-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1be8c-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1be8c-113">**HWND** che specifica l'handle per il controllo dell'animazione.</span><span class="sxs-lookup"><span data-stu-id="1be8c-113">An **HWND** that specifies the handle to the animation control.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1be8c-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1be8c-114">Requirements</span></span>



| <span data-ttu-id="1be8c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="1be8c-115">Requirement</span></span> | <span data-ttu-id="1be8c-116">Valore</span><span class="sxs-lookup"><span data-stu-id="1be8c-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1be8c-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1be8c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1be8c-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1be8c-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1be8c-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1be8c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1be8c-120">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1be8c-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1be8c-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1be8c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="1be8c-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1be8c-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

