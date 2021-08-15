---
description: Converte un flusso video tra formati di colore.
ms.assetid: 1c15dc2b-0e69-4d16-af02-8056a1eb2c5c
title: Color Converter DSP (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e97db9f3131ed7cea9076255005149544363ba8d6b548736a211973cda3999d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117880663"
---
# <a name="color-converter-dsp"></a>Provider di servizi di conversione colori

Converte un flusso video tra formati di colore.

## <a name="clsid"></a>CLSID

CLSID \_ CColorConvertDMO

## <a name="interfaces"></a>Interfacce

-   [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject)
-   [**IMFRealTimeClient**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient)
-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [**Ipropertystore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)
-   [IWMColorConvProps](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcolorconvprops)

## <a name="input-formats"></a>Formati di input

-   RGB 24
-   RGB 32
-   RGB 555
-   RGB 565
-   RGB 8
-   AYUV
-   I420
-   IYUV
-   NV11
-   NV12
-   UYVY
-   V216
-   V410
-   Y41P
-   Y41T
-   Y42T
-   YUY2
-   YV12
-   YVU9
-   YVYU

## <a name="output-formats"></a>Formati di output

-   RGB 24
-   RGB 32
-   RGB 555
-   RGB 565
-   RGB 8
-   AYUV
-   I420
-   IYUV
-   NV11
-   NV12
-   UYVY
-   V216
-   V410
-   YUY2
-   YV12
-   YVYU

## <a name="properties"></a>Proprietà

-   [MFPKEY \_ COLORCONV \_ SRCLEFT](mfpkey-colorconv-srcleft.md)
-   [MFPKEY \_ COLORCONV \_ SRCTOP](mfpkey-colorconv-srctop.md)
-   [MFPKEY \_ COLORCONV \_ DSTLEFT](mfpkey-colorconv-dstleft.md)
-   [MFPKEY \_ COLORCONV \_ DSTTOP](mfpkey-colorconv-dsttop.md)
-   [MFPKEY \_ COLORCONV \_ WIDTH](mfpkey-colorconv-width.md)
-   [MFPKEY \_ COLORCONV \_ HEIGHT](mfpkey-colorconv-height.md)
-   [MODALITÀ MFPKEY \_ \_ COLORCONV](mfpkey-colorconv-mode.md)

## <a name="remarks"></a>Commenti

Color Converter DSP viene implementato come oggetto COM che può fungere da oggetto DirectXMedia (DMO) o da Media Foundation Transform (MFT). L'oggetto ha un singolo identificatore di classe (CLSID) indipendentemente dal fatto che agisca come DMO o MFT. Per informazioni su quando un DSP funge da DMO o MFT, vedere [Processori del segnale digitale](windowsmediadigitalsignalprocessors.md).

Gli identificatori univoci globali (GUID) per i sottotipi di supporti RGB variano a seconda che un provider di servizi multimediali agirà come DMO o MFT. I GUID per i sottotipi multimediali non RGB sono gli stessi, indipendentemente dal fatto che un provider di servizi multimediali agirà come DMO o MFT. Per informazioni sui GUID che rappresentano i sottotipi multimediali, vedere [GUID di sottotipo video](video-subtype-guids.md).

Per impostazione predefinita, questo provider di servizi copia l'intera immagine di origine nel buffer di output. Facoltativamente, è possibile specificare rettangoli di origine e di destinazione. Il DSP copia la parte dell'immagine di origine definita dal rettangolo di origine e la scrive nel rettangolo di destinazione nel buffer di output. DSP non esegue alcuna operazione di ridimensionamento. I rettangoli di origine e di destinazione devono avere le stesse dimensioni. I rettangoli di origine e di destinazione non possono superare i limiti del fotogramma video.

Tutte le proprietà, ad [**eccezione di MFPKEY \_ COLORCONV \_ MODE,**](mfpkey-colorconv-mode.md) devono essere impostate in un gruppo. Se si imposta una di queste proprietà, è necessario impostare tutte le altre. In caso contrario, i rettangoli di origine e di destinazione potrebbero non essere validi, nel qual caso entrambi i metodi [**IMFTransform::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) e [**IMediaObject::P rocessOutput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput) restituiranno **E \_ INVALIDARG**.

Il convertitore di colori non supporta tutte le combinazioni di formato di input e formato di output. In genere, è necessario impostare il formato multimediale che si conosce, input o output, e quindi enumerare i formati disponibili nel flusso opposto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Colorcnv.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Processori di segnali digitali](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 
