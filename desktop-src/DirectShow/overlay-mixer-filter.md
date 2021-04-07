---
description: Filtro Overlay Mixer
ms.assetid: e80938b7-31f0-467b-a3fa-c4511d14758d
title: Filtro Overlay Mixer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d26ad8ba8a41a1cdb94eec0f4406c4845f25cda5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103875973"
---
# <a name="overlay-mixer-filter"></a>Filtro Overlay Mixer

Il filtro overlay mixer è un renderer video progettato in modo specifico per la riproduzione DVD e la trasmissione di flussi video con didascalie chiuse a linee 21. Il mixer overlay supporta anche VPEs (video Port Extensions), consentendo l'uso di decodificatori MPEG-2 hardware o sintonizzatori TV analoghi che inviano video direttamente alla scheda grafica, anziché sul bus PCI.

> [!Note]  
> Il [renderer 9 di mixaggio video](video-mixing-renderer-filter-9.md) è ora preferito sul filtro del mixer sovrapposto, eccetto negli scenari VPE.

 

Il mixer overlay USA DirectDraw per il rendering. Richiede una superficie sovrapposta sulla scheda grafica. Il flusso video primario deve essere connesso al pin 0. I flussi secondari (grafica didascalia chiusa o immagini secondarie DVD) sono connessi ai pin 1 e versioni successive. Il mixer overlay Blits i flussi secondari direttamente nel suface primario; non vengono combinate o combinate in modo alfa.

Il mixer overlay usa il renderer video per gestione finestre. Il renderer video si connette al pin di output del mixer overlay.

Questo filtro viene aggiunto automaticamente al grafico filtro quando le applicazioni utilizzano le interfacce [**IDvdGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-idvdgraphbuilder) e [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) per creare il grafico. Il gestore del grafico del filtro non aggiungerà automaticamente il mixer della sovrimpressione al grafico.

> [!Note]  
> Nella tabella seguente, i sottotipi di supporto accettati nel pin di input 0 sono dipendenti dall'hardware. Il mixer sovrapposto non è in grado di determinare se un sottotipo specifico è supportato fino a quando non viene creata la superficie DirectDraw. Pertanto, l'unico modo per un filtro upstream per determinare se un sottotipo è supportato consiste nel tentare una connessione con tale sottotipo.

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Interfacce di filtro</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iamoverlayfx"><strong>IAMOverlayFX</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamvideodecimationproperties"><strong>IAMVideoDecimationProperties</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideo"><strong>IDDrawExclModeVideo</strong></a>, <a href="ikspropertyset.md"><strong>IKsPropertySet</strong></a>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/previous-versions/windows/desktop/api/Mixerocx/nn-mixerocx-imixerocx"><strong>IMixerOCX</strong></a>, <a href="/previous-versions/windows/desktop/api/Amvideo/nn-amvideo-iqualprop"><strong>IQualProp</strong></a>, <a href="/previous-versions/windows/desktop/api/Vpnotify/nn-vpnotify-ivpnotify"><strong>IVPNotify</strong></a>, <a href="/previous-versions/windows/desktop/api/vpnotify/nn-vpnotify-ivpnotify2"><strong>IVPNotify2</strong></a></td>
</tr>
<tr class="even">
<td>Tipi di supporti pin di input</td>
<td>Tipo principale: MEDIATYPE_Video<br/> Sottotipi<br/>
<ul>
<li>MEDIASUBTYPE_Overlay (solo pin 0)</li>
<li>Formati YUV DirectDraw (solo pin 0)</li>
<li>Formati di accelerazione video DirectDraw (solo pin 0)</li>
<li>Formati RGB di DirectDraw (tutti i pin di input)</li>
</ul>
Tipi di formato:<br/>
<ul>
<li>Format_VIDEOINFO</li>
<li>Format_VIDEOINFO2</li>
</ul></td>
</tr>
<tr class="odd">
<td>Interfacce pin di input</td>
<td><a href="/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator"><strong>IAMVideoAccelerator</strong></a>, <a href="ikspin.md"><strong>IKsPin</strong></a>, <a href="ikspropertyset.md"><strong>IKsPropertySet</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig"><strong>IMixerPinConfig</strong></a>, <a href="/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2"><strong>IMixerPinConfig2</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ioverlay"><strong>iOverlay</strong></a> (solo pin 0), <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ipin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipinconnection"><strong>IPinConnection</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/previous-versions/windows/desktop/api/Vpnotify/nn-vpnotify-ivpnotify"><strong>IVPNotify</strong></a>, <a href="/previous-versions/windows/desktop/api/vpnotify/nn-vpnotify-ivpnotify2"><strong>IVPNotify2</strong></a></td>
</tr>
<tr class="even">
<td>Tipi di supporti pin di output</td>
<td>MEDIATYPE_Video, MEDIASUBTYPE_Overlay</td>
</tr>
<tr class="odd">
<td>Interfacce del PIN di output</td>
<td><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>Ipin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>CLSID filtro</td>
<td>CLSID_OverlayMixer</td>
</tr>
<tr class="odd">
<td>CLSID della pagina delle proprietà</td>
<td>Nessuna pagina delle proprietà.</td>
</tr>
<tr class="even">
<td>File eseguibile</td>
<td>qdvd.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Merito</a></td>
<td>MERIT_DO_NOT_USE</td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">Categoria filtro</a></td>
<td>CLSID_LegacyAmFilterCategory</td>
</tr>
</tbody>
</table>



 

