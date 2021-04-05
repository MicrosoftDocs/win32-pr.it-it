---
title: Effetto di illuminazione con luce riflettore speculare
description: Usare l'effetto di illuminazione spot-speculare per creare un'immagine che sembra essere una superficie riflettente, in cui la sorgente di luce è limitata a un cono di luce diretto.
ms.assetid: B6E24036-1548-4B9E-A8FE-8B87D4DBF97A
keywords:
- illuminazione speculare spot
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61f2482d9631de7383c26e791d13f1571f247fa6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048237"
---
# <a name="spot-specular-lighting-effect"></a>Effetto di illuminazione con luce riflettore speculare

Usare l'effetto di illuminazione spot-speculare per creare un'immagine che sembra essere una superficie riflettente, in cui la sorgente di luce è limitata a un cono di luce diretto. Questo effetto usa il canale alfa come mappa di altezza e accende l'immagine con una sorgente di luce puntiforme.

Il colore della bitmap di output è il risultato del colore chiaro, della posizione chiara, della direzione del cono e della geometria della superficie in base alla parte speculare del modello di illuminazione Phong. L'output del canale alfa per ogni pixel con illuminazione speculare è il massimo degli output del canale rosso, verde e blu per quel pixel.

Il CLSID per questo effetto è CLSID \_ D2D1SpotSpecular.

