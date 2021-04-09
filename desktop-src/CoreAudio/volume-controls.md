---
description: Controlli del volume
ms.assetid: b1799372-8d2c-4774-995d-e7926a159d0a
title: Controlli del volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 758fd25d4157030071a47ac8eec26dc0e4d50e4c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877933"
---
# <a name="volume-controls"></a>Controlli del volume

I client che gestiscono flussi in modalità condivisa usano in genere le interfacce [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) e [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) in [WASAPI](wasapi.md) per controllare e monitorare i livelli del volume del flusso. Tramite i metodi dell'interfaccia **ISimpleAudioVolume** , il client può ottenere e impostare i livelli di volume delle [sessioni audio](audio-sessions.md) a cui appartengono i flussi in modalità condivisa. Se sndvol o un'altra applicazione modifica il livello del volume di sessione, il client può ricevere una notifica della modifica tramite l'interfaccia **IAudioSessionEvents** .

I client che gestiscono flussi in modalità esclusiva usano in genere le interfacce [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) e [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) nell' [API EndpointVolume](endpointvolume-api.md) per controllare e monitorare i livelli del volume del flusso. Tramite i metodi dell'interfaccia **IAudioEndpointVolume** , il client può ottenere e impostare il livello di volume di un [dispositivo dell'endpoint audio](audio-endpoint-devices.md). Se sndvol o un'altra applicazione modifica il livello del volume del dispositivo endpoint, il client può ricevere una notifica della modifica tramite l'interfaccia **IAudioEndpointVolumeCallback** .

Come illustrato nelle [sessioni audio](audio-sessions.md), sndvol è il programma di controllo del volume di sistema. Visualizza i controlli volume per i dispositivi endpoint di rendering audio nel sistema. Attualmente non vengono visualizzati i controlli volume per i dispositivi endpoint di acquisizione audio. Per visualizzare i controlli del volume per un particolare dispositivo, fare clic su **dispositivo** nella barra dei menu e selezionare un nome di dispositivo nell'elenco dei dispositivi disponibili.

La finestra sndvol separa i controlli volume per un dispositivo in due gruppi. La casella di gruppo sul lato sinistro della finestra è denominata **dispositivo**. La casella **dispositivo** contiene un singolo controllo volume controllato dall'interfaccia [**IAudioEndpointVolume**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolume) . Le modifiche apportate dall'utente a questo controllo volume possono essere monitorate tramite l'interfaccia [**IAudioEndpointVolumeCallback**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumecallback) .

La casella di gruppo sul lato destro della finestra sndvol è denominata **Applications (applicazioni**). Nella casella **applicazioni** sono contenuti i controlli del volume per le applicazioni che attualmente condividono il dispositivo. Per le applicazioni che usano il dispositivo in modalità condivisa, i controlli del volume rappresentano i livelli del volume controllati dall'interfaccia [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) . Le modifiche apportate dall'utente a questi controlli volume possono essere monitorate tramite l'interfaccia [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) .

Sebbene un'applicazione in modalità condivisa possa usare l'interfaccia [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) per monitorare le modifiche apportate dall'utente al controllo volume dell'applicazione nella casella **applicazioni** nella finestra sndvol, l'applicazione non è in grado di monitorare le modifiche apportate ai controlli volume di altre applicazioni non correlate. Analogamente, un'applicazione può modificare i livelli di volume delle sessioni audio tramite l'interfaccia [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) , ma non può modificare i livelli del volume delle sessioni che appartengono ad altre applicazioni non correlate.

Tuttavia, due o più applicazioni correlate (o istanze della stessa applicazione) possono condividere lo stesso controllo volume nella casella **applicazioni** della finestra sndvol assegnando i flussi audio alla stessa sessione tra processi o associando le rispettive sessioni con lo stesso parametro di raggruppamento. Per altre informazioni, vedere [sessioni audio](audio-sessions.md) e [parametri di raggruppamento](grouping-parameters.md).

WASAPI fornisce due interfacce aggiuntive, [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume) e [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume), per controllare i livelli di volume dei flussi in modalità condivisa. Queste interfacce vengono utilizzate principalmente da client specializzati che richiedono il controllo sui livelli di volume dei singoli canali in una sessione o di singoli flussi in una sessione.

L' [API DeviceTopology](devicetopology-api.md) consente ai client di accedere ai controlli volume nelle topologie di schede audio. Tuttavia, i client che gestiscono flussi in modalità esclusiva usano in genere l'API EndpointVolume anziché l'API DeviceTopology per controllare i livelli del volume del flusso. L'API EndpointVolume semplifica il controllo del volume di un dispositivo endpoint in due modi. Prima di tutto, se un dispositivo endpoint implementa un controllo volume hardware, l'API DeviceTopology richiede che il client attraversi la topologia del dispositivo in ricerca del controllo hardware. Al contrario, l'API EndpointVolume trova automaticamente il controllo volume hardware per il client. In secondo luogo, se il dispositivo endpoint non implementa un controllo volume hardware, un client DeviceTopology deve implementare un controllo del volume nel software. Al contrario, l'API EndpointVolume sostituisce automaticamente un controllo volume software per il controllo hardware mancante.

Le sezioni seguenti descrivono i controlli volume per le sessioni audio e per i dispositivi endpoint audio:

-   [Controlli volume sessione](session-volume-controls.md)
-   [Controlli volume endpoint](endpoint-volume-controls.md)
-   [API EndpointVolume](endpointvolume-api.md)
-   [Controlli volume con rastremazione audio](audio-tapered-volume-controls.md)
-   [Contatori di picco](peak-meters.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida per programmatori](programming-guide.md)
</dt> </dl>

 

 



