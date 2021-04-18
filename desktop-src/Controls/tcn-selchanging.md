---
title: Codice di notifica TCN_SELCHANGING (COMmctrl. h)
description: Notifica alla finestra padre di un controllo struttura a schede che la scheda attualmente selezionata sta per essere modificata. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: ec7b1bd3-8932-4418-9eed-ecb7c748e4dd
keywords:
- Controlli di Windows per il codice di notifica TCN_SELCHANGING
topic_type:
- apiref
api_name:
- TCN_SELCHANGING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6ba7dcf25d243d9b42876425564fba0e01c803f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106300962"
---
# <a name="tcn_selchanging-notification-code"></a><span data-ttu-id="2de22-105">\_Codice di notifica SELCHANGING di TCN</span><span class="sxs-lookup"><span data-stu-id="2de22-105">TCN\_SELCHANGING notification code</span></span>

<span data-ttu-id="2de22-106">Notifica alla finestra padre di un controllo struttura a schede che la scheda attualmente selezionata sta per essere modificata.</span><span class="sxs-lookup"><span data-stu-id="2de22-106">Notifies a tab control's parent window that the currently selected tab is about to change.</span></span> <span data-ttu-id="2de22-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="2de22-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TCN_SELCHANGING 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="2de22-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="2de22-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2de22-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2de22-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2de22-110">Puntatore a una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) che contiene informazioni aggiuntive su questa notifica.</span><span class="sxs-lookup"><span data-stu-id="2de22-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2de22-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2de22-111">Return value</span></span>

<span data-ttu-id="2de22-112">Restituisce **true** per impedire la modifica della selezione o **false** per consentire la modifica della selezione.</span><span class="sxs-lookup"><span data-stu-id="2de22-112">Returns **TRUE** to prevent the selection from changing, or **FALSE** to allow the selection to change.</span></span>

## <a name="remarks"></a><span data-ttu-id="2de22-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="2de22-113">Remarks</span></span>

<span data-ttu-id="2de22-114">Per determinare la scheda attualmente selezionata, usare la macro [**TabCtrl \_ GetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcursel) .</span><span class="sxs-lookup"><span data-stu-id="2de22-114">To determine the currently selected tab, use the [**TabCtrl\_GetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcursel) macro.</span></span>

## <a name="requirements"></a><span data-ttu-id="2de22-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2de22-115">Requirements</span></span>



| <span data-ttu-id="2de22-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="2de22-116">Requirement</span></span> | <span data-ttu-id="2de22-117">Valore</span><span class="sxs-lookup"><span data-stu-id="2de22-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2de22-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2de22-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2de22-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2de22-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2de22-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2de22-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2de22-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2de22-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2de22-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2de22-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="2de22-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2de22-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2de22-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2de22-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2de22-125">\_selChange TCN</span><span class="sxs-lookup"><span data-stu-id="2de22-125">TCN\_SELCHANGE</span></span>](tcn-selchange.md)
</dt> </dl>

 

 





