---
description: I seguenti GUID del sottotipo video vengono definiti nel file di intestazione mfapi. h. Per specificare il sottotipo, impostare l' \_ attributo del \_ sottotipo MF mt sul tipo di supporto.
ms.assetid: 7dfd85e6-936e-4b78-a2cb-a5d59153e1c4
title: GUID del sottotipo video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38829480aed7372496fc196cc6c55d781b672a2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528555"
---
# <a name="video-subtype-guids"></a>GUID del sottotipo video

I seguenti GUID del sottotipo video vengono definiti nel file di intestazione mfapi. h. Per specificare il sottotipo, impostare l'attributo del [**\_ \_ sottotipo MF mt**](mf-mt-subtype-attribute.md) sul tipo di supporto.

Quando si usano questi sottotipi, impostare l'attributo [di \_ \_ \_ tipo principale MF mt](mf-mt-major-type-attribute.md) su **MFMediaType \_ video**.

-   [Formati RGB non compressi](#uncompressed-rgb-formats)
-   [Formati YUV: 8 bit e pallettizzati](#yuv-formats-8-bit-and-palettized)
-   [Formati YUV: a 10 bit e a 16 bit](#yuv-formats-10-bit-and-16-bit)
-   [Formati di luminanza e profondità](#luminance-and-depth-formats)
-   [Tipi di video codificati](#encoded-video-types)
-   [Creazione di GUID di sottotipo da valori FourCC e D3DFORMAT](#creating-subtype-guids-from-fourccs-and-d3dformat-values)
-   [Argomenti correlati](#related-topics)

## <a name="uncompressed-rgb-formats"></a>Formati RGB non compressi



| GUID                             | Descrizione                                                                                     |
|----------------------------------|-------------------------------------------------------------------------------------------------|
| **\_RGB8 MFVideoFormat**          | RGB, 8 bit per pixel (BPP). (Lo stesso layout di memoria di **D3DFMT \_ P8**).                            |
| **\_RGB555 MFVideoFormat**        | RGB 555, 16 BPP. (Lo stesso layout di memoria di **D3DFMT \_ X1R5G5B5**).                                  |
| **\_RGB565 MFVideoFormat**        | RGB 565, 16 BPP. (Lo stesso layout di memoria di **D3DFMT \_ R5G6B5**).                                    |
| **\_RGB24 MFVideoFormat**         | RGB, 24 BPP.                                                                                    |
| **\_Rgb32 MFVideoFormat**         | RGB, 32 BPP.                                                                                    |
| **\_ARGB32 MFVideoFormat**        | RGB, 32 BPP con canale alfa.                                                                 |
| **\_A2R10G10B10 MFVideoFormat**   | RGB, 10 BPP per ogni colore e 2 BPP per alfa. (Lo stesso layout di memoria di **D3DFMT \_ A2B10G10R10**) |
| **\_A16B16G16R16F MFVideoFormat** | RGB, 16 BPP con canale alfa. (Lo stesso layout di memoria di **D3DFMT \_ A16B16G16R16F**)               |



 

> [!Note]  
> Questi sottotipi non corrispondono ai GUID del sottotipo RGB usati negli SDK precedenti, ad esempio DirectShow.

 

## <a name="yuv-formats-8-bit-and-palettized"></a>Formati YUV: 8 bit e pallettizzati



| GUID                    | Formato | campionamento | Compresso o planare | BITS per canale |
|-------------------------|--------|----------|------------------|------------------|
| **\_AI44 MFVideoFormat** | AI44   | 4:4:4    | Compressi           | Pallettizzati       |
| **\_AYUV MFVideoFormat** | AYUV   | 4:4:4    | Compressi           | 8                |
| **\_I420 MFVideoFormat** | I420   | 4:2:0    | Planare           | 8                |
| **\_IYUV MFVideoFormat** | IYUV   | 4:2:0    | Planare           | 8                |
| **\_NV11 MFVideoFormat** | NV11   | 4:1:1    | Planare           | 8                |
| **\_NV12 MFVideoFormat** | NV12   | 4:2:0    | Planare           | 8                |
| **\_UYVY MFVideoFormat** | UYVY   | 4:2:2    | Compressi           | 8                |
| **\_Y41P MFVideoFormat** | Y41P   | 4:1:1    | Compressi           | 8                |
| **\_Y41T MFVideoFormat** | Y41T   | 4:1:1    | Compressi           | 8                |
| **\_Y42T MFVideoFormat** | Y42T   | 4:2:2    | Compressi           | 8                |
| **\_YUY2 MFVideoFormat** | YUY2   | 4:2:2    | Compressi           | 8                |
| **\_YVU9 MFVideoFormat** | YVU9   | 8:4:4    | Planare           | 9                |
| **\_YV12 MFVideoFormat** | YV12   | 4:2:0    | Planare           | 8                |
| **\_YVYU MFVideoFormat** | YVYU   | 4:2:2    | Compressi           | 8                |



 

I formati YUV consigliati sono descritti in dettaglio nell'argomento [formati YUV a 8 bit consigliati per il rendering dei video](recommended-8-bit-yuv-formats-for-video-rendering.md).

> [!Note]  
> I420 e IYUV hanno lo stesso layout in memoria, ma sono assegnati GUID di sottotipi distinti. I GUID del sottotipo corrispondono ai codici FOURCC ' I420' è IYUV '; Per ulteriori informazioni, vedere [video FourCC](video-fourccs.md) .

 

## <a name="yuv-formats-10-bit-and-16-bit"></a>Formati YUV: a 10 bit e a 16 bit



| GUID                    | Formato | campionamento | Compresso o planare | BITS per canale |
|-------------------------|--------|----------|------------------|------------------|
| **\_P010 MFVideoFormat** | P010   | 4:2:0    | Planare           | 10               |
| **\_P016 MFVideoFormat** | P016   | 4:2:0    | Planare           | 16               |
| **\_P210 MFVideoFormat** | P210   | 4:2:2    | Planare           | 10               |
| **\_P216 MFVideoFormat** | P216   | 4:2:2    | Planare           | 16               |
| **\_V210 MFVideoFormat** | V210   | 4:2:2    | Compressi           | 10               |
| **\_V216 MFVideoFormat** | v216   | 4:2:2    | Compressi           | 16               |
| **\_V410 MFVideoFormat** | V40    | 4:4:4    | Compressi           | 10               |
| **\_Y210 MFVideoFormat** | Y210   | 4:2:2    | Compressi           | 10               |
| **\_Y216 MFVideoFormat** | Y216   | 4:2:2    | Compressi           | 16               |
| **\_Y410 MFVideoFormat** | Y40    | 4:4:4    | Compressi           | 10               |
| **\_Y416 MFVideoFormat** | Y416   | 4:4:4    | Compressi           | 16               |



 

Per ulteriori informazioni su questi formati, vedere [formati video YUV a 10 bit e a 16 bit](10-bit-and-16-bit-yuv-video-formats.md).

## <a name="luminance-and-depth-formats"></a>Formati di luminanza e profondità



| GUID                   | Descrizione                                                          |
|------------------------|----------------------------------------------------------------------|
| **\_L8 MFVideoFormat**  | solo luminanza a 8 bit. (BPP). (Lo stesso layout di memoria di **D3DFMT \_ L8**). |
| **\_L16 MFVideoFormat** | solo luminanza a 16 bit. (Lo stesso layout di memoria di **D3DFMT \_ L16**).      |
| **\_D16 MFVideoFormat** | profondità del buffer z a 16 bit. (Lo stesso layout di memoria di **D3DFMT \_ D16**).      |



 

## <a name="encoded-video-types"></a>Tipi di video codificati



| GUID                        | FOURCC         | Descrizione                                                                                                                                                                                                                                                                                                 |
|-----------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_DV25 MFVideoFormat**     | DV25         | DVCPRO 25 (525-60 o 625-50).                                                                                                                                                                                                                                                                               |
| **\_DV50 MFVideoFormat**     | DV50         | DVCPRO 50 (525-60 o 625-50).                                                                                                                                                                                                                                                                               |
| **\_DVC MFVideoFormat**      | DVC         | Video DVC/DV.                                                                                                                                                                                                                                                                                               |
| **\_DVH1 MFVideoFormat**     | 'dvh1'         | DVCPRO 100 (1080/60i, 1080/50i o 720/60P).                                                                                                                                                                                                                                                                |
| **\_DVHD MFVideoFormat**     | 'dvhd'         | HD-DVCR (1125-60 o 1250-50).                                                                                                                                                                                                                                                                               |
| **\_DVSD MFVideoFormat**     | DVSD         | SDL-DVCR (525-60 o 625-50).                                                                                                                                                                                                                                                                                |
| **\_DVSL MFVideoFormat**     | 'dvsl'         | SD-DVCR (525-60 o 625-50).                                                                                                                                                                                                                                                                                 |
| **\_H263 MFVideoFormat**     | H263         | Video H. 263.                                                                                                                                                                                                                                                                                                |
| **MFVideoFormat \_ H264**     | H264         | Video H. 264.<br/> Gli esempi di supporti contengono dati Bitstream H. 264 con codici iniziali e con SPS/PPS con interfoliazione. Ogni esempio contiene un'immagine completa, ovvero un campo o un frame.<br/>                                                                                                       |
| **\_H265 MFVideoFormat**     | 'H265'         | Video H. 265.                                                                                                                                                                                                                                                                                                |
| **MFVideoFormat \_ H264 \_ es** | Non applicabile | Flusso elementare H. 264.<br/> Questo tipo di supporto è identico a quello di **MFVideoFormat \_ H264**, ad eccezione degli esempi di supporti contenenti un bitstream H. 264 frammentato. Ogni esempio può contenere un'immagine parziale; più immagini complete; oppure una o più immagini complete e un'immagine parziale.<br/>           |
| **\_HEVC MFVideoFormat**     | HEVC         | Il profilo principale HEVC e il profilo immagine principale ancora.<br/> Ogni esempio contiene un'immagine completa.<br/> Supportato in Windows 8.1 e versioni successive. Il profilo principale HEVC e il flusso elementare del profilo immagine ancora principale. <br/>                                                              |
| **MFVideoFormat \_ HEVC \_ es** | HEV         | Questo tipo di supporto è identico a quello di **MFVideoFormat \_ HEVC**, ad eccezione dei campioni multimediali che contengono un bitstream HEVC frammentato. Ogni esempio può contenere un'immagine parziale; più immagini complete; oppure una o più immagini complete e un'immagine parziale.<br/> Supportato in Windows 8.1 e versioni successive.<br/> |
| **\_M4S2 MFVideoFormat**     | ' 4S2'         | Video MPEG-4 Part 2.                                                                                                                                                                                                                                                                                        |
| **\_MJPG MFVideoFormat**     | MJPG         | JPEG di movimento.                                                                                                                                                                                                                                                                                                |
| **\_Mp43 MFVideoFormat**     | 'MP43'         | Microsoft MPEG 4 codec versione 3. Questo codec non è più supportato.                                                                                                                                                                                                                                        |
| **\_Mp4s MFVideoFormat**     | Mp4s         | ISO MPEG 4 codec versione 1.                                                                                                                                                                                                                                                                                 |
| **\_MP4V MFVideoFormat**     | MP4V         | Video MPEG-4 Part 2.                                                                                                                                                                                                                                                                                        |
| **MFVideoFormat \_ MPEG2**    | Non applicabile | Video MPEG-2. (Equivalente a **MEDIASUBTYPE \_ MPEG2 \_ video** in DirectShow).                                                                                                                                                                                                                                 |
| **\_VP80 MFVideoFormat**     | MPG1         | Video di VP8.                                                                                                                                                                                                                                                                                                  |
| **\_VP90 MFVideoFormat**     | MPG1         | Video di VP9.                                                                                                                                                                                                                                                                                                  |
| **\_MPG1 MFVideoFormat**     | MPG1         | Video MPEG-1.                                                                                                                                                                                                                                                                                               |
| **\_MSS1 MFVideoFormat**     | 'MSS1'         | Windows Media Screen codec versione 1.                                                                                                                                                                                                                                                                       |
| **\_Mss2 MFVideoFormat**     | 'MSS2'         | Codec della schermata Windows Media Video 9.                                                                                                                                                                                                                                                                         |
| **\_WMV1 MFVideoFormat**     | WMV1         | Windows Media Video codec versione 7.                                                                                                                                                                                                                                                                        |
| **\_WMV2 MFVideoFormat**     | WMV2         | Codec Windows Media Video 8.                                                                                                                                                                                                                                                                                |
| **\_WMV3 MFVideoFormat**     | WMV3         | Codec Windows Media Video 9.                                                                                                                                                                                                                                                                                |
| **\_WVC1 MFVideoFormat**     | WVC1         | SMPTE 421M ("VC-1").                                                                                                                                                                                                                                                                                        |
| **\_420O MFVideoFormat**     | '420O'         | video Planar a 8 bit per canale Planar 4:2:0.                                                                                                                                                                                                                                                                   |
| **\_AV1 MFVideoFormat**     | 'AV01'         | Video di AV1.                                                                                                                                                                                                                                                                                                |



 

## <a name="creating-subtype-guids-from-fourccs-and-d3dformat-values"></a>Creazione di GUID di sottotipo da valori FourCC e D3DFORMAT

I formati video sono spesso rappresentati da valori FourCC o **D3DFORMAT** . Un intervallo di GUID è riservato per rappresentare questi valori come sottotipi. Questi GUID hanno il formato `XXXXXXXX-0000-0010-8000-00AA00389B71` , dove `XXXXXXXX` è il codice FourCC a 4 byte o il valore **D3DFORMAT** .

Se a un formato video è associato un valore FOURCC o **D3DFORMAT** , è possibile creare il GUID del sottotipo corrispondente come segue: iniziare con la costante **MFVideoFormat \_ base** e sostituire il primo **DWORD** del GUID con il video FourCC o il valore **D3DFORMAT** . A questo scopo, è possibile usare la macro del [**\_ \_ GUID Definisci MEDIATYPE**](/windows/desktop/api/mfapi/nf-mfapi-define_mediatype_guid) .

> [!Note]  
> DirectShow usa anche questo sistema per la maggior parte dei sottotipi video, ma non per i formati RGB non compressi. Pertanto, i sottotipi RGB in DirectShow non corrispondono ai sottotipi RGB in Media Foundation.

 

L'enumerazione **D3DFORMAT** viene definita nel file di intestazione d3d9types. h. La tabella seguente illustra i formati RGB non compressi più comuni e il valore **D3DFORMAT** corrispondente.



| Formato RGB                                                              | Valore **D3DFORMAT**     |
|-------------------------------------------------------------------------|-------------------------|
| RGB a 32 bit                                                              | **\_X8R8G8B8 D3DFMT**    |
| RGB a 32 bit con canale alfa                                           | **\_A8R8G8B8 D3DFMT**    |
| RGB a 24 bit                                                              | **\_R8G8B8 D3DFMT**      |
| RGB 555 (RGB a 16 bit)                                                    | **\_X1R5G5B5 D3DFMT**    |
| RGB 555 con canale alfa                                              | **\_A4R4G4B4 D3DFMT**    |
| RGB 565 (RGB a 16 bit)                                                    | **\_R5G6B5 D3DFMT**      |
| pallettizzati RGB a 8 bit                                                    | **D3DFMT \_ P8**          |
| A2 R10 G10 B10 (RGB a 32 bit con canale alfa, 10 bit per canale RGB) | **\_A2R10G10B10 D3DFMT** |
| A2 B10 G10 R10 (RGB a 32 bit con canale alfa, 10 bit per canale RGB) | **\_A2B10G10R10 D3DFMT** |
| solo luminanza a 8 bit.                                                   | **\_L8 D3DFMT**          |
| solo luminanza a 16 bit.                                                  | **\_L16 D3DFMT**         |
| profondità del buffer z a 16 bit                                                   | **\_D16 D3DFMT**         |



 

Per ulteriori informazioni su fourcc, vedere il [video FourCC](video-fourccs.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[GUID di tipo multimediale](media-type-guids.md)
</dt> <dt>

[**sottotipo MF \_ mt \_**](mf-mt-subtype-attribute.md)
</dt> <dt>

[Tipi di supporto](media-types.md)
</dt> <dt>

[Tipi di supporti video](video-media-types.md)
</dt> </dl>

 

 




