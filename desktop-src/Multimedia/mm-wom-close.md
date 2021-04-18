---
title: Messaggio MM_WOM_CLOSE (mmsystem. h)
description: Il \_ messaggio mm WOM \_ Close viene inviato a una finestra quando viene chiuso un dispositivo di output della forma d'onda. L'handle del dispositivo non è più valido dopo l'invio di questo messaggio.
ms.assetid: 6505b688-88a1-43b2-ad4e-2f88e496430a
keywords:
- MM_WOM_CLOSE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MM_WOM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9dccdae49efc107a513e047282922f3a6de73e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302771"
---
# <a name="mm_wom_close-message"></a><span data-ttu-id="9ae70-105">MM \_ WOM \_ messaggio di chiusura</span><span class="sxs-lookup"><span data-stu-id="9ae70-105">MM\_WOM\_CLOSE message</span></span>

<span data-ttu-id="9ae70-106">Il messaggio **mm \_ WOM \_ Close** viene inviato a una finestra quando viene chiuso un dispositivo di output della forma d'onda.</span><span class="sxs-lookup"><span data-stu-id="9ae70-106">The **MM\_WOM\_CLOSE** message is sent to a window when a waveform-audio output device is closed.</span></span> <span data-ttu-id="9ae70-107">L'handle del dispositivo non è più valido dopo l'invio di questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="9ae70-107">The device handle is no longer valid after this message has been sent.</span></span>


```C++
MM_WOM_CLOSE 
wParam = (WPARAM) hOutputDev 
lParam = reserved 
```



## <a name="parameters"></a><span data-ttu-id="9ae70-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="9ae70-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ae70-109"><span id="hOutputDev"></span><span id="houtputdev"></span><span id="HOUTPUTDEV"></span>*hOutputDev*</span><span class="sxs-lookup"><span data-stu-id="9ae70-109"><span id="hOutputDev"></span><span id="houtputdev"></span><span id="HOUTPUTDEV"></span>*hOutputDev*</span></span>
</dt> <dd>

<span data-ttu-id="9ae70-110">Handle per il dispositivo che è stato chiuso.</span><span class="sxs-lookup"><span data-stu-id="9ae70-110">Handle to the device that was closed.</span></span>

</dd> <dt>

<span data-ttu-id="9ae70-111"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="9ae70-111"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="9ae70-112">Riservati deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="9ae70-112">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ae70-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9ae70-113">Return Value</span></span>

<span data-ttu-id="9ae70-114">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="9ae70-114">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ae70-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9ae70-115">Requirements</span></span>



| <span data-ttu-id="9ae70-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ae70-116">Requirement</span></span> | <span data-ttu-id="9ae70-117">Valore</span><span class="sxs-lookup"><span data-stu-id="9ae70-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ae70-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9ae70-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9ae70-119">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9ae70-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="9ae70-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9ae70-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9ae70-121">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9ae70-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="9ae70-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9ae70-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ae70-123"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9ae70-123"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ae70-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9ae70-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ae70-125">Audio Waveform</span><span class="sxs-lookup"><span data-stu-id="9ae70-125">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="9ae70-126">Messaggi di forma d'onda</span><span class="sxs-lookup"><span data-stu-id="9ae70-126">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

 





