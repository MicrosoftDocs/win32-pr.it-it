---
title: Effetto di illuminazione con luce puntuale diffusa
description: Usare l'effetto di illuminazione a virgola diffusa per creare un'immagine che sembra essere una superficie non riflettente con la luce sparsa in tutte le direzioni. Questo effetto usa il canale alfa come mappa di altezza e accende l'immagine con una sorgente di luce puntiforme.
ms.assetid: C98A4962-B9EB-4095-9AC4-F1C32C574892
keywords:
- effetto di illuminazione con diffusione puntiforme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de97edfa6c2166d5c29649aabfe97761440f8f18
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048639"
---
# <a name="point-diffuse-lighting-effect"></a>Effetto di illuminazione con luce puntuale diffusa

Usare l'effetto di illuminazione a virgola diffusa per creare un'immagine che sembra essere una superficie non riflettente con la luce sparsa in tutte le direzioni. Questo effetto usa il canale alfa come mappa di altezza e accende l'immagine con una sorgente di luce puntiforme.

Il colore della bitmap di output è il risultato del colore chiaro, della posizione chiara e della geometria della superficie. L'output del canale alfa per ogni pixel con illuminazione diffusa è sempre 1,0.

Il CLSID per questo effetto è CLSID \_ D2D1PointDiffuse. Per usare questo effetto, aggiungere dxguid. lib alle dipendenze del linker.

