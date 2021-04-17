---
title: Messaggio MM_MOM_OPEN (mmsystem. h)
description: Il \_ \_ messaggio di apertura MOM di MOM viene inviato a una finestra quando viene aperto un dispositivo di output MIDI.
ms.assetid: 1374a07c-02fa-4b43-82df-cbd96302aec5
keywords:
- MM_MOM_OPEN messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MM_MOM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2f676dccf532290ab2153b888c20fad7b19d98d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475077"
---
# <a name="mm_mom_open-message"></a><span data-ttu-id="02e2d-104">MM \_ \_ messaggio di apertura MOM</span><span class="sxs-lookup"><span data-stu-id="02e2d-104">MM\_MOM\_OPEN message</span></span>

<span data-ttu-id="02e2d-105">Il messaggio di **\_ \_ apertura MOM di MOM** viene inviato a una finestra quando viene aperto un dispositivo di output MIDI.</span><span class="sxs-lookup"><span data-stu-id="02e2d-105">The **MM\_MOM\_OPEN** message is sent to a window when a MIDI output device is opened.</span></span>


```C++
MM_MOM_OPEN 
wParam = (WPARAM) hOutput 
lParam = reserved 
```



## <a name="parameters"></a><span data-ttu-id="02e2d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="02e2d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02e2d-107"><span id="hOutput"></span><span id="houtput"></span><span id="HOUTPUT"></span>*hOutput*</span><span class="sxs-lookup"><span data-stu-id="02e2d-107"><span id="hOutput"></span><span id="houtput"></span><span id="HOUTPUT"></span>*hOutput*</span></span>
</dt> <dd>

<span data-ttu-id="02e2d-108">Handle per il dispositivo di output MIDI.</span><span class="sxs-lookup"><span data-stu-id="02e2d-108">Handle to the MIDI output device.</span></span>

</dd> <dt>

<span data-ttu-id="02e2d-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="02e2d-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="02e2d-110">Riservati Non usare.</span><span class="sxs-lookup"><span data-stu-id="02e2d-110">Reserved; do not use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02e2d-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="02e2d-111">Return Value</span></span>

<span data-ttu-id="02e2d-112">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="02e2d-112">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="02e2d-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="02e2d-113">Requirements</span></span>



| <span data-ttu-id="02e2d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="02e2d-114">Requirement</span></span> | <span data-ttu-id="02e2d-115">Valore</span><span class="sxs-lookup"><span data-stu-id="02e2d-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02e2d-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="02e2d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="02e2d-117">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="02e2d-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="02e2d-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="02e2d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="02e2d-119">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="02e2d-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="02e2d-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="02e2d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="02e2d-121"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="02e2d-121"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02e2d-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="02e2d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02e2d-123">Messaggi MIDI</span><span class="sxs-lookup"><span data-stu-id="02e2d-123">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

 





