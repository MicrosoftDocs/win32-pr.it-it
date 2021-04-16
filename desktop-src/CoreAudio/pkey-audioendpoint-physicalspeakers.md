---
description: 'Altre informazioni su: PKEY_AudioEndpoint_PhysicalSpeakers'
ms.assetid: 20049071-0a14-421e-8bc5-04af9c7117b0
title: PKEY_AudioEndpoint_PhysicalSpeakers (mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6a627ec97dc329f50cc58a15d0df516f598af86
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524081"
---
# <a name="pkey_audioendpoint_physicalspeakers"></a><span data-ttu-id="fc976-103">PKEY \_ AudioEndpoint \_ PhysicalSpeakers</span><span class="sxs-lookup"><span data-stu-id="fc976-103">PKEY\_AudioEndpoint\_PhysicalSpeakers</span></span>

<span data-ttu-id="fc976-104">La proprietà **pkey \_ AudioEndpoint \_ PhysicalSpeakers** specifica la maschera canale-configurazione per il dispositivo dell'endpoint audio.</span><span class="sxs-lookup"><span data-stu-id="fc976-104">The **PKEY\_AudioEndpoint\_PhysicalSpeakers** property specifies the channel-configuration mask for the audio endpoint device.</span></span> <span data-ttu-id="fc976-105">La maschera indica la configurazione fisica di un set di altoparlanti e specifica l'assegnazione dei canali agli altoparlanti.</span><span class="sxs-lookup"><span data-stu-id="fc976-105">The mask indicates the physical configuration of a set of speakers and specifies the assignment of channels to speakers.</span></span> <span data-ttu-id="fc976-106">Per ulteriori informazioni sulle maschere di Channel-Configuration, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="fc976-106">For more information about channel-configuration masks, see the following:</span></span>

1.  <span data-ttu-id="fc976-107">Descrizione della \_ proprietà di configurazione del canale audio KSPROPERTY \_ \_ nella documentazione di Windows DDK.</span><span class="sxs-lookup"><span data-stu-id="fc976-107">The description of the KSPROPERTY\_AUDIO\_CHANNEL\_CONFIG property in the Windows DDK documentation.</span></span>
2.  <span data-ttu-id="fc976-108">Il white paper denominato "supporto driver audio per le configurazioni dell'altoparlante Home Theater" nel sito Web [tecnologie per dispositivi audio per Windows](https://www.microsoft.com/whdc/device/audio/default.mspx) .</span><span class="sxs-lookup"><span data-stu-id="fc976-108">The white paper titled "Audio Driver Support for Home Theater Speaker Configurations" at the [Audio Device Technologies for Windows](https://www.microsoft.com/whdc/device/audio/default.mspx) website.</span></span>

<span data-ttu-id="fc976-109">Il membro **VT** della struttura **PROPVARIANT** è impostato su VT \_ UI4.</span><span class="sxs-lookup"><span data-stu-id="fc976-109">The **vt** member of the **PROPVARIANT** structure is set to VT\_UI4.</span></span>

<span data-ttu-id="fc976-110">Il membro **uintVal** della struttura **PROPVARIANT** contiene una maschera di configurazione del canale di cui viene eseguito il cast nel tipo **uint**.</span><span class="sxs-lookup"><span data-stu-id="fc976-110">The **uintVal** member of the **PROPVARIANT** structure contains a channel-configuration mask that is cast to type **UINT**.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc976-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fc976-111">Requirements</span></span>



| <span data-ttu-id="fc976-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc976-112">Requirement</span></span> | <span data-ttu-id="fc976-113">Valore</span><span class="sxs-lookup"><span data-stu-id="fc976-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc976-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fc976-114">Minimum supported client</span></span><br/> | <span data-ttu-id="fc976-115">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fc976-115">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="fc976-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fc976-116">Minimum supported server</span></span><br/> | <span data-ttu-id="fc976-117">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fc976-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="fc976-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fc976-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc976-119"><dt>Mmdeviceapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc976-119"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc976-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fc976-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc976-121">**Proprietà endpoint audio**</span><span class="sxs-lookup"><span data-stu-id="fc976-121">**Audio Endpoint Properties**</span></span>](audio-endpoint-properties.md)
</dt> <dt>

[<span data-ttu-id="fc976-122">Proprietà audio principali</span><span class="sxs-lookup"><span data-stu-id="fc976-122">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> </dl>

 

 