### <a name="remarks"></a>Commenti

Il mixer overlay usa la chiave di colore di destinazione per combinare le superfici video con sovrimpressioni. Blits la chiave di colore e il video secondario sull'area primaria e invia il video principale alla superficie di sovrapposizione. La scheda grafica compone quindi le due superfici nel buffer dei frame.

Per verificare se il driver di grafica supporta la sovrimpressione hardware, chiamare **IDirectDraw7:: getcaps**. Se il campo **dwMaxVisibleOverlays** nella struttura **DDCAPS** è maggiore di zero, il driver supporta la sovrimpressione hardware.

Le applicazioni possono controllare alcuni comportamenti sul mixer sovrapposto tramite l'interfaccia [**IMixerPinConfig2**](/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2) . Gli sviluppatori di giochi possono usare il mixer overlay per visualizzare i video in modalità esclusiva di DirectDraw, come descritto più avanti in questa sezione. Il [filtro del renderer video mixing 9](video-mixing-renderer-filter-9.md) (VMR-9) offre ora un supporto migliore per i video nei giochi. Per ulteriori informazioni, vedere [using the video Mixing Renderer](using-the-video-mixing-renderer.md).

Vengono fornite le informazioni seguenti per il vantaggio di filtrare gli sviluppatori e gli sviluppatori di giochi che desiderano utilizzare il mixer overlay in modalità esclusiva DirectDraw.

**Operazioni interne del mixer overlay**

Il mixer overlay espone un pin di input per ogni flusso in ingresso. In genere, sono presenti tre pin di input: pin 0 per i dati video e pin 1 e 2 per la riga 21 e i dati delle sottoimmagini DVD. Internamente, il mixer overlay crea un oggetto DirectDraw con una superficie primaria che comprende l'intero desktop, più una superficie sovrapposta il cui rettangolo è definito dalla dimensione del flusso video sul pin 0. Se il decodificatore non specifica una chiave di colore, il mixer overlay usa le chiavi di colore predefinite: grigio scuro per le schede grafiche più recenti e magenta per le schede a colori 256 precedenti.

> [!Note]  
> I risultati non sono definiti se il decodificatore recapita due flussi video secondari contemporaneamente nella stessa posizione sulla superficie della sovrimpressione. Questo problema si verifica a volte con DVD che contengono flussi di immagini e 21. Il video potrebbe sfarfallare o visualizzare solo uno dei flussi.

 

In Windows Vista o versioni successive, il mixer sovrimpressione Disabilita la Gestione finestre desktop (DWM) se il driver di visualizzazione supporta la sovrimpressione hardware. Le applicazioni devono evitare di usare il filtro overlay mixer; usare invece VMR-9 o il renderer video avanzato (EVR).

**Connessione upstream con il decodificatore video**

In genere, i pin di input del mixer overlay si connettono a un decodificatore video upstream. Il flusso video primario deve connettersi al pin 0. I flussi della riga 21 o della sottoimmagine si connettono al pin 1 o superiore. Se il decodificatore è un decodificatore software che usa esclusivamente la CPU dell'host, la connessione tra il decodificatore e il pin 0 è una connessione [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) . Se il decodificatore usa l'accelerazione hardware, la connessione al pin 0 deve usare [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) interfaccia. Questi due tipi di connessioni si escludono a vicenda.

