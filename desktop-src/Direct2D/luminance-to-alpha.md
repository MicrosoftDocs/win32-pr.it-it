---
title: Effetto Luminance to Alpha
description: Usare l'effetto luminance to alpha per impostare il canale alfa sulla luminanza dell'immagine e impostare i canali di colore su 0.
ms.assetid: B380DE5A-C097-47E0-8E0F-E3C9D2BA44B0
keywords:
- effetto luminance to alpha
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 803070fea76b47c1334803a4e7f8fef510cc77c8b3bc05c8477b572cb0451670
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117825262"
---
# <a name="luminance-to-alpha-effect"></a>Effetto Luminance to Alpha

Usare l'effetto luminance to alpha per impostare il canale alfa sulla luminanza dell'immagine e impostare i canali di colore su 0. È possibile usare l'output di questo effetto per creare una sovrapposizione semitrasparente in base alla luminosità dell'immagine di input. Oppure è possibile usarlo per creare una maschera immagine.

> [!Note]  
> Questo effetto non ha proprietà.

 

Il CLSID per questo effetto è CLSID \_ D2D1LuminanceToAlpha.

## <a name="example-image"></a>Immagine di esempio

Questo esempio mostra l'output dell'effetto luminance to alpha composito su una superficie bianca per mostrare l'opacità.



| Prima                                                            |
|-------------------------------------------------------------------|
| ![l'immagine prima dell'effetto.](images/default-before.jpg)        |
| After                                                             |
| ![l'immagine dopo la trasformazione.](images/18-luminancetoalpha.png) |



 


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

Questo effetto usa e restituisce immagini alfa premoltilied. L'effetto non funzionerà sulle immagini alfa rette a meno che non siano completamente opache.

> [!Note]
>
> Poiché le immagini vengono archiviate in un formato con compensazione gamma, prima di calcolare la luminanza per un'immagine è prima necessario eseguire la correzione gamma inversa per ottenere i valori di colore effettivi per l'immagine. Poiché le immagini vengono in genere archiviate a una gamma di 2,2, è possibile usare l'effetto di trasferimento Gamma con un esponente di (1/2.2) e quindi usare l'output di tale effetto.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato | Windows 8 e Platform Update per Windows 7 \[ app desktop \| Windows Store\] |
| Server minimo supportato | Windows 8 e Platform Update per Windows 7 \[ app desktop \| Windows Store\] |
| Intestazione                   | d2d1effects.h                                                                      |
| Libreria                  | d2d1.lib, dxguid.lib                                                               |



 

## <a name="output-bitmap"></a>Bitmap di output

L'output ha le stesse dimensioni dell'immagine di input.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

 
