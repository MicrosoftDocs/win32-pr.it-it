---
title: Luminanza all'effetto Alfa
description: Utilizzare la luminanza per l'effetto Alfa per impostare il canale alfa sulla luminanza dell'immagine e impostare i canali dei colori su 0.
ms.assetid: B380DE5A-C097-47E0-8E0F-E3C9D2BA44B0
keywords:
- luminanza all'effetto Alfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fb4c6fb78a1d49498b2adab6716d41e93d30deb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104561026"
---
# <a name="luminance-to-alpha-effect"></a>Luminanza all'effetto Alfa

Utilizzare la luminanza per l'effetto Alfa per impostare il canale alfa sulla luminanza dell'immagine e impostare i canali dei colori su 0. È possibile usare l'output di questo effetto per creare una sovrapposizione semitrasparente basata sulla luminosità dell'immagine di input. In alternativa, è possibile usarlo per creare una maschera immagine.

> [!Note]  
> Questo effetto non ha proprietà.

 

Il CLSID per questo effetto è CLSID \_ D2D1LuminanceToAlpha.

## <a name="example-image"></a>Immagine di esempio

Questo esempio mostra l'output della luminanza all'effetto Alfa composito su una superficie bianca per visualizzare l'opacità.



| Prima                                                            |
|-------------------------------------------------------------------|
| ![immagine prima dell'effetto.](images/default-before.jpg)        |
| After                                                             |
| ![immagine dopo la trasformazione.](images/18-luminancetoalpha.png) |



 


```C++
ComPtr<ID2D1Effect> luminanceToAlphaEffect;
m_d2dContext->CreateEffect(CLSID_D2D1LuminanceToAlpha, &luminanceToAlphaEffect);

luminanceToAlphaEffect->SetInput(0, bitmap);

// LuminanceToAlpha result is composited on top of a white surface to show opacity.
ComPtr<ID2D1Effect> floodEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Flood, &floodEffect);
floodEffect->SetValue(D2D1_FLOOD_PROP_COLOR, D2D1::Vector4F(1.0f, 1.0f, 1.0f, 1.0f));

ComPtr<ID2D1Effect> compositeEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Composite, &compositeEffect);

compositeEffect->SetInputEffect(0, floodEffect.Get());
compositeEffect->SetInputEffect(1, luminanceToAlphaEffect.Get());

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(compositeEffect.Get());
m_d2dContext->EndDraw();
```



Questo effetto imposta il canale alfa dell'output sulla luminanza dell'immagine di input usando questa matrice di colori.

![matrice di colori utilizzata dall'effetto per impostare il canale alfa.](images/luminance-to-alpha-math1.png)

Questo effetto utilizza e restituisce immagini alfa premoltiplicate. L'effetto non funzionerà su immagini Alpha dritte a meno che non siano completamente opache.

> [!Note]
>
> Poiché le immagini vengono archiviate in un formato con compensazione gamma, prima di calcolare la luminanza per un'immagine, è necessario prima eseguire la correzione gamma inversa per ottenere i valori di colore true per l'immagine. Poiché le immagini vengono in genere archiviate in 2,2 gamma, è possibile usare l'effetto di trasferimento gamma con un esponente di (1/2.2) e quindi usare l'output di tale effetto.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato | Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\] |
| Server minimo supportato | Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\] |
| Intestazione                   | d2d1effects. h                                                                      |
| Libreria                  | d2d1. lib, dxguid. lib                                                               |



 

## <a name="output-bitmap"></a>Bitmap di output

L'output ha le stesse dimensioni dell'immagine di input.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

 
