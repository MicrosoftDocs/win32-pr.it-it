---
title: Effetto di illuminazione diffusa con riflettore
description: Usare l'effetto di illuminazione con diffusione spot per creare un'immagine che sembra essere una superficie non riflettente con la quale la sorgente di luce è limitata a un cono di luce diretto e la luce è sparpagliata in tutte le direzioni.
ms.assetid: 9048D664-28DB-4DB6-9B95-3A61A1EDF5EC
keywords:
- effetto illuminazione diffusa spot
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d085e43f161275cbe46d5b8eeb03f0ad13ff5f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104552940"
---
# <a name="spot-diffuse-lighting-effect"></a>Effetto di illuminazione diffusa con riflettore

Usare l'effetto di illuminazione con diffusione spot per creare un'immagine che sembra essere una superficie non riflettente con la quale la sorgente di luce è limitata a un cono di luce diretto e la luce è sparpagliata in tutte le direzioni. Questo effetto usa il canale alfa come mappa di altezza e accende l'immagine con una sorgente di luce puntiforme.

Il colore della bitmap di output è il risultato del colore chiaro, della posizione chiara e della geometria della superficie. L'output del canale alfa per ogni pixel con illuminazione diffusa è sempre 1,0.

Il CLSID per questo effetto è CLSID \_ D2D1SpotDiffuse.

