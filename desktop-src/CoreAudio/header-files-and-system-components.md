---
description: File di intestazione e componenti di sistema
ms.assetid: de2776be-72e6-4391-8e6c-56694d683d57
title: File di intestazione e componenti di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77a47125853b51a71f2f05dacf4534ce33cfedec
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424291"
---
# <a name="header-files-and-system-components"></a>File di intestazione e componenti di sistema

Nella tabella seguente sono elencati i file di intestazione che contengono le definizioni di interfaccia per i quattro componenti Core Audio.



| Componente core audio                         | File di intestazione                  |
|----------------------------------------------|------------------------------|
| [MMDevice API](mmdevice-api.md)             | Mmdeviceapi.h                |
| [Wasapi](wasapi.md)                         | Audioclient.h, Audiopolicy.h |
| [DeviceTopology API](devicetopology-api.md) | Devicetopology.h             |
| [EndpointVolume API](endpointvolume-api.md) | Endpointvolume.h             |



 

Un altro file di intestazione, Audiosessiontypes.h, definisce le costanti usate da WASAPI. Questi file di intestazione si trovano nella directory %MSSdk%, dove \\ %MSSdk% è la directory radice dell Windows SDK installazione nel computer.

Ogni API nella tabella precedente è costituita da un set di interfacce COM correlate. Poiché alcuni aspetti dello streaming audio dipendono dalla bassa latenza e dalla sincronizzazione precisa, le implementazioni delle API MMDevice, WASAPI, DeviceTopology ed EndpointVolume non usano Microsoft .NET Framework o l'ambiente di esecuzione gestita.

Le API audio di base vengono implementate nei componenti di sistema in modalità utente Audioses.dll e Mmdevapi.dll. Le applicazioni client non accedono direttamente ai punti di ingresso in queste DLL. I client chiamano invece la **funzione CoCreateInstance** o **CoCreateInstanceEx** per ottenere l'interfaccia [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) dell'oggetto classe MMDeviceEnumerator. Questo oggetto enumera i [dispositivi endpoint audio](audio-endpoint-devices.md) nel sistema. **L'interfaccia IMMDeviceEnumerator** fa parte dell'API MMDevice. Da questa interfaccia, i client possono ottenere direttamente o indirettamente le altre interfacce nell'API MMDevice, inclusa [**l'interfaccia IMMDevice.**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) **IMMDevice rappresenta** un dispositivo endpoint audio specifico. Tramite **IMMDevice,** i client possono ottenere direttamente o indirettamente le interfacce specifiche del dispositivo in WASAPI, nell'API DeviceTopology e nell'API EndpointVolume. Per altre informazioni su **CoCreateInstance** e **CoCreateInstanceEx,** vedere la documentazione Windows SDK. Per altre informazioni sull'accesso alle interfacce nelle API audio di base, vedere [Enumerazione dei dispositivi audio.](enumerating-audio-devices.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sulle API audio di Windows Core](about-the-windows-core-audio-apis.md)
</dt> </dl>

 

 



