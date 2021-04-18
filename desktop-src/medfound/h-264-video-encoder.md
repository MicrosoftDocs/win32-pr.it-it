---
description: 'Il codificatore Microsoft Media Foundation H. 264 video è una trasformazione Media Foundation che supporta i profili H. 264 seguenti:'
ms.assetid: 4d4c768f-b76a-40ca-8736-2f592a4f4cc4
title: Codificatore video H. 264
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5631239e9db0ddf078848bc3c4a04282e7e79990
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308773"
---
# <a name="h264-video-encoder"></a>Codificatore video H. 264

Il codificatore Microsoft Media Foundation H. 264 video è una [trasformazione Media Foundation](media-foundation-transforms.md) che supporta i profili h. 264 seguenti:

-   Profilo di base
-   Main Profile
-   Profilo elevato (richiede Windows 8)

Il codificatore video H. 264 espone le interfacce seguenti:

-   [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi)
-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="input-types"></a>Tipi di input

Il tipo di supporto di input deve avere uno dei seguenti sottotipi:

-   **MFVideoFormat_I420**
-   **MFVideoFormat_IYUV**
-   **MFVideoFormat_NV12**
-   **MFVideoFormat_YUY2**
-   **MFVideoFormat_YV12**

Per altre informazioni su questi sottotipi, vedere [GUID del sottotipo video](video-subtype-guids.md).

Il tipo di output deve essere impostato prima del tipo di input. Fino a quando non viene impostato il tipo di output, il metodo [**IMFTransform:: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) del codificatore restituisce **MF_E_TRANSFORM_TYPE_NOT_SET**.

## <a name="output-types"></a>Tipi di output

Il codificatore supporta un solo sottotipo di output:

-   **MFVideoFormat_H264**

Impostare gli attributi seguenti sul tipo di supporto di output.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Attributo</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></td>
<td>Tipo principale. Deve essere <strong>MFMediaType_Video</strong>.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></td>
<td>Sottotipo video. Deve essere <strong>MFVideoFormat_H264</strong>.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-avg-bitrate-attribute.md"><strong>MF_MT_AVG_BITRATE</strong></a></td>
<td>Velocità in bit codificata media, in bit al secondo. Deve essere maggiore di zero.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-frame-rate-attribute.md"><strong>MF_MT_FRAME_RATE</strong></a></td>
<td>Frequenza di fotogrammi.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-frame-size-attribute.md"><strong>MF_MT_FRAME_SIZE</strong></a></td>
<td>Dimensioni del frame.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-interlace-mode-attribute.md"><strong>MF_MT_INTERLACE_MODE</strong></a></td>
<td>Modalità interlacciamento.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-mpeg2-profile-attribute.md"><strong>MF_MT_MPEG2_PROFILE</strong></a></td>
<td>Profilo di codifica H. 264.<br/> I valori supportati sono:<br/>
<ul>
<li><strong>eAVEncH264VProfile_Base</strong> (impostazione predefinita)</li>
<li><strong>eAVEncH264VProfile_Main</strong></li>
<li><strong>eAVEncH264VProfile_High</strong> (richiede Windows 8)</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="mf-mt-mpeg2-level-attribute.md"><strong>MF_MT_MPEG2_LEVEL</strong></a></td>
<td>facoltativo. Specifica il livello di codifica H. 264.<br/> Il valore predefinito è-1, che indica che il codificatore selezionerà il livello di codifica.<br/> È consigliabile non impostare il livello nel tipo di supporto e consentire al codificatore di selezionare il livello. Il codificatore può derivare il livello appropriato per un determinato flusso video, prendendo in considerazione i vincoli di formato e le caratteristiche del video. Per ulteriori informazioni sui vincoli di profilo e di livello, vedere l'allegato A di ITU-T H. 264.<br/></td>
</tr>
<tr class="odd">
<td><a href="mf-mt-pixel-aspect-ratio-attribute.md"><strong>MF_MT_PIXEL_ASPECT_RATIO</strong></a></td>
<td>facoltativo. Specifica le proporzioni in pixel. Il valore predefinito è 1:1.</td>
</tr>
</tbody>
</table>



 

Dopo aver impostato il tipo di output, il codificatore video aggiorna il tipo aggiungendo l'attributo [**MF_MT_MPEG_SEQUENCE_HEADER**](mf-mt-mpeg-sequence-header-attribute.md) . Questo attributo contiene l'intestazione della sequenza.

## <a name="codec-properties"></a>Proprietà codec

