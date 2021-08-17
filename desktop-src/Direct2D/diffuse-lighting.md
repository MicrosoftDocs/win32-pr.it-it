---
title: Effetto di illuminazione diffusa con riflettore
description: Usare l'effetto di illuminazione spot-diffuse per creare un'immagine che sembra essere una superficie non riflettente con la quale la sorgente di luce è limitata a un cono di luce diretto e la luce è dispersa in tutte le direzioni.
ms.assetid: 9048D664-28DB-4DB6-9B95-3A61A1EDF5EC
keywords:
- effetto spot diffuse lighting
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59ee0032351ce5409aabf75eaa36cd79362b8e51b85edb26d2d1d06ca9346bfe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075399"
---
# <a name="spot-diffuse-lighting-effect"></a>Effetto di illuminazione diffusa con riflettore

Usare l'effetto di illuminazione spot-diffuse per creare un'immagine che sembra essere una superficie non riflettente con la quale la sorgente di luce è limitata a un cono di luce diretto e la luce è dispersa in tutte le direzioni. Questo effetto usa il canale alfa come mappa di altezza e illumina l'immagine con una sorgente di luce spot.

Il colore della bitmap di output è il risultato del colore chiaro, della posizione della luce e della geometria della superficie. L'output del canale alfa per ogni pixel con illuminazione diffusa è sempre 1,0.

Il CLSID per questo effetto è CLSID \_ D2D1SpotDiffuse.

