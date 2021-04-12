---
title: Codice di notifica HDN_FILTERCHANGE (COMmctrl. h)
description: Notifica alla finestra padre del controllo intestazione che gli attributi di un filtro di controllo intestazione vengono modificati o modificati. Questo codice di notifica è stato inviato sotto forma di \_ messaggio di notifica WM.
ms.assetid: 0a46af14-569a-4119-881f-549a130f9b0d
keywords:
- Controlli di Windows per il codice di notifica HDN_FILTERCHANGE
topic_type:
- apiref
api_name:
- HDN_FILTERCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3d5d31b792e909cd79cdc6aa966bfdce450787b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475377"
---
# <a name="hdn_filterchange-notification-code"></a><span data-ttu-id="b6dda-105">\_Codice di notifica FILTERCHANGE di HDN</span><span class="sxs-lookup"><span data-stu-id="b6dda-105">HDN\_FILTERCHANGE notification code</span></span>

<span data-ttu-id="b6dda-106">Notifica alla finestra padre del controllo intestazione che gli attributi di un filtro di controllo intestazione vengono modificati o modificati.</span><span class="sxs-lookup"><span data-stu-id="b6dda-106">Notifies the header control's parent window that the attributes of a header control filter are being changed or edited.</span></span> <span data-ttu-id="b6dda-107">Questo codice di notifica è stato inviato sotto forma di messaggio di [**\_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="b6dda-107">This notification code sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_FILTERCHANGE

    pNMHeader =  (LPNMHEADER) lParam;
```



## <a name="parameters"></a><span data-ttu-id="b6dda-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b6dda-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6dda-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b6dda-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b6dda-110">Puntatore a una struttura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) contenente informazioni sul controllo intestazione e sull'elemento intestazione, inclusi gli attributi che stanno per essere modificati.</span><span class="sxs-lookup"><span data-stu-id="b6dda-110">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains information about the header control and the header item, including the attributes that are about to change.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6dda-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b6dda-111">Return value</span></span>

<span data-ttu-id="b6dda-112">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="b6dda-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6dda-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b6dda-113">Requirements</span></span>



| <span data-ttu-id="b6dda-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6dda-114">Requirement</span></span> | <span data-ttu-id="b6dda-115">Valore</span><span class="sxs-lookup"><span data-stu-id="b6dda-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b6dda-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b6dda-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b6dda-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b6dda-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b6dda-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b6dda-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b6dda-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b6dda-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b6dda-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b6dda-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6dda-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6dda-121"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6dda-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b6dda-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6dda-123">**\_SETFILTERCHANGETIMEOUT HDM**</span><span class="sxs-lookup"><span data-stu-id="b6dda-123">**HDM\_SETFILTERCHANGETIMEOUT**</span></span>](hdm-setfilterchangetimeout.md)
</dt> </dl>

 

 





