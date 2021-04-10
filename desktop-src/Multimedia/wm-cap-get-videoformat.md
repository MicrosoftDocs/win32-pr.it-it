---
title: Messaggio di WM_CAP_GET_VIDEOFORMAT (VFW. h)
description: Il \_ messaggio WM Cap \_ get \_ VIDEOFORMAT recupera una copia del formato video in uso o le dimensioni necessarie per il formato video. È possibile inviare questo messaggio in modo esplicito o usando le macro capGetVideoFormat e capGetVideoFormatSize.
ms.assetid: ac72dfdb-fe1a-4007-bdce-41e5e67d076a
keywords:
- WM_CAP_GET_VIDEOFORMAT messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WM_CAP_GET_VIDEOFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 072d71366efee550b037d4a20388817954937854
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964187"
---
# <a name="wm_cap_get_videoformat-message"></a><span data-ttu-id="f1eea-105">\_ \_ \_ Messaggio VIDEOFORMAT di WM Cap</span><span class="sxs-lookup"><span data-stu-id="f1eea-105">WM\_CAP\_GET\_VIDEOFORMAT message</span></span>

<span data-ttu-id="f1eea-106">Il messaggio **WM \_ Cap \_ get \_ VIDEOFORMAT** recupera una copia del formato video in uso o le dimensioni necessarie per il formato video.</span><span class="sxs-lookup"><span data-stu-id="f1eea-106">The **WM\_CAP\_GET\_VIDEOFORMAT** message retrieves a copy of the video format in use or the size required for the video format.</span></span> <span data-ttu-id="f1eea-107">È possibile inviare questo messaggio in modo esplicito o usando le macro [**capGetVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformat) e [**capGetVideoFormatSize**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformatsize) .</span><span class="sxs-lookup"><span data-stu-id="f1eea-107">You can send this message explicitly or by using the [**capGetVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformat) and [**capGetVideoFormatSize**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformatsize) macros.</span></span>


```C++
WM_CAP_GET_VIDEOFORMAT 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (psVideoFormat); 
```



## <a name="parameters"></a><span data-ttu-id="f1eea-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f1eea-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1eea-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span><span class="sxs-lookup"><span data-stu-id="f1eea-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="f1eea-110">Dimensione, in byte, della struttura a cui fa riferimento **s**.</span><span class="sxs-lookup"><span data-stu-id="f1eea-110">Size, in bytes, of the structure referenced by **s**.</span></span>

</dd> <dt>

<span data-ttu-id="f1eea-111"><span id="psVideoFormat"></span><span id="psvideoformat"></span><span id="PSVIDEOFORMAT"></span>*psVideoFormat*</span><span class="sxs-lookup"><span data-stu-id="f1eea-111"><span id="psVideoFormat"></span><span id="psvideoformat"></span><span id="PSVIDEOFORMAT"></span>*psVideoFormat*</span></span>
</dt> <dd>

<span data-ttu-id="f1eea-112">Puntatore a una struttura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) .</span><span class="sxs-lookup"><span data-stu-id="f1eea-112">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure.</span></span> <span data-ttu-id="f1eea-113">È anche possibile specificare **null** per recuperare il numero di byte necessari.</span><span class="sxs-lookup"><span data-stu-id="f1eea-113">You can also specify **NULL** to retrieve the number of bytes needed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1eea-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f1eea-114">Return Value</span></span>

<span data-ttu-id="f1eea-115">Restituisce la dimensione, in byte, del formato video o zero se la finestra di acquisizione non è connessa a un driver di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="f1eea-115">Returns the size, in bytes, of the video format or zero if the capture window is not connected to a capture driver.</span></span> <span data-ttu-id="f1eea-116">Per i formati video che richiedono una tavolozza, viene restituita anche la tavolozza corrente.</span><span class="sxs-lookup"><span data-stu-id="f1eea-116">For video formats that require a palette, the current palette is also returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1eea-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="f1eea-117">Remarks</span></span>

<span data-ttu-id="f1eea-118">Poiché i formati video compressi variano in requisiti di dimensioni, le applicazioni devono prima recuperare le dimensioni, quindi allocare memoria e infine richiedere i dati in formato video.</span><span class="sxs-lookup"><span data-stu-id="f1eea-118">Because compressed video formats vary in size requirements applications must first retrieve the size, then allocate memory, and finally request the video format data.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1eea-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f1eea-119">Requirements</span></span>



| <span data-ttu-id="f1eea-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1eea-120">Requirement</span></span> | <span data-ttu-id="f1eea-121">Valore</span><span class="sxs-lookup"><span data-stu-id="f1eea-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f1eea-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f1eea-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f1eea-123">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f1eea-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="f1eea-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f1eea-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f1eea-125">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f1eea-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f1eea-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f1eea-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1eea-127"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1eea-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1eea-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f1eea-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1eea-129">Acquisizione video</span><span class="sxs-lookup"><span data-stu-id="f1eea-129">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="f1eea-130">Messaggi di acquisizione video</span><span class="sxs-lookup"><span data-stu-id="f1eea-130">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

