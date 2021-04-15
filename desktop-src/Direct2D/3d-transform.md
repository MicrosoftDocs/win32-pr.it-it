---
title: Effetto con trasformazione 3D
description: Usare l'effetto di trasformazione 3D per applicare una matrice di trasformazione 4x4 arbitraria a un'immagine.
ms.assetid: BC2F2837-40F0-4293-A190-8B5F81BB01B6
keywords:
- effetto trasformazione 3D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fabe0c2c220038802b5218b54187a1ff89268bfa
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/28/2021
ms.locfileid: "104570074"
---
# <a name="3d-transform-effect"></a>Effetto con trasformazione 3D

Usare l'effetto di trasformazione 3D per applicare una matrice di trasformazione 4x4 arbitraria a un'immagine.

Questo effetto applica la matrice (M?) fornita ai vertici degli angoli dell'immagine di origine ( \[ x y z 1 \] ) utilizzando il calcolo seguente:

\[x<sub>r</sub> y<sub>r</sub> z<sub>r</sub> 1 \] = \[ x y z 1 \] \* M?

Il CLSID per questo effetto è CLSID \_ D2D13DTransform.

-   [Immagine di esempio](#example-image)
-   [Proprietà effetto](#effect-properties)
    -   [Modalità di interpolazione](#interpolation-modes)
    -   [Modalità bordo](#border-modes)
-   [Classe della matrice di trasformazione 4x4](#4x4-transform-matrix-class)
-   [Requisiti](#requirements)
-   [Argomenti correlati](#related-topics)

## <a name="example-image"></a>Immagine di esempio



| Prima                                                        |
|---------------------------------------------------------------|
| ![immagine prima della trasformazione.](images/default-before.jpg) |
| After                                                         |
| ![immagine dopo la trasformazione.](images/24-3dtransform.png)  |



 


```C++
ComPtr<ID2D1Effect> D2D13DTransformEffect;
m_d2dContext->CreateEffect(CLSID_D2D13DTransform, &D2D13DTransformEffect);

D2D13DTransformEffect->SetInput(0, bitmap);

// You can use the helper methods in D2D1::Matrix4x4F to create common matrix transformations.
D2D1_MATRIX_4X4_F matrix = 
    D2D1::Matrix4x4F::Translation(0.0f, -192.0f, 0.0f) *
    D2D1::Matrix4x4F::RotationY(30.0f) *
    D2D1::Matrix4x4F::Translation(0.0f, 192.0f, 0.0f);

D2D13DTransformEffect->SetValue(D2D1_3DTRANSFORM_PROP_TRANSFORM_MATRIX, matrix);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(D2D13DTransformEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Proprietà effetto



<table>
<thead>
<tr class="header">
<th>Nome visualizzato e enumerazione dell'indice</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>InterpolationMode<br/> D2D1_3DTRANSFORM_PROP_INTERPOLATION_MODE<br/></td>
<td>Modalità di interpolazione utilizzata dall'effetto sull'immagine. Sono disponibili 5 modalità di ridimensionamento che variano in qualità e velocità.<br/> Il tipo è D2D1_3DTRANSFORM_INTERPOLATION_MODE.<br/> Il valore predefinito è D2D1_3DTRANSFORM_INTERPOLATION_MODE_LINEAR.<br/></td>
</tr>
<tr class="even">
<td>BorderMode<br/> D2D1_3DTRANSFORM_PROP_BORDER_MODE<br/></td>
<td>Modalità utilizzata per calcolare il bordo dell'immagine, soft o hard. Per altre informazioni, vedere <a href="https://www.bing.com/search?q=Border+modes">Border modes</a> .<br/> Il tipo è D2D1_BORDER_MODE.<br/> Il valore predefinito è D2D1_BORDER_MODE_SOFT.<br/></td>
</tr>
<tr class="odd">
<td>TransformMatrix<br/> D2D1_3DTRANSFORM_PROP_TRANSFORM_MATRIX<br/></td>
<td>Matrice di trasformazione 4x4 applicata al piano di proiezione. Il calcolo matrice seguente viene usato per eseguire il mapping di punti da un sistema di coordinate 3D al sistema di coordinate 2D trasformato. <br/><img src="images/3d-transform-matrix1.png" alt="3D Depth Matrix" />Dove:<dl> X, Y, Z = coordinate del piano di proiezione di input<br />
M<sub>x, y</sub> = elementi della matrice di trasformazione<br />
X, Y, Z = coordinate del piano di proiezione di output<br />
</dl> <br/> I singoli elementi della matrice non sono limitati e sono senza unità. <br/> Il tipo è D2D1_MATRIX_4X4_F.<br/> Il valore predefinito è Matrix4x4F (1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1).<br/></td>
</tr>
</tbody>
</table>



 

### <a name="interpolation-modes"></a>Modalità di interpolazione



| Enumerazione                                                   | Descrizione                                                                                                                                                |
|---------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ 3DTRANSFORM- \_ modalità di interpolazione \_ \_ più vicina \_     | Campiona il punto singolo più vicino e lo utilizza. In questa modalità viene utilizzato un minor tempo di elaborazione, ma viene restituita l'immagine di qualità più bassa.                                 |
| D2D1 \_ 3DTRANSFORM- \_ modalità di interpolazione \_ \_ lineare                | Usa un esempio a quattro punti e un'interpolazione lineare. Questa modalità utilizza un tempo di elaborazione maggiore rispetto alla modalità adiacente più vicina, ma restituisce un'immagine di qualità superiore. |
| D2D1 \_ 3DTRANSFORM- \_ modalità di interpolazione \_ \_ cubica                 | Usa un kernel cubico di esempio 16 per l'interpolazione. Questa modalità usa la maggior parte del tempo di elaborazione, ma restituisce un'immagine di qualità superiore.                              |
| D2D1 \_ 3DTRANSFORM- \_ modalità di interpolazione più \_ \_ \_ lineare di esempio \_ | USA 4 campioni lineari all'interno di un singolo pixel per l'anti-aliasing dei bordi validi. Questa modalità è ideale per ridurre le dimensioni delle immagini con pochi pixel.    |
| D2D1 \_ 3DTRANSFORM \_ modalità di interpolazione \_ \_ anisotropico           | Usa il filtro anisotropico per campionare un modello in base alla forma trasformata della bitmap.                                                           |



 

> [!Note]  
> Se non si seleziona una modalità, l'effetto predefinito è D2D1 \_ 3DTRANSFORM \_ modalità di interpolazione \_ \_ lineare.

 

> [!Note]  
> La modalità anisotropico genera mipmap durante il ridimensionamento. Tuttavia, se si imposta la proprietà **memorizzato nella cache** su true per gli effetti che vengono inseriti in questo effetto, il mipmap non verrà generato ogni volta per immagini sufficientemente piccole.

 

### <a name="border-modes"></a>Modalità bordo



| Nome                     | Descrizione                                                                                                      |
|--------------------------|------------------------------------------------------------------------------------------------------------------|
| \_Modalità bordo \_ d2d1 \_ Soft | L'effetto riempie l'immagine con i pixel neri trasparenti durante l'interpolazione, ottenendo un bordo flessibile.<br/> |
| \_Modalità bordo \_ d2d1 \_ | L'effetto fissa l'output alla dimensione dell'immagine di input. <br/>                                         |



 

## <a name="4x4-transform-matrix-class"></a>Classe della matrice di trasformazione 4x4

Direct2D fornisce una classe della matrice 4x4 per fornire funzioni helper per trasformare l'immagine in 3 dimensioni. Vedere l'argomento [**Matrix4x4F**](/windows/desktop/api/d2d1_1helper/nl-d2d1_1helper-matrix4x4f) per altre informazioni e una descrizione di tutti i membri della classe.



| Funzione                                | Descrizione                                                                                    | Matrice                                                 |
|-----------------------------------------|------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| Matrix4x4F:: scale (X, Y, Z)              | Genera una matrice di trasformazione che ridimensiona il piano di proiezione nella direzione X, Y e/o Z. | ![matrice scale3d](images/3d-transform-matrix2.png)     |
| SkewX (X)                                | Genera una matrice di trasformazione che inclina il piano di proiezione nella direzione X.               | ![Mostra una matrice di inclinazione nella direzione X.](images/matrix4x4-skewx.png)             |
| Asimmetria (Y)                                | Genera una matrice di trasformazione che inclina il piano di proiezione nella direzione Y.               | ![matrice di inclinazione](images/matrix4x4-skewy.png)             |
| Traduzione (X, Y, Z)                    | Genera una matrice di trasformazione che converte il piano di proiezione nella direzione X, Y o Z. | ![Trasla matrice](images/3d-transform-matrix4.png)   |
| RotationX (X)                            | Genera una matrice di trasformazione che ruota il piano di proiezione sull'asse X.               | ![ruota x matrice](images/3d-transform-matrix5.png)    |
| Rotazione (Y)                            | Genera una matrice di trasformazione che ruota il piano di proiezione sull'asse Y.               | ![ruota y matrice](images/3d-transform-matrix6.png)    |
| RotationZ (Z)                            | Genera una matrice di trasformazione che ruota il piano di proiezione sull'asse Z.               | ![ruota matrice z](images/3d-transform-matrix7.png)    |
| PerspectiveProjection (D)                | Trasformazione prospettiva con un valore di profondità pari a D.                                          | ![matrice prospettiva](images/3d-transform-matrix8.png) |
| RotationArbitraryAxis (X, Y, Z, gradi) | Ruota il piano di proiezione sull'asse specificato.                                       |                                                        |



 

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

 

