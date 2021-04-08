---
title: Messaggio MM_WIM_CLOSE (mmsystem. h)
description: Il \_ \_ messaggio di chiusura Wim mm viene inviato a una finestra quando viene chiuso un dispositivo di input audio e di forma d'onda. L'handle del dispositivo non è più valido dopo l'invio di questo messaggio.
ms.assetid: 4ea35b66-6bfa-41f0-9d52-a8cf2b0a69dd
keywords:
- MM_WIM_CLOSE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MM_WIM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90d9934ef7045debbcac2f5baf1c2f750d22dad5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047828"
---
# <a name="mm_wim_close-message"></a><span data-ttu-id="087bf-105">\_Messaggio di \_ chiusura Wim mm</span><span class="sxs-lookup"><span data-stu-id="087bf-105">MM\_WIM\_CLOSE message</span></span>

<span data-ttu-id="087bf-106">Il messaggio di **\_ \_ chiusura Wim mm** viene inviato a una finestra quando viene chiuso un dispositivo di input audio e di forma d'onda.</span><span class="sxs-lookup"><span data-stu-id="087bf-106">The **MM\_WIM\_CLOSE** message is sent to a window when a waveform-audio input device is closed.</span></span> <span data-ttu-id="087bf-107">L'handle del dispositivo non è più valido dopo l'invio di questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="087bf-107">The device handle is no longer valid after this message has been sent.</span></span>


```C++
MM_WIM_CLOSE 
wParam = (WPARAM) hInputDev 
lParam = reserved 
```



## <a name="parameters"></a><span data-ttu-id="087bf-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="087bf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="087bf-109"><span id="hInputDev"></span><span id="hinputdev"></span><span id="HINPUTDEV"></span>*hInputDev*</span><span class="sxs-lookup"><span data-stu-id="087bf-109"><span id="hInputDev"></span><span id="hinputdev"></span><span id="HINPUTDEV"></span>*hInputDev*</span></span>
</dt> <dd>

<span data-ttu-id="087bf-110">Handle per il dispositivo di input della forma d'onda-audio che è stato chiuso.</span><span class="sxs-lookup"><span data-stu-id="087bf-110">Handle to the waveform-audio input device that was closed.</span></span>

</dd> <dt>

<span data-ttu-id="087bf-111"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="087bf-111"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="087bf-112">Riservati deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="087bf-112">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="087bf-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="087bf-113">Return Value</span></span>

<span data-ttu-id="087bf-114">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="087bf-114">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="087bf-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="087bf-115">Requirements</span></span>



| <span data-ttu-id="087bf-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="087bf-116">Requirement</span></span> | <span data-ttu-id="087bf-117">Valore</span><span class="sxs-lookup"><span data-stu-id="087bf-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="087bf-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="087bf-118">Minimum supported client</span></span><br/> | <span data-ttu-id="087bf-119">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="087bf-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="087bf-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="087bf-120">Minimum supported server</span></span><br/> | <span data-ttu-id="087bf-121">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="087bf-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="087bf-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="087bf-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="087bf-123"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="087bf-123"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="087bf-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="087bf-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="087bf-125">Audio Waveform</span><span class="sxs-lookup"><span data-stu-id="087bf-125">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="087bf-126">Messaggi di forma d'onda</span><span class="sxs-lookup"><span data-stu-id="087bf-126">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

 





