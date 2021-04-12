---
description: Il decodificatore MPEG4 Part 2 video decodifica i flussi video codificati in base allo standard MPEG4 Part 2.
ms.assetid: 56e32d3c-9bd0-41fe-bb22-e4ff37b7cc5c
title: MPEG-4 Part 2 video decoder (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 777e6144684c799eb58f75afd4811ccc8871a46b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226525"
---
# <a name="mpeg-4-part-2-video-decoder"></a>MPEG-4 Part 2 video decoder

Il decodificatore MPEG4 Part 2 video decodifica i flussi video codificati in base allo standard MPEG4 Part 2.

È possibile creare un'istanza del decodificatore MPEG4 Part 2 video chiamando **CoCreateInstance**. Per creare un'istanza del decodificatore che si comporta come un oggetto DMO (DirectX Media Object), usare l'identificatore di classe **CLSID \_ CMpeg4sDecMediaObject**. Per creare un istanza del decodificatore che si comporta come una trasformazione Media Foundation (MFT), usare l'identificatore di classe **CLSID \_ CMpeg4sDecMFT**.

## <a name="input-types"></a>Tipi di input

Il decodificatore MPEG4 Part 2 video supporta i tipi di supporti di input seguenti.

-   \_M4S2 MEDIASUBTYPE
-   \_M4S2 MEDIASUBTYPE
-   \_MP4V MEDIASUBTYPE
-   \_MP4V MEDIASUBTYPE
-   MEDIASUBTYPE \_ mp4s (deprecato)
-   MEDIASUBTYPE \_ mp4s (deprecato)

## <a name="output-types"></a>Tipi di output

Il decodificatore MPEG4 Part 2 video supporta i sottotipi di supporti di output seguenti quando funge da DMO.

-   \_YV12 MEDIASUBTYPE
-   \_NV12 MEDIASUBTYPE
-   \_YUY2 MEDIASUBTYPE
-   \_UYVY MEDIASUBTYPE
-   \_YVYU MEDIASUBTYPE
-   \_NV11 MEDIASUBTYPE
-   \_Rgb32 MEDIASUBTYPE
-   \_RGB24 MEDIASUBTYPE
-   \_RGB565 MEDIASUBTYPE
-   \_RGB555 MEDIASUBTYPE
-   \_RGB8 MEDIASUBTYPE

Il decodificatore MPEG4 Part 2 video supporta i sottotipi di supporti di output seguenti quando funge da MFT.

-   \_NV12 MEDIASUBTYPE
-   \_YV12 MEDIASUBTYPE

## <a name="formats"></a>Formati

Il decodificatore MPEG4 Part 2 video accetta i formati seguenti.

-   [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)
-   [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) (VIH2)
-   [**MFVideoInfo**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoinfo)
-   [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) (viene utilizzata solo la parte VIH2 dell'intestazione).

## <a name="interfaces-for-the-dmo"></a>Interfacce per DMO

Se si crea un'istanza del decodificatore MPEG4 Part 2 video come DMO, il decodificatore espone le interfacce seguenti.

-   [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject)
-   [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi)

È possibile ottenere un'interfaccia [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) chiamando **CoCreateInstance** ed è possibile ottenere un'interfaccia [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) chiamando **QueryInterface**.

## <a name="interfaces-for-the-mft"></a>Interfacce per MFT

Se si crea un'istanza del decodificatore MPEG2 Part 2 video come MFT, il decodificatore espone le interfacce seguenti.

-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)
-   [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)
-   [**IMFQualityAdvise2**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2)
-   [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)
-   [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)

È possibile ottenere un puntatore all'interfaccia [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) chiamando **CoCreateInstance** ed è possibile ottenere un puntatore all'interfaccia [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) chiamando [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes). È possibile ottenere un puntatore all'interfaccia [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise) o [**IMFQualityAdvise2**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2) chiamando **QueryInterface** in MFT. È possibile ottenere un puntatore all'interfaccia [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) o [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) chiamando [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) e passando l'identificatore del servizio **MF \_ rate \_ Control \_ Service**.

## <a name="profiles-and-levels"></a>Profili e livelli

La specifica MPEG4 definisce diversi profili, ognuno dei quali specifica gli strumenti che un codificatore può usare per generare un flusso codificato. Il decodificatore del video MPEG4 part2 supporta due di questi profili: profilo visivo semplice e profilo semplice avanzato. In altre parole, il decodificatore MPEG4 Part 2 video può decodificare i flussi codificati in base al profilo visivo semplice o al profilo semplice avanzato.

Il profilo visivo semplice supporta la trasmissione di base di video a bassa velocità in modalità progressiva. Supporta solo le immagini intra e Prediction. Supporta anche la modalità di intestazione breve, che è compatibile con le versioni precedenti del profilo di base H. 263. A partire da Windows 10, il decoder MPEG-4 Part 2 video supporta anche H. 263v2 (H. 263 +) che supporta le dimensioni delle immagini personalizzate.

Il profilo semplice avanzato supporta tutti gli strumenti del profilo visivo semplice e supporta inoltre i video interlacciati, i frame B, la compensazione del movimento trimestrale, le tabelle di quantizzazione aggiuntive e la compensazione di movimento globale.

La specifica MPEG4 definisce anche diversi livelli, ognuno dei quali specifica i vincoli sul flusso di output generato da un codificatore.

La tabella seguente illustra i profili e i livelli, insieme alle risoluzioni tipiche, supportate dal decodificatore MPEG4 Part 2 video.



| Profilo         | Level | Risoluzione tipica |
|-----------------|-------|--------------------|
| Visualizzazione semplice   | 0     | 176 x 144          |
| Visualizzazione semplice   | 1     | 176 x 144          |
| Visualizzazione semplice   | 2     | 352 x 288          |
| Visualizzazione semplice   | 3     | 352 x 288          |
| SimpleVisual    | 4a    | 640 x 480          |
| Visualizzazione semplice   | 5     | 720 x 576          |
| Semplice avanzata | 0     | 176 x 144          |
| Semplice avanzata | 1     | 176 x 144          |
| Semplice avanzata | 2     | 352 x 288          |
| Semplice avanzata | 3     | 352 x 288          |
| Semplice avanzata | 3b    | 352 x 288          |
| Semplice avanzata | 4     | 352 x 756          |
| Semplice avanzata | 5     | 720 x 576          |



 

Per ulteriori informazioni sui profili e sui livelli, vedere la specifica MPEG4 Part 2 (ISO/IEC 14496-2): Information technology--Coding of audio-visual objects--Part 2: Visual.

## <a name="decoder-properties"></a>Proprietà decodificatore

Per impostare le proprietà nel decodificatore MPEG4 Part 2 video, usare l'interfaccia [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) o l'interfaccia [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .

Il decodificatore MPEG4 Part 2 video supporta le seguenti proprietà.



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
<td>Specifica la modalità di generazione delle anteprime.<br/> <dl> Windows 7.<br />
Sola scrittura.<br />
</dl></td>
<td><strong>VARIANT_FALSE</strong></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Commenti

Gli identificatori univoci globali (GUID) per i sottotipi di supporti RGB variano a seconda che un decodificatore funga da DMO o da un MFT. I GUID per i sottotipi di supporti non RGB sono gli stessi, indipendentemente dal fatto che un decodificatore funga da DMO o da un MFT. Per informazioni sui GUID che rappresentano sottotipi di supporti, vedere tipi di [supporti](media-types.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                              |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MP4SDecd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti codec](codecobjects.md)
</dt> </dl>

 

 
