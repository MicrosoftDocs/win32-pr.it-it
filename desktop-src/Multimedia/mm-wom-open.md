---
title: Messaggio MM_WOM_OPEN (mmsystem. h)
description: Il \_ \_ messaggio di apertura mm WOM viene inviato a una finestra quando viene aperto il dispositivo di output della forma d'onda specificata.
ms.assetid: 1b0366de-61cd-4203-9173-ababaefdb153
keywords:
- MM_WOM_OPEN messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MM_WOM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 783910389f2b9be9193c8f7bb0722f70261f5fce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121663"
---
# <a name="mm_wom_open-message"></a><span data-ttu-id="ea8e6-104">MM \_ WOM \_ messaggio aperto</span><span class="sxs-lookup"><span data-stu-id="ea8e6-104">MM\_WOM\_OPEN message</span></span>

<span data-ttu-id="ea8e6-105">Il messaggio di **\_ \_ apertura mm WOM** viene inviato a una finestra quando viene aperto il dispositivo di output della forma d'onda specificata.</span><span class="sxs-lookup"><span data-stu-id="ea8e6-105">The **MM\_WOM\_OPEN** message is sent to a window when the given waveform-audio output device is opened.</span></span>


```C++
MM_WOM_OPEN 
wParam = (WPARAM) hOutputDev 
lParam = reserved 
```



## <a name="parameters"></a><span data-ttu-id="ea8e6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ea8e6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea8e6-107"><span id="hOutputDev"></span><span id="houtputdev"></span><span id="HOUTPUTDEV"></span>*hOutputDev*</span><span class="sxs-lookup"><span data-stu-id="ea8e6-107"><span id="hOutputDev"></span><span id="houtputdev"></span><span id="HOUTPUTDEV"></span>*hOutputDev*</span></span>
</dt> <dd>

<span data-ttu-id="ea8e6-108">Handle per il dispositivo che è stato aperto.</span><span class="sxs-lookup"><span data-stu-id="ea8e6-108">Handle to the device that was opened.</span></span>

</dd> <dt>

<span data-ttu-id="ea8e6-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="ea8e6-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="ea8e6-110">Riservati deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="ea8e6-110">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea8e6-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ea8e6-111">Return Value</span></span>

<span data-ttu-id="ea8e6-112">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="ea8e6-112">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea8e6-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ea8e6-113">Requirements</span></span>



| <span data-ttu-id="ea8e6-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea8e6-114">Requirement</span></span> | <span data-ttu-id="ea8e6-115">Valore</span><span class="sxs-lookup"><span data-stu-id="ea8e6-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea8e6-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ea8e6-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ea8e6-117">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ea8e6-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ea8e6-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ea8e6-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ea8e6-119">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ea8e6-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ea8e6-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ea8e6-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea8e6-121"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ea8e6-121"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea8e6-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ea8e6-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea8e6-123">Audio Waveform</span><span class="sxs-lookup"><span data-stu-id="ea8e6-123">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="ea8e6-124">Messaggi di forma d'onda</span><span class="sxs-lookup"><span data-stu-id="ea8e6-124">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

 