Il codificatore H. 264 implementa l'interfaccia [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) per l'impostazione dei parametri di codifica. Supporta le proprietà seguenti.

Per i requisiti di codec per la certificazione del codificatore HCK, vedere la sezione relativa al **codificatore hardware certificato** di seguito.

Le proprietà seguenti sono supportate in Windows 7.



| Proprietà                                                                              | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CODECAPI_AVEncCommonRateControlMode**](../directshow/avenccommonratecontrolmode-property.md) | Imposta la modalità di controllo della frequenza. Vedere la sezione Osservazioni. La modalità predefinita è la velocità in bit variabile (VBR) non vincolata.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**CODECAPI_AVEncCommonQuality**](../directshow/avenccommonquality-property.md)                 | Imposta il livello di qualità. Questa proprietà si applica quando la modalità di controllo della velocità è VBR basata sulla qualità (**eAVEncCommonRateControlMode_Quality**). L'intervallo valido è compreso tra 1 e 100. Il valore predefinito è 70. <br/> Per impostare questo parametro, impostare la proprietà prima di chiamare [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype). <br/> Per impostare questo parametro in Windows 7, impostare la proprietà prima di chiamare [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype). Il codificatore ignora le modifiche dopo l'impostazione del tipo di output. <br/> In Windows 8, questa proprietà può essere impostata in qualsiasi momento durante la codifica. Le modifiche vengono applicate a partire dal frame di input successivo. <br/> Internamente, il codificatore converte questa proprietà in un valore [AVEncVideoEncodeQP](codecapi-avencvideoencodeqp.md) . <br/> |



 

