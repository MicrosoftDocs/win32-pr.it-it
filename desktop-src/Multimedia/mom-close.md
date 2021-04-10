---
title: Messaggio MOM_CLOSE (mmsystem. h)
description: Il \_ messaggio MOM Close viene inviato a una funzione di callback di output MIDI quando viene chiuso un dispositivo di output MIDI.
ms.assetid: 229b3701-16f1-4ec8-920e-cd8231561541
keywords:
- MOM_CLOSE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MOM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68f173daa2fb104305979a72c9a14106175d7d20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964838"
---
# <a name="mom_close-message"></a><span data-ttu-id="92944-104">\_Messaggio di chiusura MOM</span><span class="sxs-lookup"><span data-stu-id="92944-104">MOM\_CLOSE message</span></span>

<span data-ttu-id="92944-105">Il messaggio **MOM \_ Close** viene inviato a una funzione di callback di output MIDI quando viene chiuso un dispositivo di output MIDI.</span><span class="sxs-lookup"><span data-stu-id="92944-105">The **MOM\_CLOSE** message is sent to a MIDI output callback function when a MIDI output device is closed.</span></span>


```C++
MOM_CLOSE 
dwParam1 = reserved 
dwParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="92944-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="92944-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92944-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="92944-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span></span>
</dt> <dd>

<span data-ttu-id="92944-108">Riservati Non usare.</span><span class="sxs-lookup"><span data-stu-id="92944-108">Reserved; do not use.</span></span>

</dd> <dt>

<span data-ttu-id="92944-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="92944-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="92944-110">Riservati Non usare.</span><span class="sxs-lookup"><span data-stu-id="92944-110">Reserved; do not use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92944-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="92944-111">Return Value</span></span>

<span data-ttu-id="92944-112">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="92944-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="92944-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="92944-113">Remarks</span></span>

<span data-ttu-id="92944-114">L'handle del dispositivo non è più valido dopo l'invio di questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="92944-114">The device handle is no longer valid after this message has been sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="92944-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="92944-115">Requirements</span></span>



| <span data-ttu-id="92944-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="92944-116">Requirement</span></span> | <span data-ttu-id="92944-117">Valore</span><span class="sxs-lookup"><span data-stu-id="92944-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92944-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="92944-118">Minimum supported client</span></span><br/> | <span data-ttu-id="92944-119">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="92944-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="92944-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="92944-120">Minimum supported server</span></span><br/> | <span data-ttu-id="92944-121">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="92944-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="92944-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="92944-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="92944-123"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="92944-123"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92944-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="92944-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92944-125">Messaggi MIDI</span><span class="sxs-lookup"><span data-stu-id="92944-125">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

 





