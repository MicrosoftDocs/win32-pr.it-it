---
description: File di intestazione e componenti di sistema
ms.assetid: de2776be-72e6-4391-8e6c-56694d683d57
title: File di intestazione e componenti di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47c4b93c63e7d32944dfdf2bf6872bd3a3153e4a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127439"
---
# <a name="header-files-and-system-components"></a>File di intestazione e componenti di sistema

Nella tabella seguente sono elencati i file di intestazione che contengono le definizioni di interfaccia per i quattro componenti audio principali.



|                                              |                              |
|----------------------------------------------|------------------------------|
| Componente audio principale                         | File di intestazione                  |
| [API MMDevice](mmdevice-api.md)             | Mmdeviceapi. h                |
| [WASAPI](wasapi.md)                         | Audioclient. h, Audiopolicy. h |
| [API DeviceTopology](devicetopology-api.md) | Devicetopology. h             |
| [API EndpointVolume](endpointvolume-api.md) | Endpointvolume. h             |



 

Un altro file di intestazione, Audiosessiontypes. h, definisce le costanti usate da WASAPI. Questi file di intestazione si trovano nella directory% MSSdk% \\ include, dove% MSSdk% è la directory radice dell'installazione del Windows SDK nel computer.

Ogni API nella tabella precedente è costituita da un set di interfacce COM correlate. Poiché alcuni aspetti del flusso audio dipendono dalla bassa latenza e dalla sincronizzazione precisa, le implementazioni delle API MMDevice, WASAPI, DeviceTopology e EndpointVolume non utilizzano il Framework Microsoft .NET o l'ambiente di esecuzione gestita.

Le API audio principali vengono implementate nei componenti di sistema in modalità utente Audioses.dll e Mmdevapi.dll. Le applicazioni client non accedono direttamente ai punti di ingresso di queste dll. Al contrario, i client chiamano la funzione **CoCreateInstance** o **CoCreateInstanceEx** per ottenere l'interfaccia [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) dell'oggetto della classe MMDeviceEnumerator. Questo oggetto enumera i [dispositivi dell'endpoint audio](audio-endpoint-devices.md) nel sistema. L'interfaccia **IMMDeviceEnumerator** fa parte dell'API MMDevice. Da questa interfaccia, i client possono ottenere direttamente o indirettamente le altre interfacce nell'API MMDevice, inclusa l'interfaccia [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) . **IMMDevice** rappresenta un dispositivo dell'endpoint audio specifico. Tramite **IMMDevice**, i client possono ottenere direttamente o indirettamente le interfacce specifiche del dispositivo in WASAPI, l'API DeviceTopology e l'API EndpointVolume. Per ulteriori informazioni su **CoCreateInstance** e **CoCreateInstanceEx**, vedere la documentazione Windows SDK. Per altre informazioni sull'accesso alle interfacce nelle API principali dell'audio, vedere [enumerazione dei dispositivi audio](enumerating-audio-devices.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sulle API audio di Windows Core](about-the-windows-core-audio-apis.md)
</dt> </dl>

 

 



