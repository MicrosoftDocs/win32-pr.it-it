---
title: Effetto con trasformazione affine 2D
description: L'effetto Di trasformazione affine 2D applica una trasformazione spaziale a un'immagine basata su una matrice 3X2 usando la trasformazione della matrice Direct2D e una delle sei modalità di interpolazione.
ms.assetid: E8973EBE-764C-4220-BB1E-3BFD4853582D
keywords:
- Effetto con trasformazione affine 2D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 337168db7a422a8a22785316d2af1960e3a78b2f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478097"
---
# <a name="2d-affine-transform-effect"></a>Effetto con trasformazione affine 2D

L'effetto Di trasformazione affine 2D applica una trasformazione spaziale a un'immagine [](direct2d-transforms-overview.md) basata su una matrice 3X2 usando la trasformazione della matrice Direct2D e una delle sei modalità di interpolazione. È possibile usare questo effetto per ruotare, ridimensionare, inclinare o traslare un'immagine. In caso contrario, è possibile combinare queste operazioni. I trasferimenti affine mantengono le linee parallele e il rapporto tra tre punti qualsiasi in un'immagine.

Il CLSID per questo effetto è CLSID \_ D2D12DAffineTransform.

-   [Immagine di esempio](#example-image)
-   [Proprietà degli effetti](#effect-properties)
-   [Modalità bordo](#border-modes)
-   [Modalità di interpolazione](#interpolation-modes)
-   [Bitmap di output](#output-bitmap)
-   [Requisiti](#requirements)
-   [Argomenti correlati](#related-topics)

## <a name="example-image"></a>Immagine di esempio



| Prima                                                             |
|--------------------------------------------------------------------|
| ![l'immagine prima dell'effetto.](images/default-before.jpg)         |
| After                                                              |
| ![l'immagine dopo la trasformazione.](images/21-2daffinetransform.png) |



 


```C++
ComPtr<ID2D1Effect> affineTransformEffect;
m_d2dContext->CreateEffect(CLSID_D2D12DAffineTransform, &affineTransformEffect);

affineTransformEffect->SetInput(0, bitmap);

D2D1_MATRIX_3X2_F matrix = D2D1::Matrix3x2F(0.9f, -0.1f,   0.1f, 0.9f,   8.0f, 45.0f);

affineTransformEffect->SetValue(D2D1_2DAFFINETRANSFORM_PROP_TRANSFORM_MATRIX, matrix);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(affineTransformEffect.Get());
m_d2dContext->EndDraw();
```



Questo effetto esegue questa operazione di matrice:

![operazione di matrice affine](images/affine-matrix-calculation.png)

Anche se la matrice di input è definita come matrice 3x2, l'ultima colonna viene riempita con 0, 0 e 1 per produrre una matrice quadrata. Ciò consente la moltiplicazione di matrici, in modo che le trasformazioni possano essere concatenate in una singola matrice.

## <a name="effect-properties"></a>Proprietà degli effetti




| Nome visualizzato ed enumerazione dell'indice | Descrizione | 
|------------------------------------|-------------|
| InterpolazioneMode<br /> D2D1_2DAFFINETRANSFORM_PROP_INTERPOLATION_MODE<br /> | Modalità di interpolazione usata per ridimensionare l'immagine. Esistono 6 modalità di scalabilità che variano in qualità e velocità.<br /> Il tipo è D2D1_2DAFFINETRANSFORM_INTERPOLATION_MODE.<br /> Il valore predefinito è D2D1_2DAFFINETRANSFORM_INTERPOLATION_MODE_LINEAR.<br /> | 
| BorderMode<br /> D2D1_2DAFFINETRANSFORM_PROP_BORDER_MODE<br /> | Modalità usata per calcolare il bordo dell'immagine, soft o hard. Per <a href="https://www.bing.com/search?q=Border+modes">altre informazioni, vedere</a> Modalità bordo. <br /> Il tipo è D2D1_BORDER_MODE.<br /> Il valore predefinito è D2D1_BORDER_MODE_SOFT.<br /> | 
| TransformMatrix<br /> D2D1_2DAFFINETRANSFORM_PROP_TRANSFORM_MATRIX<br /> | Matrice 3x2 per trasformare l'immagine usando la trasformazione della <a href="direct2d-transforms-overview.md">matrice</a>Direct2D. <br /> Il tipo è D2D1_MATRIX_3X2_F.<br /> Il valore predefinito è Matrix3x2F::Identity().<br /> | 
| Nitidezza<br /> D2D1_2DAFFINETRANSFORM_PROP_SHARPNESS<br /> | Nella modalità di interpolazione cubica di alta qualità, il livello di nitidezza del filtro di scala come float compreso tra 0 e 1. I valori sono senza unità. È possibile usare la nitidezza per regolare la qualità di un'immagine quando si ridimensiona l'immagine.<br /> Il fattore di nitidezza influisce sulla forma del kernel. Maggiore è il fattore di affilamento, più piccolo è il kernel. <br /><blockquote>[!Note]<br />Questa proprietà influisce solo sulla modalità di interpolazione cubica di alta qualità.</blockquote><br /> Il tipo è FLOAT.<br /> Il valore predefinito è 1,0f.<br /> | 




 

## <a name="border-modes"></a>Modalità bordo



| Nome                     | Descrizione                                                                                                      |
|--------------------------|------------------------------------------------------------------------------------------------------------------|
| MODALITÀ BORDO D2D1 \_ \_ \_ SOFT | L'effetto consente di riempire l'immagine con pixel neri trasparenti durante l'interpolazione, determinando un bordo soffice.<br/> |
| MODALITÀ BORDO D2D1 \_ \_ \_ HARD | L'effetto stringe l'output alle dimensioni dell'immagine di input. <br/>                                         |



 

## <a name="interpolation-modes"></a>Modalità di interpolazione



| Enumerazione                                                         | Descrizione                                                                                                                                                                                          |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ 2DAFFINETRANSFORM \_ INTERPOLATION \_ MODE \_ NEAREST \_ NEIGHBOR     | Campiota il singolo punto più vicino e lo usa. Questa modalità usa meno tempo di elaborazione, ma restituisce l'immagine di qualità più bassa.                                                                           |
| D2D1 \_ 2DAFFINETRANSFORM \_ INTERPOLAZIONE \_ \_ LINEARE                | Usa un campione di quattro punti e un'interpolazione lineare. Questa modalità usa più tempo di elaborazione rispetto alla modalità vicina più vicina, ma restituisce un'immagine di qualità superiore.                                           |
| D2D1 \_ 2DAFFINETRANSFORM \_ INTERPOLATION \_ MODE \_ CUBIC                 | Usa un kernel cubico di 16 campioni per l'interpolazione. Questa modalità usa la maggior parte del tempo di elaborazione, ma restituisce un'immagine di qualità superiore.                                                                        |
| D2D1 \_ 2DAFFINETRANSFORM \_ INTERPOLATION \_ MODE \_ MULTI \_ SAMPLE \_ LINEAR | Usa 4 campioni lineari all'interno di un singolo pixel per un anti-aliasing del bordo valido. Questa modalità è buona per ridurre di piccole quantità le immagini con pochi pixel.                                              |
| D2D1 \_ 2DAFFINETRANSFORM \_ INTERPOLATION \_ MODE \_ ANISOTROP           | Usa il filtro anisotropo per campionare un modello in base alla forma trasformata della bitmap.                                                                                                     |
| D2D1 \_ 2DAFFINETRANSFORM \_ INTERPOLATION \_ MODE \_ HIGH \_ QUALITY \_ CUBIC  | Usa un kernel cubico di qualità elevata di dimensioni variabili per eseguire un'operazione di pre-downscale dell'immagine in caso di downscaling nella matrice di trasformazione. Usa quindi la modalità di interpolazione cubica per l'output finale. |



 

> [!Note]  
> Se non si seleziona una modalità, per impostazione predefinita l'effetto è D2D1 \_ 2DAFFINETRANSFORM \_ INTERPOLATION \_ MODE \_ LINEAR.

 

> [!Note]  
> La modalità anisotrop genera mipmap durante il ridimensionamento, tuttavia, se si imposta la proprietà **Cached** su true sugli effetti immessi a questo effetto, le mipmap non verranno generate ogni volta per immagini sufficientemente piccole.

 

## <a name="output-bitmap"></a>Bitmap di output

Le dimensioni della bitmap di output dipendono dalla matrice di trasformazione applicata all'immagine.

L'effetto esegue l'operazione di trasformazione e quindi applica un rettangolo di selezione intorno al risultato. La bitmap di output è la dimensione del rettangolo di selezione.

## <a name="requirements"></a>Requisiti



| Requisito | valore |
|--------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato | Windows 8 e Platform Update per Windows 7 \[ app desktop \| Windows Store\] |
| Server minimo supportato | Windows 8 e Platform Update per Windows 7 \[ app desktop \| Windows Store\] |
| Intestazione                   | d2d1effects.h                                                                      |
| Libreria                  | d2d1.lib, dxguid.lib                                                               |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

