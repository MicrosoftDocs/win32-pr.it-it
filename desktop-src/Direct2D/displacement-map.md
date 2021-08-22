---
title: Effetto mappa di spostamento
description: Usare l'effetto mappa di spostamento per spostare i pixel dell'immagine di input in base ai valori di intensità di una seconda immagine di input.
ms.assetid: 07AA64B1-B570-428E-924F-D7DF3E4DB3F8
keywords:
- effetto mappa di spostamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73888d8168e411bf0f8daee1f2e04801353ee8358d27ba4d5cc9b1f71630a762
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119833016"
---
# <a name="displacement-map-effect"></a>Effetto mappa di spostamento

Usare l'effetto mappa di spostamento per spostare i pixel dell'immagine di input in base ai valori di intensità di una seconda immagine di input.

Il CLSID per questo effetto è CLSID \_ D2D1DisplacementMap.

-   [Immagine di esempio](#example-image)
-   [Proprietà degli effetti](#effect-properties)
-   [Canali di colore](#color-channels)
-   [Output Bitmap](#output-bitmap)
-   [Requisiti](#requirements)
-   [Argomenti correlati](#related-topics)

## <a name="example-image"></a>Immagine di esempio



| Prima                                                           |
|------------------------------------------------------------------|
| ![l'immagine prima dell'effetto.](images/default-before.jpg)       |
| After                                                            |
| ![l'immagine dopo la trasformazione.](images/19-displacementmap.png) |



 


```C++
ComPtr<ID2D1Effect> displacementMapEffect;
m_d2dContext->CreateEffect(CLSID_D2D1DisplacementMap, &displacementMapEffect);

displacementMapEffect->SetInput(0, bitmap);
displacementMapEffect->SetValue(D2D1_DISPLACEMENTMAP_PROP_SCALE, 100.0f);

// The second input of the displacement effect determines how the input image is transformed.
// For this example, we will use a turbulence effect as the second input to randomly distort the image.
ComPtr<ID2D1Effect> turbulenceEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Turbulence, &turbulenceEffect);
displacementMapEffect->SetInputEffect(1, turbulenceEffect.Get());

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(displacementMapEffect.Get());
m_d2dContext->EndDraw();
```



Le posizioni dei pixel nell'output vengono determinate usando questa formula:

C' (x,y)=C(x+ scale \* (XChannelSelector(Shift Bitmap (x,y))-0.5),y+ scale \* (YChannelSelector(Shift Bitmap (x,y))-0.5))

Dove:<dl> *C (x, y) è* il pixel di output in (x, y).  
*C (x, y) è* il pixel di input in (x, y).  
*Bitmap di spostamento (x, y) è* l'intensità in pixel di spostamento in corrispondenza delle coordinate specificate  
*XChannelSelector* l'intensità del canale RGBA selezionato dalla bitmap di spostamento che sposta l'immagine di input nella direzione X.  
*YChannelSelector* l'intensità del canale RGBA selezionato dalla bitmap di spostamento che sposta l'immagine di input nella direzione Y.  
</dl>

L'effetto ricampiona l'immagine di input in base alla proprietà scale e all'intensità dell'immagine di spostamento. Usa l'interpolazione bilineare se il campionamento viene tra pixel nell'immagine di input.

Questo effetto funziona su immagini alfa rette e premoltiliate. Il formato alfa di output è lo stesso del formato di input.

## <a name="effect-properties"></a>Proprietà degli effetti



| Enumerazione del nome visualizzato e dell'indice                                                   | Tipo e valore predefinito                                                   | Descrizione                                                                                                                                                                               |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Scalabilità<br/> \_D2D1SQUADAMENTO DELLA \_ PROPRIETÀ DELLA MAPPA \_<br/>                       | FLOAT<br/> 0,0f<br/>                                         | Moltiplica l'intensità del canale selezionato dall'immagine di spostamento. Più alta è l'impostazione di questa proprietà, maggiore sarà l'effetto che intasa i pixel<br/>                       |
| XChannelSelect<br/> D2D1 \_ PROPRIETÀ MAPPA DI SPOSTAMENTO X CHANNEL \_ \_ \_ \_ SELECT<br/> | SELETTORE CANALE D2D1 \_ \_<br/> SELETTORE DI CANALE D2D1 \_ \_ \_ A<br/> | L'effetto estrae l'intensità da questo canale di colore e la usa per spostare l'immagine a livello spaziale nella direzione X. Per [altre informazioni, vedi](#color-channels) Canali di colore.<br/> |
| YChannelSelect<br/> D2D1 \_ MAP \_ PROP Y CHANNEL \_ \_ \_ SELECT<br/> | SELETTORE CANALE D2D1 \_ \_<br/> SELETTORE DI CANALE D2D1 \_ \_ \_ A<br/> | L'effetto estrae l'intensità da questo canale di colore e la usa per spostare l'immagine a livello spaziale nella direzione Y. Per [altre informazioni, vedi](#color-channels) Canali di colore.<br/> |



 

## <a name="color-channels"></a>Canali di colore



| Enumerazione                | Descrizione                                                      |
|----------------------------|------------------------------------------------------------------|
| SELETTORE DI CANALE D2D1 \_ \_ \_ R | L'effetto estrae l'output di intensità dal canale rosso.   |
| SELETTORE CANALE D2D1 \_ \_ \_ G | L'effetto estrae l'output di intensità dal canale verde. |
| SELETTORE DI CANALE D2D1 \_ \_ \_ B | L'effetto estrae l'output di intensità dal canale blu.  |
| SELETTORE DI CANALE D2D1 \_ \_ \_ A | L'effetto estrae l'output di intensità dal canale alfa. |



 

## <a name="output-bitmap"></a>Output Bitmap

È possibile determinare le dimensioni massime della bitmap di output con queste equazioni:

Bitmap di output? Pixels=(Input Bitmap Size?( DIP)+Scale) \* (User DPI/96)

Output Bitmap<sub>y</sub> Pixels=(Input Bitmap Size<sub>y</sub>(DIP) + Scale) \* (User DPI/96)

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

 

