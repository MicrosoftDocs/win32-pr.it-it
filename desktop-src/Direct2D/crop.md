---
title: Effetto Ritaglia
description: Usare l'effetto di ritaglio per ottenere un'area specificata di un'immagine.
ms.assetid: DFB7DE20-F202-4E7F-AE63-94BF817B6E30
keywords:
- effetto di ritaglio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e342bdef882fbff89d4c67c3accfbff7287a2ad9
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472932"
---
# <a name="crop-effect"></a>Effetto Ritaglia

Usare l'effetto di ritaglio per ottenere un'area specificata di un'immagine.

Il CLSID per questo effetto è CLSID \_ D2D1Crop.

-   [Immagine di esempio](#example-image)
-   [Proprietà degli effetti](#effect-properties)
-   [Bitmap di output](#output-bitmap)
-   [Requisiti](#requirements)
-   [Argomenti correlati](#related-topics)

## <a name="example-image"></a>Immagine di esempio



| Prima                                                     |
|------------------------------------------------------------|
| ![l'immagine prima dell'effetto.](images/default-before.jpg) |
| After                                                      |
| ![l'immagine dopo la trasformazione.](images/8-crop.png)       |



 


```C++
ComPtr<ID2D1Effect> cropEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Crop, &cropEffect);

cropEffect->SetInput(0, bitmap);
cropEffect->SetValue(D2D1_CROP_PROP_RECT, D2D1::RectF(0.0f, 0.0f, 256.0f, 192.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(cropEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Proprietà degli effetti




| Nome visualizzato ed enumerazione dell'indice | Tipo e valore predefinito | Descrizione | 
|------------------------------------|------------------------|-------------|
| Rect<br /> | D2D1_VECTOR_4F<br /> | Area da ritagliare specificata come vettore nel formato (sinistra, superiore, larghezza, altezza).<br /> | 
| D2D1_CROP_PROP_RECT<br /> | {-FLT_MAX, -FLT_MAX, FLT_MAX, FLT_MAX}<br /> | Le unità sono in DIP. <br /><blockquote><p>[!Note]</p><p>L'oggetto Rect verrà troncato se si sovrappone ai limiti del bordo dell'immagine di input.<br /></p></blockquote><br /> | 
| D2D1_CROP_PROP_BORDER_MODE<br /> | D2D1_BORDER_MODE <br /> D2D1_BORDER_MODE_SOFT <br /> | <ul><li>D2D1_BORDER_MODE_SOFT: se il rettangolo di ritaglio si applica alle coordinate dei pixel frazionari, l'effetto applica l'antialiasing che determina un bordo soffice.</li><li>D2D1_BORDER_MODE_HARD: se il rettangolo di ritaglio cade sulle coordinate dei pixel frazionari, l'effetto si stringe e viene restituito un bordo rigido.</li></ul> | 




 

## <a name="output-bitmap"></a>Bitmap di output

L'output di questo effetto è la dimensione della proprietà Rect. Lunghezza e larghezza sono calc

con le equazioni seguenti: <dl> Lunghezza dell'output in Pixel=(Rect.Right-Rect.Left) \* (DPI/96 dell'utente)  
Altezza dell'output in pixel=(Rect.Bottom-Rect.Top) \* (DPI/96 dell'utente)  
</dl>

## <a name="requirements"></a>Requisiti



| Requisito | valore |
|--------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato | Windows 8 e Platform Update per Windows 7 \[ app desktop \| Windows Store\] |
| Server minimo supportato | Windows 8 e Platform Update per Windows 7 \[ app desktop \| Windows Store\] |
| Intestazione                   | d2d1effects.h                                                                      |
| Libreria                  | d2d1.lib, dxguid.lib                                                               |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

