---
title: Messaggio MIM_OPEN (mmsystem. h)
description: Il \_ messaggio aperto MIM viene inviato a una funzione di callback input MIDI quando viene aperto un dispositivo di input MIDI.
ms.assetid: c7a8b856-aedd-457d-8a21-0ec2e9303960
keywords:
- MIM_OPEN messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MIM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49fcfd05ef7702fbc7bf3108365e49660071ae9a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400284"
---
# <a name="mim_open-message"></a><span data-ttu-id="744cb-104">\_Messaggio aperto MIM</span><span class="sxs-lookup"><span data-stu-id="744cb-104">MIM\_OPEN message</span></span>

<span data-ttu-id="744cb-105">Il **messaggio \_ aperto MIM** viene inviato a una funzione di callback input MIDI quando viene aperto un dispositivo di input MIDI.</span><span class="sxs-lookup"><span data-stu-id="744cb-105">The **MIM\_OPEN** message is sent to a MIDI input callback function when a MIDI input device is opened.</span></span>


```C++
MIM_OPEN 
dwParam1 = reserved 
dwParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="744cb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="744cb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="744cb-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="744cb-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span></span>
</dt> <dd>

<span data-ttu-id="744cb-108">Riservati Non usare.</span><span class="sxs-lookup"><span data-stu-id="744cb-108">Reserved; do not use.</span></span>

</dd> <dt>

<span data-ttu-id="744cb-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="744cb-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="744cb-110">Riservati Non usare.</span><span class="sxs-lookup"><span data-stu-id="744cb-110">Reserved; do not use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="744cb-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="744cb-111">Return Value</span></span>

<span data-ttu-id="744cb-112">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="744cb-112">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="744cb-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="744cb-113">Requirements</span></span>



| <span data-ttu-id="744cb-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="744cb-114">Requirement</span></span> | <span data-ttu-id="744cb-115">Valore</span><span class="sxs-lookup"><span data-stu-id="744cb-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="744cb-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="744cb-116">Minimum supported client</span></span><br/> | <span data-ttu-id="744cb-117">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="744cb-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="744cb-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="744cb-118">Minimum supported server</span></span><br/> | <span data-ttu-id="744cb-119">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="744cb-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="744cb-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="744cb-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="744cb-121"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="744cb-121"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="744cb-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="744cb-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="744cb-123">MIDI (Musical Instrument Digital Interface)</span><span class="sxs-lookup"><span data-stu-id="744cb-123">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="744cb-124">Messaggi MIDI</span><span class="sxs-lookup"><span data-stu-id="744cb-124">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

 





