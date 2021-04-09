---
title: Effetto YCbCr
description: Converte i dati di YCbCr di JPEG sottocampionati planari e Chroma in RGB.
ms.assetid: E4492996-54DA-4C5F-B44C-8FBE97C8DD7D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c581effbadecc19c39161d2a2ec4af051d4195d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048581"
---
# <a name="ycbcr-effect"></a>Effetto YCbCr

Converte<sub>i dati</sub> di JPEG YC<sub>b</sub>C in formato Planar e Chroma sottocampionati in RGB. Questo effetto presuppone che i dati YC<sub>b</sub>C<sub>r</sub> siano formattati in conformità con lo standard JPEG. I dati per gli input possono essere ottenuti da IWICPlanarBitmapSourceTransform. L'effetto YC<sub>b</sub>C<sub>r</sub> richiede due input; il primo deve essere una \_ bitmap R8 di formato DXGI \_ contenente dati luma e il secondo deve essere un \_ formato DXGI \_ R8G8 bitmap contenente dati Chroma sottocampionati. Per ulteriori informazioni sull'utilizzo di questo effetto, vedere [supporto di JPEG YCbCr](/windows/desktop/wic/jpeg-ycbcr-support).

Il CLSID per questo effetto è CLSID \_ D2D1YCbCr.

