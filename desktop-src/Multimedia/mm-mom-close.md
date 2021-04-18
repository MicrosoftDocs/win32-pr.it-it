---
title: Messaggio MM_MOM_CLOSE (mmsystem. h)
description: Il \_ \_ messaggio di chiusura MOM mm viene inviato a una finestra quando viene chiuso un dispositivo di output MIDI.
ms.assetid: 4829bbe5-5103-4354-88a7-37def22e926e
keywords:
- MM_MOM_CLOSE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MM_MOM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ae55cbca7c5effc146dee0c5ef9be67469a9201
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475502"
---
# <a name="mm_mom_close-message"></a><span data-ttu-id="d477c-104">\_Messaggio di \_ chiusura MOM mm</span><span class="sxs-lookup"><span data-stu-id="d477c-104">MM\_MOM\_CLOSE message</span></span>

<span data-ttu-id="d477c-105">Il messaggio di **\_ \_ chiusura MOM mm** viene inviato a una finestra quando viene chiuso un dispositivo di output MIDI.</span><span class="sxs-lookup"><span data-stu-id="d477c-105">The **MM\_MOM\_CLOSE** message is sent to a window when a MIDI output device is closed.</span></span>


```C++
MM_MOM_CLOSE 
wParam = (WPARAM) hOutput 
lParam = reserved 
```



## <a name="parameters"></a><span data-ttu-id="d477c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d477c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d477c-107"><span id="hOutput"></span><span id="houtput"></span><span id="HOUTPUT"></span>*hOutput*</span><span class="sxs-lookup"><span data-stu-id="d477c-107"><span id="hOutput"></span><span id="houtput"></span><span id="HOUTPUT"></span>*hOutput*</span></span>
</dt> <dd>

<span data-ttu-id="d477c-108">Handle per il dispositivo di output MIDI.</span><span class="sxs-lookup"><span data-stu-id="d477c-108">Handle to the MIDI output device.</span></span>

</dd> <dt>

<span data-ttu-id="d477c-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="d477c-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="d477c-110">Riservati Non usare.</span><span class="sxs-lookup"><span data-stu-id="d477c-110">Reserved; do not use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d477c-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d477c-111">Return Value</span></span>

<span data-ttu-id="d477c-112">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="d477c-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d477c-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="d477c-113">Remarks</span></span>

<span data-ttu-id="d477c-114">L'handle del dispositivo non è più valido dopo l'invio di questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="d477c-114">The device handle is no longer valid after this message has been sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="d477c-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d477c-115">Requirements</span></span>



| <span data-ttu-id="d477c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d477c-116">Requirement</span></span> | <span data-ttu-id="d477c-117">Valore</span><span class="sxs-lookup"><span data-stu-id="d477c-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d477c-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d477c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d477c-119">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d477c-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d477c-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d477c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d477c-121">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d477c-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d477c-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d477c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d477c-123"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d477c-123"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d477c-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d477c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d477c-125">Messaggi MIDI</span><span class="sxs-lookup"><span data-stu-id="d477c-125">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

 





