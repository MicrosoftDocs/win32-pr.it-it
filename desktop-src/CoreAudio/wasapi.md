---
description: Informazioni su WASAPI
ms.assetid: 452b9725-b0b9-4888-bbb5-a23e0067e840
title: Informazioni su WASAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f869319f3100b797e58c7b43597869c9767ac037
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966174"
---
# <a name="about-wasapi"></a>Informazioni su WASAPI

L'API di sessione audio (WASAPI) di Windows consente alle applicazioni client di gestire il flusso di dati audio tra l'applicazione e un [dispositivo dell'endpoint audio](audio-endpoint-devices.md).

I file di intestazione Audioclient. h e Audiopolicy. h definiscono le interfacce WASAPI.

Ogni flusso audio è un membro di una [sessione audio](audio-sessions.md). Tramite l'astrazione della sessione, un client WASAPI può identificare un flusso audio come membro di un gruppo di flussi audio correlati. Il sistema è in grado di gestire tutti i flussi nella sessione come una singola unità.

Il motore audio è il [componente audio in modalità utente](user-mode-audio-components.md) tramite il quale le applicazioni condividono l'accesso a un dispositivo endpoint audio. Il motore audio trasporta i dati audio tra un buffer dell'endpoint e un dispositivo endpoint. Per riprodurre un flusso audio tramite un dispositivo endpoint di rendering, un'applicazione scrive periodicamente i dati audio in un buffer dell'endpoint di rendering. Il motore audio combina i flussi delle diverse applicazioni. Per registrare un flusso audio da un dispositivo dell'endpoint di acquisizione, un'applicazione legge periodicamente i dati audio da un buffer dell'endpoint di acquisizione.

WASAPI è costituito da diverse interfacce. Il primo è l'interfaccia [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) . Per accedere alle interfacce WASAPI, un client ottiene innanzitutto un riferimento all'interfaccia **IAudioClient** di un dispositivo endpoint audio chiamando il metodo [**IMMDevice:: Activate**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-activate) con il parametro *IID* impostato su **REFIID** IID \_ IAudioClient. Il client chiama il metodo [**IAudioClient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) per inizializzare un flusso in un dispositivo endpoint. Dopo l'inizializzazione di un flusso, il client può ottenere riferimenti alle altre interfacce WASAPI chiamando il metodo [**IAudioClient:: GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) .

Molti dei metodi in WASAPI restituiscono il codice di errore AUDCLNT \_ E \_ dispositivo \_ invalidato se il dispositivo dell'endpoint audio che un'applicazione client sta usando diventa non valido. Spesso l'applicazione può risolvere questo errore. Per ulteriori informazioni, vedere il [ripristino da un errore di Invalid-Device](recovering-from-an-invalid-device-error.md).

WASAPI implementa le interfacce seguenti.



| Interfaccia                                            | Descrizione                                                                                                                                                     |
|------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IAudioCaptureClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient)   | Consente a un client di leggere i dati di input da un buffer dell'endpoint di acquisizione.                                                                                             |
| [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient)                 | Consente a un client di creare e inizializzare un flusso audio tra un'applicazione audio e il motore audio o il buffer hardware di un dispositivo endpoint audio. |
| [**IAudioClock**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclock)                   | Consente a un client di monitorare la velocità dei dati di un flusso e la posizione corrente nel flusso.                                                                        |
| [**IAudioRenderClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiorenderclient)     | Consente a un client di scrivere i dati di output in un buffer dell'endpoint di rendering.                                                                                           |
| [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) | Consente a un client di configurare i parametri di controllo per una sessione audio e di monitorare gli eventi nella sessione.                                                 |
| [**IAudioSessionManager**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager) | Consente a un client di accedere ai controlli di sessione e ai controlli volume per le sessioni audio sia tra processi che specifiche del processo.                                 |
| [**IAudioStreamVolume**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiostreamvolume)     | Consente a un client di controllare e monitorare i livelli di volume per tutti i canali in un flusso audio.                                                           |
| [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume)   | Consente a un client di controllare i livelli di volume per tutti i canali della sessione audio a cui appartiene il flusso.                                          |
| [**ISimpleAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-isimpleaudiovolume)     | Consente a un client di controllare il livello del volume master di una sessione audio.                                                                                        |



 

I client WASAPI che richiedono la notifica di eventi correlati alla sessione devono implementare la seguente interfaccia.



| Interfaccia                                          | Descrizione                                                                                                            |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) | Fornisce notifiche di eventi correlati alla sessione, ad esempio modifiche a livello di volume, nome visualizzato e stato sessione. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione dei flussi](stream-management.md)
</dt> <dt>

[**Guida di riferimento alla programmazione**](programming-reference.md)
</dt> </dl>

 

 



