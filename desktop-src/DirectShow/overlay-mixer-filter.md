---
description: Filtro Overlay Mixer
ms.assetid: e80938b7-31f0-467b-a3fa-c4511d14758d
title: Filtro Overlay Mixer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 475726607f282ce4b7885ec6c5aea562c0380cb0
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476987"
---
# <a name="overlay-mixer-filter"></a>Filtro Overlay Mixer

Il filtro Overlay Mixer è un renderer video progettato specificamente per la riproduzione di DVD e la trasmissione di flussi video con sottotitoli codificati line-21. Overlay Mixer supporta anche le estensioni di porta video (VPE), consentendone l'uso con decodificatori MPEG-2 hardware o silezionatori TV analogici che inviano video direttamente alla scheda grafica, anziché tramite il bus PCI.

> [!Note]  
> Il [renderer di combinazione video 9](video-mixing-renderer-filter-9.md) è ora preferibile rispetto al filtro Mixer sovrapposizione, ad eccezione degli scenari di VPE.

 

Il controllo Overlay Mixer DirectDraw per il rendering. Richiede una superficie di sovrapposizione sulla scheda grafica. Il flusso video primario deve essere connesso al pin 0. I flussi secondari (immagini di sottotitoli codificati o immagini secondarie DVD) sono connessi ai segnaposto 1 e versioni successive. La sovrimpressione Mixer i flussi secondari direttamente sulla superficie primaria; non vengono combinate o combinate con alfa.

L'Mixer overlay usa il renderer video per la gestione delle finestre. Il renderer video si connette al segnaposto di output Mixer overlay.

Questo filtro viene aggiunto automaticamente al grafico dei filtri quando le applicazioni usano le interfacce [**IDvdGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-idvdgraphbuilder) e [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) per creare il grafico. Gestione filtri Graph non aggiungerà automaticamente la Mixer sovrapposizione al grafico.

> [!Note]  
> Nella tabella seguente i sottotipi di supporti accettati sul pin di input 0 dipendono dall'hardware. La proprietà Overlay Mixer determinare se un sottotipo specifico è supportato fino a quando non crea la superficie DirectDraw. Pertanto, l'unico modo per un filtro upstream per determinare se un sottotipo è supportato è tentare una connessione con tale sottotipo.

 




| | | Filtrare le interfacce | <a href="/windows/desktop/api/Strmif/nn-strmif-iamoverlayfx"><strong>IAMOverlayFX,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iamvideodecimationproperties"><strong>IAMVideoDecimationProperties,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideo"><strong>IDDrawExclModeVideo,</strong></a> <a href="ikspropertyset.md"><strong>IKsPropertySet,</strong></a> <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking,</strong></a> <a href="/previous-versions/windows/desktop/api/Mixerocx/nn-mixerocx-imixerocx"><strong>IMixerOCX,</strong></a> <a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp,</strong></a> <a href="/previous-versions/windows/desktop/api/Vpnotify/nn-vpnotify-ivpnotify"><strong>IVPNotify,</strong></a> <a href="/previous-versions/windows/desktop/api/vpnotify/nn-vpnotify-ivpnotify2"><strong>IVPNotify2</strong></a> | | Tipi di supporti pin di input | Tipo principale: MEDIATYPE_Video<br /> Sottotipi:<br /><ul><li>MEDIASUBTYPE_Overlay (solo pin 0)</li><li>Formati YUV DirectDraw (solo pin 0)</li><li>Formati di accelerazione video DirectDraw (solo pin 0)</li><li>Formati RGB DirectDraw (tutti i pin di input)</li></ul>Tipi di formato:<br /><ul><li>Format_VIDEOINFO</li><li>Format_VIDEOINFO2</li></ul> | | Interfacce pin di input | <a href="/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator"><strong>IAMVideoAccelerator,</strong></a> <a href="ikspin.md"><strong>IKsPin,</strong></a> <a href="ikspropertyset.md"><strong>IKsPropertySet,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin,</strong></a> <a href="/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig"><strong>IMixerPinConfig,</strong></a> <a href="/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2"><strong>IMixerPinConfig2,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ioverlay"><strong>IOverlay</strong></a> (solo pin 0), <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl,</strong></a> <a href="/previous-versions/windows/desktop/api/Vpnotify/nn-vpnotify-ivpnotify"><strong>IVPNotify,</strong></a> <a href="/previous-versions/windows/desktop/api/vpnotify/nn-vpnotify-ivpnotify2"><strong>IVPNotify2</strong></a> | | Tipi di supporti pin di output | MEDIATYPE_Video, MEDIASUBTYPE_Overlay | | Interfacce pin di output | <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | Filtrare i | CLSID CLSID_OverlayMixer | | ClSID della pagina delle proprietà | Nessuna pagina delle proprietà. | | File eseguibile | qdvd.dll | | <a href="merit.md">Merito</a> | MERIT_DO_NOT_USE | | <a href="filter-categories.md">Filtro categoria</a> | CLSID_LegacyAmFilterCategory | 




 

