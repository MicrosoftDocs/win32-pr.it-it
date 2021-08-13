---
description: Media Foundation eventi
ms.assetid: d925f63d-3359-4ba1-802f-0c2b11a3f973
title: Media Foundation eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38a922127941bd94103eac9cfb02ef33d1c0b789eb632f2689a3adc81494c377
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119268821"
---
# <a name="media-foundation-events"></a>Media Foundation eventi



| Event                                                                                        | Descrizione                                                                                                                                              |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MEAudioSessionDeviceRemoved](meaudiosessiondeviceremoved.md)                               | Il dispositivo audio è stato rimosso.                                                                                                                            |
| [MEAudioSessionDisconnected](meaudiosessiondisconnected.md)                                 | La sessione audio è stata disconnessa da una sessione Terminale Windows Services                                                                              |
| [MEAudioSessionExclusiveModeOverride](meaudiosessionexclusivemodeoverride.md)               | La sessione audio è stata preempted da una connessione in modalità esclusiva.                                                                                         |
| [MEAudioSessionFormatChanged](meaudiosessionformatchanged.md)                               | Il formato audio predefinito per il dispositivo audio è stato modificato.                                                                                                   |
| [MEAudioSessionGroupingParamChanged](meaudiosessiongroupingparamchanged.md)                 | Parametri di raggruppamento modificati per la sessione audio.                                                                                                   |
| [MEAudioSessionIconChanged](meaudiosessioniconchanged.md)                                   | L'icona della sessione audio è stata modificata.                                                                                                                          |
| [MEAudioSessionNameChanged](meaudiosessionnamechanged.md)                                   | Il nome visualizzato della sessione audio è stato modificato.                                                                                                                  |
| [MEAudioSessionServerShutdown](meaudiosessionservershutdown.md)                             | Il Windows server audio è stato arrestato.                                                                                                           |
| [MEAudioSessionVolumeChanged](meaudiosessionvolumechanged.md)                               | Lo stato del volume o dell'audio della sessione audio è stato modificato                                                                                                    |
| [MEBufferingStarted](mebufferingstarted.md)                                                 | Un'origine multimediale ha avviato il buffer dei dati.                                                                                                                   |
| [MEBufferingStopped](mebufferingstopped.md)                                                 | Un'origine multimediale ha interrotto la memorizzazione dei dati nel buffer.                                                                                                                   |
| [MECaptureAudioSessionDeviceRemoved](mecaptureaudiosessiondeviceremoved.md)                 | Il dispositivo è stato rimosso.                                                                                                                                  |
| [MECaptureAudioSessionDisconnected](mecaptureaudiosessiondisconnected.md)                   | La sessione audio viene disconnessa perché l'utente si è disconnesso da una sessione Terminale Windows Services (WTS).                                            |
| [MECaptureAudioSessionExclusiveModeOverride](mecaptureaudiosessionexclusivemodeoverride.md) | L'utente ha aperto un flusso audio in modalità esclusiva.                                                                                                       |
| [MECaptureAudioSessionFormatChanged](mecaptureaudiosessionformatchanged.md)                 | Il formato audio è stato modificato.                                                                                                                                |
| [MECaptureAudioSessionServerShutdown](mecaptureaudiosessionservershutdown.md)               | Arresto del server della sessione audio.                                                                                                                       |
| [MECaptureAudioSessionVolumeChanged](mecaptureaudiosessionvolumechanged.md)                 | Volume modificato.                                                                                                                                      |
| [MEConnectEnd](meconnectend.md)                                                             | L'origine di rete ha terminato l'apertura di un URL.                                                                                                               |
| [MEConnectStart](meconnectstart.md)                                                         | L'origine di rete ha iniziato ad aprire un URL.                                                                                                                |
| [MEContentProtectionMessage](mecontentprotectionmessage.md)                                 | La configurazione è stata modificata per uno schema di protezione dell'output.                                                                                               |
| [MEEnablerCompleted](meenablercompleted.md)                                                 | L'azione di un oggetto content enabler è stata completata.                                                                                                           |
| [MEEnablerProgress](meenablerprogress.md)                                                   | Segnala lo stato di avanzamento di un oggetto di abilitazione del contenuto.                                                                                                        |
| [MEEndOfPresentation](meendofpresentation.md)                                               | Generato da un'origine multimediale al termine di una presentazione.                                                                                                       |
| [MEEndOfPresentationSegment](meendofpresentationsegment.md)                                 | Generato dall'origine sequencer quando un segmento viene completato ed è seguito da un altro segmento.                                                           |
| [MEEndOfStream](meendofstream.md)                                                           | Generato da un flusso multimediale al termine del flusso.                                                                                                           |
| [ERRORE MEError](meerror.md)                                                                       | Segnala un errore grave.                                                                                                                                 |
| [MEExtendedType](meextendedtype.md)                                                         | Tipo di evento personalizzato.                                                                                                                                       |
| [MEIndividualizationCompleted](meindividualizationcompleted.md)                             | L'individualizzazione è completa.                                                                                                                           |
| [MEIndividualizationStart](meindividualizationstart.md)                                     | L'individualizzazione sta per iniziare.                                                                                                                     |
| [MELicenseAcquisitionCompleted](melicenseacquisitioncompleted.md)                           | L'acquisizione della licenza è stata completata.                                                                                                                         |
| [MELicenseAcquisitionStart](melicenseacquisitionstart.md)                                   | L'acquisizione della licenza sta per iniziare.                                                                                                                   |
| [MEMediaSample](memediasample.md)                                                           | Generato quando un flusso multimediale recapita un nuovo esempio.                                                                                                        |
| [MENewPresentation](menewpresentation.md)                                                   | Generato da un'origine multimediale, una nuova presentazione è pronta.                                                                                                    |
| [MENewStream](menewstream.md)                                                               | Generato da un'origine multimediale all'avvio di un nuovo flusso.                                                                                                    |
| [MENonFatalError](menonfatalerror.md)                                                       | Si è verificato un errore non irreversibile durante il flusso.                                                                                                             |
| [MEPolicyChanged](mepolicychanged.md)                                                       | I criteri di output per un flusso sono stati modificati.                                                                                                                  |
| [MEPolicyError](mepolicyerror.md)                                                           | Generato da un output attendibile se si verifica un errore durante l'applicazione dei criteri di output.                                                                         |
| [MEPolicyReport](mepolicyreport.md)                                                         | Contiene informazioni sullo stato relative all'imposizione di un criterio di output.                                                                                   |
| [MEPolicySet](mepolicyset.md)                                                               | Metodo [**IMFOutputTrustAuthority::SetPolicy**](/windows/desktop/api/mfidl/nf-mfidl-imfoutputtrustauthority-setpolicy) completato.                                                    |
| [MEQualityNotify](mequalitynotify.md)                                                       | Fornisce commenti e suggerimenti sulla qualità della riproduzione al gestore della qualità.                                                                                         |
| [MEReconnectEnd](mereconnectend.md)                                                         | Generato da un'origine multimediale alla fine di un tentativo di riconnessione.                                                                                           |
| [MEReconnectStart](mereconnectstart.md)                                                     | Generato da un'origine multimediale all'inizio di un tentativo di riconnessione.                                                                                         |
| [MERendererEvent](merendererevent.md)                                                       | Generato dal renderer video avanzato (EVR) quando riceve un evento utente dal presentatore.                                                            |
| [MESequencerSourceTopologyUpdated](mesequencersourcetopologyupdated.md)                     | Generato dall'origine sequencer quando il [**metodo IMFSequencerSource::UpdateTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopology) viene completato in modo asincrono. |
| [MESessionCapabilitiesChanged](mesessioncapabilitieschanged.md)                             | Generato dalla sessione multimediale quando le funzionalità della sessione cambiano.                                                                                        |
| [MESessionClosed](mesessionclosed.md)                                                       | Generato quando il [**metodo IMFMediaSession::Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) viene completato in modo asincrono.                                                 |
| [MESessionEnded](mesessionended.md)                                                         | Generato dalla sessione multimediale al termine della riproduzione dell'ultima presentazione nella coda di riproduzione.                                                    |
| [MESessionNotifyPresentationTime](mesessionnotifypresentationtime.md)                       | Generato dalla sessione multimediale all'avvio di una nuova presentazione.                                                                                              |
| [MESessionPaused](mesessionpaused.md)                                                       | Generato quando il [**metodo IMFMediaSession::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause) viene completato in modo asincrono.                                                 |
| [MESessionRateChanged](mesessionratechanged.md)                                             | Generato dalla sessione multimediale quando cambia la frequenza di riproduzione.                                                                                              |
| [MESessionScrubSampleComplete](mesessionscrubsamplecomplete.md)                             | Generato dalla sessione multimediale quando completa una richiesta di pulitura.                                                                                       |
| [MESessionStarted](mesessionstarted.md)                                                     | Generato quando il [**metodo IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) viene completato in modo asincrono.                                                 |
| [MeSessionStopped](mesessionstopped.md)                                                     | Generato quando il [**metodo IMFMediaSession::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop) viene completato in modo asincrono.                                                   |
| [MESessionStreamSinkFormatChanged](mesessionstreamsinkformatchanged.md)                     | Generato dalla sessione multimediale quando il formato viene modificato in un sink multimediale.                                                                                     |
| [MESessionTopologiesCleared](mesessiontopologiescleared.md)                                 | Generato dalla sessione multimediale quando il [**metodo IMFMediaSession::ClearTopologies**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-cleartopologies) viene completato in modo asincrono.        |
| [MESessionTopologySet](mesessiontopologyset.md)                                             | Generato dopo il completamento asincrono del metodo [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology)                                     |
| [MESessionTopologyStatus](mesessiontopologystatus.md)                                       | Generato dalla sessione multimediale quando cambia lo stato di una topologia.                                                                                       |
| [MESinkInvalidated](mesinkinvalidated.md)                                                   | Generato quando un sink multimediale diventa non valido.                                                                                                                |
| [MESourceCharacteristicsChanged](mesourcecharacteristicschanged.md)                         | Generato da un'origine multimediale quando le caratteristiche dell'origine cambiano.                                                                                       |
| [MESourceMetadataChanged](mesourcemetadatachanged.md)                                       | Generato da un'origine multimediale quando aggiorna i relativi metadati.                                                                                                   |
| [MESourcePaused](mesourcepaused.md)                                                         | Generato da un'origine multimediale quando il [**metodo IMFMediaSource::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) viene completato in modo asincrono.                                 |
| [MESourceRateChanged](mesourceratechanged.md)                                               | Generato da un'origine multimediale quando cambia la frequenza di riproduzione.                                                                                                 |
| [MESourceRateChangeRequested](mesourceratechangerequested.md)                               | Generato da un'origine multimediale per richiedere una nuova frequenza di riproduzione.                                                                                                 |
| [MESourceSeeked](mesourceseeked.md)                                                         | Generato quando un'origine multimediale cerca in una nuova posizione.                                                                                                      |
| [MESourceStarted](mesourcestarted.md)                                                       | Generato quando un'origine multimediale inizia senza eseguire la ricerca.                                                                                                       |
| [MESourceStopped](mesourcestopped.md)                                                       | Generato da un'origine multimediale quando il [**metodo IMFMediaSource::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) viene completato in modo asincrono.                                   |
| [MEStreamFormatChanged](mestreamformatchanged.md)                                           | Generato da un flusso multimediale quando cambia il tipo di contenuto multimediale del flusso.                                                                                      |
| [MEStreamPaused](mestreampaused.md)                                                         | Generato da un flusso multimediale quando il [**metodo IMFMediaSource::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) viene completato in modo asincrono.                                 |
| [MEStreamSeeked](mestreamseeked.md)                                                         | Generato da un flusso multimediale dopo una chiamata a [**IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) causa una ricerca nel flusso.                              |
| [MEStreamSinkDeviceChanged](mestreamsinkdevicechanged.md)                                   | Generato dai sink di flusso dell'EVR se il dispositivo video viene modificato.                                                                                       |
| [MEStreamSinkFormatChanged](mestreamsinkformatchanged.md)                                   | Generato da un sink di flusso quando il tipo di supporto del sink non è più valido.                                                                                   |
| [MEStreamSinkMarker](mestreamsinkmarker.md)                                                 | Generato da un sink di flusso dopo la chiamata del metodo [**IMFStreamSink::P laceMarker.**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker)                                      |
| [MEStreamSinkPaused](mestreamsinkpaused.md)                                                 | Generato da un sink di flusso quando completa la transizione allo stato sospeso.                                                                            |
| [MEStreamSinkPrerolled](mestreamsinkprerolled.md)                                           | Generato da un sink di flusso quando il flusso ha ricevuto dati di preroll sufficienti per iniziare il rendering.                                                             |
| [MEStreamSinkRateChanged](mestreamsinkratechanged.md)                                       | Generato da un sink di flusso quando la frequenza è cambiata.                                                                                                       |
| [MEStreamSinkRequestSample](mestreamsinkrequestsample.md)                                   | Generato da un sink di flusso per richiedere un nuovo esempio multimediale dalla pipeline.                                                                                 |
| [MEStreamSinkScrubSampleComplete](mestreamsinkscrubsamplecomplete.md)                       | Generato da un sink di flusso quando completa una richiesta di pulitura.                                                                                           |
| [MEStreamSinkStarted](mestreamsinkstarted.md)                                               | Generato da un sink di flusso quando completa la transizione allo stato di esecuzione.                                                                           |
| [MEStreamSinkStopped](mestreamsinkstopped.md)                                               | Generato da un sink di flusso quando completa la transizione allo stato arrestato.                                                                           |
| [MEStreamStarted](mestreamstarted.md)                                                       | Generato da un flusso multimediale quando l'origine inizia senza eseguire la ricerca.                                                                                         |
| [MEStreamStopped](mestreamstopped.md)                                                       | Generato da un flusso multimediale quando il [**metodo IMFMediaSource::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) viene completato in modo asincrono.                                   |
| [MEStreamThinMode](mestreamthinmode.md)                                                     | Generato da un flusso multimediale all'avvio o all'arresto del flusso.                                                                                    |
| [MEStreamTick](mestreamtick.md)                                                             | Segnala che in un flusso multimediale non sono disponibili dati in un momento specificato.                                                                            |
| [METransformDrainComplete](metransformdraincomplete.md)                                     | Inviato da una trasformazione Media Foundation asincrona (MFT) al termine di un'operazione di svuotamento.                                                             |
| [METransformHaveOutput](metransformhaveoutput.md)                                           | Inviato da un MFT asincrono quando sono disponibili nuovi dati di output da MFT.                                                                              |
| [METransformMarker](metransformmarker.md)                                                   | Inviato da un MFT asincrono in risposta a un messaggio [**MFT \_ MESSAGE COMMAND \_ \_ MARKER.**](mft-message-command-marker.md)                               |
| [METransformNeedInput](metransformneedinput.md)                                             | Inviato da un MFT asincrono per richiedere un nuovo esempio di input.                                                                                               |
| [MEUnknown](meunknown.md)                                                                   | Tipo di evento sconosciuto.                                                                                                                                      |
| [MEUpdatedStream](meupdatedstream.md)                                                       | Generato da un'origine multimediale al riavvio o alla ricerca di un flusso già attivo.                                                                      |
| [MEVideoCaptureDevicePreempted](mevideocapturedevicepreempted.md)                           | Il dispositivo è stato preempted.                                                                                                                           |
| [MEVideoCaptureDeviceRemoved](mevideocapturedeviceremoved.md)                               | Il dispositivo è stato rimosso.                                                                                                                             |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida di riferimento alla programmazione di Media Foundation](media-foundation-programming-reference.md)
</dt> <dt>

[Generatori di eventi multimediali](media-event-generators.md)
</dt> <dt>

[**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)
</dt> </dl>

 

 



