---
title: Effetto di illuminazione con luce puntuale speculare
description: Usare l'effetto di illuminazione punto-speculare per creare un'immagine che sembra essere una superficie riflettente.
ms.assetid: 89E22FD0-BB7F-465F-A79C-056CA9F14F5D
keywords:
- effetto illuminazione speculare punti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 355c573888604af8dfac443f4f53554a8a780071
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964537"
---
# <a name="point-specular-lighting-effect"></a>Effetto di illuminazione con luce puntuale speculare

Usare l'effetto di illuminazione punto-speculare per creare un'immagine che sembra essere una superficie riflettente. L'effetto usa il canale alfa dell'immagine come mappa di altezza e una sorgente di luce puntiforme posizionata e calcola la reflection e la luce in base alla parte speculare del modello di illuminazione Phong.

Il colore della bitmap di output è il risultato del colore chiaro, della posizione chiara e della geometria della superficie. L'output del canale alfa per ogni pixel con illuminazione speculare è il massimo degli output del canale rosso, verde e blu per quel pixel.

Il CLSID per questo effetto è CLSID \_ D2D1PointSpecular.

-   [Immagine di esempio](#example-image)
-   [Origine punto luce](#point-light-source)
-   [Mappa altezza e vettore normale](#height-map-and-normal-vector)
-   [Costante e esponente di illuminazione speculare](#specular-lighting-constant-and-exponent)
-   [Proprietà effetto](#effect-properties)
-   [Ridimensiona le modalità](#scales-modes)
-   [Requisiti](#requirements)
-   [Argomenti correlati](#related-topics)

## <a name="example-image"></a>Immagine di esempio

Nell'esempio riportato di seguito vengono illustrate le immagini di input e output dell'effetto di illuminazione punto-speculare.

![schermata di esempio dell'effetto che mostra le immagini di input e output dell'effetto di illuminazione speculare del punto.](images/point-spec-example.png)

La luce speculare si riferisce alla luce che viene riflessa in una direzione specifica in base al modello di illuminazione Phong.

![diagramma dei vettori utilizzati per cacluate un output di illuminazione speculare per una bitmap.](images/point-spec-reflected1.png)

L'effetto calcola i valori dei pixel di output finali usando le equazioni seguenti:

![equazioni per il calcolo dei valori finali dei pixel. ](images/point-spec-formula-output.png)

dove<dl> k? = costante di illuminazione speculare.  
![simbolo del vettore di unità normale della superficie. ](images/point-spec-mathchar-n.png) = vettore di unità normale della superficie che è una funzione di x e y. Vedere [mappa altezza e vettore normale](#height-map-and-normal-vector) per i calcoli.  
![simbolo del vettore di unità a metà. ](images/point-spec-mathchar-h.png) = vettore di unità "a metà" tra il vettore dell'unità occhio e il vettore di unità chiaro. Vedere [punto luce sorgente](#point-light-source) per i calcoli.  
L<sub>r</sub>, l<sub>g</sub>, l<sub>b</sub> = colore chiaro nei componenti RGB.  
</dl>

Impostare la costante di illuminazione speculare come proprietà *SpecularConstant* e il colore chiaro come proprietà *color* .

## <a name="point-light-source"></a>Origine punto luce

Una sorgente di luce puntiforme emette la luce in tutte le direzioni, come nell'immagine.

![luce puntiforme che emette la luce in tutte le direzioni.](images/point-spec-light.png)

È possibile impostare la posizione della sorgente di luce usando la proprietà *Posizioneilluminazione* . L'effetto calcola il vettore di luce, L, per una sorgente di luce puntiforme usando le equazioni seguenti:

![equazione del vettore chiaro.](images/point-spec-formula3.png)

dove Light?, Light<sub>y</sub>e Light<sub>z</sub> sono la posizione della luce di input. L'effetto calcola il vettore a metà, ovvero il ![ simbolo vettoriale a metà.](images/point-spec-mathchar-h.png) come definito nel modello di illuminazione Phong, usando qui l'equazione. Il modello di illuminazione presuppone che il vettore occhi, ![ il simbolo del vettore occhi ](images/point-spec-mathchar-e.png) , si trovi in (0, 0, 1).

![equazione vettoriale a metà.](images/point-spec-formula4.png)

Sia L che H vengono normalizzati in vettori di lunghezza unità.

## <a name="height-map-and-normal-vector"></a>Mappa altezza e vettore normale

L'effetto genera una mappa di altezza per l'immagine di input basata sul canale alfa.

Il componente Height (Z) viene calcolato utilizzando l'equazione:

![equazione per calcolare l'altezza (z) della superficie.](images/point-spec-formula6.png)

L'effetto calcola la normale della superficie, ![simbolo di vettore normale.](images/point-spec-mathchar-n.png), per la bitmap di input utilizzando una sfumatura Sobel.

## <a name="specular-lighting-constant-and-exponent"></a>Costante e esponente di illuminazione speculare

La luce speculare rappresenta la luce riflessa dalla superficie della mappa dell'altezza dell'immagine. Specificare la proprietà *SpecularExponent* che determina la quantità di Reflection speculare dalla bitmap.

Gli esponenti più grandi rappresentano oggetti più lucidi e riflettono la luce in una forma più mirata.

Proprietà di *SpecularConstant* K? definisce la quantità di luce riflessa come rapporto della luce in arrivo.

## <a name="effect-properties"></a>Proprietà effetto



| Nome visualizzato e enumerazione dell'indice                                                     | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Posizioneilluminazione<br/> D2D1 \_ POINTSPECULAR \_ - \_ \_ posizione chiara<br/>         | Posizione chiara della sorgente di luce del punto. La proprietà è un \_ vettore d2d1 \_ 3F definito come (x, y, z). Le unità si trovano in DIP (device independent pixel) e i valori sono senza unità e senza limiti. Il tipo è D2D1 \_ vector \_ 3F.<br/> Il valore predefinito è {0,0 f, 0,0 f, 0,0 f}.<br/>                                                                                                                                                                                      |
| SpecularExponent<br/> \_ \_ \_ Esponente speculare d2d1 POINTSPECULAR \_<br/>   | Esponente per il termine speculare nell'equazione di illuminazione Phong. Un valore più grande corrisponde a una superficie più riflettente. Questo valore è di unità e deve essere compreso tra 1,0 e 128. Il tipo è FLOAT.<br/> Il valore predefinito è 1.0 f.<br/>                                                                                                                                                                                                                               |
| SpecularConstant<br/> D2D1 \_ POINTSPECULAR \_ prop \_ - \_ costante speculare<br/>   | Rapporto della reflection speculare alla luce in arrivo. Il valore è di unità e deve essere compreso tra 0 e 10.000. Il tipo è FLOAT.<br/> Il valore predefinito è 1.0 f.<br/>                                                                                                                                                                                                                                                                                                   |
| SurfaceScale<br/> D2D1 \_ POINTSPECULAR \_ prop \_ Surface \_ scale<br/>           | Fattore di scala nella direzione Z per la generazione di una mappa di altezza. Il valore è di unità e deve essere compreso tra 0 e 10.000. Il tipo è FLOAT.<br/> Il valore predefinito è 1.0 f.<br/>                                                                                                                                                                                                                                                                                          |
| Colore<br/> \_Colore della \_ prop \_ POINTSPECULAR d2d1<br/>                           | Colore della luce in arrivo. Questa proprietà viene esposta come vettore D2D1 \_ \_ 3F (R, G, B) e usata per calcolare l<sub>R</sub>, l<sub>G</sub>, l<sub>B</sub>. Il tipo è D2D1 \_ vector \_ 3F.<br/> Il valore predefinito è {1.0 f, 1.0 f, 1.0 f}.<br/>                                                                                                                                                                                                                             |
| KernelUnitLength<br/> \_ \_ \_ \_ Lunghezza unità kernel d2d1 POINTSPECULAR \_<br/> | Dimensione di un elemento nel kernel Sobel utilizzata per generare la normale della superficie nelle direzioni X e Y. Questa proprietà esegue il mapping ai valori DX e dy nella sfumatura Sobel. Questa proprietà è un \_ vettore d2d1 \_ 2F (lunghezza unità kernel X, lunghezza unità kernel Y) ed è definito in (DIP/unità kernel). L'effetto usa l'interpolazione bilineare per ridimensionare la bitmap in modo che corrisponda alle dimensioni degli elementi del kernel. Il tipo è D2D1 \_ vector \_ 2F.<br/> Il valore predefinito è {1.0 f, 1.0 f}.<br/> |
| ScaleMode<br/> D2D1 \_ POINTSPECULAR \_ - \_ modalità scala della Prop \_<br/>                 | Modalità di interpolazione utilizzata dall'effetto per ridimensionare l'immagine alla lunghezza dell'unità kernel corrispondente. Sono disponibili sei modalità di ridimensionamento che variano in qualità e velocità. Per altre informazioni, vedere [modalità di ridimensionamento](#scales-modes) . <br/> Il tipo è D2D1 \_ POINTSPECULAR \_ scale \_ mode.<br/> Il valore predefinito è D2D1 \_ POINTSPECULAR \_ scale \_ mode \_ Linear.<br/>                                                                                                                          |



 

## <a name="scales-modes"></a>Ridimensiona le modalità



| Enumerazione                                             | Descrizione                                                                                                                                                                                          |
|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ POINTSPECULAR \_ - \_ modalità scala \_ più \_ vicina     | Campiona il punto singolo più vicino e lo utilizza. In questa modalità viene utilizzato un minor tempo di elaborazione, ma viene restituita l'immagine di qualità più bassa.                                                                           |
| D2D1 \_ POINTSPECULAR \_ - \_ modalità scala \_ lineare                | Usa un esempio a quattro punti e un'interpolazione lineare. Questa modalità restituisce un'immagine di qualità superiore a quella più vicina.                                                                                   |
| D2D1 \_ POINTSPECULAR- \_ modalità di ridimensionamento \_ \_ cubica                 | Usa un kernel cubico di esempio 16 per l'interpolazione. Questa modalità usa la maggior parte del tempo di elaborazione, ma restituisce un'immagine di qualità superiore.                                                                        |
| D2D1 \_ POINTSPECULAR- \_ modalità di scalabilità \_ \_ \_ multicampione \_ lineare | USA 4 campioni lineari all'interno di un singolo pixel per l'anti-aliasing dei bordi validi. Questa modalità è ideale per ridurre le dimensioni delle immagini con pochi pixel.                                              |
| D2D1 \_ \_ modalità di ridimensionamento POINTSPECULAR \_ \_           | Usa il filtro anisotropico per campionare un modello in base alla forma trasformata della bitmap.                                                                                                     |
| D2D1 \_ POINTSPECULAR \_ - \_ modalità scala di \_ alta \_ qualità \_ cubica  | Usa un kernel cubico a dimensione variabile di alta qualità per eseguire un'downscaling dell'immagine se downscaling è associato alla matrice di trasformazione. USA quindi la modalità di interpolazione cubica per l'output finale. |



 

> [!Note]  
> Se non si seleziona una modalità, l'effetto predefinito è D2D1 \_ POINTSPECULAR \_ scale \_ mode \_ Linear.

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

 

