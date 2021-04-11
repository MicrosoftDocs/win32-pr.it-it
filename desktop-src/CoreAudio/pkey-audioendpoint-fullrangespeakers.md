---
description: La \_ Proprietà pkey AudioEndpoint \_ FullRangeSpeakers specifica la maschera Channel-Configuration per gli altoparlanti con intervallo completo connessi al dispositivo dell'endpoint audio.
ms.assetid: c0a54b3d-84dc-4771-8891-167ce00e2218
title: PKEY_AudioEndpoint_FullRangeSpeakers (mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0990d08e3d78eddf0fa6397e888b1e26c9f9a767
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127442"
---
# <a name="pkey_audioendpoint_fullrangespeakers"></a><span data-ttu-id="8005a-103">PKEY \_ AudioEndpoint \_ FullRangeSpeakers</span><span class="sxs-lookup"><span data-stu-id="8005a-103">PKEY\_AudioEndpoint\_FullRangeSpeakers</span></span>

<span data-ttu-id="8005a-104">La proprietà **pkey \_ AudioEndpoint \_ FullRangeSpeakers** specifica la maschera Channel-Configuration per gli altoparlanti con intervallo completo connessi al dispositivo dell'endpoint audio.</span><span class="sxs-lookup"><span data-stu-id="8005a-104">The **PKEY\_AudioEndpoint\_FullRangeSpeakers** property specifies the channel-configuration mask for the full-range speakers that are connected to the audio endpoint device.</span></span> <span data-ttu-id="8005a-105">La maschera indica la configurazione fisica degli altoparlanti con intervallo completo e specifica l'assegnazione di canali a tali altoparlanti.</span><span class="sxs-lookup"><span data-stu-id="8005a-105">The mask indicates the physical configuration of the full-range speakers and specifies the assignment of channels to those speakers.</span></span>

<span data-ttu-id="8005a-106">Il membro **VT** della struttura **PROPVARIANT** è impostato su VT \_ UI4.</span><span class="sxs-lookup"><span data-stu-id="8005a-106">The **vt** member of the **PROPVARIANT** structure is set to VT\_UI4.</span></span>

<span data-ttu-id="8005a-107">Il membro **uintVal** della struttura **PROPVARIANT** contiene una maschera di configurazione del canale di cui viene eseguito il cast nel tipo **uint**.</span><span class="sxs-lookup"><span data-stu-id="8005a-107">The **uintVal** member of the **PROPVARIANT** structure contains a channel-configuration mask that is cast to type **UINT**.</span></span>

<span data-ttu-id="8005a-108">Un altoparlante con intervallo completo è in grado di riprodurre suoni nell'intervallo completo, da bassi a acuti.</span><span class="sxs-lookup"><span data-stu-id="8005a-108">A full-range speaker is capable of playing sounds over the full range from bass to treble.</span></span> <span data-ttu-id="8005a-109">In genere, gli altoparlanti più grandi sono di intervallo completo, ma gli altoparlanti più piccoli sono significativamente meno in grado di riprodurre suoni bassi.</span><span class="sxs-lookup"><span data-stu-id="8005a-109">Typically, larger speakers are full range but smaller speakers are significantly less capable of playing bass sounds.</span></span> <span data-ttu-id="8005a-110">In Windows Vista, il motore audio utilizza questa proprietà per gestire i livelli bassi nel flusso di output audio che viene riprodotto dal dispositivo dell'endpoint audio.</span><span class="sxs-lookup"><span data-stu-id="8005a-110">In Windows Vista, the audio engine uses this property to manage bass levels in the audio output stream that is played by the audio endpoint device.</span></span>

<span data-ttu-id="8005a-111">La maschera Channel-Configuration per questa proprietà è nello stesso formato della maschera Channel-Configuration della proprietà [**pkey \_ AudioEndpoint \_ PhysicalSpeakers**](pkey-audioendpoint-physicalspeakers.md) .</span><span class="sxs-lookup"><span data-stu-id="8005a-111">The channel-configuration mask for this property is in the same format as the channel-configuration mask for the [**PKEY\_AudioEndpoint\_PhysicalSpeakers**](pkey-audioendpoint-physicalspeakers.md) property.</span></span> <span data-ttu-id="8005a-112">Per ulteriori informazioni sulle maschere di Channel-Configuration, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="8005a-112">For more information about channel-configuration masks, see the following:</span></span>

-   <span data-ttu-id="8005a-113">Descrizione della \_ proprietà di configurazione del canale audio KSPROPERTY \_ \_ nella documentazione di Windows DDK.</span><span class="sxs-lookup"><span data-stu-id="8005a-113">The description of the KSPROPERTY\_AUDIO\_CHANNEL\_CONFIG property in the Windows DDK documentation.</span></span>
-   <span data-ttu-id="8005a-114">Il white paper denominato "supporto driver audio per le configurazioni dell'altoparlante Home Theater" nel sito Web [tecnologie per dispositivi audio per Windows](https://www.microsoft.com/whdc/device/audio/default.mspx) .</span><span class="sxs-lookup"><span data-stu-id="8005a-114">The white paper titled "Audio Driver Support for Home Theater Speaker Configurations" at the [Audio Device Technologies for Windows](https://www.microsoft.com/whdc/device/audio/default.mspx) website.</span></span>

<span data-ttu-id="8005a-115">Il sistema ottiene la maschera di configurazione del canale per la \_ Proprietà pkey AudioEndpoint \_ FullRangeSpeakers dall'utente.</span><span class="sxs-lookup"><span data-stu-id="8005a-115">The system obtains the channel-configuration mask for the PKEY\_AudioEndpoint\_FullRangeSpeakers property from the user.</span></span> <span data-ttu-id="8005a-116">L'utente immette queste informazioni tramite il pannello di controllo multimediale di Windows Mmsys.cpl.</span><span class="sxs-lookup"><span data-stu-id="8005a-116">The user enters this information through the Windows multimedia control panel, Mmsys.cpl.</span></span> <span data-ttu-id="8005a-117">Per ulteriori informazioni su Mmsys.cpl, vedere la documentazione di Windows DDK.</span><span class="sxs-lookup"><span data-stu-id="8005a-117">For more information about Mmsys.cpl, see the Windows DDK documentation.</span></span>

<span data-ttu-id="8005a-118">La maschera Channel-Configuration per la \_ Proprietà pkey AudioEndpoint \_ FullRangeSpeakers di un dispositivo endpoint audio è un subset della maschera Channel-Configuration per la proprietà pkey \_ AudioEndpoint \_ PhysicalSpeakers dello stesso dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8005a-118">The channel-configuration mask for the PKEY\_AudioEndpoint\_FullRangeSpeakers property of an audio endpoint device is a subset of the channel-configuration mask for the PKEY\_AudioEndpoint\_PhysicalSpeakers property of the same device.</span></span>

<span data-ttu-id="8005a-119">Se, ad esempio, un dispositivo endpoint audio aziona un set di 5,1 altoparlanti surround, la maschera Channel-Configuration per la \_ Proprietà pkey AudioEndpoint \_ PHYSICALSPEAKERS è KSAUDIO \_ speaker \_ 5POINT1.</span><span class="sxs-lookup"><span data-stu-id="8005a-119">For example, if an audio endpoint device drives a set of 5.1 surround-sound speakers, then the channel-configuration mask for the PKEY\_AudioEndpoint\_PhysicalSpeakers property is KSAUDIO\_SPEAKER\_5POINT1.</span></span> <span data-ttu-id="8005a-120">Questa maschera indica la presenza di altoparlanti front-left, Front-Right, Front-Center, Side-Left e side-right, oltre a un subwoofer.</span><span class="sxs-lookup"><span data-stu-id="8005a-120">This mask indicates the presence of front-left, front-right, front-center, side-left, and side-right speakers—plus a subwoofer.</span></span> <span data-ttu-id="8005a-121">Se gli altoparlanti front-left e front-right sono sufficientemente grandi per produrre suoni bassi, ma il lato anteriore e quello inferiore non sono disponibili, la maschera Channel-Configuration per la proprietà PKEY \_ AudioEndpoint \_ FULLRANGESPEAKERS è KSAUDIO \_ speaker \_ stereo, che indica solo gli altoparlanti front-left e front-right.</span><span class="sxs-lookup"><span data-stu-id="8005a-121">If the front-left and front-right speakers are large enough to produce bass sounds but the smaller front-center and side speakers are not, then the channel-configuration mask for the PKEY\_AudioEndpoint\_FullRangeSpeakers property is KSAUDIO\_SPEAKER\_STEREO, which indicates only the front-left and front-right speakers.</span></span> <span data-ttu-id="8005a-122">Channel-Configuration Masks KSAUDIO \_ speaker \_ 5POINT1 e KSAUDIO \_ speaker \_ stereo sono definiti nel file di intestazione Ksmedia. h.</span><span class="sxs-lookup"><span data-stu-id="8005a-122">Channel-configuration masks KSAUDIO\_SPEAKER\_5POINT1 and KSAUDIO\_SPEAKER\_STEREO are defined in header file Ksmedia.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="8005a-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8005a-123">Requirements</span></span>



| <span data-ttu-id="8005a-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="8005a-124">Requirement</span></span> | <span data-ttu-id="8005a-125">Valore</span><span class="sxs-lookup"><span data-stu-id="8005a-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8005a-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8005a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="8005a-127">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8005a-127">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="8005a-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8005a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="8005a-129">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8005a-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="8005a-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8005a-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="8005a-131"><dt>Mmdeviceapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="8005a-131"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8005a-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8005a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8005a-133">**Proprietà endpoint audio**</span><span class="sxs-lookup"><span data-stu-id="8005a-133">**Audio Endpoint Properties**</span></span>](audio-endpoint-properties.md)
</dt> <dt>

[<span data-ttu-id="8005a-134">Proprietà audio principali</span><span class="sxs-lookup"><span data-stu-id="8005a-134">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> <dt>

[<span data-ttu-id="8005a-135">**PKEY \_ AudioEndpoint- \_ Proprietà PhysicalSpeakers**</span><span class="sxs-lookup"><span data-stu-id="8005a-135">**PKEY\_AudioEndpoint\_PhysicalSpeakers Property**</span></span>](pkey-audioendpoint-physicalspeakers.md)
</dt> </dl>

 

 




