---
title: Codice di notifica LVN_MARQUEEBEGIN (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di visualizzazione elenco che è iniziata una selezione del rettangolo di selezione. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: e9daa264-1861-4791-9a12-cf95d86a688e
keywords:
- Controlli di Windows per il codice di notifica LVN_MARQUEEBEGIN
topic_type:
- apiref
api_name:
- LVN_MARQUEEBEGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d46d399b8355bea0ddb2054340d52db59c3ad27
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302797"
---
# <a name="lvn_marqueebegin-notification-code"></a><span data-ttu-id="fe171-105">\_Codice di notifica MARQUEEBEGIN di LVN</span><span class="sxs-lookup"><span data-stu-id="fe171-105">LVN\_MARQUEEBEGIN notification code</span></span>

<span data-ttu-id="fe171-106">Notifica alla finestra padre di un controllo di visualizzazione elenco che è iniziata una selezione del rettangolo di selezione.</span><span class="sxs-lookup"><span data-stu-id="fe171-106">Notifies a list-view control's parent window that a bounding box (marquee) selection has begun.</span></span> <span data-ttu-id="fe171-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="fe171-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_MARQUEEBEGIN

    pnmv = (LPNMLISTVIEW) lParam;
```



## <a name="parameters"></a><span data-ttu-id="fe171-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="fe171-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe171-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fe171-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fe171-110">Puntatore a una struttura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) .</span><span class="sxs-lookup"><span data-stu-id="fe171-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe171-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fe171-111">Return value</span></span>

<span data-ttu-id="fe171-112">Per accettare il codice di notifica, restituire zero.</span><span class="sxs-lookup"><span data-stu-id="fe171-112">To accept the notification code, return zero.</span></span> <span data-ttu-id="fe171-113">Per uscire dalla selezione del rettangolo di selezione, restituire un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="fe171-113">To quit the bounding box selection, return nonzero.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe171-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="fe171-114">Remarks</span></span>

<span data-ttu-id="fe171-115">La *selezione* di un riquadro è il processo che consente di fare clic sull'area client della finestra visualizzazione elenco e di trascinare per selezionare più elementi contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="fe171-115">A *bounding box selection* is the process of clicking the list-view window's client area and dragging to select multiple items simultaneously.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe171-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fe171-116">Requirements</span></span>



| <span data-ttu-id="fe171-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe171-117">Requirement</span></span> | <span data-ttu-id="fe171-118">Valore</span><span class="sxs-lookup"><span data-stu-id="fe171-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fe171-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fe171-119">Minimum supported client</span></span><br/> | <span data-ttu-id="fe171-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fe171-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fe171-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fe171-121">Minimum supported server</span></span><br/> | <span data-ttu-id="fe171-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fe171-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fe171-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fe171-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe171-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe171-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





