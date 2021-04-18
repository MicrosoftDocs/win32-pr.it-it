---
description: "L'enumerazione AudioDeviceProperty viene usata dai metodi ITAudioDeviceControl:: GetRange, ITAudioDeviceControl:: Get e ITAudioDeviceControl:: set per indicare la proprietà da risolvere."
ms.assetid: 0ed9b75e-3c79-4e41-9883-63b85ebfae06
title: Enumerazione AudioDeviceProperty (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab807759bfb316858be41ea9bb4b78d795ee1a1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328738"
---
# <a name="audiodeviceproperty-enumeration"></a><span data-ttu-id="3c610-103">Enumerazione AudioDeviceProperty</span><span class="sxs-lookup"><span data-stu-id="3c610-103">AudioDeviceProperty enumeration</span></span>

<span data-ttu-id="3c610-104">\[ Questa enumerazione non è disponibile per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="3c610-104">\[ This enumeration is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="3c610-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="3c610-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="3c610-106">L'enumerazione **AudioDeviceProperty** viene usata dai metodi [**ITAudioDeviceControl:: GetRange**](itaudiodevicecontrol-getrange.md), [**ITAudioDeviceControl:: Get**](itaudiodevicecontrol-get.md)e [**ITAudioDeviceControl:: set**](itaudiodevicecontrol-set.md) per indicare la proprietà da risolvere.</span><span class="sxs-lookup"><span data-stu-id="3c610-106">The **AudioDeviceProperty** enum is used by the [**ITAudioDeviceControl::GetRange**](itaudiodevicecontrol-getrange.md), [**ITAudioDeviceControl::Get**](itaudiodevicecontrol-get.md), and [**ITAudioDeviceControl::Set**](itaudiodevicecontrol-set.md) methods to indicate the property being addressed.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c610-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3c610-107">Syntax</span></span>


```C++
} AudioDeviceProperty;
```



## <a name="constants"></a><span data-ttu-id="3c610-108">Costanti</span><span class="sxs-lookup"><span data-stu-id="3c610-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="3c610-109"><span id="AudioDevice_DuplexMode"></span><span id="audiodevice_duplexmode"></span><span id="AUDIODEVICE_DUPLEXMODE"></span>**\_DuplexMode AudioDevice**</span><span class="sxs-lookup"><span data-stu-id="3c610-109"><span id="AudioDevice_DuplexMode"></span><span id="audiodevice_duplexmode"></span><span id="AUDIODEVICE_DUPLEXMODE"></span>**AudioDevice\_DuplexMode**</span></span>
</dt> <dd>

<span data-ttu-id="3c610-110">Indica che è in corso l'impostazione o il recupero della modalità duplex del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3c610-110">Indicates that the duplex mode of the device is being set or retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="3c610-111"><span id="AudioDevice_AutomaticGainControl"></span><span id="audiodevice_automaticgaincontrol"></span><span id="AUDIODEVICE_AUTOMATICGAINCONTROL"></span>**\_AutomaticGainControl AudioDevice**</span><span class="sxs-lookup"><span data-stu-id="3c610-111"><span id="AudioDevice_AutomaticGainControl"></span><span id="audiodevice_automaticgaincontrol"></span><span id="AUDIODEVICE_AUTOMATICGAINCONTROL"></span>**AudioDevice\_AutomaticGainControl**</span></span>
</dt> <dd>

<span data-ttu-id="3c610-112">Indica che è in corso l'impostazione o il recupero del controllo del guadagno automatico del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3c610-112">Indicates that the automatic gain control of the device is being set or retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="3c610-113"><span id="AudioDevice_AcousticEchoCancellation"></span><span id="audiodevice_acousticechocancellation"></span><span id="AUDIODEVICE_ACOUSTICECHOCANCELLATION"></span>**\_AcousticEchoCancellation AudioDevice**</span><span class="sxs-lookup"><span data-stu-id="3c610-113"><span id="AudioDevice_AcousticEchoCancellation"></span><span id="audiodevice_acousticechocancellation"></span><span id="AUDIODEVICE_ACOUSTICECHOCANCELLATION"></span>**AudioDevice\_AcousticEchoCancellation**</span></span>
</dt> <dd>

<span data-ttu-id="3c610-114">Indica che le proprietà di annullamento Echo acustico del dispositivo vengono impostate o recuperate.</span><span class="sxs-lookup"><span data-stu-id="3c610-114">Indicates that the acoustic echo cancellation properties of the device are being set or retrieved.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3c610-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3c610-115">Requirements</span></span>



| <span data-ttu-id="3c610-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c610-116">Requirement</span></span> | <span data-ttu-id="3c610-117">Valore</span><span class="sxs-lookup"><span data-stu-id="3c610-117">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3c610-118">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="3c610-118">TAPI version</span></span><br/> | <span data-ttu-id="3c610-119">Richiede TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="3c610-119">Requires TAPI 3.1</span></span><br/>                                                       |
| <span data-ttu-id="3c610-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3c610-120">Header</span></span><br/>       | <dl> <span data-ttu-id="3c610-121"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c610-121"><dt>Ipmsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c610-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3c610-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c610-123">**ITAudioDeviceControl:: GetRange**</span><span class="sxs-lookup"><span data-stu-id="3c610-123">**ITAudioDeviceControl::GetRange**</span></span>](itaudiodevicecontrol-getrange.md)
</dt> <dt>

[<span data-ttu-id="3c610-124">**ITAudioDeviceControl:: Get**</span><span class="sxs-lookup"><span data-stu-id="3c610-124">**ITAudioDeviceControl::Get**</span></span>](itaudiodevicecontrol-get.md)
</dt> <dt>

[<span data-ttu-id="3c610-125">**ITAudioDeviceControl:: set**</span><span class="sxs-lookup"><span data-stu-id="3c610-125">**ITAudioDeviceControl::Set**</span></span>](itaudiodevicecontrol-set.md)
</dt> </dl>

 

 




