---
description: Il Media Foundation video H.265 è una trasformazione Media Foundation che supporta la codifica del contenuto nel formato H.265/HEVC.
ms.assetid: 790CFB39-6FC0-432D-A434-5262C30EABF4
title: Codificatore video H.265/HEVC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b95eee96d3313df2604919883cf631b0aef999f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467488"
---
# <a name="h265--hevc-video-encoder"></a>Codificatore video H.265/HEVC

Il Media Foundation video H.265 è un [Media Foundation Transform](media-foundation-transforms.md) che supporta la codifica del contenuto nel formato H.265/HEVC. Il codificatore supporta i profili seguenti:

-   Main Profile

Il codificatore video H.265 espone le interfacce seguenti:

-   [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi)
-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="input-types"></a>Tipi di input

Il tipo di supporto di input deve avere uno dei sottotipi seguenti:

-   **MFVideoFormat \_ IYUV**
-   **MFVideoFormat \_ NV12**
-   **MFVideoFormat \_ YUY2**
-   **MFVideoFormat \_ YV12**

Per altre informazioni su questi sottotipi, vedere [GUID del sottotipo video.](video-subtype-guids.md)

Il tipo di output deve essere impostato prima del tipo di input. Fino a quando non viene impostato il tipo di output, il metodo [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) del codificatore restituisce **MF \_ E TRANSFORM TYPE NOT \_ \_ \_ \_ SET**.

## <a name="output-types"></a>Tipi di output

Il codificatore supporta un singolo sottotipo di output:

-   **MFVideoFormat \_ H265**

Impostare gli attributi seguenti sul tipo di supporto di output.




| Attributo | Descrizione | 
|-----------|-------------|
| <a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a> | Tipo principale. Deve essere <strong>MFMediaType_Video</strong>. | 
| <a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a> | Sottotipo video. Deve essere <strong>MFVideoFormat_HEVC</strong>. | 
| <a href="mf-mt-avg-bitrate-attribute.md"><strong>MF_MT_AVG_BITRATE</strong></a> | Velocità in bit codificata media, in bit al secondo. Deve essere maggiore di zero. | 
| <a href="mf-mt-frame-rate-attribute.md"><strong>MF_MT_FRAME_RATE</strong></a> | Frequenza dei fotogrammi. | 
| <a href="mf-mt-frame-size-attribute.md"><strong>MF_MT_FRAME_SIZE</strong></a> | Dimensioni del frame. | 
| <a href="mf-mt-interlace-mode-attribute.md"><strong>MF_MT_INTERLACE_MODE</strong></a> | Modalità interlacciato. | 
| <a href="mf-mt-video-profile.md">MF_MT_VIDEO_PROFILE</a> | Profilo di codifica H.265.<br /> I valori supportati sono: <br /><ul><li><strong>eAVEncH265VProfile_Main_420_8</strong></li></ul> | 
| <a href="mf-mt-mpeg2-level-attribute.md"><strong>MF_MT_MPEG2_LEVEL</strong></a> | Specifica il livello del video codificato. Per altre informazioni sui vincoli di profilo e livello, vedere l'allegato A di ITU-T H.265.<br /> | 
| <a href="mf-mt-pixel-aspect-ratio-attribute.md"><strong>MF_MT_PIXEL_ASPECT_RATIO</strong></a> | facoltativo. Specifica le proporzioni in pixel. Il valore predefinito è 1:1. | 




 

Dopo aver impostato il tipo di output, il codificatore video aggiorna il tipo aggiungendo l'attributo [**\_ MF MT \_ MPEG \_ SEQUENCE \_ HEADER.**](mf-mt-mpeg-sequence-header-attribute.md) Questo attributo contiene l'intestazione della sequenza.

## <a name="supported-imftransform-methods"></a>Metodi IMFTransform supportati

Per il codificatore H.265/HEVC sono supportati i metodi seguenti dell'interfaccia [**IMFTransform:**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

-   [**GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes)
-   [**GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype)
-   [**GetInputCurrentType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputcurrenttype)
-   [**GetInputStatus**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstatus)
-   [**GetInputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreaminfo)
-   [**GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype)
-   [**GetOutputCurrentType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputcurrenttype)
-   [**GetOutputStatus**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstatus)
-   [**GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo)
-   [**GetStreamCount**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamcount)
-   [**GetStreamLimits**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamlimits)
-   [**ProcessEvent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent)
-   [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage)
-   [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput)
-   [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)
-   [**SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype)
-   [**SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)
-   [**SetOutputBounds**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputbounds)