Se il decodificatore viene disegnato direttamente sulla superficie della sovrimpressione, deve usare l'interfaccia [**iOverlay**](/windows/desktop/api/Strmif/nn-strmif-ioverlay) sul pin 0 e implementare l'interfaccia [**IOverlayNotify**](/windows/desktop/api/Strmif/nn-strmif-ioverlaynotify) .

I filtri che racchiudono un decodificatore hardware e si connettono al mixer sovrapposto tramite una porta video devono implementare l'interfaccia [**IVPConfig**](/previous-versions/windows/desktop/api/Vpconfig/nn-vpconfig-ivpconfig) . Il mixer overlay implementa l'interfaccia [**IVPNotify**](/previous-versions/windows/desktop/api/Vpnotify/nn-vpnotify-ivpnotify) . Queste due interfacce consentono al decodificatore di specificare le superfici di sovrapposizione richieste e consentono al mixer della sovrimpressione di indicare al decodificatore la posizione di tali superfici nella memoria video.

Il mixer overlay garantisce inoltre che il rettangolo video venga ridimensionato correttamente. L'acquisizione video comporta determinati problemi per quanto riguarda il ridimensionamento dell'immagine di anteprima e l'acquisizione di fotogrammi video con interfoliazione. Se si sviluppa un filtro o un driver WDM per un dispositivo di acquisizione video hardware, vedere le pagine di riferimento [**IVPConfig**](/previous-versions/windows/desktop/api/Vpconfig/nn-vpconfig-ivpconfig) e [**IVPNotify**](/previous-versions/windows/desktop/api/Vpnotify/nn-vpnotify-ivpnotify) per altre informazioni su questi argomenti.

Il mixer overlay non viene usato negli scenari di acquisizione 1394 o USB. Viene usato nell'acquisizione video tramite il bus PCI.

**Connessione downstream con il renderer video**

Il mixer di sovrimpressione ha un pin di output che si connette al filtro [renderer video](video-renderer-filter.md) . Il renderer video, in questo caso, non esegue il rendering del video; gestisce semplicemente la finestra video.

La connessione pin usa l'interfaccia [**iOverlay**](/windows/desktop/api/Strmif/nn-strmif-ioverlay) anziché l'interfaccia [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) . Il renderer video passa il relativo handle di finestra tramite il mixer overlay a DirectDraw, che gestisce il ritaglio del rettangolo. Le applicazioni possono controllare il renderer video tramite le interfacce [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) e [**IBasicVideo2**](/windows/desktop/api/Control/nn-control-ibasicvideo2) in gestione grafico dei filtri.

**Modalità esclusiva di DirectDraw**

La modalità esclusiva DirectDraw del mixer overlay consente ai giochi di visualizzare video in una parte dello schermo. In questa modalità, il mixer di sovrimpressione esegue il rendering del video direttamente in una superficie DirectDraw creata dall'applicazione di gioco, anziché in una finestra fornita dal renderer video. Questo consente ai giochi di controllare la chiave di colore. Il mixer sovrimpressione espone solo un pin di input in modalità esclusiva DirectDraw, il che significa che in questa modalità non è possibile eseguire la combinazione di una singola riga 21 o DVD.

Per usare il mixer overlay in modalità esclusiva DirectDraw, creare un'istanza del mixer overlay ed eseguire una query per l'interfaccia [**IDDrawExclModeVideo**](/windows/desktop/api/Strmif/nn-strmif-iddrawexclmodevideo) prima di compilare il grafico del filtro. Chiamare quindi [**IDDrawExclModeVideo:: SetDDrawSurface**](/windows/desktop/api/Strmif/nf-strmif-iddrawexclmodevideo-setddrawsurface) per specificare la superficie DirectDraw per il rendering. Una limitazione significativa di questa modalità è che il gioco non ottiene l'accesso ai bit di video effettivi. Se si usa **IDDrawExclModeVideo**, l'applicazione crea la superficie primaria e il mixer di sovrapposizione crea la superficie della sovrimpressione.

È anche possibile usare la modalità esclusiva DirectDraw per eseguire il rendering senza finestra, ad esempio in una pagina Web, ma questa operazione non è consigliata, perché il mixer overlay non esegue alcuna operazione di combinazione in questa modalità. Ciò significa che non è possibile visualizzare alcuna riga 21 o dati di immagine.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Filtri DirectShow](directshow-filters.md)
</dt> </dl>

 

 




