---
description: Di seguito sono riportate le costanti di gesti rapidi.
ms.assetid: 21aaf8f0-13b7-4f97-ad4a-3557a7020337
title: Scorre le costanti (Tabflicks. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b9a83f9a35a2c1a9cbd7c4b048a8c985f5eea34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129535"
---
# <a name="flicks-constants"></a><span data-ttu-id="404c7-103">Costanti rapide</span><span class="sxs-lookup"><span data-stu-id="404c7-103">Flicks Constants</span></span>

<span data-ttu-id="404c7-104">Di seguito sono riportate le costanti di gesti rapidi.</span><span class="sxs-lookup"><span data-stu-id="404c7-104">The following are the Flicks constants.</span></span>



| <span data-ttu-id="404c7-105">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="404c7-105">Constant/value</span></span>                                                                                                                                                                                                                                   | <span data-ttu-id="404c7-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="404c7-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FLICK_WM_HANDLED_MASK"></span><span id="flick_wm_handled_mask"></span><dl> <span data-ttu-id="404c7-107"><dt>**Gesto rapido \_ 0x1 \_ \_ maschera gestita WM**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="404c7-107"><dt>**FLICK\_WM\_HANDLED\_MASK**</dt> <dt>0x1</dt></span></span> </dl> | <span data-ttu-id="404c7-108">Valore da restituire dopo la gestione del messaggio del [**\_ messaggio del messaggio di \_ scorrimento del Tablet WM**](wm-tablet-flick-message.md) .</span><span class="sxs-lookup"><span data-stu-id="404c7-108">The value to return after handling the [**WM\_TABLET\_FLICK Message**](wm-tablet-flick-message.md) message.</span></span> <span data-ttu-id="404c7-109">Se viene restituita la **\_ \_ \_ maschera gestibile con scorrimento rapido** , non viene eseguita alcuna azione.</span><span class="sxs-lookup"><span data-stu-id="404c7-109">If **FLICK\_WM\_HANDLED\_MASK** is returned, no further action occurs.</span></span> <span data-ttu-id="404c7-110">In caso contrario, Windows invia notifiche di completamento, ad esempio [**WM \_ APPCOMMAND**](/windows/desktop/inputdev/wm-appcommand), [**WM \_ VSCROLL**](/windows/desktop/Controls/wm-vscroll)o [**WM \_ KeyDown**](/windows/desktop/inputdev/wm-keydown), a seconda dell'azione associata al gesto rapido della penna.</span><span class="sxs-lookup"><span data-stu-id="404c7-110">Otherwise, Windows sends follow-up notifications, such as [**WM\_APPCOMMAND**](/windows/desktop/inputdev/wm-appcommand), [**WM\_VSCROLL**](/windows/desktop/Controls/wm-vscroll), or [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown), depending on which action is associated with the pen flick.</span></span> <br/> |
| <span id="NUM_FLICK_DIRECTIONS"></span><span id="num_flick_directions"></span><dl> <span data-ttu-id="404c7-111">Numero di <dt>**\_ \_Direzioni di scorrimento**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="404c7-111"><dt>**NUM\_FLICK\_DIRECTIONS**</dt> <dt>8</dt></span></span> </dl>       | <span data-ttu-id="404c7-112">Il numero di direzioni definito nell'enumerazione [**FLICKDIRECTION**](/windows/desktop/api/tabflicks/ne-tabflicks-flickdirection) .</span><span class="sxs-lookup"><span data-stu-id="404c7-112">The number of directions defined in the [**FLICKDIRECTION**](/windows/desktop/api/tabflicks/ne-tabflicks-flickdirection) enumeration.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                              |



## <a name="requirements"></a><span data-ttu-id="404c7-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="404c7-113">Requirements</span></span>



| <span data-ttu-id="404c7-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="404c7-114">Requirement</span></span> | <span data-ttu-id="404c7-115">Valore</span><span class="sxs-lookup"><span data-stu-id="404c7-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="404c7-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="404c7-116">Minimum supported client</span></span><br/> | <span data-ttu-id="404c7-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="404c7-117">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="404c7-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="404c7-118">Minimum supported server</span></span><br/> | <span data-ttu-id="404c7-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="404c7-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="404c7-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="404c7-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="404c7-121"><dt>Tabflicks. h</dt></span><span class="sxs-lookup"><span data-stu-id="404c7-121"><dt>Tabflicks.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="404c7-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="404c7-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="404c7-123">**Enumerazione FLICKDIRECTION**</span><span class="sxs-lookup"><span data-stu-id="404c7-123">**FLICKDIRECTION Enumeration**</span></span>](/windows/desktop/api/tabflicks/ne-tabflicks-flickdirection)
</dt> <dt>

[<span data-ttu-id="404c7-124">**\_Messaggio di \_ scorrimento rapido del Tablet WM**</span><span class="sxs-lookup"><span data-stu-id="404c7-124">**WM\_TABLET\_FLICK Message**</span></span>](wm-tablet-flick-message.md)
</dt> <dt>

[<span data-ttu-id="404c7-125">Movimenti rapidi</span><span class="sxs-lookup"><span data-stu-id="404c7-125">Flicks Gestures</span></span>](flicks-gestures.md)
</dt> <dt>

<span data-ttu-id="404c7-126">[Risposta ai gesti rapidi della penna](/previous-versions//dd356077(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="404c7-126">[Responding to Pen Flicks](/previous-versions//dd356077(v=vs.85))</span></span>
</dt> </dl>

 

