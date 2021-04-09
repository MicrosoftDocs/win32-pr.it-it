---
title: Messaggio di WM_CAP_PAL_MANUALCREATE (VFW. h)
description: Il \_ messaggio MANUALCREATE di WM Cap \_ \_ richiede che il driver di acquisizione campiona manualmente i fotogrammi video e crei una nuova tavolozza. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro capPaletteManual.
ms.assetid: 96b6b2d6-084a-411e-8495-ea27e0c4f04f
keywords:
- WM_CAP_PAL_MANUALCREATE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WM_CAP_PAL_MANUALCREATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dfd5b6588381ede0faaae539d3d8418b041f458
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740959"
---
# <a name="wm_cap_pal_manualcreate-message"></a><span data-ttu-id="974db-105">\_Messaggio MANUALCREATE di WM Cap \_ PAL \_</span><span class="sxs-lookup"><span data-stu-id="974db-105">WM\_CAP\_PAL\_MANUALCREATE message</span></span>

<span data-ttu-id="974db-106">Il **messaggio \_ \_ \_ MANUALCREATE di WM Cap** richiede che il driver di acquisizione campiona manualmente i fotogrammi video e crei una nuova tavolozza.</span><span class="sxs-lookup"><span data-stu-id="974db-106">The **WM\_CAP\_PAL\_MANUALCREATE** message requests that the capture driver manually sample video frames and create a new palette.</span></span> <span data-ttu-id="974db-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capPaletteManual**](/windows/desktop/api/Vfw/nf-vfw-cappalettemanual) .</span><span class="sxs-lookup"><span data-stu-id="974db-107">You can send this message explicitly or by using the [**capPaletteManual**](/windows/desktop/api/Vfw/nf-vfw-cappalettemanual) macro.</span></span>


```C++
WM_CAP_PAL_MANUALCREATE 
wParam = (WPARAM) (fGrab); 
lParam = (LPARAM) (DWORD) (iColors); 
```



## <a name="parameters"></a><span data-ttu-id="974db-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="974db-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="974db-109"><span id="fGrab"></span><span id="fgrab"></span><span id="FGRAB"></span>*fGrab*</span><span class="sxs-lookup"><span data-stu-id="974db-109"><span id="fGrab"></span><span id="fgrab"></span><span id="FGRAB"></span>*fGrab*</span></span>
</dt> <dd>

<span data-ttu-id="974db-110">Flag istogramma tavolozza.</span><span class="sxs-lookup"><span data-stu-id="974db-110">Palette histogram flag.</span></span> <span data-ttu-id="974db-111">Impostare questo parametro su **true** per ogni frame incluso nella creazione della tavolozza ottimale.</span><span class="sxs-lookup"><span data-stu-id="974db-111">Set this parameter to **TRUE** for each frame included in creating the optimal palette.</span></span> <span data-ttu-id="974db-112">Dopo che l'ultimo frame è stato raccolto, impostare questo parametro su **false** per calcolare la tavolozza ottimale e inviarla al driver di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="974db-112">After the last frame has been collected, set this parameter to **FALSE** to calculate the optimal palette and send it to the capture driver.</span></span>

</dd> <dt>

<span data-ttu-id="974db-113"><span id="iColors"></span><span id="icolors"></span><span id="ICOLORS"></span>*iColors*</span><span class="sxs-lookup"><span data-stu-id="974db-113"><span id="iColors"></span><span id="icolors"></span><span id="ICOLORS"></span>*iColors*</span></span>
</dt> <dd>

<span data-ttu-id="974db-114">Numero di colori nella tavolozza.</span><span class="sxs-lookup"><span data-stu-id="974db-114">Number of colors in the palette.</span></span> <span data-ttu-id="974db-115">Il valore massimo per questo parametro è 256.</span><span class="sxs-lookup"><span data-stu-id="974db-115">The maximum value for this parameter is 256.</span></span> <span data-ttu-id="974db-116">Questo valore viene usato solo durante la raccolta del primo frame in una sequenza.</span><span class="sxs-lookup"><span data-stu-id="974db-116">This value is used only during collection of the first frame in a sequence.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="974db-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="974db-117">Return Value</span></span>

<span data-ttu-id="974db-118">Restituisce **true** se l'operazione è riuscita o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="974db-118">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

<span data-ttu-id="974db-119">Se si verifica un errore e viene impostata una funzione di callback di errore utilizzando il messaggio di errore di richiamata di [**WM \_ Cap \_ set \_ \_**](wm-cap-set-callback-error.md) , viene chiamata la funzione di callback dell'errore.</span><span class="sxs-lookup"><span data-stu-id="974db-119">If an error occurs and an error callback function is set using the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) message, the error callback function is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="974db-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="974db-120">Requirements</span></span>



| <span data-ttu-id="974db-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="974db-121">Requirement</span></span> | <span data-ttu-id="974db-122">Valore</span><span class="sxs-lookup"><span data-stu-id="974db-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="974db-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="974db-123">Minimum supported client</span></span><br/> | <span data-ttu-id="974db-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="974db-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="974db-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="974db-125">Minimum supported server</span></span><br/> | <span data-ttu-id="974db-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="974db-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="974db-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="974db-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="974db-128"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="974db-128"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="974db-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="974db-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="974db-130">Acquisizione video</span><span class="sxs-lookup"><span data-stu-id="974db-130">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="974db-131">Messaggi di acquisizione video</span><span class="sxs-lookup"><span data-stu-id="974db-131">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





