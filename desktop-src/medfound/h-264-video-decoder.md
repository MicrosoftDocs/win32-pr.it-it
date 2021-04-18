---
description: Il decodificatore Media Foundation H. 264 video è una trasformazione Media Foundation che supporta la decodifica dei profili Baseline, Main e High, fino al livello 5,1.
ms.assetid: 783a3618-981a-4573-9e9e-ebf5eeb75d06
title: Decoder video H. 264
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75c4713b1a4e36d1ba085b2239c24ca0f6e4fae0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484053"
---
# <a name="h264-video-decoder"></a>Decoder video H. 264

Il decodificatore Media Foundation H. 264 video è una [trasformazione Media Foundation](media-foundation-transforms.md) che supporta la decodifica dei profili Baseline, Main e High, fino al livello 5,1.

Il decodificatore video H. 264 espone le interfacce seguenti.

-   [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) (supportato in Windows 8)
-   [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)
-   [**IMFQualityAdvise2**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2)
-   [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)
-   [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)
-   [**IMFRealTimeClient**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient)
-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

Per creare un'istanza del decodificatore, eseguire una delle operazioni seguenti:

-   Chiamare la funzione [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) o [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .
-   Chiamare [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance). Il CLSID per il decodificatore è **CLSID \_ CMSH264DecoderMFT**, dichiarato in wmcodecdsp. h.

## <a name="input-types"></a>Tipi di input

Il tipo di input deve contenere almeno i due attributi seguenti:



| Attributo                                                 | Descrizione                                                                                   |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**\_ \_ tipo principale MF \_ mt**](mf-mt-major-type-attribute.md) | **Video di MFMediaType \_**                                                                        |
| [**sottotipo MF \_ mt \_**](mf-mt-subtype-attribute.md)        | [MFVideoFormat \_ H264](video-subtype-guids.md) o MFVideoFormat \_ H264 \_ es |



 

Se il tipo di input contiene solo questi due attributi, il decodificatore offrirà un tipo di output predefinito, che funge da segnaposto. Quando il decodificatore riceve un numero di campioni di input sufficiente per produrre un frame di output, segnala una modifica di formato restituendo **MF \_ E \_ Transform \_ Stream \_ Change** da [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput). Vedere la documentazione di **ProcessOutput** per informazioni dettagliate sulla gestione delle modifiche del formato.

Per evitare una modifica del formato iniziale, fornire quante più informazioni possibile nel tipo di input, tra cui:



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
<td><a href="mf-mt-frame-rate-attribute.md"><strong>MF_MT_FRAME_RATE</strong></a></td>
<td>Frequenza di fotogrammi.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-frame-size-attribute.md"><strong>MF_MT_FRAME_SIZE</strong></a></td>
<td>Dimensioni del frame.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-interlace-mode-attribute.md"><strong>MF_MT_INTERLACE_MODE</strong></a></td>
<td>Modalità interlacciamento.
<blockquote>
[!Note]<br />
Nel video H. 264 la struttura interlacciata può variare in modo dinamico, quindi il valore consigliato di questo attributo viene <strong>MFVideoInterlace_MixedInterlaceOrProgressive</strong>. Le informazioni interlacciate nel flusso elementare video hanno la precedenza sul tipo di supporto. Per altre informazioni, vedere <a href="video-interlacing.md">interlacciamento video</a>.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="mf-mt-pixel-aspect-ratio-attribute.md"><strong>MF_MT_PIXEL_ASPECT_RATIO</strong></a></td>
<td>Proporzioni pixel.</td>
</tr>
</tbody>
</table>



 

Il tipo di input deve essere impostato prima del tipo di output. Fino a quando non viene impostato il tipo di input, il metodo [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) del codificatore restituisce il **tipo di \_ trasformazione MF E \_ \_ \_ non \_ impostato**.

## <a name="output-types"></a>Tipi di output

Il decodificatore supporta i sottotipi di output seguenti:

-   **\_I420 MFVideoFormat**
-   **\_IYUV MFVideoFormat**
-   **\_NV12 MFVideoFormat**
-   **\_YUY2 MFVideoFormat**
-   **\_YV12 MFVideoFormat**

Per altre informazioni su questi sottotipi, vedere [GUID del sottotipo video](video-subtype-guids.md).

## <a name="transform-attributes"></a>Attributi di trasformazione

Il decodificatore H. 264 implementa il metodo [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) . Le applicazioni possono utilizzare questo metodo per ottenere o impostare gli attributi seguenti.



| Attributo                                                                                       | Descrizione                                                                                |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [Codecapis \_ AVDecVideoAcceleration \_ H264](../directshow/avdecvideoacceleration-h264-property.md)            | Abilita o Disabilita l'accelerazione hardware.                                                 |
| [Codecapis \_ AVDecVideoThumbnailGenerationMode](../directshow/avdecvideothumbnailgenerationmode-property.md) | Abilita o Disabilita la modalità di generazione delle anteprime.                                             |
| [\_Compatibile con \_ D3D \_](mf-sa-d3d-aware-attribute.md)                                             | Indica che il decodificatore supporta l'accelerazione video DirectX (DXVA). Considera come di sola lettura. |



 