Per le seguenti proprietà è necessario Windows 8.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Proprietà</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="codecapi-avencadaptivemode.md">CODECAPI_AVEncAdaptiveMode</a></td>
<td>Imposta la modalità di codifica adattiva. Il codificatore H. 264 supporta le modalità seguenti in Windows 8:
<ul>
<li><strong>eAVEncAdaptiveMode_None</strong>. Nessuna codifica adattiva. (impostazione predefinita).</li>
<li><strong>eAVEncAdaptiveMode_FrameRate</strong>. In modo adattivo modificare la frequenza dei fotogrammi.</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/DirectShow/avenccommonbuffersize-property">CODECAPI_AVEncCommonBufferSize</a></td>
<td>Imposta la dimensione del buffer, in byte, per la codifica di velocità in bit costante (CBR).<br/> L'intervallo valido è [1... 2 ³ ² – 1]. <br/> Richiede Windows 8. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/avenccommonmaxbitrate-property">CODECAPI_AVEncCommonMaxBitRate</a></td>
<td>Per la codifica VBR vincolata, specifica la frequenza con cui &quot; &quot; viene svuotato il bucket di perdita, in bit al secondo. Questa proprietà si applica quando la modalità di controllo della velocità è <strong>eAVEncCommonRateControlMode_PeakConstrainedVBR</strong>. <br/> L'intervallo valido è [1... 2 ³ ² – 1]. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/DirectShow/avenccommonmeanbitrate-property">CODECAPI_AVEncCommonMeanBitRate</a></td>
<td>Imposta la velocità in bit media per il flusso di bit codificato, in bit al secondo. Questa proprietà viene ignorata se la modalità di controllo della velocità è <strong>eAVEncCommonRateControlMode_Quality</strong>. <br/> L'intervallo valido è [1... 2 ³ ² – 1]. <br/> Nelle modalità CBR e VBR non vincolate la velocità in bit media determina la dimensione finale del file. In modalità CBR la velocità in bit media è anche la velocità con cui i bit compressi vengono svuotati dal &quot; bucket di perdita. &quot; per ulteriori informazioni, vedere <a href="the-leaky-bucket-buffer-model.md">il modello di buffer di bucket a perdita</a>. <br/> In Windows 7, la velocità in bit media viene specificata dall'attributo <a href="mf-mt-avg-bitrate-attribute.md">MF_MT_AVG_BITRATE</a> nel tipo di supporto. <br/> In Windows 8 è possibile impostare la velocità in bit media usando l'attributo <a href="mf-mt-avg-bitrate-attribute.md">MF_MT_AVG_BITRATE</a> o la proprietà <a href="/windows/desktop/DirectShow/avenccommonmeanbitrate-property">CODECAPI_AVEncCommonMeanBitRate</a> . Se entrambe le impostazioni sono impostate, CODECAPI_AVEncCommonMeanBitRate esegue l'override di. In Windows 8 è possibile impostare la velocità in bit media durante la codifica. Se la velocità in bit viene modificata, il codificatore utilizza la codifica adattiva.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/avenccommonqualityvsspeed-property">CODECAPI_AVEncCommonQualityVsSpeed</a></td>
<td>Imposta il compromesso di qualità/velocità. Intervallo valido:
<ul>
<li>0 – 33: complessità bassa</li>
<li>34 – 66: complessità media (impostazione predefinita)</li>
<li>67 – 100: complessità elevata</li>
</ul>
<br/> Questo valore influiscono sul modo in cui il codificatore esegue diverse operazioni di codifica, ad esempio la compensazione del movimento. A livelli di complessità più elevati, il codificatore viene eseguito più lentamente, ma produce una qualità migliore con la stessa velocità in bit.<br/></td>
</tr>
<tr class="even">
<td><a href="codecapi-avench264cabacenable.md">CODECAPI_AVEncH264CABACEnable</a></td>
<td>Abilita o Disabilita CABAC (codice aritmetico binario adattivo per il contesto) per la codifica dell'entropia H. 264. Il valore predefinito è <strong>VARIANT_FALSE</strong>. <br/> CABAC non viene usato per il profilo di base.<br/></td>
</tr>
<tr class="odd">
<td><a href="codecapi-avench264spsid.md">CODECAPI_AVEncH264SPSID</a></td>
<td>Imposta il valore di <strong>seq_parameter_set_id</strong> nell'unità SPS nal del Bitstream H. 264. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/DirectShow/avencmpvdefaultbpicturecount-property">CODECAPI_AVEncMPVDefaultBPictureCount</a></td>
<td>Imposta il numero massimo di fotogrammi B consecutivi nel bitstream di output. I valori validi sono:
<ul>
<li>0: non usare i frame B (impostazione predefinita).</li>
<li>1: usare un frame B.</li>
<li>2: usare due fotogrammi B.</li>
</ul>
Per impostare questo parametro, impostare la proprietà prima di chiamare <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype"><strong>IMFTransform:: SetOutputType</strong></a>. <br/> Per il profilo di base, il numero di fotogrammi B è sempre zero. Il codificatore eseguirà l'override dei valori diversi da zero.<br/> Per gli altri profili H. 264, se questa proprietà è diversa da zero, il modello di codifica è IBBPBBP, in cui il numero massimo di fotogrammi B consecutivi è uguale a <a href="/windows/desktop/DirectShow/avencmpvdefaultbpicturecount-property">CODECAPI_AVEncMPVDefaultBPictureCount</a>. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/avencmpvgopsize-property">CODECAPI_AVEncMPVGOPSize</a></td>
<td>Imposta il numero di immagini da un'intestazione GOP alla successiva, incluso l'ancoraggio principale ma non quello seguente. <br/> L'intervallo valido è [0... 2 ³ ² – 1]. Se il valore è zero, il codificatore seleziona la dimensione GOP. Il valore predefinito è zero. <br/></td>
</tr>
<tr class="even">
<td><a href="codecapi-avencnumworkerthreads.md">CODECAPI_AVEncNumWorkerThreads</a></td>
<td>Imposta il numero di thread di lavoro utilizzati da un codificatore.<br/> L'intervallo valido è compreso tra 0 e 16. Se è zero, il codificatore seleziona il numero di thread. <br/></td>
</tr>
<tr class="odd">
<td><a href="codecapi-avencvideocontenttype.md">CODECAPI_AVEncVideoContentType</a></td>
<td>Indica il tipo di contenuto video.<br/></td>
</tr>
<tr class="even">
<td><a href="codecapi-avencvideoencodeqp.md">CODECAPI_AVEncVideoEncodeQP</a></td>
<td>Intervallo valido: 16-51. Il valore predefinito è 24. <br/> Questa proprietà si applica quando la modalità di controllo della velocità è <strong>eAVEncCommonRateControlMode_Quality</strong>. <br/> Questa proprietà configura la stessa impostazione di codifica di <a href="/windows/desktop/DirectShow/avenccommonquality-property"><strong>AVEncCommonQuality</strong></a>. Tuttavia, <a href="codecapi-avencvideoencodeqp.md">AVEncVideoEncodeQP</a> consente all'applicazione di specificare direttamente il valore di QP. Se entrambe le proprietà sono impostate, AVEncVideoEncodeQP esegue l'override di. <br/> Il valore predefinito di 24 corrisponde al valore predefinito 70 per l'impostazione <a href="/windows/desktop/DirectShow/avenccommonquality-property"><strong>AVEncCommonQuality</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="codecapi-avencvideoforcekeyframe.md">CODECAPI_AVEncVideoForceKeyFrame</a></td>
<td>Impone al codificatore di codificare il fotogramma successivo come fotogramma chiave.<br/></td>
</tr>
<tr class="even">
<td><a href="codecapi-avencvideominqp.md">CODECAPI_AVEncVideoMinQP</a></td>
<td>Intervallo valido: 0 – 51. Il valore predefinito è 0. <br/> Questa proprietà si applica a tutte le modalità di controllo della frequenza. Il codificatore non deve produrre un valore QP inferiore a quello specificato dalla proprietà <a href="codecapi-avencvideominqp.md">CODECAPI_AVEncVideoMinQP</a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="codecapi-avlowlatencymode.md">CODECAPI_AVLowLatencyMode</a></td>
<td>Abilita o Disabilita la modalità a bassa latenza. Vedere &quot; multithreading &quot; nella sezione Osservazioni.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Commenti