-   [Immagine di esempio](#example-image)
-   [Proprietà effetto](#effect-properties)
-   [Modalità di ridimensionamento](#scale-modes)
-   [Requisiti](#requirements)
-   [Argomenti correlati](#related-topics)

## <a name="example-image"></a>Immagine di esempio

Nell'esempio riportato di seguito vengono illustrate le immagini di input e output dell'effetto di illuminazione con diffusione spot.

![schermata di esempio di effetto che Mostra ](images/spot-diffuse-example.png)

L'effetto calcola i valori dei pixel di output finali viene calcolato usando le equazioni seguenti:

![calcolo bitmap di output](images/spot-diffuse-formula.png)

Dove:<dl> k<sub>d</sub> = costante di illuminazione diffusa. Specificato dall'utente.  
![simbolo vettoriale normale.](images/point-spec-mathchar-n.png) = vettore di unità normale della superficie, funzione di x e y.  
![simbolo vettoriale chiaro.](images/distant-spec-mathchar-l.png) = vettore di unità che punta dalla superficie alla luce.  
L<sub>r</sub>, l<sub>g</sub>, l<sub>b</sub> = colore chiaro nei componenti RGB.  
</dl>

## <a name="effect-properties"></a>Proprietà effetto



| Nome visualizzato e enumerazione dell'indice                                                     | Tipo e valore predefinito                                                                      | Descrizione                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Posizioneilluminazione<br/> D2D1 \_ SPOTDIFFUSE \_ - \_ \_ posizione chiara<br/>           | \_Vettore d2d1 \_ 3F<br/> {0,0 f, 0,0 f, 0,0 f}<br/>                                   | Posizione chiara della sorgente di luce del punto. La proprietà è un \_ vettore d2d1 \_ 3F definito come (x, y, z). Le unità sono in DIP (device independent pixel) e non sono associate.<br/>                                                                                                                                                                                                                   |
| PointsAt<br/> \_Punti della \_ prop \_ SPOTDIFFUSE \_ d2d1<br/>                     | \_Vettore d2d1 \_ 3F<br/> {0,0 f, 0,0 f, 0,0 f}<br/>                                   | Dove la luce spot è concentrata. La proprietà viene esposta come vettore D2D1 \_ \_ 3F con (x, y, z). Le unità si trovano in DIP e i valori non sono associati.<br/>                                                                                                                                                                                                                                          |
| Focus<br/> D2D1 \_ SPOTDIFFUSE \_ prop \_ Focus<br/>                             | FLOAT<br/> 1,0 f<br/>                                                            | Lo stato attivo della luce spot. Questa proprietà è unitaria e viene definita tra 0 e 200.<br/>                                                                                                                                                                                                                                                                                                      |
| LimitingConeAngle<br/> D2D1 \_ SPOTDIFFUSE \_ prop \_ limitazione dell' \_ angolo del cono \_<br/> | FLOAT<br/> 90.0 f<br/>                                                           | Angolo del cono che limita l'area in cui viene proiettata la luce. Non viene proiettata alcuna luce all'esterno del cono. L'angolo del cono di limitazione è l'angolo tra l'asse della luce spot (l'asse tra le proprietà *Posizioneilluminazione* e *PointsAt* ) e il cono chiaro. Questa proprietà è definita in gradi e deve essere compresa tra 0 e 90 gradi.<br/>                                            |
| DiffuseConstant<br/> \_Costante d2d1 SPOTDIFFUSE \_ prop \_ diffusa \_<br/>       | FLOAT<br/> 1,0 f<br/>                                                            | Rapporto tra la reflection diffusa e la quantità di luce in arrivo. Questa proprietà deve essere compresa tra 0 e 10.000 ed è di unità. <br/>                                                                                                                                                                                                                                                                     |
| SurfaceScale<br/> D2D1 \_ SPOTDIFFUSE \_ prop \_ Surface \_ scale<br/>             | FLOAT<br/> 1,0 f<br/>                                                            | Fattore di scala nella direzione Z. La scala della superficie è unitaria e deve essere compresa tra 0 e 10.000.<br/>                                                                                                                                                                                                                                                                                          |
| Colore<br/> \_Colore della \_ prop \_ SPOTDIFFUSE d2d1<br/>                             | \_Vettore d2d1 \_ 3F<br/> {1.0 f, 1.0 f, 1.0 f}<br/>                                   | Colore della luce in arrivo. Questa proprietà viene esposta come Vector 3 (R, G, B) e usata per calcolare L<sub>R</sub>, l<sub>G</sub>, l<sub>B</sub>. <br/>                                                                                                                                                                                                                                         |
| KernelUnitLength<br/> \_ \_ \_ \_ Lunghezza unità kernel d2d1 SPOTDIFFUSE \_<br/>   | D2D1 \_ vector \_ 2F<br/> {1.0 f, 1.0 f}<br/>                                         | Dimensione di un elemento nel kernel Sobel utilizzata per generare la normale della superficie nella direzione X e Y. Questa proprietà esegue il mapping ai valori DX e dy nella sfumatura Sobel. Questa proprietà è un \_ vettore d2d1 \_ 2F (lunghezza unità kernel X, lunghezza unità kernel Y) ed è definito in (DIP/unità kernel). L'effetto usa l'interpolazione bilineare per ridimensionare la bitmap in modo che corrisponda alle dimensioni degli elementi del kernel.<br/> |
| ScaleMode<br/> D2D1 \_ SPOTDIFFUSE \_ - \_ modalità scala della Prop \_<br/>                   | \_Modalità di \_ ridimensionamento SPOTDIFFUSE d2d1 \_<br/> D2D1 \_ SPOTDIFFUSE \_ - \_ modalità scala \_ lineare<br/> | Modalità di interpolazione utilizzata dall'effetto per ridimensionare l'immagine alla lunghezza dell'unità kernel corrispondente. Sono disponibili sei modalità di ridimensionamento che variano in qualità e velocità. Per altre informazioni, vedere [modalità di ridimensionamento](#scale-modes) .<br/>                                                                                                                                                                                  |



 

## <a name="scale-modes"></a>Modalità di ridimensionamento



| Enumerazione                                           | Descrizione                                                                                                                                                                                          |
|-------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ SPOTDIFFUSE \_ - \_ modalità scala \_ più \_ vicina     | Campiona il punto singolo più vicino e lo utilizza. In questa modalità viene utilizzato un minor tempo di elaborazione, ma viene restituita l'immagine di qualità più bassa.                                                                           |
| D2D1 \_ SPOTDIFFUSE \_ - \_ modalità scala \_ lineare                | Usa un esempio a quattro punti e un'interpolazione lineare. Questa modalità restituisce un'immagine di qualità superiore a quella più vicina.                                                                                   |
| D2D1 \_ SPOTDIFFUSE- \_ modalità di ridimensionamento \_ \_ cubica                 | Usa un kernel cubico di esempio 16 per l'interpolazione. Questa modalità usa la maggior parte del tempo di elaborazione, ma restituisce un'immagine di qualità superiore.                                                                        |
| D2D1 \_ SPOTDIFFUSE- \_ modalità di scalabilità \_ \_ \_ multicampione \_ lineare | USA 4 campioni lineari all'interno di un singolo pixel per l'anti-aliasing dei bordi validi. Questa modalità è ideale per ridurre le dimensioni delle immagini con pochi pixel.                                              |
| D2D1 \_ \_ modalità di ridimensionamento SPOTDIFFUSE \_ \_           | Usa il filtro anisotropico per campionare un modello in base alla forma trasformata della bitmap.                                                                                                     |
| D2D1 \_ SPOTDIFFUSE \_ - \_ modalità scala di \_ alta \_ qualità \_ cubica  | Usa un kernel cubico a dimensione variabile di alta qualità per eseguire un'downscaling dell'immagine se downscaling è associato alla matrice di trasformazione. USA quindi la modalità di interpolazione cubica per l'output finale. |



 

> [!Note]  
> Se non si seleziona una modalità, l'effetto predefinito è D2D1 \_ SPOTDIFFUSE \_ scale \_ mode \_ Linear.

 

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

 

