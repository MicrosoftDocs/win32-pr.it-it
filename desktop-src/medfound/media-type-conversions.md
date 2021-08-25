---
description: Conversioni di tipi di supporti
ms.assetid: 6aee18b8-79b1-47fb-816f-d1c2c77b3a03
title: Conversioni di tipi di supporti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aacb4b7209ec96493c7b32c9de15ecf55071d7fb2861eda86f6f38fed8566e71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119827471"
---
# <a name="media-type-conversions"></a>Conversioni di tipi di supporti

In alcuni casi è necessario eseguire la conversione tra Media Foundation tipi di supporti e le strutture dei tipi di supporti meno recenti da DirectShow o Windows Media Format SDK.

### <a name="from-a-format-structure-to-a-media-foundation-type"></a>Da una struttura di formato a un Media Foundation tipo

Le funzioni seguenti inizializzano un Media Foundation tipo di supporto da una struttura di formato. Queste funzioni sono utili anche se un flusso di dati o un'intestazione di file contiene una struttura di formato. Ad esempio, l'intestazione del file per i file audio WAVE contiene una [**struttura WAVEFORMATEX.**](/previous-versions/dd757713(v=vs.85))



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Struttura da convertire</th>
<th>Funzione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/win32/api/strmif/ns-strmif-am_media_type"><strong>AM_MEDIA_TYPE</strong></a> (DirectShow)<br/> <a href="/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type"><strong>DMO_MEDIA_TYPE</strong></a> (DirectX Media Objects) <br/> <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type"><strong>WM_MEDIA_TYPE</strong></a> (Windows Media Format SDK) <br/>
<blockquote>
[!Note]<br />
Queste strutture sono equivalenti.
</blockquote>
<br/> <br/></td>
<td><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromammediatype"><strong>MFInitMediaTypeFromAMMediaType</strong></a></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader"><strong>BITMAPINFOHEADER</strong></a></td>
<td><a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreatevideomediatypefrombitmapinfoheaderex"><strong>MFCreateVideoMediaTypeFromBitMapInfoHeaderEx</strong></a></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat"><strong>MFVIDEOFORMAT</strong></a></td>
<td><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefrommfvideoformat"><strong>MFInitMediaTypeFromMFVideoFormat</strong></a></td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo"><strong>MPEG1VIDEOINFO</strong></a></td>
<td><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefrommpeg1videoinfo"><strong>MFInitMediaTypeFromMPEG1VideoInfo</strong></a></td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo"><strong>MPEG2VIDEOINFO</strong></a></td>
<td><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefrommpeg2videoinfo"><strong>MFInitMediaTypeFromMPEG2VideoInfo</strong></a></td>
</tr>
<tr class="even">
<td><a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2"><strong>VIDEOINFOHEADER2</strong></a></td>
<td><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromvideoinfoheader2"><strong>MFInitMediaTypeFromVideoInfoHeader2</strong></a></td>
</tr>
<tr class="odd">
<td><a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader"><strong>VIDEOINFOHEADER</strong></a></td>
<td><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromvideoinfoheader"><strong>MFInitMediaTypeFromVideoInfoHeader</strong></a></td>
</tr>
<tr class="even">
<td><a href="/previous-versions/dd757713(v=vs.85)"><strong>WAVEFORMATEX</strong></a> o <a href="/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)"> <strong>WAVEFORMATEXTENSIBLE</strong></a></td>
<td><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex"><strong>MFInitMediaTypeFromWaveFormatEx</strong></a></td>
</tr>
</tbody>
</table>



 

### <a name="from-a-media-foundation-type-to-a-format-structure"></a>Da un Media Foundation tipo a una struttura di formato

Le funzioni seguenti creano o inizializzano una struttura di formato da un Media Foundation tipo di supporto.



