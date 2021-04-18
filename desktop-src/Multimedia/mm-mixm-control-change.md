---
title: Messaggio MM_MIXM_CONTROL_CHANGE (mmsystem. h)
description: Il \_ \_ messaggio di modifica del controllo MIXM mm \_ viene inviato da un dispositivo mixer per notificare a un'applicazione che lo stato di un controllo associato a una linea audio è stato modificato. L'applicazione deve aggiornare i valori visualizzati e memorizzati nella cache per il controllo specificato.
ms.assetid: 921c55a7-86c0-43d1-b817-bfbd3c4bb28b
keywords:
- MM_MIXM_CONTROL_CHANGE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MM_MIXM_CONTROL_CHANGE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12daa4d9e107a9ba687331731ee9fd7e6f0dc886
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302025"
---
# <a name="mm_mixm_control_change-message"></a><span data-ttu-id="53f8b-105">MM \_ \_ messaggio di \_ modifica controllo MIXM</span><span class="sxs-lookup"><span data-stu-id="53f8b-105">MM\_MIXM\_CONTROL\_CHANGE message</span></span>

<span data-ttu-id="53f8b-106">Il messaggio di **\_ \_ \_ modifica del controllo MIXM mm** viene inviato da un dispositivo mixer per notificare a un'applicazione che lo stato di un controllo associato a una linea audio è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="53f8b-106">The **MM\_MIXM\_CONTROL\_CHANGE** message is sent by a mixer device to notify an application that the state of a control associated with an audio line has changed.</span></span> <span data-ttu-id="53f8b-107">L'applicazione deve aggiornare i valori visualizzati e memorizzati nella cache per il controllo specificato.</span><span class="sxs-lookup"><span data-stu-id="53f8b-107">The application should refresh its display and cached values for the specified control.</span></span>


```C++
MM_MIXM_CONTROL_CHANGE 
wParam = (WPARAM) hMixer 
lParam = (LPARAM) dwControlID 
```



## <a name="parameters"></a><span data-ttu-id="53f8b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="53f8b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53f8b-109"><span id="hMixer"></span><span id="hmixer"></span><span id="HMIXER"></span>*hMixer*</span><span class="sxs-lookup"><span data-stu-id="53f8b-109"><span id="hMixer"></span><span id="hmixer"></span><span id="HMIXER"></span>*hMixer*</span></span>
</dt> <dd>

<span data-ttu-id="53f8b-110">Handle per il dispositivo mixer (**HMIXER**) che ha inviato il messaggio di notifica.</span><span class="sxs-lookup"><span data-stu-id="53f8b-110">Handle to the mixer device (**HMIXER**) that sent the notification message.</span></span>

</dd> <dt>

<span data-ttu-id="53f8b-111"><span id="dwControlID"></span><span id="dwcontrolid"></span><span id="DWCONTROLID"></span>*dwControlID*</span><span class="sxs-lookup"><span data-stu-id="53f8b-111"><span id="dwControlID"></span><span id="dwcontrolid"></span><span id="DWCONTROLID"></span>*dwControlID*</span></span>
</dt> <dd>

<span data-ttu-id="53f8b-112">Identificatore di controllo per il controllo mixer con stato modificato.</span><span class="sxs-lookup"><span data-stu-id="53f8b-112">Control identifier for the mixer control that has changed state.</span></span> <span data-ttu-id="53f8b-113">Questo identificatore corrisponde al membro **dwControlID** della struttura **MIXERCONTROL** restituita dalla funzione **mixerGetlineControls**.</span><span class="sxs-lookup"><span data-stu-id="53f8b-113">This identifier is the same as the **dwControlID** member of the **MIXERCONTROL** structure returned by the **mixerGetLineControls** function.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="53f8b-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="53f8b-114">Remarks</span></span>

<span data-ttu-id="53f8b-115">Un'applicazione deve aprire un dispositivo mixer e specificare una finestra di callback per ricevere il messaggio di **\_ \_ \_ modifica del controllo MIXM mm** .</span><span class="sxs-lookup"><span data-stu-id="53f8b-115">An application must open a mixer device and specify a callback window to receive the **MM\_MIXM\_CONTROL\_CHANGE** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="53f8b-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="53f8b-116">Requirements</span></span>



| <span data-ttu-id="53f8b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="53f8b-117">Requirement</span></span> | <span data-ttu-id="53f8b-118">Valore</span><span class="sxs-lookup"><span data-stu-id="53f8b-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53f8b-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="53f8b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="53f8b-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="53f8b-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="53f8b-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="53f8b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="53f8b-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="53f8b-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="53f8b-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="53f8b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="53f8b-124"><dt>Mmsystem. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="53f8b-124"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53f8b-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="53f8b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53f8b-126">Mixer audio</span><span class="sxs-lookup"><span data-stu-id="53f8b-126">Audio Mixers</span></span>](audio-mixers.md)
</dt> <dt>

[<span data-ttu-id="53f8b-127">Messaggi mixer audio</span><span class="sxs-lookup"><span data-stu-id="53f8b-127">Audio Mixer Messages</span></span>](audio-mixer-messages.md)
</dt> </dl>

 

 





