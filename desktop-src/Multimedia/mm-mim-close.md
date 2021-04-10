---
title: Messaggio MM_MIM_CLOSE (mmsystem. h)
description: Il \_ \_ messaggio di chiusura MIM mm viene inviato a una finestra quando un dispositivo di input MIDI viene chiuso.
ms.assetid: 261021aa-4df6-44d8-aad3-5f98b1213459
keywords:
- MM_MIM_CLOSE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MM_MIM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8ce511365b1faa49faefaf4ed25c5b8befb2288
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964524"
---
# <a name="mm_mim_close-message"></a><span data-ttu-id="86c0c-104">MM \_ \_ messaggio di chiusura MIM</span><span class="sxs-lookup"><span data-stu-id="86c0c-104">MM\_MIM\_CLOSE message</span></span>

<span data-ttu-id="86c0c-105">Il messaggio di **\_ \_ chiusura MIM mm** viene inviato a una finestra quando un dispositivo di input MIDI viene chiuso.</span><span class="sxs-lookup"><span data-stu-id="86c0c-105">The **MM\_MIM\_CLOSE** message is sent to a window when a MIDI input device is closed.</span></span>


```C++
MM_MIM_CLOSE 
wParam = (WPARAM) hInput 
lParam = reserved 
```



## <a name="parameters"></a><span data-ttu-id="86c0c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="86c0c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86c0c-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span><span class="sxs-lookup"><span data-stu-id="86c0c-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span></span>
</dt> <dd>

<span data-ttu-id="86c0c-108">Handle per il dispositivo di input MIDI che è stato chiuso.</span><span class="sxs-lookup"><span data-stu-id="86c0c-108">Handle to the MIDI input device that was closed.</span></span>

</dd> <dt>

<span data-ttu-id="86c0c-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="86c0c-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="86c0c-110">Riservati Non usare.</span><span class="sxs-lookup"><span data-stu-id="86c0c-110">Reserved; do not use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86c0c-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="86c0c-111">Return Value</span></span>

<span data-ttu-id="86c0c-112">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="86c0c-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="86c0c-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="86c0c-113">Remarks</span></span>

<span data-ttu-id="86c0c-114">L'handle del dispositivo non è più valido dopo l'invio di questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="86c0c-114">The device handle is no longer valid after this message has been sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="86c0c-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="86c0c-115">Requirements</span></span>



| <span data-ttu-id="86c0c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="86c0c-116">Requirement</span></span> | <span data-ttu-id="86c0c-117">Valore</span><span class="sxs-lookup"><span data-stu-id="86c0c-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86c0c-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="86c0c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="86c0c-119">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="86c0c-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="86c0c-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="86c0c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="86c0c-121">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="86c0c-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="86c0c-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="86c0c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="86c0c-123"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="86c0c-123"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86c0c-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="86c0c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86c0c-125">MIDI (Musical Instrument Digital Interface)</span><span class="sxs-lookup"><span data-stu-id="86c0c-125">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="86c0c-126">Messaggi MIDI</span><span class="sxs-lookup"><span data-stu-id="86c0c-126">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

 





