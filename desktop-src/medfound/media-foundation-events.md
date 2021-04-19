---
description: Eventi Media Foundation
ms.assetid: d925f63d-3359-4ba1-802f-0c2b11a3f973
title: Eventi Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a63beeb3222ffef4151f45be95d13f9cf9ff4f9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320503"
---
# <a name="media-foundation-events"></a>Eventi Media Foundation



| Event                                                                                        | Descrizione                                                                                                                                              |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MEAudioSessionDeviceRemoved](meaudiosessiondeviceremoved.md)                               | Il dispositivo audio è stato rimosso.                                                                                                                            |
| [MEAudioSessionDisconnected](meaudiosessiondisconnected.md)                                 | La sessione audio è stata disconnessa da una sessione di Servizi terminal di Windows                                                                              |
| [MEAudioSessionExclusiveModeOverride](meaudiosessionexclusivemodeoverride.md)               | La sessione audio è stata interrotta da una connessione in modalità esclusiva.                                                                                         |
| [MEAudioSessionFormatChanged](meaudiosessionformatchanged.md)                               | Il formato audio predefinito per il dispositivo audio è stato modificato.                                                                                                   |
| [MEAudioSessionGroupingParamChanged](meaudiosessiongroupingparamchanged.md)                 | Parametri di raggruppamento modificati per la sessione audio.                                                                                                   |
| [MEAudioSessionIconChanged](meaudiosessioniconchanged.md)                                   | Icona della sessione audio modificata.                                                                                                                          |
| [MEAudioSessionNameChanged](meaudiosessionnamechanged.md)                                   | Nome visualizzato della sessione audio modificato.                                                                                                                  |
| [MEAudioSessionServerShutdown](meaudiosessionservershutdown.md)                             | Il sistema server audio Windows è stato arrestato.                                                                                                           |
| [MEAudioSessionVolumeChanged](meaudiosessionvolumechanged.md)                               | Il volume o lo stato di silenziamento della sessione audio è stato modificato                                                                                                    |
| [MEBufferingStarted](mebufferingstarted.md)                                                 | Origine multimediale avviata per il buffer dei dati.                                                                                                                   |
| [MEBufferingStopped](mebufferingstopped.md)                                                 | Un'origine multimediale ha interrotto l'inserimento dei dati nel buffer.                                                                                                                   |
| [MECaptureAudioSessionDeviceRemoved](mecaptureaudiosessiondeviceremoved.md)                 | Il dispositivo è stato rimosso.                                                                                                                                  |
| [MECaptureAudioSessionDisconnected](mecaptureaudiosessiondisconnected.md)                   | La sessione audio è disconnessa perché l'utente si è disconnesso da una sessione di Servizi terminal di Windows (WTS).                                            |
| [MECaptureAudioSessionExclusiveModeOverride](mecaptureaudiosessionexclusivemodeoverride.md) | L'utente ha aperto un flusso audio in modalità esclusiva.                                                                                                       |
| [MECaptureAudioSessionFormatChanged](mecaptureaudiosessionformatchanged.md)                 | Il formato audio è stato modificato.                                                                                                                                |
| [MECaptureAudioSessionServerShutdown](mecaptureaudiosessionservershutdown.md)               | Arresto del server della sessione audio.                                                                                                                       |
| [MECaptureAudioSessionVolumeChanged](mecaptureaudiosessionvolumechanged.md)                 | Il volume è stato modificato.                                                                                                                                      |
| [MEConnectEnd](meconnectend.md)                                                             | L'origine di rete ha terminato l'apertura di un URL.                                                                                                               |
| [MEConnectStart](meconnectstart.md)                                                         | L'origine di rete ha avviato l'apertura di un URL.                                                                                                                |
| [MEContentProtectionMessage](mecontentprotectionmessage.md)                                 | La configurazione è stata modificata per uno schema di protezione dell'output.                                                                                               |
| [MEEnablerCompleted](meenablercompleted.md)                                                 | L'azione di un oggetto Enabler del contenuto è stata completata.                                                                                                           |
| [MEEnablerProgress](meenablerprogress.md)                                                   | Segnala lo stato di avanzamento di un oggetto abilitatore del contenuto.                                                                                                        |
| [MEEndOfPresentation](meendofpresentation.md)                                               | Generato da un'origine multimediale al termine di una presentazione.                                                                                                       |
| [MEEndOfPresentationSegment](meendofpresentationsegment.md)                                 | Generato dall'origine del sequencer quando un segmento viene completato ed è seguito da un altro segmento.                                                           |
| [MEEndOfStream](meendofstream.md)                                                           | Generato da un flusso multimediale al termine del flusso.                                                                                                           |
| [MEError](meerror.md)                                                                       | Segnala un errore grave.                                                                                                                                 |
| [MEExtendedType](meextendedtype.md)                                                         | Tipo di evento personalizzato.                                                                                                                                       |
| [MEIndividualizationCompleted](meindividualizationcompleted.md)                             | L'individualizzazione è stata completata.                                                                                                                           |
| [MEIndividualizationStart](meindividualizationstart.md)                                     | L'individualizzazione sta per iniziare.                                                                                                                     |
| [MELicenseAcquisitionCompleted](melicenseacquisitioncompleted.md)                           | L'acquisizione della licenza è stata completata.                                                                                                                         |
| [MELicenseAcquisitionStart](melicenseacquisitionstart.md)                                   | L'acquisizione della licenza sta per iniziare.                                                                                                                   |
| [MEMediaSample](memediasample.md)                                                           | Generato quando un flusso multimediale fornisce un nuovo esempio.                                                                                                        |
| [MENewPresentation](menewpresentation.md)                                                   | Generato da un'origine multimediale una nuova presentazione è pronta.                                                                                                    |
| [MENewStream](menewstream.md)                                                               | Generato da un'origine multimediale quando avvia un nuovo flusso.                                                                                                    |
| [MENonFatalError](menonfatalerror.md)                                                       | Si è verificato un errore non irreversibile durante il flusso.                                                                                                             |
| [MEPolicyChanged](mepolicychanged.md)                                                       | Il criterio di output per un flusso è stato modificato.                                                                                                                  |
| [MEPolicyError](mepolicyerror.md)                                                           | Generato da un output attendibile se si verifica un errore durante l'applicazione dei criteri di output.                                                                         |
| [MEPolicyReport](mepolicyreport.md)                                                         | Contiene informazioni sullo stato relative all'applicazione di criteri di output.                                                                                   |
| [MEPolicySet](mepolicyset.md)                                                               | Il metodo [**IMFOutputTrustAuthority:: Sepolicy**](/windows/desktop/api/mfidl/nf-mfidl-imfoutputtrustauthority-setpolicy) è stato completato.                                                    |
| [MEQualityNotify](mequalitynotify.md)                                                       | Fornisce commenti e suggerimenti sulla qualità della riproduzione al gestore qualità.                                                                                         |
| [MEReconnectEnd](mereconnectend.md)                                                         | Generato da un'origine multimediale al termine di un tentativo di riconnessione.                                                                                           |
| [MEReconnectStart](mereconnectstart.md)                                                     | Generato da un'origine multimediale all'inizio di un tentativo di riconnessione.                                                                                         |
| [MERendererEvent](merendererevent.md)                                                       | Generato dal renderer video avanzato (EVR) quando riceve un evento utente dal Presenter.                                                            |
| [MESequencerSourceTopologyUpdated](mesequencersourcetopologyupdated.md)                     | Generato dall'origine del sequencer quando il metodo [**IMFSequencerSource:: UpdateTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopology) viene completato in modo asincrono. |
| [MESessionCapabilitiesChanged](mesessioncapabilitieschanged.md)                             | Generato dalla sessione multimediale quando le funzionalità della sessione cambiano.                                                                                        |
| [MESessionClosed](mesessionclosed.md)                                                       | Generato quando il metodo [**IMFMediaSession:: Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) viene completato in modo asincrono.                                                 |
| [MESessionEnded](mesessionended.md)                                                         | Generato dalla sessione multimediale al termine della riproduzione dell'ultima presentazione nella coda di riproduzione.                                                    |
| [MESessionNotifyPresentationTime](mesessionnotifypresentationtime.md)                       | Generato dalla sessione multimediale all'avvio di una nuova presentazione.                                                                                              |
| [MESessionPaused](mesessionpaused.md)                                                       | Generato quando il metodo [**IMFMediaSession::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause) viene completato in modo asincrono.                                                 |
| [MESessionRateChanged](mesessionratechanged.md)                                             | Generato dalla sessione multimediale quando cambia la velocità di riproduzione.                                                                                              |
| [MESessionScrubSampleComplete](mesessionscrubsamplecomplete.md)                             | Generato dalla sessione multimediale quando completa una richiesta di ripulitura.                                                                                       |
| [MESessionStarted](mesessionstarted.md)                                                     | Generato quando il metodo [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) viene completato in modo asincrono.                                                 |
| [MESessionStopped](mesessionstopped.md)                                                     | Generato quando il metodo [**IMFMediaSession:: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop) viene completato in modo asincrono.                                                   |
| [MESessionStreamSinkFormatChanged](mesessionstreamsinkformatchanged.md)                     | Generato dalla sessione multimediale quando il formato viene modificato in un sink multimediale.                                                                                     |
| [MESessionTopologiesCleared](mesessiontopologiescleared.md)                                 | Generato dalla sessione multimediale quando il metodo [**IMFMediaSession:: ClearTopologies**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-cleartopologies) viene completato in modo asincrono.        |
| [MESessionTopologySet](mesessiontopologyset.md)                                             | Generato dopo che il metodo [**IMFMediaSession:: Setopologity**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) viene completato in modo asincrono                                     |
| [MESessionTopologyStatus](mesessiontopologystatus.md)                                       | Generato dalla sessione multimediale quando lo stato di una topologia cambia.                                                                                       |
| [MESinkInvalidated](mesinkinvalidated.md)                                                   | Generato quando un sink multimediale diventa non valido.                                                                                                                |
| [MESourceCharacteristicsChanged](mesourcecharacteristicschanged.md)                         | Generato da un'origine multimediale quando le caratteristiche dell'origine cambiano.                                                                                       |
| [MESourceMetadataChanged](mesourcemetadatachanged.md)                                       | Generato da un'origine multimediale durante l'aggiornamento dei relativi metadati.                                                                                                   |
| [MESourcePaused](mesourcepaused.md)                                                         | Generato da un'origine multimediale quando il metodo [**IMFMediaSource::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) viene completato in modo asincrono.                                 |
| [MESourceRateChanged](mesourceratechanged.md)                                               | Generato da un'origine multimediale quando cambia la velocità di riproduzione.                                                                                                 |
| [MESourceRateChangeRequested](mesourceratechangerequested.md)                               | Generato da un'origine multimediale per richiedere una nuova velocità di riproduzione.                                                                                                 |
| [MESourceSeeked](mesourceseeked.md)                                                         | Generato quando un'origine multimediale cerca una nuova posizione.                                                                                                      |
| [MESourceStarted](mesourcestarted.md)                                                       | Generato quando un'origine multimediale viene avviata senza cercare.                                                                                                       |
| [MESourceStopped](mesourcestopped.md)                                                       | Generato da un'origine multimediale quando il metodo [**IMFMediaSource:: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) viene completato in modo asincrono.                                   |
| [MEStreamFormatChanged](mestreamformatchanged.md)                                           | Generato da un flusso multimediale quando cambia il tipo di supporto del flusso.                                                                                      |
| [MEStreamPaused](mestreampaused.md)                                                         | Generato da un flusso multimediale quando il metodo [**IMFMediaSource::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) viene completato in modo asincrono.                                 |
| [MEStreamSeeked](mestreamseeked.md)                                                         | Generato da un flusso multimediale dopo una chiamata a [**IMFMediaSource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) causa una ricerca nel flusso.                              |
| [MEStreamSinkDeviceChanged](mestreamsinkdevicechanged.md)                                   | Generato dai sink del flusso di EVR se il dispositivo video viene modificato.                                                                                       |
| [MEStreamSinkFormatChanged](mestreamsinkformatchanged.md)                                   | Generato da un sink del flusso quando il tipo di supporto del sink non è più valido.                                                                                   |
| [MEStreamSinkMarker](mestreamsinkmarker.md)                                                 | Generato da un sink del flusso dopo la chiamata del metodo [**IMFStreamSink::P lacemarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) .                                      |
| [MEStreamSinkPaused](mestreamsinkpaused.md)                                                 | Generato da un sink del flusso quando completa la transizione allo stato sospeso.                                                                            |
| [MEStreamSinkPrerolled](mestreamsinkprerolled.md)                                           | Generato da un sink del flusso quando il flusso ha ricevuto un numero sufficiente di dati di preroll per avviare il rendering.                                                             |
| [MEStreamSinkRateChanged](mestreamsinkratechanged.md)                                       | Generato da un sink del flusso quando la frequenza è cambiata.                                                                                                       |
| [MEStreamSinkRequestSample](mestreamsinkrequestsample.md)                                   | Generato da un sink del flusso per richiedere un nuovo campione multimediale dalla pipeline.                                                                                 |
| [MEStreamSinkScrubSampleComplete](mestreamsinkscrubsamplecomplete.md)                       | Generato da un sink del flusso quando completa una richiesta di ripulitura.                                                                                           |
| [MEStreamSinkStarted](mestreamsinkstarted.md)                                               | Generato da un sink del flusso quando completa la transizione allo stato di esecuzione.                                                                           |
| [MEStreamSinkStopped](mestreamsinkstopped.md)                                               | Generato da un sink del flusso quando completa la transizione allo stato interrotto.                                                                           |
| [MEStreamStarted](mestreamstarted.md)                                                       | Generato da un flusso multimediale quando l'origine viene avviata senza la ricerca.                                                                                         |
| [MEStreamStopped](mestreamstopped.md)                                                       | Generato da un flusso multimediale quando il metodo [**IMFMediaSource:: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) viene completato in modo asincrono.                                   |
| [MEStreamThinMode](mestreamthinmode.md)                                                     | Generato da un flusso multimediale quando inizia o smette di assottigliare il flusso.                                                                                    |
| [MEStreamTick](mestreamtick.md)                                                             | Segnala che a un flusso multimediale non sono disponibili dati a un'ora specificata.                                                                            |
| [METransformDrainComplete](metransformdraincomplete.md)                                     | Inviato da una trasformazione di Media Foundation asincrona (MFT) quando un'operazione di svuotamento è stata completata.                                                             |
| [METransformHaveOutput](metransformhaveoutput.md)                                           | Inviato da un MFT asincrono quando sono disponibili nuovi dati di output dalla MFT.                                                                              |
| [METransformMarker](metransformmarker.md)                                                   | Inviato da un MFT asincrono in risposta a un messaggio dell' [**\_ indicatore del \_ comando \_ del messaggio MFT**](mft-message-command-marker.md) .                               |
| [METransformNeedInput](metransformneedinput.md)                                             | Inviato da un MFT asincrono per richiedere un nuovo esempio di input.                                                                                               |
| [MEUnknown](meunknown.md)                                                                   | Tipo di evento sconosciuto.                                                                                                                                      |
| [MEUpdatedStream](meupdatedstream.md)                                                       | Generato da un'origine multimediale quando viene riavviato o Cerca un flusso già attivo.                                                                      |
| [MEVideoCaptureDevicePreempted](mevideocapturedevicepreempted.md)                           | Il dispositivo è stato interrotto.                                                                                                                           |
| [MEVideoCaptureDeviceRemoved](mevideocapturedeviceremoved.md)                               | Il dispositivo è stato rimosso.                                                                                                                             |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida di riferimento alla programmazione di Media Foundation](media-foundation-programming-reference.md)
</dt> <dt>

[Generatori di eventi multimediali](media-event-generators.md)
</dt> <dt>

[**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)
</dt> </dl>

 

 



