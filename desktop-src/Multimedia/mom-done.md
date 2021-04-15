---
title: Messaggio MOM_DONE (Mciapi. h)
description: Il \_ messaggio MOM done viene inviato a una funzione di callback di output MIDI quando il buffer di flusso o esclusivo del sistema specificato è stato riprodotto e viene restituito all'applicazione.
ms.assetid: 0b9bd0e1-c87d-4f21-912e-5ac9f5c04192
keywords:
- MOM_DONE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MOM_DONE
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8af3f58f7d8f4625971dde5d7ec807c9f963d40f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400492"
---
# <a name="mom_done-message"></a><span data-ttu-id="b5cbd-104">\_Messaggio MOM done</span><span class="sxs-lookup"><span data-stu-id="b5cbd-104">MOM\_DONE message</span></span>

<span data-ttu-id="b5cbd-105">Il messaggio **MOM \_ done** viene inviato a una funzione di callback di output MIDI quando il buffer di flusso o esclusivo del sistema specificato è stato riprodotto e viene restituito all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b5cbd-105">The **MOM\_DONE** message is sent to a MIDI output callback function when the specified system-exclusive or stream buffer has been played and is being returned to the application.</span></span>


```C++
MOM_DONE 
dwParam1 = (DWORD) lpMidiHdr 
dwParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="b5cbd-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b5cbd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5cbd-107"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span><span class="sxs-lookup"><span data-stu-id="b5cbd-107"><span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*</span></span>
</dt> <dd>

<span data-ttu-id="b5cbd-108">Puntatore a una struttura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) che identifica il buffer.</span><span class="sxs-lookup"><span data-stu-id="b5cbd-108">Pointer to a [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) structure identifying the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="b5cbd-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="b5cbd-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="b5cbd-110">Riservati Non usare.</span><span class="sxs-lookup"><span data-stu-id="b5cbd-110">Reserved; do not use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5cbd-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b5cbd-111">Return Value</span></span>

<span data-ttu-id="b5cbd-112">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="b5cbd-112">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5cbd-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b5cbd-113">Requirements</span></span>



| <span data-ttu-id="b5cbd-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5cbd-114">Requirement</span></span> | <span data-ttu-id="b5cbd-115">Valore</span><span class="sxs-lookup"><span data-stu-id="b5cbd-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b5cbd-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b5cbd-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b5cbd-117">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b5cbd-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="b5cbd-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b5cbd-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b5cbd-119">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b5cbd-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b5cbd-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b5cbd-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5cbd-121"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5cbd-121"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5cbd-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b5cbd-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5cbd-123">Messaggi MIDI</span><span class="sxs-lookup"><span data-stu-id="b5cbd-123">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

