---
description: 'Il Microsoft Media Foundation video H.264 è una trasformazione Media Foundation che supporta i profili H.264 seguenti:'
ms.assetid: 4d4c768f-b76a-40ca-8736-2f592a4f4cc4
title: Codificatore video H.264
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 875974c53be265fbcace8cf99e2bdd78d69cdda5
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467528"
---
# <a name="h264-video-encoder"></a>Codificatore video H.264

Il Microsoft Media Foundation video H.264 è una trasformazione [Media Foundation](media-foundation-transforms.md) che supporta i profili H.264 seguenti:

-   Profilo di base
-   Main Profile
-   Profilo elevato (richiede Windows 8)

Il codificatore video H.264 espone le interfacce seguenti:

-   [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi)
-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="input-types"></a>Tipi di input

Il tipo di supporto di input deve avere uno dei sottotipi seguenti:

-   **MFVideoFormat_I420**
-   **MFVideoFormat_IYUV**
-   **MFVideoFormat_NV12**
-   **MFVideoFormat_YUY2**
-   **MFVideoFormat_YV12**

Per altre informazioni su questi sottotipi, vedere [GUID del sottotipo video.](video-subtype-guids.md)

Il tipo di output deve essere impostato prima del tipo di input. Fino a quando non viene impostato il tipo di output, il metodo [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) del codificatore **restituisce MF_E_TRANSFORM_TYPE_NOT_SET**.

## <a name="output-types"></a>Tipi di output

Il codificatore supporta un singolo sottotipo di output:

-   **MFVideoFormat_H264**

Impostare gli attributi seguenti sul tipo di supporto di output.




| Attributo | Descrizione | 
|-----------|-------------|
| <a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a> | Tipo principale. Deve essere <strong>MFMediaType_Video</strong>. | 
| <a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a> | Sottotipo video. Deve essere <strong>MFVideoFormat_H264</strong>. | 
| <a href="mf-mt-avg-bitrate-attribute.md"><strong>MF_MT_AVG_BITRATE</strong></a> | Velocità in bit codificata media, in bit al secondo. Deve essere maggiore di zero. | 
| <a href="mf-mt-frame-rate-attribute.md"><strong>MF_MT_FRAME_RATE</strong></a> | Frequenza dei fotogrammi. | 
| <a href="mf-mt-frame-size-attribute.md"><strong>MF_MT_FRAME_SIZE</strong></a> | Dimensioni del frame. | 
| <a href="mf-mt-interlace-mode-attribute.md"><strong>MF_MT_INTERLACE_MODE</strong></a> | Modalità interlacciato. | 
| <a href="mf-mt-mpeg2-profile-attribute.md"><strong>MF_MT_MPEG2_PROFILE</strong></a> | Profilo di codifica H.264.<br /> I valori supportati sono:<br /><ul><li><strong>eAVEncH264VProfile_Base</strong> (impostazione predefinita)</li><li><strong>eAVEncH264VProfile_Main</strong></li><li><strong>eAVEncH264VProfile_High</strong> (richiede Windows 8)</li></ul> | 
| <a href="mf-mt-mpeg2-level-attribute.md"><strong>MF_MT_MPEG2_LEVEL</strong></a> | facoltativo. Specifica il livello di codifica H.264.<br /> Il valore predefinito è -1, che indica che il codificatore selezionerà il livello di codifica.<br /> È consigliabile non impostare il livello nel tipo di supporto e consentire al codificatore di selezionare il livello. Il codificatore può derivare il livello appropriato per un determinato flusso video, tenendo conto dei vincoli di formato e delle caratteristiche del video. Per altre informazioni sui vincoli di profilo e livello, vedere l'allegato A di ITU-T H.264.<br /> | 
| <a href="mf-mt-pixel-aspect-ratio-attribute.md"><strong>MF_MT_PIXEL_ASPECT_RATIO</strong></a> | facoltativo. Specifica le proporzioni in pixel. Il valore predefinito è 1:1. | 




 

