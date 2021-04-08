---
description: API EndpointVolume
ms.assetid: 1fe1cd57-a0a4-4e08-ab52-3b6e66d14e79
title: API EndpointVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 081b827045250336aa499e386a8dafedb6ae068b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748551"
---
# <a name="endpointvolume-api"></a>API EndpointVolume

L'API EndpointVolume consente ai client specializzati di controllare e monitorare i livelli di volume dei [dispositivi dell'endpoint audio](audio-endpoint-devices.md). Un client ottiene i riferimenti alle interfacce nell'API EndpointVolume ottenendo l'interfaccia [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) di un dispositivo dell'endpoint audio e chiamando il metodo [**IMMDevice:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) .

Il file di intestazione Endpointvolume. h definisce le interfacce nell'API EndpointVolume.

Le applicazioni audio che usano l' [API MMDevice](mmdevice-api.md) e [WASAPI](wasapi.md) in genere usano l'interfaccia [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) per controllare i livelli di volume per ogni singola sessione. Solo due tipi di applicazioni audio richiedono l'uso dell'API EndpointVolume. Questi tipi di applicazioni sono:

-   Applicazioni che gestiscono i livelli di volume master dei dispositivi dell'endpoint audio, in modo analogo al programma di controllo del volume di Windows, Sndvol.exe.
-   Applicazioni audio professionali ("Audio Pro") che richiedono l'accesso in modalità esclusiva ai dispositivi dell'endpoint audio.

L'uso inappropriato dell'API EndpointVolume può interferire con i criteri audio di Windows e interrompere le impostazioni del volume di sistema dell'utente.

Se un dispositivo endpoint audio implementa il volume hardware e i controlli di silenziamento, l'API EndpointVolume usa tali controlli per gestire il volume del dispositivo. In caso contrario, l'API EndpointVolume implementa i controlli nel software, in modo trasparente per il client.

Se un dispositivo dispone di controlli di volume e silenziamento hardware, le modifiche apportate alle impostazioni volume e mute del dispositivo tramite l'API EndpointVolume influiscono sul livello del volume sia in modalità condivisa che in modalità esclusiva. Se un dispositivo non dispone di controlli di volume e silenziamento hardware, le modifiche apportate al volume software e ai controlli di silenziamento tramite l'API EndpointVolume influiscono sul livello del volume in modalità condivisa, ma non in modalità esclusiva. In modalità esclusiva, il client e il dispositivo scambiano direttamente i dati audio, ignorando i controlli software.

Per le applicazioni che devono gestire il volume hardware e i controlli di silenziamento, l'API di EndpointVolume offre due potenziali vantaggi rispetto all' [API DeviceTopology](devicetopology-api.md).

In primo luogo, un numero di dispositivi scheda audio non dispone di controlli volume hardware. Se un dispositivo non dispone di un controllo volume hardware, l'interfaccia [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) nell'API EndpointVolume implementa automaticamente un controllo volume software nel flusso da o verso tale dispositivo. Per un client dell'API EndpointVolume, il risultato è lo stesso se il controllo del volume viene implementato nell'hardware dal dispositivo o nel software dall'interfaccia API EndpointVolume.

In secondo luogo, anche se il dispositivo adapter implementa i controlli volume hardware, un'applicazione che usa l'API DeviceTopology per implementare un algoritmo di attraversamento della topologia potrebbe non riuscire a trovare il controllo che sta cercando. In genere, un'applicazione di questo tipo è progettata per attraversare la topologia hardware di un determinato dispositivo o set di dispositivi correlati. L'applicazione rischia di non riuscire se tenta di attraversare la topologia di un dispositivo per cui non è stato progettato o testato appositamente.

Solo le applicazioni specializzate che devono accedere a funzioni hardware diverse dai controlli volume e mute richiedono l'uso dell'API DeviceTopology. Per le applicazioni che richiedono il controllo solo del livello di volume di un flusso in modalità esclusiva, l'API EndpointVolume è più semplice da usare e funziona in modo affidabile con una gamma più ampia di dispositivi hardware audio.

Per esempi di codice che usano le interfacce nell'API EndpointVolume, vedere gli argomenti seguenti:

-   [Controlli volume endpoint](endpoint-volume-controls.md)
-   [Contatori di picco](peak-meters.md)

Per vedere un esempio che usa l'API EndpointVolume, vedere [EndpointVolume](endpointvolume.md) nel Windows SDK.

L'API EndpointVolume implementa le interfacce seguenti.



| Interfaccia                                                | Descrizione                                                                             |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume)     | Rappresenta i controlli del volume nel flusso audio da o verso un dispositivo endpoint audio. |
| [**IAudioMeterInformation**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudiometerinformation) | Rappresenta un indicatore di picco nel flusso audio da o verso un dispositivo endpoint audio.        |



 

Inoltre, i client dell'API EndpointVolume che richiedono la notifica delle modifiche del volume e del muting nei dispositivi dell'endpoint audio devono implementare la seguente interfaccia.



| Interfaccia                                                            | Descrizione                                                                                       |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) | Fornisce notifiche in caso di modifica del livello di volume o di muting di un dispositivo dell'endpoint audio. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Controlli del volume](volume-controls.md)
</dt> <dt>

[**Interfaccia IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice)
</dt> <dt>

[**IMMDevice:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate)
</dt> <dt>

[**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume)
</dt> <dt>

[**Guida di riferimento alla programmazione**](programming-reference.md)
</dt> </dl>

 

 



