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
# <a name="devinterface_xxx-guids"></a>\_GUID DEVINTERFACE xxx

I \_ GUID DEVINTERFACE xxx vengono usati per rappresentare i GUID per le interfacce del dispositivo.

<dl> <dt>

<span id="DEVINTERFACE_AUDIO_CAPTURE"></span><span id="devinterface_audio_capture"></span>**\_acquisizione audio \_ DEVINTERFACE**
</dt> <dd> <dl> <dt>



Specifica la stringa di query utilizzata per enumerare tutti i dispositivi di acquisizione audio nel sistema. Questo valore viene restituito da [**MediaDevice:: GetAudioCaptureSelector**](/uwp/api/windows.media.devices.mediadevice.getaudiocaptureselector).

Il passaggio di questo valore a [**ActivateAudioInterfaceAsync**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync) attiva l'interfaccia richiesta sul dispositivo di acquisizione audio predefinito.


</dt> </dl> </dd> <dt>

<span id="DEVINTERFACE_AUDIO_RENDER"></span><span id="devinterface_audio_render"></span>**\_rendering audio \_ DEVINTERFACE**
</dt> <dd> <dl> <dt>



Specifica la stringa di query utilizzata per enumerare tutti i dispositivi di rendering audio nel sistema. Questo valore viene restituito da [**MediaDevice:: GetAudioRenderSelector**](/uwp/api/windows.media.devices.mediadevice.getaudiorenderselector).

Il passaggio di questo valore a [**ActivateAudioInterfaceAsync**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync) attiva l'interfaccia richiesta sul dispositivo di rendering audio predefinito.


</dt> </dl> </dd> <dt>

<span id="DEVINTERFACE_MIDI_INPUT"></span><span id="devinterface_midi_input"></span>**\_input MIDI \_ DEVINTERFACE**
</dt> <dd> <dl> <dt>



Specifica la stringa di query utilizzata per enumerare tutti gli oggetti [**MidiInPort**](/uwp/api/Windows.Devices.Midi.MidiInPort) nel sistema. Questo valore viene restituito da [**MidiInPort:: GetDeviceSelector**](/uwp/api/windows.devices.midi.midiinport.getdeviceselector).


</dt> </dl> </dd> <dt>

<span id="DEVINTERFACE_MIDI_OUTPUT"></span><span id="devinterface_midi_output"></span>**\_output MIDI \_ DEVINTERFACE**
</dt> <dd> <dl> <dt>



Specifica la stringa di query utilizzata per enumerare tutti gli oggetti [**MidiOutPort**](/uwp/api/Windows.Devices.Midi.MidiOutPort) nel sistema. Questo valore viene restituito da [**MidiOutPort:: GetDeviceSelector**](/uwp/api/windows.devices.midi.midioutport.getdeviceselector).


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Mmdeviceapi. h</dt> </dl> |



 

