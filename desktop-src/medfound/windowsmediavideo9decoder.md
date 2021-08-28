---
description: Il Windows decoder Media Video 9 decodifica i flussi video codificati dal Windows Media Video Encoder.
ms.assetid: 08f68d1c-c226-4bf6-abd0-fce0f9ddbc05
title: Windows Decodificatore Media Video 9 (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df973e78f69e1f1ff0e649b2c4f5637380be9f27
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474307"
---
# <a name="windows-media-video-9-decoder"></a>Windows Decodificatore Media Video 9

Il Windows decoder Media Video 9 decodifica i flussi video codificati dal Windows [**Media Video Encoder.**](windowsmediavideo9encoder.md) Il codificatore e il decodificatore supportano le quattro categorie di video codificate seguenti.

-   Windows Profilo semplice di Media Video 9
-   Windows Profilo principale di Media Video 9
-   Windows Profilo avanzato di Media Video 9
-   Windows Immagine di Media Video 9.1

## <a name="class-identifier"></a>Identificatore di classe

L'identificatore di classe (CLSID) per il decodificatore Windows Media Video è rappresentato dalla costante **CLSID \_ CWMVDecMediaObject**. È possibile creare un'istanza del decodificatore video chiamando **CoCreateInstance**.

## <a name="interfaces"></a>Interfacce

Un oggetto decodificatore video espone [**l'interfaccia IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) in modo che l'oggetto possa essere usato come oggetto multimediale DirectX (DMO) e espone l'interfaccia [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) in modo che l'oggetto possa essere usato come trasformazione Media Foundation (MFT).

Un decodificatore video si comporta come DMO o MFT a seconda delle interfacce che si ottengono e della versione di Windows in esecuzione. La tabella seguente illustra le condizioni in cui un decodificatore video si comporta come DMO o MFT.



| Sistema operativo            | Comportamento del decodificatore                                                                                                                                                      |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP                  | Un Windows video decoder multimediale si comporta sempre come DMO.                                                                                                                |
| Windows Vista e Windows 7 | Per impostazione predefinita, Windows decodificatore video multimediale si comporta come DMO. Se si ottiene [**un'interfaccia IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) in un decodificatore video, si comporta come un MFT. |



 

A partire da Windows 7, il decodificatore Windows Video multimediale implementa [**l'interfaccia IDMOQualityControl.**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-idmoqualitycontrol)

## <a name="input-formats"></a>Formati di input

La tabella seguente illustra i codici a quattro caratteri (FOURCC) che corrispondono alle categorie di input codificate supportate dal decodificatore Windows Media Video.



| Category                               | FOURCC                                   |
|----------------------------------------|------------------------------------------|
| Windows Profilo semplice di Media Video 9   | "WMV3"                                   |
| Windows Profilo principale di Media Video 9     | "WMV3"                                   |
| Windows Profilo avanzato di Media Video 9 | "WVC1"                                   |
| Windows Immagine di Media Video 9.1          | "WMVP" per la versione 9.1, "WVP2" per la versione 9.1 2 |



 

## <a name="output-formats"></a>Formati di output

Il Windows Media Video decoder supporta i sottotipi multimediali di output seguenti quando funge da DMO.

-   MEDIASUBTYPE \_ NV12
-   MEDIASUBTYPE \_ YV12
-   MEDIASUBTYPE \_ YUY2
-   MEDIASUBTYPE \_ UYVY
-   MEDIASUBTYPE \_ YVYU
-   MEDIASUBTYPE \_ NV11
-   MEDIASUBTYPE \_ RGB32
-   MEDIASUBTYPE \_ RGB24
-   MEDIASUBTYPE \_ RGB565
-   MEDIASUBTYPE \_ RGB555
-   MEDIASUBTYPE \_ RGB8

Il Windows Media Video decoder supporta i sottotipi multimediali di output seguenti quando funge da MFT.

-   MFVideoFormat \_ NV12
-   MFVideoFormat \_ YV12
-   MFVideoFormat \_ YUY2
-   MFVideoFormat \_ UYVY
-   MFVideoFormat \_ YVYU
-   MFVideoFormat \_ NV11
-   MFVideoFormat \_ RGB32
-   MFVideoFormat \_ RGB24
-   MFVideoFormat \_ RGB565
-   MFVideoFormat \_ RGB555
-   MFVideoFormat \_ RGB8

## <a name="properties"></a>Proprietà

Il Windows media video supporta le proprietà seguenti.




| Proprietà | Descrizione | 
|----------|-------------|
| <a href="mfpkey-decoder-deinterlacingproperty.md">MFPKEY_DECODER_DEINTERLACING</a> | Specifica se il codec decodifica i fotogrammi video interlacciati dal flusso compresso come fotogrammi progressivi.<br /><dl> Windows XP e versioni successive.<br />Profilo semplice, Profilo principale, Profilo avanzato.<br />Proprietà di lettura/scrittura.<br /></dl> | 
| <a href="mfpkey-dxva-enabledproperty.md">MFPKEY_DXVA_ENABLED</a> | Specifica se il decodificatore userà l'hardware di accelerazione video DirectX, se disponibile.<br /><dl> Windows XP e versioni successive.<br />Profilo semplice, Profilo principale, Profilo avanzato.<br />Sola scrittura.<br /></dl> | 
| <a href="mfpkey-avdecvideoswpowerlevelproperty.md">MFPKEY_AVDecVideoSWPowerLevel</a> | Specifica il livello di alimentazione per il decodificatore.<br /><dl> Windows 7.<br />Profilo semplice, Profilo principale, Profilo avanzato, Immagine.<br />Proprietà di lettura/scrittura.<br /></dl> | 
| <a href="mfpkey-fi-enabledproperty.md">MFPKEY_FI_ENABLED</a> | Specifica se il decodificatore deve usare l'interpolazione dei fotogrammi.<br /><dl> Windows XP e versioni successive.<br />Profilo semplice, Profilo principale, Profilo avanzato, Immagine.<br />Sola scrittura.<br /></dl> | 
| <a href="mfpkey-fi-supportedproperty.md">MFPKEY_FI_SUPPORTED</a> | Specifica se il decodificatore supporta l'interpolazione dei fotogrammi.<br /><dl> Windows XP e versioni successive.<br />Profilo semplice, Profilo principale, Profilo avanzato, Immagine<br />Di sola lettura.<br /></dl> | 
| <a href="mfpkey-numthreadsdecproperty.md">MFPKEY_NUMTHREADSDEC</a> | Specifica il numero di thread che verranno utilizzati dal decodificatore.<br /><dl> Windows Vista e versioni successive.<br />Profilo semplice, Profilo principale, Profilo avanzato, Immagine.<br />Proprietà di lettura/scrittura.<br /></dl> | 
| <a href="mfpkey-postprocessmodeproperty.md">MFPKEY_POSTPROCESSMODE</a> | Specifica la modalità di post-elaborazione per il decodificatore.<br /><dl> Windows Vista e versioni successive.<br />Profilo semplice, Profilo principale, Profilo avanzato, Immagine.<br />Sola scrittura.<br /></dl> | 
| <strong>g_wszWMVCNeedsDrain</strong> | Specifica se il decodificatore deve essere svuotato.<br /><dl> Windows 8<br />Di sola lettura.<br /></dl> Questa proprietà viene usata dal runtime di Windows Media Format. Il tipo di proprietà è <strong>VARIANT_BOOL</strong>. Se il valore è <strong>VARIANT_TRUE</strong>, il decodificatore deve essere svuotato dopo una discontinuità. Per altre informazioni sullo svuotamento di un MFT, vedere <a href="basic-mft-processing-model.md">Modello di elaborazione MFT di base</a>.<br /><blockquote>[!Note]<br />Per eseguire query su questa proprietà, usare <a href="/windows/desktop/com/ipropertybag-and-ipersistpropertybag"><strong>l'interfaccia IPropertyBag.</strong></a></blockquote><br /> | 




 

## <a name="remarks"></a>Commenti

La risoluzione massima consentita dal Windows Media Video 9 è 4096x4096.

## <a name="requirements"></a>Requisiti



| Requisito | valore |
|-------------------|-----------------------------------------------------------------------------------------|
| Client<br/> | Windows XP, Windows Vista o Windows 7<br/>                                       |
| Intestazione<br/> | <dl> <dt>Wmcodecdsp.h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Wmvdecod.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti codec](codecobjects.md)
</dt> <dt>

[Implementazione di codec](codecimplementation.md)
</dt> </dl>

 

 
