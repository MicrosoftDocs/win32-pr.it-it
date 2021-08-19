---
description: EndpointVolume API
ms.assetid: 1fe1cd57-a0a4-4e08-ab52-3b6e66d14e79
title: EndpointVolume API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22965e882a2f7d413ae58690fc9bc5f8134aba0e7b26838ca38c74d7f0093c98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018449"
---
# <a name="endpointvolume-api"></a>EndpointVolume API

L'API EndpointVolume consente ai client specializzati di controllare e monitorare i livelli di volume dei [dispositivi endpoint audio.](audio-endpoint-devices.md) Un client ottiene riferimenti alle interfacce nell'API EndpointVolume ottenendo [**l'interfaccia IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) di un dispositivo endpoint audio e chiamando il [**metodo IMMDevice::Activate.**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate)

Il file di intestazione Endpointvolume.h definisce le interfacce nell'API EndpointVolume.

Le applicazioni audio che usano [l'API MMDevice](mmdevice-api.md) e [WASAPI](wasapi.md) in genere usano l'interfaccia [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) per controllare i livelli di volume per sessione. Solo due tipi di applicazioni audio richiedono l'uso dell'API EndpointVolume. Questi tipi di applicazione sono:

-   Applicazioni che gestiscono i livelli di volume master dei dispositivi endpoint audio, in modo simile al programma Windows di controllo del volume, Sndvol.exe.
-   Professional applicazioni audio ("pro audio") che richiedono l'accesso in modalità esclusiva ai dispositivi endpoint audio.

L'uso non appropriato dell'API EndpointVolume può interferire con Windows audio e interrompere le impostazioni del volume di sistema dell'utente.

Se un dispositivo endpoint audio implementa i controlli del volume hardware e dell'audio, l'API EndpointVolume usa tali controlli per gestire il volume del dispositivo. In caso contrario, l'API EndpointVolume implementa i controlli nel software, in modo trasparente per il client.

Se un dispositivo dispone di controlli del volume e dell'audio hardware, le modifiche apportate alle impostazioni del volume e dell'audio del dispositivo tramite l'API EndpointVolume influiscono sul livello del volume sia in modalità condivisa che in modalità esclusiva. Se un dispositivo non dispone di controlli del volume hardware e dell'audio, le modifiche apportate al volume software e i controlli di disattivazione dell'audio tramite l'API EndpointVolume influiscono sul livello del volume in modalità condivisa, ma non in modalità esclusiva. In modalità esclusiva, il client e il dispositivo scambiano direttamente i dati audio, ignorando i controlli software.

Per le applicazioni che devono gestire i controlli del volume hardware e dell'audio, l'API EndpointVolume offre due potenziali vantaggi rispetto [all'API DeviceTopology](devicetopology-api.md).

In primo luogo, un certo numero di dispositivi scheda audio non dispone di controlli del volume hardware. Se un dispositivo non dispone di un controllo del volume hardware, l'interfaccia [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) nell'API EndpointVolume implementa automaticamente un controllo del volume software nel flusso verso o da tale dispositivo. Per un client dell'API EndpointVolume, il risultato è lo stesso se il controllo del volume viene implementato nell'hardware dal dispositivo o nel software dall'interfaccia API EndpointVolume.

In secondo momento, anche se il dispositivo adapter implementa i controlli del volume hardware, un'applicazione che usa l'API DeviceTopology per implementare un algoritmo di attraversamento della topologia potrebbe non riuscire a trovare il controllo che sta cercando. In genere, un'applicazione di questo tipo è progettata per attraversare la topologia hardware di un determinato dispositivo o set di dispositivi correlati. L'applicazione rischia di avere esito negativo se tenta di attraversare la topologia di un dispositivo per cui non è stata specificatamente progettata o testata.

Solo le applicazioni specializzate che devono accedere a funzioni hardware diverse da controlli volume e mute richiedono l'uso dell'API DeviceTopology. Per le applicazioni che richiedono il controllo solo del livello di volume di un flusso in modalità esclusiva, l'API EndpointVolume è più semplice da usare e funziona in modo affidabile con una gamma più ampia di dispositivi hardware audio.

Per esempi di codice che usano le interfacce nell'API EndpointVolume, vedere gli argomenti seguenti:

-   [Controlli del volume dell'endpoint](endpoint-volume-controls.md)
-   [Metri di picco](peak-meters.md)

Per un esempio che usa l'API EndpointVolume, vedere [EndpointVolume](endpointvolume.md) in Windows SDK.

L'API EndpointVolume implementa le interfacce seguenti.



| Interfaccia                                                | Descrizione                                                                             |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume)     | Rappresenta i controlli del volume nel flusso audio da o verso un dispositivo endpoint audio. |
| [**IAudioMeterInformation**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) | Rappresenta un contatore di picco nel flusso audio da o verso un dispositivo endpoint audio.        |



 

Inoltre, i client dell'API EndpointVolume che richiedono la notifica del volume e la modifica delle modifiche nei dispositivi endpoint audio devono implementare l'interfaccia seguente.



| Interfaccia                                                            | Descrizione                                                                                       |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) | Fornisce notifiche quando il livello del volume o lo stato di disattivazione di un dispositivo endpoint audio cambia. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Controlli del volume](volume-controls.md)
</dt> <dt>

[**Interfaccia IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice)
</dt> <dt>

[**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate)
</dt> <dt>

[**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume)
</dt> <dt>

[**Guida di riferimento alla programmazione**](programming-reference.md)
</dt> </dl>

 

 



