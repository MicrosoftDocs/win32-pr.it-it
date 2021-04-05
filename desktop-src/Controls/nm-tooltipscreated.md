---
title: Codice di notifica NM_TOOLTIPSCREATED (COMmctrl. h)
description: Notifica alla finestra padre di un controllo che il controllo ha creato un controllo ToolTip. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 8108f084-212d-4a16-b604-1ec134b1bb43
keywords:
- Controlli di Windows per il codice di notifica NM_TOOLTIPSCREATED
topic_type:
- apiref
api_name:
- NM_TOOLTIPSCREATED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e2e99850b17b0f2b06948a09b70a89e67e65a50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048191"
---
# <a name="nm_tooltipscreated-notification-code"></a><span data-ttu-id="74d86-105">\_Codice di notifica TOOLTIPSCREATED Nm</span><span class="sxs-lookup"><span data-stu-id="74d86-105">NM\_TOOLTIPSCREATED notification code</span></span>

<span data-ttu-id="74d86-106">Notifica alla finestra padre di un controllo che il controllo ha creato un controllo ToolTip.</span><span class="sxs-lookup"><span data-stu-id="74d86-106">Notifies a control's parent window that the control has created a tooltip control.</span></span> <span data-ttu-id="74d86-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="74d86-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_TOOLTIPSCREATED

    lpnmttc = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="74d86-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="74d86-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74d86-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="74d86-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="74d86-110">Puntatore a una struttura [**NMTOOLTIPSCREATED**](/windows/win32/api/commctrl/ns-commctrl-nmtooltipscreated) che contiene informazioni aggiuntive su questa notifica.</span><span class="sxs-lookup"><span data-stu-id="74d86-110">A pointer to an [**NMTOOLTIPSCREATED**](/windows/win32/api/commctrl/ns-commctrl-nmtooltipscreated) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74d86-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="74d86-111">Return value</span></span>

<span data-ttu-id="74d86-112">Se non diversamente specificato, il controllo Ignora il valore restituito da questo codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="74d86-112">Unless otherwise specified, the control ignores the return value from this notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="74d86-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="74d86-113">Requirements</span></span>



| <span data-ttu-id="74d86-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="74d86-114">Requirement</span></span> | <span data-ttu-id="74d86-115">Valore</span><span class="sxs-lookup"><span data-stu-id="74d86-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="74d86-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="74d86-116">Minimum supported client</span></span><br/> | <span data-ttu-id="74d86-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="74d86-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="74d86-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="74d86-118">Minimum supported server</span></span><br/> | <span data-ttu-id="74d86-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="74d86-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="74d86-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="74d86-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="74d86-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="74d86-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