Dopo aver impostato il tipo di output, il codificatore video aggiorna il tipo aggiungendo [**l'MF_MT_MPEG_SEQUENCE_HEADER**](mf-mt-mpeg-sequence-header-attribute.md) attributo . Questo attributo contiene l'intestazione della sequenza.

## <a name="codec-properties"></a>Proprietà codec

Il codificatore H.264 implementa [**l'interfaccia ICodecAPI per**](/windows/win32/api/strmif/nn-strmif-icodecapi) l'impostazione dei parametri di codifica. Supporta le proprietà seguenti.

Per i requisiti del codec per la certificazione del codificatore HCK, vedere la **sezione Codificatore hardware certificato** più avanti.

Le proprietà seguenti sono supportate in Windows 7.



| Proprietà                                                                              | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CODECAPI_AVEncCommonRateControlMode**](../directshow/avenccommonratecontrolmode-property.md) | Imposta la modalità di controllo della frequenza. Vedere la sezione Osservazioni. La modalità predefinita è VBR (Unconstrained Variable Bit Rate).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**CODECAPI_AVEncCommonQuality**](../directshow/avenccommonquality-property.md)                 | Imposta il livello di qualità. Questa proprietà si applica quando la modalità di controllo della frequenza è vbr basata sulla qualità **(eAVEncCommonRateControlMode_Quality**). L'intervallo valido è compreso tra 1 e 100. Il valore predefinito è 70. <br/> Per impostare questo parametro, impostare la proprietà prima di chiamare [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype). <br/> Per impostare questo parametro in Windows 7, impostare la proprietà prima di chiamare [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype). Il codificatore ignora le modifiche dopo l'impostazione del tipo di output. <br/> In Windows 8, questa proprietà può essere impostata in qualsiasi momento durante la codifica. Le modifiche vengono applicate a partire dal frame di input successivo. <br/> Internamente, il codificatore converte questa proprietà in un [valore AVEncVideoEncodeQP.](codecapi-avencvideoencodeqp.md) <br/> |



 

Le proprietà seguenti richiedono Windows 8.




