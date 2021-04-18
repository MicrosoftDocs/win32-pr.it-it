---
description: "L'enumerazione AudioSettingsProperty viene usata dai metodi ITAudioSettings:: GetRange, ITAudioSettings:: Get e ITAudioSettings:: set per indicare la proprietà dell'impostazione audio da risolvere."
ms.assetid: b91c8213-f102-4ebb-ad8a-e43709b3daad
title: Enumerazione AudioSettingsProperty (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 759e3ca9d9559c35c64c117b9b84b1cee4a1fad1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328735"
---
# <a name="audiosettingsproperty-enumeration"></a><span data-ttu-id="34e4c-103">Enumerazione AudioSettingsProperty</span><span class="sxs-lookup"><span data-stu-id="34e4c-103">AudioSettingsProperty enumeration</span></span>

<span data-ttu-id="34e4c-104">\[ Questa enumerazione non è disponibile per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="34e4c-104">\[ This enumeration is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="34e4c-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="34e4c-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="34e4c-106">L'enumerazione **AudioSettingsProperty** viene usata dai metodi [**ITAudioSettings:: GetRange**](itaudiosettings-getrange.md), [**ITAudioSettings:: Get**](itaudiosettings-get.md)e [**ITAudioSettings:: set**](itaudiosettings-set.md) per indicare la proprietà dell'impostazione audio da risolvere.</span><span class="sxs-lookup"><span data-stu-id="34e4c-106">The **AudioSettingsProperty** enum is used by the [**ITAudioSettings::GetRange**](itaudiosettings-getrange.md), [**ITAudioSettings::Get**](itaudiosettings-get.md), and [**ITAudioSettings::Set**](itaudiosettings-set.md) methods to indicate the audio setting property being addressed.</span></span>

## <a name="syntax"></a><span data-ttu-id="34e4c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="34e4c-107">Syntax</span></span>


```C++
} AudioSettingsProperty;
```



## <a name="constants"></a><span data-ttu-id="34e4c-108">Costanti</span><span class="sxs-lookup"><span data-stu-id="34e4c-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="34e4c-109"><span id="AudioSettings_SignalLevel"></span><span id="audiosettings_signallevel"></span><span id="AUDIOSETTINGS_SIGNALLEVEL"></span>**\_SignalLevel AudioSettings**</span><span class="sxs-lookup"><span data-stu-id="34e4c-109"><span id="AudioSettings_SignalLevel"></span><span id="audiosettings_signallevel"></span><span id="AUDIOSETTINGS_SIGNALLEVEL"></span>**AudioSettings\_SignalLevel**</span></span>
</dt> <dd>

<span data-ttu-id="34e4c-110">Proprietà delle impostazioni del segnale.</span><span class="sxs-lookup"><span data-stu-id="34e4c-110">Signal settings property.</span></span>

</dd> <dt>

<span data-ttu-id="34e4c-111"><span id="AudioSettings_SilenceThreshold"></span><span id="audiosettings_silencethreshold"></span><span id="AUDIOSETTINGS_SILENCETHRESHOLD"></span>**\_SilenceThreshold AudioSettings**</span><span class="sxs-lookup"><span data-stu-id="34e4c-111"><span id="AudioSettings_SilenceThreshold"></span><span id="audiosettings_silencethreshold"></span><span id="AUDIOSETTINGS_SILENCETHRESHOLD"></span>**AudioSettings\_SilenceThreshold**</span></span>
</dt> <dd>

<span data-ttu-id="34e4c-112">Proprietà soglia di inattività.</span><span class="sxs-lookup"><span data-stu-id="34e4c-112">Silence threshold property.</span></span>

</dd> <dt>

<span data-ttu-id="34e4c-113"><span id="AudioSettings_Volume"></span><span id="audiosettings_volume"></span><span id="AUDIOSETTINGS_VOLUME"></span>**\_Volume AudioSettings**</span><span class="sxs-lookup"><span data-stu-id="34e4c-113"><span id="AudioSettings_Volume"></span><span id="audiosettings_volume"></span><span id="AUDIOSETTINGS_VOLUME"></span>**AudioSettings\_Volume**</span></span>
</dt> <dd>

<span data-ttu-id="34e4c-114">Proprietà del volume.</span><span class="sxs-lookup"><span data-stu-id="34e4c-114">Volume property.</span></span>

</dd> <dt>

<span data-ttu-id="34e4c-115"><span id="AudioSettings_Balance"></span><span id="audiosettings_balance"></span><span id="AUDIOSETTINGS_BALANCE"></span>**\_Bilanciamento AudioSettings**</span><span class="sxs-lookup"><span data-stu-id="34e4c-115"><span id="AudioSettings_Balance"></span><span id="audiosettings_balance"></span><span id="AUDIOSETTINGS_BALANCE"></span>**AudioSettings\_Balance**</span></span>
</dt> <dd>

<span data-ttu-id="34e4c-116">Proprietà Balance.</span><span class="sxs-lookup"><span data-stu-id="34e4c-116">Balance property.</span></span>

</dd> <dt>

<span data-ttu-id="34e4c-117"><span id="AudioSettings_Loudness"></span><span id="audiosettings_loudness"></span><span id="AUDIOSETTINGS_LOUDNESS"></span>**\_Sonorità AudioSettings**</span><span class="sxs-lookup"><span data-stu-id="34e4c-117"><span id="AudioSettings_Loudness"></span><span id="audiosettings_loudness"></span><span id="AUDIOSETTINGS_LOUDNESS"></span>**AudioSettings\_Loudness**</span></span>
</dt> <dd>

<span data-ttu-id="34e4c-118">Proprietà di sonorità.</span><span class="sxs-lookup"><span data-stu-id="34e4c-118">Loudness property.</span></span>

</dd> <dt>

<span data-ttu-id="34e4c-119"><span id="AudioSettings_Treble"></span><span id="audiosettings_treble"></span><span id="AUDIOSETTINGS_TREBLE"></span>**AudioSettings \_ acuti**</span><span class="sxs-lookup"><span data-stu-id="34e4c-119"><span id="AudioSettings_Treble"></span><span id="audiosettings_treble"></span><span id="AUDIOSETTINGS_TREBLE"></span>**AudioSettings\_Treble**</span></span>
</dt> <dd>

<span data-ttu-id="34e4c-120">Proprietà Treble.</span><span class="sxs-lookup"><span data-stu-id="34e4c-120">Treble property.</span></span>

</dd> <dt>

<span data-ttu-id="34e4c-121"><span id="AudioSettings_Bass"></span><span id="audiosettings_bass"></span><span id="AUDIOSETTINGS_BASS"></span>**AudioSettings \_ Bass**</span><span class="sxs-lookup"><span data-stu-id="34e4c-121"><span id="AudioSettings_Bass"></span><span id="audiosettings_bass"></span><span id="AUDIOSETTINGS_BASS"></span>**AudioSettings\_Bass**</span></span>
</dt> <dd>

<span data-ttu-id="34e4c-122">Proprietà Bass.</span><span class="sxs-lookup"><span data-stu-id="34e4c-122">Bass property.</span></span>

</dd> <dt>

<span data-ttu-id="34e4c-123"><span id="AudioSettings_Mono"></span><span id="audiosettings_mono"></span><span id="AUDIOSETTINGS_MONO"></span>**\_Mono AudioSettings**</span><span class="sxs-lookup"><span data-stu-id="34e4c-123"><span id="AudioSettings_Mono"></span><span id="audiosettings_mono"></span><span id="AUDIOSETTINGS_MONO"></span>**AudioSettings\_Mono**</span></span>
</dt> <dd>

<span data-ttu-id="34e4c-124">Proprietà mono.</span><span class="sxs-lookup"><span data-stu-id="34e4c-124">Monaural property.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="34e4c-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="34e4c-125">Requirements</span></span>



| <span data-ttu-id="34e4c-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="34e4c-126">Requirement</span></span> | <span data-ttu-id="34e4c-127">Valore</span><span class="sxs-lookup"><span data-stu-id="34e4c-127">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="34e4c-128">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="34e4c-128">TAPI version</span></span><br/> | <span data-ttu-id="34e4c-129">Richiede TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="34e4c-129">Requires TAPI 3.1</span></span><br/>                                                       |
| <span data-ttu-id="34e4c-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="34e4c-130">Header</span></span><br/>       | <dl> <span data-ttu-id="34e4c-131"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="34e4c-131"><dt>Ipmsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34e4c-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="34e4c-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34e4c-133">**ITAudioSettings:: GetRange**</span><span class="sxs-lookup"><span data-stu-id="34e4c-133">**ITAudioSettings::GetRange**</span></span>](itaudiosettings-getrange.md)
</dt> <dt>

[<span data-ttu-id="34e4c-134">**ITAudioSettings:: Get**</span><span class="sxs-lookup"><span data-stu-id="34e4c-134">**ITAudioSettings::Get**</span></span>](itaudiosettings-get.md)
</dt> <dt>

[<span data-ttu-id="34e4c-135">**ITAudioSettings:: set**</span><span class="sxs-lookup"><span data-stu-id="34e4c-135">**ITAudioSettings::Set**</span></span>](itaudiosettings-set.md)
</dt> </dl>

 

 




