---
description: Il filtro codificatore video Microsoft MPEG-2 codifica i video MPEG-2 e MPEG-1.
ms.assetid: d52c1299-0641-405c-8960-edd738b56823
title: Codificatore video Microsoft MPEG-2 (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02c96db605586c6abf0f51537689a9365df2842c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304174"
---
# <a name="microsoft-mpeg-2-video-encoder"></a>Codificatore video Microsoft MPEG-2

Il filtro codificatore video Microsoft MPEG-2 codifica i video MPEG-2 e MPEG-1.

Per codificare i flussi audio/video multiplex, usare il filtro del [**codificatore MPEG-2 di Microsoft**](microsoft-mpeg-2-encoder.md) , che incapsula le funzioni di questo filtro e del filtro [**codificatore audio Microsoft MPEG-2**](microsoft-mpeg-2-audio-encoder.md) .

> [!Note]  
> Questo filtro non è supportato nelle piattaforme basate su IA-64.

 



Informazioni sul filtro

Interfacce di filtro

[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/> [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/> **IEncoderAPI**<br/> [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**IVideoEncoder**](/windows/win32/api/strmif/nn-strmif-ivideoencoder)<br/>

Tipi di supporti pin di input

**MEDIATYPE \_ Video**, **MEDIASUBTYPE \_ I420**<br/> **MEDIATYPE \_ Video**, **MEDIASUBTYPE \_ IYUV**<br/> **MEDIATYPE \_ Video**, **MEDIASUBTYPE \_ RGB24**<br/> **MEDIATYPE \_ Video**, **MEDIASUBTYPE \_ UYVY**<br/> **MEDIATYPE \_ Video**, **MEDIASUBTYPE \_ YUY2**<br/> **MEDIATYPE \_ Video**, **MEDIASUBTYPE \_ YV12**<br/>

Interfacce pin di input

[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

Tipi di supporti pin di output

**MEDIATYPE \_ Flusso**, **\_ \_ video MEDIASUBTYPE MPEG2**<br/> **MEDIATYPE \_ Flusso**, **\_ \_ programma MEDIASUBTYPE MPEG2**<br/> **MEDIATYPE \_ Flusso**, **\_ \_ trasporto MPEG2 MEDIASUBTYPE**<br/> **MEDIATYPE \_ Video**, **\_ \_ video MEDIASUBTYPE MPEG2**<br/>

Interfacce del PIN di output

[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

CLSID filtro

**CLSID \_ CMPEG2EncoderVideoDS** (dichiarata in wmcodecdsp. h)

File eseguibile

msmpeg2enc.dll

[Merito](merit.md)

**il merito non viene \_ \_ \_ utilizzato**

[Categoria filtro](filter-categories.md)

**\_LEGACYAMFILTERCATEGORY CLSID**



 

## <a name="remarks"></a>Commenti

Il codificatore video MPEG-2 può produrre i tipi di output seguenti:

-   Flusso elementare video
-   Video in un flusso di programma MPEG-2
-   Video in un flusso di trasporto MPEG-2

Supporta i seguenti profili e livelli MPEG-2:



| Profilo        | Livelli                     | Commenti                                            |
|----------------|----------------------------|----------------------------------------------------|
| Profilo semplice | Principale                       |                                                    |
| Main Profile   | Low, Main, High, High-1440 |                                                    |
| Profilo elevato   | Main, High, High-1440      | Nessun supporto per la scalabilità o 4:2:2/4:4:4 (solo 4:2:0) |
| Profilo 4:2:2  | Principale, alto                 | Nessun supporto per la scalabilità o 4:2:2 (solo 4:2:0)       |



 

### <a name="codec-properties"></a>Proprietà codec

Il filtro supporta le seguenti proprietà tramite [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi).



| Proprietà                                                                                      | Predefinito                                                          | Valori supportati                                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AVEncCodecType**](avenccodectype-property.md)                                             | Video MPEG-2                                                     | **\_GUID AVEncMPEG1Video di CODEcapi \_**<br/> **\_GUID AVEncMPEG2Video di CODEcapi \_**<br/>                                                                                                                        |
| [**AVEncCommonBufferInLevel**](avenccommonbufferinlevel-property.md)                         | 12222464 bit                                                    |                                                                                                                                                                                                                      |
| [**AVEncCommonBufferOutLevel**](avenccommonbufferoutlevel-property.md)                       | 12222464 bit                                                    |                                                                                                                                                                                                                      |
| [**AVEncCommonBufferSize**](avenccommonbuffersize-property.md)                               | 12222464 bit                                                    |                                                                                                                                                                                                                      |
| [**AVEncCommonFormatConstraint**](avenccommonformatconstraint-property.md)                   | Non specificata                                                      | **CODEcapi \_ GUID \_ AVEncCommonFormatUnSpecified** (nessun vincolo di formato)<br/> **CODEcapi \_ GUID \_ AVEncCommonFormatDVD \_ V** (DVD-video)<br/> **CODEcapi \_ GUID \_ AVEncCommonFormatVCD** (video CD)<br/> |
| [**AVEncCommonMaxBitRate**](avenccommonmaxbitrate-property.md)                               | 9,8 milioni (9,8 Mbit al secondo)                                       |                                                                                                                                                                                                                      |
| [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md)                             | 7 milioni (7,0 Mbit al secondo)                                       |                                                                                                                                                                                                                      |
| [**AVEncCommonMinBitRate**](avenccommonminbitrate-property.md)                               | 128                                                              |                                                                                                                                                                                                                      |
| [**AVEncCommonMultipassMode**](avenccommonmultipassmode-property.md)                         | 1                                                                | 1                                                                                                                                                                                                                    |
| [**AVEncCommonQuality**](avenccommonquality-property.md)                                     | 100                                                              | 1-100                                                                                                                                                                                                              |
| [**AVEncCommonQualityVsSpeed**](avenccommonqualityvsspeed-property.md)                       | 75                                                               | 0-100                                                                                                                                                                                                              |
| [**AVEncCommonRateControlMode**](avenccommonratecontrolmode-property.md)                     | CBR                                                              | **eAVEncCommonRateControlMode \_ CBR**<br/> **\_PeakConstrainedVBR eAVEncCommonRateControlMode**<br/> **\_qualità eAVEncCommonRateControlMode**<br/>                                                   |
| [**AVEncInputVideoSystem**](avencinputvideosystem-property.md)                               | Non specificata                                                      | eAVEncInputVideoSystem non \_ specificato<br/> eAVEncInputVideoSystem \_ PAL<br/> eAVEncInputVideoSystem \_ NTSC<br/>                                                                                        |
| [**AVEncMPVDefaultBPictureCount**](avencmpvdefaultbpicturecount-property.md)                 | 2                                                                | 0-2                                                                                                                                                                                                                |
| [**AVEncMPVFrameFieldMode**](avencmpvframefieldmode-property.md)                             | Modalità frame                                                       |                                                                                                                                                                                                                      |
| [**AVEncMPVGenerateHeaderSeqDispExt**](avencmpvgenerateheaderseqdispext-property.md)         | **TRUE**                                                         |                                                                                                                                                                                                                      |
| [**AVEncMPVGenerateHeaderSeqExt**](avencmpvgenerateheaderseqext-property.md)                 | **TRUE**                                                         |                                                                                                                                                                                                                      |
| [**AVEncMPVGOPOpen**](avencmpvgopopen-property.md)                                           | **FALSE**                                                        |                                                                                                                                                                                                                      |
| [**AVEncMPVGOPSInSeq**](avencmpvgopsinseq-property.md)                                       | 1                                                                | 0-1                                                                                                                                                                                                                |
| [**AVEncMPVGOPSize**](avencmpvgopsize-property.md)                                           | 18 fotogrammi (campi 36) per NTSC; 15 frame (30 campi) in caso contrario. | 1-30; vedere la sezione Osservazioni                                                                                                                                                                                                  |
| [**AVEncMPVIntraDCPrecision**](avencmpvintradcprecision-property.md)                         | 9                                                                | 8-10                                                                                                                                                                                                               |
| [**AVEncMPVLevel**](avencmpvlevel-property.md)                                               | Alto                                                             |                                                                                                                                                                                                                      |
| [**AVEncMPVProfile**](avencmpvprofile-property.md)                                           | Principale                                                             |                                                                                                                                                                                                                      |
| [**AVEncVideoDefaultUpperFieldDominant**](avencvideodefaultupperfielddominant-property.md)   | **TRUE**                                                         |                                                                                                                                                                                                                      |
| [**AVEncVideoForceSourceScanType**](avencvideoforcesourcescantype-property.md)               | Interlaced                                                       | **eAVEncVideoSourceScan \_ interlacciato**<br/> **eAVEncVideoSourceScan \_ progressive**<br/>                                                                                                                   |
| [**AVEncVideoInputChromaResolution**](avencvideoinputchromaresolution-property.md)           | 4:2:0                                                            | **eAVEncVideoChromaResolution \_ 420** (4:2:0)<br/> **\_SameAsSource eAVEncVideoChromaResolution**<br/>                                                                                                     |
| [**AVEncVideoInputChromaSubsampling**](avencvideoinputchromasubsampling-property.md)         | Uguale all'origine                                                   |                                                                                                                                                                                                                      |
| [**AVEncVideoInputColorNominalRange**](avencvideoinputcolornominalrange-property.md)         | Uguale all'origine                                                   |                                                                                                                                                                                                                      |
| [**AVEncVideoInputColorPrimaries**](avencvideoinputcolorprimaries-property.md)               | Uguale all'origine                                                   |                                                                                                                                                                                                                      |
| [**AVEncVideoInputColorTransferFunction**](avencvideoinputcolortransferfunction-property.md) | Uguale all'origine                                                   |                                                                                                                                                                                                                      |
| [**AVEncVideoInputColorTransferMatrix**](avencvideoinputcolortransfermatrix-property.md)     | Uguale all'origine                                                   |                                                                                                                                                                                                                      |
| [**AVEncVideoMaxKeyframeDistance**](avencvideomaxkeyframedistance-property.md)               | [**AVEncMPVGOPSize**](avencmpvgopsize-property.md) -1          | 0 o [**AVEncMPVGOPSize**](avencmpvgopsize-property.md) -1                                                                                                                                                         |
| [**AVEncVideoNoOfFieldsToEncode**](avencvideonooffieldstoencode-property.md)                 | 0                                                                |                                                                                                                                                                                                                      |
| [**AVEncVideoOutputChromaResolution**](avencvideooutputchromaresolution-property.md)         | 4:2:0                                                            | **eAVEncVideoChromaResolution \_ 420** (4:2:0)<br/> **\_SameAsSource eAVEncVideoChromaResolution**<br/>                                                                                                     |
| [**AVEncVideoOutputFrameRate**](avencvideooutputframerate-property.md)                       |                                                                  | Deve corrispondere alla frequenza dei fotogrammi di input.                                                                                                                                                                            |
| [**AVEncVideoOutputScanType**](avencvideooutputscantype-property.md)                         | Uguale all'input                                                    | **\_SameAsInput eAVEncVideoOutputScan**                                                                                                                                                                               |
| [**AVEncVideoPixelAspectRatio**](avencvideopixelaspectratio-property.md)                     | 1:1                                                              |                                                                                                                                                                                                                      |



 

È consigliabile impostare le proprietà nell'ordine seguente:

1.  [**AVEncCommonFormatConstraint**](avenccommonformatconstraint-property.md)
2.  [**AVEncCodecType**](avenccodectype-property.md)
3.  [**AVEncMPVProfile**](avencmpvprofile-property.md)
4.  [**AVEncMPVLevel**](avencmpvlevel-property.md)
5.  [**AVEncInputVideoSystem**](avencinputvideosystem-property.md)

Impostare le proprietà rimanenti in qualsiasi ordine. (Tuttavia, vedere [struttura GOP](#gop-structure)).

È possibile impostare le proprietà mentre è in esecuzione il grafico dei filtri. Si verifica un ritardo di almeno un GOP prima che le nuove impostazioni abbiano effetto.

### <a name="encoder-operation"></a>Operazione del codificatore

Quando si codifica il video MPEG-1, il codificatore imposta automaticamente il codice del **\_ \_ flag dei parametri vincolati** a 1 bit nell'intestazione della sequenza se vengono soddisfatti tutti i vincoli.

Se necessario, il codificatore Arrotonda le dimensioni del video di input in modo che le dimensioni del video di output corrispondano ai requisiti MPEG. Per i video progressivi, le dimensioni di output vengono arrotondate per eccesso a un multiplo di 16 in larghezza e altezza. Per i video interlacciati, la larghezza viene arrotondata per eccesso a un multiplo di 16 e l'altezza viene arrotondata per eccesso a un multiplo di 32. Questa operazione di arrotondamento usa la spaziatura interna in base alle esigenze.

Se il video è interlacciato, il codificatore esegue il rilevamento automatico di telecine (3:2 a discesa). Il video di input può contenere coppie di immagini di campo, oltre ai frame interlacciati.

Il formato interno del codificatore è 4:2:0 IYUV (identico a I420). Consente di eseguire la conversione dei colori dai formati video YUY2, YV12, UYVY e RGB-24.

Per vincolare il Bitstream a un formato di destinazione (DVD o VCD), impostare la proprietà [**AVEncCommonFormatConstraint**](avenccommonformatconstraint-property.md) . Se questa proprietà ha un valore diverso da **GUID \_ AVEncCommonFormatUnSpecified**, il codificatore limita la sintassi MPEG a quella consentita dal formato di destinazione.

Per la codifica live, impostare la proprietà [**AVEncCommonQualityVsSpeed**](avenccommonqualityvsspeed-property.md) su zero. In questo modo, il codificatore viene ottimizzato per la velocità.

### <a name="encoding-modes"></a>Modalità di codifica

Il codificatore supporta diverse modalità di codifica:

-   Velocità in bit costante (CBR) a una sessione.
-   Velocità in bit di una variabile basata sulla qualità (VBR), usando una dimensione del passaggio del quantizzatore costante. In questa modalità, il codificatore tenta di soddisfare un livello di qualità di destinazione, fino a una velocità massima in bit.
-   VBR con vincolo di picco un solo passaggio. In questa modalità, il codificatore tenta di ottenere una velocità in bit media di destinazione entro determinati limiti interni.

Per configurare la modalità di codifica, impostare le proprietà seguenti:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Modalità</th>
<th>Proprietà</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>CBR</td>
<td><a href="avenccommonratecontrolmode-property.md"><strong>AVEncCommonRateControlMode</strong></a>  =  <strong>eAVEncCommonRateControlMode_CBR</strong><br/> <a href="avenccommonqualityvsspeed-property.md"><strong>AVEncCommonQualityVsSpeed</strong></a><br/> <a href="avenccommonmeanbitrate-property.md"><strong>AVEncCommonMeanBitRate</strong></a><br/></td>
</tr>
<tr class="even">
<td>VBR basato sulla qualità</td>
<td><a href="avenccommonratecontrolmode-property.md"><strong>AVEncCommonRateControlMode</strong></a>  =  <strong>eAVEncCommonRateControlMode_Quality</strong><br/> <a href="avenccommonquality-property.md"><strong>AVEncCommonQuality</strong></a><br/> <a href="avenccommonmaxbitrate-property.md"><strong>AVEncCommonMaxBitRate</strong></a><br/>
<blockquote>
[!Note]<br />
In questa modalità, le proprietà <a href="avenccommonmeanbitrate-property.md"><strong>AVEncCommonMeanBitRate</strong></a> e <a href="avenccommonminbitrate-property.md"><strong>AVEncCommonMinBitRate</strong></a> non vengono utilizzate. Si presuppone che la velocità in bit minima sia zero.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>VBR con vincoli di picco</td>
<td><a href="avenccommonratecontrolmode-property.md"><strong>AVEncCommonRateControlMode</strong></a>  =  <strong>eAVEncCommonRateControlMode_PeakConstrainedVBR</strong><br/> <a href="avenccommonmultipassmode-property.md"><strong>AVEncCommonMultipassMode</strong></a> = 1<br/> <a href="avenccommonminbitrate-property.md"><strong>AVEncCommonMinBitRate</strong></a><br/> <a href="avenccommonmaxbitrate-property.md"><strong>AVEncCommonMaxBitRate</strong></a><br/> <a href="avenccommonmeanbitrate-property.md"><strong>AVEncCommonMeanBitRate</strong></a><br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> Il VBR a due passaggi non è supportato.

 

### <a name="aspect-ratio"></a>Proporzioni

Le proporzioni di visualizzazione e le proporzioni dei pixel sono correlate alla formula seguente:

<dl> Visualizza proporzioni = PAR × (larghezza immagine/altezza immagine)  
</dl>

Il codificatore usa questa formula per calcolare il valore delle \_ proporzioni pel \_ per i Bitstream MPEG-1 o \_ \_ le informazioni sulle proporzioni per i Bitstream MPEG-2. (Vedere rispettivamente ISO/IEC 11172 e ISO/IEC 138181-2).

Il codificatore tenta le impostazioni seguenti in ordine:

1.  Se l'applicazione imposta la proprietà [**AVEncVideoPixelAspectRatio**](avencvideopixelaspectratio-property.md) in qualsiasi momento prima dell'esecuzione del grafico di filtro, questa proprietà viene utilizzata per la par.
2.  In caso contrario, se i membri **dwPictAspectRatioX** e **DwPictAspectRatioY** della struttura [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) sono diversi da zero, questi membri vengono utilizzati per le proporzioni di visualizzazione e il par viene calcolato dalle proporzioni di visualizzazione.
3.  Se nessuno di questi valori è presente, si presuppone che sia 1,0 e che le proporzioni di visualizzazione vengano calcolate di conseguenza.

In modalità di codifica live ([**AVEncCommonQualityVsSpeed**](avenccommonqualityvsspeed-property.md) uguale a zero), le proporzioni di visualizzazione devono essere 4:3 o 16:9 e il valore predefinito è 4:3. Se le proporzioni di visualizzazione calcolate non sono 4:3 o 16:9, il codificatore usa il valore 4:3.

### <a name="gop-structure"></a>Struttura GOP

Per specificare la struttura del gruppo di immagini (GOP), impostare le proprietà seguenti in ordine:

1.  [**AVEncMPVGOPSize**](avencmpvgopsize-property.md)
2.  [**AVEncVideoMaxKeyframeDistance**](avencvideomaxkeyframedistance-property.md)
3.  [**AVEncMPVDefaultBPictureCount**](avencmpvdefaultbpicturecount-property.md)

In base a queste impostazioni, il codificatore produce una delle seguenti strutture GOP:



| [**AVEncVideoMaxKeyframeDistance**](avencvideomaxkeyframedistance-property.md) | [**AVEncMPVDefaultBPictureCount**](avencmpvdefaultbpicturecount-property.md) | Struttura GOP |
|---------------------------------------------------------------------------------|-------------------------------------------------------------------------------|---------------|
| 0                                                                               | 0                                                                             | IIII...       |
| [**AVEncMPVGOPSize**](avencmpvgopsize-property.md) -1                         | 0                                                                             | IPPP...       |
| [**AVEncMPVGOPSize**](avencmpvgopsize-property.md) -1                         | 1                                                                             | IBPBP...      |
| [**AVEncMPVGOPSize**](avencmpvgopsize-property.md) -1                         | 2                                                                             | IBBPBBP...    |



 

La struttura GOP predefinita è IBBPBBP... con una dimensione GOP di 15 frame.

Se l'applicazione vincola il formato di destinazione a DVD (tramite la proprietà [**AVEncCommonFormatConstraint**](avenccommonformatconstraint-property.md) ) e imposta la proprietà [**AVEncInputVideoSystem**](avencinputvideosystem-property.md) su NTSC o PAL, il codificatore supporta le dimensioni GOP seguenti:



| Sistema video | Dimensioni GOP valide | Dimensioni GOP predefinite |
|--------------|-----------------|------------------|
| NTSC         | 1-18            | 18 (36 campi)   |
| elenco di accesso alla pubblicazione          | 1-15            | 15 (30 campi)   |



 

### <a name="codec-property-change-lists"></a>Elenchi di modifiche delle proprietà codec

Impostando il valore di una proprietà del codec è possibile modificare l'intervallo valido di un'altra proprietà. (Ad esempio, vincolando il formato di destinazione si limita la velocità in bit media). Ogni volta che l'applicazione imposta una proprietà, il codificatore controlla se le altre proprietà ora non rientrano nell'intervallo valido. In tal caso, il codificatore Reimposta la proprietà sul nuovo valore predefinito. Per ricevere notifiche quando si verifica questo problema, eseguire le operazioni seguenti:

1.  Chiamare [**ICodecAPI:: RegisterForEvent**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-registerforevent) con il valore **codecapite \_ durante Depot**.
2.  Usare l'interfaccia [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) per monitorare gli eventi dal grafico dei filtri.
3.  Se l'intervallo o il valore predefinito di una proprietà viene modificato, il codificatore invia un evento di [**\_ \_ evento del codecapite EC**](ec-codecapi-event.md) con un elenco di proprietà modificate.

### <a name="iencoderapi-support"></a>Supporto di IEncoderAPI

Per compatibilità con le versioni precedenti, il filtro supporta le seguenti proprietà tramite l'interfaccia **IEncoderAPI** :



| Proprietà                       | Descrizione                                                                              |
|--------------------------------|------------------------------------------------------------------------------------------|
| **\_velocità in bit ENCAPIPARAM**       | Equivalente a [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md).         |
| **\_velocità in \_ bit ENCAPIPARAM picco** | Equivalente a [**AVEncCommonMaxBitRate**](avenccommonmaxbitrate-property.md).           |
| **\_modalità a bitrate ENCAPIPARAM \_** | Equivalente a [**AVEncCommonRateControlMode**](avenccommonratecontrolmode-property.md). |



 

Quando si imposta la proprietà **ENCAPIPARAM \_ bitrate \_ mode** , i valori vengono mappati come segue:



| **\_modalità a bitrate ENCAPIPARAM \_** | [**AVEncCommonRateControlMode**](avenccommonratecontrolmode-property.md) |
|--------------------------------|---------------------------------------------------------------------------|
| **ConstantBitRate**            | **eAVEncCommonRateControlMode \_ CBR**                                      |
| **VariableBitRateAverage**     | Vedere la nota.                                                                 |
| **VariableBitRatePeak**        | **\_PeakConstrainedVBR eAVEncCommonRateControlMode**                       |



 

> [!Note]  
> Attualmente, il codificatore video MPEG-2 non supporta la modalità di codifica **VariableBitRateAverage** . Se si imposta questo valore, l'impostazione predefinita del codificatore è la codifica CBR (**eAVEncCommonRateControlMode \_ CBR**).

 

Quando si recupera la proprietà della **\_ \_ Modalità bitrate ENCAPIPARAM** , i valori vengono mappati come segue:



| [**AVEncCommonRateControlMode**](avenccommonratecontrolmode-property.md) | **\_modalità a bitrate ENCAPIPARAM \_** |
|---------------------------------------------------------------------------|--------------------------------|
| **eAVEncCommonRateControlMode \_ CBR**                                      | **ConstantBitRate**            |
| **\_qualità eAVEncCommonRateControlMode**                                  | **VariableBitRatePeak**        |
| **\_PeakConstrainedVBR eAVEncCommonRateControlMode**                       | **VariableBitRatePeak**        |



 

### <a name="limitations"></a>Limitazioni

Attualmente il codificatore non supporta le funzionalità seguenti:

-   Generazione di pacchetti di flusso elementare (PES) in pacchetto.
-   Conversione della frequenza di frame. Il flusso di input deve avere una frequenza dei fotogrammi valida per un bitstream MPEG-2.
-   Estensioni della frequenza dei frame per MPEG-2 **( \_ \_ estensione della \_ frequenza** dei fotogrammi, estensione della frequenza dei fotogrammi **\_ \_ \_ d**).
-   Posizioni del buffer di ingresso/uscita (VBV) per una clip.
-   Inserimento dei dati riga 21 (informazioni sulla didascalia chiusa) nel flusso elementare del video.
-   Impostazione del campo **\_ codice ora** a 25 bit nell'intestazione GOP per MPEG-2.
-   Filtro di Denoise.
-   DRM (Digital Rights Management).

Il codificatore introduce una latenza di codifica di almeno un GOP.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, Windows 7 Ultimate \[ desktop apps\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl>                                                                                       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Filtri DirectShow](directshow-filters.md)
</dt> <dt>

[**Tipi di supporti di Demultiplexer MPEG-2**](mpeg-2-demultiplexer-media-types.md)
</dt> </dl>

 

 
