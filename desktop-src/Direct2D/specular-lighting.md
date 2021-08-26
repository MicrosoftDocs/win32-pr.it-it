---
title: Effetto di illuminazione con luce riflettore speculare
description: Usare l'effetto di illuminazione speculare spot per creare un'immagine che sembra essere una superficie riflettente in cui la sorgente di luce è limitata a un cono di luce diretto.
ms.assetid: B6E24036-1548-4B9E-A8FE-8B87D4DBF97A
keywords:
- illuminazione speculare spot
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9edc4c75eaa17369ba0d0d9f1838d8857053def9aaab3dacceb8bf761b9c04c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120000376"
---
# <a name="spot-specular-lighting-effect"></a>Effetto di illuminazione con luce riflettore speculare

Usare l'effetto di illuminazione speculare spot per creare un'immagine che sembra essere una superficie riflettente in cui la sorgente di luce è limitata a un cono di luce diretto. Questo effetto usa il canale alfa come mappa di altezza e illumina l'immagine con una sorgente di luce punto.

Il colore della bitmap di output è il risultato di colore chiaro, posizione della luce, direzione del cono e geometria della superficie in base alla parte speculare del modello di illuminazione Phong. L'output del canale alfa per ogni pixel con illuminazione speculare è il massimo degli output dei canali rosso, verde e blu per tale pixel.

Il CLSID per questo effetto è CLSID \_ D2D1SpotSpecular.

