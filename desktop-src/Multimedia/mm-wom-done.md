---
title: Messaggio MM_WOM_DONE (mmsystem. h)
description: Il \_ messaggio mm WOM \_ Done viene inviato a una finestra quando il buffer di output specificato viene restituito all'applicazione. I buffer vengono restituiti all'applicazione quando vengono riprodotti o come risultato di una chiamata alla funzione waveOutReset.
ms.assetid: bbdebb68-82e5-4963-90bb-f93f8a91a8cf
keywords:
- MM_WOM_DONE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MM_WOM_DONE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7198aa2f60a7f5a0e6d839a3ee5b453a3a4d3f59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743914"
---
# <a name="mm_wom_done-message"></a><span data-ttu-id="724c1-105">MM \_ WOM \_ fatto messaggio</span><span class="sxs-lookup"><span data-stu-id="724c1-105">MM\_WOM\_DONE message</span></span>

<span data-ttu-id="724c1-106">Il messaggio **mm \_ WOM \_ done** viene inviato a una finestra quando il buffer di output specificato viene restituito all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="724c1-106">The **MM\_WOM\_DONE** message is sent to a window when the given output buffer is being returned to the application.</span></span> <span data-ttu-id="724c1-107">I buffer vengono restituiti all'applicazione quando vengono riprodotti o come risultato di una chiamata alla funzione [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset) .</span><span class="sxs-lookup"><span data-stu-id="724c1-107">Buffers are returned to the application when they have been played, or as the result of a call to the [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset) function.</span></span>


```C++
MM_WOM_DONE 
wParam = (WPARAM) hOutputDev 
lParam = (LONG) lpwvhdr 
```



## <a name="parameters"></a><span data-ttu-id="724c1-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="724c1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="724c1-109"><span id="hOutputDev"></span><span id="houtputdev"></span><span id="HOUTPUTDEV"></span>*hOutputDev*</span><span class="sxs-lookup"><span data-stu-id="724c1-109"><span id="hOutputDev"></span><span id="houtputdev"></span><span id="HOUTPUTDEV"></span>*hOutputDev*</span></span>
</dt> <dd>

<span data-ttu-id="724c1-110">Handle per il dispositivo di output waveform-audio che ha riprodotto il buffer.</span><span class="sxs-lookup"><span data-stu-id="724c1-110">Handle to the waveform-audio output device that played the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="724c1-111"><span id="lpwvhdr"></span><span id="LPWVHDR"></span>*lpwvhdr*</span><span class="sxs-lookup"><span data-stu-id="724c1-111"><span id="lpwvhdr"></span><span id="LPWVHDR"></span>*lpwvhdr*</span></span>
</dt> <dd>

<span data-ttu-id="724c1-112">Puntatore a una struttura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) che identifica il buffer.</span><span class="sxs-lookup"><span data-stu-id="724c1-112">Pointer to a [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure identifying the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="724c1-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="724c1-113">Return Value</span></span>

<span data-ttu-id="724c1-114">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="724c1-114">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="724c1-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="724c1-115">Requirements</span></span>



| <span data-ttu-id="724c1-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="724c1-116">Requirement</span></span> | <span data-ttu-id="724c1-117">Valore</span><span class="sxs-lookup"><span data-stu-id="724c1-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="724c1-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="724c1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="724c1-119">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="724c1-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="724c1-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="724c1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="724c1-121">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="724c1-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="724c1-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="724c1-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="724c1-123"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="724c1-123"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="724c1-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="724c1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="724c1-125">Audio Waveform</span><span class="sxs-lookup"><span data-stu-id="724c1-125">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="724c1-126">Messaggi di forma d'onda</span><span class="sxs-lookup"><span data-stu-id="724c1-126">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

