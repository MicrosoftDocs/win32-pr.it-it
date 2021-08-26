---
title: Effetto con trasformazione prospettica 3D
description: Usare l'effetto trasformazione prospettiva 3D per ruotare l'immagine in 3 dimensioni come se fosse vista da una distanza.
ms.assetid: 0E1A940E-2DCA-4772-BB68-7E5EF5CEF833
keywords:
- Effetto trasformazione prospettiva 3d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 513d48a38e948f1255afa0cad3972a626c1e5b9039c9285c9c49b4180a5791d6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079646"
---
# <a name="3d-perspective-transform-effect"></a>Effetto con trasformazione prospettica 3D

Usare l'effetto trasformazione prospettiva 3D per ruotare l'immagine in 3 dimensioni come se fosse vista da una distanza.

La trasformazione della prospettiva 3D è più comoda dell'effetto di trasformazione 3D, ma espone solo un subset della funzionalità. È possibile calcolare una matrice di trasformazione 3D completa e applicare una matrice di trasformazione più arbitraria a un'immagine usando [l'effetto trasformazione 3D.](3d-transform.md)

Il CLSID per questo effetto è CLSID \_ D2D13DPerspectiveTransform.

-   [Immagine di esempio](#example-image)
-   [Proprietà degli effetti](#effect-properties)
-   [Modalità di interpolazione](#interpolation-modes)
-   [Modalità bordo](#border-modes)
-   [Bitmap di output](#output-bitmap)
-   [Requisiti](#requirements)
-   [Argomenti correlati](#related-topics)

## <a name="example-image"></a>Immagine di esempio



| Prima                                                               |
|----------------------------------------------------------------------|
| ![l'immagine prima dell'effetto.](images/default-before.jpg)           |
| After                                                                |
| ![l'immagine dopo l'effetto.](images/23-3dperspectivetransform.png) |



 


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



## <a name="effect-properties"></a>Proprietà degli effetti



| Nome visualizzato ed enumerazione dell'indice                                                              | Descrizione                                                                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| InterpolazioneMode<br/> MODALITÀ DI \_ \_ \_ INTERPOLAZIONE DELLA PROPRIETÀ D2D1 3DPERSPECTIVETRANSFORM \_<br/> | Modalità di interpolazione utilizzata dall'effetto sull'immagine. Esistono 5 modalità di scalabilità che variano in qualità e velocità.<br/> Il tipo è D2D1 \_ 3DPERSPECTIVETRANSFORM \_ INTERPOLATION \_ MODE.<br/> Il valore predefinito è D2D1 \_ 3DPERSPECTIVETRANSFORM \_ INTERPOLATION \_ MODE \_ LINEAR.<br/>              |
| BorderMode<br/> MODALITÀ BORDO DELLA \_ PROPRIETÀ D2D1 3DPERSPECTIVETRANSFORM \_ \_ \_<br/>               | Modalità usata per calcolare il bordo dell'immagine, soft o hard. Per [altre informazioni, vedere](https://www.bing.com/search?q=Border+modes) Modalità bordo.<br/> Il tipo è D2D1 \_ BORDER \_ MODE.<br/> Il valore predefinito è D2D1 \_ BORDER \_ MODE \_ SOFT.<br/>                                                              |
| Profondità<br/> D2D1 \_ 3DPERSPECTIVETRANSFORM \_ PROP \_ DEPTH<br/>                           | Distanza tra *PerspectiveOrigin* e il piano di proiezione. Il valore specificato in DIP e deve essere maggiore di 0.<br/> Il tipo è FLOAT.<br/> Il valore predefinito è 1000,0f.<br/>                                                                                               |
| PerspectiveOrigin<br/> D2D1 \_ 3DPERSPECTIVETRANSFORM \_ PROP \_ PERSPECTIVE \_ ORIGIN<br/> | Posizione X e Y del visualizzatore nella scena 3D. Questa proprietà è un vettore D2D1 \_ \_ 2F definito come: (punto X, punto Y). Le unità sono in DIP.<br/> Impostare il valore Z con la *proprietà Depth.*<br/> Il tipo è D2D1 \_ VECTOR \_ 2F.<br/> Il valore predefinito è {0.0f, 0.0f}.<br/> |
| LocalOffset<br/> OFFSET LOCALE DELLA \_ PROPRIETÀ D2D1 3DPERSPECTIVETRANSFORM \_ \_ \_<br/>             | Traslazione eseguita dall'effetto prima di ruotare il piano di proiezione. Questa proprietà è un vettore D2D1 \_ \_ 3F definito come: (X, Y, Z). Le unità sono in DIP.<br/> Il tipo è D2D1 \_ VECTOR \_ 3F.<br/> Il valore predefinito è {0.0f, 0.0f, 0.0f}.<br/>                                        |
| GlobalOffset<br/> OFFSET GLOBALE DELLA PROPRIETÀ \_ D2D1 3DPERSPECTIVETRANSFORM \_ \_ \_<br/>           | Traslazione eseguita dall'effetto dopo la rotazione del piano di proiezione. Questa proprietà è un vettore D2D1 \_ \_ 3F definito come: (X, Y, Z). Le unità sono in DIP.<br/> Il tipo è D2D1 \_ VECTOR \_ 3F.<br/> Il valore predefinito è {0.0f, 0.0f, 0.0f}.<br/>                                         |
| RotationOrigin<br/> D2D1 \_ 3DPERSPECTIVETRANSFORM \_ PROP \_ ROTATION \_ ORIGIN<br/>       | Punto centrale della rotazione eseguita dall'effetto. Questa proprietà è un vettore D2D1 \_ \_ 3F definito come: (X, Y, Z). Le unità sono in DIP.<br/> Il tipo è D2D1 \_ VECTOR \_ 3F.<br/> Il valore predefinito è {0.0f, 0.0f, 0.0f}.<br/>                                                            |
| Rotazione<br/> ROTAZIONE DELLE PROPRIETÀ D2D1 \_ 3DPERSPECTIVETRANSFORM \_ \_<br/>                     | Gli angoli di rotazione per ogni asse. Questa proprietà è un vettore D2D1 \_ \_ 3F definito come: (X, Y, Z). Le unità sono in gradi.<br/> Il tipo è D2D1 \_ VECTOR \_ 3F.<br/> Il valore predefinito è {0.0f, 0.0f, 0.0f}.<br/>                                                                         |



 

## <a name="interpolation-modes"></a>Modalità di interpolazione



| Enumerazione                                                              | Descrizione                                                                                                                                                |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ 3DPERSPECTIVETRANSFORM \_ INTERPOLATION \_ MODE \_ NEAREST \_ NEIGHBOR     | Campiota il singolo punto più vicino e lo usa. Questa modalità usa meno tempo di elaborazione, ma restituisce l'immagine di qualità più bassa.                                 |
| MODALITÀ DI \_ INTERPOLAZIONE D2D1 3DPERSPECTIVETRANSFORM \_ \_ \_ LINEARE                | Usa un campione di quattro punti e un'interpolazione lineare. Questa modalità usa più tempo di elaborazione rispetto alla modalità vicina più vicina, ma restituisce un'immagine di qualità superiore. |
| D2D1 \_ 3DPERSPECTIVETRANSFORM \_ INTERPOLATION \_ MODE \_ CUBIC                 | Usa un kernel cubo di 16 campioni per l'interpolazione. Questa modalità usa la maggior parte del tempo di elaborazione, ma restituisce un'immagine di qualità superiore.                              |
| D2D1 \_ 3DPERSPECTIVETRANSFORM \_ INTERPOLATION \_ MODE \_ MULTI \_ SAMPLE \_ LINEAR | Usa 4 campioni lineari all'interno di un singolo pixel per un anti-aliasing del bordo valido. Questa modalità è buona per ridurre di piccole quantità le immagini con pochi pixel.    |
| D2D1 \_ 3DPERSPECTIVETRANSFORM \_ INTERPOLATION \_ MODE \_ ANISOTROP           | Usa il filtro anisotropo per campionare un modello in base alla forma trasformata della bitmap.                                                           |



 

> [!Note]  
> Se non si seleziona una modalità, per impostazione predefinita l'effetto è D2D1 \_ 3DPERSPECTIVETRANSFORM \_ INTERPOLATION \_ MODE \_ LINEAR.

 

> [!Note]  
> La modalità anisotrop genera mipmap durante il ridimensionamento, tuttavia, se si imposta la proprietà **Cached** su true sugli effetti immessi a questo effetto, le mipmap non verranno generate ogni volta per immagini sufficientemente piccole.

 

## <a name="border-modes"></a>Modalità bordo



| Nome                     | Descrizione                                                                                                      |
|--------------------------|------------------------------------------------------------------------------------------------------------------|
| MODALITÀ BORDO D2D1 \_ \_ \_ SOFT | L'effetto riempire l'immagine con pixel neri trasparenti durante l'interpolazione, determinando un bordo soffice.<br/> |
| MODALITÀ BORDO D2D1 \_ \_ \_ HARD | L'effetto stringe l'output alle dimensioni dell'immagine di input. <br/>                                         |



 

## <a name="output-bitmap"></a>Bitmap di output

Le dimensioni della bitmap di output dipendono dalla matrice di trasformazione applicata all'immagine.

L'effetto esegue l'operazione di trasformazione e quindi applica un rettangolo di selezione intorno al risultato. La bitmap di output è la dimensione del rettangolo di selezione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato | Windows 8 e l'aggiornamento della piattaforma per Windows 7 \[ app desktop \| Windows Store\] |
| Server minimo supportato | Windows 8 e l'aggiornamento della piattaforma per Windows 7 \[ app desktop \| Windows Store\] |
| Intestazione                   | d2d1effects.h                                                                      |
| Libreria                  | d2d1.lib, dxguid.lib                                                               |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