Il codificatore supporta le modalità di controllo della frequenza seguenti.



| Modalità                                  | Costante                                            | Descrizione                                                                                                                                                                                                                                         |
|---------------------------------------|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Velocità in bit costante (CBR)               | **eAVEncCommonRateControlMode_CBR**                | Il codificatore tenta di ottenere una velocità in bit costante, usando un modello "bucket Leak". La velocità in bit di destinazione viene fornita dalla proprietà [CODECAPI_AVEncCommonMeanBitRate](../directshow/avenccommonmeanbitrate-property.md) . <br/> Richiede Windows 8. <br/> |
| Velocità in bit variabile vincolata (VBR)   | **eAVEncCommonRateControlMode_PeakConstrainedVBR** | Il codificatore usa un modello di "bucket a perdita" con una velocità in bit massima. La velocità di svuotamento per il bucket perso è determinata dalla proprietà [CODECAPI_AVEncCommonMaxBitRate](../directshow/avenccommonmaxbitrate-property.md) . <br/> Richiede Windows 8. <br/>     |
| Velocità in bit della variabile basata sulla qualità (VBR) | **eAVEncCommonRateControlMode_Quality**            | Il codificatore tenta di ottenere un livello di qualità costante, fornito dalla proprietà [**AVEncCommonQuality**](../directshow/avenccommonquality-property.md) .                                                                                                           |
| VBR non vincolato                     | **eAVEncCommonRateControlMode_UnconstrainedVBR**   | Il codificatore tenta di ottenere la velocità in bit di destinazione fornita dall'attributo [**MF_MT_AVG_BITRATE**](mf-mt-avg-bitrate-attribute.md) nel tipo di supporto di output. Si tratta della modalità predefinita.                                                              |



 

Le modalità CBR e VBR vincolate richiedono Windows 8.

In Windows 8, il codificatore imposta gli attributi seguenti sugli esempi di output:

-   [MFSampleExtension_DecodeTimestamp](mfsampleextension-decodetimestamp.md)
-   [MFSampleExtension_VideoEncodePictureType](mfsampleextension-videoencodepicturetype.md)
-   [MFSampleExtension_VideoEncodeQP](mfsampleextension-videoencodeqp.md)

> [!Note]  
> Una versione precedente della documentazione ha erroneamente indicato che il codificatore è supportato in Windows Server 2008 R2.

 

### <a name="multithreading"></a>Multithreading

In Windows 8 il codificatore supporta due modalità di codifica:

-   **Codifica Slice.** In questa modalità, le sezioni vengono codificate in parallelo. Ogni sezione è codificata in un thread diverso. Questa modalità presenta una bassa latenza, perché una singola immagine è codificata in parallelo. Questo approccio, tuttavia, non viene ridimensionato con l'aumentare del numero di core, perché il numero di sezioni è limitato dal numero di righe di macroblocco nell'immagine di input.
-   **Codifica multiframe.** In questa modalità, il codificatore accetta più frame di input e li codifica in parallelo. Questa modalità offre una migliore scalabilità in un ambiente multicore, ma introduce più latenza.

Per ridurre al minimo la latenza, l'impostazione predefinita del codificatore è la codifica Slice. Per abilitare la codifica multiframe, impostare la proprietà [CODECAPI_AVLowLatencyMode](codecapi-avlowlatencymode.md) su **VARIANT_FALSE**.

Per impostare il numero di thread di lavoro utilizzati dal codificatore, impostare la proprietà [CODECAPI_AVEncNumWorkerThreads](codecapi-avencnumworkerthreads.md) .

