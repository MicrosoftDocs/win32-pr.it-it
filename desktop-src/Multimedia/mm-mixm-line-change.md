---
title: Messaggio MM_MIXM_LINE_CHANGE (mmsystem. h)
description: Il \_ messaggio di modifica della riga MIXM mm \_ \_ viene inviato da un dispositivo mixer per notificare a un'applicazione che lo stato di una linea audio sul dispositivo specificato è stato modificato. L'applicazione deve aggiornare i valori visualizzati e memorizzati nella cache per la riga audio specificata.
ms.assetid: 68ada0be-9dc5-4edf-b924-ef0d10a1b79a
keywords:
- MM_MIXM_LINE_CHANGE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MM_MIXM_LINE_CHANGE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92c4aa10d9934f8cf5f5747ecb4e4eb736af2655
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302024"
---
# <a name="mm_mixm_line_change-message"></a><span data-ttu-id="6c4ce-105">MIXM MM- \_ \_ messaggio di \_ modifica riga</span><span class="sxs-lookup"><span data-stu-id="6c4ce-105">MM\_MIXM\_LINE\_CHANGE message</span></span>

<span data-ttu-id="6c4ce-106">Il messaggio di **\_ \_ \_ modifica della riga MIXM mm** viene inviato da un dispositivo mixer per notificare a un'applicazione che lo stato di una linea audio sul dispositivo specificato è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="6c4ce-106">The **MM\_MIXM\_LINE\_CHANGE** message is sent by a mixer device to notify an application that the state of an audio line on the specified device has changed.</span></span> <span data-ttu-id="6c4ce-107">L'applicazione deve aggiornare i valori visualizzati e memorizzati nella cache per la riga audio specificata.</span><span class="sxs-lookup"><span data-stu-id="6c4ce-107">The application should refresh its display and cached values for the specified audio line.</span></span>


```C++
MM_MIXM_LINE_CHANGE 
wParam = (WPARAM) hMixer 
lParam = (LPARAM) dwLineID 
```



## <a name="parameters"></a><span data-ttu-id="6c4ce-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="6c4ce-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c4ce-109"><span id="hMixer"></span><span id="hmixer"></span><span id="HMIXER"></span>*hMixer*</span><span class="sxs-lookup"><span data-stu-id="6c4ce-109"><span id="hMixer"></span><span id="hmixer"></span><span id="HMIXER"></span>*hMixer*</span></span>
</dt> <dd>

<span data-ttu-id="6c4ce-110">Handle per il dispositivo mixer che ha inviato il messaggio di notifica.</span><span class="sxs-lookup"><span data-stu-id="6c4ce-110">Handle to the mixer device that sent the notification message.</span></span>

</dd> <dt>

<span data-ttu-id="6c4ce-111"><span id="dwLineID"></span><span id="dwlineid"></span><span id="DWLINEID"></span>*dwLineID*</span><span class="sxs-lookup"><span data-stu-id="6c4ce-111"><span id="dwLineID"></span><span id="dwlineid"></span><span id="DWLINEID"></span>*dwLineID*</span></span>
</dt> <dd>

<span data-ttu-id="6c4ce-112">Identificatore di riga per la linea audio con stato modificato.</span><span class="sxs-lookup"><span data-stu-id="6c4ce-112">Line identifier for the audio line that has changed state.</span></span> <span data-ttu-id="6c4ce-113">Questo identificatore corrisponde al membro **dwLineID** della struttura **MIXERLINE** restituita dalla funzione **mixerGetLineInfo**.</span><span class="sxs-lookup"><span data-stu-id="6c4ce-113">This identifier is the same as the **dwLineID** member of the **MIXERLINE** structure returned by the **mixerGetLineInfo** function.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6c4ce-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="6c4ce-114">Remarks</span></span>

<span data-ttu-id="6c4ce-115">Un'applicazione deve aprire un dispositivo mixer e specificare una finestra di callback per ricevere il messaggio di **\_ \_ \_ modifica della riga MIXM mm** .</span><span class="sxs-lookup"><span data-stu-id="6c4ce-115">An application must open a mixer device and specify a callback window to receive the **MM\_MIXM\_LINE\_CHANGE** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c4ce-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6c4ce-116">Requirements</span></span>



| <span data-ttu-id="6c4ce-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c4ce-117">Requirement</span></span> | <span data-ttu-id="6c4ce-118">Valore</span><span class="sxs-lookup"><span data-stu-id="6c4ce-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c4ce-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6c4ce-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6c4ce-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6c4ce-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="6c4ce-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6c4ce-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6c4ce-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6c4ce-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="6c4ce-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6c4ce-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c4ce-124"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6c4ce-124"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c4ce-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6c4ce-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c4ce-126">Mixer audio</span><span class="sxs-lookup"><span data-stu-id="6c4ce-126">Audio Mixers</span></span>](audio-mixers.md)
</dt> <dt>

[<span data-ttu-id="6c4ce-127">Messaggi mixer audio</span><span class="sxs-lookup"><span data-stu-id="6c4ce-127">Audio Mixer Messages</span></span>](audio-mixer-messages.md)
</dt> </dl>

 

 





