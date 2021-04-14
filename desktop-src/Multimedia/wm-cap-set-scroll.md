---
title: Messaggio di WM_CAP_SET_SCROLL (VFW. h)
description: Il messaggio di scorrimento di WM \_ Cap \_ set \_ definisce la parte del fotogramma video da visualizzare nella finestra di acquisizione.
ms.assetid: 545605e4-6b1f-403a-a3ab-0fd6750ae776
keywords:
- WM_CAP_SET_SCROLL messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WM_CAP_SET_SCROLL
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 812b76bdcad166b9f766957032f232293d4083c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479054"
---
# <a name="wm_cap_set_scroll-message"></a><span data-ttu-id="cfd3d-104">\_Messaggio di \_ scorrimento set di estremità WM \_</span><span class="sxs-lookup"><span data-stu-id="cfd3d-104">WM\_CAP\_SET\_SCROLL message</span></span>

<span data-ttu-id="cfd3d-105">Il messaggio di **scorrimento di WM \_ Cap \_ set \_** definisce la parte del fotogramma video da visualizzare nella finestra di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="cfd3d-105">The **WM\_CAP\_SET\_SCROLL** message defines the portion of the video frame to display in the capture window.</span></span> <span data-ttu-id="cfd3d-106">Questo messaggio imposta l'angolo superiore sinistro dell'area client della finestra di acquisizione sulle coordinate di un pixel specificato all'interno del frame del video.</span><span class="sxs-lookup"><span data-stu-id="cfd3d-106">This message sets the upper left corner of the client area of the capture window to the coordinates of a specified pixel within the video frame.</span></span> <span data-ttu-id="cfd3d-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capSetScrollPos**](/windows/desktop/api/Vfw/nf-vfw-capsetscrollpos) .</span><span class="sxs-lookup"><span data-stu-id="cfd3d-107">You can send this message explicitly or by using the [**capSetScrollPos**](/windows/desktop/api/Vfw/nf-vfw-capsetscrollpos) macro.</span></span>


```C++
WM_CAP_SET_SCROLL 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPPOINT) (lpP); 
```



## <a name="parameters"></a><span data-ttu-id="cfd3d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="cfd3d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfd3d-109"><span id="lpP"></span><span id="lpp"></span><span id="LPP"></span>*lpP*</span><span class="sxs-lookup"><span data-stu-id="cfd3d-109"><span id="lpP"></span><span id="lpp"></span><span id="LPP"></span>*lpP*</span></span>
</dt> <dd>

<span data-ttu-id="cfd3d-110">Indirizzo per contenere la posizione di scorrimento desiderata.</span><span class="sxs-lookup"><span data-stu-id="cfd3d-110">Address to contain the desired scroll position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfd3d-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cfd3d-111">Return Value</span></span>

<span data-ttu-id="cfd3d-112">Restituisce **true** se l'operazione è riuscita o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="cfd3d-112">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="cfd3d-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="cfd3d-113">Remarks</span></span>

<span data-ttu-id="cfd3d-114">La posizione di scorrimento influiscono sull'immagine nelle modalità anteprima e sovrapposizione.</span><span class="sxs-lookup"><span data-stu-id="cfd3d-114">The scroll position affects the image in both preview and overlay modes.</span></span>

## <a name="requirements"></a><span data-ttu-id="cfd3d-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cfd3d-115">Requirements</span></span>



| <span data-ttu-id="cfd3d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="cfd3d-116">Requirement</span></span> | <span data-ttu-id="cfd3d-117">Valore</span><span class="sxs-lookup"><span data-stu-id="cfd3d-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="cfd3d-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cfd3d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="cfd3d-119">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="cfd3d-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="cfd3d-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cfd3d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="cfd3d-121">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="cfd3d-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="cfd3d-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cfd3d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="cfd3d-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="cfd3d-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfd3d-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cfd3d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfd3d-125">Acquisizione video</span><span class="sxs-lookup"><span data-stu-id="cfd3d-125">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="cfd3d-126">Messaggi di acquisizione video</span><span class="sxs-lookup"><span data-stu-id="cfd3d-126">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





