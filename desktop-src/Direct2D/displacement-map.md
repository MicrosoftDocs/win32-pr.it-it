---
title: Effetto Mappa di spostamento
description: Utilizzare l'effetto Mappa di spostamento per posizionare i pixel dell'immagine di input in base ai valori di intensità di una seconda immagine di input.
ms.assetid: 07AA64B1-B570-428E-924F-D7DF3E4DB3F8
keywords:
- effetto Mappa di spostamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd0ad2deb0c584ccc9c55faebd60f803d66efa42
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119058"
---
# <a name="displacement-map-effect"></a>Effetto Mappa di spostamento

Utilizzare l'effetto Mappa di spostamento per posizionare i pixel dell'immagine di input in base ai valori di intensità di una seconda immagine di input.

Il CLSID per questo effetto è CLSID \_ D2D1DisplacementMap.

-   [Immagine di esempio](#example-image)
-   [Proprietà effetto](#effect-properties)
-   [Canali colori](#color-channels)
-   [Bitmap di output](#output-bitmap)
-   [Requisiti](#requirements)
-   [Argomenti correlati](#related-topics)

## <a name="example-image"></a>Immagine di esempio



| Prima                                                           |
|------------------------------------------------------------------|
| ![immagine prima dell'effetto.](images/default-before.jpg)       |
| After                                                            |
| ![immagine dopo la trasformazione.](images/19-displacementmap.png) |



 


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



I percorsi dei pixel nell'output vengono determinati utilizzando la formula seguente:

C'(x, y) = C (x + scale \* (XChannelSelector (bitmap di spostamento (x, y))-0,5), y + scale \* (YChannelSelector (bitmap di spostamento (x, y))-0,5))

Dove:<dl> *C (x, y)* è il pixel di output in corrispondenza di (x, y).  
*C (x, y)* è il pixel di input in corrispondenza di (x, y).  
La *bitmap di spostamento (x, y)* è l'intensità del pixel di spostamento in corrispondenza delle coordinate specificate.  
*XChannelSelector* l'intensità del canale RGBA selezionato dalla bitmap di spostamento che sposta l'immagine di input nella direzione X.  
*YChannelSelector* l'intensità del canale RGBA selezionato dalla bitmap di spostamento che sposta l'immagine di input nella direzione Y.  
</dl>

L'effetto Ricampiona l'immagine di input in base alla proprietà scale e all'intensità dell'immagine di spostamento. Usa l'interpolazione bilineare se il campionamento è compreso tra i pixel nell'immagine di input.

Questo effetto funziona su immagini alfa diritte e premoltiplicate. Il formato alfa di output corrisponde al formato di input.

## <a name="effect-properties"></a>Proprietà effetto



| Nome visualizzato e enumerazione dell'indice                                                   | Tipo e valore predefinito                                                   | Descrizione                                                                                                                                                                               |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Scalabilità<br/> D2D1 \_ DISPLACEMENTMAP \_ prop \_ scale<br/>                       | FLOAT<br/> 0,0 f<br/>                                         | Moltiplica l'intensità del canale selezionato dall'immagine di spostamento. Maggiore è l'impostazione di questa proprietà, maggiore sarà l'effetto di spostamento dei pixel<br/>                       |
| XChannelSelect<br/> \_Selezione del canale d2d1 DISPLACEMENTMAP \_ prop \_ X \_ \_<br/> | \_Selettore di canale d2d1 \_<br/> \_ \_ Selettore \_ di canale A d2d1<br/> | L'effetto estrae l'intensità da questo canale di colore e la usa per posizionare l'immagine nella direzione X. Per altre informazioni, vedere [canali dei colori](#color-channels) .<br/> |
| YChannelSelect<br/> \_Select d2d1 DISPLACEMENTMAP \_ prop \_ Y \_ Channel \_<br/> | \_Selettore di canale d2d1 \_<br/> \_ \_ Selettore \_ di canale A d2d1<br/> | L'effetto estrae l'intensità da questo canale di colore e la usa per posizionare l'immagine nella direzione Y. Per altre informazioni, vedere [canali dei colori](#color-channels) .<br/> |



 

## <a name="color-channels"></a>Canali colori



| Enumerazione                | Descrizione                                                      |
|----------------------------|------------------------------------------------------------------|
| \_ \_ R selettore canale d2d1 \_ | L'effetto estrae l'output dell'intensità dal canale rosso.   |
| \_Selettore di canale d2d1 \_ \_ G | L'effetto estrae l'output dell'intensità dal canale verde. |
| \_Selettore di canale d2d1 \_ \_ B | L'effetto estrae l'output dell'intensità dal canale blu.  |
| \_ \_ Selettore \_ di canale A d2d1 | L'effetto estrae l'output dell'intensità dal canale alfa. |



 

## <a name="output-bitmap"></a>Bitmap di output

È possibile determinare le dimensioni massime della bitmap di output con le equazioni seguenti:

Bitmap di output? Pixel = (dimensioni bitmap di input? ( DIP) + scala) \* (dpi utente/96)

Bitmap di output<sub>y</sub> pixel = (input bitmap size<sub>y</sub>(DIP) + scale) \* (dpi utente/96)

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

 

