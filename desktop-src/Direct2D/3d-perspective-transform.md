---
title: Effetto con trasformazione prospettica 3D
description: Usare l'effetto di trasformazione prospettiva 3D per ruotare l'immagine in 3 dimensioni come se fosse visualizzata da una distanza.
ms.assetid: 0E1A940E-2DCA-4772-BB68-7E5EF5CEF833
keywords:
- effetto trasformazione prospettiva 3D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ed2b1c5131319dd711d2c7802a0bfabceaaa32e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874654"
---
# <a name="3d-perspective-transform-effect"></a>Effetto con trasformazione prospettica 3D

Usare l'effetto di trasformazione prospettiva 3D per ruotare l'immagine in 3 dimensioni come se fosse visualizzata da una distanza.

La trasformazione prospettiva 3D è più comoda rispetto all'effetto trasformazione 3D, ma espone solo un subset della funzionalità. È possibile calcolare una matrice di trasformazione 3D completa e applicare una matrice di trasformazione più arbitraria a un'immagine usando l'effetto di [trasformazione 3D](3d-transform.md) .

Il CLSID per questo effetto è CLSID \_ D2D13DPerspectiveTransform.

-   [Immagine di esempio](#example-image)
-   [Proprietà effetto](#effect-properties)
-   [Modalità di interpolazione](#interpolation-modes)
-   [Modalità bordo](#border-modes)
-   [Bitmap di output](#output-bitmap)
-   [Requisiti](#requirements)
-   [Argomenti correlati](#related-topics)

## <a name="example-image"></a>Immagine di esempio



| Prima                                                               |
|----------------------------------------------------------------------|
| ![immagine prima dell'effetto.](images/default-before.jpg)           |
| After                                                                |
| ![immagine dopo l'effetto.](images/23-3dperspectivetransform.png) |



 


```C++
ComPtr<ID2D1Effect> perspectiveTransformEffect;
m_d2dContext->CreateEffect(CLSID_D2D13DPerspectiveTransform, &perspectiveTransformEffect);

perspectiveTransformEffect->SetInput(0, bitmap);

perspectiveTransformEffect->SetValue(D2D1_3DPERSPECTIVETRANSFORM_PROP_PERSPECTIVE_ORIGIN, D2D1::Vector3F(0.0f, 192.0f, 0.0f));
perspectiveTransformEffect->SetValue(D2D1_3DPERSPECTIVETRANSFORM_PROP_ROTATION, D2D1::Vector3F(0.0f, 30.0f, 0.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(perspectiveTransformEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Proprietà effetto



| Nome visualizzato e enumerazione dell'indice                                                              | Descrizione                                                                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| InterpolationMode<br/> \_Modalità di \_ \_ interpolazione della prop 3DPERSPECTIVETRANSFORM d2d1 \_<br/> | Modalità di interpolazione utilizzata dall'effetto sull'immagine. Sono disponibili 5 modalità di ridimensionamento che variano in qualità e velocità.<br/> Il tipo è D2D1 \_ 3DPERSPECTIVETRANSFORM \_ Interpolation \_ mode.<br/> Il valore predefinito è D2D1 \_ 3DPERSPECTIVETRANSFORM \_ modalità di interpolazione \_ \_ lineare.<br/>              |
| BorderMode<br/> \_ \_ \_ Modalità bordo prop 3DPERSPECTIVETRANSFORM \_ d2d1<br/>               | Modalità utilizzata per calcolare il bordo dell'immagine, soft o hard. Per altre informazioni, vedere [Border modes](https://www.bing.com/search?q=Border+modes) .<br/> Il tipo è D2D1 \_ Border \_ mode.<br/> Il valore predefinito è D2D1 \_ Border \_ mode \_ .<br/>                                                              |
| Profondità<br/> \_Profondità della \_ prop \_ 3DPERSPECTIVETRANSFORM d2d1<br/>                           | Distanza tra il *PerspectiveOrigin* e il piano di proiezione. Il valore specificato in DIP e deve essere maggiore di 0.<br/> Il tipo è FLOAT.<br/> Il valore predefinito è 1000.0 f.<br/>                                                                                               |
| PerspectiveOrigin<br/> \_ \_ \_ Origine prospettiva d2d1 3DPERSPECTIVETRANSFORM \_ prop<br/> | Posizione X e Y del visualizzatore nella scena 3D. Questa proprietà è un D2D1 \_ vector \_ 2F definito come: (punto X, punto Y). Le unità sono in tuffi.<br/> Il valore Z viene impostato con la proprietà *Depth* .<br/> Il tipo è D2D1 \_ vector \_ 2F.<br/> Il valore predefinito è {0,0 f, 0,0 f}.<br/> |
| LocalOffset<br/> D2D1 \_ 3DPERSPECTIVETRANSFORM \_ prop \_ Local \_ offset<br/>             | Una traduzione che l'effetto esegue prima di ruotare il piano di proiezione. Questa proprietà è un \_ vettore d2d1 \_ 3F definito come: (X, Y, Z). Le unità sono in tuffi.<br/> Il tipo è D2D1 \_ vector \_ 3F.<br/> Il valore predefinito è {0,0 f, 0,0 f, 0,0 f}.<br/>                                        |
| GlobalOffset<br/> \_ \_ \_ Offset globale d2d1 3DPERSPECTIVETRANSFORM \_ prop<br/>           | Una traduzione che l'effetto esegue dopo la rotazione del piano di proiezione. Questa proprietà è un \_ vettore d2d1 \_ 3F definito come: (X, Y, Z). Le unità sono in tuffi.<br/> Il tipo è D2D1 \_ vector \_ 3F.<br/> Il valore predefinito è {0,0 f, 0,0 f, 0,0 f}.<br/>                                         |
| RotationOrigin<br/> D2D1 \_ 3DPERSPECTIVETRANSFORM \_ prop \_ Rotation \_ Origin<br/>       | Punto centrale della rotazione eseguita dall'effetto. Questa proprietà è un \_ vettore d2d1 \_ 3F definito come: (X, Y, Z). Le unità sono in tuffi.<br/> Il tipo è D2D1 \_ vector \_ 3F.<br/> Il valore predefinito è {0,0 f, 0,0 f, 0,0 f}.<br/>                                                            |
| Rotazione<br/> \_Rotazione della \_ prop \_ 3DPERSPECTIVETRANSFORM d2d1<br/>                     | Angoli di rotazione per ogni asse. Questa proprietà è un \_ vettore d2d1 \_ 3F definito come: (X, Y, Z). Le unità sono in gradi.<br/> Il tipo è D2D1 \_ vector \_ 3F.<br/> Il valore predefinito è {0,0 f, 0,0 f, 0,0 f}.<br/>                                                                         |



 

## <a name="interpolation-modes"></a>Modalità di interpolazione



| Enumerazione                                                              | Descrizione                                                                                                                                                |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ 3DPERSPECTIVETRANSFORM- \_ modalità di interpolazione \_ \_ più vicina \_     | Campiona il punto singolo più vicino e lo utilizza. In questa modalità viene utilizzato un minor tempo di elaborazione, ma viene restituita l'immagine di qualità più bassa.                                 |
| D2D1 \_ 3DPERSPECTIVETRANSFORM- \_ modalità di interpolazione \_ \_ lineare                | Usa un esempio a quattro punti e un'interpolazione lineare. Questa modalità utilizza un tempo di elaborazione maggiore rispetto alla modalità adiacente più vicina, ma restituisce un'immagine di qualità superiore. |
| D2D1 \_ 3DPERSPECTIVETRANSFORM- \_ modalità di interpolazione \_ \_ cubica                 | Usa un kernel cubico di esempio 16 per l'interpolazione. Questa modalità usa la maggior parte del tempo di elaborazione, ma restituisce un'immagine di qualità superiore.                              |
| D2D1 \_ 3DPERSPECTIVETRANSFORM- \_ modalità di interpolazione più \_ \_ \_ lineare di esempio \_ | USA 4 campioni lineari all'interno di un singolo pixel per l'anti-aliasing dei bordi validi. Questa modalità è ideale per ridurre le dimensioni delle immagini con pochi pixel.    |
| D2D1 \_ 3DPERSPECTIVETRANSFORM \_ modalità di interpolazione \_ \_ anisotropico           | Usa il filtro anisotropico per campionare un modello in base alla forma trasformata della bitmap.                                                           |



 

> [!Note]  
> Se non si seleziona una modalità, l'effetto predefinito è D2D1 \_ 3DPERSPECTIVETRANSFORM \_ modalità di interpolazione \_ \_ lineare.

 

> [!Note]  
> La modalità anisotropico genera mipmap durante il ridimensionamento. Tuttavia, se si imposta la proprietà **memorizzato nella cache** su true per gli effetti che vengono inseriti in questo effetto, il mipmap non verrà generato ogni volta per immagini sufficientemente piccole.

 

## <a name="border-modes"></a>Modalità bordo



| Nome                     | Descrizione                                                                                                      |
|--------------------------|------------------------------------------------------------------------------------------------------------------|
| \_Modalità bordo \_ d2d1 \_ Soft | L'effetto riempie l'immagine con i pixel neri trasparenti durante l'interpolazione, ottenendo un bordo flessibile.<br/> |
| \_Modalità bordo \_ d2d1 \_ | L'effetto fissa l'output alla dimensione dell'immagine di input. <br/>                                         |



 

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

 

