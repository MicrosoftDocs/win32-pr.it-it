---
description: Questo filtro decodifica il video MPEG-1, MPEG-2, H. 264.
ms.assetid: d8195c3a-97ac-4ad1-a097-18878c8fda6f
title: Decodificatore video Microsoft MPEG-2 (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8460b5b554fffc8f0dd8679810e5ef3f42bcb004
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401113"
---
# <a name="microsoft-mpeg-2-video-decoder"></a>Decoder video Microsoft MPEG-2

Questo filtro decodifica il video MPEG-1, MPEG-2, H. 264.

> [!Note]  
> La decodifica del video H. 264 richiede Windows 7.

 

> [!Note]  
> Questo filtro non è supportato nelle piattaforme basate su IA-64.

 

Nel registro di sistema il nome descrittivo di questo filtro è "Microsoft DTV-DVD video decoder".



Informazioni sul filtro

Interfacce di filtro

[**IAMDecoderCaps**](/windows/desktop/api/Strmif/nn-strmif-iamdecodercaps)<br/> [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/> [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/>

Tipi di supporti pin di input

Pin di input video:

-   MEDIATYPE \_ DVD \_ Encrypted \_ Pack, \_ video MEDIASUBTYPE MPEG2 \_
-   MEDIATYPE \_ MPEG2 \_ PE, \_ video MEDIASUBTYPE MPEG2 \_
-   \_Video di MEDIATYPE, MEDIASUBTYPE \_ MPEG1Packet
-   \_Video di MEDIATYPE, MEDIASUBTYPE \_ MPEG1Payload
-   Video \_ di MEDIATYPE, \_ video di MEDIASUBTYPE MPEG2 \_

Pin di input della sottoimmagine:<br/>

-   MEDIATYPE \_ DVD \_ Encrypted \_ Pack, \_ \_ sottoimmagine DVD MEDIASUBTYPE

A partire da Windows 7, il pin di input video supporta anche i tipi di input seguenti:<br/>

-   **MEDIATYPE \_ Video**, **MEDIASUBTYPE \_ AVC1**
-   **MEDIATYPE \_ Video**, **MEDIASUBTYPE \_ H264**
-   **MEDIATYPE \_ Video**, **MEDIASUBTYPE \_ H264**
-   **MEDIATYPE \_ Video**, **MEDIASUBTYPE \_ x264**
-   **MEDIATYPE \_ Video**, **MEDIASUBTYPE \_ x264**

Per ulteriori informazioni, vedere i [tipi di video H. 264](h-264-video-types.md) . Il tipo di supporto di input può variare in modo dinamico tra i tipi MPEG2 e H. 264.<br/>

Interfacce pin di input

[**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/> [**IKsPropertySet**](ikspropertyset.md)<br/> [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [**IMFSampleProtection**](/windows/win32/api/mfidl/nn-mfidl-imfsampleprotection)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

Tipi di supporti pin di output

Pin di output del video:

-   MEDIATYPE \_ video, DXVA \_ ModeMPEG2 \_ A (DXVA 1,0)
-   MEDIATYPE \_ video, DXVA \_ ModeMPEG2 \_ C (DXVA 1,0)
-   \_Video di MEDIATYPE, MEDIASUBTYPE \_ I420 (decodifica software o DXVA 2.0)
-   \_Video di MEDIATYPE, MEDIASUBTYPE \_ NV12 (decodifica software o DXVA 2.0)
-   \_Video di MEDIATYPE, MEDIASUBTYPE \_ YUY2 (decodifica software o DXVA 2.0)
-   MEDIATYPE \_ video, MEDIASUBTYPE \_ IMC3 (solo DXVA 2.0)
-   MEDIATYPE \_ video, MEDIASUBTYPE \_ IMC4 (solo DXVA 2.0)
-   MEDIATYPE \_ video, MEDIASUBTYPE \_ S340 (solo DXVA 2.0)
-   MEDIATYPE \_ video, MEDIASUBTYPE \_ YV12 (solo DXVA 2.0)

Pin di output riga 21:<br/>

-   MEDIATYPE \_ AUXLine21Data, MEDIASUBTYPE \_ Line21 \_ GOPPacket

Pin di output della sottoimmagine:<br/>

-   \_Video di MEDIATYPE, MEDIASUBTYPE \_ AI44
-   \_Video di MEDIATYPE, MEDIASUBTYPE \_ ARGB32
-   \_Video di MEDIATYPE, MEDIASUBTYPE \_ ARGB4444
-   \_Video di MEDIATYPE, MEDIASUBTYPE \_ AYUV

Interfacce del PIN di output

[**IAMVideoAcceleratorNotify**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoacceleratornotify) (solo pin di output video)<br/> [**IKsPropertySet**](ikspropertyset.md)<br/> [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/> [**IVPConfig**](/previous-versions/windows/desktop/api/Vpconfig/nn-vpconfig-ivpconfig)<br/>

CLSID filtro

**CLSID \_ CMPEG2VidDecoderDS** (definito in wmcodecdsp. h)

File eseguibile

msmpeg2vdec.dll

[Merito](merit.md)

Il **merito \_ NORMALE** -1

[Categoria filtro](filter-categories.md)

**\_LEGACYAMFILTERCATEGORY CLSID**



 

## <a name="remarks"></a>Commenti

Questo filtro ha due pin di input e tre pin di output.

Pin di input:

-   Input video
-   Input della sottoimmagine

Pin di output:

-   Output video
-   Output riga 21
-   Output della sottoimmagine

Il filtro non crea il pin di output della sottoimmagine, a meno che il pin di input del video non sia connesso con un tipo di supporto del **\_ \_ \_ pacchetto DVD crittografato MEDIATYPE** .

### <a name="mpeg-12-support"></a>Supporto MPEG-1/2

Per MPEG-1 e MPEG-2, il decodificatore supporta i formati seguenti:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Profili/livelli</td>
<td>Qualsiasi combinazione dei seguenti profili e livelli:<br/>
<ul>
<li>Profili: semplice, principale</li>
<li>Livelli: Low, Main, High, High 1440</li>
</ul></td>
</tr>
<tr class="even">
<td>Formati Chroma</td>
<td>Chroma 4:2:0</td>
</tr>
<tr class="odd">
<td>Risoluzione massima</td>
<td>1920 × 1088 pixel</td>
</tr>
<tr class="even">
<td>DXVA</td>
<td>Il decodificatore supporta la versione 1 e la versione 2 di DirectX Video Acceleration (DXVA).</td>
</tr>
</tbody>
</table>



 

Il decodificatore non supporta i Bitstream scalabili. L'input deve essere un flusso video elementare.

Il decodificatore non supporta i formati Chroma 4:2:2.

### <a name="h264-support"></a>Supporto di H. 264

Per H. 264, il decodificatore supporta i formati seguenti:



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Profili/livelli    | Profili Baseline, Main e High, fino al livello 5,1. Per informazioni dettagliate, vedere la specifica ITU-T H. 264.                                                                                                                                                                          |
| Formati Chroma     | 4:2:0 Chroma o monocromatico                                                                                                                                                                                                                                                |
| Risoluzione minima | 48 × 48 pixel                                                                                                                                                                                                                                                            |
| Risoluzione massima | 1920 × 1088 pixel                                                                                                                                                                                                                                                        |
| DXVA               | Il decodificatore supporta DXVA versione 2, ma non DXVA versione 1. La decodifica DXVA è supportata solo per i Bitstream della linea di base, principale e del profilo superiore compatibili con la principale. I Bitstream di base compatibili con la principale sono definiti come **profilo \_ idc**= 66 e **\_ \_ flag set1 vincolato**= 1. |



 

Il decodificatore non supporta la tecnologia granulare dei film.

Per informazioni sui tipi di supporto H. 264, vedere [tipi di video h. 264](h-264-video-types.md).

### <a name="codec-properties"></a>Proprietà codec

I pin di input supportano i set di proprietà seguenti tramite [**IKsPropertySet**](ikspropertyset.md):

-   [**Set di proprietà di protezione copia DVD**](dvd-copy-protection-property-set.md)
-   [**Set di proprietà della sottoimmagine DVD**](dvd-subpicture-property-set.md) (solo pin dell'immagine)

I pin di input supportano le proprietà seguenti tramite [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):



| Proprietà                                                                  | Richiede      |
|---------------------------------------------------------------------------|---------------|
| [**AVDecCommonInputFormat**](avdeccommoninputformat-property.md)         | Windows Vista |
| [**AVDecVideoInputScanType**](avdecvideoinputscantype-property.md)       | Windows Vista |
| [**AVDecVideoPixelAspectRatio**](avdecvideopixelaspectratio-property.md) | Windows Vista |



 

Il filtro supporta le seguenti proprietà tramite [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):



| Proprietà                                                                                | Richiede      |
|-----------------------------------------------------------------------------------------|---------------|
| [**AVDecMmcssClass**](avdecmmcss-property.md)                                          | Windows Vista |
| [**AVDecVideoAcceleration \_ H264**](avdecvideoacceleration-h264-property.md)            | Windows 7     |
| [**AVDecVideoAcceleration \_ MPEG2**](avdecvideoacceleration-mpeg2-property.md)          | Windows 7     |
| [**AVDecVideoDropPicWithMissingRef**](avdecvideodroppicwithmissingref-property.md)     | Windows 7     |
| [**AVDecVideoFastDecodeMode**](avdecvideofastdecodemode.md)                            | Windows 7     |
| [**AVDecVideoImageSize**](avdecvideoimagesize.md)                                      | Windows 7     |
| [**AVDecVideoSoftwareDeinterlaceMode**](avdecvideosoftwaredeinterlacemode-property.md) | Windows 7     |
| [**AVDecVideoThumbnailGenerationMode**](avdecvideothumbnailgenerationmode-property.md) | Windows 7     |



 

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

[**Tipi di supporti DVD**](dvd-media-types.md)
</dt> <dt>

[Tipi di video H. 264](h-264-video-types.md)
</dt> </dl>

 

 