-   [Immagine di esempio](#example-image)
-   [Sorgente di luce spot](#spot-light-source)
-   [Proprietà effetto](#effect-properties)
-   [Modalità di ridimensionamento](#scale-modes)
-   [Requisiti](#requirements)
-   [Argomenti correlati](#related-topics)

## <a name="example-image"></a>Immagine di esempio

Nell'esempio riportato di seguito vengono illustrate le immagini di input e output dell'effetto di illuminazione spot-speculare.

![schermata di esempio effetto.](images/spot-spec-example.png)

La luce speculare si riferisce alla luce che viene riflessa in una direzione specifica.

![diagramma dei vettori utilizzati per cacluate un output di illuminazione speculare per una bitmap.](images/point-spec-reflected1.png)

L'effetto calcola i valori dei pixel di output finali viene calcolato usando le equazioni riportate di seguito:

![equazioni del pixel di output.](images/spot-formula1.png)

dove

![definizioni di variabili.](images/spot-formula2.png)

## <a name="spot-light-source"></a>Sorgente di luce spot

Una sorgente di luce spot emette una luce in un cono in una direzione specifica e non emette luce all'esterno del cono.

La sorgente di luce spot calcola il vettore di luce L e il vettore a metà altezza H allo stesso modo dell'effetto del [punto-speculare](point-specular.md) .

L'effetto calcola il colore chiaro, L<sub>r</sub>, l<sub>g</sub>, l<sub>b</sub>, come funzione della posizione della sorgente di luce, come illustrato con le equazioni qui:

![equazione per la sorgente di luce spot](images/spot-formula3.png)

Vettore ![simbolo vettoriale chiaro.](images/spot-mathchar-l.png) viene definito da queste equazioni:

![equazione: Vector](images/spot-formula4.png)

Vettore ![simbolo vettore t](images/spot-mathchar-t.png) viene definito da queste equazioni:

![equazione: Vector 2](images/spot-formula5.png)

## <a name="effect-properties"></a>Proprietà effetto



| Nome visualizzato e enumerazione dell'indice                                                        | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Posizioneilluminazione<br/> D2D1 \_ SPOTSPECULAR \_ - \_ \_ posizione chiara<br/>             | Posizione chiara della sorgente di luce del punto. La proprietà è un \_ vettore d2d1 \_ 3F definito come (x, y, z). Le unità sono in DIP (device independent pixel) e non sono associate. Il tipo è D2D1 \_ vector \_ 3F.<br/> Il valore predefinito è {0,0 f, 0,0 f, 0,0 f}.<br/>                                                                                                                                                                                                              |
| PointsAt<br/> \_Punti della \_ prop \_ SPOTSPECULAR \_ d2d1<br/>                       | Dove la luce spot è concentrata. La proprietà viene esposta come vettore D2D1 \_ \_ 3F con (x, y, z). Le unità si trovano in DIP e i valori non sono associati. Il tipo è D2D1 \_ vector \_ 3F.<br/> Il valore predefinito è {0,0 f, 0,0 f, 0,0 f}.<br/>                                                                                                                                                                                                                                     |
| Focus<br/> D2D1 \_ SPOTSPECULAR \_ prop \_ Focus<br/>                               | Lo stato attivo della luce spot. Questa proprietà è unitaria e viene definita tra 0 e 200. Il tipo è FLOAT.<br/> Il valore predefinito è 1.0 f.<br/>                                                                                                                                                                                                                                                                                                                          |
| LimitingConeAngle<br/> \_Angolo del \_ \_ cono di \_ limitazione della \_ prop \_ d2d1 spot<br/> | Angolo del cono che limita l'area in cui viene proiettata la luce. Non viene proiettata alcuna luce all'esterno del cono. L'angolo del cono di limitazione è l'angolo tra l'asse della luce spot (l'asse tra le proprietà *Posizioneilluminazione* e *PointsAt* ) e il cono chiaro. Questa proprietà è definita in gradi e deve essere compresa tra 0 e 90 gradi. Il tipo è FLOAT.<br/> Il valore predefinito è 90.0 f.<br/>                                                               |
| SpecularExponent<br/> \_ \_ \_ Esponente speculare d2d1 SPOTSPECULAR \_<br/>       | Esponente per il termine speculare nell'equazione di illuminazione Phong. Un valore più grande corrisponde a una superficie più riflettente. Questo valore è di unità e deve essere compreso tra 1,0 e 128. Il tipo è FLOAT.<br/> Il valore predefinito è 1.0 f.<br/>                                                                                                                                                                                                                               |
| SpecularConstant<br/> D2D1 \_ SPOTSPECULAR \_ prop \_ - \_ costante speculare<br/>       | Rapporto della reflection speculare alla luce in arrivo. Il valore è di unità e deve essere compreso tra 0 e 10.000. Il tipo è FLOAT.<br/> Il valore predefinito è 1.0 f.<br/>                                                                                                                                                                                                                                                                                                   |
| SurfaceScale<br/> D2D1 \_ SPOTSPECULAR \_ prop \_ Surface \_ scale<br/>               | Fattore di scala nella direzione Z per la generazione di una mappa di altezza. Il valore è di unità e deve essere compreso tra 0 e 10.000. Il tipo è FLOAT.<br/> Il valore predefinito è 1.0 f.<br/>                                                                                                                                                                                                                                                                                          |
| Colore<br/> \_Colore della \_ prop \_ SPOTSPECULAR d2d1<br/>                               | Colore della luce in arrivo. Questa proprietà viene esposta come Vector 3 (R, G, B) e usata per calcolare L<sub>R</sub>, l<sub>G</sub>, l<sub>B</sub>. Il tipo è D2D1 \_ vector \_ 3F.<br/> Il valore predefinito è {1.0 f, 1.0 f, 1.0 f}.<br/>                                                                                                                                                                                                                                     |
| KernelUnitLength<br/> \_ \_ \_ \_ Lunghezza unità kernel d2d1 SPOTSPECULAR \_<br/>     | Dimensione di un elemento nel kernel Sobel utilizzata per generare la normale della superficie nella direzione X e Y. Questa proprietà esegue il mapping ai valori DX e dy nella sfumatura Sobel. Questa proprietà è un \_ vettore d2d1 \_ 2F (lunghezza unità kernel X, lunghezza unità kernel Y) ed è definito in (DIP/unità kernel). L'effetto usa l'interpolazione bilineare per ridimensionare la bitmap in modo che corrisponda alle dimensioni degli elementi del kernel. Il tipo è D2D1 \_ vector \_ 2F.<br/> Il valore predefinito è {1.0 f, 1.0 f}.<br/> |
| ScaleMode<br/> D2D1 \_ SPOTSPECULAR \_ - \_ modalità scala della Prop \_<br/>                     | Modalità di interpolazione utilizzata dall'effetto per ridimensionare l'immagine alla lunghezza dell'unità kernel corrispondente. Sono disponibili sei modalità di ridimensionamento che variano in qualità e velocità. Per altre informazioni, vedere [modalità di ridimensionamento](#scale-modes) . <br/> Il tipo è D2D1 \_ SPOTSPECULAR \_ scale \_ mode.<br/> Il valore predefinito è D2D1 \_ SPOTSPECULAR \_ scale \_ mode \_ Linear.<br/>                                                                                                                             |



 

## <a name="scale-modes"></a>Modalità di ridimensionamento



| Enumerazione                                            | Descrizione                                                                                                                                                                                          |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ SPOTSPECULAR \_ - \_ modalità scala \_ più \_ vicina     | Campiona il punto singolo più vicino e lo utilizza. In questa modalità viene utilizzato un minor tempo di elaborazione, ma viene restituita l'immagine di qualità più bassa.                                                                           |
| D2D1 \_ SPOTSPECULAR \_ - \_ modalità scala \_ lineare                | Usa un esempio a quattro punti e un'interpolazione lineare. Questa modalità restituisce un'immagine di qualità superiore a quella più vicina.                                                                                   |
| D2D1 \_ SPOTSPECULAR- \_ modalità di ridimensionamento \_ \_ cubica                 | Usa un kernel cubico di esempio 16 per l'interpolazione. Questa modalità usa la maggior parte del tempo di elaborazione, ma restituisce un'immagine di qualità superiore.                                                                        |
| D2D1 \_ SPOTSPECULAR- \_ modalità di scalabilità \_ \_ \_ multicampione \_ lineare | USA 4 campioni lineari all'interno di un singolo pixel per l'anti-aliasing dei bordi validi. Questa modalità è ideale per ridurre le dimensioni delle immagini con pochi pixel.                                              |
| D2D1 \_ \_ modalità di ridimensionamento SPOTSPECULAR \_ \_           | Usa il filtro anisotropico per campionare un modello in base alla forma trasformata della bitmap.                                                                                                     |
| D2D1 \_ SPOTSPECULAR \_ - \_ modalità scala di \_ alta \_ qualità \_ cubica  | Usa un kernel cubico a dimensione variabile di alta qualità per eseguire un'downscaling dell'immagine se downscaling è associato alla matrice di trasformazione. USA quindi la modalità di interpolazione cubica per l'output finale. |



 

> [!Note]  
> Se non si seleziona una modalità, l'effetto predefinito è D2D1 \_ SPOTSPECULAR \_ scale \_ mode \_ Linear.

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

 

