---
title: Messaggio di MCIWNDM_SETZOOM (VFW. h)
description: Il \_ messaggio MCIWNDM di Zoom ridimensiona un'immagine video in base a un fattore di zoom. Questo Marco regola le dimensioni di una finestra MCIWnd mantenendo le proporzioni costanti. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro MCIWndSetZoom.
ms.assetid: c899b678-5ba7-4f0a-9ef9-c5370b3b4ea8
keywords:
- MCIWNDM_SETZOOM messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_SETZOOM
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80ecb513735c4e62266892e8ad55c7bf5daca151
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475515"
---
# <a name="mciwndm_setzoom-message"></a><span data-ttu-id="e4d2d-106">MCIWNDM- \_ messaggio di zoom</span><span class="sxs-lookup"><span data-stu-id="e4d2d-106">MCIWNDM\_SETZOOM message</span></span>

<span data-ttu-id="e4d2d-107">Il messaggio **MCIWNDM di \_ Zoom** ridimensiona un'immagine video in base a un fattore di zoom.</span><span class="sxs-lookup"><span data-stu-id="e4d2d-107">The **MCIWNDM\_SETZOOM** message resizes a video image according to a zoom factor.</span></span> <span data-ttu-id="e4d2d-108">Questo Marco regola le dimensioni di una finestra MCIWnd mantenendo le proporzioni costanti.</span><span class="sxs-lookup"><span data-stu-id="e4d2d-108">This marco adjusts the size of an MCIWnd window while maintaining a constant aspect ratio.</span></span> <span data-ttu-id="e4d2d-109">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndSetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetzoom) .</span><span class="sxs-lookup"><span data-stu-id="e4d2d-109">You can send this message explicitly or by using the [**MCIWndSetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetzoom) macro.</span></span>


```C++
MCIWNDM_SETZOOM 
wParam = 0; 
lParam = (LPARAM) (UINT) iZoom; 
```



## <a name="parameters"></a><span data-ttu-id="e4d2d-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="e4d2d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4d2d-111"><span id="iZoom"></span><span id="izoom"></span><span id="IZOOM"></span>*iZoom*</span><span class="sxs-lookup"><span data-stu-id="e4d2d-111"><span id="iZoom"></span><span id="izoom"></span><span id="IZOOM"></span>*iZoom*</span></span>
</dt> <dd>

<span data-ttu-id="e4d2d-112">Fattore di zoom espresso come percentuale dell'immagine originale.</span><span class="sxs-lookup"><span data-stu-id="e4d2d-112">Zoom factor expressed as a percentage of the original image.</span></span> <span data-ttu-id="e4d2d-113">Specificare 100 per visualizzare l'immagine alla dimensione creata, 200 per visualizzare l'immagine al doppio delle dimensioni normali o 50 per visualizzare l'immagine a metà delle dimensioni normali.</span><span class="sxs-lookup"><span data-stu-id="e4d2d-113">Specify 100 to display the image at its authored size, 200 to display the image at twice its normal size, or 50 to display the image at half its normal size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4d2d-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e4d2d-114">Return Value</span></span>

<span data-ttu-id="e4d2d-115">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="e4d2d-115">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4d2d-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e4d2d-116">Requirements</span></span>



| <span data-ttu-id="e4d2d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4d2d-117">Requirement</span></span> | <span data-ttu-id="e4d2d-118">Valore</span><span class="sxs-lookup"><span data-stu-id="e4d2d-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e4d2d-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e4d2d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e4d2d-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e4d2d-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="e4d2d-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e4d2d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e4d2d-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e4d2d-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e4d2d-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e4d2d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4d2d-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4d2d-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4d2d-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e4d2d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4d2d-126">**MCIWndSetZoom**</span><span class="sxs-lookup"><span data-stu-id="e4d2d-126">**MCIWndSetZoom**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndsetzoom)
</dt> </dl>

 

 





