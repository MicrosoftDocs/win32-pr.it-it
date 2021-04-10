---
title: Messaggio MM_MOM_DONE (mmsystem. h)
description: Il \_ messaggio mm MOM \_ Done viene inviato a una finestra quando il buffer di flusso o esclusivo del sistema MIDI specificato è stato riprodotto e viene restituito all'applicazione.
ms.assetid: 4651d5b4-3c98-4fa7-b761-dafb30e0d31e
keywords:
- MM_MOM_DONE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MM_MOM_DONE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46ad5d4a7e91cc05aa51017cba79418b34445362
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047968"
---
# <a name="mm_mom_done-message"></a><span data-ttu-id="b1c0e-104">MM \_ \_ messaggio MOM done</span><span class="sxs-lookup"><span data-stu-id="b1c0e-104">MM\_MOM\_DONE message</span></span>

<span data-ttu-id="b1c0e-105">Il messaggio **mm \_ MOM \_ done** viene inviato a una finestra quando il buffer di flusso o esclusivo del sistema MIDI specificato è stato riprodotto e viene restituito all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b1c0e-105">The **MM\_MOM\_DONE** message is sent to a window when the specified MIDI system-exclusive or stream buffer has been played and is being returned to the application.</span></span>


```C++
MM_MOM_DONE 
wParam = (WPARAM) hOutput 
lParam = (LPARAM) lpMidiHdr 
```



## <a name="parameters"></a><span data-ttu-id="b1c0e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b1c0e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1c0e-107"><span id="hOutput"></span><span id="houtput"></span><span id="HOUTPUT"></span>*hOutput*</span><span class="sxs-lookup"><span data-stu-id="b1c0e-107"><span id="hOutput"></span><span id="houtput"></span><span id="HOUTPUT"></span>*hOutput*</span></span>
</dt> <dd>

<span data-ttu-id="b1c0e-108">Handle per il dispositivo di output MIDI che ha eseguito il buffer.</span><span class="sxs-lookup"><span data-stu-id="b1c0e-108">Handle to the MIDI output device that played the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="b1c0e-109"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span><span class="sxs-lookup"><span data-stu-id="b1c0e-109"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span></span>
</dt> <dd>

<span data-ttu-id="b1c0e-110">Puntatore a una struttura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) che identifica il buffer.</span><span class="sxs-lookup"><span data-stu-id="b1c0e-110">Pointer to a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure identifying the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1c0e-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b1c0e-111">Return Value</span></span>

<span data-ttu-id="b1c0e-112">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="b1c0e-112">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1c0e-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b1c0e-113">Requirements</span></span>



| <span data-ttu-id="b1c0e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1c0e-114">Requirement</span></span> | <span data-ttu-id="b1c0e-115">Valore</span><span class="sxs-lookup"><span data-stu-id="b1c0e-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1c0e-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b1c0e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b1c0e-117">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b1c0e-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b1c0e-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b1c0e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b1c0e-119">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b1c0e-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b1c0e-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b1c0e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1c0e-121"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b1c0e-121"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1c0e-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b1c0e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1c0e-123">Messaggi MIDI</span><span class="sxs-lookup"><span data-stu-id="b1c0e-123">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

