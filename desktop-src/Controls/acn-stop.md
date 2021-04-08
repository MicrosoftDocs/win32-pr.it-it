---
title: Codice di notifica ACN_STOP (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di animazione che la riproduzione del clip AVI associato è stata interrotta. Questo codice di notifica viene inviato sotto forma di un \_ messaggio di comando WM.
ms.assetid: 2f21a2ec-975f-4592-8b21-956bd5311ef4
keywords:
- Controlli di Windows per il codice di notifica ACN_STOP
topic_type:
- apiref
api_name:
- ACN_STOP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cbdb27677439b7f08b489cba9024d44f3ebee6d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048071"
---
# <a name="acn_stop-notification-code"></a><span data-ttu-id="2c4ba-105">Codice di notifica di arresto di ACN \_</span><span class="sxs-lookup"><span data-stu-id="2c4ba-105">ACN\_STOP notification code</span></span>

<span data-ttu-id="2c4ba-106">Notifica alla finestra padre di un controllo di animazione che la riproduzione del clip AVI associato è stata interrotta.</span><span class="sxs-lookup"><span data-stu-id="2c4ba-106">Notifies the parent window of an animation control that the associated AVI clip has stopped playing.</span></span> <span data-ttu-id="2c4ba-107">Questo codice di notifica viene inviato sotto forma di un messaggio di [**\_ comando WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="2c4ba-107">This notification code is sent in the form of a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
ACN_STOP     

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="2c4ba-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="2c4ba-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c4ba-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2c4ba-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2c4ba-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contiene l'identificatore del controllo dell'animazione.</span><span class="sxs-lookup"><span data-stu-id="2c4ba-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the animation control's identifier.</span></span> <span data-ttu-id="2c4ba-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica il codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="2c4ba-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="2c4ba-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2c4ba-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2c4ba-113">**HWND** che specifica l'handle per il controllo dell'animazione.</span><span class="sxs-lookup"><span data-stu-id="2c4ba-113">An **HWND** that specifies the handle to the animation control.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2c4ba-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2c4ba-114">Requirements</span></span>



| <span data-ttu-id="2c4ba-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c4ba-115">Requirement</span></span> | <span data-ttu-id="2c4ba-116">Valore</span><span class="sxs-lookup"><span data-stu-id="2c4ba-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2c4ba-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2c4ba-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2c4ba-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2c4ba-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2c4ba-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2c4ba-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2c4ba-120">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2c4ba-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2c4ba-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2c4ba-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c4ba-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c4ba-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

