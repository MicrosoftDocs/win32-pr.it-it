---
title: Codice di notifica HDN_TRACK (COMmctrl. h)
description: Notifica alla finestra padre di un controllo di intestazione che l'utente sta trascinando un divisore nel controllo intestazione. Questo codice di notifica viene inviato sotto forma di messaggio di \_ notifica WM.
ms.assetid: 26660ae1-0d6e-4ee7-8b6a-d621abef352d
keywords:
- Controlli di Windows per il codice di notifica HDN_TRACK
topic_type:
- apiref
api_name:
- HDN_TRACK
- HDN_TRACKA
- HDN_TRACKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91b55ac23e2de17788b17c1f121530308de9e7a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874118"
---
# <a name="hdn_track-notification-code"></a><span data-ttu-id="c99fe-105">HDN \_ traccia del codice di notifica</span><span class="sxs-lookup"><span data-stu-id="c99fe-105">HDN\_TRACK notification code</span></span>

<span data-ttu-id="c99fe-106">Notifica alla finestra padre di un controllo di intestazione che l'utente sta trascinando un divisore nel controllo intestazione.</span><span class="sxs-lookup"><span data-stu-id="c99fe-106">Notifies a header control's parent window that the user is dragging a divider in the header control.</span></span> <span data-ttu-id="c99fe-107">Questo codice di notifica viene inviato sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="c99fe-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_TRACK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="c99fe-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="c99fe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c99fe-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c99fe-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c99fe-110">Puntatore a una struttura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) contenente informazioni sul controllo intestazione e sull'elemento il cui divisore viene trascinato.</span><span class="sxs-lookup"><span data-stu-id="c99fe-110">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains information about the header control and the item whose divider is being dragged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c99fe-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c99fe-111">Return value</span></span>

<span data-ttu-id="c99fe-112">Restituisce **false** per continuare a tenere traccia del divisore o **true** per terminare la verifica.</span><span class="sxs-lookup"><span data-stu-id="c99fe-112">Returns **FALSE** to continue tracking the divider, or **TRUE** to end tracking.</span></span>

## <a name="requirements"></a><span data-ttu-id="c99fe-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c99fe-113">Requirements</span></span>



| <span data-ttu-id="c99fe-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="c99fe-114">Requirement</span></span> | <span data-ttu-id="c99fe-115">Valore</span><span class="sxs-lookup"><span data-stu-id="c99fe-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c99fe-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c99fe-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c99fe-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c99fe-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c99fe-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c99fe-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c99fe-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c99fe-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c99fe-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c99fe-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c99fe-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c99fe-121"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="c99fe-122">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="c99fe-122">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="c99fe-123">**HDN \_ TRACKW** (Unicode) e **HDN \_ tracka** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="c99fe-123">**HDN\_TRACKW** (Unicode) and **HDN\_TRACKA** (ANSI)</span></span><br/>                       |



 

 