### <a name="remarks"></a>Commenti

L'Mixer di sovrimpressione usa la chiave di colore di destinazione per combinare le superfici video con le sovrimpressione. Invia la chiave di colore e il video secondario alla superficie primaria e invia il video primario alla superficie di sovrapposizione. La scheda grafica quindi composita le due superfici nel buffer dei frame.

Per verificare se il driver di grafica supporta la sovrapposizione hardware, chiamare **IDirectDraw7::GetCaps**. Se il **campo dwMaxVisibleOverlays** nella struttura **DDCAPS** è maggiore di zero, il driver supporta la sovrapposizione hardware.

Le applicazioni possono controllare alcuni comportamenti nell'Mixer overlay tramite [**l'interfaccia IMixerPinConfig2.**](/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2) Gli sviluppatori di giochi possono usare il Mixer overlay per visualizzare il video in modalità esclusiva DirectDraw, come descritto più avanti in questa sezione. Il [filtro renderer di combinazione](video-mixing-renderer-filter-9.md) video 9 (VMR-9) offre ora un supporto migliore per i video nei giochi. Per altre informazioni, vedere [Uso del renderer di combinazione video](using-the-video-mixing-renderer.md).

Le informazioni seguenti vengono fornite a vantaggio degli sviluppatori di filtri e degli sviluppatori di giochi che vogliono usare l'Mixer overlay in modalità esclusiva DirectDraw.

**Sovrimpressione Mixer operazioni interne**

La proprietà Overlay Mixer un pin di input per ogni flusso in ingresso. In genere, sono presenti tre pin di input: il pin 0 per i dati video e i pin 1 e 2 per i dati delle immagini secondarie della riga 21 e DVD. Internamente, il Mixer Overlay crea un oggetto DirectDraw con una superficie primaria che comprende l'intero desktop, oltre a una superficie di sovrapposizione il cui rettangolo è definito dalle dimensioni del flusso video sul Pin 0. Se il decodificatore non specifica una chiave di colore, il Mixer di sovrapposizione usa chiavi di colore predefinite: grigio scuro per le schede grafiche più recenti e magenta per le schede di 256 colori precedenti.

> [!Note]  
> I risultati non sono definiti se il decodificatore fornisce due flussi video secondari contemporaneamente nella stessa posizione sulla superficie di sovrapposizione. Questa situazione si verifica in alcuni casi con DVD contenenti immagini secondarie e flussi di riga 21. Il video potrebbe sfarfallio o visualizzare solo uno dei flussi.

 

In Windows Vista o versioni successive, l'Mixer overlay disabilita la composizione Gestione finestre desktop (DWM) se il driver di visualizzazione supporta la sovrapposizione hardware. Le applicazioni devono evitare l'uso del Mixer overlay. usare invece VMR-9 o Enhanced Video Renderer (EVR).

**Connessione upstream con il decodificatore video**

In genere, Mixer pin di input di Overlay si connettono a un decodificatore video upstream. Il flusso video primario deve connettersi al pin 0. I flussi della riga 21 o dell'immagine secondaria si connettono al pin 1 o versione successiva. Se il decodificatore è un decodificatore software che usa esclusivamente la CPU host, la connessione tra il decodificatore e il Pin 0 è una [**connessione IMemInputPin.**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) Se il decodificatore usa l'accelerazione hardware, la connessione al Pin 0 deve usare l'inferenza [**IAMVideoAccelerator.**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) Questi due tipi di connessioni si escludono a vicenda.