In Windows 8, il decodificatore H. 264 supporta anche gli attributi seguenti.



| Attributo                                                                                                     | Descrizione                                                                                                 |
|---------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [Codecapis \_ AVLowLatencyMode](codecapi-avlowlatencymode.md)                                                   | Abilita o Disabilita la modalità di decodifica a bassa latenza.                                                              |
| [Codecapis \_ AVDecNumWorkerThreads](codecapi-avdecnumworkerthreads.md)                                         | Imposta il numero di thread di lavoro utilizzati dal decodificatore.                                                      |
| [Codecapis \_ AVDecVideoMaxCodedWidth](codecapi-avdecvideomaxcodedwidth.md)                                     | Imposta la larghezza massima dell'immagine che il decodificatore accetterà come tipo di input.                               |
| [Codecapis \_ AVDecVideoMaxCodedHeight](codecapi-avdecvideomaxcodedheight.md)                                   | Imposta l'altezza massima dell'immagine che il decodificatore accetterà come tipo di input.                              |
| [\_ \_ numero minimo di \_ campioni di output MF \_ sa \_](mf-sa-minimum-output-sample-count.md)                               | Specifica il numero massimo di campioni di output.                                                             |
| [il \_ decodificatore MFT \_ espone i \_ \_ tipi \_ di output in \_ \_ ordine nativo](mft-decoder-expose-output-types-in-native-order.md) | Specifica se un decodificatore espone i tipi di output IYUV/I420 (adatti per la transcodifica) prima di altri formati. |



 

In Windows 8, il decodificatore H. 264 supporta l'interfaccia [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) . Questa interfaccia fornisce un'API alternativate per l'impostazione delle proprietà dei codec seguenti.

-   [Codecapis \_ AVDecVideoMaxCodedWidth](codecapi-avdecvideomaxcodedwidth.md)
-   [Codecapis \_ AVDecVideoAcceleration \_ H264](../directshow/avdecvideoacceleration-h264-property.md)
-   [Codecapis \_ AVDecVideoMaxCodedHeight](codecapi-avdecvideomaxcodedheight.md)
-   [Codecapis \_ AVDecVideoMaxCodedWidth](codecapi-avdecvideomaxcodedwidth.md)
-   [Codecapis \_ AVDecVideoThumbnailGenerationMode](../directshow/avdecvideothumbnailgenerationmode-property.md)

## <a name="format-constraints"></a>Vincoli di formato

Il decodificatore supporta i formati seguenti:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Profili/livelli</td>
<td>Profili Baseline, Main e High, fino al livello 5,1. Per informazioni dettagliate, vedere la specifica ITU-T H. 264.</td>
</tr>
<tr class="even">
<td>Formati Chroma</td>
<td>4:2:0 Chroma o monocromatico</td>
</tr>
<tr class="odd">
<td>Risoluzione minima</td>
<td>48 × 48 pixel</td>
</tr>
<tr class="even">
<td>Risoluzione massima</td>
<td>4096 × 2304 pixel<br/> La risoluzione massima garantita per l'accelerazione DXVA è 1920 × 1088 pixel; con risoluzioni più elevate, la decodifica viene eseguita con DXVA, se supportata dall'hardware sottostante. in caso contrario, la decodifica viene eseguita con il software.<br/>
<blockquote>
[!Note]<br />
In Windows 7 la risoluzione massima supportata è 1920 × 1088 pixel per la decodifica sia del software che del DXVA.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td>DXVA</td>
<td>Il decodificatore supporta DXVA versione 2, ma non DXVA versione 1. La decodifica DXVA è supportata solo per i Bitstream della linea di base, principale e del profilo superiore compatibili con la principale. I Bitstream di base compatibili con la principale sono definiti come <strong>profile_idc</strong>= 66 e <strong>constrained_set1_flag</strong>= 1.</td>
</tr>
</tbody>
</table>



 

I dati di input devono essere conformi all'allegato B di ISO/IEC 14496-10. I dati devono includere i codici iniziali. Il decodificatore ignora i byte finché non trova un set di parametri di sequenza (SPS) e un set di parametri immagine (PPS) validi nel flusso di byte.

Il decodificatore non supporta la tecnologia granulare dei film.

> [!Note]  
> Una versione precedente della documentazione ha erroneamente indicato che il decodificatore è supportato in Windows Server 2008 R2.

 

Se è installato il supplemento di aggiornamento della piattaforma per Windows Vista, il decodificatore video H. 264 è disponibile in Windows Vista, ma è accessibile solo in Windows Vista tramite il [lettore di origine](source-reader.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                  |
| DLL<br/>                      | <dl> <dt>Msmpeg2vdec.dll</dt> </dl> |



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

 

 
