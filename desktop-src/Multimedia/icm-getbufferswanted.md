---
title: Messaggio di ICM_GETBUFFERSWANTED (VFW. h)
description: Il \_ messaggio MCI GETBUFFERSWANTED esegue una query su un driver per il numero di buffer da allocare. È possibile inviare questo messaggio in modo esplicito o utilizzando la macro ICGetBuffersWanted.
ms.assetid: 109e8627-7ed4-4f17-bf7f-e77f42dfc8c7
keywords:
- ICM_GETBUFFERSWANTED messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- ICM_GETBUFFERSWANTED
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06de8cc3bcfe463d0318651c8e2d51b269504769
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963881"
---
# <a name="icm_getbufferswanted-message"></a><span data-ttu-id="0e50f-105">\_Messaggio GETBUFFERSWANTED ICM</span><span class="sxs-lookup"><span data-stu-id="0e50f-105">ICM\_GETBUFFERSWANTED message</span></span>

<span data-ttu-id="0e50f-106">Il messaggio **MCI \_ GETBUFFERSWANTED** esegue una query su un driver per il numero di buffer da allocare.</span><span class="sxs-lookup"><span data-stu-id="0e50f-106">The **ICM\_GETBUFFERSWANTED** message queries a driver for the number of buffers to allocate.</span></span> <span data-ttu-id="0e50f-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**ICGetBuffersWanted**](/windows/desktop/api/Vfw/nf-vfw-icgetbufferswanted) .</span><span class="sxs-lookup"><span data-stu-id="0e50f-107">You can send this message explicitly or by using the [**ICGetBuffersWanted**](/windows/desktop/api/Vfw/nf-vfw-icgetbufferswanted) macro.</span></span>


```C++
ICM_GETBUFFERSWANTED 
wParam = (DWORD_PTR) (LPVOID) lpdwBuffers; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="0e50f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="0e50f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e50f-109"><span id="lpdwBuffers"></span><span id="lpdwbuffers"></span><span id="LPDWBUFFERS"></span>*lpdwBuffers*</span><span class="sxs-lookup"><span data-stu-id="0e50f-109"><span id="lpdwBuffers"></span><span id="lpdwbuffers"></span><span id="LPDWBUFFERS"></span>*lpdwBuffers*</span></span>
</dt> <dd>

<span data-ttu-id="0e50f-110">Indirizzo per contenere il numero di campioni necessari al driver per eseguire in modo efficiente il rendering dei dati.</span><span class="sxs-lookup"><span data-stu-id="0e50f-110">Address to contain the number of samples the driver needs to efficiently render the data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e50f-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0e50f-111">Return Value</span></span>

<span data-ttu-id="0e50f-112">Restituisce ICERR \_ OK se ha esito positivo o ICERR non \_ supportato in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="0e50f-112">Returns ICERR\_OK if successful or ICERR\_UNSUPPORTED otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e50f-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="0e50f-113">Remarks</span></span>

<span data-ttu-id="0e50f-114">Questo messaggio viene usato dai driver che usano l'hardware per eseguire il rendering dei dati e vogliono garantire un ritardo di tempo minimo causato dall'attesa dell'arrivo dei buffer.</span><span class="sxs-lookup"><span data-stu-id="0e50f-114">This message is used by drivers that use hardware to render data and want to ensure a minimal time lag caused by waiting for buffers to arrive.</span></span> <span data-ttu-id="0e50f-115">Ad esempio, se un driver controlla una lavagna di decompressione video che può ospitare 10 frame di video, potrebbe restituire 10 per questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="0e50f-115">For example, if a driver controls a video decompression board that can hold 10 frames of video, it could return 10 for this message.</span></span> <span data-ttu-id="0e50f-116">In questo modo, le applicazioni devono provare a rimanere 10 frame prima del frame attualmente necessario.</span><span class="sxs-lookup"><span data-stu-id="0e50f-116">This instructs applications to try to stay 10 frames ahead of the frame it currently needs.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e50f-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0e50f-117">Requirements</span></span>



| <span data-ttu-id="0e50f-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e50f-118">Requirement</span></span> | <span data-ttu-id="0e50f-119">Valore</span><span class="sxs-lookup"><span data-stu-id="0e50f-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0e50f-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0e50f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0e50f-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0e50f-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="0e50f-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0e50f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0e50f-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0e50f-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="0e50f-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0e50f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e50f-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e50f-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e50f-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0e50f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e50f-127">Gestione compressione video</span><span class="sxs-lookup"><span data-stu-id="0e50f-127">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="0e50f-128">Messaggi di compressione video</span><span class="sxs-lookup"><span data-stu-id="0e50f-128">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





