---
title: Messaggio MM_WIM_OPEN (mmsystem. h)
description: Il \_ \_ messaggio di apertura Wim di mm viene inviato a una finestra quando viene aperto un dispositivo di input della forma d'onda.
ms.assetid: 4c646f58-c324-467e-871b-8fc36d5b89bc
keywords:
- MM_WIM_OPEN messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MM_WIM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64ff028dcd9dc851d94699ef5cb75707429ba149
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048763"
---
# <a name="mm_wim_open-message"></a><span data-ttu-id="6ea9a-104">\_Messaggio di \_ apertura Wim mm</span><span class="sxs-lookup"><span data-stu-id="6ea9a-104">MM\_WIM\_OPEN message</span></span>

<span data-ttu-id="6ea9a-105">Il messaggio di **\_ \_ apertura Wim di mm** viene inviato a una finestra quando viene aperto un dispositivo di input della forma d'onda.</span><span class="sxs-lookup"><span data-stu-id="6ea9a-105">The **MM\_WIM\_OPEN** message is sent to a window when a waveform-audio input device is opened.</span></span>


```C++
MM_WIM_OPEN 
wParam = (WPARAM) hInputDev 
lParam = reserved 
```



## <a name="parameters"></a><span data-ttu-id="6ea9a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6ea9a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ea9a-107"><span id="hInputDev"></span><span id="hinputdev"></span><span id="HINPUTDEV"></span>*hInputDev*</span><span class="sxs-lookup"><span data-stu-id="6ea9a-107"><span id="hInputDev"></span><span id="hinputdev"></span><span id="HINPUTDEV"></span>*hInputDev*</span></span>
</dt> <dd>

<span data-ttu-id="6ea9a-108">Handle per il dispositivo che è stato aperto.</span><span class="sxs-lookup"><span data-stu-id="6ea9a-108">Handle to the device that was opened.</span></span>

</dd> <dt>

<span data-ttu-id="6ea9a-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="6ea9a-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="6ea9a-110">Riservati deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="6ea9a-110">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ea9a-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6ea9a-111">Return Value</span></span>

<span data-ttu-id="6ea9a-112">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="6ea9a-112">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ea9a-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6ea9a-113">Requirements</span></span>



| <span data-ttu-id="6ea9a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ea9a-114">Requirement</span></span> | <span data-ttu-id="6ea9a-115">Valore</span><span class="sxs-lookup"><span data-stu-id="6ea9a-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ea9a-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6ea9a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6ea9a-117">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6ea9a-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="6ea9a-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6ea9a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6ea9a-119">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6ea9a-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="6ea9a-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6ea9a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ea9a-121"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6ea9a-121"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ea9a-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6ea9a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ea9a-123">Audio Waveform</span><span class="sxs-lookup"><span data-stu-id="6ea9a-123">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="6ea9a-124">Messaggi di forma d'onda</span><span class="sxs-lookup"><span data-stu-id="6ea9a-124">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

 





