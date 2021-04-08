---
title: Messaggio MOM_OPEN (mmsystem. h)
description: Il \_ messaggio MOM aperto viene inviato a una funzione di callback di output MIDI quando viene aperto un dispositivo di output MIDI.
ms.assetid: f3360482-7d16-419c-b5d1-0dd3a6e3c690
keywords:
- MOM_OPEN messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MOM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24072aad6bff9ce192460c2c8525da4506f32746
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743362"
---
# <a name="mom_open-message"></a><span data-ttu-id="6b2e8-104">\_Messaggio di apertura MOM</span><span class="sxs-lookup"><span data-stu-id="6b2e8-104">MOM\_OPEN message</span></span>

<span data-ttu-id="6b2e8-105">Il messaggio **MOM \_ aperto** viene inviato a una funzione di callback di output MIDI quando viene aperto un dispositivo di output MIDI.</span><span class="sxs-lookup"><span data-stu-id="6b2e8-105">The **MOM\_OPEN** message is sent to a MIDI output callback function when a MIDI output device is opened.</span></span>


```C++
MOM_OPEN 
dwParam1 = reserved 
dwParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="6b2e8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6b2e8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b2e8-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="6b2e8-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span></span>
</dt> <dd>

<span data-ttu-id="6b2e8-108">Riservati Non usare.</span><span class="sxs-lookup"><span data-stu-id="6b2e8-108">Reserved; do not use.</span></span>

</dd> <dt>

<span data-ttu-id="6b2e8-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="6b2e8-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="6b2e8-110">Riservati Non usare.</span><span class="sxs-lookup"><span data-stu-id="6b2e8-110">Reserved; do not use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b2e8-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6b2e8-111">Return Value</span></span>

<span data-ttu-id="6b2e8-112">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="6b2e8-112">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b2e8-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6b2e8-113">Requirements</span></span>



| <span data-ttu-id="6b2e8-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b2e8-114">Requirement</span></span> | <span data-ttu-id="6b2e8-115">Valore</span><span class="sxs-lookup"><span data-stu-id="6b2e8-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b2e8-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6b2e8-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6b2e8-117">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6b2e8-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="6b2e8-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6b2e8-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6b2e8-119">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6b2e8-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="6b2e8-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6b2e8-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b2e8-121"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6b2e8-121"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b2e8-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6b2e8-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b2e8-123">Messaggi MIDI</span><span class="sxs-lookup"><span data-stu-id="6b2e8-123">MIDI Messages</span></span>](midi-messages.md)
</dt> </dl>

 

 





