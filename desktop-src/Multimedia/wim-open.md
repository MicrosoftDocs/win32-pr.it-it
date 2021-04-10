---
title: Messaggio WIM_OPEN (mmsystem. h)
description: Il \_ messaggio di apertura WIM viene inviato a una funzione di callback di input della forma d'onda-audio quando viene aperto un dispositivo di input audio e di forma d'onda.
ms.assetid: de18e6b2-ea28-46d9-812c-e6dac49838ee
keywords:
- WIM_OPEN messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WIM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57c1661482149c90cf3f2bd6b10620cb32f380be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964777"
---
# <a name="wim_open-message"></a><span data-ttu-id="aab7d-104">\_Messaggio aperto Wim</span><span class="sxs-lookup"><span data-stu-id="aab7d-104">WIM\_OPEN message</span></span>

<span data-ttu-id="aab7d-105">Il messaggio di **\_ apertura Wim** viene inviato a una funzione di callback di input della forma d'onda-audio quando viene aperto un dispositivo di input audio e di forma d'onda.</span><span class="sxs-lookup"><span data-stu-id="aab7d-105">The **WIM\_OPEN** message is sent to a waveform-audio input callback function when a waveform-audio input device is opened.</span></span>


```C++
WIM_OPEN 
dwParam1 = reserved 
dwParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="aab7d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="aab7d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aab7d-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="aab7d-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span></span>
</dt> <dd>

<span data-ttu-id="aab7d-108">Riservati deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="aab7d-108">Reserved; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="aab7d-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="aab7d-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="aab7d-110">Riservati deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="aab7d-110">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aab7d-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="aab7d-111">Return Value</span></span>

<span data-ttu-id="aab7d-112">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="aab7d-112">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="aab7d-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aab7d-113">Requirements</span></span>



| <span data-ttu-id="aab7d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="aab7d-114">Requirement</span></span> | <span data-ttu-id="aab7d-115">Valore</span><span class="sxs-lookup"><span data-stu-id="aab7d-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aab7d-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aab7d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="aab7d-117">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="aab7d-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="aab7d-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aab7d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="aab7d-119">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="aab7d-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="aab7d-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="aab7d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="aab7d-121"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="aab7d-121"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aab7d-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aab7d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aab7d-123">Audio Waveform</span><span class="sxs-lookup"><span data-stu-id="aab7d-123">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="aab7d-124">Messaggi di forma d'onda</span><span class="sxs-lookup"><span data-stu-id="aab7d-124">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

 





