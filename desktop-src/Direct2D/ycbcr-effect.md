---
title: Effetto YCbCr
description: Converte i dati JPEG YCbCr planari e chroma sottocampionati in RGB.
ms.assetid: E4492996-54DA-4C5F-B44C-8FBE97C8DD7D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5302300cc539571fabb1c3d786686ffc514636133391e706fc5963002656764
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119636091"
---
# <a name="ycbcr-effect"></a>Effetto YCbCr

Converte i dati JPEG YC<sub>b</sub>C<sub>r</sub> sottocampionati planari e chroma in RGB. Questo effetto presuppone che i dati YC<sub>b</sub>C<sub>r</sub> siano formattati in conformità con lo standard JPEG. I dati per gli input possono essere ottenuti da IWICPlanarBitmapSourceTransform. L'effetto YC<sub>b</sub>C<sub>r</sub> richiede due input. il primo deve essere una bitmap DXGI FORMAT R8 contenente dati luma e il secondo deve essere una \_ \_ bitmap DXGI \_ FORMAT R8G8 contenente dati \_ chroma sottocampionati. Per altre informazioni sull'uso di questo effetto, vedere [Supporto di JPEG YCbCr.](/windows/desktop/wic/jpeg-ycbcr-support)

Il CLSID per questo effetto è CLSID \_ D2D1YCbCr.

