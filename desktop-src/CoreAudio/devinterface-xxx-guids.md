---
description: I \_ GUID DEVINTERFACE xxx vengono usati per rappresentare i GUID per le interfacce del dispositivo.
ms.assetid: 2503463B-D7C6-4C82-8421-424D79FD1C2A
title: GUID di DEVINTERFACE_XXX (mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 796f113d26ebc351a4d576ed76485d24d89fdb04
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330095"
---
# <a name="devinterface_xxx-guids"></a><span data-ttu-id="2cd9d-103">\_GUID DEVINTERFACE xxx</span><span class="sxs-lookup"><span data-stu-id="2cd9d-103">DEVINTERFACE\_XXX GUIDs</span></span>

<span data-ttu-id="2cd9d-104">I \_ GUID DEVINTERFACE xxx vengono usati per rappresentare i GUID per le interfacce del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2cd9d-104">The DEVINTERFACE\_XXX GUIDs are used to represent the GUIDs for device interfaces.</span></span>

<dl> <dt>

<span data-ttu-id="2cd9d-105"><span id="DEVINTERFACE_AUDIO_CAPTURE"></span><span id="devinterface_audio_capture"></span>**\_acquisizione audio \_ DEVINTERFACE**</span><span class="sxs-lookup"><span data-stu-id="2cd9d-105"><span id="DEVINTERFACE_AUDIO_CAPTURE"></span><span id="devinterface_audio_capture"></span>**DEVINTERFACE\_AUDIO\_CAPTURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2cd9d-106">Specifica la stringa di query utilizzata per enumerare tutti i dispositivi di acquisizione audio nel sistema.</span><span class="sxs-lookup"><span data-stu-id="2cd9d-106">Specifies the query string used to enumerate all audio capture devices on the system.</span></span> <span data-ttu-id="2cd9d-107">Questo valore viene restituito da [**MediaDevice:: GetAudioCaptureSelector**](/uwp/api/windows.media.devices.mediadevice.getaudiocaptureselector).</span><span class="sxs-lookup"><span data-stu-id="2cd9d-107">This value is returned by [**MediaDevice::GetAudioCaptureSelector**](/uwp/api/windows.media.devices.mediadevice.getaudiocaptureselector).</span></span>

<span data-ttu-id="2cd9d-108">Il passaggio di questo valore a [**ActivateAudioInterfaceAsync**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync) attiva l'interfaccia richiesta sul dispositivo di acquisizione audio predefinito.</span><span class="sxs-lookup"><span data-stu-id="2cd9d-108">Passing this value to [**ActivateAudioInterfaceAsync**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync) activates the requested interface on the default audio capture device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2cd9d-109"><span id="DEVINTERFACE_AUDIO_RENDER"></span><span id="devinterface_audio_render"></span>**\_rendering audio \_ DEVINTERFACE**</span><span class="sxs-lookup"><span data-stu-id="2cd9d-109"><span id="DEVINTERFACE_AUDIO_RENDER"></span><span id="devinterface_audio_render"></span>**DEVINTERFACE\_AUDIO\_RENDER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2cd9d-110">Specifica la stringa di query utilizzata per enumerare tutti i dispositivi di rendering audio nel sistema.</span><span class="sxs-lookup"><span data-stu-id="2cd9d-110">Specifies the query string used to enumerate all audio render devices on the system.</span></span> <span data-ttu-id="2cd9d-111">Questo valore viene restituito da [**MediaDevice:: GetAudioRenderSelector**](/uwp/api/windows.media.devices.mediadevice.getaudiorenderselector).</span><span class="sxs-lookup"><span data-stu-id="2cd9d-111">This value is returned by [**MediaDevice::GetAudioRenderSelector**](/uwp/api/windows.media.devices.mediadevice.getaudiorenderselector).</span></span>

<span data-ttu-id="2cd9d-112">Il passaggio di questo valore a [**ActivateAudioInterfaceAsync**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync) attiva l'interfaccia richiesta sul dispositivo di rendering audio predefinito.</span><span class="sxs-lookup"><span data-stu-id="2cd9d-112">Passing this value to [**ActivateAudioInterfaceAsync**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync) activates the requested interface on the default audio render device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2cd9d-113"><span id="DEVINTERFACE_MIDI_INPUT"></span><span id="devinterface_midi_input"></span>**\_input MIDI \_ DEVINTERFACE**</span><span class="sxs-lookup"><span data-stu-id="2cd9d-113"><span id="DEVINTERFACE_MIDI_INPUT"></span><span id="devinterface_midi_input"></span>**DEVINTERFACE\_MIDI\_INPUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2cd9d-114">Specifica la stringa di query utilizzata per enumerare tutti gli oggetti [**MidiInPort**](/uwp/api/Windows.Devices.Midi.MidiInPort) nel sistema.</span><span class="sxs-lookup"><span data-stu-id="2cd9d-114">Specifies the query string used to enumerate all [**MidiInPort**](/uwp/api/Windows.Devices.Midi.MidiInPort) objects on the system.</span></span> <span data-ttu-id="2cd9d-115">Questo valore viene restituito da [**MidiInPort:: GetDeviceSelector**](/uwp/api/windows.devices.midi.midiinport.getdeviceselector).</span><span class="sxs-lookup"><span data-stu-id="2cd9d-115">This value is returned by [**MidiInPort::GetDeviceSelector**](/uwp/api/windows.devices.midi.midiinport.getdeviceselector).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2cd9d-116"><span id="DEVINTERFACE_MIDI_OUTPUT"></span><span id="devinterface_midi_output"></span>**\_output MIDI \_ DEVINTERFACE**</span><span class="sxs-lookup"><span data-stu-id="2cd9d-116"><span id="DEVINTERFACE_MIDI_OUTPUT"></span><span id="devinterface_midi_output"></span>**DEVINTERFACE\_MIDI\_OUTPUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="2cd9d-117">Specifica la stringa di query utilizzata per enumerare tutti gli oggetti [**MidiOutPort**](/uwp/api/Windows.Devices.Midi.MidiOutPort) nel sistema.</span><span class="sxs-lookup"><span data-stu-id="2cd9d-117">Specifies the query string used to enumerate all [**MidiOutPort**](/uwp/api/Windows.Devices.Midi.MidiOutPort) objects on the system.</span></span> <span data-ttu-id="2cd9d-118">Questo valore viene restituito da [**MidiOutPort:: GetDeviceSelector**](/uwp/api/windows.devices.midi.midioutport.getdeviceselector).</span><span class="sxs-lookup"><span data-stu-id="2cd9d-118">This value is returned by [**MidiOutPort::GetDeviceSelector**](/uwp/api/windows.devices.midi.midioutport.getdeviceselector).</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2cd9d-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2cd9d-119">Requirements</span></span>



| <span data-ttu-id="2cd9d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="2cd9d-120">Requirement</span></span> | <span data-ttu-id="2cd9d-121">Valore</span><span class="sxs-lookup"><span data-stu-id="2cd9d-121">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2cd9d-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2cd9d-122">Header</span></span><br/> | <dl> <span data-ttu-id="2cd9d-123"><dt>Mmdeviceapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="2cd9d-123"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



 

