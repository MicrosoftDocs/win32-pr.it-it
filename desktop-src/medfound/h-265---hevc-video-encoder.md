---
description: Il codificatore Media Foundation H. 265 video è una trasformazione Media Foundation che supporta la codifica del contenuto nel formato H. 265/HEVC.
ms.assetid: 790CFB39-6FC0-432D-A434-5262C30EABF4
title: Codificatore video H. 265/HEVC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 015295792a72f3250c47389192586dbc00566858
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966945"
---
# <a name="h265--hevc-video-encoder"></a>Codificatore video H. 265/HEVC

Il codificatore Media Foundation H. 265 video è una [trasformazione Media Foundation](media-foundation-transforms.md) che supporta la codifica del contenuto nel formato H. 265/HEVC. Il codificatore supporta i profili seguenti:

-   Main Profile

Il codificatore video H. 265 espone le interfacce seguenti:

-   [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi)
-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="input-types"></a>Tipi di input

Il tipo di supporto di input deve avere uno dei seguenti sottotipi:

-   **\_IYUV MFVideoFormat**
-   **\_NV12 MFVideoFormat**
-   **\_YUY2 MFVideoFormat**
-   **\_YV12 MFVideoFormat**

Per altre informazioni su questi sottotipi, vedere [GUID del sottotipo video](video-subtype-guids.md).

Il tipo di output deve essere impostato prima del tipo di input. Fino a quando non viene impostato il tipo di output, il metodo [**IMFTransform:: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) del codificatore restituisce il **tipo di \_ trasformazione MF E \_ \_ \_ non \_ impostato**.

## <a name="output-types"></a>Tipi di output

Il codificatore supporta un solo sottotipo di output:

-   **\_H265 MFVideoFormat**

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
<td>Sottotipo video. Deve essere <strong>MFVideoFormat_HEVC</strong>.</td>
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
<td><a href="mf-mt-video-profile.md">MF_MT_VIDEO_PROFILE</a></td>
<td>Profilo di codifica H. 265.<br/> I valori supportati sono: <br/>
<ul>
<li><strong>eAVEncH265VProfile_Main_420_8</strong></li>
</ul></td>
</tr>
<tr class="even">
<td><a href="mf-mt-mpeg2-level-attribute.md"><strong>MF_MT_MPEG2_LEVEL</strong></a></td>
<td>Specifica il livello del video codificato. Per ulteriori informazioni sui vincoli di profilo e di livello, vedere l'allegato A di ITU-T H. 265.<br/></td>
</tr>
<tr class="odd">
<td><a href="mf-mt-pixel-aspect-ratio-attribute.md"><strong>MF_MT_PIXEL_ASPECT_RATIO</strong></a></td>
<td>facoltativo. Specifica le proporzioni in pixel. Il valore predefinito è 1:1.</td>
</tr>
</tbody>
</table>



 

Dopo aver impostato il tipo di output, il codificatore video aggiorna il tipo aggiungendo l'attributo dell' [**\_ \_ \_ \_ intestazione della sequenza MPEG di MF mt**](mf-mt-mpeg-sequence-header-attribute.md) . Questo attributo contiene l'intestazione della sequenza.

## <a name="supported-imftransform-methods"></a>Metodi IMFTransform supportati

Per il codificatore H. 265/HEVC sono supportati i seguenti metodi dell'interfaccia [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) :

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

Tutti gli altri metodi di [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) restituiranno l'errore E \_ NOTIMPL.

## <a name="supported-icodecapi-methods"></a>Metodi ICodecAPI supportati

Per il codificatore H. 265/HEVC sono supportati i seguenti metodi dell'interfaccia [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) :

-   [**IsSupported**](/windows/win32/api/strmif/nf-strmif-icodecapi-issupported)
-   [**SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue)
-   [**GetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-getvalue)
-   [**GetParameterRange**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparameterrange)
-   [**GetParameterValues**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparametervalues)