| Funzione                                                                             | Struttura di destinazione                                                                                                                                                                    |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IMFMediaType::GetRepresentation**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getrepresentation)            | [**AM \_ TIPO \_ DI**](/windows/win32/api/strmif/ns-strmif-am_media_type)SUPPORTO, [**MFVIDEOFORMAT,**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat) [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)o [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) |
| [**MFCreateAMMediaTypeFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateammediatypefrommfmediatype)     | [**TIPO \_ DI SUPPORTO \_ AM**](/windows/win32/api/strmif/ns-strmif-am_media_type)                                                                                                                                          |
| [**MFCreateMFVideoFormatFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemfvideoformatfrommfmediatype) | [**MFVIDEOFORMAT**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat)                                                                                                                                              |
| [**MFCreateWaveFormatExFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatewaveformatexfrommfmediatype)   | [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) o [ **WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85))                                                                                    |
| [**MFInitAMMediaTypeFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfinitammediatypefrommfmediatype)         | [**TIPO \_ DI SUPPORTO \_ AM**](/windows/win32/api/strmif/ns-strmif-am_media_type)                                                                                                                                          |



 

## <a name="format-mappings"></a>Mapping dei formati

Nelle tabelle seguenti sono elencati Media Foundation attributi che corrispondono a varie strutture di formato. Non tutti questi attributi possono essere tradotti direttamente. Per eseguire conversioni, è necessario usare le funzioni elencate nella sezione precedente. queste tabelle vengono fornite principalmente come riferimento.

### <a name="am_media_type"></a>TIPO \_ DI SUPPORTO \_ AM



| Membro                   | Attributo                                                                            |
|--------------------------|--------------------------------------------------------------------------------------|
| **bTemporalCompression** | [**MF \_ MT \_ ALL \_ SAMPLES \_ INDEPENDENT**](mf-mt-all-samples-independent-attribute.md) |
| **bFixedSizeSamples**    | [**ESEMPI DI \_ DIMENSIONI \_ \_ FISSE MF MT \_**](mf-mt-fixed-size-samples-attribute.md)           |
| **lSampleSize**          | [**DIMENSIONI DEL \_ CAMPIONE MF \_ \_ MT**](mf-mt-sample-size-attribute.md)                          |



 

### <a name="waveformatex-waveformatextensible"></a>WAVEFORMATEX, WAVEFORMATEXTENSIBLE



| Membro                  | Attributo                                                                                                                                                                 |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **wFormatTag**          | [**MF \_ MT \_ SUBTYPE**](mf-mt-subtype-attribute.md)<br/> Se **wFormatTag** è EXTENSIBLE WAVE \_ \_ FORMAT, il sottotipo viene trovato nel **membro SubFormat.**<br/> |
| **nChannels**           | [**MF \_ MT \_ AUDIO \_ NUM \_ CHANNELS**](mf-mt-audio-num-channels-attribute.md)                                                                                                |
| **nSamplesPerSec**      | [**ESEMPI \_ DI AUDIO MT MF \_ \_ AL \_ \_ SECONDO**](mf-mt-audio-samples-per-second-attribute.md)                                                                                   |
| **nAvgBytesPerSec**     | [**MF \_ MT \_ AUDIO \_ AVG BYTES AL \_ \_ \_ SECONDO**](mf-mt-audio-avg-bytes-per-second-attribute.md)                                                                              |
| **nBlockAlign**         | [**MF \_ MT \_ AUDIO \_ BLOCK \_ ALIGNMENT**](mf-mt-audio-block-alignment-attribute.md)                                                                                          |
| **wBitsPerSample**      | [**MF \_ MT \_ AUDIO \_ BITS \_ PER \_ SAMPLE**](mf-mt-audio-bits-per-sample-attribute.md)                                                                                         |
| **wValidBitsPerSample** | [**MF \_ MT \_ AUDIO \_ VALID \_ BITS \_ PER \_ SAMPLE**](mf-mt-audio-valid-bits-per-sample-attribute.md)                                                                            |
| **wSamplesPerBlock**    | [**ESEMPI \_ DI AUDIO MT MF \_ \_ PER \_ \_ BLOCCO**](mf-mt-audio-samples-per-block-attribute.md)                                                                                     |
| **dwChannelMask**       | [**MF \_ MT \_ AUDIO \_ CHANNEL \_ MASK**](mf-mt-audio-channel-mask-attribute.md)                                                                                                |
| **Formato secondario**           | [**MF \_ MT \_ SUBTYPE**](mf-mt-subtype-attribute.md)                                                                                                                        |
| Dati aggiuntivi              | [**MF \_ MT \_ USER \_ DATA**](mf-mt-user-data-attribute.md)                                                                                                                   |



 

