---
title: Messaggio PGN_HOTITEMCHANGE (COMmctrl. h)
description: Notifica alla finestra padre di un controllo pager che l'elemento attivo (evidenziato) è stato modificato. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 0f59677c-0251-49f4-b909-6fac6d93f354
keywords:
- Controlli di Windows Message PGN_HOTITEMCHANGE
topic_type:
- apiref
api_name:
- PGN_HOTITEMCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 573f3dd93a6e4b0b3db6682d36804416d6f6f1e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048257"
---
# <a name="pgn_hotitemchange-message"></a><span data-ttu-id="227e1-105">\_Messaggio PGN HOTITEMCHANGE</span><span class="sxs-lookup"><span data-stu-id="227e1-105">PGN\_HOTITEMCHANGE message</span></span>

<span data-ttu-id="227e1-106">Notifica alla finestra padre di un controllo pager che l'elemento attivo (evidenziato) è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="227e1-106">Notifies a pager control's parent window that the hot (highlighted) item has change.</span></span> <span data-ttu-id="227e1-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="227e1-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PGN_HOTITEMCHANGE

    pnmPGHotItem = (LPNMPGHOTITEM) lParam;
```



## <a name="parameters"></a><span data-ttu-id="227e1-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="227e1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="227e1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="227e1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="227e1-110">Puntatore a una struttura [**NMPGHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmpghotitem) che contiene informazioni su questo codice di notifica.</span><span class="sxs-lookup"><span data-stu-id="227e1-110">Pointer to a [**NMPGHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmpghotitem) structure that contains information about this notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="227e1-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="227e1-111">Return value</span></span>

<span data-ttu-id="227e1-112">Restituisce zero per evidenziare l'elemento o un valore diverso da zero per impedire l'evidenziazione.</span><span class="sxs-lookup"><span data-stu-id="227e1-112">Return zero to highlight the item or nonzero to prevent highlighting.</span></span>

## <a name="remarks"></a><span data-ttu-id="227e1-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="227e1-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="227e1-114">Per usare questo codice di notifica, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0.</span><span class="sxs-lookup"><span data-stu-id="227e1-114">To use this notification code, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="227e1-115">Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="227e1-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="227e1-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="227e1-116">Requirements</span></span>



| <span data-ttu-id="227e1-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="227e1-117">Requirement</span></span> | <span data-ttu-id="227e1-118">Valore</span><span class="sxs-lookup"><span data-stu-id="227e1-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="227e1-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="227e1-119">Minimum supported client</span></span><br/> | <span data-ttu-id="227e1-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="227e1-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="227e1-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="227e1-121">Minimum supported server</span></span><br/> | <span data-ttu-id="227e1-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="227e1-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="227e1-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="227e1-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="227e1-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="227e1-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





