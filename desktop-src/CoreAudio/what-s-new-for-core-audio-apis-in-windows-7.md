---
description: Le API Audio core sono state introdotte in Windows Vista, che ha fornito un nuovo set di componenti audio in modalità utente che un'applicazione client può usare per eseguire il rendering o acquisire flussi audio con funzionalità audio migliorate.
ms.assetid: eb99c266-16d2-4a14-bc1d-059a0a94db13
title: Novità delle API Core Audio in Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6160b275512a7efbd3b795e263f2ce8ae01be965
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474707"
---
# <a name="whats-new-for-core-audio-apis-in-windows-7"></a>Novità delle API Core Audio in Windows 7

Le API Audio core sono state introdotte in Windows Vista, che ha fornito un nuovo set di componenti audio in modalità utente che un'applicazione client può usare per eseguire il rendering o acquisire flussi audio con funzionalità audio migliorate. Per una panoramica generale di questo set di API, vedere [Informazioni sulle API audio Windows Core](about-the-windows-core-audio-apis.md).

Le API core audio sono state migliorate in Windows 7. La tabella seguente riepiloga le nuove funzionalità e i miglioramenti apportati alle API Audio core:




| Funzionalità | Descrizione | 
|---------|-------------|
| Miglioramenti generici | Le funzionalità seguenti sono state migliorate in Windows 7:<ul><li>In Windows 7 flussi in modalità di condivisione vengono eseguiti in <em>modalità a bassa latenza.</em> Il motore audio viene eseguito in modalità pull con una riduzione significativa della latenza. Ciò è molto utile per le applicazioni di comunicazione che richiedono una bassa latenza del flusso audio per uno streaming più veloce.</li><li>Windows 7 offre un migliore rilevamento del ruolo del dispositivo quando viene aggiunto un nuovo dispositivo al sistema. Per altre informazioni, vedere <a href="device-roles-in-windows-vista.md">Uso dei ruoli del dispositivo.</a></li><li>In Windows 7 è possibile ascoltare musica dal lettore multimediale portatile tramite gli altoparlanti del computer. È possibile usare questa funzionalità di Monitoraggio acquisizione collegando un lettore multimediale portatile al computer con un cavo audio analogico. In passato alcuni OEM hanno fornito questa funzionalità nel driver audio usando un loopback hardware. In Windows 7, questa funzionalità è stata aggiunta al sistema operativo. Poiché si trova nel sistema e non nel driver, è possibile usarlo per qualsiasi altro dispositivo connesso al sistema, ad esempio un visore USB.</li><li>L'audio HDMI è stato migliorato in Windows 7, che fornisce il supporto per il formato a velocità in bit elevata. Con questo miglioramento, è possibile supportare formati audio multicanale e audio compresso tramite un connettore HDMI a un ricevitore audio.</li><li>In Windows Vista, Windows Media Player la musica viene riprodotta solo tramite il dispositivo audio predefinito, che non può essere modificato dall'utente. Per Windows Media Player eseguire il rendering dell'audio in un dispositivo specifico, è necessario modificare il dispositivo predefinito nel <strong>pannello di</strong> controllo Suoni. In Windows 7, Windows Media Player api che consentono a un'applicazione di eseguire il rendering in qualsiasi dispositivo selezionato dall'utente e non solo nel dispositivo predefinito.</li><li>In Windows Vista, se un computer che riproduce l'audio passa alla modalità risparmio energia, il computer è bloccato e se l'utente vuole interrompere la riproduzione, l'utente deve accedere e premere il tasto di arresto per arrestare la riproduzione. In Windows 7, se il computer è bloccato, è comunque possibile controllare la riproduzione usando il controllo HID sulla tastiera.</li><li>Windows 7 riduce il consumo di energia per qualsiasi applicazione che usa DirectSound e DirectShow per il rendering dei contenuti multimediali. Inoltre, il servizio Utilità di pianificazione classi multimediali abilita l'audio resiliente agli errori e usa meno potenza durante la generazione degli esempi audio.</li></ul> | 
| Dispositivo di comunicazione (nuovo) | In questa versione è stato aggiunto un nuovo tipo di dispositivo al pannello di controllo <strong>Suoni:</strong> <strong>Dispositivo di</strong> comunicazione. Questo dispositivo viene usato principalmente per le comunicazioni, ad esempio per effettuare o ricevere chiamate telefoniche nel computer. Un'applicazione di comunicazione può usare i componenti Core Audio per ottenere un riferimento all'endpoint del dispositivo di comunicazione predefinito ed eseguire il rendering dei flussi audio a scopo di comunicazione. Il sistema operativo considera il flusso aperto in un dispositivo di comunicazione come un flusso di comunicazione. Le operazioni WASAPI in un flusso di comunicazione sono simili a qualsiasi altro flusso audio. Per altre informazioni, vedere <a href="device-roles-in-windows-vista.md">Uso dei ruoli del dispositivo.</a> | 
| Attenuazione del flusso o anatroccolo audio (Nuovo) | L'attenuazione <a href="stream-attenuation.md">automatica</a> o l'attenuazione dei flussi è una nuova funzionalità di Windows 7 destinata alle applicazioni VoIP e Unified Communication. Per impostazione predefinita, il sistema operativo riduce l'intensità di un flusso audio quando un flusso di comunicazione, ad esempio una telefonata, viene ricevuto sul dispositivo di comunicazione tramite il computer. Le opzioni di volume vengono impostate dall'utente nel <strong>pannello di</strong> controllo Audio. Sono state aggiunte nuove API nell'SDK Windows che consentono alle applicazioni di sostituire il comportamento di ducking predefinito. Per altre informazioni sull'implementazione di una funzionalità di papering personalizzata, vedere <a href="providing-a-custom-ducking-experience.md">Providing a Custom Ducking Behavior</a>. <br /> | 
| Routing di flusso (Nuovo) | In Windows 7, le API Audio core sono state migliorate per trasferire facilmente un flusso audio da un dispositivo esistente a un nuovo endpoint audio predefinito. I set di API audio di alto livello che usano API audio di base, ad esempio le API Media Foundation, DirectSound e WAVE, implementano la funzionalità di routing del flusso. Le applicazioni multimediali che usano questi set di API per riprodurre o acquisire un flusso usano l'implementazione predefinita e non devono modificare l'applicazione. Tuttavia, se l'applicazione multimediale usa direttamente le API Audio core, l'applicazione deve fornire l'implementazione del routing del flusso. A tale scopo, l'applicazione deve gestire i nuovi eventi aggiunti che inviano una notifica a un client WASAPI quando il dispositivo predefinito viene connesso o rimosso. Per altre informazioni su questa funzionalità, vedere <a href="stream-routing.md">Routing di flusso</a>. | 
| Audio in modalità utente protetto (PUMA) (migliorato) | PUMA è stato aggiornato per Windows 7 per fornire le funzionalità seguenti:<ul><li>Impostazione di bit SCMS (Serial Copying Management System) su endpoint S/PDIF e bit High-bandwidth Digital Content Protection (HDCP) sugli endpoint HDMI (High-Definition Multimedia Interface).</li><li>Abilitazione dei controlli di protezione SCMS e HDMI all'esterno di un ambiente protetto (PE).</li></ul>Per altre informazioni sui miglioramenti, vedere <a href="protected-user-mode-audio--puma-.md">Protected User Mode Audio (PUMA)</a>.<br /> | 
| La <strong>struttura WAVEFORMATEXTENSIBLE</strong> è stata estesa alla <strong>WAVEFORMATEXTENSIBLE_IEC61937</strong> (Nuova) | Nella Windows 7 è stata aggiunta una nuova struttura per supportare le trasmissioni IEC 61937. <strong>WAVEFORMATEXTENSIBLE_IEC61937</strong> estende la struttura <strong>WAVEFORMATEXTENSIBLE</strong> per archiviare due set di caratteristiche del flusso audio: il formato audio codificato prima della trasmissione e le caratteristiche del flusso audio dopo la decodifica. La nuova struttura specifica in modo esplicito il numero effettivo di canali, le dimensioni del campione e la velocità dei dati di un formato non PCM. Con queste informazioni, un'applicazione può dedurre il livello di qualità del flusso non PCM dopo che è stato decompresso e riprodotto. Per altre informazioni, vedere Rappresentazione dei formati per le trasmissioni <a href="representing-formats-for-iec-61937-transmissions.md">IEC 61937</a>.<br /> | 
| <a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize"><strong>IAudioClient::Initialize</strong></a> (migliorato) | Il <a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize"><strong>metodo IAudioClient::Initialize</strong></a> è stato migliorato per indicare errori specifici che potrebbero verificarsi durante l'apertura di un flusso audio. I nuovi codici di errore sono:<ul><li>AUDCLNT_E_BUFFER_SIZE_NOT_ALIGNED</li><li>AUDCLNT_E_BUFFER_SIZE_ERROR</li><li>AUDCLNT_E_INVALID_DEVICE_PERIOD</li></ul>Per altre informazioni su questi errori, vedere la sezione Valore restituito in <a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize"><strong>IAudioClient::Initialize</strong></a>.<br /> | 
| <a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer"><strong>IAudioCaptureClient::GetBuffer</strong></a> e <a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer"><strong>IAudioRenderClient::GetBuffer</strong></a> (migliorato) | I <a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer"><strong>metodi IAudioCaptureClient::GetBuffer</strong></a> e <a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer"><strong>IAudioRenderClient::GetBuffer</strong></a> sono stati migliorati per restituire il codice di errore AUDCLNT_E_BUFFER_ERROR che indica che il buffer dell'endpoint in modalità esclusiva non è stato recuperato. Per altre informazioni, vedere Osservazioni in <a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer"><strong>IAudioCaptureClient::GetBuffer</strong></a> e <a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer"><strong>IAudioRenderClient::GetBuffer</strong></a>. | 
| Funzionalità di rilevamento jack (migliorata) | Una nuova interfaccia in Windows 7, <a href="/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription2"><strong>IKsJackDescription2,</strong></a>estende <a href="/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription"><strong>IKsJackDescription.</strong></a> Usando la nuova interfaccia, lo stack audio o un'applicazione può ottenere informazioni aggiuntive sul jack. Ciò include la funzionalità di rilevamento del jack e la modifica dinamica del formato del dispositivo. | 
| Windows Esempi (nuovo) | Sono stati aggiunti nuovi esempi all'SDK Windows che illustrano l'uso delle API Audio core. Per altre informazioni, vedere <a href="sdk-samples-that-use-the-core-audio-apis.md">Esempi di SDK che usano le API audio di base.</a> | 




 

## <a name="major-new-interfaces"></a>Principali nuove interfacce

Le interfacce seguenti sono nuove per Windows 7:

-   [**IAudioClock2**](/windows/desktop/api/audioclient/nn-audioclient-iaudioclock2)
-   [**IAudioClockAdjustment**](/windows/desktop/api/audioclient/nn-audioclient-iaudioclockadjustment)
-   [**IAudioEndpointVolumeEx**](/windows/desktop/api/Endpointvolume/nn-endpointvolume-iaudioendpointvolumeex)
-   [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2)
-   [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2)
-   [**IAudioSessionEnumerator**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionenumerator)
-   [**IAudioSessionNotification**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionnotification)
-   [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification)
-   [**IKsJackDescription2**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription2)
-   [**IKsJackSinkInformation**](/windows/desktop/api/Devicetopology/nn-devicetopology-iksjacksinkinformation)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sulle WINDOWS Core Audio](about-the-windows-core-audio-apis.md)
</dt> </dl>

 

 




