---
title: Messaggio MM_MIM_OPEN (mmsystem. h)
description: Il \_ \_ messaggio di apertura mm MIM viene inviato a una finestra quando viene aperto un dispositivo di input MIDI.
ms.assetid: 8dfc24a0-0ab8-4f49-954f-0c0a55fa28bc
keywords:
- MM_MIM_OPEN messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MM_MIM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7d87e391336b948d0c784048baeffa7bba88b29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873269"
---
# <a name="mm_mim_open-message"></a><span data-ttu-id="f35ed-104">MM \_ \_ messaggio aperto MIM</span><span class="sxs-lookup"><span data-stu-id="f35ed-104">MM\_MIM\_OPEN message</span></span>

<span data-ttu-id="f35ed-105">Il messaggio di **\_ \_ apertura mm MIM** viene inviato a una finestra quando viene aperto un dispositivo di input MIDI.</span><span class="sxs-lookup"><span data-stu-id="f35ed-105">The **MM\_MIM\_OPEN** message is sent to a window when a MIDI input device is opened.</span></span>


```C++
MM_MIM_OPEN 
wParam = (WPARAM) hInput 
lParam = reserved 
```



## <a name="parameters"></a><span data-ttu-id="f35ed-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f35ed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f35ed-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span><span class="sxs-lookup"><span data-stu-id="f35ed-107"><span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*</span></span>
</dt> <dd>

<span data-ttu-id="f35ed-108">Handle per il dispositivo di input MIDI che è stato aperto.</span><span class="sxs-lookup"><span data-stu-id="f35ed-108">Handle to the MIDI input device that was opened.</span></span>

</dd> <dt>

<span data-ttu-id="f35ed-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="f35ed-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="f35ed-110">Riservati Non usare.</span><span class="sxs-lookup"><span data-stu-id="f35ed-110">Reserved; do not use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f35ed-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f35ed-111">Return Value</span></span>

<span data-ttu-id="f35ed-112">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="f35ed-112">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f35ed-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f35ed-113">Requirements</span></span>



| <span data-ttu-id="f35ed-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f35ed-114">Requirement</span></span> | <span data-ttu-id="f35ed-115">Valore</span><span class="sxs-lookup"><span data-stu-id="f35ed-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f35ed-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f35ed-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f35ed-117">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f35ed-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f35ed-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f35ed-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f35ed-119">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f35ed-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f35ed-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f35ed-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f35ed-121"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f35ed-121"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f35ed-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f35ed-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f35ed-123">MIDI (Musical Instrument Digital Interface)</span><span class="sxs-lookup"><span data-stu-id="f35ed-123">Musical Instrument Digital Interface (MIDI)</span></span>](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[<span data-ttu-id="f35ed-124">Messaggi MIDI</span><span class="sxs-lookup"><span data-stu-id="f35ed-124">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

 





