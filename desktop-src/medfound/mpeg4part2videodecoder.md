---
description: Il decodificatore MPEG4 Part 2 Video decodifica i flussi video codificati in base agli standard MPEG4 Part 2.
ms.assetid: 56e32d3c-9bd0-41fe-bb22-e4ff37b7cc5c
title: Decodificatore video MPEG-4 parte 2 (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 847e5be8c506e534c42962ecf6b0037a2ecb2f184c9c47fa92981fa32fd55422
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973020"
---
# <a name="mpeg-4-part-2-video-decoder"></a>Decodificatore video MPEG-4 parte 2

Il decodificatore MPEG4 Part 2 Video decodifica i flussi video codificati in base agli standard MPEG4 Part 2.

È possibile creare un'istanza del decodificatore MPEG4 Part 2 Video chiamando **CoCreateInstance.** Per creare un'istanza del decodificatore che si comporta come un oggetto multimediale DirectX (DMO), usare l'identificatore di classe **CLSID \_ CMpeg4sDecMediaObject**. Per creare un'istance del decodificatore che si comporta come una trasformazione Media Foundation (MFT), usare l'identificatore di classe **CLSID \_ CMpeg4sDecMFT**.

## <a name="input-types"></a>Tipi di input

Il decodificatore MPEG4 Part 2 Video supporta i tipi di supporti di input seguenti.

-   MEDIASUBTYPE \_ M4S2
-   MEDIASUBTYPE \_ m4s2
-   MEDIASUBTYPE \_ MP4V
-   MEDIASUBTYPE \_ mp4v
-   MEDIASUBTYPE \_ MP4S (deprecato)
-   MEDIASUBTYPE \_ mp4s (deprecato)

## <a name="output-types"></a>Tipi di output

Il decodificatore MPEG4 Part 2 Video supporta i sottotipi multimediali di output seguenti quando funge da DMO.

-   MEDIASUBTYPE \_ YV12
-   MEDIASUBTYPE \_ NV12
-   MEDIASUBTYPE \_ YUY2
-   MEDIASUBTYPE \_ UYVY
-   MEDIASUBTYPE \_ YVYU
-   MEDIASUBTYPE \_ NV11
-   MEDIASUBTYPE \_ RGB32
-   MEDIASUBTYPE \_ RGB24
-   MEDIASUBTYPE \_ RGB565
-   MEDIASUBTYPE \_ RGB555
-   MEDIASUBTYPE \_ RGB8

Il decodificatore MPEG4 Part 2 Video supporta i sottotipi multimediali di output seguenti quando funge da MFT.

-   MEDIASUBTYPE \_ NV12
-   MEDIASUBTYPE \_ YV12

## <a name="formats"></a>Formati

Il decodificatore MPEG4 Part 2 Video accetta i formati seguenti.

-   [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)
-   [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) (VIH2)
-   [**MFVideoInfo**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoinfo)
-   [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) (viene usata solo la parte VIH2 dell'intestazione).

## <a name="interfaces-for-the-dmo"></a>Interfacce per l'DMO

Se si crea un'istanza del decodificatore MPEG4 Part 2 Video come DMO, il decodificatore espone le interfacce seguenti.

-   [**Oggetto IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject)
-   [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi)

È possibile ottenere [**un'interfaccia IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) chiamando **CoCreateInstance** ed è possibile ottenere [**un'interfaccia ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) chiamando **QueryInterface.**

## <a name="interfaces-for-the-mft"></a>Interfacce per MFT

Se si crea un'istanza del decodificatore MPEG2 Part 2 Video come MFT, il decodificatore espone le interfacce seguenti.

-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [**Attributi IMF**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)
-   [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)
-   [**IMFQualityAdvise2**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2)
-   [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)
-   [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)

È possibile ottenere un puntatore all'interfaccia [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) chiamando **CoCreateInstance** ed è possibile ottenere un puntatore all'interfaccia [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) chiamando [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes). È possibile ottenere un puntatore [**all'interfaccia IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise) o [**IMFQualityAdvise2**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2) chiamando **QueryInterface** su MFT. È possibile ottenere un puntatore [**all'interfaccia IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) o [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) chiamando [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) e passando l'identificatore del servizio **MF \_ RATE CONTROL \_ \_ SERVICE.**

## <a name="profiles-and-levels"></a>Profili e livelli

La specifica MPEG4 definisce diversi profili, ognuno dei quali specifica gli strumenti che un codificatore può usare per generare un flusso codificato. MpEG4 Part2 Video Decoder supporta due di questi profili: Simple Visual Profile (Profilo visivo semplice) e Advanced Simple Profile (Profilo semplice avanzato). In altre parole, il decodificatore MPEG4 Part 2 Video può decodificare i flussi codificati in base a Simple Visual Profile o Advanced Simple Profile.

Simple Visual Profile supporta la trasmissione di base di video a bassa velocità in bit in modalità progressiva. Supporta solo immagini Intra e Prediction. Supporta anche la modalità intestazione breve, compatibile con le versioni precedenti del profilo di base H.263. A partire da Windows 10, MPEG-4 Part 2 Video Decoder supporta anche H.263v2 (H.263+) che supporta dimensioni di immagine personalizzate.

Advanced Simple Profile supporta tutti gli strumenti di Simple Visual Profile e, inoltre, supporta video interlacciati, fotogrammi B, compensazione del movimento trimestrale, tabelle di quantizzazione aggiuntive e compensazione del movimento globale.

La specifica MPEG4 definisce anche diversi livelli, ognuno dei quali specifica i vincoli sul flusso di output generato da un codificatore.

La tabella seguente illustra i profili e i livelli, insieme alle risoluzioni tipiche, supportati dal decodificatore VIDEO MPEG4 parte 2.



| Profilo         | Level | Risoluzione tipica |
|-----------------|-------|--------------------|
| Oggetto visivo semplice   | 0     | 176 x 144          |
| Oggetto visivo semplice   | 1     | 176 x 144          |
| Oggetto visivo semplice   | 2     | 352 x 288          |
| Oggetto visivo semplice   | 3     | 352 x 288          |
| SimpleVisual    | 4a    | 640 x 480          |
| Oggetto visivo semplice   | 5     | 720 x 576          |
| Advanced Simple | 0     | 176 x 144          |
| Advanced Simple | 1     | 176 x 144          |
| Advanced Simple | 2     | 352 x 288          |
| Advanced Simple | 3     | 352 x 288          |
| Advanced Simple | 3b    | 352 x 288          |
| Semplice avanzato | 4     | 352 x 756          |
| Semplice avanzato | 5     | 720 x 576          |



 

Per altre informazioni sui profili e i livelli, vedere la specifica MPEG4 Part 2 (ISO/IEC 14496-2): Information technology -- Coding of audio-visual objects -- Part 2: Visual(ISO/IEC 14496-2): Information technology -- Coding of audio-visual objects -- Part 2: Visual (Specifica MPEG4 parte 2: oggetto visivo).

## <a name="decoder-properties"></a>Proprietà decodificatore

Per impostare le proprietà nel decodificatore video MPEG4 part 2, usare [**l'interfaccia ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) o [**L'interfaccia IMFAttributes.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)

Il decodificatore video MPEG4 parte 2 supporta le proprietà seguenti.



<table>
<thead>
<tr class="header">
<th>Proprietà</th>
<th>Descrizione</th>
<th>Valore predefinito</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/avdecvideoswpowerlevel-property"><strong>CODECAPI_AVDecVideoSWPowerLevel</strong></a></td>
<td>Specifica il livello di alimentazione.<br/> <dl> Windows 7.<br />
Sola scrittura.<br />
</dl></td>
<td>100</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/DirectShow/avdecvideothumbnailgenerationmode-property"><strong>CODECAPI_AVDecVideoThumbnailGenerationMode</strong></a></td>
<td>Specifica la modalità di generazione dell'anteprima.<br/> <dl> Windows 7.<br />
Sola scrittura.<br />
</dl></td>
<td><strong>VARIANT_FALSE</strong></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Commenti

Gli identificatori univoci globali (GUID) per i sottotipi di supporti RGB variano a seconda che un decodificatore funge da DMO o MFT. I GUID per i sottotipi di supporti non RGB sono gli stessi, indipendentemente dal fatto che un decodificatore funge da DMO o MFT. Per informazioni sui GUID che rappresentano i sottotipi multimediali, vedere [Tipi di supporti](media-types.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                              |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MP4SDecd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti codec](codecobjects.md)
</dt> </dl>

 

 
