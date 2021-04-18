---
description: Le API di base audio sono state introdotte in Windows Vista, che hanno fornito un nuovo set di componenti audio in modalità utente che un'applicazione client può usare per eseguire il rendering o acquisire flussi audio con funzionalità audio migliorate.
ms.assetid: eb99c266-16d2-4a14-bc1d-059a0a94db13
title: Novità relative alle API audio di base in Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3c87a4daa9e645587253239082475e59fd1563c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304865"
---
# <a name="whats-new-for-core-audio-apis-in-windows-7"></a>Novità relative alle API audio di base in Windows 7

Le API di base audio sono state introdotte in Windows Vista, che hanno fornito un nuovo set di componenti audio in modalità utente che un'applicazione client può usare per eseguire il rendering o acquisire flussi audio con funzionalità audio migliorate. Per una panoramica generale di questo set di API, vedere [informazioni sulle API audio di Windows Core](about-the-windows-core-audio-apis.md).

Le API di base audio sono state migliorate in Windows 7. La tabella seguente riepiloga le nuove funzionalità e i miglioramenti apportati alle API audio principali:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Funzionalità</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Miglioramenti generici</td>
<td>Le funzionalità seguenti sono state migliorate in Windows 7:
<ul>
<li>Nei flussi in modalità di condivisione di Windows 7 viene eseguito in <em>modalità a bassa latenza</em>. Il motore audio viene eseguito in modalità pull con una riduzione significativa della latenza. Questa operazione è molto utile per le applicazioni di comunicazione che richiedono una latenza di flusso audio bassa per un flusso più veloce.</li>
<li>Windows 7 fornisce un migliore rilevamento del ruolo del dispositivo quando un nuovo dispositivo viene aggiunto al sistema. Per ulteriori informazioni, vedere <a href="device-roles-in-windows-vista.md">utilizzo dei ruoli del dispositivo</a>.</li>
<li>In Windows 7 è possibile ascoltare musica dal lettore multimediale portatile tramite gli speaker del computer. È possibile utilizzare questa funzionalità di monitoraggio acquisizione inserendo un lettore multimediale portatile nel computer con un cavo audio analogico. In passato alcuni OEM hanno fornito questa funzionalità nel driver audio usando un loopback hardware. In Windows 7 questa funzionalità è stata aggiunta al sistema operativo. Poiché si tratta del sistema e non del driver, è possibile usarlo per qualsiasi altro dispositivo connesso al sistema, ad esempio una cuffia USB.</li>
<li>L'audio HDMI è stato migliorato in Windows 7, che fornisce il supporto per il formato a bitrate elevato. Con questo miglioramento, è possibile supportare audio multicanale e formati audio compressi su un connettore HDMI a un ricevitore audio.</li>
<li>In Windows Vista, Windows Media Player riproduce musica solo tramite il dispositivo audio predefinito, che non può essere modificato dall'utente. Per fare in modo che Windows Media Player esegua il rendering dell'audio in un dispositivo specifico, è necessario modificare il dispositivo predefinito nel pannello di controllo <strong>suoni</strong> . In Windows 7, Windows Media Player fornisce le API che consentono a un'applicazione di eseguire il rendering su qualsiasi dispositivo selezionato dall'utente e non solo sul dispositivo predefinito.</li>
<li>In Windows Vista, se un computer che sta riproducendo audio passa alla modalità di risparmio energia, il computer è bloccato e se l'utente desidera interrompere la riproduzione, l'utente deve effettuare l'accesso e premere il tasto Stop per arrestare la riproduzione. In Windows 7, se il computer è bloccato, è comunque possibile controllare la riproduzione usando il controllo HID sulla tastiera.</li>
<li>Windows 7 riduce il consumo di energia elettrica per qualsiasi applicazione che usa DirectSound e DirectShow per eseguire il rendering dei file multimediali. Inoltre, il servizio Utilità di pianificazione classi multimediali consente l'audio con resilienza e usa meno potenza durante la generazione degli esempi audio.</li>
</ul></td>
</tr>
<tr class="even">
<td>Dispositivo di comunicazione (nuovo)</td>
<td>In questa versione è stato aggiunto un nuovo tipo di dispositivo al pannello di controllo <strong>suoni</strong> : dispositivo di <strong>comunicazione</strong> . Questo dispositivo viene usato principalmente per le comunicazioni, ovvero per inserire o ricevere chiamate telefoniche sul computer. Un'applicazione di comunicazione può usare i componenti audio principali per ottenere un riferimento all'endpoint del dispositivo di comunicazione predefinito ed eseguire il rendering dei flussi audio a scopo di comunicazione. Il sistema operativo considera il flusso aperto in un dispositivo di comunicazione come flusso di comunicazione. Le operazioni WASAPI su un flusso di comunicazione sono simili ad altri flussi audio. Per ulteriori informazioni, vedere <a href="device-roles-in-windows-vista.md">utilizzo dei ruoli del dispositivo</a>.</td>
</tr>
<tr class="odd">
<td>Attenuazione del flusso o ducking audio (nuovo)</td>
<td>Il ducking automatico o l' <a href="stream-attenuation.md">attenuazione dei flussi</a> è una nuova funzionalità di Windows 7 progettata per applicazioni di comunicazione VoIP e unificata. Per impostazione predefinita, il sistema operativo riduce l'intensità di un flusso audio quando un flusso di comunicazione, ad esempio una telefonata, viene ricevuto sul dispositivo di comunicazione tramite il computer. Le opzioni del volume vengono impostate dall'utente nel pannello di controllo <strong>audio</strong> . Nel Windows SDK sono state aggiunte nuove API che consentono alle applicazioni di sostituire il comportamento predefinito di ducking. Per altre informazioni sull'implementazione di una funzionalità di ducking personalizzata, vedere <a href="providing-a-custom-ducking-experience.md">fornire un comportamento di ducking personalizzato</a>. <br/></td>
</tr>
<tr class="even">
<td>Routing del flusso (nuovo)</td>
<td>In Windows 7 le API di base sono state migliorate per trasferire facilmente un flusso audio da un dispositivo esistente a un nuovo endpoint audio predefinito. I set di API audio di alto livello che usano le API audio principali, ad esempio Media Foundation, DirectSound e WAVE, implementano la funzionalità di routing dei flussi. Le applicazioni multimediali che usano questi set di API per riprodurre o acquisire un flusso usano l'implementazione predefinita e non devono modificare l'applicazione. Tuttavia, se l'applicazione multimediale USA direttamente le API di base audio, l'applicazione deve fornire l'implementazione del routing del flusso. A tale scopo, l'applicazione deve gestire i nuovi eventi aggiunti che inviano una notifica a un client di WASAPI quando il dispositivo predefinito è connesso o rimosso. Per ulteriori informazioni su questa funzionalità, vedere <a href="stream-routing.md">routing del flusso</a>.</td>
</tr>
<tr class="odd">
<td>Audio in modalità utente protetto (PUMA) (migliorato)</td>
<td>PUMA è stato aggiornato per Windows 7 per fornire le funzionalità seguenti:
<ul>
<li>Impostazione dei bit MSC (Serial Copying Management System) negli endpoint S/PDIF e nei bit protezione del contenuto digitali (HDCP) a larghezza di banda elevata negli endpoint di High-Definition (HDMI).</li>
<li>Abilitazione dei controlli di protezione msc e HDMI all'esterno di un ambiente protetto (PE).</li>
</ul>
Per ulteriori informazioni sui miglioramenti, vedere <a href="protected-user-mode-audio--puma-.md">Protected User Mode Audio (Puma)</a>.<br/></td>
</tr>
<tr class="even">
<td>La struttura <strong>WAVEFORMATEXTENSIBLE</strong> è stata estesa alla struttura <strong>WAVEFORMATEXTENSIBLE_IEC61937</strong> (nuovo)</td>
<td>In Windows 7 è stata aggiunta una nuova struttura per supportare le trasmissioni IEC 61937. <strong>WAVEFORMATEXTENSIBLE_IEC61937</strong> estende la struttura <strong>WAVEFORMATEXTENSIBLE</strong> per archiviare due set di caratteristiche del flusso audio: il formato audio codificato prima della trasmissione e le caratteristiche del flusso audio dopo che è stato decodificato. La nuova struttura specifica in modo esplicito il numero effettivo di canali, le dimensioni del campione e la velocità dati di un formato non PCM. Con queste informazioni, un'applicazione può dedurre il livello di qualità del flusso non PCM dopo che è stato decompresso e riprodotto. Per ulteriori informazioni, vedere <a href="representing-formats-for-iec-61937-transmissions.md">rappresentazione di formati per trasmissioni IEC 61937</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize"><strong>IAudioClient:: Initialize</strong></a> (migliorato)</td>
<td>Il metodo <a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize"><strong>IAudioClient:: Initialize</strong></a> è stato migliorato per indicare errori specifici che potrebbero verificarsi durante l'apertura di un flusso audio. I nuovi codici di errore sono:
<ul>
<li>AUDCLNT_E_BUFFER_SIZE_NOT_ALIGNED</li>
<li>AUDCLNT_E_BUFFER_SIZE_ERROR</li>
<li>AUDCLNT_E_INVALID_DEVICE_PERIOD</li>
</ul>
Per ulteriori informazioni su questi errori, vedere la sezione valore restituito in <a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize"><strong>IAudioClient:: Initialize</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer"><strong>IAudioCaptureClient:: GetBuffer</strong></a> e <a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer"><strong>IAudioRenderClient:: GetBuffer</strong></a> (migliorato)</td>
<td>I metodi <a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer"><strong>IAudioCaptureClient:: GetBuffer</strong></a> e <a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer"><strong>IAudioRenderClient:: GetBuffer</strong></a> sono stati migliorati per restituire il codice di errore AUDCLNT_E_BUFFER_ERROR che indica che il buffer dell'endpoint in modalità esclusiva non è stato recuperato. Per ulteriori informazioni, vedere la sezione Osservazioni in <a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudiocaptureclient-getbuffer"><strong>IAudioCaptureClient:: GetBuffer</strong></a> e <a href="/windows/desktop/api/Audioclient/nf-audioclient-iaudiorenderclient-getbuffer"><strong>IAudioRenderClient:: GetBuffer</strong></a>.</td>
</tr>
<tr class="odd">
<td>Funzionalità rilevamento jack (migliorata)</td>
<td>Una nuova interfaccia di Windows 7, <a href="/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription2"><strong>IKsJackDescription2</strong></a>, estende <a href="/windows/desktop/api/Devicetopology/nn-devicetopology-iksjackdescription"><strong>IKsJackDescription</strong></a>. Usando la nuova interfaccia, lo stack audio o un'applicazione può ottenere informazioni Jack aggiuntive. Sono incluse le funzionalità di rilevamento di Jack e se il formato del dispositivo è stato modificato dinamicamente.</td>
</tr>
<tr class="even">
<td>Esempi di Windows (nuovo)</td>
<td>Sono stati aggiunti nuovi esempi all'Windows SDK che illustrano l'uso delle API di base di audio. Per altre informazioni, vedere <a href="sdk-samples-that-use-the-core-audio-apis.md">esempi di SDK che usano le API di base di audio</a>.</td>
</tr>
</tbody>
</table>



 

## <a name="major-new-interfaces"></a>Nuove interfacce principali

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

[Informazioni sulle API audio di Windows Core](about-the-windows-core-audio-apis.md)
</dt> </dl>

 

 




