---
description: Conversioni di tipi di supporto
ms.assetid: 6aee18b8-79b1-47fb-816f-d1c2c77b3a03
title: Conversioni di tipi di supporto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee3a72e74439251f9661e0ff27166c504e47c238
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103761465"
---
# <a name="media-type-conversions"></a>Conversioni di tipi di supporto

In alcuni casi è necessario eseguire la conversione tra Media Foundation tipi di supporto e le strutture di tipo multimediale precedenti da DirectShow o Windows Media Format SDK.

### <a name="from-a-format-structure-to-a-media-foundation-type"></a>Da una struttura di formato a un tipo di Media Foundation

Le funzioni seguenti inizializzano un Media Foundation tipo di supporto da una struttura di formato. Queste funzioni sono utili anche se un flusso di dati o un'intestazione di file contiene una struttura di formato. L'intestazione di file per i file audio WAVE, ad esempio, contiene una struttura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .



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
<td><a href="/windows/win32/api/strmif/ns-strmif-am_media_type"><strong>AM_MEDIA_TYPE</strong></a> (DirectShow)<br/> <a href="/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type"><strong>DMO_MEDIA_TYPE</strong></a> (oggetti multimediali DirectX) <br/> <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type"><strong>WM_MEDIA_TYPE</strong></a> (Windows Media Format SDK) <br/>
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



 

### <a name="from-a-media-foundation-type-to-a-format-structure"></a>Da un tipo di Media Foundation a una struttura di formato

Le funzioni seguenti creano o inizializzano una struttura di formato da un tipo di supporto Media Foundation.



| Funzione                                                                             | Struttura di destinazione                                                                                                                                                                    |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IMFMediaType:: getrappresentation**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getrepresentation)            | [**Am \_ MEDIA \_ Type**](/windows/win32/api/strmif/ns-strmif-am_media_type), [**MFVIDEOFORMAT**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat), [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)o [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) |
| [**MFCreateAMMediaTypeFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateammediatypefrommfmediatype)     | [**\_tipo di supporto am \_**](/windows/win32/api/strmif/ns-strmif-am_media_type)                                                                                                                                          |
| [**MFCreateMFVideoFormatFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemfvideoformatfrommfmediatype) | [**MFVIDEOFORMAT**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat)                                                                                                                                              |
| [**MFCreateWaveFormatExFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatewaveformatexfrommfmediatype)   | [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) o [ **WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85))                                                                                    |
| [**MFInitAMMediaTypeFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfinitammediatypefrommfmediatype)         | [**\_tipo di supporto am \_**](/windows/win32/api/strmif/ns-strmif-am_media_type)                                                                                                                                          |



 

## <a name="format-mappings"></a>Mapping del formato

Nelle tabelle seguenti sono elencati gli attributi Media Foundation che corrispondono a diverse strutture di formato. Non tutti questi attributi possono essere tradotti direttamente. Per eseguire le conversioni, è necessario usare le funzioni elencate nella sezione precedente. Queste tabelle vengono fornite principalmente per riferimento.

### <a name="am_media_type"></a>\_tipo di supporto am \_



| Membro                   | Attributo                                                                            |
|--------------------------|--------------------------------------------------------------------------------------|
| **bTemporalCompression** | [**\_ \_ tutti gli esempi MF mt \_ \_ Independent**](mf-mt-all-samples-independent-attribute.md) |
| **bFixedSizeSamples**    | [**\_esempi di \_ \_ dimensioni fisse MF mt \_**](mf-mt-fixed-size-samples-attribute.md)           |
| **lSampleSize**          | [**\_ \_ dimensioni campione MF \_ mt**](mf-mt-sample-size-attribute.md)                          |



 

### <a name="waveformatex-waveformatextensible"></a>WAVEFORMATEX, WAVEFORMATEXTENSIBLE



