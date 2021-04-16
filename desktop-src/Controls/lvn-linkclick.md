---
title: Codice di notifica LVN_LINKCLICK (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di visualizzazione elenco che è stato fatto clic su un collegamento. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: de8f40d6-b79e-4324-af67-9a3c0915609d
keywords:
- Controlli di Windows per il codice di notifica LVN_LINKCLICK
topic_type:
- apiref
api_name:
- LVN_LINKCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd69fb463e71523fcbd4eeb65a6a718d27847c09
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479432"
---
# <a name="lvn_linkclick-notification-code"></a><span data-ttu-id="43a86-105">\_Codice di notifica LINKCLICK di LVN</span><span class="sxs-lookup"><span data-stu-id="43a86-105">LVN\_LINKCLICK notification code</span></span>

<span data-ttu-id="43a86-106">Notifica alla finestra padre di un controllo di visualizzazione elenco che è stato fatto clic su un collegamento.</span><span class="sxs-lookup"><span data-stu-id="43a86-106">Notifies a list-view control's parent window that a link has been clicked on.</span></span> <span data-ttu-id="43a86-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="43a86-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_LINKCLICK
        
    pLinkInfo = (NMLVLINK*) lParam;         
```



## <a name="parameters"></a><span data-ttu-id="43a86-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="43a86-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43a86-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="43a86-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="43a86-110">Puntatore a una struttura [**NMLVLINK**](/windows/win32/api/commctrl/ns-commctrl-nmlvlink) .</span><span class="sxs-lookup"><span data-stu-id="43a86-110">Pointer to an [**NMLVLINK**](/windows/win32/api/commctrl/ns-commctrl-nmlvlink) structure.</span></span> <span data-ttu-id="43a86-111">L'identificatore del gruppo contenente il collegamento si trova nel membro **iSubItem** .</span><span class="sxs-lookup"><span data-stu-id="43a86-111">The identifier of the group containing the link is in the **iSubItem** member.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43a86-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="43a86-112">Return value</span></span>

<span data-ttu-id="43a86-113">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="43a86-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="43a86-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="43a86-114">Remarks</span></span>

<span data-ttu-id="43a86-115">Nell'esempio seguente viene illustrato il modo in cui un'applicazione può rispondere a questo codice di notifica nel gestore di messaggi di [**\_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="43a86-115">The following example shows how an application might respond to this notification code in its [**WM\_NOTIFY**](wm-notify.md) message handler.</span></span> <span data-ttu-id="43a86-116">Nell'esempio viene attivato o disattivato lo stato compresso del gruppo e viene impostato il testo del collegamento appropriato.</span><span class="sxs-lookup"><span data-stu-id="43a86-116">The example toggles the collapsed state of the group and sets the appropriate link text.</span></span>

``` syntax
case LVN_LINKCLICK:
{
    NMLVLINK* pLinkInfo = (NMLVLINK*)lParam;
    HWND hList = pLinkInfo->hdr.hwndFrom;
    LVGROUP groupInfo;
    groupInfo.cbSize = sizeof(groupInfo);
    groupInfo.mask = LVGF_TASK;
    int groupIndex = pLinkInfo->iSubItem;
    if (ListView_GetGroupState(hList, groupIndex, LVGS_COLLAPSED))
    {
        ListView_SetGroupState(hList, groupIndex, LVGS_COLLAPSED, 0);
        groupInfo.pszTask = L"Hide";
    }
    else
    {
        ListView_SetGroupState(hList, groupIndex, LVGS_COLLAPSED, LVGS_COLLAPSED);
        groupInfo.pszTask = L"Show";
     }
      ListView_SetGroupInfo(hList, groupIndex, &groupInfo);
      break;
}
```

## <a name="requirements"></a><span data-ttu-id="43a86-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="43a86-117">Requirements</span></span>



| <span data-ttu-id="43a86-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="43a86-118">Requirement</span></span> | <span data-ttu-id="43a86-119">Valore</span><span class="sxs-lookup"><span data-stu-id="43a86-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="43a86-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="43a86-120">Minimum supported client</span></span><br/> | <span data-ttu-id="43a86-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="43a86-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="43a86-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="43a86-122">Minimum supported server</span></span><br/> | <span data-ttu-id="43a86-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="43a86-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="43a86-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="43a86-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="43a86-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="43a86-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





