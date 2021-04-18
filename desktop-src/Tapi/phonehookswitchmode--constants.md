---
description: Le \_ costanti del flag di bit PHONEHOOKSWITCHMODE descrivono i componenti del microfono e del relatore di un dispositivo hookswitch.
ms.assetid: 532bf089-d5ca-4a04-847d-69e48990ff5c
title: Costanti PHONEHOOKSWITCHMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8028cb531d5b38185edf75ae58e4c3c855398f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333944"
---
# <a name="phonehookswitchmode_-constants"></a><span data-ttu-id="91a53-103">\_Costanti PHONEHOOKSWITCHMODE</span><span class="sxs-lookup"><span data-stu-id="91a53-103">PHONEHOOKSWITCHMODE\_ Constants</span></span>

<span data-ttu-id="91a53-104">Le costanti del flag di bit **PHONEHOOKSWITCHMODE \_** descrivono i componenti del microfono e del relatore di un dispositivo hookswitch.</span><span class="sxs-lookup"><span data-stu-id="91a53-104">The **PHONEHOOKSWITCHMODE\_** bit-flag constants describe the microphone and speaker components of a hookswitch device.</span></span>

<dl> <dt>

<span data-ttu-id="91a53-105"><span id="PHONEHOOKSWITCHMODE_MIC"></span><span id="phonehookswitchmode_mic"></span>**PHONEHOOKSWITCHMODE \_ MIC**</span><span class="sxs-lookup"><span data-stu-id="91a53-105"><span id="PHONEHOOKSWITCHMODE_MIC"></span><span id="phonehookswitchmode_mic"></span>**PHONEHOOKSWITCHMODE\_MIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="91a53-106">Il microfono del dispositivo è attivo, l'altoparlante è disattivato.</span><span class="sxs-lookup"><span data-stu-id="91a53-106">The device's microphone is active, the speaker is mute.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="91a53-107"><span id="PHONEHOOKSWITCHMODE_MICSPEAKER"></span><span id="phonehookswitchmode_micspeaker"></span>**\_MICSPEAKER PHONEHOOKSWITCHMODE**</span><span class="sxs-lookup"><span data-stu-id="91a53-107"><span id="PHONEHOOKSWITCHMODE_MICSPEAKER"></span><span id="phonehookswitchmode_micspeaker"></span>**PHONEHOOKSWITCHMODE\_MICSPEAKER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="91a53-108">Il microfono e l'altoparlante del dispositivo sono entrambi attivi.</span><span class="sxs-lookup"><span data-stu-id="91a53-108">The device's microphone and speaker are both active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="91a53-109"><span id="PHONEHOOKSWITCHMODE_ONHOOK"></span><span id="phonehookswitchmode_onhook"></span>**OnHook PHONEHOOKSWITCHMODE \_**</span><span class="sxs-lookup"><span data-stu-id="91a53-109"><span id="PHONEHOOKSWITCHMODE_ONHOOK"></span><span id="phonehookswitchmode_onhook"></span>**PHONEHOOKSWITCHMODE\_ONHOOK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="91a53-110">Il microfono e l'altoparlante del dispositivo sono entrambi OnHook.</span><span class="sxs-lookup"><span data-stu-id="91a53-110">The device's microphone and speaker are both onhook.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="91a53-111"><span id="PHONEHOOKSWITCHMODE_SPEAKER"></span><span id="phonehookswitchmode_speaker"></span>**PHONEHOOKSWITCHMODE \_ speaker**</span><span class="sxs-lookup"><span data-stu-id="91a53-111"><span id="PHONEHOOKSWITCHMODE_SPEAKER"></span><span id="phonehookswitchmode_speaker"></span>**PHONEHOOKSWITCHMODE\_SPEAKER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="91a53-112">L'altoparlante del dispositivo è attivo, il microfono è disattivato.</span><span class="sxs-lookup"><span data-stu-id="91a53-112">The device's speaker is active, the microphone is mute.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="91a53-113"><span id="PHONEHOOKSWITCHMODE_UNKNOWN"></span><span id="phonehookswitchmode_unknown"></span>**PHONEHOOKSWITCHMODE \_ sconosciuto**</span><span class="sxs-lookup"><span data-stu-id="91a53-113"><span id="PHONEHOOKSWITCHMODE_UNKNOWN"></span><span id="phonehookswitchmode_unknown"></span>**PHONEHOOKSWITCHMODE\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="91a53-114">La modalità hookswitch del dispositivo è sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="91a53-114">The device's hookswitch mode is currently unknown.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="91a53-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="91a53-115">Remarks</span></span>

<span data-ttu-id="91a53-116">Nessuna estensibilità.</span><span class="sxs-lookup"><span data-stu-id="91a53-116">No extensibility.</span></span> <span data-ttu-id="91a53-117">Tutti i 32 bit sono riservati.</span><span class="sxs-lookup"><span data-stu-id="91a53-117">All 32 bits are reserved.</span></span>

<span data-ttu-id="91a53-118">Queste costanti vengono usate per fornire un singolo livello di controllo sui componenti del microfono e del altoparlante di un dispositivo telefonico.</span><span class="sxs-lookup"><span data-stu-id="91a53-118">These constants are used to provide an individual level of control over the microphone and speaker components of a phone device.</span></span>

## <a name="requirements"></a><span data-ttu-id="91a53-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="91a53-119">Requirements</span></span>



| <span data-ttu-id="91a53-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="91a53-120">Requirement</span></span> | <span data-ttu-id="91a53-121">Valore</span><span class="sxs-lookup"><span data-stu-id="91a53-121">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="91a53-122">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="91a53-122">TAPI version</span></span><br/> | <span data-ttu-id="91a53-123">Richiede TAPI 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="91a53-123">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="91a53-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="91a53-124">Header</span></span><br/>       | <dl> <span data-ttu-id="91a53-125"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="91a53-125"><dt>Tapi.h</dt></span></span> </dl> |



 

 




