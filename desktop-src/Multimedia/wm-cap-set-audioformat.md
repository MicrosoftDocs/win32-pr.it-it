---
title: Messaggio di WM_CAP_SET_AUDIOFORMAT (VFW. h)
description: Il \_ messaggio WM Cap \_ set \_ AUDIOFORMAT imposta il formato audio da usare quando si esegue lo streaming o l'acquisizione di passaggi. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro capSetAudioFormat.
ms.assetid: 8bffa401-3d36-43bb-9f69-988ebc69b860
keywords:
- WM_CAP_SET_AUDIOFORMAT messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WM_CAP_SET_AUDIOFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c519ed936d2e71d9eee88435a94acc8c567a9a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120086"
---
# <a name="wm_cap_set_audioformat-message"></a><span data-ttu-id="2de44-105">\_ \_ Messaggio AUDIOFORMAT set di estremità WM \_</span><span class="sxs-lookup"><span data-stu-id="2de44-105">WM\_CAP\_SET\_AUDIOFORMAT message</span></span>

<span data-ttu-id="2de44-106">Il messaggio **WM \_ Cap \_ set \_ AUDIOFORMAT** imposta il formato audio da usare quando si esegue lo streaming o l'acquisizione di passaggi.</span><span class="sxs-lookup"><span data-stu-id="2de44-106">The **WM\_CAP\_SET\_AUDIOFORMAT** message sets the audio format to use when performing streaming or step capture.</span></span> <span data-ttu-id="2de44-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**capSetAudioFormat**](/windows/desktop/api/Vfw/nf-vfw-capsetaudioformat) .</span><span class="sxs-lookup"><span data-stu-id="2de44-107">You can send this message explicitly or by using the [**capSetAudioFormat**](/windows/desktop/api/Vfw/nf-vfw-capsetaudioformat) macro.</span></span>


```C++
WM_CAP_SET_AUDIOFORMAT 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPWAVEFORMATEX) (psAudioFormat); 
```



## <a name="parameters"></a><span data-ttu-id="2de44-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="2de44-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2de44-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span><span class="sxs-lookup"><span data-stu-id="2de44-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="2de44-110">Dimensione, in byte, della struttura a cui fa riferimento **s**.</span><span class="sxs-lookup"><span data-stu-id="2de44-110">Size, in bytes, of the structure referenced by **s**.</span></span>

</dd> <dt>

<span data-ttu-id="2de44-111"><span id="psAudioFormat"></span><span id="psaudioformat"></span><span id="PSAUDIOFORMAT"></span>*psAudioFormat*</span><span class="sxs-lookup"><span data-stu-id="2de44-111"><span id="psAudioFormat"></span><span id="psaudioformat"></span><span id="PSAUDIOFORMAT"></span>*psAudioFormat*</span></span>
</dt> <dd>

<span data-ttu-id="2de44-112">Puntatore a una struttura [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) o [**PCMWAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-pcmwaveformat) che definisce il formato audio.</span><span class="sxs-lookup"><span data-stu-id="2de44-112">Pointer to a [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) or [**PCMWAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-pcmwaveformat) structure that defines the audio format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2de44-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2de44-113">Return Value</span></span>

<span data-ttu-id="2de44-114">Restituisce **true** se l'operazione è riuscita o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="2de44-114">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="2de44-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2de44-115">Requirements</span></span>



| <span data-ttu-id="2de44-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="2de44-116">Requirement</span></span> | <span data-ttu-id="2de44-117">Valore</span><span class="sxs-lookup"><span data-stu-id="2de44-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="2de44-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2de44-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2de44-119">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2de44-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="2de44-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2de44-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2de44-121">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2de44-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="2de44-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2de44-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="2de44-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="2de44-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2de44-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2de44-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2de44-125">Acquisizione video</span><span class="sxs-lookup"><span data-stu-id="2de44-125">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="2de44-126">Messaggi di acquisizione video</span><span class="sxs-lookup"><span data-stu-id="2de44-126">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

