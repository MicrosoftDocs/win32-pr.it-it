---
description: I GUID DEVINTERFACE \_ XXX vengono usati per rappresentare i GUID per le interfacce di dispositivo.
ms.assetid: 2503463B-D7C6-4C82-8421-424D79FD1C2A
title: DEVINTERFACE_XXX GUID (Mmdeviceapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cef6a105ed8e34519a2ca0a06d9d4f43a7aa91495fae9f54eedfa44d79b043c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118406794"
---
# <a name="devinterface_xxx-guids"></a>GUID DEVINTERFACE \_ XXX

I GUID DEVINTERFACE \_ XXX vengono usati per rappresentare i GUID per le interfacce di dispositivo.

<dl> <dt>

<span id="DEVINTERFACE_AUDIO_CAPTURE"></span><span id="devinterface_audio_capture"></span>**ACQUISIZIONE AUDIO DEVINTERFACE \_ \_**
</dt> <dd> <dl> <dt>



Specifica la stringa di query usata per enumerare tutti i dispositivi di acquisizione audio nel sistema. Questo valore viene restituito [**da MediaDevice::GetAudioCaptureSelector.**](/uwp/api/windows.media.devices.mediadevice.getaudiocaptureselector)

Il passaggio di questo valore [**ad ActivateAudioInterfaceAsync**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync) attiva l'interfaccia richiesta nel dispositivo di acquisizione audio predefinito.


</dt> </dl> </dd> <dt>

<span id="DEVINTERFACE_AUDIO_RENDER"></span><span id="devinterface_audio_render"></span>**RENDERING AUDIO DEVINTERFACE \_ \_**
</dt> <dd> <dl> <dt>



Specifica la stringa di query usata per enumerare tutti i dispositivi di rendering audio nel sistema. Questo valore viene restituito [**da MediaDevice::GetAudioRenderSelector.**](/uwp/api/windows.media.devices.mediadevice.getaudiorenderselector)

Il passaggio di questo valore [**ad ActivateAudioInterfaceAsync**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync) attiva l'interfaccia richiesta nel dispositivo di rendering audio predefinito.


</dt> </dl> </dd> <dt>

<span id="DEVINTERFACE_MIDI_INPUT"></span><span id="devinterface_midi_input"></span>**DEVINTERFACE \_ MIDI \_ INPUT**
</dt> <dd> <dl> <dt>



Specifica la stringa di query usata per enumerare tutti [**gli oggetti MidiInPort**](/uwp/api/Windows.Devices.Midi.MidiInPort) nel sistema. Questo valore viene restituito [**da MidiInPort::GetDeviceSelector**](/uwp/api/windows.devices.midi.midiinport.getdeviceselector).


</dt> </dl> </dd> <dt>

<span id="DEVINTERFACE_MIDI_OUTPUT"></span><span id="devinterface_midi_output"></span>**OUTPUT \_ MIDI DI DEVINTERFACE \_**
</dt> <dd> <dl> <dt>



Specifica la stringa di query usata per enumerare [**tutti gli oggetti MidiOutPort**](/uwp/api/Windows.Devices.Midi.MidiOutPort) nel sistema. Questo valore viene restituito [**da MidiOutPort::GetDeviceSelector**](/uwp/api/windows.devices.midi.midioutport.getdeviceselector).


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Mmdeviceapi.h</dt> </dl> |



 

