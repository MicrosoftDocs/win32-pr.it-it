---
title: Effetto di rotazione della tonalità
description: Usare l'effetto di rotazione della tonalità per modificare la tonalità di un'immagine applicando una matrice di colori in base all'angolo di rotazione.
ms.assetid: D322DB2C-2B8B-4101-BFB2-97E49CAC7BF6
keywords:
- Effetto di rotazione della tonalità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 531ab9b1649db96bc5ee100df98ed10b4021b506e3ad71bb426778655348b2df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119569132"
---
# <a name="hue-rotatation-effect"></a>Effetto di rotazione della tonalità

Usare l'effetto di rotazione della tonalità per modificare la tonalità di un'immagine applicando una matrice di colori in base all'angolo di rotazione.

Il CLSID per questo effetto è CLSID \_ D2D1HueRotation.

-   [Immagine di esempio](#example-image)
-   [Proprietà degli effetti](#effect-properties)
-   [Bitmap di output](#output-bitmap)
-   [Requisiti](#requirements)
-   [Argomenti correlati](#related-topics)

## <a name="example-image"></a>Immagine di esempio

L'esempio seguente mostra le immagini di input e output dell'effetto di rotazione della tonalità con un angolo di rotazione di 270 gradi.



| Prima                                                       |
|--------------------------------------------------------------|
| ![l'immagine prima dell'effetto.](images/default-before.jpg)   |
| After                                                        |
| ![l'immagine dopo la trasformazione.](images/17-huerotation.png) |



 


```C++
ComPtr<ID2D1Effect> hueRotationEffect;
m_d2dContext->CreateEffect(CLSID_D2D1HueRotation, &hueRotationEffect);

hueRotationEffect->SetInput(0, bitmap);
hueRotationEffect->SetValue(D2D1_HUEROTATION_PROP_ANGLE, 270.0f);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(hueRotationEffect.Get());
m_d2dContext->EndDraw();
```



L'effetto calcola una matrice di colori in base all'angolo di rotazione (*?*) specificato con la proprietà D2D1 \_ HUEROTATION \_ PROP \_ ANGLE. Ecco le equazioni della matrice.

![Calcoli della rotazione della tonalità](images/hue-formula.png)

La matrice creata dipende solo dall'angolo di rotazione. Se è necessaria [una matrice specifica,](color-matrix.md) è possibile usare l'effetto matrice di colori.

## <a name="effect-properties"></a>Proprietà degli effetti



| Enumerazione del nome visualizzato e dell'indice                         | Tipo e valore predefinito           | Descrizione                              |
|------------------------------------------------------------|----------------------------------|------------------------------------------|
| Angle<br/> D2D1 \_ HUEROTATION \_ PROP \_ ANGLE<br/> | FLOAT<br/> 0,0f<br/> | Angolo in gradi per ruotare la tonalità. |



 

## <a name="output-bitmap"></a>Bitmap di output

Le dimensioni della bitmap di output sono le stesse della bitmap di input.

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

 

