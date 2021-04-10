---
title: Effetto con trasformazione affine 2D
description: L'effetto di trasformazione affine 2D applica una trasformazione spaziale a un'immagine basata su una matrice 3X2 usando la trasformazione della matrice Direct2D e una delle sei modalità di interpolazione.
ms.assetid: E8973EBE-764C-4220-BB1E-3BFD4853582D
keywords:
- Effetto con trasformazione affine 2D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3017992d34cd98095f01192ea948684a6b52e53
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121694"
---
# <a name="2d-affine-transform-effect"></a>Effetto con trasformazione affine 2D

L'effetto di trasformazione affine 2D applica una trasformazione spaziale a un'immagine basata su una matrice 3X2 usando la [trasformazione](direct2d-transforms-overview.md) della matrice Direct2D e una delle sei modalità di interpolazione. È possibile utilizzare questo effetto per ruotare, ridimensionare, inclinare o tradurre un'immagine. In alternativa, è possibile combinare queste operazioni. I trasferimenti affini conservano linee parallele e il rapporto tra tre punti di un'immagine.

Il CLSID per questo effetto è CLSID \_ D2D12DAffineTransform.

-   [Immagine di esempio](#example-image)
-   [Proprietà effetto](#effect-properties)
-   [Modalità bordo](#border-modes)
-   [Modalità di interpolazione](#interpolation-modes)
-   [Bitmap di output](#output-bitmap)
-   [Requisiti](#requirements)
-   [Argomenti correlati](#related-topics)

## <a name="example-image"></a>Immagine di esempio



| Prima                                                             |
|--------------------------------------------------------------------|
| ![immagine prima dell'effetto.](images/default-before.jpg)         |
| After                                                              |
| ![immagine dopo la trasformazione.](images/21-2daffinetransform.png) |



 


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



Questo effetto esegue questa operazione della matrice:

![operazione di matrice affine](images/affine-matrix-calculation.png)

Sebbene la matrice di input sia definita come matrice 3x2, l'ultima colonna viene riempita con 0, 0 e 1 per produrre una matrice quadrata. Questo consente la moltiplicazione di matrici, in modo che le trasformazioni possano essere concatenate in una singola matrice.

## <a name="effect-properties"></a>Proprietà effetto



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Nome visualizzato e enumerazione dell'indice</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>InterpolationMode<br/> D2D1_2DAFFINETRANSFORM_PROP_INTERPOLATION_MODE<br/></td>
<td>Modalità di interpolazione utilizzata per ridimensionare l'immagine. Sono disponibili 6 modalità di ridimensionamento che variano in qualità e velocità.<br/> Il tipo è D2D1_2DAFFINETRANSFORM_INTERPOLATION_MODE.<br/> Il valore predefinito è D2D1_2DAFFINETRANSFORM_INTERPOLATION_MODE_LINEAR.<br/></td>
</tr>
<tr class="even">
<td>BorderMode<br/> D2D1_2DAFFINETRANSFORM_PROP_BORDER_MODE<br/></td>
<td>Modalità utilizzata per calcolare il bordo dell'immagine, soft o hard. Per altre informazioni, vedere <a href="https://www.bing.com/search?q=Border+modes">Border modes</a> . <br/> Il tipo è D2D1_BORDER_MODE.<br/> Il valore predefinito è D2D1_BORDER_MODE_SOFT.<br/></td>
</tr>
<tr class="odd">
<td>TransformMatrix<br/> D2D1_2DAFFINETRANSFORM_PROP_TRANSFORM_MATRIX<br/></td>
<td>Matrice 3x2 per trasformare l'immagine utilizzando la <a href="direct2d-transforms-overview.md">trasformazione</a>della matrice Direct2D. <br/> Il tipo è D2D1_MATRIX_3X2_F.<br/> Il valore predefinito è Matrix3x2F:: Identity ().<br/></td>
</tr>
<tr class="even">
<td>Nitidezza<br/> D2D1_2DAFFINETRANSFORM_PROP_SHARPNESS<br/></td>
<td>Nella modalità di interpolazione cubica di alta qualità, il livello di nitidezza del filtro di ridimensionamento come float compreso tra 0 e 1. I valori sono di unità. È possibile usare la nitidezza per regolare la qualità di un'immagine quando si ridimensiona l'immagine.<br/> Il fattore di nitidezza influiscono sulla forma del kernel. Maggiore è il fattore di nitidezza, minore è il kernel. <br/>
<blockquote>
[!Note]<br />
Questa proprietà ha effetto solo sulla modalità di interpolazione cubica di alta qualità.
</blockquote>
<br/> Il tipo è FLOAT.<br/> Il valore predefinito è 1.0 f.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="border-modes"></a>Modalità bordo



| Nome                     | Descrizione                                                                                                      |
|--------------------------|------------------------------------------------------------------------------------------------------------------|
| \_Modalità bordo \_ d2d1 \_ Soft | L'effetto riempie l'immagine con i pixel neri trasparenti durante l'interpolazione, ottenendo un bordo flessibile.<br/> |
| \_Modalità bordo \_ d2d1 \_ | L'effetto fissa l'output alla dimensione dell'immagine di input. <br/>                                         |



 

## <a name="interpolation-modes"></a>Modalità di interpolazione



| Enumerazione                                                         | Descrizione                                                                                                                                                                                          |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ 2DAFFINETRANSFORM- \_ modalità di interpolazione \_ \_ più vicina \_     | Campiona il punto singolo più vicino e lo utilizza. In questa modalità viene utilizzato un minor tempo di elaborazione, ma viene restituita l'immagine di qualità più bassa.                                                                           |
| D2D1 \_ 2DAFFINETRANSFORM- \_ modalità di interpolazione \_ \_ lineare                | Usa un esempio a quattro punti e un'interpolazione lineare. Questa modalità utilizza un tempo di elaborazione maggiore rispetto alla modalità adiacente più vicina, ma restituisce un'immagine di qualità superiore.                                           |
| D2D1 \_ 2DAFFINETRANSFORM- \_ modalità di interpolazione \_ \_ cubica                 | Usa un kernel cubico di esempio 16 per l'interpolazione. Questa modalità usa la maggior parte del tempo di elaborazione, ma restituisce un'immagine di qualità superiore.                                                                        |
| D2D1 \_ 2DAFFINETRANSFORM- \_ modalità di interpolazione più \_ \_ \_ lineare di esempio \_ | USA 4 campioni lineari all'interno di un singolo pixel per l'anti-aliasing dei bordi validi. Questa modalità è ideale per ridurre le dimensioni delle immagini con pochi pixel.                                              |
| D2D1 \_ 2DAFFINETRANSFORM \_ modalità di interpolazione \_ \_ anisotropico           | Usa il filtro anisotropico per campionare un modello in base alla forma trasformata della bitmap.                                                                                                     |
| D2D1 \_ 2DAFFINETRANSFORM- \_ modalità di interpolazione \_ \_ alta \_ qualità \_ cubica  | Usa un kernel cubico a dimensione variabile di alta qualità per eseguire un'downscaling dell'immagine se downscaling è associato alla matrice di trasformazione. USA quindi la modalità di interpolazione cubica per l'output finale. |



 

> [!Note]  
> Se non si seleziona una modalità, l'effetto predefinito è D2D1 \_ 2DAFFINETRANSFORM \_ modalità di interpolazione \_ \_ lineare.

 

> [!Note]  
> La modalità anisotropico genera mipmap durante il ridimensionamento. Tuttavia, se si imposta la proprietà **memorizzato nella cache** su true per gli effetti che vengono inseriti in questo effetto, il mipmap non verrà generato ogni volta per immagini sufficientemente piccole.

 

## <a name="output-bitmap"></a>Bitmap di output

Le dimensioni della bitmap di output dipendono dalla matrice di trasformazione applicata all'immagine.

L'effetto esegue l'operazione di trasformazione e quindi applica un rettangolo di delimitazione intorno al risultato. La bitmap di output corrisponde alla dimensione del rettangolo di delimitazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato | Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\] |
| Server minimo supportato | Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\] |
| Intestazione                   | d2d1effects. h                                                                      |
| Libreria                  | d2d1. lib, dxguid. lib                                                               |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

