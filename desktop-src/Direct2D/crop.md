---
title: Effetto di ritaglio
description: Usare l'effetto di ritaglio per restituire un'area specificata di un'immagine.
ms.assetid: DFB7DE20-F202-4E7F-AE63-94BF817B6E30
keywords:
- effetto di ritaglio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 653ceaf4cf8b5922fe05e151c1639269f3169b57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873761"
---
# <a name="crop-effect"></a>Effetto di ritaglio

Usare l'effetto di ritaglio per restituire un'area specificata di un'immagine.

Il CLSID per questo effetto è CLSID \_ D2D1Crop.

-   [Immagine di esempio](#example-image)
-   [Proprietà effetto](#effect-properties)
-   [Bitmap di output](#output-bitmap)
-   [Requisiti](#requirements)
-   [Argomenti correlati](#related-topics)

## <a name="example-image"></a>Immagine di esempio



| Prima                                                     |
|------------------------------------------------------------|
| ![immagine prima dell'effetto.](images/default-before.jpg) |
| After                                                      |
| ![immagine dopo la trasformazione.](images/8-crop.png)       |



 


```C++
ComPtr<ID2D1Effect> cropEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Crop, &cropEffect);

cropEffect->SetInput(0, bitmap);
cropEffect->SetValue(D2D1_CROP_PROP_RECT, D2D1::RectF(0.0f, 0.0f, 256.0f, 192.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(cropEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Proprietà effetto



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Nome visualizzato e enumerazione dell'indice</th>
<th>Tipo e valore predefinito</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Rect<br/></td>
<td>D2D1_VECTOR_4F<br/></td>
<td>Area da ritagliare specificata come vettore nel form (a sinistra, superiore, larghezza, altezza).<br/></td>
</tr>
<tr class="even">
<td>D2D1_CROP_PROP_RECT<br/></td>
<td>{-FLT_MAX,-FLT_MAX, FLT_MAX, FLT_MAX}<br/></td>
<td>Le unità sono in tuffi. <br/>
<blockquote>
<p>[!Note]</p>
<p>Il rettangolo verrà troncato se si sovrappone ai limiti del bordo dell'immagine di input.<br/></p>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>D2D1_CROP_PROP_BORDER_MODE<br/></td>
<td>D2D1_BORDER_MODE <br/> D2D1_BORDER_MODE_SOFT <br/></td>
<td><ul>
<li>D2D1_BORDER_MODE_SOFT: se il rettangolo di ritaglio è costituito da coordinate dei pixel frazionari, l'effetto applica l'anti-aliasing che produce un bordo flessibile.</li>
<li>D2D1_BORDER_MODE_HARD: se il rettangolo di ritaglio è costituito da coordinate dei pixel frazionari, l'effetto si blocca che determina un bordo rigido.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="output-bitmap"></a>Bitmap di output

L'output di questo effetto corrisponde alla dimensione della proprietà Rect. La lunghezza e la larghezza sono calcoli

ulated usando le equazioni qui: <dl> Lunghezza di output in pixel = (Rect. Right-Rect. Left) \* (dpi utente/96)  
Altezza di output in pixel = (Rect. Bottom-Rect.Top) \* (dpi utente/96)  
</dl>

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

 

