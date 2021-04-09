---
title: Messaggio WOM_OPEN (mmsystem. h)
description: Il \_ messaggio aperto WOM viene inviato a una funzione di callback di output waveform-audio quando viene aperto un dispositivo di output della forma d'onda.
ms.assetid: 7fa175d3-7c07-4ca0-a0bd-4526fbc24f8d
keywords:
- WOM_OPEN messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WOM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3cfca721019b28a5bf039e8c56c75892d85bd5e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104118942"
---
# <a name="wom_open-message"></a><span data-ttu-id="933c7-104">WOM \_ messaggio aperto</span><span class="sxs-lookup"><span data-stu-id="933c7-104">WOM\_OPEN message</span></span>

<span data-ttu-id="933c7-105">Il **messaggio \_ aperto WOM** viene inviato a una funzione di callback di output waveform-audio quando viene aperto un dispositivo di output della forma d'onda.</span><span class="sxs-lookup"><span data-stu-id="933c7-105">The **WOM\_OPEN** message is sent to a waveform-audio output callback function when a waveform-audio output device is opened.</span></span>


```C++
WOM_OPEN 
dwParam1 = reserved 
dwParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="933c7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="933c7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="933c7-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="933c7-107"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span></span>
</dt> <dd>

<span data-ttu-id="933c7-108">Riservati deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="933c7-108">Reserved; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="933c7-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="933c7-109"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="933c7-110">Riservati deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="933c7-110">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="933c7-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="933c7-111">Return Value</span></span>

<span data-ttu-id="933c7-112">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="933c7-112">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="933c7-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="933c7-113">Requirements</span></span>



| <span data-ttu-id="933c7-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="933c7-114">Requirement</span></span> | <span data-ttu-id="933c7-115">Valore</span><span class="sxs-lookup"><span data-stu-id="933c7-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="933c7-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="933c7-116">Minimum supported client</span></span><br/> | <span data-ttu-id="933c7-117">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="933c7-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="933c7-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="933c7-118">Minimum supported server</span></span><br/> | <span data-ttu-id="933c7-119">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="933c7-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="933c7-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="933c7-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="933c7-121"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="933c7-121"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="933c7-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="933c7-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="933c7-123">Audio Waveform</span><span class="sxs-lookup"><span data-stu-id="933c7-123">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="933c7-124">Messaggi di forma d'onda</span><span class="sxs-lookup"><span data-stu-id="933c7-124">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

 





