---
title: Effetto di illuminazione con luce puntuale speculare
description: Usare l'effetto di illuminazione speculare punto per creare un'immagine che sembra essere una superficie riflettente.
ms.assetid: 89E22FD0-BB7F-465F-A79C-056CA9F14F5D
keywords:
- effetto di illuminazione speculare punto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37adb0c6ea0ca946abf819730dcc378f421bf2c220dc0ab8d41916f570501d0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075185"
---
# <a name="point-specular-lighting-effect"></a>Effetto di illuminazione con luce puntuale speculare

Usare l'effetto di illuminazione speculare punto per creare un'immagine che sembra essere una superficie riflettente. L'effetto usa il canale alfa dell'immagine come mappa di altezza e una sorgente di luce punto posizionata e calcola la luce e la reflection in base alla parte speculare del modello di illuminazione Phong.

Il colore della bitmap di output è il risultato di colore chiaro, posizione della luce e geometria della superficie. L'output del canale alfa per ogni pixel con illuminazione speculare è il massimo degli output dei canali rosso, verde e blu per tale pixel.

Il CLSID per questo effetto è CLSID \_ D2D1PointSpecular.

-   [Immagine di esempio](#example-image)
-   [Sorgente di luce punto](#point-light-source)
-   [Mappa dell'altezza e vettore normale](#height-map-and-normal-vector)
-   [Costante ed esponente dell'illuminazione speculare](#specular-lighting-constant-and-exponent)
-   [Proprietà degli effetti](#effect-properties)
-   [Scales modes (Modalità di ridimensionamento)](#scales-modes)
-   [Requisiti](#requirements)
-   [Argomenti correlati](#related-topics)

## <a name="example-image"></a>Immagine di esempio

L'esempio seguente mostra le immagini di input e output dell'effetto di illuminazione speculare punto.

![Screenshot di esempio dell'effetto che mostra le immagini di input e output dell'effetto di illuminazione speculare punto.](images/point-spec-example.png)

La luce speculare si riferisce alla luce riflessa in una direzione specifica in base al modello di illuminazione Phong.

![diagramma dei vettori usati per ottenere un output di illuminazione speculare per una bitmap.](images/point-spec-reflected1.png)

L'effetto calcola i valori in pixel di output finali usando le equazioni qui:

![equazioni per il calcolo dei valori in pixel finali. ](images/point-spec-formula-output.png)

dove<dl> K? = costante di illuminazione speculare.  
![simbolo del vettore di unità normale della superficie. ](images/point-spec-mathchar-n.png) = vettore di unità normale della superficie che è una funzione di x e y. Per [i calcoli, vedere Mappa dell'altezza](#height-map-and-normal-vector) e vettore normale.  
![Simbolo del vettore di unità a metà. ](images/point-spec-mathchar-h.png) = vettore di unità "a metà" tra vettore di unità oculare e vettore di unità di luce. Per [i calcoli, vedere](#point-light-source) Point light source (Sorgente di luce punto).  
L<sub>r</sub>, L<sub>g</sub>, L<sub>b</sub> = il colore chiaro nei componenti RGB.  
</dl>

Impostare la costante di illuminazione speculare come *proprietà SpecularConstant* e il colore chiaro come *proprietà Color.*

## <a name="point-light-source"></a>Sorgente di luce punto

Una sorgente di luce punto emette luce in tutte le direzioni, come nell'immagine qui.

![una luce punto che emette luce in tutte le direzioni.](images/point-spec-light.png)

È possibile impostare la posizione della sorgente di luce usando *la proprietà LightPosition.* L'effetto calcola il vettore di luce, L, per una sorgente di luce punto usando le equazioni seguenti:

![equazione del vettore di luce.](images/point-spec-formula3.png)

dove Light?, Light<sub>y</sub>e Light<sub>z</sub> sono la posizione della luce di input. L'effetto calcola il simbolo del vettore a metà ![ strada.](images/point-spec-mathchar-h.png) come definito nel modello di illuminazione Phong, usando l'equazione qui. Il modello di illuminazione presuppone che il vettore oculare, il simbolo del vettore oculare , si trovi ![ ](images/point-spec-mathchar-e.png) in (0,0,1).

![equazione di vettore a metà.](images/point-spec-formula4.png)

Sia L che H vengono normalizzati in vettori di lunghezza unità.

## <a name="height-map-and-normal-vector"></a>Mappa dell'altezza e vettore normale

L'effetto genera una mappa di altezza per l'immagine di input in base al canale alfa.

Il componente altezza (Z) viene calcolato usando l'equazione:

![Equazione per il calcolo dell'altezza (z) della superficie.](images/point-spec-formula6.png)

L'effetto calcola la normale della superficie, ![simbolo di vettore normale.](images/point-spec-mathchar-n.png), per la bitmap di input che usa una sfumatura Sobel.

## <a name="specular-lighting-constant-and-exponent"></a>Costante ed esponente dell'illuminazione speculare

La luce speculare rappresenta la luce riflessa dalla superficie dell'oggetto della mappa dell'altezza dell'immagine. Si specifica la *proprietà SpecularExponent* che determina la quantità di reflection speculare dalla bitmap.

Gli esponenti più grandi rappresentano oggetti più luminosi e riflettono la luce in una forma più mirata.

La *proprietà SpecularConstant* K? definisce la quantità di luce riflessa come rapporto della luce in ingresso.

## <a name="effect-properties"></a>Proprietà degli effetti



| Enumerazione del nome visualizzato e dell'indice                                                     | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LightPosition<br/> PUNTI \_ D2D1SOCIEZIONE \_ DELLA LUCE DELLA PROPRIETÀ \_ D2D1 \_<br/>         | Posizione di luce della sorgente di luce punto. La proprietà è un vector 3F D2D1 \_ \_ definito come (x, y, z). Le unità sono espresse in DIP (Device Independent Pixel) e i valori sono senza unità e senza debounded. Il tipo è D2D1 \_ VECTOR \_ 3F.<br/> Il valore predefinito è {0.0f, 0.0f, 0.0f}.<br/>                                                                                                                                                                                      |
| SpecularExponent<br/> PUNTI D2D1 \_ \_ ESPONENTE \_ SPECULARE DELLA PROPRIETÀ \_ SPECULARE<br/>   | Esponente per il termine speculare nell'equazione di illuminazione phong. Un valore più grande corrisponde a una superficie più riflettente. Questo valore è senza unità e deve essere compreso tra 1,0 e 128. Il tipo è FLOAT.<br/> Il valore predefinito è 1,0f.<br/>                                                                                                                                                                                                                               |
| SpecularConstant<br/> COSTANTE \_ \_ SPECULARE DELLA PROPRIETÀ POINTPEULAR D2D1 \_ \_<br/>   | Rapporto tra la reflection speculare e la luce in ingresso. Il valore è senza unità e deve essere compreso tra 0 e 10.000. Il tipo è FLOAT.<br/> Il valore predefinito è 1,0f.<br/>                                                                                                                                                                                                                                                                                                   |
| SurfaceScale<br/> D2D1 \_ POINTSPECOLARE \_ LA SUPERFICIE DELLA PROPRIETÀ \_ \_ SCALA<br/>           | Fattore di scala nella direzione Z per la generazione di una mappa di altezza. Il valore è senza unità e deve essere compreso tra 0 e 10.000. Il tipo è FLOAT.<br/> Il valore predefinito è 1,0f.<br/>                                                                                                                                                                                                                                                                                          |
| Color<br/> D2D1 \_ POINTSPECOLARE \_ PROP \_ COLOR<br/>                           | Colore della luce in ingresso. Questa proprietà viene esposta come D2D1 \_ VECTOR \_ 3F (R, G,<sub></sub>B)<sub></sub>e usata per calcolare L<sub>R</sub>, L G , L B . Il tipo è D2D1 \_ VECTOR \_ 3F.<br/> Il valore predefinito è {1.0f, 1.0f, 1.0f}.<br/>                                                                                                                                                                                                                             |
| KernelUnitLength<br/> D2D1 \_ POINTSPECOLARE \_ LUNGHEZZA UNITÀ KERNEL PROP \_ \_ \_<br/> | Dimensione di un elemento nel kernel Sobel usata per generare la normale della superficie nelle direzioni X e Y. Questa proprietà esegue il mapping ai valori dx e dy nella sfumatura Sobel. Questa proprietà è D2D1 \_ VECTOR \_ 2F (Kernel Unit Length X, Kernel Unit Length Y) ed è definita in (DIP/unità kernel). L'effetto usa l'interpolazione bilineare per ridimensionare la bitmap in modo che corrisponda alle dimensioni degli elementi del kernel. Il tipo è D2D1 \_ VECTOR \_ 2F.<br/> Il valore predefinito è {1.0f, 1.0f}.<br/> |
| Scalemode<br/> D2D1 \_ POINTSPECOLARE \_ PROP SCALE \_ \_ MODE<br/>                 | Modalità di interpolazione utilizzata dall'effetto per ridimensionare l'immagine in base alla lunghezza di unità del kernel corrispondente. Esistono sei modalità di scalabilità che variano in qualità e velocità. Per [altre informazioni, vedere](#scales-modes) Modalità di ridimensionamento. <br/> Il tipo è D2D1 \_ POINTSPECOLA \_ SCALE \_ MODE.<br/> Il valore predefinito è D2D1 \_ POINTSPECOLA \_ SCALE \_ MODE \_ LINEAR.<br/>                                                                                                                          |



 

## <a name="scales-modes"></a>Scales modes (Modalità di ridimensionamento)



| Enumerazione                                             | Descrizione                                                                                                                                                                                          |
|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ POINTSPECOLARE \_ SCALE MODE NEAREST \_ \_ \_ NEIGHBOR     | Campioni il singolo punto più vicino e lo usa. Questa modalità usa meno tempo di elaborazione, ma restituisce l'immagine di qualità più bassa.                                                                           |
| PUNTI D2D1 \_ MODALITÀ SCALA \_ LINEARE \_ \_                | Usa un campione di quattro punti e l'interpolazione lineare. Questa modalità restituisce un'immagine di qualità superiore a quella del vicino più vicino.                                                                                   |
| D2D1 \_ POINTSPECOLARE \_ SCALE MODE \_ \_ CUBIC                 | Usa un kernel cubico di 16 campioni per l'interpolazione. Questa modalità usa la maggior parte del tempo di elaborazione, ma restituisce un'immagine di qualità superiore.                                                                        |
| D2D1 \_ POINTSPECOLARE \_ MODALITÀ \_ \_ \_ MULTI-CAMPIONE \_ LINEARE | Usa 4 campioni lineari all'interno di un singolo pixel per un anti-aliasing dei bordi valido. Questa modalità è buona per ridurre di piccole quantità le immagini con pochi pixel.                                              |
| D2D1 \_ POINTSPECOLARE \_ MODALITÀ SCALA \_ \_ ANISO STANDBY           | Usa il filtro anisotropo per campionare un criterio in base alla forma trasformata della bitmap.                                                                                                     |
| D2D1 \_ POINTSPECOLARE \_ SCALE MODE HIGH QUALITY \_ \_ \_ \_ CUBIC  | Usa un kernel cubico di qualità elevata di dimensioni variabili per eseguire una scalabilità pre-ridimensionata dell'immagine se la scalabilità è coinvolta nella matrice di trasformazione. Usa quindi la modalità di interpolazione cubica per l'output finale. |



 

> [!Note]  
> Se non si seleziona una modalità, l'effetto predefinito è D2D1 POINTSPECOLA SCALE MODE LINEAR ( D2D1 \_ POINTSPECOLA \_ SCALE \_ MODE \_ LINEAR).

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

 