### <a name="videoinfoheader-videoinfoheader2"></a>VIDEOINFOHEADER, VIDEOINFOHEADER2



| Membro                                         | Attributo                                                                                                                                                                                                                                        |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **dwBitRate**                                  | [**MF \_ MT \_ AVG \_ BITRATE**](mf-mt-avg-bitrate-attribute.md)                                                                                                                                                                                      |
| **dwBitErrorRate**                             | [**MF \_ MT \_ AVG \_ BIT \_ ERROR \_ RATE**](mf-mt-avg-bit-error-rate-attribute.md)                                                                                                                                                                      |
| **AvgTimePerFrame**                            | [**MF \_ MT \_ FRAME \_ RATE;**](mf-mt-frame-rate-attribute.md)usare [**MFAverageTimePerFrameToFrameRate**](/windows/desktop/api/mfapi/nf-mfapi-mfaveragetimeperframetoframerate) per calcolare questo valore.                                                                             |
| **dwInterlaceFlags**                           | [**MODALITÀ \_ INTERLACE MF MT \_ \_**](mf-mt-interlace-mode-attribute.md)                                                                                                                                                                                |
| **dwCopyProtectFlags**                         | Nessun equivalente definito                                                                                                                                                                                                                            |
| **dwPictAspectRatioX**, **dwPictAspectRatioY** | [**MF \_ MT \_ PIXEL \_ ASPECT \_ RATIO;**](mf-mt-pixel-aspect-ratio-attribute.md)deve eseguire la conversione dalle proporzioni dell'immagine alle proporzioni dell'immagine.                                                                                                      |
| **dwControlFlags**                             | [**MF \_ FLAG \_ DI CONTROLLO MT PAD \_ \_**](mf-mt-pad-control-flags-attribute.md). Se è presente il flag **\_ AMCONTROL COLORINFO \_ PRESENT,** impostare gli attributi di colore estesi descritti in [Informazioni sul colore estese](extended-color-information.md). |
| **bmiHeader.biWidth**, **bmiHeader.biHeight**  | [**DIMENSIONI \_ DEL FRAME MT \_ \_ MF**](mf-mt-frame-size-attribute.md)                                                                                                                                                                                        |
| **bmiHeader.biBitCount**                       | Implicito nel sottotipo ([**MF \_ MT \_ SUBTYPE**](mf-mt-subtype-attribute.md)).                                                                                                                                                                    |
| **bmiHeader.biCompression**                    | Implicito nel sottotipo.                                                                                                                                                                                                                         |
| **bmiHeader.biSizeImage**                      | [**DIMENSIONI DEL \_ CAMPIONE MF \_ \_ MT**](mf-mt-sample-size-attribute.md)                                                                                                                                                                                      |
| Informazioni sul riquadro                            | [**MF \_ MT \_ PALETTE**](mf-mt-palette-attribute.md)                                                                                                                                                                                               |



 

Gli attributi seguenti possono essere dedosi dalla struttura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) o [**VIDEOINFOHEADER2,**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) ma richiedono anche una certa conoscenza dei dettagli del formato. Ad esempio, diversi formati YUV hanno requisiti di stride diversi.

-   [**MF \_ MT \_ DEFAULT \_ STRIDE**](mf-mt-default-stride-attribute.md)
-   [**MF \_ MT \_ MINIMUM \_ DISPLAY \_ APERTURE**](mf-mt-minimum-display-aperture-attribute.md)
-   [**MF \_ MT \_ PAN \_ SCAN \_ APERTURE**](mf-mt-pan-scan-aperture-attribute.md)

### <a name="mpeg1videoinfo"></a>MPEG1VIDEOINFO



| Membro                                   | Attributo                                                                       |
|------------------------------------------|---------------------------------------------------------------------------------|
| **dwStartTimeCode**                      | [**CODICE ORA \_ DI \_ INIZIO MPEG MF MT \_ \_ \_**](mf-mt-mpeg-start-time-code-attribute.md) |
| **bSequenceHeader**                      | [**INTESTAZIONE DELLA \_ SEQUENZA \_ MPEG MF MT \_ \_**](mf-mt-mpeg-sequence-header-attribute.md)  |
| **biXPelsPerMeter**, **biYPelsPerMeter** | [**PROPORZIONI \_ DEI PIXEL MF MT \_ \_ \_**](mf-mt-pixel-aspect-ratio-attribute.md)      |



 

