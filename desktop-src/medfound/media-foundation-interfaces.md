---
description: Interfacce di Media Foundation
ms.assetid: 3e367190-4c88-430e-adbf-9837e1bf0d2b
title: Interfacce di Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a12379dc83287b2a03ae0223a5a9a7d945d8fa77
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103968861"
---
# <a name="media-foundation-interfaces"></a>Interfacce di Media Foundation

## <a name="in-this-section"></a>Contenuto della sezione



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Argomento</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Mfmediacapture/nn-mfmediacapture-iadvancedmediacapture"><strong>IAdvancedMediaCapture</strong></a><br/></td>
<td>Abilita l'acquisizione avanzata dei supporti.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediacapture/nn-mfmediacapture-iadvancedmediacaptureinitializationsettings"><strong>IAdvancedMediaCaptureInitializationSettings</strong></a><br/></td>
<td>Fornisce le impostazioni di inizializzazione per Advanced Media Capture.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Mfmediacapture/nn-mfmediacapture-iadvancedmediacapturesettings"><strong>IAdvancedMediaCaptureSettings</strong></a><br/></td>
<td>Fornisce le impostazioni per Advanced Media Capture.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9"><strong>IDirect3DDeviceManager9</strong></a><br/></td>
<td>Consente a due thread di condividere lo stesso dispositivo Direct3D 9 e fornisce l'accesso alle funzionalità di accelerazione video DirectX (DXVA) del dispositivo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoaccelerationservice"><strong>IDirectXVideoAccelerationService</strong></a><br/></td>
<td>Fornisce servizi di accelerazione video DirectX (DXVA) da un dispositivo Direct3D.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder"><strong>IDirectXVideoDecoder</strong></a><br/></td>
<td>Rappresenta un dispositivo di decodificatore video DXVA (DirectX Video Acceleration).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice"><strong>IDirectXVideoDecoderService</strong></a><br/></td>
<td>Fornisce l'accesso ai servizi di decodificatori DirectX Video Acceleration (DXVA).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration"><strong>IDirectXVideoMemoryConfiguration</strong></a><br/></td>
<td>Imposta il tipo di memoria video per le superfici video non compresse.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessor"><strong>IDirectXVideoProcessor</strong></a><br/></td>
<td>Rappresenta un dispositivo processore video DXVA (DirectX Video Acceleration).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice"><strong>IDirectXVideoProcessorService</strong></a><br/></td>
<td>Fornisce l'accesso ai servizi di elaborazione video DXVA (DirectX Video Acceleration).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/evr/nn-evr-ievrfilterconfig"><strong>IEVRFilterConfig</strong></a><br/></td>
<td>Imposta il numero di pin di input nel filtro EVR (DirectShow <a href="/windows/desktop/DirectShow/enhanced-video-renderer-filter"><strong>Enhanced video renderer</strong></a> ).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/evr/nn-evr-ievrfilterconfigex"><strong>IEVRFilterConfigEx</strong></a><br/></td>
<td>Configura il filtro EVR (DirectShow <a href="/windows/desktop/DirectShow/enhanced-video-renderer-filter"><strong>Enhanced video renderer</strong></a> ).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/evr/nn-evr-ievrtrustedvideoplugin"><strong>IEVRTrustedVideoPlugin</strong></a><br/></td>
<td>Abilita un componente plug-in per il renderer video migliorato (EVR) per l'utilizzo con supporti protetti.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/evr9/nn-evr9-ievrvideostreamcontrol"><strong>IEVRVideoStreamControl</strong></a><br/></td>
<td>Questa interfaccia non è supportata.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer"><strong>IMF2DBuffer</strong></a><br/></td>
<td>Rappresenta un buffer che contiene una superficie bidimensionale, ad esempio un fotogramma video. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer2"><strong>IMF2DBuffer2</strong></a><br/></td>
<td>Rappresenta un buffer che contiene una superficie bidimensionale, ad esempio un fotogramma video.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate"><strong>IMFActivate</strong></a><br/></td>
<td>Consente all'applicazione di rinviare la creazione di un oggetto.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo"><strong>IMFASFContentInfo</strong></a><br/></td>
<td>Fornisce metodi per utilizzare la sezione di intestazione dei file conformi alla specifica ASF (Advanced Systems Format). <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer"><strong>IMFASFIndexer</strong></a><br/></td>
<td>Fornisce metodi per lavorare con gli indici nei file di formato di sistema (ASF).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmultiplexer"><strong>IMFASFMultiplexer</strong></a><br/></td>
<td>Fornisce metodi per la creazione di pacchetti di dati ASF (Advanced Systems Format).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmutualexclusion"><strong>IMFASFMutualExclusion</strong></a><br/></td>
<td>Configura un oggetto di esclusione reciproca del formato Advanced Systems (ASF) che gestisce le informazioni su un gruppo di flussi in un profilo ASF che si escludono a vicenda.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile"><strong>IMFASFProfile</strong></a><br/></td>
<td>Gestisce un profilo ASF (Advanced Systems Format).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter"><strong>IMFASFSplitter</strong></a><br/></td>
<td>Fornisce i metodi per leggere i dati da un file di formato Advanced Systems (ASF).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig"><strong>IMFASFStreamConfig</strong></a><br/></td>
<td>Configura le impostazioni di un flusso in un file ASF.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamprioritization"><strong>IMFASFStreamPrioritization</strong></a><br/></td>
<td>Non implementato.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamselector"><strong>IMFASFStreamSelector</strong></a><br/></td>
<td>Seleziona i flussi in un file di formato Advanced Systems (ASF), in base alle informazioni sull'esclusione reciproca nell'intestazione ASF.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback"><strong>IMFAsyncCallback</strong></a><br/></td>
<td>Interfaccia di callback per notificare all'applicazione quando viene completato un metodo asincrono. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Mfobjects/nn-mfobjects-imfasynccallbacklogging"><strong>IMFAsyncCallbackLogging</strong></a><br/></td>
<td>Fornisce informazioni di registrazione sull'oggetto padre a cui è associato il callback asincrono.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult"><strong>IMFAsyncResult</strong></a><br/></td>
<td>Fornisce informazioni sul risultato di un'operazione asincrona. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes"><strong>IMFAttributes</strong></a><br/></td>
<td>Fornisce un metodo generico per archiviare le coppie chiave/valore in un oggetto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfaudiomediatype"><strong>IMFAudioMediaType</strong></a><br/></td>
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfaudiomediatype"><strong>IMFAudioMediaType</strong></a> non è più disponibile per l'uso a partire da Windows 7.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy"><strong>IMFAudioPolicy</strong></a><br/></td>
<td>Configura la sessione audio associata al renderer di streaming audio (SAR).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfaudiostreamvolume"><strong>IMFAudioStreamVolume</strong></a><br/></td>
<td>Controlla i livelli di volume dei singoli canali audio.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfbufferlistnotify"><strong>IMFBufferListNotify</strong></a><br/></td>
<td>Consente all'oggetto <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebufferlist"><strong>IMFSourceBufferList</strong></a> di inviare una notifica ai client di importanti modifiche di stato.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream"><strong>IMFByteStream</strong></a><br/></td>
<td>Rappresenta un flusso di byte da un'origine dati, che potrebbe essere un file locale, un file di rete o un'altra origine.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfbytestreambuffering"><strong>IMFByteStreamBuffering</strong></a><br/></td>
<td>Controlla il modo in cui un flusso di byte memorizza nel buffer i dati da una rete. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamcachecontrol"><strong>IMFByteStreamCacheControl</strong></a><br/></td>
<td>Controlla il modo in cui un flusso di byte di rete trasferisce i dati in una cache locale.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamcachecontrol2"><strong>IMFByteStreamCacheControl2</strong></a><br/></td>
<td>Controlla il modo in cui un flusso di byte di rete trasferisce i dati in una cache locale.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler"><strong>IMFByteStreamHandler</strong></a><br/></td>
<td>Crea un'origine multimediale da un flusso di byte. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestreamproxyclassfactory"><strong>IMFByteStreamProxyClassFactory</strong></a><br/></td>
<td>Crea un proxy per un flusso di byte.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamtimeseek"><strong>IMFByteStreamTimeSeek</strong></a><br/></td>
<td>Cerca un flusso di byte in base alla posizione del tempo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengine"><strong>IMFCaptureEngine</strong></a><br/></td>
<td>Controlla uno o più dispositivi di acquisizione.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengineclassfactory"><strong>IMFCaptureEngineClassFactory</strong></a><br/></td>
<td>Crea un'istanza del motore di acquisizione.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengineoneventcallback"><strong>IMFCaptureEngineOnEventCallback</strong></a><br/></td>
<td>Interfaccia di callback per la ricezione di eventi dal motore di acquisizione.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengineonsamplecallback"><strong>IMFCaptureEngineOnSampleCallback</strong></a><br/></td>
<td>Interfaccia di callback per la ricezione di dati dal motore di acquisizione.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengineonsamplecallback2"><strong>IMFCaptureEngineOnSampleCallback2</strong></a><br/></td>
<td>Estensioni per l'interfaccia di callback <a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengineonsamplecallback"><strong>IMFCaptureEngineOnSampleCallback</strong></a> utilizzata per ricevere dati dal motore di acquisizione.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturephotosink"><strong>IMFCapturePhotoSink</strong></a><br/></td>
<td>Controlla il sink foto.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturepreviewsink"><strong>IMFCapturePreviewSink</strong></a><br/></td>
<td>Controlla il sink di anteprima.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturerecordsink"><strong>IMFCaptureRecordSink</strong></a><br/></td>
<td>Controlla il sink di registrazione.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturesink"><strong>IMFCaptureSink</strong></a><br/></td>
<td>Controlla un sink di acquisizione, ovvero un oggetto che riceve uno o più flussi da un dispositivo di acquisizione.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturesink2"><strong>IMFCaptureSink2</strong></a><br/></td>
<td>Estende l'interfaccia <a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturesink"><strong>IMFCaptureSink</strong></a> per fornire funzionalità per l'impostazione dinamica del tipo di supporto di output del sink di record o del sink di anteprima.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturesource"><strong>IMFCaptureSource</strong></a><br/></td>
<td>Controlla l'oggetto di origine di acquisizione. L'origine di acquisizione gestisce i dispositivi di acquisizione audio e video.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfcdmsuspendnotify"><strong>IMFCdmSuspendNotify</strong></a><br/></td>
<td>Usato per consentire al client di inviare una notifica al modulo di decrittografia del contenuto (CDM) quando le risorse globali devono essere riportate in uno stato coerente prima della sospensione. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfclock"><strong>IMFClock</strong></a><br/></td>
<td>Fornisce informazioni sull'intervallo da un clock in Microsoft Media Foundation.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfclockconsumer"><strong>IMFClockConsumer</strong></a><br/></td>
<td>Implementato da un'app per ottenere l'accesso a <a href="/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock"><strong>IMFPresentationClock</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink"><strong>IMFClockStateSink</strong></a><br/></td>
<td>Riceve notifiche di modifica dello stato dal clock della presentazione. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection"><strong>IMFCollection</strong></a><br/></td>
<td>Rappresenta una raccolta generica di puntatori <strong>IUnknown</strong> . <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfcontentdecryptorcontext"><strong>IMFContentDecryptorContext</strong></a><br/></td>
<td>Consente a un componente di decrittografia di gestire chiavi hardware e decrittografare gli esempi di hardware.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler"><strong>IMFContentEnabler</strong></a><br/></td>
<td>Implementa un passaggio da eseguire per l'accesso dell'utente ai contenuti multimediali.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectiondevice"><strong>IMFContentProtectionDevice</strong></a><br/></td>
<td>Consente a un decrittografatore di comunicare con il processore di sicurezza che implementa la decrittografia hardware per un sistema di protezione. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager"><strong>IMFContentProtectionManager</strong></a><br/></td>
<td>Abilita la riproduzione del contenuto protetto fornendo all'applicazione un puntatore a un oggetto Enabler del contenuto.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/evr/nn-evr-imfdesiredsample"><strong>IMFDesiredSample</strong></a><br/></td>
<td>Consente al presentatore per il renderer video avanzato (EVR) di richiedere un frame specifico dal mixer video.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmp2dlna/nn-mfmp2dlna-imfdlnasinkinit"><strong>IMFDLNASinkInit</strong></a><br/></td>
<td>Inizializza il sink di supporto Digital Living Network Alliance (DLNA). <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfdrmnethelper"><strong>IMFDRMNetHelper</strong></a><br/></td>
<td>Configura Windows Media Digital Rights Management (DRM) per i dispositivi di rete in un sink di rete.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgibuffer"><strong>IMFDXGIBuffer</strong></a><br/></td>
<td>Rappresenta un buffer che contiene una superficie Microsoft DirectX Graphics Infrastructure (DXGI).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager"><strong>IMFDXGIDeviceManager</strong></a><br/></td>
<td>Consente a due thread di condividere lo stesso dispositivo Microsoft Direct3D 11.<br/></td>
</tr>
<tr class="odd">
<td><a href="imfdxgidevicemanagersource.md"><strong>IMFDXGIDeviceManagerSource</strong></a><br/></td>
<td>Fornisce la funzionalità per ottenere <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager"><strong>IMFDXGIDeviceManager</strong></a> dall'Media Foundation sink di rendering video.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock"><strong>IMFFieldOfUseMFTUnlock</strong></a><br/></td>
<td>Consente a un'applicazione di usare una trasformazione Media Foundation (MFT) che presenta restrizioni sull'uso.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imffinalizablemediasink"><strong>IMFFinalizableMediaSink</strong></a><br/></td>
<td>Facoltativamente supportata dai sink di supporto per eseguire le attività richieste prima dell'arresto.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfgetservice"><strong>IMFGetService</strong></a><br/></td>
<td>Esegue una query su un oggetto per un'interfaccia del servizio specificata. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfhttpdownloadrequest"><strong>IMFHttpDownloadRequest</strong></a><br/></td>
<td>Le applicazioni implementano questa interfaccia per eseguire l'override dell'implementazione predefinita dei protocolli HTTP e HTTPS utilizzati da Microsoft Media Foundation. Le applicazioni forniscono l'interfaccia <strong>IMFHttpDownloadRequest</strong> per Media Foundation tramite il metodo <a href="/windows/desktop/api/mfidl/nf-mfidl-imfhttpdownloadsession-createrequest"><strong>CreateRequest</strong></a> sull'interfaccia <a href="/windows/desktop/api/mfidl/nn-mfidl-imfhttpdownloadsession"><strong>IMFHttpDownloadSession</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfhttpdownloadsession"><strong>IMFHttpDownloadSession</strong></a><br/></td>
<td>Le applicazioni implementano questa interfaccia per eseguire l'override dell'implementazione predefinita dei protocolli HTTP e HTTPS utilizzati da Microsoft Media Foundation. Le applicazioni forniscono l'interfaccia <strong>IMFHttpDownloadSession</strong> per Media Foundation tramite il metodo <a href="/windows/desktop/api/mfidl/nf-mfidl-imfhttpdownloadsessionprovider-createhttpdownloadsession"><strong>CreateHttpDownloadSession</strong></a> sull'interfaccia <a href="/windows/desktop/api/mfidl/nn-mfidl-imfhttpdownloadsessionprovider"><strong>IMFHttpDownloadSessionProvider</strong></a> . Microsoft Media Foundation usa questa interfaccia per eseguire il download di una risorsa identificata da un URL HTTP o HTTPS. È possibile inviare più richieste HTTP per scaricare la risorsa. L'interfaccia <strong>IMFHttpDownloadSession</strong> viene utilizzata per creare queste singole richieste HTTP.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfhttpdownloadsessionprovider"><strong>IMFHttpDownloadSessionProvider</strong></a><br/></td>
<td>Le applicazioni implementano questa interfaccia per fornire un'implementazione personalizzata di download HTTP o HTTPS. Utilizzare l'interfaccia <a href="/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver"><strong>IMFSourceResolver</strong></a> per registrare il provider. Per ulteriori informazioni, vedere <a href="using-the-source-resolver.md">using the source resolver</a>. Una volta registrato, il Microsoft Media Foundation richiamerà il metodo <a href="/windows/desktop/api/mfidl/nf-mfidl-imfhttpdownloadsessionprovider-createhttpdownloadsession"><strong>CreateHttpDownloadSession</strong></a> dell'implementazione del provider per aprire URL http o https invece di usare l'implementazione predefinita.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfsharingengine/nn-mfsharingengine-imfimagesharingengine"><strong>IMFImageSharingEngine</strong></a><br/></td>
<td>Consente la condivisione delle immagini.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfsharingengine/nn-mfsharingengine-imfimagesharingengineclassfactory"><strong>IMFImageSharingEngineClassFactory</strong></a><br/></td>
<td>Crea un'istanza di <a href="/windows/desktop/api/mfsharingengine/nn-mfsharingengine-imfimagesharingengine"><strong>IMFImageSharingEngine</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfinputtrustauthority"><strong>IMFInputTrustAuthority</strong></a><br/></td>
<td>Consente ad altri componenti nel percorso multimediale protetto (PMP) di usare il sistema di protezione dell'input fornito da un'autorità di attendibilità di input.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imflocalmftregistration"><strong>IMFLocalMFTRegistration</strong></a><br/></td>
<td>Registra Media Foundation trasformazioni (MFTs) nel processo del chiamante.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer"><strong>IMFMediaBuffer</strong></a><br/></td>
<td>Rappresenta un blocco di memoria che contiene dati multimediali.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengine"><strong>IMFMediaEngine</strong></a><br/></td>
<td>Consente a un'applicazione di riprodurre file audio o video.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineclassfactory"><strong>IMFMediaEngineClassFactory</strong></a><br/></td>
<td>Crea un'istanza del motore multimediale.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineclassfactory2"><strong>IMFMediaEngineClassFactory2</strong></a><br/></td>
<td>Crea un'istanza dell'oggetto <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeys"><strong>IMFMediaKeys</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineclassfactoryex"><strong>IMFMediaEngineClassFactoryEx</strong></a><br/></td>
<td>Estensione per l'interfaccia <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineclassfactory"><strong>IMFMediaEngineClassFactory</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineeme"><strong>IMFMediaEngineEME</strong></a><br/></td>
<td>Implementata dal motore multimediale per aggiungere metodi di estensioni multimediali crittografati.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineex"><strong>IMFMediaEngineEx</strong></a><br/></td>
<td>Estende l'interfaccia <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengine"><strong>IMFMediaEngine</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineextension"><strong>IMFMediaEngineExtension</strong></a><br/></td>
<td>Consente a un'applicazione di caricare le risorse multimediali nel motore multimediale.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineneedkeynotify"><strong>IMFMediaEngineNeedKeyNotify</strong></a><br/></td>
<td>Rappresenta un callback al motore multimediale per inviare notifiche ai dati della richiesta di chiave.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaenginenotify"><strong>IMFMediaEngineNotify</strong></a><br/></td>
<td>Interfaccia di callback per l'interfaccia <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengine"><strong>IMFMediaEngine</strong></a> . <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineopminfo"><strong>IMFMediaEngineOPMInfo</strong></a><br/></td>
<td>Fornisce metodi per ottenere informazioni su <a href="output-protection-manager.md">Output Protection Manager</a> (OPM).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineprotectedcontent"><strong>IMFMediaEngineProtectedContent</strong></a><br/></td>
<td>Consente al motore multimediale di riprodurre contenuti video protetti.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaenginesrcelements"><strong>IMFMediaEngineSrcElements</strong></a><br/></td>
<td>Fornisce al motore multimediale un elenco di risorse multimediali.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaenginesrcelementsex"><strong>IMFMediaEngineSrcElementsEx</strong></a><br/></td>
<td>Estende l'interfaccia <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaenginesrcelements"><strong>IMFMediaEngineSrcElements</strong></a> per fornire funzionalità aggiuntive.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaenginesupportssourcetransfer"><strong>IMFMediaEngineSupportsSourceTransfer</strong></a><br/></td>
<td>Consente il trasferimento dell'origine multimediale tra il motore multimediale e il motore di condivisione per la riproduzione in.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaenginewebsupport"><strong>IMFMediaEngineWebSupport</strong></a><br/></td>
<td>Abilita la riproduzione di audio Web.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaerror"><strong>IMFMediaError</strong></a><br/></td>
<td>Fornisce lo stato di errore corrente per il motore multimediale.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent"><strong>IMFMediaEvent</strong></a><br/></td>
<td>Rappresenta un evento generato da un oggetto Media Foundation. Usare questa interfaccia per ottenere informazioni sull'evento.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator"><strong>IMFMediaEventGenerator</strong></a><br/></td>
<td>Recupera gli eventi da qualsiasi Media Foundation oggetto che genera eventi. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventqueue"><strong>IMFMediaEventQueue</strong></a><br/></td>
<td>Fornisce una coda di eventi per le applicazioni che devono implementare l'interfaccia <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator"><strong>IMFMediaEventGenerator</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeys"><strong>IMFMediaKeys</strong></a><br/></td>
<td>Rappresenta i tasti multimediali utilizzati per la decrittografia dei dati multimediali utilizzando un sistema di chiavi digitale Rights Management (DRM). <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeysession"><strong>IMFMediaKeySession</strong></a><br/></td>
<td>Rappresenta una sessione con il sistema di chiavi Digital Rights Management (DRM).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeysessionnotify"><strong>IMFMediaKeySessionNotify</strong></a><br/></td>
<td>Fornisce un meccanismo per notificare all'app le informazioni relative alla sessione di chiavi multimediali. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasession"><strong>IMFMediaSession</strong></a><br/></td>
<td>Fornisce controlli di riproduzione per contenuto protetto e non protetto.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfsharingengine/nn-mfsharingengine-imfmediasharingengine"><strong>IMFMediaSharingEngine</strong></a><br/></td>
<td>Abilita la condivisione di contenuti multimediali.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfsharingengine/nn-mfsharingengine-imfmediasharingengineclassfactory"><strong>IMFMediaSharingEngineClassFactory</strong></a><br/></td>
<td>Crea un'istanza di <a href="/windows/desktop/api/mfsharingengine/nn-mfsharingengine-imfmediasharingengine"><strong>IMFMediaSharingEngine</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasink"><strong>IMFMediaSink</strong></a><br/></td>
<td>Implementata dagli oggetti del sink multimediale.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasinkpreroll"><strong>IMFMediaSinkPreroll</strong></a><br/></td>
<td>Consente a un sink multimediale di ricevere campioni prima dell'avvio del clock di presentazione.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasource"><strong>IMFMediaSource</strong></a><br/></td>
<td>Implementata dagli oggetti di origine del supporto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex"><strong>IMFMediaSourceEx</strong></a><br/></td>
<td>Estende l'interfaccia <a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasource"><strong>IMFMediaSource</strong></a> per fornire funzionalità aggiuntive per un'origine multimediale.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension"><strong>IMFMediaSourceExtension</strong></a><br/></td>
<td>Fornisce funzionalità per l'estensione di origine multimediale (MSE).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextensionnotify"><strong>IMFMediaSourceExtensionNotify</strong></a><br/></td>
<td>Fornisce la funzionalità per la generazione di eventi associati a <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension"><strong>IMFMediaSourceExtension</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcepresentationprovider"><strong>IMFMediaSourcePresentationProvider</strong></a><br/></td>
<td>Fornisce notifiche all'origine del sequencer.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider"><strong>IMFMediaSourceTopologyProvider</strong></a><br/></td>
<td>Consente a un'applicazione di ottenere una topologia dall'origine del sequencer.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediastream"><strong>IMFMediaStream</strong></a><br/></td>
<td>Rappresenta un flusso in un'origine multimediale. <br/></td>
</tr>
<tr class="odd">
<td><a href="imfmediastreamsourcesamplerequest.md"><strong>IMFMediaStreamSourceSampleRequest</strong></a><br/></td>
<td>Rappresenta una richiesta di un campione da un MediaStreamSource. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediatimerange"><strong>IMFMediaTimeRange</strong></a><br/></td>
<td>Rappresenta un elenco di intervalli di tempo, in cui ogni intervallo è definito da un'ora di inizio e di fine.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype"><strong>IMFMediaType</strong></a><br/></td>
<td>Rappresenta una descrizione di un formato multimediale. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler"><strong>IMFMediaTypeHandler</strong></a><br/></td>
<td>Ottiene e imposta i tipi di supporto in un oggetto, ad esempio un'origine multimediale o un sink multimediale. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfmetadata"><strong>IMFMetadata</strong></a><br/></td>
<td>Gestisce i metadati per un oggetto.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider"><strong>IMFMetadataProvider</strong></a><br/></td>
<td>Ottiene i metadati da un'origine supporto o da un altro oggetto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamattributesmanager"><strong>IMFMuxStreamAttributesManager</strong></a><br/></td>
<td>Fornisce l'accesso all' <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes"><strong>IMFAttributes</strong></a> dei flussi sottoflussi di un'origine multimediale con multiplexing.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamsamplemanager"><strong>IMFMuxStreamSampleManager</strong></a><br/></td>
<td>Consente di recuperare gli oggetti <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfsample"><strong>IMFSample</strong></a> per i singoli flussi di dati all'interno dell'output di un'origine multimediale con multiplexing.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreammediatypemanager"><strong>IMFMuxStreamMediaTypeManager</strong></a><br/></td>
<td>Consente la gestione delle configurazioni di flusso per un'origine multimediale con multiplexing. Una configurazione di flusso definisce un set di flussi sottoflussi che possono essere inclusi nell'output multiplexato.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential"><strong>IMFNetCredential</strong></a><br/></td>
<td>Imposta e recupera le informazioni relative a nome utente e password per scopi di autenticazione. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialcache"><strong>IMFNetCredentialCache</strong></a><br/></td>
<td>Ottiene le credenziali dalla cache delle credenziali.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager"><strong>IMFNetCredentialManager</strong></a><br/></td>
<td>Implementato dalle applicazioni per fornire le credenziali utente per un'origine di rete.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfnetcrossoriginsupport"><strong>IMFNetCrossOriginSupport</strong></a><br/></td>
<td>Implementata dai client che vogliono applicare un criterio tra le origini per i download di contenuti multimediali HTML5. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocator"><strong>IMFNetProxyLocator</strong></a><br/></td>
<td>Determina il proxy da utilizzare per la connessione a un server.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocatorfactory"><strong>IMFNetProxyLocatorFactory</strong></a><br/></td>
<td>Crea un oggetto localizzatore proxy, che determina il proxy da usare.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfnetresourcefilter"><strong>IMFNetResourceFilter</strong></a><br/></td>
<td>Invia una notifica all'applicazione quando un flusso di byte richiede un URL e consente all'applicazione di bloccare il reindirizzamento dell'URL.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfnetschemehandlerconfig"><strong>IMFNetSchemeHandlerConfig</strong></a><br/></td>
<td>Configura un plug-in dello schema di rete. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfobjectreferencestream"><strong>IMFObjectReferenceStream</strong></a><br/></td>
<td>Esegue il marshalling di un puntatore a interfaccia a e da un flusso. <br/> Gli oggetti flusso che supportano <strong>IStream</strong> possono esporre questa interfaccia per fornire il marshalling personalizzato per i puntatori di interfaccia.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfoutputpolicy"><strong>IMFOutputPolicy</strong></a><br/></td>
<td>Incapsula i criteri di utilizzo da un'autorità di attendibilità di input (ITA).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfoutputschema"><strong>IMFOutputSchema</strong></a><br/></td>
<td>Incapsula le informazioni su un sistema di protezione dell'output e i dati di configurazione corrispondenti.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfoutputtrustauthority"><strong>IMFOutputTrustAuthority</strong></a><br/></td>
<td>Incapsula la funzionalità di uno o più sistemi di protezione output supportati da un output attendibile.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfplugincontrol"><strong>IMFPluginControl</strong></a><br/></td>
<td>Controlla il modo in cui vengono enumerate le origini e le trasformazioni dei supporti in Media Foundation.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfplugincontrol2"><strong>IMFPluginControl2</strong></a><br/></td>
<td>Controlla il modo in cui vengono enumerate le origini e le trasformazioni dei supporti in Media Foundation.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem"><strong>IMFPMediaItem</strong></a><br/></td>
<td>Rappresenta un elemento multimediale. (Deprecata)<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer"><strong>IMFPMediaPlayer</strong></a><br/></td>
<td>Contiene i metodi per riprodurre file multimediali. (Deprecata)<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback"><strong>IMFPMediaPlayerCallback</strong></a><br/></td>
<td>Interfaccia di callback per l'interfaccia <a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer"><strong>IMFPMediaPlayer</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfpmpclient"><strong>IMFPMPClient</strong></a><br/></td>
<td>Consente a un'origine multimediale di ricevere un puntatore all'interfaccia <a href="/windows/desktop/api/mfidl/nn-mfidl-imfpmphost"><strong>IMFPMPHost</strong></a> . <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfpmpclientapp"><strong>IMFPMPClientApp</strong></a><br/></td>
<td>Fornisce un meccanismo per un'origine multimediale per implementare la funzionalità di protezione del contenuto in un'app di Windows Store.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfpmphost"><strong>IMFPMPHost</strong></a><br/></td>
<td>Consente a un'origine multimediale nel processo dell'applicazione di creare oggetti nel processo del percorso multimediale protetto (PMP).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfpmphostapp"><strong>IMFPMPHostApp</strong></a><br/></td>
<td>Consente a un'origine multimediale di creare un oggetto <a href="/windows/desktop/WinRT/reference">Windows Runtime</a> nel processo del <a href="protected-media-path.md">percorso multimediale protetto</a> (PMP). <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfpmpserver"><strong>IMFPMPServer</strong></a><br/></td>
<td>Consente a due istanze della <a href="media-session.md">sessione multimediale</a> di condividere lo stesso processo di percorso multimediale protetto (PMP). <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock"><strong>IMFPresentationClock</strong></a><br/></td>
<td>Rappresenta un orologio di presentazione, utilizzato per pianificare il rendering degli esempi e la sincronizzazione di più flussi.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor"><strong>IMFPresentationDescriptor</strong></a><br/></td>
<td>Vengono descritti i dettagli di una presentazione. Una <em>presentazione</em> è un set di flussi multimediali correlati che condividono un tempo di presentazione comune. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfpresentationtimesource"><strong>IMFPresentationTimeSource</strong></a><br/></td>
<td>Fornisce i tempi di clock per il clock di presentazione. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfprotectedenvironmentaccess"><strong>IMFProtectedEnvironmentAccess</strong></a><br/></td>
<td>Fornisce un metodo che consente ai sistemi di protezione del contenuto di eseguire un handshake con l'ambiente protetto. Questa operazione è necessaria perché le API <strong>CreateFile</strong> e <strong>DeviceIoControl</strong> non sono disponibili per le app di Windows Store.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise"><strong>IMFQualityAdvise</strong></a><br/></td>
<td>Consente al gestore della qualità di regolare la qualità audio o video di un componente nella pipeline.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2"><strong>IMFQualityAdvise2</strong></a><br/></td>
<td>Consente a un oggetto pipeline di regolare la propria qualità audio o video in risposta ai messaggi di qualità.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadviselimits"><strong>IMFQualityAdviseLimits</strong></a><br/></td>
<td>Esegue una query su un oggetto per il numero di <em>modalità di qualità</em> supportate.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualitymanager"><strong>IMFQualityManager</strong></a><br/></td>
<td>Regola la qualità della riproduzione. Questa interfaccia viene esposta dal gestore qualità. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol"><strong>IMFRateControl</strong></a><br/></td>
<td>Ottiene o imposta la velocità di riproduzione. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfratesupport"><strong>IMFRateSupport</strong></a><br/></td>
<td>Esegue una query sull'intervallo di frequenze di riproduzione supportate, inclusa la riproduzione inversa.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfreadwriteclassfactory"><strong>IMFReadWriteClassFactory</strong></a><br/></td>
<td>Crea un'istanza del writer di sink o del lettore di origine.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient"><strong>IMFRealTimeClient</strong></a><br/></td>
<td>Notifica a un oggetto pipeline di registrarsi con il servizio Utilità di pianificazione classi multimediali (MMCSS).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclientex"><strong>IMFRealTimeClientEx</strong></a><br/></td>
<td>Notifica a un oggetto pipeline di registrarsi con il servizio Utilità di pianificazione classi multimediali (MMCSS). <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfremoteasynccallback"><strong>IMFRemoteAsyncCallback</strong></a><br/></td>
<td>Usato dalla DLL Media Foundation Proxy/Stub per eseguire il marshalling di determinate chiamate di metodo asincrone tra i limiti del processo.<br/> Le applicazioni non utilizzano né implementano questa interfaccia.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfremotedesktopplugin"><strong>IMFRemoteDesktopPlugin</strong></a><br/></td>
<td>Modifica una topologia da utilizzare in un ambiente Servizi terminal. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfremoteproxy"><strong>IMFRemoteProxy</strong></a><br/></td>
<td>Esposto da oggetti che fungono da proxy per un oggetto remoto.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsamistyle"><strong>IMFSAMIStyle</strong></a><br/></td>
<td>Imposta e recupera gli stili di interscambio multimediale (SAMI) sincronizzati sull' <a href="sami-media-source.md">origine dei supporti Sami</a>. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfsample"><strong>IMFSample</strong></a><br/></td>
<td>Rappresenta un esempio multimediale, ovvero un oggetto contenitore per i dati multimediali.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsamplegrabbersinkcallback"><strong>IMFSampleGrabberSinkCallback</strong></a><br/></td>
<td>Interfaccia di callback per ottenere i dati multimediali dal sink Sample-Grabber. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsamplegrabbersinkcallback2"><strong>IMFSampleGrabberSinkCallback2</strong></a><br/></td>
<td>Estende l'interfaccia <a href="/windows/desktop/api/mfidl/nn-mfidl-imfsamplegrabbersinkcallback"><strong>IMFSampleGrabberSinkCallback</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfsampleoutputstream"><strong>IMFSampleOutputStream</strong></a><br/></td>
<td>Scrive esempi di supporti in un flusso di byte.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsampleprotection"><strong>IMFSampleProtection</strong></a><br/></td>
<td>Fornisce la crittografia per i dati multimediali all'interno del percorso multimediale protetto (PMP). <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsavejob"><strong>IMFSaveJob</strong></a><br/></td>
<td>Salva in modo permanente i dati multimediali da un flusso di byte di origine a un flusso di byte fornito dall'applicazione.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfschemehandler"><strong>IMFSchemeHandler</strong></a><br/></td>
<td>Crea un'origine multimediale o un flusso di byte da un URL. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsecurechannel"><strong>IMFSecureChannel</strong></a><br/></td>
<td>Stabilisce un canale protetto unidirezionale tra due oggetti. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfseekinfo"><strong>IMFSeekInfo</strong></a><br/></td>
<td>Per una particolare posizione di ricerca, ottiene i due fotogrammi chiave più vicini.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensoractivitiesreport"><strong>IMFSensorActivitiesReport</strong></a><br/></td>
<td>Fornisce l'accesso agli oggetti <a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensoractivityreport"><strong>IMFSensorActivityReport</strong></a> che descrivono l'attività corrente di un sensore.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensoractivitiesreportcallback"><strong>IMFSensorActivitiesReportCallback</strong></a><br/></td>
<td>Interfaccia implementata dal client per ricevere callback quando sono disponibili report sulle attività dei sensori.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensoractivitymonitor"><strong>IMFSensorActivityMonitor</strong></a><br/></td>
<td>Fornisce metodi per il controllo di un monitoraggio attività del sensore.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensoractivityreport"><strong>IMFSensorActivityReport</strong></a><br/></td>
<td>Rappresenta un report di attività per un sensore.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensordevice"><strong>IMFSensorDevice</strong></a><br/></td>
<td>Rappresenta un dispositivo sensore che può appartenere a un gruppo di sensori, rappresentato dall'interfaccia <a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensorgroup"><strong>IMFSensorGroup</strong></a> . Il termine &quot; dispositivo &quot; in questo contesto può fare riferimento a un dispositivo fisico, a un'origine multimediale personalizzata o a un provider di frame.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensorgroup"><strong>IMFSensorGroup</strong></a><br/></td>
<td>Rappresenta un gruppo di dispositivi sensore da cui è possibile creare un <a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasource"><strong>IMFMediaSource</strong></a> . Il termine &quot; dispositivo &quot; in questo contesto può fare riferimento a un dispositivo fisico, a un'origine multimediale personalizzata o a un provider di frame. Un gruppo di sensori può effettivamente contenere più dispositivi sensore o contenere solo un singolo dispositivo, ma si comporta comunque come un gruppo di sensori.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensorprocessactivity"><strong>IMFSensorProcessActivity</strong></a><br/></td>
<td>Rappresenta l'attività di un processo associato a un sensore.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensorprofilecollection"><strong>IMFSensorProfileCollection</strong></a><br/></td>
<td>Contiene una raccolta di oggetti profilo del sensore di Media Foundation.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensorprofile"><strong>IMFSensorProfile</strong></a><br/></td>
<td>Descrive un profilo del sensore di Media Foundation.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensorstream"><strong>IMFSensorStream</strong></a><br/></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensortransformfactory"><strong>IMFSensorTransformFactory</strong></a><br/></td>
<td>Interfaccia implementata da trasformazioni dei sensori per consentire alla pipeline multimediale di eseguire query sui requisiti della trasformazione del sensore e di creare un'istanza di runtime della trasformazione del sensore.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource"><strong>IMFSequencerSource</strong></a><br/></td>
<td>Implementata dall' <a href="sequencer-source.md">origine del sequencer</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfsharingengine/nn-mfsharingengine-imfsharingengineclassfactory"><strong>IMFSharingEngineClassFactory</strong></a><br/></td>
<td>Crea un'istanza del motore di condivisione multimediale.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfshutdown"><strong>IMFShutdown</strong></a><br/></td>
<td>Esposto da alcuni oggetti Media Foundation che devono essere arrestati in modo esplicito. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsignedlibrary"><strong>IMFSignedLibrary</strong></a><br/></td>
<td>Fornisce un metodo che consente ai sistemi di protezione del contenuto di ottenere l'indirizzo della procedura di una funzione nella libreria firmata. Questo metodo offre la stessa funzionalità di <strong>GetProcAddress</strong> , che non è disponibile per le app di Windows Store.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsimpleaudiovolume"><strong>IMFSimpleAudioVolume</strong></a><br/></td>
<td>Controlla il livello del volume master della sessione audio associata al renderer di streaming audio (SAR) e all'origine di acquisizione audio.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriter"><strong>IMFSinkWriter</strong></a><br/></td>
<td>Implementato dall'oggetto writer del sink di Media Foundation.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwritercallback"><strong>IMFSinkWriterCallback</strong></a><br/></td>
<td>Interfaccia di callback per il writer di sink Media Foundation. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwritercallback2"><strong>IMFSinkWriterCallback2</strong></a><br/></td>
<td>Estende l'interfaccia <a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwritercallback"><strong>IMFSinkWriterCallback</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriterencoderconfig"><strong>IMFSinkWriterEncoderConfig</strong></a><br/></td>
<td>Fornisce funzionalità aggiuntive sul writer di sink per la modifica dinamica del tipo di supporto e della configurazione del codificatore. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriterex"><strong>IMFSinkWriterEx</strong></a><br/></td>
<td>Estende l'interfaccia <a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriter"><strong>IMFSinkWriter</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer"><strong>IMFSourceBuffer</strong></a><br/></td>
<td>Rappresenta un buffer che contiene i dati multimediali per un <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension"><strong>IMFMediaSourceExtension</strong></a>. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebufferlist"><strong>IMFSourceBufferList</strong></a><br/></td>
<td>Rappresenta una raccolta di oggetti <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer"><strong>IMFSourceBuffer</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffernotify"><strong>IMFSourceBufferNotify</strong></a><br/></td>
<td>Fornisce la funzionalità per la generazione di eventi associati a <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer"><strong>IMFSourceBuffer</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor"><strong>IMFSourceOpenMonitor</strong></a><br/></td>
<td>Interfaccia di callback per ricevere notifiche da un'origine di rete sullo stato di avanzamento di un'operazione di apertura asincrona.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader"><strong>IMFSourceReader</strong></a><br/></td>
<td>Implementato dal Media Foundation oggetto Reader di origine.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereadercallback"><strong>IMFSourceReaderCallback</strong></a><br/></td>
<td>Interfaccia di callback per il lettore di origine Media Foundation.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereadercallback2"><strong>IMFSourceReaderCallback2</strong></a><br/></td>
<td>Estende l'interfaccia <a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereadercallback"><strong>IMFSourceReaderCallback</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereaderex"><strong>IMFSourceReaderEx</strong></a><br/></td>
<td>Estende l'interfaccia <a href="/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader"><strong>IMFSourceReader</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver"><strong>IMFSourceResolver</strong></a><br/></td>
<td>Crea un'origine multimediale da un URL o un flusso di byte.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfspatialaudio/nn-mfspatialaudio-imfspatialaudioobjectbuffer"><strong>IMFSpatialAudioObjectBuffer</strong></a><br/></td>
<td>Rappresenta una sezione di dati audio con i metadati posizionali e di rendering associati. Gli oggetti audio spaziali vengono archiviati in istanze <a href="/windows/desktop/api/mfspatialaudio/nn-mfspatialaudio-imfspatialaudiosample"><strong>IMFSpatialAudioSample</strong></a> e consentono il passaggio di informazioni audio spaziali tra Media Foundation componenti.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfspatialaudio/nn-mfspatialaudio-imfspatialaudiosample"><strong>IMFSpatialAudioSample</strong></a><br/></td>
<td>Rappresenta un esempio multimediale con informazioni sul suono spaziale. Ogni <a href="/windows/desktop/api/mfspatialaudio/nn-mfspatialaudio-imfspatialaudiosample"><strong>IMFSpatialAudioSample</strong></a> contiene uno o più oggetti <a href="/windows/desktop/api/mfspatialaudio/nn-mfspatialaudio-imfspatialaudioobjectbuffer"><strong>IMFSpatialAudioObjectBuffer</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsslcertificatemanager"><strong>IMFSSLCertificateManager</strong></a><br/></td>
<td>Implementato da un client e chiamato da Media Foundation per ottenere il certificato client Secure Sockets Layer (SSL) richiesto dal server. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor"><strong>IMFStreamDescriptor</strong></a><br/></td>
<td>Ottiene informazioni su un flusso in un'origine multimediale. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfstreamingsinkconfig"><strong>IMFStreamingSinkConfig</strong></a><br/></td>
<td>Passa le informazioni di configurazione ai sink multimediali utilizzati per lo streaming del contenuto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink"><strong>IMFStreamSink</strong></a><br/></td>
<td>Rappresenta un flusso in un oggetto sink multimediale.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfsystemid"><strong>IMFSystemId</strong></a><br/></td>
<td>Fornisce un metodo che retireves i dati degli ID di sistema.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imftimecodetranslate"><strong>IMFTimecodeTranslate</strong></a><br/></td>
<td>Esegue la conversione tra i codici temporali SMPTE (Society of Motion Picture e Television Engineers) e le unità di tempo di 100 nanosecondi.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtext"><strong>IMFTimedText</strong></a><br/></td>
<td>Un oggetto con testo temporizzato rappresenta un componente del testo temporizzato.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtextbinary"><strong>IMFTimedTextBinary</strong></a><br/></td>
<td>Rappresenta il contenuto dei dati di un oggetto di testo temporizzato.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtextcue"><strong>IMFTimedTextCue</strong></a><br/></td>
<td>Rappresenta l'oggetto temporizzato del cue di testo. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtextformattedtext"><strong>IMFTimedTextFormattedText</strong></a><br/></td>
<td>Rappresenta un blocco di testo temporizzato formattato.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtextnotify"><strong>IMFTimedTextNotify</strong></a><br/></td>
<td>Interfaccia che definisce i callback per Media Foundation notifiche di testo temporizzato.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtextregion"><strong>IMFTimedTextRegion</strong></a><br/></td>
<td>Rappresenta l'area di visualizzazione di un oggetto di testo temporizzato.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtextstyle"><strong>IMFTimedTextStyle</strong></a><br/></td>
<td>Rappresenta lo stile per il testo temporizzato.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtexttrack"><strong>IMFTimedTextTrack</strong></a><br/></td>
<td>Rappresenta una traccia del testo temporizzato.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imftimedtexttracklist"><strong>IMFTimedTextTrackList</strong></a><br/></td>
<td>Rappresenta un elenco di tracce di testo temporizzato.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imftimer"><strong>IMFTimer</strong></a><br/></td>
<td>Fornisce un timer che richiama un callback a un'ora specificata.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imftopoloader"><strong>IMFTopoLoader</strong></a><br/></td>
<td>Converte una topologia parziale in una topologia completa.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imftopology"><strong>IMFTopology</strong></a><br/></td>
<td>Rappresenta una topologia. Una <em>topologia</em> descrive una raccolta di origini multimediali, sink e trasformazioni connesse in un determinato ordine.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imftopologynode"><strong>IMFTopologyNode</strong></a><br/></td>
<td>Rappresenta un nodo in una topologia.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imftopologynodeattributeeditor"><strong>IMFTopologyNodeAttributeEditor</strong></a><br/></td>
<td>Aggiorna gli attributi di uno o più nodi nella topologia corrente della sessione multimediale.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/evr/nn-evr-imftopologyservicelookup"><strong>IMFTopologyServiceLookup</strong></a><br/></td>
<td>Consente a un mixer video o un presentatore video personalizzato di ottenere i puntatori di interfaccia dal <a href="enhanced-video-renderer.md">renderer video avanzato</a> (EVR).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient"><strong>IMFTopologyServiceLookupClient</strong></a><br/></td>
<td>Inizializza un mixer video o un presentatore.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imftrackedsample"><strong>IMFTrackedSample</strong></a><br/></td>
<td>Tiene traccia dei conteggi dei riferimenti in un file multimediale di esempio.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imftranscodeprofile"><strong>IMFTranscodeProfile</strong></a><br/></td>
<td>Implementato dall'oggetto profilo transcodifica.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imftranscodesinkinfoprovider"><strong>IMFTranscodeSinkInfoProvider</strong></a><br/></td>
<td>Implementato dall'oggetto di attivazione del sink di transcodifica.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mftransform/nn-mftransform-imftransform"><strong>IMFTransform</strong></a><br/></td>
<td>Implementata da tutte le <a href="media-foundation-transforms.md">trasformazioni di Media Foundation</a> (MFTS).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imftrustedinput"><strong>IMFTrustedInput</strong></a><br/></td>
<td>Implementata da componenti che forniscono autorità di attendibilità di input (ITAs). Questa interfaccia viene usata per ottenere l'ITA per ogni flusso del componente. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imftrustedoutput"><strong>IMFTrustedOutput</strong></a><br/></td>
<td>Implementata da componenti che forniscono autorità di attendibilità di output (OTA).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/evr/nn-evr-imfvideodeviceid"><strong>IMFVideoDeviceID</strong></a><br/></td>
<td>Restituisce l'identificatore del dispositivo supportato da un componente renderer video.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol"><strong>IMFVideoDisplayControl</strong></a><br/></td>
<td>Controlla il modo in cui il <a href="enhanced-video-renderer.md">renderer video avanzato</a> (EVR) Visualizza il video.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfvideomediatype"><strong>IMFVideoMediaType</strong></a><br/></td>
<td>Rappresenta una descrizione di un formato video.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/evr9/nn-evr9-imfvideomixerbitmap"><strong>IMFVideoMixerBitmap</strong></a><br/></td>
<td>Alfa-fonde un'immagine bitmap statica con il video visualizzato dal <a href="enhanced-video-renderer.md">renderer video avanzato</a> (EVR).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/evr/nn-evr-imfvideomixercontrol"><strong>IMFVideoMixerControl</strong></a><br/></td>
<td>Controlla il modo in cui il <a href="enhanced-video-renderer.md">renderer video avanzato</a> (EVR) combina i sottoflussi video.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/evr/nn-evr-imfvideomixercontrol2"><strong>IMFVideoMixerControl2</strong></a><br/></td>
<td>Controlla le preferenze per la deinterlacciamento dei video.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/evr/nn-evr-imfvideopositionmapper"><strong>IMFVideoPositionMapper</strong></a><br/></td>
<td>Esegue il mapping di una posizione in un flusso video di input alla posizione corrispondente in un flusso video di output.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/evr/nn-evr-imfvideopresenter"><strong>IMFVideoPresenter</strong></a><br/></td>
<td>Rappresenta un presentatore video. Un <em>presentatore video</em> è un oggetto che riceve i frame video, in genere da un mixer video, e li presenta in qualche modo, in genere eseguendone il rendering sullo schermo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor"><strong>IMFVideoProcessor</strong></a><br/></td>
<td>Controlla l'elaborazione video nel <a href="enhanced-video-renderer.md">renderer video avanzato</a> (EVR).<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfvideoprocessorcontrol"><strong>IMFVideoProcessorControl</strong></a><br/></td>
<td>Configura il <a href="video-processor-mft.md"><strong>processore video MFT</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfvideoprocessorcontrol2"><strong>IMFVideoProcessorControl2</strong></a><br/></td>
<td>Configura il <a href="video-processor-mft.md"><strong>processore video MFT</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/evr/nn-evr-imfvideorenderer"><strong>IMFVideoRenderer</strong></a><br/></td>
<td>Imposta un nuovo mixer o Presenter per il <a href="enhanced-video-renderer.md">renderer video avanzato</a> (EVR).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocator"><strong>IMFVideoSampleAllocator</strong></a><br/></td>
<td>Alloca esempi video per un sink di supporti video.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorcallback"><strong>IMFVideoSampleAllocatorCallback</strong></a><br/></td>
<td>Consente a un'applicazione di tenere traccia dei campioni video allocati dal renderer video avanzato (EVR).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorex"><strong>IMFVideoSampleAllocatorEx</strong></a><br/></td>
<td>Alloca esempi video contenenti superfici di trama Direct3D 11.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatornotify"><strong>IMFVideoSampleAllocatorNotify</strong></a><br/></td>
<td>Callback per l'interfaccia <a href="/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorcallback"><strong>IMFVideoSampleAllocatorCallback</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatornotifyex"><strong>IMFVideoSampleAllocatorNotifyEx</strong></a><br/></td>
<td>Callback per l'interfaccia <a href="/windows/desktop/api/mfidl/nn-mfidl-imfvideosampleallocatorcallback"><strong>IMFVideoSampleAllocatorCallback</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices"><strong>IMFWorkQueueServices</strong></a><br/></td>
<td>Controlla le code di lavoro create dalla <a href="media-session.md">sessione multimediale</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservicesex"><strong>IMFWorkQueueServicesEx</strong></a><br/></td>
<td>Estende l'interfaccia <a href="/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices"><strong>IMFWorkQueueServices</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfsharingengine/nn-mfsharingengine-iplaytocontrol"><strong>IPlayToControl</strong></a><br/></td>
<td>Consente all'oggetto <strong>playToConnection</strong> di connettersi a un elemento multimediale.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfsharingengine/nn-mfsharingengine-iplaytocontrolwithcapabilities"><strong>IPlayToControlWithCapabilities</strong></a><br/></td>
<td>Fornisce la funzionalità per <a href="/windows/desktop/api/mfsharingengine/nn-mfsharingengine-iplaytosourceclassfactory"><strong>IPlayToSource</strong></a> per determinare le funzionalità del contenuto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfsharingengine/nn-mfsharingengine-iplaytosourceclassfactory"><strong>IPlayToSourceClassFactory</strong></a><br/></td>
<td>Crea un'istanza dell'oggetto <a href="/uwp/api/Windows.Media.PlayTo.PlayToSource"><strong>PlayToSource</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecleakybucket"><strong>IWMCodecLeakyBucket</strong></a><br/></td>
<td>Configura i &quot; parametri del bucket &quot; a perdita in un codificatore video.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecoutputtimestamp"><strong>IWMCodecOutputTimestamp</strong></a><br/></td>
<td>Ottiene il timestamp del fotogramma video successivo da decodificare.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecprivatedata"><strong>IWMCodecPrivateData</strong></a><br/></td>
<td>Ottiene i dati del codec privato che devono essere accodati al tipo di supporto di output. Questi dati del codec sono necessari per la decodifica corretta del contenuto Windows Media Video.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecprops"><strong>IWMCodecProps</strong></a><br/></td>
<td>Fornisce metodi che recuperano le proprietà del codec specifiche del formato.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecstrings"><strong>IWMCodecStrings</strong></a><br/></td>
<td>Recupera i nomi e le stringhe descrittive per codec e formati.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcolorconvprops"><strong>IWMColorConvProps</strong></a><br/></td>
<td>Imposta le proprietà per il convertitore di colori DSP. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmresamplerprops"><strong>IWMResamplerProps</strong></a><br/></td>
<td>Imposta le proprietà nel DSP del ricampionatore audio. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmresizerprops"><strong>IWMResizerProps</strong></a><br/></td>
<td>Imposta le proprietà nel DSP video Resizer.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmsampleextensionsupport"><strong>IWMSampleExtensionSupport</strong></a><br/></td>
<td>Configura il supporto dei codec per le estensioni di esempio. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmvideodecoderhurryup"><strong>IWMVideoDecoderHurryup</strong></a><br/></td>
<td>Controlla la velocità del decodificatore video.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmvideodecoderreconbuffer"><strong>IWMVideoDecoderReconBuffer</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Questa interfaccia è obsoleta e non deve essere utilizzata.
</blockquote>
<br/> Gestisce i fotogrammi video ricostruiti.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmvideoforcekeyframe"><strong>IWMVideoForceKeyFrame</strong></a><br/></td>
<td>Impone al codificatore di codificare il frame corrente come fotogramma chiave. <br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida di riferimento alla programmazione di Media Foundation](media-foundation-programming-reference.md)
</dt> </dl>

 

 
