---
title: Effetto Rotazione tonalità
description: Usare l'effetto di rotazione tonalità per modificare la tonalità di un'immagine applicando una matrice di colori basata sull'angolo di rotazione.
ms.assetid: D322DB2C-2B8B-4101-BFB2-97E49CAC7BF6
keywords:
- effetto Rotazione tonalità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 525dbe8fc94377080fbae34b80252c84c05073ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104562147"
---
# <a name="hue-rotatation-effect"></a>Effetto Rotazione tonalità

Usare l'effetto di rotazione tonalità per modificare la tonalità di un'immagine applicando una matrice di colori basata sull'angolo di rotazione.

Il CLSID per questo effetto è CLSID \_ D2D1HueRotation.

-   [Immagine di esempio](#example-image)
-   [Proprietà effetto](#effect-properties)
-   [Bitmap di output](#output-bitmap)
-   [Requisiti](#requirements)
-   [Argomenti correlati](#related-topics)

## <a name="example-image"></a>Immagine di esempio

Nell'esempio riportato di seguito vengono illustrate le immagini di input e di output dell'effetto Rotazione tonalità con un angolo di rotazione di 270 gradi.



| Prima                                                       |
|--------------------------------------------------------------|
| ![immagine prima dell'effetto.](images/default-before.jpg)   |
| After                                                        |
| ![immagine dopo la trasformazione.](images/17-huerotation.png) |



 


```C++
ComPtr<ID2D1Effect> hueRotationEffect;
m_d2dContext->CreateEffect(CLSID_D2D1HueRotation, &hueRotationEffect);

hueRotationEffect->SetInput(0, bitmap);
hueRotationEffect->SetValue(D2D1_HUEROTATION_PROP_ANGLE, 270.0f);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(hueRotationEffect.Get());
m_d2dContext->EndDraw();
```



L'effetto calcola una matrice di colori basata sull'angolo di rotazione (*?*) specificato con la proprietà d2d1 \_ HUEROTATION \_ prop \_ Angle. Ecco le equazioni della matrice.

![calcoli di rotazione tonalità](images/hue-formula.png)

La matrice creata dipende solo dall'angolo di rotazione. Se è necessaria una matrice specifica, è possibile usare l'effetto della [matrice di colori](color-matrix.md) .

## <a name="effect-properties"></a>Proprietà effetto



| Nome visualizzato e enumerazione dell'indice                         | Tipo e valore predefinito           | Descrizione                              |
|------------------------------------------------------------|----------------------------------|------------------------------------------|
| Angle<br/> \_Angolo della \_ prop \_ HUEROTATION d2d1<br/> | FLOAT<br/> 0,0 f<br/> | Angolo per ruotare la tonalità, in gradi. |



 

## <a name="output-bitmap"></a>Bitmap di output

La dimensione bitmap di output corrisponde alla dimensione bitmap di input.

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

 