-   [Proprietà degli effetti](#effect-properties)
-   [Modalità di sottocampionamento](#subsampling-modes)
-   [Modalità di interpolazione](#interpolation-modes)
-   [Bitmap di output](#output-bitmap)
-   [Requisiti](#requirements)
-   [Argomenti correlati](#related-topics)

## <a name="effect-properties"></a>Proprietà degli effetti



| Enumerazione del nome visualizzato e dell'indice                                          | Descrizione                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ChromaSubsampling<br/> D2D1 \_ YCBCR \_ CHROMA \_ SUBSAMPLING<br/>    | Specifica il sottocampionamento della chroma dell'immagine chroma di input. <br/> Il tipo è D2D1 \_ YCBCR \_ CHROMA \_ SUBSAMPLING.<br/> Il valore predefinito è D2D1 \_ YCBCR \_ CHROMA \_ SUBSAMPLING \_ AUTO.<br/>                                                                                                |
| TransformMatrix <br/> MATRICE DI TRASFORMAZIONE DELLA PROPRIETÀ D2D1 \_ YCBCR \_ \_ \_<br/> | Matrice [3x2 che](/previous-versions/dotnet/netframework-3.0/ms750596(v=vs.85)) specifica la trasformazione affine allineata all'asse dell'immagine. Le trasformazioni allineate all'asse includono scale, capovolgimenti e rotazioni di 90 gradi. <br/> Il tipo è D2D1 \_ MATRIX \_ 3X2 \_ F.<br/> Il valore predefinito è Matrix3x2F::Identity().<br/> |
| InterpolationMode<br/> MODALITÀ INTERPOLAZIONE D2D1 \_ \_ YCBCR \_<br/>    | Modalità di interpolazione.<br/> Il tipo è D2D1 \_ YCBCR \_ INTERPOLATION \_ MODE.<br/>                                                                                                                                                                                                             |



 

## <a name="subsampling-modes"></a>Modalità di sottocampionamento



| Enumerazione                                       | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ YCBCR \_ CHROMA \_ SUBSAMPLING \_ AUTO<br/> | Questa modalità tenta di dedurre il sottocampionamento chroma dai limiti delle immagini di input. Quando questa opzione è selezionata, il piano più piccolo viene ricampionato in base alle dimensioni del piano più grande e il rettangolo di output di questo effetto è l'intersezione dei due piani. Quando si usa questa modalità, è necessario fare attenzione quando si applicano effetti ai piani di input che modificano i limiti dell'immagine, ad esempio la trasformazione del bordo, in modo da mantenere il rapporto di dimensioni desiderato tra i piani. <br/> |
| D2D1 \_ YCBCR \_ CHROMA \_ SUBSAMPLING \_ 420<br/>  | Il piano chroma viene sottocampionato orizzontalmente da e sottocampionato verticalmente da . Quando questa opzione è selezionata, il piano chroma viene upsampled orizzontalmente e verticalmente di 2x e il rettangolo di output di questo effetto è l'intersezione dei due piani.<br/>                                                                                                                                                                                                                          |
| D2D1 \_ YCBCR \_ CHROMA \_ SUBSAMPLING \_ 422<br/>  | Il piano chroma viene sottocampionato orizzontalmente da . Quando questa opzione è selezionata, il piano chroma viene upsampled orizzontalmente di 2x e il rettangolo di output di questo effetto è l'intersezione dei due piani.<br/>                                                                                                                                                                                                                                                                        |
| D2D1 \_ YCBCR \_ CHROMA \_ SUBSAMPLING \_ 444<br/>  | Il piano chroma non viene sottocampionato. Quando questa opzione è selezionata, il rettangolo di output dell'effetto è l'intersezione dei due piani.<br/>                                                                                                                                                                                                                                                                                                                                            |
| D2D1 \_ YCBCR \_ CHROMA \_ SUBSAMPLING \_ 440<br/>  | Il piano chroma viene sottocampionato verticalmente da . Quando questa opzione è selezionata, il piano chroma viene upsampled verticalmente di 2x e il rettangolo di output di questo effetto è l'intersezione dei due piani.<br/>                                                                                                                                                                                                                                                                            |



 

## <a name="interpolation-modes"></a>Modalità di interpolazione



| Enumerazione                                             | Descrizione                                                                                                                                                                                          |
|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ YCBCR \_ INTERPOLAZIONE \_ MODE NEAREST \_ \_ NEIGHBOR     | Campioni il singolo punto più vicino e lo usa. Questa modalità usa meno tempo di elaborazione, ma restituisce l'immagine di qualità più bassa.                                                                           |
| MODALITÀ DI INTERPOLAZIONE D2D1 \_ YCBCR \_ \_ \_ LINEARE                | Usa un campione di quattro punti e l'interpolazione lineare. Questa modalità usa più tempo di elaborazione rispetto alla modalità adiacente più vicina, ma restituisce un'immagine di qualità superiore.                                           |
| MODALITÀ DI INTERPOLAZIONE D2D1 \_ YCBCR \_ \_ \_ CUBICA                 | Usa un kernel cubico di 16 campioni per l'interpolazione. Questa modalità usa la maggior parte del tempo di elaborazione, ma restituisce un'immagine di qualità superiore.                                                                        |
| D2D1 \_ YCBCR \_ INTERPOLAZIONE \_ MODALITÀ \_ \_ MULTI-CAMPIONE \_ LINEARE | Usa 4 campioni lineari all'interno di un singolo pixel per un anti-aliasing dei bordi valido. Questa modalità è buona per ridurre di piccole quantità le immagini con pochi pixel.                                              |
| MODALITÀ DI INTERPOLAZIONE D2D1 \_ YCBCR \_ \_ \_ ANISO STANDBY           | Usa il filtro anisotropo per campionare un criterio in base alla forma trasformata della bitmap.                                                                                                     |
| CUBO DI ALTA QUALITÀ DELLA MODALITÀ DI INTERPOLAZIONE D2D1 \_ YCBCR \_ \_ \_ \_ \_  | Usa un kernel cubico di qualità elevata di dimensioni variabili per eseguire una scalabilità pre-ridimensionata dell'immagine se la scalabilità è coinvolta nella matrice di trasformazione. Usa quindi la modalità di interpolazione cubica per l'output finale. |



 

## <a name="output-bitmap"></a>Bitmap di output

Le dimensioni della bitmap di output dipendono dalla matrice di trasformazione applicata all'immagine.

L'effetto esegue l'operazione di trasformazione e quindi applica un rettangolo di selezione intorno al risultato. La bitmap di output è la dimensione del rettangolo di selezione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------------|---------------------------------------------------------------|
| Client minimo supportato | \[Windows 8.1 app desktop \| Windows Store\]            |
| Server minimo supportato | Windows Server 2012 App desktop R2 \[ \| Windows store\] |
| Intestazione                   | d2d1effects \_ 1.h                                              |
| Libreria                  | d2d1.lib, dxguid.lib                                          |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> <dt>

[Supporto di JPEG YCbCr](/windows/desktop/wic/jpeg-ycbcr-support)
</dt> <dt>

[**IWICPlanarBitmapSourceTransform**](/windows/desktop/api/wincodec/nn-wincodec-iwicplanarbitmapsourcetransform)
</dt> </dl>

 

