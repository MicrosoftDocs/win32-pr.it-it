---
description: Il filtro Microsoft MPEG-2 Video Encoder codifica i video MPEG-2 e MPEG-1.
ms.assetid: d52c1299-0641-405c-8960-edd738b56823
title: Codificatore video MPEG-2 Microsoft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7f7b70b9a754aefda3158ae355eb84c24b71b7e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474717"
---
# <a name="microsoft-mpeg-2-video-encoder"></a>Codificatore video MPEG-2 Microsoft

Il filtro Microsoft MPEG-2 Video Encoder codifica i video MPEG-2 e MPEG-1.

Per codificare e codificare flussi audio/video multiplex, usare il filtro [**Microsoft MPEG-2 Encoder,**](microsoft-mpeg-2-encoder.md) che incapsula le funzioni di questo filtro e del filtro [**Microsoft MPEG-2 Audio Encoder.**](microsoft-mpeg-2-audio-encoder.md)

> [!Note]  
> Questo filtro non è supportato nelle piattaforme basate su IA-64.

 



Filtrare le informazioni

Interfacce di filtro

[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/> [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/> **IEncoderAPI**<br/> [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**IVideoEncoder**](/windows/win32/api/strmif/nn-strmif-ivideoencoder)<br/>

Tipi di supporti pin di input

**MEDIATYPE \_ Video,** **MEDIASUBTYPE \_ I420**<br/> **MEDIATYPE \_ Video,** **MEDIASUBTYPE \_ IYUV**<br/> **MEDIATYPE \_ Video,** **MEDIASUBTYPE \_ RGB24**<br/> **MEDIATYPE \_ Video,** **MEDIASUBTYPE \_ UYVY**<br/> **MEDIATYPE \_ Video,** **MEDIASUBTYPE \_ YUY2**<br/> **MEDIATYPE \_ Video,** **MEDIASUBTYPE \_ YV12**<br/>

Interfacce pin di input

[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

Tipi di supporti pin di output

**MEDIATYPE \_ Stream,** **MEDIASUBTYPE \_ MPEG2 \_ VIDEO**<br/> **MEDIATYPE \_ Stream,** **MEDIASUBTYPE \_ MPEG2 \_ PROGRAM**<br/> **MEDIATYPE \_ Flusso,** **MEDIASUBTYPE \_ MPEG2 \_ TRANSPORT**<br/> **MEDIATYPE \_ Video,** **MEDIASUBTYPE \_ MPEG2 \_ VIDEO**<br/>

Interfacce pin di output

[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

Filtro CLSID

**CLSID \_ CMPEG2EncoderVideoDS** (dichiarato in wmcodecdsp.h)

File eseguibile

msmpeg2enc.dll

[Merito](merit.md)

**MERITO \_ NON \_ \_ USARE**

[Categoria filtro](filter-categories.md)

**CLSID \_ LegacyAmFilterCategory**



 

## <a name="remarks"></a>Commenti

Il codificatore video MPEG-2 può produrre i tipi di output seguenti:

-   Flusso elementare video
-   Video in un flusso di programma MPEG-2
-   Video in un flusso di trasporto MPEG-2

Supporta i profili e i livelli MPEG-2 seguenti:



| Profilo        | Livelli                     | Commenti                                            |
|----------------|----------------------------|----------------------------------------------------|
| Profilo semplice | Principale                       |                                                    |
| Main Profile   | Low, Main, High, High-1440 |                                                    |
| Profilo elevato   | Main, High, High-1440      | Nessuna scalabilità o supporto 4:2:2/4:4:4 (solo 4:2:0) |
| Profilo 4:2:2  | Principale, Alto                 | Nessuna scalabilità o supporto 4:2:2 (solo 4:2:0)       |



 

### <a name="codec-properties"></a>Proprietà codec

Il filtro supporta le proprietà seguenti tramite [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi).



| Proprietà                                                                                      | Predefinito                                                          | Valori supportati                                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AVEncCodecType**](avenccodectype-property.md)                                             | Video MPEG-2                                                     | **CODECAPI \_ GUID \_ AVEncMPEG1Video**<br/> **CODECAPI \_ GUID \_ AVEncMPEG2Video**<br/>                                                                                                                        |
| [**AVEncCommonBufferInLevel**](avenccommonbufferinlevel-property.md)                         | 12222464 bit                                                    |                                                                                                                                                                                                                      |
| [**AVEncCommonBufferOutLevel**](avenccommonbufferoutlevel-property.md)                       | 12222464 bit                                                    |                                                                                                                                                                                                                      |
| [**AVEncCommonBufferSize**](avenccommonbuffersize-property.md)                               | 12222464 bit                                                    |                                                                                                                                                                                                                      |
| [**AVEncCommonFormatConstraint**](avenccommonformatconstraint-property.md)                   | Non specificata                                                      | **CODECAPI \_ GUID \_ AVEncCommonFormatUnSpecified** (nessun vincolo di formato)<br/> **CODECAPI \_ GUID \_ AVEncCommonFormatDVD \_ V** (DVD-Video)<br/> **CODECAPI \_ GUID \_ AVEncCommonFormatVCD** (Video CD)<br/> |
| [**AVEncCommonMaxBitRate**](avenccommonmaxbitrate-property.md)                               | 9800000 (9,8 Mbit al secondo)                                       |                                                                                                                                                                                                                      |
| [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md)                             | 7000000 (7,0 Mbit al secondo)                                       |                                                                                                                                                                                                                      |
| [**AVEncCommonMinBitRate**](avenccommonminbitrate-property.md)                               | 128                                                              |                                                                                                                                                                                                                      |
| [**AVEncCommonMultipassMode**](avenccommonmultipassmode-property.md)                         | 1                                                                | 1                                                                                                                                                                                                                    |
| [**AVEncCommonQuality**](avenccommonquality-property.md)                                     | 100                                                              | 1 — 100                                                                                                                                                                                                              |
| [**AVEncCommonQualityVsSpeed**](avenccommonqualityvsspeed-property.md)                       | 75                                                               | 0 — 100                                                                                                                                                                                                              |
| [**AVEncCommonRateControlMode**](avenccommonratecontrolmode-property.md)                     | CBR                                                              | **EAVEncCommonRateControlMode \_ CBR**<br/> **eAVEncCommonRateControlMode \_ PeakConstrainedVBR**<br/> **Qualità eAVEncCommonRateControlMode \_**<br/>                                                   |
| [**AVEncInputVideoSystem**](avencinputvideosystem-property.md)                               | Non specificata                                                      | eAVEncInputVideoSystem \_ Unspecified<br/> eAVEncInputVideoSystem \_ PAL<br/> eAVEncInputVideoSystem \_ NTSC<br/>                                                                                        |
| [**AVEncMPVDefaultBPictureCount**](avencmpvdefaultbpicturecount-property.md)                 | 2                                                                | 0 — 2                                                                                                                                                                                                                |
| [**AVEncMPVFrameFieldMode**](avencmpvframefieldmode-property.md)                             | Modalità frame                                                       |                                                                                                                                                                                                                      |
| [**AVEncMPVGenerateHeaderSeqDispExt**](avencmpvgenerateheaderseqdispext-property.md)         | **TRUE**                                                         |                                                                                                                                                                                                                      |
| [**AVEncMPVGenerateHeaderSeqExt**](avencmpvgenerateheaderseqext-property.md)                 | **TRUE**                                                         |                                                                                                                                                                                                                      |
| [**AVEncMPVGOPOpen**](avencmpvgopopen-property.md)                                           | **FALSE**                                                        |                                                                                                                                                                                                                      |
| [**AVEncMPVGOPSInSeq**](avencmpvgopsinseq-property.md)                                       | 1                                                                | 0 — 1                                                                                                                                                                                                                |
| [**AVEncMPVGOPSize**](avencmpvgopsize-property.md)                                           | 18 frame (36 campi) per NTSC; 15 frame (30 campi) in caso contrario. | 1 — 30; Vedere la sezione Osservazioni                                                                                                                                                                                                  |
| [**AVEncMPVIntraDCPrecision**](avencmpvintradcprecision-property.md)                         | 9                                                                | 8 — 10                                                                                                                                                                                                               |
| [**AVEncMPVLevel**](avencmpvlevel-property.md)                                               | Alto                                                             |                                                                                                                                                                                                                      |
| [**AVEncMPVProfile**](avencmpvprofile-property.md)                                           | Principale                                                             |                                                                                                                                                                                                                      |
| [**AVEncVideoDefaultUpperFieldDominant**](avencvideodefaultupperfielddominant-property.md)   | **TRUE**                                                         |                                                                                                                                                                                                                      |
| [**AVEncVideoForceSourceScanType**](avencvideoforcesourcescantype-property.md)               | Interlaced                                                       | **Interlacciato eAVEncVideoSourceScan \_**<br/> **eAVEncVideoSourceScan \_ Progressive**<br/>                                                                                                                   |
| [**AVEncVideoInputChromaResolution**](avencvideoinputchromaresolution-property.md)           | 4:2:0                                                            | **eAVEncVideoChromaResolution \_ 420** (4:2:0)<br/> **eAVEncVideoChromaResolution \_ SameAsSource**<br/>                                                                                                     |
| [**AVEncVideoInputChromaSubsampling**](avencvideoinputchromasubsampling-property.md)         | Uguale all'origine                                                   |                                                                                                                                                                                                                      |
| [**AVEncVideoInputColorNominalRange**](avencvideoinputcolornominalrange-property.md)         | Uguale all'origine                                                   |                                                                                                                                                                                                                      |
| [**AVEncVideoInputColorPrimaries**](avencvideoinputcolorprimaries-property.md)               | Uguale all'origine                                                   |                                                                                                                                                                                                                      |
| [**AVEncVideoInputColorTransferFunction**](avencvideoinputcolortransferfunction-property.md) | Uguale all'origine                                                   |                                                                                                                                                                                                                      |
| [**AVEncVideoInputColorTransferMatrix**](avencvideoinputcolortransfermatrix-property.md)     | Uguale all'origine                                                   |                                                                                                                                                                                                                      |
| [**AVEncVideoMaxKeyframeDistance**](avencvideomaxkeyframedistance-property.md)               | [**AVEncMPVGOPSize**](avencmpvgopsize-property.md) - 1          | 0 o [**AVEncMPVGOPSize**](avencmpvgopsize-property.md) - 1                                                                                                                                                         |
| [**AVEncVideoNoOfFieldsToEncode**](avencvideonooffieldstoencode-property.md)                 | 0                                                                |                                                                                                                                                                                                                      |
| [**AVEncVideoOutputChromaResolution**](avencvideooutputchromaresolution-property.md)         | 4:2:0                                                            | **eAVEncVideoChromaResolution \_ 420** (4:2:0)<br/> **eAVEncVideoChromaResolution \_ SameAsSource**<br/>                                                                                                     |
| [**AVEncVideoOutputFrameRate**](avencvideooutputframerate-property.md)                       |                                                                  | Deve essere uguale alla frequenza dei fotogrammi di input.                                                                                                                                                                            |
| [**AVEncVideoOutputScanType**](avencvideooutputscantype-property.md)                         | Uguale all'input                                                    | **eAVEncVideoOutputScan \_ SameAsInput**                                                                                                                                                                               |
| [**AVEncVideoPixelAspectRatio**](avencvideopixelaspectratio-property.md)                     | 1:1                                                              |                                                                                                                                                                                                                      |



 

È consigliabile impostare le proprietà nell'ordine seguente:

1.  [**AVEncCommonFormatConstraint**](avenccommonformatconstraint-property.md)
2.  [**AVEncCodecType**](avenccodectype-property.md)
3.  [**AVEncMPVProfile**](avencmpvprofile-property.md)
4.  [**AVEncMPVLevel**](avencmpvlevel-property.md)
5.  [**AVEncInputVideoSystem**](avencinputvideosystem-property.md)

Impostare le proprietà rimanenti in qualsiasi ordine. Vedere tuttavia [Struttura GOP.](#gop-structure)

È possibile impostare le proprietà mentre il grafico dei filtri è in esecuzione. Si verifica un ritardo di almeno un GOP prima che le nuove impostazioni siano effettive.

### <a name="encoder-operation"></a>Operazione del codificatore

Quando si codifica un video MPEG-1, il codificatore imposta automaticamente il codice del **\_ \_ flag** dei parametri vincolati a 1 bit nell'intestazione della sequenza se vengono soddisfatti tutti i vincoli.

Se necessario, il codificatore arrotonda le dimensioni video di input in modo che le dimensioni video di output corrispondano ai requisiti MPEG. Per i video progressivi, le dimensioni di output vengono arrotondate a un multiplo di 16 sia in larghezza che in altezza. Per i video interlacciati, la larghezza viene arrotondata a un multiplo di 16 e l'altezza viene arrotondata a un multiplo di 32. Questa operazione di arrotondamento usa la spaziatura interna in base alle esigenze.

Se il video è interlacciato, il codificatore esegue il rilevamento telegrafico automatico (3:2 a discesa). Il video di input può contenere coppie di immagini di campo, oltre a fotogrammi interlacciati.

Il formato interno del codificatore è 4:2:0 IYUV (identico a I420). Può eseguire la conversione dei colori dai formati video YUY2, YV12, UYVY e RGB-24.

Per vincolare il flusso di bit a un formato di destinazione (DVD o VCD), impostare la [**proprietà AVEncCommonFormatConstraint.**](avenccommonformatconstraint-property.md) Se questa proprietà ha un valore diverso da **GUID \_ AVEncCommonFormatUnSpecified**, il codificatore limita la sintassi MPEG a quella consentita dal formato di destinazione.

Per la codifica live, impostare [**la proprietà AVEncCommonQualityVsSpeed**](avenccommonqualityvsspeed-property.md) su zero. In questo modo il codificatore viene ottimizzato per la velocità.

### <a name="encoding-modes"></a>Modalità di codifica

Il codificatore supporta diverse modalità di codifica:

-   Velocità in bit costante (CBR) a un passaggio.
-   Velocità in bit variabile basata sulla qualità a un passaggio, usando una dimensione costante del passaggio del quantizer. In questa modalità il codificatore tenta di soddisfare un livello di qualità di destinazione, fino a una velocità in bit massima.
-   VbR con vincoli di picco a un passaggio. In questa modalità, il codificatore tenta di ottenere una velocità in bit media di destinazione entro determinati limiti interni.

Per configurare la modalità di codifica, impostare le proprietà seguenti:




| Mode | Proprietà | 
|------|------------|
| CBR | <a href="avenccommonratecontrolmode-property.md"><strong>AVEncCommonRateControlMode</strong></a>  =  <strong>eAVEncCommonRateControlMode_CBR</strong><br /><a href="avenccommonqualityvsspeed-property.md"><strong>AVEncCommonQualityVsSpeed</strong></a><br /><a href="avenccommonmeanbitrate-property.md"><strong>AVEncCommonMeanBitRate</strong></a><br /> | 
| VbR basato sulla qualità | <a href="avenccommonratecontrolmode-property.md"><strong>AVEncCommonRateControlMode</strong></a>  =  <strong>eAVEncCommonRateControlMode_Quality</strong><br /><a href="avenccommonquality-property.md"><strong>AVEncCommonQuality</strong></a><br /><a href="avenccommonmaxbitrate-property.md"><strong>AVEncCommonMaxBitRate</strong></a><br /><blockquote>[!Note]<br />In questa modalità le <a href="avenccommonmeanbitrate-property.md"><strong>proprietà AVEncCommonMeanBitRate</strong></a> e <a href="avenccommonminbitrate-property.md"><strong>AVEncCommonMinBitRate</strong></a> non vengono usate. Si presuppone che la velocità in bit minima sia zero.</blockquote><br /> | 
| VbR con vincoli di picco | <a href="avenccommonratecontrolmode-property.md"><strong>AVEncCommonRateControlMode</strong></a>  =  <strong>eAVEncCommonRateControlMode_PeakConstrainedVBR</strong><br /><a href="avenccommonmultipassmode-property.md"><strong>AVEncCommonMultipassMode</strong></a> = 1<br /><a href="avenccommonminbitrate-property.md"><strong>AVEncCommonMinBitRate</strong></a><br /><a href="avenccommonmaxbitrate-property.md"><strong>AVEncCommonMaxBitRate</strong></a><br /><a href="avenccommonmeanbitrate-property.md"><strong>AVEncCommonMeanBitRate</strong></a><br /> | 




 

> [!Note]  
> La funzione VBR a due passi non è supportata.

 

### <a name="aspect-ratio"></a>Proporzioni

Le proporzioni di visualizzazione e le proporzioni pixel (PAR) sono correlate dalla formula seguente:

<dl> Proporzioni di visualizzazione = dimensioni par × (larghezza immagine/altezza immagine)  
</dl>

Il codificatore usa questa formula per calcolare il valore delle proporzioni dei persi per i bitstream MPEG-1 o le informazioni sulle proporzioni per \_ \_ i \_ \_ bitstream MPEG-2. Vedere rispettivamente ISO/IEC 11172 e ISO/IEC 138181-2.

Il codificatore prova le impostazioni seguenti, nell'ordine indicato:

1.  Se l'applicazione imposta la [**proprietà AVEncVideoPixelAspectRatio**](avencvideopixelaspectratio-property.md) in qualsiasi momento prima dell'esecuzione del grafico del filtro, questa proprietà viene usata per par.
2.  In caso contrario, se i membri **dwPictAspectRatioX** e **dwPictAspectRatioY** della struttura [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) sono diversi da zero, questi membri vengono usati per le proporzioni di visualizzazione e il par viene calcolato in base alle proporzioni dello schermo.
3.  Se nessuno di questi valori è presente, si presuppone che par sia 1,0 e le proporzioni di visualizzazione vengono calcolate di conseguenza.

Nella modalità di codifica live [**(AVEncCommonQualityVsSpeed**](avenccommonqualityvsspeed-property.md) uguale a zero), le proporzioni dello schermo devono essere 4:3 o 16:9, con un valore predefinito di 4:3. Se le proporzioni dello schermo calcolate non sono 4:3 o 16:9, il codificatore usa il valore 4:3.

### <a name="gop-structure"></a>Struttura GOP

Per specificare la struttura del gruppo di immagini (GOP), impostare le proprietà seguenti nell'ordine indicato:

1.  [**AVEncMPVGOPSize**](avencmpvgopsize-property.md)
2.  [**AVEncVideoMaxKeyframeDistance**](avencvideomaxkeyframedistance-property.md)
3.  [**AVEncMPVDefaultBPictureCount**](avencmpvdefaultbpicturecount-property.md)

In base a queste impostazioni, il codificatore produce una delle strutture GOP seguenti:



| [**AVEncVideoMaxKeyframeDistance**](avencvideomaxkeyframedistance-property.md) | [**AVEncMPVDefaultBPictureCount**](avencmpvdefaultbpicturecount-property.md) | Struttura GOP |
|---------------------------------------------------------------------------------|-------------------------------------------------------------------------------|---------------|
| 0                                                                               | 0                                                                             | IIII...       |
| [**AVEncMPVGOPSize**](avencmpvgopsize-property.md) - 1                         | 0                                                                             | IPPP...       |
| [**AVEncMPVGOPSize**](avencmpvgopsize-property.md) - 1                         | 1                                                                             | IBPBP...      |
| [**AVEncMPVGOPSize**](avencmpvgopsize-property.md) - 1                         | 2                                                                             | IBBPBBP...    |



 

La struttura GOP predefinita è IBBPBBP... con una dimensione GOP di 15 fotogrammi.

Se l'applicazione vincola il formato di destinazione su DVD (tramite la proprietà [**AVEncCommonFormatConstraint)**](avenccommonformatconstraint-property.md) e imposta la proprietà [**AVEncInputVideoSystem**](avencinputvideosystem-property.md) su NTSC o PAL, il codificatore supporta le dimensioni GOP seguenti:



| Sistema video | Dimensioni GOP valide | Dimensioni GOP predefinite |
|--------------|-----------------|------------------|
| NTSC         | 1-18            | 18 (36 campi)   |
| elenco di accesso alla pubblicazione          | 1-15            | 15 (30 campi)   |



 

### <a name="codec-property-change-lists"></a>Elenchi di modifiche alle proprietà del codec

L'impostazione del valore di una proprietà del codec può modificare l'intervallo valido di un'altra proprietà. Ad esempio, vincolando il formato di destinazione si limita la velocità in bit media. Ogni volta che l'applicazione imposta una proprietà, il codificatore verifica se eventuali altre proprietà non rientrano nell'intervallo valido. In tal caso, il codificatore reimposta tale proprietà sul nuovo valore predefinito. Per ricevere notifiche in questo caso, eseguire le operazioni seguenti:

1.  Chiamare [**ICodecAPI::RegisterForEvent**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-registerforevent) con il **valore CODECAPI \_ CHANGELISTS**.
2.  Usare [**l'interfaccia IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) per monitorare gli eventi dal grafico dei filtri.
3.  Se l'intervallo o il valore predefinito di una proprietà cambia, il codificatore invia un evento [**\_ EC CODECAPI \_ EVENT**](ec-codecapi-event.md) con un elenco di proprietà modificate.

### <a name="iencoderapi-support"></a>Supporto IEncoderAPI

Per compatibilità con le versioni precedenti, il filtro supporta le proprietà seguenti tramite **l'interfaccia IEncoderAPI:**



| Proprietà                       | Descrizione                                                                              |
|--------------------------------|------------------------------------------------------------------------------------------|
| **ENCAPIPARAM \_ BITRATE**       | Equivale a [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md).         |
| **VELOCITÀ IN BIT DI PICCO ENCAPIPARAM \_ \_** | Equivalente a [**AVEncCommonMaxBitRate**](avenccommonmaxbitrate-property.md).           |
| **MODALITÀ BITRATE ENCAPIPARAM \_ \_** | Equivale a [**AVEncCommonRateControlMode.**](avenccommonratecontrolmode-property.md) |



 

Quando si imposta la **proprietà ENCAPIPARAM \_ BITRATE \_ MODE,** i valori vengono mappati come segue:



| **MODALITÀ BITRATE ENCAPIPARAM \_ \_** | [**AVEncCommonRateControlMode**](avenccommonratecontrolmode-property.md) |
|--------------------------------|---------------------------------------------------------------------------|
| **ConstantBitRate**            | **EAVEncCommonRateControlMode \_ CBR**                                      |
| **VariableBitRateAverage**     | Vedere la nota.                                                                 |
| **VariableBitRatePeak**        | **eAVEncCommonRateControlMode \_ PeakConstrainedVBR**                       |



 

> [!Note]  
> Attualmente, il codificatore video MPEG-2 non supporta la **modalità di codifica VariableBitRateAverage.** Se si imposta questo valore, il codificatore predefinito è la codifica CBR (**eAVEncCommonRateControlMode \_ CBR).**

 

Quando si riceve la **proprietà ENCAPIPARAM \_ BITRATE \_ MODE,** viene eseguito il mapping dei valori come segue:



| [**AVEncCommonRateControlMode**](avenccommonratecontrolmode-property.md) | **MODALITÀ BITRATE ENCAPIPARAM \_ \_** |
|---------------------------------------------------------------------------|--------------------------------|
| **EAVEncCommonRateControlMode \_ CBR**                                      | **ConstantBitRate**            |
| **Qualità eAVEncCommonRateControlMode \_**                                  | **VariableBitRatePeak**        |
| **eAVEncCommonRateControlMode \_ PeakConstrainedVBR**                       | **VariableBitRatePeak**        |



 

### <a name="limitations"></a>Limitazioni

Attualmente il codificatore non supporta alcuna delle funzionalità seguenti:

-   Generazione di pacchetti PES (Packetized Element Stream).
-   Conversione della frequenza dei fotogrammi. Il flusso di input deve avere una frequenza di fotogrammi valida per un flusso di bit MPEG-2.
-   Estensioni della frequenza fotogrammi per MPEG-2 ( estensione frequenza **\_ \_ \_ fotogrammi n**, estensione **\_ \_ frequenza \_ fotogrammi d**).
-   Posizioni del buffer di ingresso/uscita (VBV) per un clip.
-   Inserimento di dati della riga 21 (informazioni sui sottotitoli codificati) nel flusso elementare del video.
-   Impostazione del campo del codice temporale a 25 **bit \_** nell'intestazione GOP per MPEG-2.
-   Denozionare il filtro.
-   DRM (Digital Rights Management).

Il codificatore introduce una latenza di codifica di almeno un GOP.

## <a name="requirements"></a>Requisiti



| Requisito | valore |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, Windows 7 Ultimate \[ desktop apps only\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl>                                                                                       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[DirectShow Filtri](directshow-filters.md)
</dt> <dt>

[**Tipi di supporti demultiplexer MPEG-2**](mpeg-2-demultiplexer-media-types.md)
</dt> </dl>

 

 
