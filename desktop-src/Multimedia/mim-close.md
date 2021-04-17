---
title: Messaggio MIM_CLOSE (mmsystem. h)
description: Il \_ messaggio di chiusura MIM viene inviato a una funzione di callback input MIDI quando viene chiuso un dispositivo di input MIDI.
ms.assetid: c19ecd3a-c3a5-4f17-9d44-d0d71eefcb15
keywords:
- MIM_CLOSE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MIM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5549d9bef1e802b0b34ab6437b1386519a25d349
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517409"
---
# <a name="mim_close-message"></a><span data-ttu-id="de6ff-104">\_Messaggio di chiusura MIM</span><span class="sxs-lookup"><span data-stu-id="de6ff-104">MIM\_CLOSE message</span></span>

<span data-ttu-id="de6ff-105">Il messaggio di **\_ chiusura MIM** viene inviato a una funzione di callback input MIDI quando viene chiuso un dispositivo di input MIDI.</span><span class="sxs-lookup"><span data-stu-id="de6ff-105">The **MIM\_CLOSE** message is sent to a MIDI input callback function when a MIDI input device is closed.</span></span>


```C++
MIM_CLOSE 
dwParam1 = reserved 
dwParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="de6ff-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="de6ff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de6ff-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="de6ff-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span></span>
</dt> <dd>

<span data-ttu-id="de6ff-108">Riservati Non usare.</span><span class="sxs-lookup"><span data-stu-id="de6ff-108">Reserved; do not use.</span></span>

</dd> <dt>

<span data-ttu-id="de6ff-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="de6ff-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="de6ff-110">Riservati Non usare.</span><span class="sxs-lookup"><span data-stu-id="de6ff-110">Reserved; do not use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de6ff-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="de6ff-111">Return Value</span></span>

<span data-ttu-id="de6ff-112">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="de6ff-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="de6ff-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="de6ff-113">Remarks</span></span>

<span data-ttu-id="de6ff-114">L'handle del dispositivo non è più valido dopo l'invio di questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="de6ff-114">The device handle is no longer valid after this message has been sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="de6ff-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="de6ff-115">Requirements</span></span>



| <span data-ttu-id="de6ff-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="de6ff-116">Requirement</span></span> | <span data-ttu-id="de6ff-117">Valore</span><span class="sxs-lookup"><span data-stu-id="de6ff-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de6ff-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="de6ff-118">Minimum supported client</span></span><br/> | <span data-ttu-id="de6ff-119">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="de6ff-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="de6ff-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="de6ff-120">Minimum supported server</span></span><br/> | <span data-ttu-id="de6ff-121">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="de6ff-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="de6ff-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="de6ff-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="de6ff-123"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="de6ff-123"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de6ff-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="de6ff-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de6ff-125">MIDI (Musical Instrument Digital Interface)</span><span class="sxs-lookup"><span data-stu-id="de6ff-125">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="de6ff-126">Messaggi MIDI</span><span class="sxs-lookup"><span data-stu-id="de6ff-126">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

 