-   [Immagine di esempio](#example-image)
-   [Proprietà effetto](#effect-properties)
-   [Modalità di ridimensionamento](#scale-modes)
-   [Requisiti](#requirements)
-   [Argomenti correlati](#related-topics)

## <a name="example-image"></a>Immagine di esempio

Nell'esempio riportato di seguito vengono illustrate le immagini di input e di output dell'effetto di illuminazione con diffusione puntiforme.

![schermata di esempio di effetto che mostra le immagini di input e output dell'effetto di illuminazione diffusa del punto.](images/point-diffuse-example.png)

L'illuminazione diffusa si riferisce alla luce che viene riflessa in più direzioni, come illustrato qui.

![la luce diffusa di illuminazione è sparsa in tutte le direzioni.](images/point-diffuse-lighting.png)

L'effetto calcola i valori dei pixel di output finali viene calcolato usando le equazioni seguenti:

![calcoli bitmap di output.](images/point-diffuse-formula1.png)

Dove:<dl> k<sub>d</sub> = costante di illuminazione diffusa. Specificato dall'utente.  
![simbolo di vettore normale della superficie.](images/point-spec-mathchar-n.png) = vettore di unità normale della superficie, funzione di x e y.  
![simbolo del vettore di unità.](images/distant-spec-mathchar-l.png) = vettore di unità che punta dalla superficie alla luce.  
L<sub>r</sub>, l<sub>g</sub>, l<sub>b</sub> = colore chiaro nei componenti RGB.  
</dl>

## <a name="effect-properties"></a>Proprietà effetto



| Nome visualizzato e enumerazione dell'indice                                                    | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Posizioneilluminazione<br/> D2D1 \_ POINTDIFFUSE \_ - \_ \_ posizione chiara<br/>         | Posizione chiara della sorgente di luce del punto. La proprietà è un \_ vettore d2d1 \_ 3F definito come (x, y, z). Le unità sono in DIP (device independent pixel) e non sono associate. <br/> Il tipo è D2D1 \_ vector \_ 3F.<br/> Il valore predefinito è {0,0 f, 0,0 f, 0,0 f}.<br/>                                                                                                                                                                                                              |
| DiffuseConstant<br/> \_Costante d2d1 POINTDIFFUSE \_ prop \_ diffusa \_<br/>     | Rapporto tra la reflection diffusa e la quantità di luce in arrivo. Questa proprietà deve essere compresa tra 0 e 10.000 ed è di unità. <br/> Il tipo è FLOAT.<br/> Il valore predefinito è 1.0 f.<br/>                                                                                                                                                                                                                                                                                          |
| SurfaceScale<br/> D2D1 \_ POINTDIFFUSE \_ prop \_ Surface \_ scale<br/>           | Fattore di scala nella direzione Z. La scala della superficie è unitaria e deve essere compresa tra 0 e 10.000.<br/> Il tipo è FLOAT.<br/> Il valore predefinito è 1.0 f.<br/>                                                                                                                                                                                                                                                                                                               |
| Colore<br/> \_Colore della \_ prop \_ POINTDIFFUSE d2d1<br/>                           | Colore della luce in arrivo. Questa proprietà viene esposta come Vector 3 (R, G, B) e usata per calcolare L<sub>R</sub>, l<sub>G</sub>, l<sub>B</sub>. <br/> Il tipo è D2D1 \_ vector \_ 3F.<br/> Il valore predefinito è {1.0 f, 1.0 f, 1.0 f}.<br/>                                                                                                                                                                                                                                     |
| KernelUnitLength<br/> \_ \_ \_ \_ Lunghezza unità kernel d2d1 POINTDIFFUSE \_<br/> | Dimensione di un elemento nel kernel Sobel utilizzata per generare la normale della superficie nella direzione X e Y. Questa proprietà esegue il mapping ai valori DX e dy nella sfumatura Sobel. Questa proprietà è un \_ vettore d2d1 \_ 2F (lunghezza unità kernel X, lunghezza unità kernel Y) ed è definito in (DIP/unità kernel). L'effetto usa l'interpolazione bilineare per ridimensionare la bitmap in modo che corrisponda alle dimensioni degli elementi del kernel. <br/> Il tipo è D2D1 \_ vector \_ 2F.<br/> Il valore predefinito è {1.0 f, 1.0 f}.<br/> |
| ScaleMode<br/> D2D1 \_ POINTDIFFUSE \_ - \_ modalità scala della Prop \_<br/>                 | Modalità di interpolazione utilizzata dall'effetto per ridimensionare l'immagine alla lunghezza dell'unità kernel corrispondente. Sono disponibili sei modalità di ridimensionamento che variano in qualità e velocità. Per altre informazioni, vedere [modalità di ridimensionamento](#scale-modes) . <br/> Il tipo è D2D1 \_ POINTDIFFUSE \_ scale \_ mode.<br/> Il valore predefinito è D2D1 \_ POINTDIFFUSE \_ scale \_ mode \_ Linear.<br/>                                                                                                                                         |



 

## <a name="scale-modes"></a>Modalità di ridimensionamento



| Enumerazione                                            | Descrizione                                                                                                                                                                                          |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ POINTDIFFUSE \_ - \_ modalità scala \_ più \_ vicina     | Campiona il punto singolo più vicino e lo utilizza. In questa modalità viene utilizzato un minor tempo di elaborazione, ma viene restituita l'immagine di qualità più bassa.                                                                           |
| D2D1 \_ POINTDIFFUSE \_ - \_ modalità scala \_ lineare                | Usa un esempio a quattro punti e un'interpolazione lineare. Questa modalità restituisce un'immagine di qualità superiore a quella più vicina.                                                                                   |
| D2D1 \_ POINTDIFFUSE- \_ modalità di ridimensionamento \_ \_ cubica                 | Usa un kernel cubico di esempio 16 per l'interpolazione. Questa modalità usa la maggior parte del tempo di elaborazione, ma restituisce un'immagine di qualità superiore.                                                                        |
| D2D1 \_ POINTDIFFUSE- \_ modalità di scalabilità \_ \_ \_ multicampione \_ lineare | USA 4 campioni lineari all'interno di un singolo pixel per l'anti-aliasing dei bordi validi. Questa modalità è ideale per ridurre le dimensioni delle immagini con pochi pixel.                                              |
| D2D1 \_ \_ modalità di ridimensionamento POINTDIFFUSE \_ \_           | Usa il filtro anisotropico per campionare un modello in base alla forma trasformata della bitmap.                                                                                                     |
| D2D1 \_ POINTDIFFUSE \_ - \_ modalità scala di \_ alta \_ qualità \_ cubica  | Usa un kernel cubico a dimensione variabile di alta qualità per eseguire un'downscaling dell'immagine se downscaling è associato alla matrice di trasformazione. USA quindi la modalità di interpolazione cubica per l'output finale. |



 

> [!Note]  
> Se non si seleziona una modalità, l'effetto predefinito è D2D1 \_ POINTDIFFUSE \_ scale \_ mode \_ Linear.

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

 