| Proprietà | Descrizione | 
|----------|-------------|
| <a href="codecapi-avencadaptivemode.md">CODECAPI_AVEncAdaptiveMode</a> | Imposta la modalità di codifica adattiva. Il codificatore H.264 supporta le modalità seguenti in Windows 8:<ul><li><strong>eAVEncAdaptiveMode_None</strong>. Nessuna codifica adattiva. (impostazione predefinita).</li><li><strong>eAVEncAdaptiveMode_FrameRate</strong>. Modificare in modo adattivo la frequenza dei fotogrammi.</li></ul><br /> | 
| <a href="/windows/desktop/DirectShow/avenccommonbuffersize-property">CODECAPI_AVEncCommonBufferSize</a> | Imposta le dimensioni del buffer, in byte, per la codifica CBR (Constant Bit Rate).<br /> L'intervallo valido è [1 ... 2°-1]. <br /> Richiede Windows 8. <br /> | 
| <a href="/windows/desktop/DirectShow/avenccommonmaxbitrate-property">CODECAPI_AVEncCommonMaxBitRate</a> | Per la codifica VBR vincolata, specifica la frequenza con cui il "bucket che perde" viene svuotato, in bit al secondo. Questa proprietà si applica quando la modalità di controllo della frequenza <strong>è eAVEncCommonRateControlMode_PeakConstrainedVBR</strong>. <br /> L'intervallo valido è [1 ... 2²²–1]. <br /> | 
| <a href="/windows/desktop/DirectShow/avenccommonmeanbitrate-property">CODECAPI_AVEncCommonMeanBitRate</a> | Imposta la velocità in bit media per il flusso di bit codificato, in bit al secondo. Questa proprietà viene ignorata se la modalità di controllo della frequenza è <strong>eAVEncCommonRateControlMode_Quality</strong>. <br /> L'intervallo valido è [1 ... 2²²–1]. <br /> Nelle modalità CBR e VBR senza vincoli, la velocità in bit media determina le dimensioni finali del file. In modalità CBR, la velocità in bit media è anche la velocità con cui i bit compressi vengono svuotati dal "bucket che perde". Per altre informazioni, vedere <a href="the-leaky-bucket-buffer-model.md">Il modello di buffer del bucket che</a>perde. <br /> In Windows 7, la velocità in bit media viene specificata <a href="mf-mt-avg-bitrate-attribute.md">dall'attributo MF_MT_AVG_BITRATE</a> sul tipo di supporto. <br /> In Windows 8, è possibile impostare la velocità in bit media usando l'attributo <a href="mf-mt-avg-bitrate-attribute.md">MF_MT_AVG_BITRATE</a> o la <a href="/windows/desktop/DirectShow/avenccommonmeanbitrate-property">proprietà</a> CODECAPI_AVEncCommonMeanBitRate. Se entrambe le proprietà sono impostate, CODECAPI_AVEncCommonMeanBitRate override. In Windows 8 è possibile impostare la velocità in bit media durante la codifica. Se la velocità in bit cambia, il codificatore usa la codifica adattiva.<br /> | 
| <a href="/windows/desktop/DirectShow/avenccommonqualityvsspeed-property">CODECAPI_AVEncCommonQualityVsSpeed</a> | Imposta il compromesso qualità/velocità. Intervallo valido:<ul><li>0-33: bassa complessità</li><li>34-66: complessità media (impostazione predefinita)</li><li>67-100: complessità elevata</li></ul><br /> Questo valore influisce sul modo in cui il codificatore esegue varie operazioni di codifica, ad esempio la compensazione del movimento. A livelli di complessità più elevati, il codificatore viene eseguito più lentamente, ma produce una qualità migliore alla stessa velocità in bit.<br /> | 
| <a href="codecapi-avench264cabacenable.md">CODECAPI_AVEncH264CABACEnable</a> | Abilita o disabilita CABAC (codifica aritmetica binaria context-adaptive) per la codifica entropia H.264. Il valore predefinito è <strong>VARIANT_FALSE</strong>. <br /> CABAC non viene usato per il profilo baseline.<br /> | 
| <a href="codecapi-avench264spsid.md">CODECAPI_AVEncH264SPSID</a> | Imposta il valore di <strong>seq_parameter_set_id</strong> nell'unità NAL SPS del flusso di bit H.264. <br /> | 
| <a href="/windows/desktop/DirectShow/avencmpvdefaultbpicturecount-property">CODECAPI_AVEncMPVDefaultBPictureCount</a> | Imposta il numero massimo di fotogrammi B consecutivi nel flusso di bit di output. I valori validi sono:<ul><li>0: non usare fotogrammi B (impostazione predefinita).</li><li>1: usare un frame B.</li><li>2: usare due fotogrammi B.</li></ul>Per impostare questo parametro, impostare la proprietà prima di chiamare <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype"><strong>IMFTransform::SetOutputType</strong></a>. <br /> Per Profilo di base, il numero di fotogrammi B è sempre zero. Il codificatore eseguirà l'override di valori diversi da zero.<br /> Per altri profili H.264, se questa proprietà è diversa da zero, il modello di codifica è IBBPBBP, dove il numero massimo di fotogrammi B consecutivi è uguale a <a href="/windows/desktop/DirectShow/avencmpvdefaultbpicturecount-property">CODECAPI_AVEncMPVDefaultBPictureCount</a>. <br /> | 
| <a href="/windows/desktop/DirectShow/avencmpvgopsize-property">CODECAPI_AVEncMPVGOPSize</a> | Imposta il numero di immagini da un'intestazione GOP alla successiva, incluso l'ancoraggio iniziale ma non quello seguente. <br /> L'intervallo valido è [0 ... 2²²–1]. Se zero, il codificatore seleziona le dimensioni GOP. Il valore predefinito è zero. <br /> | 
| <a href="codecapi-avencnumworkerthreads.md">CODECAPI_AVEncNumWorkerThreads</a> | Imposta il numero di thread di lavoro utilizzati da un codificatore.<br /> L'intervallo valido è compreso tra 0 e 16. Se zero, il codificatore seleziona il numero di thread. <br /> | 
| <a href="codecapi-avencvideocontenttype.md">CODECAPI_AVEncVideoContentType</a> | Indica il tipo di contenuto video.<br /> | 
| <a href="codecapi-avencvideoencodeqp.md">CODECAPI_AVEncVideoEncodeQP</a> | Intervallo valido: 16-51. Il valore predefinito è 24. <br /> Questa proprietà si applica quando la modalità di controllo della frequenza è <strong>eAVEncCommonRateControlMode_Quality</strong>. <br /> Questa proprietà configura la stessa impostazione di codifica di <a href="/windows/desktop/DirectShow/avenccommonquality-property"><strong>AVEncCommonQuality</strong></a>. TUTTAVIA, <a href="codecapi-avencvideoencodeqp.md">AVEncVideoEncodeQP</a> consente all'applicazione di specificare direttamente il valore di QP. Se entrambe le proprietà sono impostate, AVEncVideoEncodeQP esegue l'override. <br /> Il valore predefinito 24 corrisponde al valore predefinito 70 per <a href="/windows/desktop/DirectShow/avenccommonquality-property"><strong>l'impostazione AVEncCommonQuality.</strong></a><br /> | 
| <a href="codecapi-avencvideoforcekeyframe.md">CODECAPI_AVEncVideoForceKeyFrame</a> | Forza il codificatore a codificare il fotogramma successivo come fotogramma chiave.<br /> | 
| <a href="codecapi-avencvideominqp.md">CODECAPI_AVEncVideoMinQP</a> | Intervallo valido: 0-51. Il valore predefinito è 0. <br /> Questa proprietà si applica a tutte le modalità di controllo della frequenza. Il codificatore non deve produrre un valore QP inferiore a quello specificato dalla CODECAPI_AVEncVideoMinQP <a href="codecapi-avencvideominqp.md">proprietà</a> .<br /> | 
| <a href="codecapi-avlowlatencymode.md">CODECAPI_AVLowLatencyMode</a> | Abilita o disabilita la modalità a bassa latenza. Vedere "Multithreading" nella sezione Osservazioni.<br /> | 




 