-   [Immagine di esempio](#example-image)
-   [Sorgente di luce spot](#spot-light-source)
-   [Proprietà degli effetti](#effect-properties)
-   [Modalità di scalabilità](#scale-modes)
-   [Requisiti](#requirements)
-   [Argomenti correlati](#related-topics)

## <a name="example-image"></a>Immagine di esempio

L'esempio seguente mostra le immagini di input e output dell'effetto di illuminazione speculare spot.

![Screenshot di esempio dell'effetto.](images/spot-spec-example.png)

La luce speculare si riferisce alla luce riflessa in una particolare direzione.

![diagramma dei vettori usati per ottenere un output di illuminazione speculare per una bitmap.](images/point-spec-reflected1.png)

L'effetto calcola i valori in pixel di output finali usando le equazioni seguenti:

![equazioni di pixel di output.](images/spot-formula1.png)

dove

![definizioni di variabili.](images/spot-formula2.png)

## <a name="spot-light-source"></a>Sorgente di luce spot

Una sorgente di luce spot emette luce in un cono in una direzione specifica e non emette luce all'esterno del cono.

La sorgente di luce spot calcola il vettore di luce L e il vettore a metà strada H allo stesso modo [dell'effetto speculare punto.](point-specular.md)

L'effetto calcola il colore chiaro, L<sub>r</sub>, L<sub>g</sub>, L<sub>b</sub>, come funzione della posizione della sorgente di luce, come illustrato con le equazioni seguenti:

![equazione per la sorgente di luce spot](images/spot-formula3.png)

Vettore ![simbolo di vettore chiaro.](images/spot-mathchar-l.png) è definito da queste equazioni:

![equazione: vector](images/spot-formula4.png)

Vettore ![Simbolo di vettore t](images/spot-mathchar-t.png) è definito da queste equazioni:

![equazione: vettore 2](images/spot-formula5.png)

## <a name="effect-properties"></a>Proprietà degli effetti



| Enumerazione del nome visualizzato e dell'indice                                                        | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LightPosition<br/> PUNTI \_ D2D1SOCIEZIONE \_ DELLA LUCE DELLA PROPRIETÀ \_ D2D1 \_<br/>             | Posizione di luce della sorgente di luce punto. La proprietà è un vector 3F D2D1 \_ \_ definito come (x, y, z). Le unità sono espresse in DIP (Device Independent Pixel) e non sono debounded. Il tipo è D2D1 \_ VECTOR \_ 3F.<br/> Il valore predefinito è {0.0f, 0.0f, 0.0f}.<br/>                                                                                                                                                                                                              |
| Punti A<br/> PUNTI \_ D2D1PECOLARE \_ PROP PUNTA \_ \_ A<br/>                       | Posizione in cui è concentrata la luce spot. La proprietà viene esposta come vector 3F D2D1 \_ \_ con (x, y, z). Le unità sono in DIP e i valori non sono associati. Il tipo è D2D1 \_ VECTOR \_ 3F.<br/> Il valore predefinito è {0.0f, 0.0f, 0.0f}.<br/>                                                                                                                                                                                                                                     |
| Focus<br/> PUNTI D2D1 \_ FOCUS DELLA PROPRIETÀ DI \_ \_ BASE<br/>                               | Stato attivo della luce spot. Questa proprietà è senza unità ed è definita tra 0 e 200. Il tipo è FLOAT.<br/> Il valore predefinito è 1,0f.<br/>                                                                                                                                                                                                                                                                                                                          |
| LimitingConeAngle<br/> D2D1 \_ SPOT \_ SPECULAR \_ PROP \_ LIMITING \_ CONE \_ ANGLE<br/> | Angolo del cono che limita l'area in cui viene proiettata la luce. Non viene proiettata alcuna luce all'esterno del cono. L'angolo del cono limitante è l'angolo tra l'asse della luce spot (l'asse tra le proprietà *LightPosition* e *PointsAt)* e il cono di luce spot. Questa proprietà è definita in gradi e deve essere compresa tra 0 e 90 gradi. Il tipo è FLOAT.<br/> Il valore predefinito è 90,0f.<br/>                                                               |
| SpecularExponent<br/> PUNTI D2D1 \_ \_ ESPONENTE \_ SPECULARE DELLA PROPRIETÀ \_ SPECULARE<br/>       | Esponente per il termine speculare nell'equazione di illuminazione phong. Un valore più grande corrisponde a una superficie più riflettente. Questo valore è senza unità e deve essere compreso tra 1,0 e 128. Il tipo è FLOAT.<br/> Il valore predefinito è 1,0f.<br/>                                                                                                                                                                                                                               |
| SpecularConstant<br/> D2D1 \_ SPOTSPEULAR \_ PROP \_ SPECULAR \_ CONSTANT<br/>       | Rapporto tra la reflection speculare e la luce in ingresso. Il valore è senza unità e deve essere compreso tra 0 e 10.000. Il tipo è FLOAT.<br/> Il valore predefinito è 1,0f.<br/>                                                                                                                                                                                                                                                                                                   |
| SurfaceScale<br/> PUNTI \_ D2D1RIQUADARE \_ DELLA SUPERFICIE DELLA PROPRIETÀ DI \_ \_ RIFERIMENTO<br/>               | Fattore di scala nella direzione Z per la generazione di una mappa di altezza. Il valore è senza unità e deve essere compreso tra 0 e 10.000. Il tipo è FLOAT.<br/> Il valore predefinito è 1,0f.<br/>                                                                                                                                                                                                                                                                                          |
| Color<br/> PUNTI D2D1 \_ COLORE DELLA PROPRIETÀ DI \_ \_ BASE<br/>                               | Colore della luce in ingresso. Questa proprietà viene esposta come Vector 3 (R, G, B) e usata per calcolare L<sub>R</sub>, L<sub>G</sub>, L<sub>B</sub>. Il tipo è D2D1 \_ VECTOR \_ 3F.<br/> Il valore predefinito è {1.0f, 1.0f, 1.0f}.<br/>                                                                                                                                                                                                                                     |
| KernelUnitLength<br/> PUNTI D2D1 \_ LUNGHEZZE UNITÀ \_ KERNEL DELLA \_ PROPRIETÀ \_ \_ DEL KERNEL<br/>     | Dimensione di un elemento nel kernel Sobel usata per generare la normale della superficie nella direzione X e Y. Questa proprietà esegue il mapping ai valori dx e dy nella sfumatura Sobel. Questa proprietà è D2D1 \_ VECTOR \_ 2F (Kernel Unit Length X, Kernel Unit Length Y) ed è definita in (DIP/Unità kernel). L'effetto usa l'interpolazione bilineare per ridimensionare la bitmap in modo che corrisponda alle dimensioni degli elementi del kernel. Il tipo è D2D1 \_ VECTOR \_ 2F.<br/> Il valore predefinito è {1.0f, 1.0f}.<br/> |
| Scalemode<br/> PUNTI D2D1PROP \_ \_ SCALE MODE (MODALITÀ DI \_ SCALA DELLE PROPRIETÀ DI \_ BASE)<br/>                     | Modalità di interpolazione utilizzata dall'effetto per ridimensionare l'immagine in base alla lunghezza di unità del kernel corrispondente. Esistono sei modalità di scalabilità che variano in qualità e velocità. Per [altre informazioni, vedere](#scale-modes) Modalità di ridimensionamento. <br/> Il tipo è D2D1 \_ SPOTSPECOLA \_ SCALE \_ MODE.<br/> Il valore predefinito è D2D1 \_ SPOTSPECOLA \_ SCALE \_ MODE \_ LINEAR.<br/>                                                                                                                             |



 

## <a name="scale-modes"></a>Modalità di scalabilità



| Enumerazione                                            | Descrizione                                                                                                                                                                                          |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PUNTI \_ D2D1QUADRO VICINO PIÙ VICINO ALLA MODALITÀ SCALA \_ DELLA \_ \_ \_ MAPPA     | Campioni il singolo punto più vicino e lo usa. Questa modalità usa meno tempo di elaborazione, ma restituisce l'immagine di qualità più bassa.                                                                           |
| PUNTI D2D1 \_ MODALITÀ \_ DI SCALA \_ LINEARE \_                | Usa un campione di quattro punti e l'interpolazione lineare. Questa modalità restituisce un'immagine di qualità superiore a quella del vicino più vicino.                                                                                   |
| PUNTI D2D1 \_ MODALITÀ \_ DI SCALA \_ \_ CUBICA                 | Usa un kernel cubico di 16 campioni per l'interpolazione. Questa modalità usa la maggior parte del tempo di elaborazione, ma restituisce un'immagine di qualità superiore.                                                                        |
| PUNTI D2D1 \_ LINEARI \_ MULTI-CAMPIONE IN MODALITÀ \_ \_ SCALA \_ \_ STANDARD | Usa 4 campioni lineari all'interno di un singolo pixel per un anti-aliasing dei bordi valido. Questa modalità è buona per ridurre di piccole quantità le immagini con pochi pixel.                                              |
| D2D1 \_ SPOTSPECOLARE \_ SCALE MODE \_ \_ ANISO STANDBY           | Usa un filtro anisotropo per campionare un criterio in base alla forma trasformata della bitmap.                                                                                                     |
| PUNTI \_ D2D1QUADRE \_ CUBICA \_ DI ALTA QUALITÀ IN MODALITÀ SCALA \_ \_ \_ STANDARD  | Usa un kernel cubico di alta qualità di dimensioni variabili per eseguire una scalabilità pre-ridimensionata dell'immagine se la scalabilità è coinvolta nella matrice di trasformazione. Usa quindi la modalità di interpolazione cubica per l'output finale. |



 

> [!Note]  
> Se non si seleziona una modalità, per impostazione predefinita l'effetto è D2D1 \_ SPOTSPE LINEAR \_ SCALE MODE \_ \_ (SCALA LINEARE).

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

 

