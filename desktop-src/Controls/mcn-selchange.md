---
title: Codice di notifica MCN_SELCHANGE (COMmctrl. h)
description: Inviato da un controllo di calendario mensile quando cambia la data o l'intervallo di date attualmente selezionato. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 8923524f-d257-409d-bd3e-021684b88856
keywords:
- Controlli di Windows per il codice di notifica MCN_SELCHANGE
topic_type:
- apiref
api_name:
- MCN_SELCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffa328ca0173afd3a577f6cf14e0204cd5c0f7d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047996"
---
# <a name="mcn_selchange-notification-code"></a><span data-ttu-id="10b35-105">\_Codice di notifica SelChange di MCN</span><span class="sxs-lookup"><span data-stu-id="10b35-105">MCN\_SELCHANGE notification code</span></span>

<span data-ttu-id="10b35-106">Inviato da un controllo di calendario mensile quando cambia la data o l'intervallo di date attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="10b35-106">Sent by a month calendar control when the currently selected date or range of dates changes.</span></span> <span data-ttu-id="10b35-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="10b35-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
MCN_SELCHANGE

    lpNMSelChange = (LPNMSELCHANGE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="10b35-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="10b35-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10b35-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="10b35-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="10b35-110">Puntatore a una struttura [**NMSELCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmselchange) che contiene informazioni sull'intervallo di date attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="10b35-110">Pointer to an [**NMSELCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmselchange) structure that contains information about the currently selected date range.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10b35-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="10b35-111">Return value</span></span>

<span data-ttu-id="10b35-112">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="10b35-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="10b35-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="10b35-113">Remarks</span></span>

<span data-ttu-id="10b35-114">Ad esempio, il controllo Invia MCN \_ selChange quando l'utente modifica in modo esplicito la selezione nel mese corrente o quando la selezione viene modificata in modo implicito in risposta alla navigazione successiva/precedente del mese.</span><span class="sxs-lookup"><span data-stu-id="10b35-114">For example, the control sends MCN\_SELCHANGE when the user explicitly changes the selection within the current month or when the selection is implicitly changed in response to next/previous month navigation.</span></span> <span data-ttu-id="10b35-115">Questo codice di notifica viene inoltre inviato dal sistema a intervalli regolari, in modo che il controllo possa rispondere alle modifiche apportate alla data.</span><span class="sxs-lookup"><span data-stu-id="10b35-115">This notification code is also sent by the system at regular intervals so that the control can respond to date changes.</span></span>

<span data-ttu-id="10b35-116">Questo codice di notifica è simile a [MCN \_ SELECT](mcn-select.md), ma viene inviato in risposta a una modifica di selezione.</span><span class="sxs-lookup"><span data-stu-id="10b35-116">This notification code is similar to [MCN\_SELECT](mcn-select.md), but it is sent in response to any selection change.</span></span> <span data-ttu-id="10b35-117">MCN \_ Select viene inviato solo per la selezione di una data esplicita.</span><span class="sxs-lookup"><span data-stu-id="10b35-117">MCN\_SELECT is sent only for an explicit date selection.</span></span>

## <a name="requirements"></a><span data-ttu-id="10b35-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="10b35-118">Requirements</span></span>



| <span data-ttu-id="10b35-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="10b35-119">Requirement</span></span> | <span data-ttu-id="10b35-120">Valore</span><span class="sxs-lookup"><span data-stu-id="10b35-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="10b35-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="10b35-121">Minimum supported client</span></span><br/> | <span data-ttu-id="10b35-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="10b35-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="10b35-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="10b35-123">Minimum supported server</span></span><br/> | <span data-ttu-id="10b35-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="10b35-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="10b35-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="10b35-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="10b35-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="10b35-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