## <a name="remarks"></a>Commenti

Il codificatore supporta le modalità di controllo della frequenza seguenti.



| Mode                                  | Costante                                            | Descrizione                                                                                                                                                                                                                                         |
|---------------------------------------|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Velocità in bit costante (CBR)               | **eAVEncCommonRateControlMode_CBR**                | Il codificatore tenta di ottenere una velocità in bit costante, usando un modello "bucket che perde". La velocità in bit di destinazione viene specificata dalla [proprietà CODECAPI_AVEncCommonMeanBitRate](../directshow/avenccommonmeanbitrate-property.md) destinazione. <br/> Richiede Windows 8. <br/> |
| Velocità in bit variabile vincolata (VBR)   | **eAVEncCommonRateControlMode_PeakConstrainedVBR** | Il codificatore usa un modello "bucket che perde" con una velocità in bit di picco. La frequenza di svuotamento per il bucket che perde viene specificata dalla [CODECAPI_AVEncCommonMaxBitRate](../directshow/avenccommonmaxbitrate-property.md) proprietà . <br/> Richiede Windows 8. <br/>     |
| Velocità in bit variabile basata sulla qualità (VBR) | **eAVEncCommonRateControlMode_Quality**            | Il codificatore tenta di ottenere un livello di qualità costante, dato dalla [**proprietà AVEncCommonQuality.**](../directshow/avenccommonquality-property.md)                                                                                                           |
| VBR senza vincoli                     | **eAVEncCommonRateControlMode_UnconstrainedVBR**   | Il codificatore tenta di ottenere la velocità in bit di destinazione specificata [**dall'attributo MF_MT_AVG_BITRATE**](mf-mt-avg-bitrate-attribute.md) nel tipo di supporto di output. Si tratta della modalità predefinita.                                                              |



 

Le modalità CBR e VBR vincolate richiedono Windows 8.

In Windows 8 codificatore imposta gli attributi seguenti negli esempi di output:

-   [MFSampleExtension_DecodeTimestamp](mfsampleextension-decodetimestamp.md)
-   [MFSampleExtension_VideoEncodePictureType](mfsampleextension-videoencodepicturetype.md)
-   [MFSampleExtension_VideoEncodeQP](mfsampleextension-videoencodeqp.md)

> [!Note]  
> Una versione precedente della documentazione ha erroneamente dichiarato che il codificatore è supportato Windows Server 2008 R2.

 

### <a name="multithreading"></a>Multithreading

In Windows 8, il codificatore supporta due modalità di codifica:

-   **Codifica della sezione.** In questa modalità, le sezioni vengono codificate in parallelo. Ogni sezione viene codificata in un thread diverso. Questa modalità ha bassa latenza, perché una singola immagine è codificata in parallelo. Tuttavia, questo approccio non viene ridimensionato con l'aumentare del numero di core, perché il numero di sezioni è delimitato dal numero di righe di macroblock nell'immagine di input.
-   **Codifica multi-frame.** In questa modalità, il codificatore accetta più fotogrammi di input e li codifica in parallelo. Questa modalità è più scalabile in un ambiente multicore, ma introduce una maggiore latenza.

Per impostazione predefinita, il codificatore viene codificato in sezioni, per ridurre al minimo la latenza. Per abilitare la codifica multi-frame, impostare [la proprietà CODECAPI_AVLowLatencyMode](codecapi-avlowlatencymode.md) su **VARIANT_FALSE**.

Per impostare il numero di thread di lavoro usati dal codificatore, impostare la [CODECAPI_AVEncNumWorkerThreads](codecapi-avencnumworkerthreads.md) proprietà .

In Windows 7, il codificatore usa sempre la codifica delle sezioni.

### <a name="certified-hardware-encoder"></a>Codificatore hardware certificato

Se è presente un codificatore hardware certificato, verrà in genere usato al posto del codificatore di sistema della posta in arrivo per Media Foundation scenari correlati. I codificatori certificati sono necessari per supportare un determinato set **di proprietà ICodecAPI** e possono facoltativamente supportare un altro set di proprietà. Il processo di certificazione deve garantire che le proprietà richieste siano supportate correttamente e, se è supportata una proprietà facoltativa, che sia supportata correttamente.

Di seguito è riportato il set di proprietà **ICodecAPI** obbligatorie e facoltative che i codificatori devono superare la certificazione del codificatore HCK.

Le proprietà Windows 8 e Windows 8.1 **ICodecAPI** sono obbligatorie:

-   [CODECAPI_AVEncCommonRateControlMode](../directshow/avenccommonratecontrolmode-property.md)
-   [CODECAPI_AVEncCommonQuality](../directshow/avenccommonquality-property.md)
-   [CODECAPI_AVEncCommonQualityVsSpeed](../directshow/avenccommonqualityvsspeed-property.md)
-   [CODECAPI_AVEncCommonMeanBitRate](../directshow/avenccommonmeanbitrate-property.md)
-   [CODECAPI_AVEncCommonMaxBitRate](../directshow/avenccommonmaxbitrate-property.md)
-   [CODECAPI_AVEncCommonBufferSize](../directshow/avenccommonbuffersize-property.md)
-   [CODECAPI_AVEncMPVGOPSize](../directshow/avencmpvgopsize-property.md)
-   [CODECAPI_AVEncVideoEncodeQP](codecapi-avencvideoencodeqp.md)
-   [CODECAPI_AVEncVideoForceKeyFrame](codecapi-avencvideoforcekeyframe.md)

Le proprietà Windows 8.1 **ICodecAPI** sono facoltative, ma vengono testate in HCK, se supportate.

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

Le proprietà Windows 8 e Windows 8.1 **ICodecAPI** sono facoltative, ma vengono testate in HCK, se supportate.

-   [CODECAPI_AVEncVideoTemporalLayerCount](codecapi-avencvideotemporallayercount.md) (statico)
-   [CODECAPI_AVLowLatencyMode](codecapi-avlowlatencymode.md)

Le proprietà **ICodecAPI** seguenti sono facoltative. Non vengono testati in HCK.

-   [CODECAPI_AVEncMPVDefaultBPictureCount](../directshow/avencmpvdefaultbpicturecount-property.md)

## <a name="requirements"></a>Requisiti



| Requisito | valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                |
| DLL<br/>                      | <dl> <dt>Mfh264enc.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti codec](codecobjects.md)
</dt> <dt>

[Supporto mpeg-4 in Media Foundation](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[Formati multimediali supportati in Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> <dt>

[Tipi di supporti video](video-media-types.md)
</dt> </dl>

 

 
