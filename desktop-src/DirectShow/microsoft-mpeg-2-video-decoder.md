---
description: Questo filtro decodifica il video MPEG-1, MPEG-2, H.264.
ms.assetid: d8195c3a-97ac-4ad1-a097-18878c8fda6f
title: Microsoft MPEG-2 Video Decoder (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7bcd49aeff922bced12fa8d236259d0775d0fb1c6f9f7d0a05df1204f77f6c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119791431"
---
# <a name="microsoft-mpeg-2-video-decoder"></a>Microsoft MPEG-2 Video Decoder

Questo filtro decodifica il video MPEG-1, MPEG-2, H.264.

> [!Note]  
> La decodifica del video H.264 richiede Windows 7.

 

> [!Note]  
> Questo filtro non è supportato nelle piattaforme basate su IA-64.

 

Nel Registro di sistema il nome descrittivo di questo filtro è "Microsoft DTV-DVD Video Decoder".



Filtrare le informazioni

Interfacce di filtro

[**IAMDecoderCaps**](/windows/desktop/api/Strmif/nn-strmif-iamdecodercaps)<br/> [**Filtro IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/> [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/>

Tipi di supporti pin di input

Pin di input video:

-   MEDIATYPE \_ DVD \_ ENCRYPTED \_ PACK, MEDIASUBTYPE \_ MPEG2 \_ VIDEO
-   MEDIATYPE \_ MPEG2 \_ PES, MEDIASUBTYPE \_ MPEG2 \_ VIDEO
-   MEDIATYPE \_ Video, MEDIASUBTYPE \_ MPEG1Packet
-   MEDIATYPE \_ Video, MEDIASUBTYPE \_ MPEG1Payload
-   VIDEO \_ MEDIATYPE, MEDIASUBTYPE \_ MPEG2 \_ VIDEO

Segnaposto di input per le immagini secondarie:<br/>

-   IMMAGINE SECONDARIA \_ DVD \_ ENCRYPTED \_ PACK, MEDIASUBTYPE \_ DVD \_

A partire Windows 7, il pin di input video supporta anche i tipi di input seguenti:<br/>

-   **MEDIATYPE \_ Video**, **MEDIASUBTYPE \_ AVC1**
-   **MEDIATYPE \_ Video**, **MEDIASUBTYPE \_ H264**
-   **MEDIATYPE \_ Video**, **MEDIASUBTYPE \_ h264**
-   **MEDIATYPE \_ Video**, **MEDIASUBTYPE \_ X264**
-   **MEDIATYPE \_ Video,** **MEDIASUBTYPE \_ x264**

Per [altre informazioni, vedere H.264 Video Types](h-264-video-types.md) (Tipi di video H.264). Il tipo di supporto di input può cambiare in modo dinamico tra i tipi MPEG2 e H.264.<br/>

Interfacce pin di input

[**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/> [**IKsPropertySet**](ikspropertyset.md)<br/> [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [**IMFSampleProtection**](/windows/win32/api/mfidl/nn-mfidl-imfsampleprotection)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

Tipi di supporti pin di output

Pin di output video:

-   Video \_ MEDIATYPE, DXVA \_ ModeMPEG2 \_ A (DXVA 1.0)
-   Video \_ MEDIATYPE, DXVA \_ ModeMPEG2 \_ C (DXVA 1.0)
-   MEDIATYPE \_ Video, MEDIASUBTYPE \_ I420 (decodifica software o DXVA2.0)
-   MEDIATYPE \_ Video, MEDIASUBTYPE \_ NV12 (Decodifica software o DXVA2.0)
-   MEDIATYPE \_ Video, MEDIASUBTYPE \_ YUY2 (Decodifica software o DXVA2.0)
-   MEDIATYPE \_ Video, MEDIASUBTYPE \_ IMC3 (solo DXVA2.0)
-   MEDIATYPE \_ Video, MEDIASUBTYPE \_ IMC4 (solo DXVA2.0)
-   MEDIATYPE \_ Video, MEDIASUBTYPE \_ S340 (solo DXVA2.0)
-   MEDIATYPE \_ Video, MEDIASUBTYPE \_ YV12 (solo DXVA2.0)

Pin di output riga 21:<br/>

-   MEDIATYPE \_ AUXLine21Data, MEDIASUBTYPE \_ Line21 \_ GOPPacket

Segnaposto di output dell'immagine secondaria:<br/>

-   MEDIATYPE \_ Video, MEDIASUBTYPE \_ AI44
-   MEDIATYPE \_ Video, MEDIASUBTYPE \_ ARGB32
-   MEDIATYPE \_ Video, MEDIASUBTYPE \_ ARGB4444
-   MEDIATYPE \_ Video, MEDIASUBTYPE \_ AYUV

Interfacce pin di output

[**IAMVideoAcceleratorNotify**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoacceleratornotify) (solo pin di output video)<br/> [**IKsPropertySet**](ikspropertyset.md)<br/> [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/> [**IVPConfig**](/previous-versions/windows/desktop/api/Vpconfig/nn-vpconfig-ivpconfig)<br/>

CLSID del filtro

**CLSID \_ CMPEG2VidDecoderDS** (definito in wmcodecdsp.h)

File eseguibile

msmpeg2vdec.dll

[Merito](merit.md)

**LE DUE SIE \_ NORMAL** - 1

[Categoria filtro](filter-categories.md)

**CLSID \_ LegacyAmFilterCategory**



 

## <a name="remarks"></a>Commenti

Questo filtro ha due pin di input e tre pin di output.

Pin di input:

-   Input video
-   Input dell'immagine secondaria

Pin di output:

-   Output video
-   Output della riga 21
-   Output delle immagini secondarie

Il filtro non crea il pin di output dell'immagine secondaria a meno che il pin di input video non sia connesso con un tipo di supporto **MEDIATYPE \_ DVD \_ ENCRYPTED \_ PACK.**

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
<td>Qualsiasi combinazione dei profili e dei livelli seguenti:<br/>
<ul>
<li>Profili: Simple, Main</li>
<li>Livelli: Basso, Principale, Alto, Alto 1440</li>
</ul></td>
</tr>
<tr class="even">
<td>Formati chroma</td>
<td>4:2:0 chroma</td>
</tr>
<tr class="odd">
<td>Risoluzione massima</td>
<td>1920 × 1088 pixel</td>
</tr>
<tr class="even">
<td>Dxva</td>
<td>Il decodificatore supporta DirectX Video Acceleration (DXVA) versione 1 e versione 2.</td>
</tr>
</tbody>
</table>



 

Il decodificatore non supporta i bitstream scalabili. L'input deve essere un flusso video elementare.

Il decodificatore non supporta i formati chroma 4:2:2.

### <a name="h264-support"></a>Supporto H.264

Per H.264, il decodificatore supporta i formati seguenti:



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Profili/livelli    | Profili di base, principale e alto, fino al livello 5.1. Per informazioni dettagliate, vedere la specifica ITU-T H.264.                                                                                                                                                                          |
| Formati chroma     | 4:2:0 chroma o monocroma                                                                                                                                                                                                                                                |
| Risoluzione minima | 48 × 48 pixel                                                                                                                                                                                                                                                            |
| Risoluzione massima | 1920 × 1088 pixel                                                                                                                                                                                                                                                        |
| Dxva               | Il decodificatore supporta DXVA versione 2, ma non DXVA versione 1. La decodifica DXVA è supportata solo per i bitstream di bit baseline, main e high profile compatibili con Main. I bitstream di base compatibili con main sono definiti come **profilo \_ idc**=66 e **flag \_ set1 \_ vincolato**=1. |



 

Il decodificatore non supporta La tecnologia Film Grain.

Per informazioni sui tipi di supporti H.264, vedere [Tipi di video H.264.](h-264-video-types.md)

### <a name="codec-properties"></a>Proprietà codec

I pin di input supportano i seguenti set di proprietà [**tramite IKsPropertySet:**](ikspropertyset.md)

-   [**Set di proprietà protezione copia DVD**](dvd-copy-protection-property-set.md)
-   [**Dvd Subpicture Property Set (dvd Subpicture Property Set**](dvd-subpicture-property-set.md) ( subpicture pin only)

I pin di input supportano le proprietà seguenti tramite [**ICodecAPI:**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)



| Proprietà                                                                  | Richiede      |
|---------------------------------------------------------------------------|---------------|
| [**AVDecCommonInputFormat**](avdeccommoninputformat-property.md)         | Windows Vista |
| [**AVDecVideoInputScanType**](avdecvideoinputscantype-property.md)       | Windows Vista |
| [**AVDecVideoPixelAspectRatio**](avdecvideopixelaspectratio-property.md) | Windows Vista |



 

Il filtro supporta le proprietà seguenti tramite [**ICodecAPI:**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)



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
| Client minimo supportato<br/> | Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, Windows 7 Ultimate \[ desktop apps only\]<br/> |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl>                                                                                       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[DirectShow Filtri](directshow-filters.md)
</dt> <dt>

[**Tipi di supporti DVD**](dvd-media-types.md)
</dt> <dt>

[Tipi di video H.264](h-264-video-types.md)
</dt> </dl>

 

 
