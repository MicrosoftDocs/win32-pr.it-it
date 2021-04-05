---
title: Codice di notifica TCN_SELCHANGE (COMmctrl. h)
description: Notifica alla finestra padre di un controllo struttura a schede che la scheda attualmente selezionata è stata modificata. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: f40e30f6-169b-4381-a300-12c3befb5fc5
keywords:
- Controlli di Windows per il codice di notifica TCN_SELCHANGE
topic_type:
- apiref
api_name:
- TCN_SELCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8578ac9fee7754b1ae27c05c6ec1b15636090040
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739863"
---
# <a name="tcn_selchange-notification-code"></a><span data-ttu-id="1f147-105">\_Codice di notifica SelChange di TCN</span><span class="sxs-lookup"><span data-stu-id="1f147-105">TCN\_SELCHANGE notification code</span></span>

<span data-ttu-id="1f147-106">Notifica alla finestra padre di un controllo struttura a schede che la scheda attualmente selezionata è stata modificata.</span><span class="sxs-lookup"><span data-stu-id="1f147-106">Notifies a tab control's parent window that the currently selected tab has changed.</span></span> <span data-ttu-id="1f147-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="1f147-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TCN_SELCHANGE 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="1f147-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="1f147-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f147-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1f147-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1f147-110">Puntatore a una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) che contiene informazioni aggiuntive su questa notifica.</span><span class="sxs-lookup"><span data-stu-id="1f147-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f147-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1f147-111">Return value</span></span>

<span data-ttu-id="1f147-112">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="1f147-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f147-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="1f147-113">Remarks</span></span>

<span data-ttu-id="1f147-114">Per determinare la scheda attualmente selezionata, usare la macro [**TabCtrl \_ GetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcursel) .</span><span class="sxs-lookup"><span data-stu-id="1f147-114">To determine the currently selected tab, use the [**TabCtrl\_GetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcursel) macro.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f147-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1f147-115">Requirements</span></span>



| <span data-ttu-id="1f147-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f147-116">Requirement</span></span> | <span data-ttu-id="1f147-117">Valore</span><span class="sxs-lookup"><span data-stu-id="1f147-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1f147-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1f147-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1f147-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1f147-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1f147-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1f147-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1f147-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1f147-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1f147-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1f147-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f147-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f147-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f147-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1f147-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f147-125">\_SELCHANGING TCN</span><span class="sxs-lookup"><span data-stu-id="1f147-125">TCN\_SELCHANGING</span></span>](tcn-selchanging.md)
</dt> </dl>

 

 