| Membro                  | Attributo                                                                                                                                                                 |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **wFormatTag**          | [**sottotipo MF \_ mt \_**](mf-mt-subtype-attribute.md)<br/> Se **wFormatTag** è \_ Extensible Format WAVE \_ , il sottotipo viene trovato nel membro **subformat** .<br/> |
| **nChannels**           | [**numero \_ di \_ \_ canali audio MF mt \_**](mf-mt-audio-num-channels-attribute.md)                                                                                                |
| **nSamplesPerSec**      | [**\_ \_ campioni audio MF \_ mt \_ al \_ secondo**](mf-mt-audio-samples-per-second-attribute.md)                                                                                   |
| **nAvgBytesPerSec**     | [**\_ \_ Media byte audio MF mt \_ \_ \_ al \_ secondo**](mf-mt-audio-avg-bytes-per-second-attribute.md)                                                                              |
| **nBlockAlign**         | [**\_ \_ \_ allineamento blocchi audio MF \_ mt**](mf-mt-audio-block-alignment-attribute.md)                                                                                          |
| **wBitsPerSample**      | [**\_ \_ bit audio MF \_ mt \_ per \_ campione**](mf-mt-audio-bits-per-sample-attribute.md)                                                                                         |
| **wValidBitsPerSample** | [**\_ \_ bit validi per l'audio MF mt \_ \_ \_ per \_ campione**](mf-mt-audio-valid-bits-per-sample-attribute.md)                                                                            |
| **wSamplesPerBlock**    | [**\_ \_ campioni audio MF \_ mt \_ per \_ blocco**](mf-mt-audio-samples-per-block-attribute.md)                                                                                     |
| **dwChannelMask**       | [**\_ \_ \_ maschera canale audio MF \_ mt**](mf-mt-audio-channel-mask-attribute.md)                                                                                                |
| **Sottoformati**           | [**sottotipo MF \_ mt \_**](mf-mt-subtype-attribute.md)                                                                                                                        |
| Dati aggiuntivi              | [**\_ \_ dati utente MF \_ mt**](mf-mt-user-data-attribute.md)                                                                                                                   |



 

### <a name="videoinfoheader-videoinfoheader2"></a>VIDEOINFOHEADER, VIDEOINFOHEADER2



| Membro                                         | Attributo                                                                                                                                                                                                                                        |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **dwBitRate**                                  | [**\_velocità in \_ bit media MF mt \_**](mf-mt-avg-bitrate-attribute.md)                                                                                                                                                                                      |
| **dwBitErrorRate**                             | [**\_frequenza di \_ \_ errori bit \_ medio \_ MF mt**](mf-mt-avg-bit-error-rate-attribute.md)                                                                                                                                                                      |
| **AvgTimePerFrame**                            | [**MF \_ \_ \_ Frequenza fotogrammi mt**](mf-mt-frame-rate-attribute.md); usare [**MFAverageTimePerFrameToFrameRate**](/windows/desktop/api/mfapi/nf-mfapi-mfaveragetimeperframetoframerate) per calcolare questo valore.                                                                             |
| **dwInterlaceFlags**                           | [**\_modalità di \_ intreccio MF mt \_**](mf-mt-interlace-mode-attribute.md)                                                                                                                                                                                |
| **dwCopyProtectFlags**                         | Nessun equivalente definito                                                                                                                                                                                                                            |
| **dwPictAspectRatioX**, **dwPictAspectRatioY** | [**MF \_ Proporzioni MT \_ pixel \_ \_**](mf-mt-pixel-aspect-ratio-attribute.md); è necessario convertire le proporzioni dell'immagine in proporzioni dell'immagine.                                                                                                      |
| **dwControlFlags**                             | [**MF \_ \_flag di \_ controllo \_ del pad mt**](mf-mt-pad-control-flags-attribute.md). Se è presente il flag **AMCONTROL \_ COLORINFO \_ present** , impostare gli attributi di colore esteso descritti in [informazioni estese sui colori](extended-color-information.md). |
| **bmiHeader. biWidth**, **BmiHeader. biHeight**  | [**\_dimensioni del \_ frame MF mt \_**](mf-mt-frame-size-attribute.md)                                                                                                                                                                                        |
| **bmiHeader.biBitCount**                       | Implicito nel sottotipo ([**\_ \_ sottotipo MF mt**](mf-mt-subtype-attribute.md)).                                                                                                                                                                    |
| **bmiHeader. biCompression**                    | Implicito nel sottotipo.                                                                                                                                                                                                                         |
| **bmiHeader.biSizeImage**                      | [**\_ \_ dimensioni campione MF \_ mt**](mf-mt-sample-size-attribute.md)                                                                                                                                                                                      |
| Informazioni tavolozza                            | [**\_ \_ tavolozza MF mt**](mf-mt-palette-attribute.md)                                                                                                                                                                                               |



 

Gli attributi seguenti possono essere dedotti dalla struttura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) o [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) , ma richiedono anche una certa conoscenza dei dettagli del formato. Ad esempio, diversi formati YUV hanno requisiti di stride diversi.

-   [**\_ \_ stride predefinito MF \_ mt**](mf-mt-default-stride-attribute.md)
-   [**\_ \_ \_ apertura minima schermo \_ MF mt**](mf-mt-minimum-display-aperture-attribute.md)
-   [**\_apertura dell' \_ analisi della panoramica MF mt \_ \_**](mf-mt-pan-scan-aperture-attribute.md)

### <a name="mpeg1videoinfo"></a>MPEG1VIDEOINFO



| Membro                                   | Attributo                                                                       |
|------------------------------------------|---------------------------------------------------------------------------------|
| **dwStartTimeCode**                      | [**\_ \_ \_ codice ora di inizio \_ MF mt MPEG \_**](mf-mt-mpeg-start-time-code-attribute.md) |
| **bSequenceHeader**                      | [**\_intestazione della sequenza MF mt \_ MPEG \_ \_**](mf-mt-mpeg-sequence-header-attribute.md)  |
| **biXPelsPerMeter**, **biYPelsPerMeter** | [**proporzioni MF \_ mt \_ pixel \_ \_**](mf-mt-pixel-aspect-ratio-attribute.md)      |



 

### <a name="mpeg2videoinfo"></a>MPEG2VIDEOINFO



| Membro               | Attributo                                                                       |
|----------------------|---------------------------------------------------------------------------------|
| **dwStartTimeCode**  | [**\_ \_ \_ codice ora di inizio \_ MF mt MPEG \_**](mf-mt-mpeg-start-time-code-attribute.md) |
| **dwSequenceHeader** | [**\_intestazione della sequenza MF mt \_ MPEG \_ \_**](mf-mt-mpeg-sequence-header-attribute.md)  |
| **dwProfile**        | [**\_ \_ Profilo MPEG2 MF \_ mt**](mf-mt-mpeg2-profile-attribute.md)                 |
| **dwLevel**          | [**\_ \_ Livello MPEG2 MF \_ mt**](mf-mt-mpeg2-level-attribute.md)                     |
| **dwFlags**          | [**\_ \_ Flag MPEG2 MF \_ mt**](mf-mt-mpeg2-flags-attribute.md)                     |



 

## <a name="examples"></a>Esempio

Il codice seguente compila una struttura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) da un tipo di supporto video. Si noti che questa conversione perde alcune informazioni sul formato (interlacciamento, frequenza dei fotogrammi, dati di colore estesi). Tuttavia, potrebbe essere utile quando si salva una bitmap da un frame video, ad esempio.


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

[Tipi di supporto](media-types.md)
</dt> </dl>

 

 
