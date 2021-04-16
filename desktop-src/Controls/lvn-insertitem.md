---
title: Codice di notifica LVN_INSERTITEM (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di visualizzazione elenco che è stato inserito un nuovo elemento. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 8d368fb2-e4fc-4dc4-a89e-872ba1278b75
keywords:
- Controlli di Windows per il codice di notifica LVN_INSERTITEM
topic_type:
- apiref
api_name:
- LVN_INSERTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba70ba806dea2725385badee4b5c57e927a9d42b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479440"
---
# <a name="lvn_insertitem-notification-code"></a><span data-ttu-id="1f8da-105">Codice di notifica di LVN \_ INSERTITEM</span><span class="sxs-lookup"><span data-stu-id="1f8da-105">LVN\_INSERTITEM notification code</span></span>

<span data-ttu-id="1f8da-106">Notifica alla finestra padre di un controllo di visualizzazione elenco che è stato inserito un nuovo elemento.</span><span class="sxs-lookup"><span data-stu-id="1f8da-106">Notifies a list-view control's parent window that a new item was inserted.</span></span> <span data-ttu-id="1f8da-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="1f8da-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_INSERTITEM

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="1f8da-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="1f8da-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f8da-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1f8da-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1f8da-110">Puntatore a una struttura [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) .</span><span class="sxs-lookup"><span data-stu-id="1f8da-110">Pointer to an [**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) structure.</span></span> <span data-ttu-id="1f8da-111">Il membro **iItem** identifica il nuovo elemento e gli altri membri sono pari a zero.</span><span class="sxs-lookup"><span data-stu-id="1f8da-111">The **iItem** member identifies the new item, and the other members are zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f8da-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1f8da-112">Return value</span></span>

<span data-ttu-id="1f8da-113">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="1f8da-113">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f8da-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1f8da-114">Requirements</span></span>



| <span data-ttu-id="1f8da-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f8da-115">Requirement</span></span> | <span data-ttu-id="1f8da-116">Valore</span><span class="sxs-lookup"><span data-stu-id="1f8da-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1f8da-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1f8da-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1f8da-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1f8da-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1f8da-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1f8da-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1f8da-120">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1f8da-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1f8da-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1f8da-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f8da-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f8da-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





