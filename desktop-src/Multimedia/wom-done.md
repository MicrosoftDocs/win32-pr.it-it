---
title: Messaggio WOM_DONE (mmsystem. h)
description: Il \_ messaggio WOM done viene inviato a una funzione di callback di output waveform-audio quando il buffer di output specificato viene restituito all'applicazione.
ms.assetid: cac94a44-d1b0-43de-b3ec-ae34547b1fc3
keywords:
- WOM_DONE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- WOM_DONE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab64598a2dfdd329615ca116fb6382909bb83b01
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119131"
---
# <a name="wom_done-message"></a><span data-ttu-id="6ab62-104">\_Messaggio WOM completato</span><span class="sxs-lookup"><span data-stu-id="6ab62-104">WOM\_DONE message</span></span>

<span data-ttu-id="6ab62-105">Il messaggio **WOM \_ done** viene inviato a una funzione di callback di output waveform-audio quando il buffer di output specificato viene restituito all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6ab62-105">The **WOM\_DONE** message is sent to a waveform-audio output callback function when the given output buffer is being returned to the application.</span></span> <span data-ttu-id="6ab62-106">I buffer vengono restituiti all'applicazione quando vengono riprodotti o come risultato di una chiamata alla funzione [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset) .</span><span class="sxs-lookup"><span data-stu-id="6ab62-106">Buffers are returned to the application when they have been played, or as the result of a call to the [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset) function.</span></span>


```C++
WOM_DONE 
dwParam1 = (DWORD) lpwvhdr 
dwParam2 = reserved 
```



## <a name="parameters"></a><span data-ttu-id="6ab62-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="6ab62-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ab62-108"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="6ab62-108"><span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*</span></span>
</dt> <dd>

<span data-ttu-id="6ab62-109">Puntatore a una struttura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) che identifica il buffer.</span><span class="sxs-lookup"><span data-stu-id="6ab62-109">Pointer to a [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure identifying the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="6ab62-110"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="6ab62-110"><span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*</span></span>
</dt> <dd>

<span data-ttu-id="6ab62-111">Riservati deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="6ab62-111">Reserved; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ab62-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6ab62-112">Return Value</span></span>

<span data-ttu-id="6ab62-113">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="6ab62-113">This message does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ab62-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6ab62-114">Requirements</span></span>



| <span data-ttu-id="6ab62-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ab62-115">Requirement</span></span> | <span data-ttu-id="6ab62-116">Valore</span><span class="sxs-lookup"><span data-stu-id="6ab62-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ab62-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6ab62-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6ab62-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6ab62-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="6ab62-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6ab62-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6ab62-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6ab62-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="6ab62-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6ab62-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ab62-122"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6ab62-122"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ab62-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6ab62-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ab62-124">Audio Waveform</span><span class="sxs-lookup"><span data-stu-id="6ab62-124">Waveform Audio</span></span>](waveform-audio.md)
</dt> <dt>

[<span data-ttu-id="6ab62-125">Messaggi di forma d'onda</span><span class="sxs-lookup"><span data-stu-id="6ab62-125">Waveform Messages</span></span>](waveform-messages.md)
</dt> </dl>

 

