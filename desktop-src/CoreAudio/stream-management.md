---
description: Gestione dei flussi
ms.assetid: 936d8d69-e86c-418b-b5b0-c4fbbfa1dd49
title: Gestione dei flussi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 669e3be8af4532f9045c08f07400d47c423d507d4e11da4ada0b1a279c52772d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077435"
---
# <a name="stream-management"></a>Gestione dei flussi

Dopo aver enumerato i dispositivi [endpoint audio](audio-endpoint-devices.md) nel sistema e aver identificato un dispositivo di rendering o acquisizione appropriato, l'attività successiva per un'applicazione client audio è aprire una connessione con il dispositivo endpoint e gestire il flusso di dati audio su tale connessione. [WASAPI](wasapi.md) consente ai client di creare e gestire flussi audio.

WASAPI implementa diverse interfacce per fornire servizi di gestione del flusso ai client audio. L'interfaccia primaria è [**IAudioClient.**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) Un client ottiene **l'interfaccia IAudioClient** per un dispositivo endpoint audio chiamando il metodo [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) (con il parametro *iid* impostato su **REFIID** \_ IID IAudioClient) nell'oggetto endpoint.

Il client chiama i metodi [**nell'interfaccia IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) per eseguire le operazioni seguenti:

-   Individuare i formati audio supportati dal dispositivo endpoint.
-   Ottenere le dimensioni del buffer dell'endpoint.
-   Ottenere il formato e la latenza del flusso.
-   Avviare, arrestare e reimpostare il flusso che passa attraverso il dispositivo endpoint.
-   Accedere ad altri servizi audio.

Per creare un flusso, un client chiama il [**metodo IAudioClient::Initialize.**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) Tramite questo metodo, il client specifica il formato dei dati per il flusso, le dimensioni del buffer dell'endpoint e se il flusso opera in modalità condivisa o esclusiva.

I metodi rimanenti [**nell'interfaccia IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) rientrano in due gruppi:

-   Metodi che possono essere chiamati solo dopo l'apertura del flusso [**da parte di IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize).
-   Metodi che possono essere chiamati in qualsiasi momento prima o dopo la [**chiamata Initialize.**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize)

I metodi seguenti possono essere chiamati solo dopo la chiamata a [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize):

-   [**IAudioClient::GetBufferSize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getbuffersize)
-   [**IAudioClient::GetCurrentPadding**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getcurrentpadding)
-   [**IAudioClient::GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice)
-   [**IAudioClient::GetStreamLatency**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getstreamlatency)
-   [**IAudioClient::Reset**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-reset)
-   [**IAudioClient::Start**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-start)
-   [**IAudioClient::Stop**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-stop)

I metodi seguenti possono essere chiamati prima o dopo la chiamata [**IAudioClient::Initialize:**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize)

-   [**IAudioClient::GetDevicePeriod**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getdeviceperiod)
-   [**IAudioClient::GetMixFormat**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getmixformat)
-   [**IAudioClient::IsFormatSupported**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-isformatsupported)

Per accedere ai servizi client audio aggiuntivi, il client chiama il [**metodo IAudioClient::GetService.**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) Tramite questo metodo, il client può ottenere riferimenti alle interfacce seguenti:

-   [**IAudioRenderClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiorenderclient)

    Scrive i dati di rendering in un buffer dell'endpoint di rendering audio.

-   [**IAudioCaptureClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient)

    Legge i dati acquisiti da un buffer dell'endpoint di acquisizione audio.

-   [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol)

    Comunica con il gestore della sessione audio per configurare e gestire la sessione audio associata al flusso.

-   [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume)

    Controlla il livello di volume della sessione audio associata al flusso.

-   [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)

    Controlla i livelli di volume dei singoli canali nella sessione audio associata al flusso.

-   [**IAudioClock**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclock)

    Monitora la velocità dei dati del flusso e la posizione del flusso.

Inoltre, i client WASAPI che richiedono la notifica di eventi correlati alla sessione devono implementare l'interfaccia seguente:

-   [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents)

    Per ricevere notifiche degli eventi, il client passa un puntatore alla relativa interfaccia [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) al metodo [**IAudioSessionControl::RegisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) come parametro di chiamata.

Infine, un client potrebbe usare un'API di livello superiore per creare un flusso audio, ma anche richiedere l'accesso ai controlli sessione e ai controlli volume per la sessione che contiene il flusso. Un'API di livello superiore in genere non fornisce questo accesso. Il client può ottenere i controlli per una sessione specifica tramite [**l'interfaccia IAudioSessionManager.**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager) Questa interfaccia consente al client di ottenere le interfacce [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) e [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume) per una sessione senza richiedere al client di usare l'interfaccia [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) per creare un flusso e assegnare il flusso alla sessione. Un client ottiene **l'interfaccia IAudioSessionManager** per un dispositivo endpoint audio chiamando il metodo [**IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) (con il parametro *iid* impostato su **REFIID** \_ IID IAudioSessionManager) nell'oggetto endpoint.

Le [**interfacce IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol), [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents)e [**IAudioSessionManager**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager) sono definite nel file di intestazione Audiopolicy.h. Tutte le altre interfacce WASAPI sono definite nel file di intestazione Audioclient.h.

Le sezioni seguenti descrivono come usare WASAPI per gestire i flussi audio:

-   [Informazioni su WASAPI](wasapi.md)
-   [Rendering di un flusso](rendering-a-stream.md)
-   [Acquisizione di un flusso](capturing-a-stream.md)
-   [Registrazione loopback](loopback-recording.md)
-   [Modalità Flussi](exclusive-mode-streams.md)
-   [Ripristino da un errore Invalid-Device errore](recovering-from-an-invalid-device-error.md)
-   [Uso di un dispositivo di comunicazione](using-the-communication-device.md)
-   [Routing di flusso](stream-routing.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida per programmatori](programming-guide.md)
</dt> </dl>

 

 