### <a name="mpeg2videoinfo"></a>MPEG2VIDEOINFO



| Membro               | Attributo                                                                       |
|----------------------|---------------------------------------------------------------------------------|
| **dwStartTimeCode**  | [**CODICE ORA \_ DI \_ INIZIO MPEG MF MT \_ \_ \_**](mf-mt-mpeg-start-time-code-attribute.md) |
| **dwSequenceHeader** | [**INTESTAZIONE DELLA \_ SEQUENZA \_ MPEG MF MT \_ \_**](mf-mt-mpeg-sequence-header-attribute.md)  |
| **dwProfile**        | [**PROFILO \_ \_ MPEG2 MF MT \_**](mf-mt-mpeg2-profile-attribute.md)                 |
| **dwLevel**          | [**MF \_ MT \_ MPEG2 \_ LEVEL**](mf-mt-mpeg2-level-attribute.md)                     |
| **dwFlags**          | [**MF \_ MT \_ MPEG2 \_ FLAGS**](mf-mt-mpeg2-flags-attribute.md)                     |



 

## <a name="examples"></a>Esempio

Il codice seguente inserisce una struttura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) da un tipo di supporto video. Si noti che queste conversioni perdono alcune delle informazioni sul formato (interlacciamento, frequenza fotogrammi, dati di colore estesi). Tuttavia, potrebbe essere utile quando si salva una bitmap da un fotogramma video, ad esempio.


```C++
#include <dshow.h>
#include <dvdmedia.h>

// Converts a video type to a BITMAPINFO structure.
// The caller must free the structure by calling CoTaskMemFree.

// Note that this conversion loses some format information, including 
// interlacing, and frame rate.

HRESULT GetBitmapInfoHeaderFromMFMediaType(
    IMFMediaType *pType,            // Pointer to the media type.
    BITMAPINFOHEADER **ppBmih,      // Receives a pointer to the structure. 
    DWORD *pcbSize)                 // Receives the size of the structure.
{
    *ppBmih = NULL;
    *pcbSize = 0;

    GUID majorType = GUID_NULL;
    AM_MEDIA_TYPE *pmt = NULL;
    DWORD cbSize = 0;
    DWORD cbOffset = 0;
    BITMAPINFOHEADER *pBMIH = NULL;

    // Verify that this is a video type.
    HRESULT hr = pType->GetMajorType(&majorType);
    if (FAILED(hr))
    {
        goto done;
    }

    if (majorType != MFMediaType_Video)
    {
        hr = MF_E_INVALIDMEDIATYPE;
        goto done;
    }

    hr = pType->GetRepresentation(AM_MEDIA_TYPE_REPRESENTATION, (void**)&pmt);
    if (FAILED(hr))
    {
        goto done;
    }

    if (pmt->formattype == FORMAT_VideoInfo)
    {
        cbOffset = (FIELD_OFFSET(VIDEOINFOHEADER,bmiHeader));
    }
    else if (pmt->formattype == FORMAT_VideoInfo2)
    {
        cbOffset = (FIELD_OFFSET(VIDEOINFOHEADER2,bmiHeader));
    }
    else
    {
        hr = MF_E_INVALIDMEDIATYPE; // Unsupported format type.
        goto done;
    }

    if (pmt->cbFormat - cbOffset < sizeof(BITMAPINFOHEADER))
    {
        hr = E_UNEXPECTED; // Bad format size. 
        goto done;
    }

    cbSize = pmt->cbFormat - cbOffset;

    pBMIH = (BITMAPINFOHEADER*)CoTaskMemAlloc(cbSize);
    if (pBMIH == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }
    
    CopyMemory(pBMIH, pmt->pbFormat + cbOffset, cbSize);
    
    *ppBmih = pBMIH;
    *pcbSize = cbSize;

done:
    if (pmt)
    {
        pType->FreeRepresentation(AM_MEDIA_TYPE_REPRESENTATION, pmt);
    }
    return hr;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tipi di supporti](media-types.md)
</dt> </dl>

 

 
