---
description: Converte un flusso video tra i formati di colore.
ms.assetid: 1c15dc2b-0e69-4d16-af02-8056a1eb2c5c
title: Convertitore di colori DSP (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73a8418d6eeeffcf83a38452b19f18a6baa60bcc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484108"
---
# <a name="color-converter-dsp"></a>Convertitore di colori DSP

Converte un flusso video tra i formati di colore.

## <a name="clsid"></a>CLSID

\_CCOLORCONVERTDMO CLSID

## <a name="interfaces"></a>Interfacce

-   [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject)
-   [**IMFRealTimeClient**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient)
-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)
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
-   [\_larghezza COLORCONV \_ MFPKEY](mfpkey-colorconv-width.md)
-   [\_altezza COLORCONV \_ MFPKEY](mfpkey-colorconv-height.md)
-   [\_modalità COLORCONV \_ MFPKEY](mfpkey-colorconv-mode.md)

## <a name="remarks"></a>Commenti

Il convertitore di colori DSP viene implementato come un oggetto COM che può fungere da oggetto DirectXMedia (DMO) o da una trasformazione Media Foundation (MFT). L'oggetto ha un singolo identificatore di classe (CLSID), indipendentemente dal fatto che funga da DMO o da MFT. Per informazioni sul momento in cui un DSP funge da DMO o da un MFT, vedere [processori di segnali digitali](windowsmediadigitalsignalprocessors.md).

Gli identificatori univoci globali (GUID) per i sottotipi di supporti RGB variano a seconda che un DSP funga da DMO o da un MFT. I GUID per i sottotipi di supporti non RGB sono gli stessi, indipendentemente dal fatto che un DSP funga da DMO o da un MFT. Per informazioni sui GUID che rappresentano sottotipi di supporti, vedere GUID del [sottotipo video](video-subtype-guids.md).

Per impostazione predefinita, questo DSP copia l'intera immagine di origine nel buffer di output. Facoltativamente, è possibile specificare i rettangoli di origine e di destinazione. Il DSP copia la parte dell'immagine di origine definita dal rettangolo di origine e la scrive nel rettangolo di destinazione nel buffer di output. Il DSP non esegue alcun ridimensionamento. i rettangoli di origine e di destinazione devono avere le stesse dimensioni. I rettangoli di origine e di destinazione non possono superare i limiti del fotogramma video.

Tutte le proprietà, ad eccezione della [**\_ \_ modalità COLORCONV di MFPKEY**](mfpkey-colorconv-mode.md) , devono essere impostate in un gruppo. Se si imposta una di queste proprietà, è necessario impostare tutte le altre. In caso contrario, i rettangoli di origine e di destinazione potrebbero non essere validi, nel qual caso entrambi i metodi [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) e [**IMediaObject::P Rocessoutput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput) restituiranno **e \_ INVALIDARG**.

Il convertitore di colori non supporta tutte le combinazioni di formato di input e di output. In genere, è necessario impostare il formato dei supporti noto, ovvero input o output, ed enumerare i formati disponibili sul flusso opposto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Colorcnv.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Processori di segnale digitale](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 
