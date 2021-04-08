---
title: Codice di notifica HDN_ENDTRACK (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di intestazione che l'utente ha terminato il trascinamento di un divisore. Questo codice di notifica è stato inviato sotto forma di \_ messaggio di notifica WM.
ms.assetid: d9b25871-7bd6-439c-91b8-e8249d9be67d
keywords:
- Controlli di Windows per il codice di notifica HDN_ENDTRACK
topic_type:
- apiref
api_name:
- HDN_ENDTRACK
- HDN_ENDTRACKA
- HDN_ENDTRACKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42ab7625690a2de0414f1da391f26f919c1c2617
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047938"
---
# <a name="hdn_endtrack-notification-code"></a><span data-ttu-id="12b74-105">\_Codice di notifica ENDTRACK di HDN</span><span class="sxs-lookup"><span data-stu-id="12b74-105">HDN\_ENDTRACK notification code</span></span>

<span data-ttu-id="12b74-106">Notifica alla finestra padre di un controllo di intestazione che l'utente ha terminato il trascinamento di un divisore.</span><span class="sxs-lookup"><span data-stu-id="12b74-106">Notifies a header control's parent window that the user has finished dragging a divider.</span></span> <span data-ttu-id="12b74-107">Questo codice di notifica è stato inviato sotto forma di messaggio di [**\_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="12b74-107">This notification code sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_ENDTRACK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="12b74-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="12b74-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12b74-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="12b74-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="12b74-110">Puntatore a una struttura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) contenente informazioni sul controllo intestazione e sull'elemento il cui divisore è stato trascinato.</span><span class="sxs-lookup"><span data-stu-id="12b74-110">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains information about the header control and the item whose divider was dragged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12b74-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="12b74-111">Return value</span></span>

<span data-ttu-id="12b74-112">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="12b74-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="12b74-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="12b74-113">Requirements</span></span>



| <span data-ttu-id="12b74-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="12b74-114">Requirement</span></span> | <span data-ttu-id="12b74-115">Valore</span><span class="sxs-lookup"><span data-stu-id="12b74-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="12b74-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="12b74-116">Minimum supported client</span></span><br/> | <span data-ttu-id="12b74-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="12b74-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="12b74-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="12b74-118">Minimum supported server</span></span><br/> | <span data-ttu-id="12b74-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="12b74-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="12b74-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="12b74-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="12b74-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="12b74-121"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="12b74-122">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="12b74-122">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="12b74-123">**HDN \_ ENDTRACKW** (Unicode) e **HDN \_ ENDTRACKA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="12b74-123">**HDN\_ENDTRACKW** (Unicode) and **HDN\_ENDTRACKA** (ANSI)</span></span><br/>                 |



 

 





