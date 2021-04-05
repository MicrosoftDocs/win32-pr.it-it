---
title: Messaggio RBN_AUTOBREAK (COMmctrl. h)
description: Notifica all'elemento padre di un controllo Rebar che verrà visualizzata un'interruzioni nella barra. L'elemento padre determina se eseguire l'interruzioni. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: b7a63027-6cfa-4d5a-9ea6-fdd8b4fb6864
keywords:
- Controlli di Windows Message RBN_AUTOBREAK
topic_type:
- apiref
api_name:
- RBN_AUTOBREAK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d614277d89578cb66e528ba16656ed55681ebbcf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874566"
---
# <a name="rbn_autobreak-message"></a><span data-ttu-id="8e8ab-106">\_Messaggio di AUTOBREAK RBN</span><span class="sxs-lookup"><span data-stu-id="8e8ab-106">RBN\_AUTOBREAK message</span></span>

<span data-ttu-id="8e8ab-107">Notifica all'elemento padre di un controllo [Rebar](rebar-controls.md) che verrà visualizzata un'interruzioni nella barra.</span><span class="sxs-lookup"><span data-stu-id="8e8ab-107">Notifies a [rebar's](rebar-controls.md) parent that a break will appear in the bar.</span></span> <span data-ttu-id="8e8ab-108">L'elemento padre determina se eseguire l'interruzioni.</span><span class="sxs-lookup"><span data-stu-id="8e8ab-108">The parent determines whether to make the break.</span></span> <span data-ttu-id="8e8ab-109">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="8e8ab-109">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_AUTOBREAK

    pnmRebarAutoBreak = (LPNMREBARAUTOBREAK) lParam;
```



## <a name="parameters"></a><span data-ttu-id="8e8ab-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="8e8ab-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e8ab-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8e8ab-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8e8ab-112">Puntatore a una struttura [**NMREBARAUTOBREAK**](/windows/win32/api/commctrl/ns-commctrl-nmrebarautobreak) contenente informazioni sul codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="8e8ab-112">Pointer to a [**NMREBARAUTOBREAK**](/windows/win32/api/commctrl/ns-commctrl-nmrebarautobreak) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e8ab-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8e8ab-113">Return value</span></span>

<span data-ttu-id="8e8ab-114">Il valore restituito per questa notifica non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="8e8ab-114">The return value for this notification is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e8ab-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="8e8ab-115">Remarks</span></span>

<span data-ttu-id="8e8ab-116">Il valore nel membro **fAutoBreak** della struttura [**NMREBARAUTOBREAK**](/windows/win32/api/commctrl/ns-commctrl-nmrebarautobreak) indica se deve verificarsi un'interruzioni nel controllo Rebar.</span><span class="sxs-lookup"><span data-stu-id="8e8ab-116">The value in the **fAutoBreak** member of the [**NMREBARAUTOBREAK**](/windows/win32/api/commctrl/ns-commctrl-nmrebarautobreak) structure indicates whether a break should occur in the rebar.</span></span>

<span data-ttu-id="8e8ab-117">Per usare questo codice di notifica, specificare Comctl32.dll versione 6 nel manifesto.</span><span class="sxs-lookup"><span data-stu-id="8e8ab-117">To use this notification code, specify Comctl32.dll version 6 in the manifest.</span></span> <span data-ttu-id="8e8ab-118">Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="8e8ab-118">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8e8ab-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8e8ab-119">Requirements</span></span>



| <span data-ttu-id="8e8ab-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e8ab-120">Requirement</span></span> | <span data-ttu-id="8e8ab-121">Valore</span><span class="sxs-lookup"><span data-stu-id="8e8ab-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8e8ab-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8e8ab-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8e8ab-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8e8ab-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8e8ab-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8e8ab-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8e8ab-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8e8ab-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8e8ab-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8e8ab-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e8ab-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e8ab-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





