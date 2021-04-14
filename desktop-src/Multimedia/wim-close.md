---
title: Messaggio WIM_CLOSE (mmsystem. h)
description: Il \_ messaggio di chiusura WIM viene inviato alla funzione di callback di input della forma d'onda-audio specificata quando viene chiuso un dispositivo di input audio e di forma d'onda. L'handle del dispositivo non è più valido dopo l'invio di questo messaggio.
ms.assetid: 3774b8b4-b03b-49e7-b9cd-cf3f194df847
keywords:
- WIM_CLOSE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WIM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6028ac6c45aa013138aab227e79d8d210ad70bb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478718"
---
# <a name="wim_close-message"></a><span data-ttu-id="e2461-105">\_Messaggio di chiusura Wim</span><span class="sxs-lookup"><span data-stu-id="e2461-105">WIM\_CLOSE message</span></span>

<span data-ttu-id="e2461-106">Il messaggio di **\_ chiusura Wim** viene inviato alla funzione di callback di input della forma d'onda-audio specificata quando viene chiuso un dispositivo di input audio e di forma d'onda.</span><span class="sxs-lookup"><span data-stu-id="e2461-106">The **WIM\_CLOSE** message is sent to the given waveform-audio input callback function when a waveform-audio input device is closed.</span></span> <span data-ttu-id="e2461-107">L'handle del dispositivo non è più valido dopo l'invio di questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="e2461-107">The device handle is no longer valid after this message has been sent.</span></span>


```C++
WIM_CLOSE 
dwParam1 = reserved 
dwParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="e2461-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e2461-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2461-109"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="e2461-109"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span></span>
</dt> <dd>

<span data-ttu-id="e2461-110">Riservati deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="e2461-110">Reserved; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="e2461-111"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="e2461-111"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="e2461-112">Riservati deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="e2461-112">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2461-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e2461-113">Return Value</span></span>

<span data-ttu-id="e2461-114">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="e2461-114">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2461-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e2461-115">Requirements</span></span>



| <span data-ttu-id="e2461-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2461-116">Requirement</span></span> | <span data-ttu-id="e2461-117">Valore</span><span class="sxs-lookup"><span data-stu-id="e2461-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2461-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e2461-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e2461-119">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e2461-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e2461-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e2461-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e2461-121">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e2461-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e2461-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e2461-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2461-123"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e2461-123"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2461-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e2461-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2461-125">Audio Waveform</span><span class="sxs-lookup"><span data-stu-id="e2461-125">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="e2461-126">Messaggi di forma d'onda</span><span class="sxs-lookup"><span data-stu-id="e2461-126">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

 