Tutti gli altri metodi di [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) restituiranno l'errore E \_ NOTIMPL.

## <a name="codec-properties"></a>Proprietà codec

Il codificatore H. 265 implementa l'interfaccia [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) per l'impostazione dei parametri di codifica. Supporta le proprietà seguenti.

Per i requisiti di codec per la certificazione del codificatore HCK, vedere la sezione relativa al **codificatore hardware certificato** di seguito.



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
<td><a href="/windows/desktop/DirectShow/avenccommonratecontrolmode-property"><strong>CODECAPI_AVEncCommonRateControlMode</strong></a></td>
<td>Imposta la modalità di controllo della frequenza. Le modalità supportate sono:<br/>
<ul>
<li><strong>eAVEncCommonRateControlMode_CBR</strong></li>
<li><strong>eAVEncCommonRateControlMode_Quality</strong></li>
</ul>
Se vengono specificate altre modalità, verrà usato il controllo della velocità <strong>eAVEncCommonRateControlMode_CBR</strong> .<br/> Si tratta di un valore VT_UI4.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/DirectShow/avenccommonmeanbitrate-property">CODECAPI_AVEncCommonMeanBitRate</a></td>
<td>Imposta la velocità in bit media per il flusso di bit codificato, in bit al secondo. <br/> L'intervallo valido è [1... 2 ³ ² – 1]. <br/> Si tratta di un valore VT_UI4.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/avenccommonbuffersize-property">CODECAPI_AVEncCommonBufferSize</a></td>
<td>Imposta la dimensione del buffer, in byte, per la codifica di velocità in bit costante (CBR).<br/> L'intervallo valido è [1... 2 ³ ² – 1]. <br/> Si tratta di un valore VT_UI4.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/DirectShow/avenccommonmaxbitrate-property">CODECAPI_AVEncCommonMaxBitRate</a></td>
<td>Imposta la velocità in bit massima per le modalità di controllo della frequenza che consentono una velocità in bit di picco. <br/> L'intervallo valido è [1... 2 ³ ² – 1]. <br/> Si tratta di un valore VT_UI4.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/avencmpvgopsize-property">CODECAPI_AVEncMPVGOPSize</a></td>
<td>Imposta il numero di immagini da un'intestazione GOP alla successiva, incluso l'ancoraggio principale ma non quello seguente. <br/> L'intervallo valido è [0... 2 ³ ² – 1]. Se il valore è zero, il codificatore seleziona la dimensione GOP. Il valore predefinito è zero. <br/> Si tratta di un valore VT_UI4.<br/></td>
</tr>
<tr class="even">
<td><a href="codecapi-avlowlatencymode.md">CODECAPI_AVLowLatencyMode</a></td>
<td>Abilita o Disabilita la modalità a bassa latenza. <br/> Si tratta di un valore VT_BOOL.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/avenccommonqualityvsspeed-property">CODECAPI_AVEncCommonQualityVsSpeed</a></td>
<td>Imposta il compromesso di qualità/velocità. Questo valore influiscono sul modo in cui il codificatore esegue diverse operazioni di codifica, ad esempio la compensazione del movimento. A livelli di complessità più elevati, il codificatore viene eseguito più lentamente, ma produce una qualità migliore con la stessa velocità in bit. <br/> L'intervallo valido è 0 – 100. Internamente, questo valore viene mappato a un set più piccolo di livelli di qualità/velocità supportato dal codificatore.<br/> Si tratta di un valore VT_UI4.<br/></td>
</tr>
<tr class="even">
<td><a href="codecapi-avencvideoforcekeyframe.md">CODECAPI_AVEncVideoForceKeyFrame</a></td>
<td>Impone al codificatore di codificare il fotogramma successivo come fotogramma chiave.<br/> Si tratta di un valore VT_UI4.<br/></td>
</tr>
<tr class="odd">
<td><a href="codecapi-avencvideoencodeqp.md">CODECAPI_AVEncVideoEncodeQP</a></td>
<td>Quando questa proprietà è impostata, il codificatore userà il QP specificato per codificare il frame successivo e tutti i frame successivi fino a quando non viene specificato un nuovo QP. <br/> Intervallo valido: 0-51, inclusivo <br/></td>
</tr>
<tr class="even">
<td><a href="codecapi-avencvideominqp.md">CODECAPI_AVEncVideoMinQP</a></td>
<td>Questa proprietà consente di impostare un limite per il numero minimo di QP che il codificatore può usare durante controllo della frequenza CBR.<br/> Si tratta di un valore VT_UI4.<br/></td>
</tr>
<tr class="odd">
<td><a href="codecapi-avencvideomaxqp.md">CODECAPI_AVEncVideoMaxQP</a></td>
<td>Questa proprietà consente di impostare un limite per il numero massimo di QP che il codificatore può usare durante controllo della frequenza CBR.<br/> Si tratta di un valore VT_UI4.<br/></td>
</tr>
<tr class="even">
<td><a href="codecapi-videoencoderdisplaycontenttype.md">CODECAPI_VideoEncoderDisplayContentType</a></td>
<td>Imposta un valore che indica se il contenuto è video a schermo intero, anziché il contenuto dello schermo che potrebbe contenere una finestra di video più piccola o senza video.<br/> Si tratta di un valore VT_UI4.<br/></td>
</tr>
<tr class="odd">
<td><a href="codecapi-avencnumworkerthreads.md">CODECAPI_AVEncNumWorkerThreads</a></td>
<td>Imposta il numero di thread utilizzati per eseguire l'operazione di compressione. Il codificatore suddividerà il frame in riquadri in modo che il numero di thread sia uguale al numero di riquadri.<br/>
<ul>
<li>Numero di processori logici. Il numero di thread deve essere minore o uguale al numero di processori logici.</li>
<li>Dimensioni del frame. Le dimensioni di un riquadro devono essere maggiori o uguali a 265x64 pixel.</li>
<li>Parità. Il numero di thread deve essere un valore pari. Se il valore specificato è dispari, verrà usato il successivo valore di pari livello inferiore.</li>
</ul>
Si tratta di un valore VT_UI4.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="certified-hardware-encoder"></a>Codificatore hardware certificato

