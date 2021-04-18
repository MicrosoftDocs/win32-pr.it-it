---
description: Il decodificatore Windows Media Video 9 decodifica i flussi video codificati dal codificatore Windows Media Video.
ms.assetid: 08f68d1c-c226-4bf6-abd0-fce0f9ddbc05
title: Decodificatore Windows Media Video 9 (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96d89e05f82ce503016a10d5591a23bc673d0db5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329985"
---
# <a name="windows-media-video-9-decoder"></a>Decodificatore Windows Media Video 9

Il decodificatore Windows Media Video 9 decodifica i flussi video codificati dal [**codificatore Windows Media video**](windowsmediavideo9encoder.md). Il codificatore e il decodificatore supportano le quattro categorie di video codificate seguenti.

-   Profilo semplice Windows Media Video 9
-   Profilo principale Windows Media Video 9
-   Profilo avanzato Windows Media Video 9
-   Immagine di Windows Media Video 9,1

## <a name="class-identifier"></a>Identificatore di classe

L'identificatore di classe (CLSID) per il decodificatore Windows Media Video è rappresentato dalla costante **CLSID \_ CWMVDecMediaObject**. È possibile creare un'istanza del decodificatore video chiamando **CoCreateInstance**.

## <a name="interfaces"></a>Interfacce

Un oggetto decodificatore video espone l'interfaccia [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) in modo che l'oggetto possa essere usato come DMO (DirectX Media Object) ed espone l'interfaccia [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) in modo che l'oggetto possa essere usato come trasformazione Media Foundation (MFT).

Un decodificatore video si comporta come DMO o MFT, a seconda delle interfacce ottenute e della versione di Windows in esecuzione. Nella tabella seguente vengono illustrate le condizioni in base alle quali un decodificatore video si comporta come DMO o MFT.



| Sistema operativo            | Comportamento del decodificatore                                                                                                                                                      |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP                  | Un decodificatore Windows Media video si comporta sempre come DMO.                                                                                                                |
| Windows Vista e Windows 7 | Per impostazione predefinita, un decodificatore Windows Media video si comporta come DMO. Se si ottiene un'interfaccia [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) in un decodificatore video, si comporta come un MFT. |



 

A partire da Windows 7, il decodificatore Windows Media Video implementa l'interfaccia [**IDMOQualityControl**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-idmoqualitycontrol) .

## <a name="input-formats"></a>Formati di input

La tabella seguente illustra i codici a quattro caratteri (fourcc) che corrispondono alle categorie di input codificati supportati dal decodificatore Windows Media Video.



| Category                               | FOURCC                                   |
|----------------------------------------|------------------------------------------|
| Profilo semplice Windows Media Video 9   | WMV3                                   |
| Profilo principale Windows Media Video 9     | WMV3                                   |
| Profilo avanzato Windows Media Video 9 | WVC1                                   |
| Immagine di Windows Media Video 9,1          | "WMVP" per 9,1, "WVP2" per 9,1 versione 2 |



 

## <a name="output-formats"></a>Formati di output

Il decodificatore Windows Media Video supporta i sottotipi di supporti di output seguenti quando funge da DMO.

-   \_NV12 MEDIASUBTYPE
-   \_YV12 MEDIASUBTYPE
-   \_YUY2 MEDIASUBTYPE
-   \_UYVY MEDIASUBTYPE
-   \_YVYU MEDIASUBTYPE
-   \_NV11 MEDIASUBTYPE
-   \_Rgb32 MEDIASUBTYPE
-   \_RGB24 MEDIASUBTYPE
-   \_RGB565 MEDIASUBTYPE
-   \_RGB555 MEDIASUBTYPE
-   \_RGB8 MEDIASUBTYPE

Il decodificatore Windows Media Video supporta i sottotipi di supporti di output seguenti quando funge da MFT.

-   \_NV12 MFVideoFormat
-   \_YV12 MFVideoFormat
-   \_YUY2 MFVideoFormat
-   \_UYVY MFVideoFormat
-   \_YVYU MFVideoFormat
-   \_NV11 MFVideoFormat
-   \_Rgb32 MFVideoFormat
-   \_RGB24 MFVideoFormat
-   \_RGB565 MFVideoFormat
-   \_RGB555 MFVideoFormat
-   \_RGB8 MFVideoFormat

## <a name="properties"></a>Proprietà

Il decodificatore Windows Media Video supporta le seguenti proprietà.



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
<td><a href="mfpkey-decoder-deinterlacingproperty.md">MFPKEY_DECODER_DEINTERLACING</a></td>
<td>Specifica se il codec decodifica i fotogrammi video interlacciati dal flusso compresso come frame progressivi.<br/> <dl> Windows XP e versioni successive.<br />
Profilo semplice, profilo principale, profilo avanzato.<br />
Proprietà di lettura/scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-dxva-enabledproperty.md">MFPKEY_DXVA_ENABLED</a></td>
<td>Specifica se il decodificatore userà l'hardware di accelerazione video DirectX, se disponibile.<br/> <dl> Windows XP e versioni successive.<br />
Profilo semplice, profilo principale, profilo avanzato.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-avdecvideoswpowerlevelproperty.md">MFPKEY_AVDecVideoSWPowerLevel</a></td>
<td>Specifica il livello di alimentazione per il decodificatore.<br/> <dl> Windows 7.<br />
Profilo semplice, profilo principale, profilo avanzato, immagine.<br />
Proprietà di lettura/scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-fi-enabledproperty.md">MFPKEY_FI_ENABLED</a></td>
<td>Specifica se il decodificatore deve usare l'interpolazione dei frame.<br/> <dl> Windows XP e versioni successive.<br />
Profilo semplice, profilo principale, profilo avanzato, immagine.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-fi-supportedproperty.md">MFPKEY_FI_SUPPORTED</a></td>
<td>Specifica se il decodificatore supporta l'interpolazione dei frame.<br/> <dl> Windows XP e versioni successive.<br />
Profilo semplice, profilo principale, profilo avanzato, immagine<br />
Di sola lettura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-numthreadsdecproperty.md">MFPKEY_NUMTHREADSDEC</a></td>
<td>Specifica il numero di thread che saranno utilizzati dal decodificatore.<br/> <dl> Windows Vista e versioni successive.<br />
Profilo semplice, profilo principale, profilo avanzato, immagine.<br />
Proprietà di lettura/scrittura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-postprocessmodeproperty.md">MFPKEY_POSTPROCESSMODE</a></td>
<td>Specifica la modalità di post-elaborazione per il decodificatore.<br/> <dl> Windows Vista e versioni successive.<br />
Profilo semplice, profilo principale, profilo avanzato, immagine.<br />
Sola scrittura.<br />
</dl></td>
</tr>
<tr class="even">
<td><strong>g_wszWMVCNeedsDrain</strong></td>
<td>Specifica se il decodificatore deve essere svuotato.<br/> <dl> Windows 8<br />
Di sola lettura.<br />
</dl> Questa proprietà viene utilizzata dal runtime del formato Windows Media. Il tipo di proprietà è <strong>VARIANT_BOOL</strong>. Se il valore è <strong>VARIANT_TRUE</strong>, il decodificatore deve essere svuotato dopo una discontinuità. Per altre informazioni sullo svuotamento di un MFT, vedere <a href="basic-mft-processing-model.md">modello di elaborazione MFT di base</a>.<br/>
<blockquote>
[!Note]<br />
Per eseguire una query su questa proprietà, usare l'interfaccia <a href="/windows/desktop/com/ipropertybag-and-ipersistpropertybag"><strong>IPropertyBag</strong></a> .
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Commenti

La risoluzione massima consentita dal decodificatore Windows Media Video 9 è 4096x4096.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|-----------------------------------------------------------------------------------------|
| Client<br/> | Windows XP, Windows Vista o Windows 7<br/>                                       |
| Intestazione<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Wmvdecod.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti codec](codecobjects.md)
</dt> <dt>

[Implementazione del codec](codecimplementation.md)
</dt> </dl>

 

 