-   [Proprietà effetto](#effect-properties)
-   [Modalità di campionamento secondario](#subsampling-modes)
-   [Modalità di interpolazione](#interpolation-modes)
-   [Bitmap di output](#output-bitmap)
-   [Requisiti](#requirements)
-   [Argomenti correlati](#related-topics)

## <a name="effect-properties"></a>Proprietà effetto



| Nome visualizzato e enumerazione dell'indice                                          | Descrizione                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ChromaSubsampling<br/> \_SOTTOcampionamento d2d1 YCbCr \_ Chroma \_<br/>    | Specifica il sottocampionamento Chroma dell'immagine croma di input. <br/> Il tipo è D2D1 \_ YCbCr \_ Chroma \_ sottocampionamento.<br/> Il valore predefinito è D2D1 \_ YCbCr \_ Chroma \_ subsampling \_ auto.<br/>                                                                                                |
| TransformMatrix <br/> \_Matrice di \_ \_ trasformazione prop YCbCr d2d1 \_<br/> | [Matrice 3x2](/previous-versions/dotnet/netframework-3.0/ms750596(v=vs.85)) che specifica la trasformazione affine allineata all'asse dell'immagine. Le trasformazioni allineate asse includono scala, Capovolgi e rotazioni di 90 gradi. <br/> Il tipo è D2D1 \_ Matrix \_ 3x2 \_ F.<br/> Il valore predefinito è Matrix3x2F:: Identity ().<br/> |
| InterpolationMode<br/> D2D1 \_ YCbCr- \_ modalità di interpolazione \_<br/>    | Modalità di interpolazione.<br/> Il tipo è D2D1 \_ YCbCr \_ Interpolation \_ mode.<br/>                                                                                                                                                                                                             |



 

## <a name="subsampling-modes"></a>Modalità di campionamento secondario



| Enumerazione                                       | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ YCbCr \_ - \_ sottocampionamento \_ automatico<br/> | Questa modalità tenta di dedurre il campionamento secondario Chroma dai limiti delle immagini di input. Quando questa opzione è selezionata, il piano più piccolo viene sottoposto a campionamento fino alla dimensione del piano più grande e il rettangolo di output di questo effetto è l'intersezione dei due piani. Quando si usa questa modalità, è necessario prestare attenzione quando si applicano effetti ai piani di input che modificano i limiti dell'immagine, ad esempio la trasformazione del bordo, in modo che venga mantenuto il rapporto di dimensioni desiderato tra i piani. <br/> |
| \_SOTTOcampionamento d2d1 YCbCr \_ Chroma \_ \_ 420<br/>  | Il piano Chroma viene sottocampionato orizzontalmente da e sottocampionato verticalmente da. Quando questa opzione è selezionata, il piano Chroma viene sottoposto a campionamento orizzontale e verticale di 2x e il rettangolo di output di questo effetto è l'intersezione dei due piani.<br/>                                                                                                                                                                                                                          |
| \_SOTTOcampionamento d2d1 YCbCr \_ Chroma \_ \_ 422<br/>  | Il piano Chroma viene sottocampionato orizzontalmente da. Quando questa opzione è selezionata, il piano Chroma viene sottoposto a campionamento orizzontale di 2x e il rettangolo di output di questo effetto è l'intersezione dei due piani.<br/>                                                                                                                                                                                                                                                                        |
| \_SOTTOcampionamento d2d1 YCbCr \_ Chroma \_ \_ 444<br/>  | Il piano croma non viene sottocampionato. Quando questa opzione è selezionata, il rettangolo di output di Effect s è l'intersezione dei due piani.<br/>                                                                                                                                                                                                                                                                                                                                            |
| \_SOTTOcampionamento d2d1 YCbCr \_ Chroma \_ \_ 440<br/>  | Il piano Chroma viene sottocampionato verticalmente da. Quando questa opzione è selezionata, il piano Chroma viene sottoposto a campionamento verticale da 2x e il rettangolo di output di questo effetto è l'intersezione dei due piani.<br/>                                                                                                                                                                                                                                                                            |



 

## <a name="interpolation-modes"></a>Modalità di interpolazione



| Enumerazione                                             | Descrizione                                                                                                                                                                                          |
|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ YCbCr- \_ modalità di interpolazione \_ \_ più vicina \_     | Campiona il punto singolo più vicino e lo utilizza. In questa modalità viene utilizzato un minor tempo di elaborazione, ma viene restituita l'immagine di qualità più bassa.                                                                           |
| D2D1 \_ YCbCr- \_ modalità di interpolazione \_ \_ lineare                | Usa un esempio a quattro punti e un'interpolazione lineare. Questa modalità utilizza un tempo di elaborazione maggiore rispetto alla modalità adiacente più vicina, ma restituisce un'immagine di qualità superiore.                                           |
| D2D1 \_ YCbCr- \_ modalità di interpolazione \_ \_ cubica                 | Usa un kernel cubico di esempio 16 per l'interpolazione. Questa modalità usa la maggior parte del tempo di elaborazione, ma restituisce un'immagine di qualità superiore.                                                                        |
| D2D1 \_ YCbCr- \_ modalità di interpolazione più \_ \_ \_ lineare di esempio \_ | USA 4 campioni lineari all'interno di un singolo pixel per l'anti-aliasing dei bordi validi. Questa modalità è ideale per ridurre le dimensioni delle immagini con pochi pixel.                                              |
| D2D1 \_ YCbCr \_ modalità di interpolazione \_ \_ anisotropico           | Usa il filtro anisotropico per campionare un modello in base alla forma trasformata della bitmap.                                                                                                     |
| D2D1 \_ YCbCr- \_ modalità di interpolazione \_ \_ alta \_ qualità \_ cubica  | Usa un kernel cubico a dimensione variabile di alta qualità per eseguire un'downscaling dell'immagine se downscaling è associato alla matrice di trasformazione. USA quindi la modalità di interpolazione cubica per l'output finale. |



 

## <a name="output-bitmap"></a>Bitmap di output

Le dimensioni della bitmap di output dipendono dalla matrice di trasformazione applicata all'immagine.

L'effetto esegue l'operazione di trasformazione e quindi applica un rettangolo di delimitazione intorno al risultato. La bitmap di output corrisponde alla dimensione del rettangolo di delimitazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------------|---------------------------------------------------------------|
| Client minimo supportato | App desktop Windows 8.1 app di \[ \| Windows Store\]            |
| Server minimo supportato | App desktop di Windows Server 2012 R2 app di \[ \| Windows Store\] |
| Intestazione                   | d2d1effects \_ 1. h                                              |
| Libreria                  | d2d1. lib, dxguid. lib                                          |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> <dt>

[Supporto di YCbCr JPEG](/windows/desktop/wic/jpeg-ycbcr-support)
</dt> <dt>

[**IWICPlanarBitmapSourceTransform**](/windows/desktop/api/wincodec/nn-wincodec-iwicplanarbitmapsourcetransform)
</dt> </dl>

 