Se è presente un codificatore hardware certificato, in genere verrà usato al posto del codificatore di sistema della posta in arrivo per Media Foundation scenari correlati. I codificatori certificati sono necessari per supportare un determinato set di proprietà **ICodecAPI** e possono facoltativamente supportare un altro set di proprietà. Il processo di certificazione deve garantire che le proprietà obbligatorie siano supportate correttamente e, se è supportata una proprietà facoltativa, anche se è supportata correttamente.

Di seguito è riportato il set di proprietà **ICodecAPI** obbligatorie e facoltative per i codificatori per passare la certificazione del codificatore HCK.

-   [Codecapis \_ AVEncCommonRateControlMode](../directshow/avenccommonratecontrolmode-property.md)
-   [Codecapis \_ AVEncCommonQuality](../directshow/avenccommonquality-property.md)
-   [Codecapis \_ AVEncCommonMeanBitRate](../directshow/avenccommonmeanbitrate-property.md)
-   [Codecapis \_ AVEncCommonBufferSize](../directshow/avenccommonbuffersize-property.md)
-   [Codecapis \_ AVEncMPVGOPSize](../directshow/avencmpvgopsize-property.md)
-   [Codecapis \_ AVEncVideoEncodeQP](codecapi-avencvideoencodeqp.md)
-   [Codecapis \_ AVEncVideoForceKeyFrame](codecapi-avencvideoforcekeyframe.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/>                                              |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                |
| DLL<br/>                      | <dl> <dt>Mfh265enc.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti codec](codecobjects.md)
</dt> </dl>

 

 