Se il decodificatore disegna direttamente sulla superficie di sovrapposizione, deve usare [**l'interfaccia IOverlay**](/windows/desktop/api/Strmif/nn-strmif-ioverlay) sul pin 0 e implementare [**l'interfaccia IOverlayNotify.**](/windows/desktop/api/Strmif/nn-strmif-ioverlaynotify)

I filtri che esegono il wrapping di un decodificatore hardware e si connettono al Mixer overlay tramite una porta video devono implementare [**l'interfaccia IVPConfig.**](/previous-versions/windows/desktop/api/Vpconfig/nn-vpconfig-ivpconfig) L'Mixer sovrimpressione implementa [**l'interfaccia IVPNotify.**](/previous-versions/windows/desktop/api/Vpnotify/nn-vpnotify-ivpnotify) Queste due interfacce consentono al decodificatore di specificare le superfici di sovrapposizione necessarie e consentono al Mixer di sovrapposizione di informare il decodificatore della posizione di tali superfici nella memoria video.

L'Mixer sovrimpressione garantisce anche che il rettangolo video venga ridimensionato correttamente. L'acquisizione di video comporta alcuni problemi relativi al ridimensionamento dell'immagine di anteprima e all'acquisizione di fotogrammi video interleaved. Se si sviluppa un filtro o un driver WDM per un dispositivo di acquisizione video hardware, fare riferimento alle pagine di riferimento [**DIVPConfig**](/previous-versions/windows/desktop/api/Vpconfig/nn-vpconfig-ivpconfig) e [**IVPNotify**](/previous-versions/windows/desktop/api/Vpnotify/nn-vpnotify-ivpnotify) per altre informazioni su questi argomenti.

L'Mixer overlay non viene usato negli scenari di acquisizione USB o 1394. Viene usato nell'acquisizione video sul bus PCI.

**Connessione downstream con il renderer video**

L'Mixer sovrimpressione ha un segnaposto di output che si connette al filtro [renderer](video-renderer-filter.md) video. Il renderer video in questo caso non esegue il rendering del video. gestisce semplicemente la finestra video.

La connessione pin usa [**l'interfaccia IOverlay**](/windows/desktop/api/Strmif/nn-strmif-ioverlay) anziché [**l'interfaccia IMemInputPin.**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) Il renderer video passa l'handle della finestra tramite il Mixer overlay a DirectDraw, che gestisce il ritaglio del rettangolo. Le applicazioni possono controllare il renderer video tramite [**le interfacce IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) e [**IBasicVideo2**](/windows/desktop/api/Control/nn-control-ibasicvideo2) in Filter Graph Manager.

**Modalità esclusiva DirectDraw**

La modalità Mixer DirectDraw di Overlay consente ai giochi di visualizzare video in una parte dello schermo. In questa modalità, il Mixer overlay esegue il rendering del video direttamente su una superficie DirectDraw creata dall'applicazione di gioco, anziché in una finestra fornita dal renderer video. Ciò consente ai giochi di controllare la chiave di colore. L'Mixer overlay espone un solo pin di input in modalità esclusiva DirectDraw, il che significa che non è possibile combinare immagini secondarie della riga 21 o DVD in questa modalità.

Per usare l'Mixer Overlay in modalità esclusiva DirectDraw, creare un'istanza del Mixer overlay ed eseguire una query per l'interfaccia [**IDDrawExclModeVideo**](/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideo) prima di compilare il grafico dei filtri. Chiamare quindi [**IDDrawExclModeVideo::SetDDrawSurface**](/windows/desktop/api/Strmif/nf-strmif-iddrawexclmodevideo-setddrawsurface) per specificare la superficie DirectDraw per il rendering. Una limitazione significativa di questa modalità è che il gioco non ottiene l'accesso ai bit video effettivi. Se si usa **IDDrawExclModeVideo,** l'applicazione crea la superficie primaria e l'Mixer overlay crea la superficie di sovrapposizione.

È anche possibile usare la modalità esclusiva DirectDraw per eseguire il rendering senza finestra, ad esempio in una pagina Web, ma non è consigliabile, perché il Mixer di sovrapposizione non esegue alcuna combinazione in questa modalità. Ciò significa che non è possibile visualizzare dati della riga 21 o dell'immagine secondaria.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectShow Filtri](directshow-filters.md)
</dt> </dl>

 

 