-   [Immagine di esempio](#example-image)
-   [Proprietà degli effetti](#effect-properties)
-   [Modalità di scalabilità](#scale-modes)
-   [Requisiti](#requirements)
-   [Argomenti correlati](#related-topics)

## <a name="example-image"></a>Immagine di esempio

L'esempio seguente mostra le immagini di input e output dell'effetto di illuminazione spot-diffuse.

![Screenshot di esempio dell'effetto che mostra ](images/spot-diffuse-example.png)

L'effetto calcola i valori finali dei pixel di output usando queste equazioni:

![calcolo bitmap di output](images/spot-diffuse-formula.png)

Dove:<dl> k<sub>d</sub> = costante di illuminazione diffusa. Specificato dall'utente.  
![simbolo di vettore normale.](images/point-spec-mathchar-n.png) = vettore di unità normale della superficie, una funzione di x e y.  
![simbolo di vettore chiaro.](images/distant-spec-mathchar-l.png) = vettore unità che punta dalla superficie alla luce.  
L<sub>r</sub>, L<sub>g</sub>, L<sub>b</sub> = il colore chiaro nei componenti RGB.  
</dl>

## <a name="effect-properties"></a>Proprietà degli effetti



| Nome visualizzato ed enumerazione dell'indice                                                     | Tipo e valore predefinito                                                                      | Descrizione                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LightPosition<br/> D2D1 \_ SPOTDIFFUSE \_ PROP \_ LIGHT \_ POSITION<br/>           | D2D1 \_ VECTOR \_ 3F<br/> {0.0f, 0.0f, 0.0f}<br/>                                   | Posizione della luce della sorgente di luce del punto. La proprietà è un vettore D2D1 \_ \_ 3F definito come (x, y, z). Le unità sono in dip (Device Independent Pixel) e non sono associati.<br/>                                                                                                                                                                                                                   |
| PointsAt<br/> D2D1 \_ SPOTDIFFUSE \_ PROP \_ POINTS \_ AT<br/>                     | D2D1 \_ VECTOR \_ 3F<br/> {0.0f, 0.0f, 0.0f}<br/>                                   | Posizione in cui è concentrata la luce spot. La proprietà viene esposta come vettore D2D1 \_ \_ 3F con (x, y, z). Le unità sono in DIP e i valori non sono associati.<br/>                                                                                                                                                                                                                                          |
| Focus<br/> D2D1 \_ SPOTDIFFUSE \_ PROP \_ FOCUS<br/>                             | FLOAT<br/> 1.0f<br/>                                                            | Messa a fuoco della luce spot. Questa proprietà è senza unità ed è definita tra 0 e 200.<br/>                                                                                                                                                                                                                                                                                                      |
| LimitazioneconeAngle<br/> D2D1 \_ SPOTDIFFUSE \_ PROP \_ LIMITING \_ CONE \_ ANGLE<br/> | FLOAT<br/> 90.0f<br/>                                                           | Angolo del cono che limita l'area in cui viene proiettata la luce. All'esterno del cono non viene proiettata alcuna luce. L'angolo del cono limitante è l'angolo tra l'asse della luce spot (l'asse tra le proprietà *LightPosition* e *PointsAt)* e il cono di luce spot. Questa proprietà è definita in gradi e deve essere compresa tra 0 e 90 gradi.<br/>                                            |
| DiffuseConstant<br/> D2D1 \_ SPOTDIFFUSE \_ PROP \_ DIFFUSE \_ CONSTANT<br/>       | FLOAT<br/> 1.0f<br/>                                                            | Rapporto tra la riflessione diffusa e la quantità di luce in ingresso. Questa proprietà deve essere compresa tra 0 e 10.000 ed è senza unità. <br/>                                                                                                                                                                                                                                                                     |
| SurfaceScale<br/> D2D1 \_ SPOTDIFFUSE \_ PROP \_ SURFACE \_ SCALE<br/>             | FLOAT<br/> 1.0f<br/>                                                            | Fattore di scala nella direzione Z. La scala della superficie è senza unità e deve essere compresa tra 0 e 10.000.<br/>                                                                                                                                                                                                                                                                                          |
| Color<br/> D2D1 \_ SPOTDIFFUSE \_ PROP \_ COLOR<br/>                             | D2D1 \_ VECTOR \_ 3F<br/> {1.0f, 1.0f, 1.0f}<br/>                                   | Colore della luce in ingresso. Questa proprietà viene esposta come vettore 3 (R, G, B) e usata per calcolare L<sub>R,</sub>L<sub>G,</sub>L<sub>B.</sub> <br/>                                                                                                                                                                                                                                         |
| KernelUnitLength<br/> D2D1 \_ SPOTDIFFUSE \_ PROP \_ KERNEL \_ UNIT \_ LENGTH<br/>   | VETTORE D2D1 \_ \_ 2F<br/> {1.0f, 1.0f}<br/>                                         | Dimensione di un elemento nel kernel Sobel usata per generare la normale della superficie nella direzione X e Y. Questa proprietà esegue il mapping ai valori dx e dy nella sfumatura Sobel. Questa proprietà è D2D1 \_ VECTOR \_ 2F(Kernel Unit Length X, Kernel Unit Length Y) ed è definita in (DIP/Unità kernel). L'effetto usa l'interpolazione bilineare per ridimensionare la bitmap in modo che corrisponda alle dimensioni degli elementi del kernel.<br/> |
| Scalemode<br/> D2D1 \_ SPOTDIFFUSE \_ PROP \_ SCALE \_ MODE<br/>                   | D2D1 \_ SPOTDIFFUSE \_ SCALE \_ MODE<br/> D2D1 \_ SPOTDIFFUSE \_ SCALE \_ MODE \_ LINEAR<br/> | Modalità di interpolazione utilizzata dall'effetto per ridimensionare l'immagine in base alla lunghezza dell'unità del kernel corrispondente. Esistono sei modalità di scalabilità che variano in qualità e velocità. Per [altre informazioni, vedere Modalità](#scale-modes) di scalabilità.<br/>                                                                                                                                                                                  |



 

## <a name="scale-modes"></a>Modalità di scalabilità



| Enumerazione                                           | Descrizione                                                                                                                                                                                          |
|-------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ SPOTDIFFUSE \_ SCALE \_ MODE \_ NEAREST \_ NEIGHBOR     | Campiota il singolo punto più vicino e lo usa. Questa modalità usa meno tempo di elaborazione, ma restituisce l'immagine di qualità più bassa.                                                                           |
| D2D1 \_ SPOTDIFFUSE \_ SCALE \_ MODE \_ LINEAR                | Usa un campione di quattro punti e un'interpolazione lineare. Questa modalità restituisce un'immagine di qualità superiore a quella del vicino più vicino.                                                                                   |
| D2D1 \_ SPOTDIFFUSE \_ SCALE \_ MODE \_ CUBIC                 | Usa un kernel cubico di 16 campioni per l'interpolazione. Questa modalità usa la maggior parte del tempo di elaborazione, ma restituisce un'immagine di qualità superiore.                                                                        |
| D2D1 \_ SPOTDIFFUSE \_ SCALE \_ MODE \_ MULTI \_ SAMPLE \_ LINEAR | Usa 4 campioni lineari all'interno di un singolo pixel per un anti-aliasing dei bordi valido. Questa modalità è buona per ridurre di piccole quantità le immagini con pochi pixel.                                              |
| D2D1 \_ SPOTDIFFUSE \_ SCALE MODE \_ \_ ANISO STANDBY           | Usa il filtro anisotropo per campionare un criterio in base alla forma trasformata della bitmap.                                                                                                     |
| D2D1 \_ SPOTDIFFUSE \_ SCALE \_ MODE \_ HIGH \_ QUALITY \_ CUBIC  | Usa un kernel cubico di qualità elevata di dimensioni variabili per eseguire una scalabilità pre-ridimensionata dell'immagine se la scalabilità è coinvolta nella matrice di trasformazione. Usa quindi la modalità di interpolazione cubica per l'output finale. |



 

> [!Note]  
> Se non si seleziona una modalità, per impostazione predefinita l'effetto è D2D1 \_ SPOTDIFFUSE \_ SCALE \_ MODE LINEAR(D2D1 SPOTDIFFUSE SCALE MODE \_ LINEAR).

 

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

 

