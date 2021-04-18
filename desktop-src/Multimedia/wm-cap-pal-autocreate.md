---
title: Messaggio di WM_CAP_PAL_AUTOCREATE (VFW. h)
description: Il \_ messaggio WM Cap \_ PAL \_ creazione automatica richiede che il driver di acquisizione fotogrammi video di esempio e crei automaticamente una nuova tavolozza. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro capPaletteAuto.
ms.assetid: b94d245d-adf4-4fe0-b053-87109ef5fd2f
keywords:
- WM_CAP_PAL_AUTOCREATE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WM_CAP_PAL_AUTOCREATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ba70de46167121aa9a83959c6d9e202039f65cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301371"
---
# <a name="wm_cap_pal_autocreate-message"></a><span data-ttu-id="2d521-105">\_Messaggio di \_ \_ creazione autocreata di WM Cap PAL</span><span class="sxs-lookup"><span data-stu-id="2d521-105">WM\_CAP\_PAL\_AUTOCREATE message</span></span>

<span data-ttu-id="2d521-106">Il messaggio **WM \_ Cap \_ PAL \_ creazione** automatica richiede che il driver di acquisizione fotogrammi video di esempio e crei automaticamente una nuova tavolozza.</span><span class="sxs-lookup"><span data-stu-id="2d521-106">The **WM\_CAP\_PAL\_AUTOCREATE** message requests that the capture driver sample video frames and automatically create a new palette.</span></span> <span data-ttu-id="2d521-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capPaletteAuto**](/windows/desktop/api/Vfw/nf-vfw-cappaletteauto) .</span><span class="sxs-lookup"><span data-stu-id="2d521-107">You can send this message explicitly or by using the [**capPaletteAuto**](/windows/desktop/api/Vfw/nf-vfw-cappaletteauto) macro.</span></span>


```C++
WM_CAP_PAL_AUTOCREATE 
wParam = (WPARAM) (iFrames); 
lParam = (LPARAM) (DWORD) (iColors); 
```



## <a name="parameters"></a><span data-ttu-id="2d521-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="2d521-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d521-109"><span id="iFrames"></span><span id="iframes"></span><span id="IFRAMES"></span>*iFrames*</span><span class="sxs-lookup"><span data-stu-id="2d521-109"><span id="iFrames"></span><span id="iframes"></span><span id="IFRAMES"></span>*iFrames*</span></span>
</dt> <dd>

<span data-ttu-id="2d521-110">Numero di frame da campionare.</span><span class="sxs-lookup"><span data-stu-id="2d521-110">Number of frames to sample.</span></span>

</dd> <dt>

<span data-ttu-id="2d521-111"><span id="iColors"></span><span id="icolors"></span><span id="ICOLORS"></span>*iColors*</span><span class="sxs-lookup"><span data-stu-id="2d521-111"><span id="iColors"></span><span id="icolors"></span><span id="ICOLORS"></span>*iColors*</span></span>
</dt> <dd>

<span data-ttu-id="2d521-112">Numero di colori nella tavolozza.</span><span class="sxs-lookup"><span data-stu-id="2d521-112">Number of colors in the palette.</span></span> <span data-ttu-id="2d521-113">Il valore massimo per questo parametro è 256.</span><span class="sxs-lookup"><span data-stu-id="2d521-113">The maximum value for this parameter is 256.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d521-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2d521-114">Return Value</span></span>

<span data-ttu-id="2d521-115">Restituisce **true** se l'operazione è riuscita o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="2d521-115">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

<span data-ttu-id="2d521-116">Se si verifica un errore e viene impostata una funzione di callback di errore utilizzando il messaggio di errore di richiamata di [**WM \_ Cap \_ set \_ \_**](wm-cap-set-callback-error.md) , viene chiamata la funzione di callback dell'errore.</span><span class="sxs-lookup"><span data-stu-id="2d521-116">If an error occurs and an error callback function is set using the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) message, the error callback function is called.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d521-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="2d521-117">Remarks</span></span>

<span data-ttu-id="2d521-118">La sequenza video campionata deve includere tutti i colori desiderati nella tavolozza.</span><span class="sxs-lookup"><span data-stu-id="2d521-118">The sampled video sequence should include all the colors you want in the palette.</span></span> <span data-ttu-id="2d521-119">Per ottenere la tavolozza migliore, potrebbe essere necessario campionare l'intera sequenza anziché una parte di esso.</span><span class="sxs-lookup"><span data-stu-id="2d521-119">To obtain the best palette, you might have to sample the whole sequence rather than a portion of it.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d521-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2d521-120">Requirements</span></span>



| <span data-ttu-id="2d521-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d521-121">Requirement</span></span> | <span data-ttu-id="2d521-122">Valore</span><span class="sxs-lookup"><span data-stu-id="2d521-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="2d521-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2d521-123">Minimum supported client</span></span><br/> | <span data-ttu-id="2d521-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2d521-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="2d521-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2d521-125">Minimum supported server</span></span><br/> | <span data-ttu-id="2d521-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2d521-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="2d521-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2d521-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d521-128"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d521-128"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d521-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2d521-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d521-130">Acquisizione video</span><span class="sxs-lookup"><span data-stu-id="2d521-130">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="2d521-131">Messaggi di acquisizione video</span><span class="sxs-lookup"><span data-stu-id="2d521-131">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