In Windows 7, il codificatore usa sempre la codifica Slice.

### <a name="certified-hardware-encoder"></a>Codificatore hardware certificato

Se è presente un codificatore hardware certificato, in genere verrà usato al posto del codificatore di sistema della posta in arrivo per Media Foundation scenari correlati. I codificatori certificati sono necessari per supportare un determinato set di proprietà **ICodecAPI** e possono facoltativamente supportare un altro set di proprietà. Il processo di certificazione deve garantire che le proprietà obbligatorie siano supportate correttamente e, se è supportata una proprietà facoltativa, anche se è supportata correttamente.

Di seguito è riportato il set di proprietà **ICodecAPI** obbligatorie e facoltative per i codificatori per passare la certificazione del codificatore HCK.

Sono necessarie le seguenti proprietà di Windows 8 e Windows 8.1 **ICodecAPI** :

-   [CODECAPI_AVEncCommonRateControlMode](../directshow/avenccommonratecontrolmode-property.md)
-   [CODECAPI_AVEncCommonQuality](../directshow/avenccommonquality-property.md)
-   [CODECAPI_AVEncCommonQualityVsSpeed](../directshow/avenccommonqualityvsspeed-property.md)
-   [CODECAPI_AVEncCommonMeanBitRate](../directshow/avenccommonmeanbitrate-property.md)
-   [CODECAPI_AVEncCommonMaxBitRate](../directshow/avenccommonmaxbitrate-property.md)
-   [CODECAPI_AVEncCommonBufferSize](../directshow/avenccommonbuffersize-property.md)
-   [CODECAPI_AVEncMPVGOPSize](../directshow/avencmpvgopsize-property.md)
-   [CODECAPI_AVEncVideoEncodeQP](codecapi-avencvideoencodeqp.md)
-   [CODECAPI_AVEncVideoForceKeyFrame](codecapi-avencvideoforcekeyframe.md)

Le seguenti Windows 8.1 proprietà **ICodecAPI** sono facoltative, ma sono testate in HCK se supportate.

-   [CODECAPI_AVEncVideoMinQP](codecapi-avencvideominqp.md)
-   [CODECAPI_AVEncVideoLTRBufferControl](codecapi-avencvideoltrbuffercontrol.md)
-   [CODECAPI_AVEncVideoMarkLTRFrame](codecapi-avencvideomarkltrframe.md)
-   [CODECAPI_AVEncVideoUseLTRFrame](codecapi-avencvideouseltrframe.md)
-   [CODECAPI_AVEncVideoEncodeFrameTypeQP](codecapi-avencvideoencodeframetypeqp.md)
-   [CODECAPI_AVEncSliceControlMode](codecapi-avencslicecontrolmode.md)
-   [CODECAPI_AVEncSliceControlSize](codecapi-avencslicecontrolsize.md)
-   [CODECAPI_AVEncVideoMaxNumRefFrame](codecapi-avencvideomaxnumrefframe.md)
-   [CODECAPI_AVEncVideoMeanAbsoluteDifference](codecapi-avencvideomeanabsolutedifference.md)
-   [CODECAPI_AVEncVideoMaxQP](codecapi-avencvideomaxqp.md)
-   [CODECAPI_AVEncVideoROIEnabled](codecapi-avencvideoroienabled.md)
-   [CODECAPI_AVEncVideoTemporalLayerCount](codecapi-avencvideotemporallayercount.md) (dinamico)
-   [CODECAPI_AVEncH264CABACEnable](codecapi-avench264cabacenable.md)

Le seguenti proprietà di Windows 8 e Windows 8.1 **ICodecAPI** sono facoltative, ma sono testate in HCK se supportate.

-   [CODECAPI_AVEncVideoTemporalLayerCount](codecapi-avencvideotemporallayercount.md) (statico)
-   [CODECAPI_AVLowLatencyMode](codecapi-avlowlatencymode.md)

Le proprietà **ICodecAPI** seguenti sono facoltative. Non vengono testati in HCK.

-   [CODECAPI_AVEncMPVDefaultBPictureCount](../directshow/avencmpvdefaultbpicturecount-property.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                               |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                |
| DLL<br/>                      | <dl> <dt>Mfh264enc.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti codec](codecobjects.md)
</dt> <dt>

[Supporto MPEG-4 in Media Foundation](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[Formati multimediali supportati in Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> <dt>

[Tipi di supporti video](video-media-types.md)
</dt> </dl>

 

 
