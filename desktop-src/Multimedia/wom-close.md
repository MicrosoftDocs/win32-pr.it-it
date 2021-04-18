---
title: Messaggio WOM_CLOSE (mmsystem. h)
description: Il \_ messaggio di chiusura WOM viene inviato a una funzione di callback di output waveform-audio quando viene chiuso un dispositivo di output della forma d'onda. L'handle del dispositivo non è più valido dopo l'invio di questo messaggio.
ms.assetid: ac20216a-6a60-4e62-8241-3ca6f33567f1
keywords:
- WOM_CLOSE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WOM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a802d6eceed018fa0c25591ee9e4b38708e1787e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301370"
---
# <a name="wom_close-message"></a><span data-ttu-id="c8027-105">\_Messaggio di chiusura WOM</span><span class="sxs-lookup"><span data-stu-id="c8027-105">WOM\_CLOSE message</span></span>

<span data-ttu-id="c8027-106">Il messaggio di **\_ chiusura WOM** viene inviato a una funzione di callback di output waveform-audio quando viene chiuso un dispositivo di output della forma d'onda.</span><span class="sxs-lookup"><span data-stu-id="c8027-106">The **WOM\_CLOSE** message is sent to a waveform-audio output callback function when a waveform-audio output device is closed.</span></span> <span data-ttu-id="c8027-107">L'handle del dispositivo non è più valido dopo l'invio di questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="c8027-107">The device handle is no longer valid after this message has been sent.</span></span>


```C++
WOM_CLOSE 
dwParam1 = reserved 
dwParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="c8027-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="c8027-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8027-109"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="c8027-109"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span></span>
</dt> <dd>

<span data-ttu-id="c8027-110">Riservati deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="c8027-110">Reserved; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="c8027-111"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="c8027-111"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="c8027-112">Riservati deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="c8027-112">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8027-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c8027-113">Return Value</span></span>

<span data-ttu-id="c8027-114">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="c8027-114">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8027-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c8027-115">Requirements</span></span>



| <span data-ttu-id="c8027-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8027-116">Requirement</span></span> | <span data-ttu-id="c8027-117">Valore</span><span class="sxs-lookup"><span data-stu-id="c8027-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8027-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c8027-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c8027-119">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c8027-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c8027-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c8027-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c8027-121">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c8027-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c8027-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c8027-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8027-123"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c8027-123"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8027-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c8027-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8027-125">Audio Waveform</span><span class="sxs-lookup"><span data-stu-id="c8027-125">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="c8027-126">Messaggi di forma d'onda</span><span class="sxs-lookup"><span data-stu-id="c8027-126">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

 





