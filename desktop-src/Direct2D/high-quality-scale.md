---
title: Effetto di scalabilità
description: Utilizzare questo effetto per ridimensionare un'immagine verso l'alto o verso il basso. L'effetto è costituito da sei modalità di ridimensionamento adiacenti, lineari, cubici, multicampionamento lineare, anisotropico e cubi di alta qualità.
ms.assetid: 99DFA8DB-384B-4F64-90A2-0D3D7E1ACF27
keywords:
- effetto scala
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad3af77bc24db387fff0854e0432c270fa2ce6d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400542"
---
# <a name="scale-effect"></a>Effetto di scalabilità

Utilizzare questo effetto per ridimensionare un'immagine verso l'alto o verso il basso. L'effetto è costituito da sei modalità di ridimensionamento: adiacente più vicino, lineare, cubico, lineare a più campioni, anisotropico e cubi di alta qualità.

Il CLSID per questo effetto è CLSID \_ D2D1Scale.

-   [Immagine di esempio](#example-image)
-   [Proprietà effetto](#effect-properties)
    -   [Modalità bordo](#border-modes)
-   [Modalità di interpolazione](#interpolation-modes)
-   [Bitmap di output](#output-bitmap)
-   [Requisiti](#requirements)
-   [Argomenti correlati](#related-topics)

## <a name="example-image"></a>Immagine di esempio

Questo esempio mostra lo zoom dell'effetto di scala in 2 volte l'input e il ritaglio alle dimensioni originali.



| Prima                                                     |
|------------------------------------------------------------|
| ![immagine prima dell'effetto.](images/default-before.jpg) |
| After                                                      |
| ![immagine dopo la trasformazione.](images/22-scale.png)     |



 


```C++
ComPtr<ID2D1Effect> scaleEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Scale, &scaleEffect);

scaleEffect->SetInput(0, bitmap);

scaleEffect->SetValue(D2D1_SCALE_PROP_CENTER_POINT, D2D1::Vector2F(256.0f, 192.0f));
scaleEffect->SetValue(D2D1_SCALE_PROP_SCALE, D2D1::Vector2F(2.0f, 2.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(scaleEffect.Get());
m_d2dContext->EndDraw();
```



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
<td>Scalabilità<br/> D2D1_SCALE_PROP_SCALE<br/></td>
<td>Quantità di scala nella direzione X e Y come rapporto tra le dimensioni di output e le dimensioni di input. Questa proprietà a D2D1_VECTOR_2Fdefined come: (scala X, scala Y). Gli importi di scala sono FLOAT, unità e devono essere positivi o 0.<br/> Il tipo è D2D1_VECTOR_2F.<br/> Il valore predefinito è {1.0 f, 1.0 f}.<br/></td>
</tr>
<tr class="even">
<td>CenterPoint<br/> D2D1_SCALE_PROP_CENTER_POINT<br/></td>
<td>Punto centrale di ridimensionamento dell'immagine. Questa proprietà è un D2D1_VECTOR_2F definito come: (punto X, punto Y). Le unità sono in tuffi.<br/> Usare la proprietà punto centrale per ridimensionare un punto diverso dall'angolo superiore sinistro.<br/> Il tipo è D2D1_VECTOR_2F.<br/> Il valore predefinito è {0,0 f, 0,0 f}.<br/></td>
</tr>
<tr class="odd">
<td>BorderMode<br/> D2D1_SCALE_PROP_BORDER_MODE<br/></td>
<td>Modalità utilizzata per calcolare il bordo dell'immagine, soft o hard. Per altre informazioni, vedere <a href="#border-modes">Border modes</a> . <br/> Il tipo è D2D1_BORDER_MODE.<br/> Il valore predefinito è D2D1_BORDER_MODE_SOFT.<br/></td>
</tr>
<tr class="even">
<td>Nitidezza<br/> D2D1_SCALE_PROP_SHARPNESS<br/></td>
<td>Nella modalità di interpolazione cubica di alta qualità, il livello di nitidezza del filtro di ridimensionamento come float compreso tra 0 e 1. I valori sono di unità. È possibile usare la nitidezza per regolare la qualità di un'immagine quando si ridimensiona l'immagine verso il basso.<br/> Il fattore di nitidezza influiscono sulla forma del kernel. Maggiore è il fattore di nitidezza, minore è il kernel.<br/>
<blockquote>
[!Note]<br />
Questa proprietà ha effetto solo sulla modalità di interpolazione cubica di alta qualità.
</blockquote>
<br/> Il tipo è FLOAT.<br/> Il valore predefinito è 0,0 f.<br/></td>
</tr>
<tr class="odd">
<td>InterpolationMode<br/> D2D1_SCALE_PROP_INTERPOLATION_MODE<br/></td>
<td>Modalità di interpolazione utilizzata dall'effetto per ridimensionare l'immagine. Sono disponibili 6 modalità di ridimensionamento che variano in qualità e velocità. Per altre informazioni, vedere <a href="#interpolation-modes">modalità di interpolazione</a> . <br/> Il tipo è D2D1_SCALE_INTERPOLATION_MODE.<br/> Il valore predefinito è D2D1_SCALE_INTERPOLATION_MODE_LINEAR.<br/></td>
</tr>
</tbody>
</table>



 

### <a name="border-modes"></a>Modalità bordo



| Nome                     | Descrizione                                                                                                                                                                                                                                                              |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Modalità bordo \_ d2d1 \_ Soft | L'effetto riempie l'immagine di input con i pixel neri trasparenti per i campioni all'esterno dei limiti di input quando applica il kernel di convoluzione. Viene creato un bordo flessibile per l'immagine e il processo espande la bitmap di output in base alla dimensione del kernel.<br/> |
| \_Modalità bordo \_ d2d1 \_ | L'effetto estende l'immagine di input con una trasformazione del bordo di tipo mirror per i campioni all'esterno dei limiti di input. La dimensione della bitmap di output è uguale alla dimensione della bitmap di input.<br/>                                                                       |



 

\`

## <a name="interpolation-modes"></a>Modalità di interpolazione



| Enumerazione                                             | Descrizione                                                                                                                                                                                          |
|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Modalità di \_ interpolazione scala d2d1 \_ \_ più \_ vicina     | Campiona il punto singolo più vicino e lo utilizza. In questa modalità viene utilizzato un minor tempo di elaborazione, ma viene restituita l'immagine di qualità più bassa.                                                                           |
| \_Modalità di \_ interpolazione scala d2d1 \_ \_ lineare                | Usa un esempio a quattro punti e un'interpolazione lineare. Questa modalità utilizza un tempo di elaborazione maggiore rispetto alla modalità adiacente più vicina, ma restituisce un'immagine di qualità superiore.                                           |
| \_Modalità di \_ interpolazione scala d2d1 \_ \_ cubica                 | Usa un kernel cubico di esempio 16 per l'interpolazione. Questa modalità usa la maggior parte del tempo di elaborazione, ma restituisce un'immagine di qualità superiore.                                                                        |
| \_Modalità di \_ interpolazione con SCALAbilità d2d1 \_ \_ \_ multicampione \_ lineare | USA 4 campioni lineari all'interno di un singolo pixel per l'anti-aliasing dei bordi validi. Questa modalità è ideale per ridurre le dimensioni delle immagini con pochi pixel.                                              |
| \_Modalità di \_ interpolazione con SCALAbilità d2d1 \_ \_           | Usa il filtro anisotropico per campionare un modello in base alla forma trasformata della bitmap.                                                                                                     |
| D2D1 \_ di \_ \_ \_ alta \_ qualità in modalità interpolazione \_  | Usa un kernel cubico a dimensione variabile di alta qualità per eseguire un'downscaling dell'immagine se downscaling è associato alla matrice di trasformazione. USA quindi la modalità di interpolazione cubica per l'output finale. |



 

> [!Note]  
> Se non si seleziona una modalità, l'effetto viene impostato sul valore predefinito D2D1 \_ \_ modalità di interpolazione \_ \_ lineare.

 

> [!Note]  
> La modalità anisotropico genera mipmap durante il ridimensionamento. Tuttavia, se si imposta la proprietà **memorizzato nella cache** su true per gli effetti che vengono inseriti in questo effetto, il mipmap non verrà generato ogni volta per immagini sufficientemente piccole.

 

## <a name="output-bitmap"></a>Bitmap di output

La posizione e le dimensioni della bitmap di output dipendono dal fattore di scala e dal punto centrale specificati.

È possibile calcolare le dimensioni della bitmap di output usando questa equazione:<dl> BitmapSize? (Pixel) = scala? \* Dimensioni originali della bitmap? (DIP) \* (UserDPI/96)  
BitmapSize<sub>y</sub>(pixel) = scala<sub>y</sub> \* dimensioni bitmap originali<sub>y</sub> (DIP) \* (UserDPI/96)  
</dl>

L'effetto Arrotonda le frazioni di pixel fino al pixel intero più vicino.

Il percorso della bitmap è (0, 0) o il valore della proprietà del punto centrale.

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

 