Tutti gli [**altri metodi IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) restituiranno l'errore E \_ NOTIMPL.

## <a name="supported-icodecapi-methods"></a>Metodi ICodecAPI supportati

Per il codificatore H.265/HEVC sono supportati i metodi seguenti dell'interfaccia [**ICodecAPI:**](/windows/win32/api/strmif/nn-strmif-icodecapi)

-   [**IsSupported**](/windows/win32/api/strmif/nf-strmif-icodecapi-issupported)
-   [**SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue)
-   [**Getvalue**](/windows/win32/api/strmif/nf-strmif-icodecapi-getvalue)
-   [**GetParameterRange**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparameterrange)
-   [**GetParameterValues**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparametervalues)

Tutti gli [**altri metodi ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) restituiranno l'errore E \_ NOTIMPL.

## <a name="codec-properties"></a>Proprietà codec

Il codificatore H.265 implementa [**l'interfaccia ICodecAPI per**](/windows/win32/api/strmif/nn-strmif-icodecapi) l'impostazione dei parametri di codifica. Supporta le proprietà seguenti.

Per i requisiti del codec per la certificazione del codificatore HCK, vedere la **sezione Codificatore hardware certificato** più avanti.




| Proprietà | Descrizione | 
|----------|-------------|
| <a href="/windows/desktop/DirectShow/avenccommonratecontrolmode-property"><strong>CODECAPI_AVEncCommonRateControlMode</strong></a> | Imposta la modalità di controllo della frequenza. Le modalità supportate sono:<br /><ul><li><strong>eAVEncCommonRateControlMode_CBR</strong></li><li><strong>eAVEncCommonRateControlMode_Quality</strong></li></ul>Se vengono specificate altre modalità, verrà <strong>eAVEncCommonRateControlMode_CBR</strong> controllo della frequenza.<br /> Si tratta di un VT_UI4 predefinito.<br /> | 
| <a href="/windows/desktop/DirectShow/avenccommonmeanbitrate-property">CODECAPI_AVEncCommonMeanBitRate</a> | Imposta la velocità in bit media per il flusso di bit codificato, in bit al secondo. <br /> L'intervallo valido è [1 ... 2°-1]. <br /> Si tratta di un VT_UI4 predefinito.<br /> | 
| <a href="/windows/desktop/DirectShow/avenccommonbuffersize-property">CODECAPI_AVEncCommonBufferSize</a> | Imposta le dimensioni del buffer, in byte, per la codifica CBR (Constant Bit Rate).<br /> L'intervallo valido è [1 ... 2°-1]. <br /> Si tratta di un VT_UI4 predefinito.<br /> | 
| <a href="/windows/desktop/DirectShow/avenccommonmaxbitrate-property">CODECAPI_AVEncCommonMaxBitRate</a> | Imposta la velocità in bit massima per le modalità di controllo della frequenza che consentono una velocità in bit di picco. <br /> L'intervallo valido è [1 ... 2°-1]. <br /> Si tratta di un VT_UI4 predefinito.<br /> | 
| <a href="/windows/desktop/DirectShow/avencmpvgopsize-property">CODECAPI_AVEncMPVGOPSize</a> | Imposta il numero di immagini da un'intestazione GOP alla successiva, incluso l'ancoraggio iniziale ma non quello seguente. <br /> L'intervallo valido è [0 ... 2°-1]. Se zero, il codificatore seleziona le dimensioni GOP. Il valore predefinito è zero. <br /> Si tratta di un VT_UI4 predefinito.<br /> | 
| <a href="codecapi-avlowlatencymode.md">CODECAPI_AVLowLatencyMode</a> | Abilita o disabilita la modalità a bassa latenza. <br /> Si tratta di un VT_BOOL predefinito.<br /> | 
| <a href="/windows/desktop/DirectShow/avenccommonqualityvsspeed-property">CODECAPI_AVEncCommonQualityVsSpeed</a> | Imposta il compromesso qualità/velocità. Questo valore influisce sul modo in cui il codificatore esegue varie operazioni di codifica, ad esempio la compensazione del movimento. A livelli di complessità più elevati, il codificatore viene eseguito più lentamente, ma produce una qualità migliore alla stessa velocità in bit. <br /> L'intervallo valido è compreso tra 0 e 100. Internamente, questo valore viene mappato a un set più piccolo di livelli di qualità/velocità supportati dal codificatore.<br /> Si tratta di un VT_UI4 predefinito.<br /> | 
| <a href="codecapi-avencvideoforcekeyframe.md">CODECAPI_AVEncVideoForceKeyFrame</a> | Forza il codificatore a codificare il fotogramma successivo come fotogramma chiave.<br /> Si tratta di un VT_UI4 predefinito.<br /> | 
| <a href="codecapi-avencvideoencodeqp.md">CODECAPI_AVEncVideoEncodeQP</a> | Quando questa proprietà è impostata, il codificatore userà il QP specificato per codificare il fotogramma successivo e tutti i fotogrammi successivi fino a quando non viene specificato un nuovo QP. <br /> Intervallo valido: 0-51, inclusi <br /> | 
| <a href="codecapi-avencvideominqp.md">CODECAPI_AVEncVideoMinQP</a> | Questa proprietà imposta un limite per il QP minimo che il codificatore può usare durante il controllo della frequenza CBR.<br /> Si tratta di un VT_UI4 predefinito.<br /> | 
| <a href="codecapi-avencvideomaxqp.md">CODECAPI_AVEncVideoMaxQP</a> | Questa proprietà imposta un limite per il QP massimo che il codificatore può usare durante il controllo della frequenza CBR.<br /> Si tratta di un VT_UI4 predefinito.<br /> | 
| <a href="codecapi-videoencoderdisplaycontenttype.md">CODECAPI_VideoEncoderDisplayContentType</a> | Imposta se il contenuto è un video a schermo intero, a differenza del contenuto dello schermo che potrebbe avere una finestra di video più piccola o senza video.<br /> Si tratta di un VT_UI4 predefinito.<br /> | 
| <a href="codecapi-avencnumworkerthreads.md">CODECAPI_AVEncNumWorkerThreads</a> | Imposta il numero di thread utilizzati per eseguire l'operazione di compressione. Il codificatore dividerà il frame in riquadri in modo che il numero di thread sia uguale al numero di riquadri.<br /><ul><li>Numero di processori logici. Il numero di thread deve essere minore o uguale al numero di processori logici.</li><li>Dimensioni del frame. Le dimensioni di un riquadro devono essere maggiori o uguali a 265x64 pixel.</li><li>Parità. Il numero di thread deve essere un valore pari. Se il valore specificato è dispari, verrà usato il successivo valore pari inferiore.</li></ul>Si tratta di un VT_UI4 predefinito.<br /> | 




 

## <a name="certified-hardware-encoder"></a>Codificatore hardware certificato

Se è presente un codificatore hardware certificato, verrà in genere usato al posto del codificatore di sistema della posta in arrivo Media Foundation scenari correlati. I codificatori certificati sono necessari per supportare un determinato set di proprietà **ICodecAPI** e possono facoltativamente supportare un altro set di proprietà. Il processo di certificazione deve garantire che le proprietà obbligatorie siano supportate correttamente e, se è supportata una proprietà facoltativa, che sia supportata correttamente.

Di seguito è riportato il set di proprietà **ICodecAPI** obbligatorie e facoltative che i codificatori possono superare la certificazione del codificatore HCK.

-   [CODECAPI \_ AVEncCommonRateControlMode](../directshow/avenccommonratecontrolmode-property.md)
-   [CODECAPI \_ AVEncCommonQuality](../directshow/avenccommonquality-property.md)
-   [CODECAPI \_ AVEncCommonMeanBitRate](../directshow/avenccommonmeanbitrate-property.md)
-   [CODECAPI \_ AVEncCommonBufferSize](../directshow/avenccommonbuffersize-property.md)
-   [CODECAPI \_ AVEncMPVGOPSize](../directshow/avencmpvgopsize-property.md)
-   [CODECAPI \_ AVEncVideoEncodeQP](codecapi-avencvideoencodeqp.md)
-   [CODECAPI \_ AVEncVideoForceKeyFrame](codecapi-avencvideoforcekeyframe.md)

## <a name="requirements"></a>Requisiti



| Requisito | valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                              |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                |
| DLL<br/>                      | <dl> <dt>Mfh265enc.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti codec](codecobjects.md)
</dt> </dl>

 

 
