---
description: Informazioni su WASAPI
ms.assetid: 452b9725-b0b9-4888-bbb5-a23e0067e840
title: Informazioni su WASAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3effb34ec0cde0a53d0eb6f6e9718aa13fc308417b33427f168364afc32086ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088181"
---
# <a name="about-wasapi"></a>Informazioni su WASAPI

L Windows API (Audio Session API) consente alle applicazioni client di gestire il flusso di dati audio tra l'applicazione e un [dispositivo endpoint audio.](audio-endpoint-devices.md)

I file di intestazione Audioclient.h e Audiopolicy.h definiscono le interfacce WASAPI.

Ogni flusso audio è membro di una [sessione audio.](audio-sessions.md) Tramite l'astrazione della sessione, un client WASAPI può identificare un flusso audio come membro di un gruppo di flussi audio correlati. Il sistema può gestire tutti i flussi nella sessione come singola unità.

Il motore audio è il componente [audio in modalità utente tramite](user-mode-audio-components.md) il quale le applicazioni condividono l'accesso a un dispositivo endpoint audio. Il motore audio trasporta i dati audio tra un buffer endpoint e un dispositivo endpoint. Per riprodurre un flusso audio tramite un dispositivo endpoint di rendering, un'applicazione scrive periodicamente i dati audio in un buffer dell'endpoint di rendering. Il motore audio combina i flussi delle varie applicazioni. Per registrare un flusso audio da un dispositivo endpoint di acquisizione, un'applicazione legge periodicamente i dati audio da un buffer dell'endpoint di acquisizione.

WASAPI è costituito da diverse interfacce. Il primo di questi è [**l'interfaccia IAudioClient.**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) Per accedere alle interfacce WASAPI, un client ottiene innanzitutto un riferimento all'interfaccia **IAudioClient** di un dispositivo endpoint audio chiamando il [**metodo IMMDevice::Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) con il parametro *iid* impostato su **REFIID** \_ IID IAudioClient. Il client chiama il [**metodo IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) per inizializzare un flusso in un dispositivo endpoint. Dopo l'inizializzazione di un flusso, il client può ottenere riferimenti alle altre interfacce WASAPI chiamando il [**metodo IAudioClient::GetService.**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice)

Molti dei metodi in WASAPI restituiscono il codice di errore AUDCLNT E DEVICE INVALIDATED se il dispositivo endpoint audio utilizzato da un'applicazione \_ client non è più \_ \_ valido. Spesso l'applicazione può eseguire il ripristino da questo errore. Per altre informazioni, vedere [Recovering from an Invalid-Device Error](recovering-from-an-invalid-device-error.md).

WASAPI implementa le interfacce seguenti.



| Interfaccia                                            | Descrizione                                                                                                                                                     |
|------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IAudioCaptureClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient)   | Consente a un client di leggere i dati di input da un buffer dell'endpoint di acquisizione.                                                                                             |
| [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient)                 | Consente a un client di creare e inizializzare un flusso audio tra un'applicazione audio e il motore audio o il buffer hardware di un dispositivo endpoint audio. |
| [**IAudioClock**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclock)                   | Consente a un client di monitorare la velocità dei dati di un flusso e la posizione corrente nel flusso.                                                                        |
| [**IAudioRenderClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiorenderclient)     | Consente a un client di scrivere dati di output in un buffer dell'endpoint di rendering.                                                                                           |
| [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) | Consente a un client di configurare i parametri di controllo per una sessione audio e di monitorare gli eventi nella sessione.                                                 |
| [**IAudioSessionManager**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager) | Consente a un client di accedere ai controlli sessione e ai controlli volume sia per sessioni audio tra processi che per sessioni audio specifiche del processo.                                 |
| [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume)     | Consente a un client di controllare e monitorare i livelli di volume per tutti i canali in un flusso audio.                                                           |
| [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)   | Consente a un client di controllare i livelli di volume per tutti i canali nella sessione audio a cui appartiene il flusso.                                          |
| [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume)     | Consente a un client di controllare il livello del volume master di una sessione audio.                                                                                        |



 

I client WASAPI che richiedono la notifica degli eventi correlati alla sessione devono implementare l'interfaccia seguente.



| Interfaccia                                          | Descrizione                                                                                                            |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) | Fornisce notifiche di eventi correlati alla sessione, ad esempio modifiche al livello del volume, al nome visualizzato e allo stato della sessione. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione dei flussi](stream-management.md)
</dt> <dt>

[**Guida di riferimento alla programmazione**](programming-reference.md)
</dt> </dl>

 

 



