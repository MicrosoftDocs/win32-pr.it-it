---
title: Effetto di illuminazione speculare a distanza
description: Usare l'effetto di illuminazione speculare distanti per creare un'immagine che sembra essere una superficie riflettente in cui la sorgente di luce sembra essere proveniente da una lunga distanza (ad esempio il sole o le luci di sovraccarico).
ms.assetid: 74D71A2D-8D1D-4FDE-898A-2D2F5A8D5D31
keywords:
- illuminazione speculare distante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a02bbf6e928691f88de3adc41fc3ae84cbc1e7df69b3b5998ca903a7556d29d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119768851"
---
# <a name="distant-specular-lighting-effect"></a>Effetto di illuminazione speculare a distanza

Usare l'effetto di illuminazione speculare distanti per creare un'immagine che sembra essere una superficie riflettente in cui la sorgente di luce sembra essere proveniente da una lunga distanza (ad esempio il sole o le luci di sovraccarico). Questo effetto usa il canale alfa come mappa di altezza e illumina l'immagine con una sorgente di luce distante.

Il colore della bitmap di output è il risultato di colore chiaro, posizione della luce e geometria della superficie. L'output del canale alfa per ogni pixel con illuminazione speculare è il massimo degli output dei canali rosso, verde e blu per tale pixel.

Il CLSID per questo effetto è CLSID \_ D2D1DistantSpecular.

-   [Immagine di esempio](#example-image)
-   [Sorgente di luce distante](#distant-light-source)
-   [Proprietà degli effetti](#effect-properties)
-   [Modalità di scalabilità](#scale-modes)
-   [Requisiti](#requirements)
-   [Argomenti correlati](#related-topics)

## <a name="example-image"></a>Immagine di esempio

L'esempio seguente mostra le immagini di input e output dell'effetto di illuminazione speculare distante.

![Screenshot di esempio dell'effetto che mostra le immagini di input e output dell'effetto di illuminazione speculare distante. ](images/distant-spec-example.png)

La bitmap di output finale può essere calcolata usando le equazioni seguenti.

![Calcolo bitmap di output](images/distant-spec-formula1.png)

dove <dl> K? = costante di illuminazione speculare.  
![simbolo normale della superficie. ](images/point-spec-mathchar-n.png) = vettore di unità normale della superficie.  
![simbolo di vettore a metà. ](images/point-spec-mathchar-h.png) = vettore di unità "a metà" tra vettore di unità oculare e vettore di unità di luce.  
C<sub>r</sub>, C<sub>g</sub>, C<sub>b</sub> = il colore chiaro nei componenti RGB.  
</dl>

## <a name="distant-light-source"></a>Sorgente di luce distante

L'immagine mostra un esempio della direzione della luce da una sorgente di luce distante.

![fonte di luce distante](images/distant-spec-lightsource.png)

L'effetto usa i parametri azimuth e elevation per calcolare il vettore di luce ![Vettore l.](images/distant-spec-mathchar-l.png) usando le equazioni seguenti:

![calcolo del vettore di luce](images/distant-spec-formula2.png)

dove Light?, Light<sub>y e</sub>Light<sub>z</sub> sono i valori di posizione della luce di input.

## <a name="effect-properties"></a>Proprietà degli effetti



| Enumerazione del nome visualizzato e dell'indice                                                       | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Azimuth<br/> D2D1 \_ DISTANTSPECULAR \_ PROP \_ AZIMUTH<br/>                       | Angolo di direzione della sorgente di luce nel piano XY rispetto all'asse X nella direzione del clock del contatore. Le unità sono in gradi e devono essere compresi tra 0 e 360 gradi.<br/> Il tipo è FLOAT.<br/> Il valore predefinito è 0,0f.<br/>                                                                                                                                                                              |
| Altitudine<br/> D2D1 \_ DISTANTSPECULAR \_ PROP \_ ELEVATION<br/>                   | Angolo di direzione della sorgente di luce nel piano YZ rispetto all'asse Y nella direzione del clock del contatore. Le unità sono in gradi e devono essere compresi tra 0 e 360 gradi. <br/> Il tipo è FLOAT.<br/> Il valore predefinito è 0,0f.<br/>                                                                                                                                                                             |
| SpecularExponent<br/> D2D1 \_ DISTANTSPECULAR \_ PROP \_ SPECULAR \_ EXPONENT<br/>   | Esponente per il termine speculare nell'equazione di illuminazione phong. Un valore più grande corrisponde a una superficie più riflettente. Il valore è senza unità e deve essere compreso tra 1,0 e 128. Il tipo è FLOAT.<br/> Il valore predefinito è 1,0f.<br/>                                                                                                                                                                                          |
| SpecularConstant<br/> COSTANTE \_ \_ SPECULARE DELLA PROPRIETÀ D2D1 DISTANTSPECULAR \_ \_<br/>   | Rapporto tra la reflection speculare e la luce in ingresso. Il valore è senza unità e deve essere compreso tra 0 e 10.000. Il tipo è FLOAT.<br/> Il valore predefinito è 1,0f.<br/>                                                                                                                                                                                                                                                             |
| SurfaceScale<br/> D2D1 \_ DISTANTSPECULAR \_ PROP \_ SURFACE \_ SCALE<br/>           | Fattore di scala nella direzione Z. Il valore è senza unità e deve essere compreso tra 0 e 10.000. Il tipo è FLOAT.<br/> Il valore predefinito è 1,0f.<br/>                                                                                                                                                                                                                                                                                |
| Color<br/> D2D1 \_ DISTANTSPECULAR \_ PROP \_ COLOR<br/>                           | Colore della luce in ingresso. Questa proprietà viene esposta come D2D1 \_ VECTOR \_ 3F (R, G,<sub></sub>B)<sub></sub>e usata per calcolare L<sub>R</sub>, L G , L B . Il tipo è D2D1 \_ VECTOR \_ 3F.<br/> Il valore predefinito è {1.0f, 1.0f, 1.0f}.<br/>                                                                                                                                                                                       |
| KernelUnitLength<br/> D2D1 \_ DISTANTSPECULAR \_ PROP \_ KERNEL \_ UNIT \_ LENGTH<br/> | Dimensione di un elemento nel kernel Sobel usata per generare la normale della superficie nella direzione X e Y. Questa proprietà è D2D1 \_ VECTOR \_ 2F (Kernel Unit Length X, Kernel Unit Length Y) ed è definita in (DIP(Device-Independent Pixel)/Kernel Unit). L'effetto usa l'interpolazione bilineare per ridimensionare la bitmap in modo che corrisponda alle dimensioni degli elementi del kernel. Il tipo è D2D1 \_ VECTOR \_ 2F.<br/> Il valore predefinito è {1.0f, 1.0f}.<br/> |
| Scalemode<br/> D2D1 \_ DISTANTSPECULAR \_ PROP \_ SCALE \_ MODE<br/>                 | Modalità di interpolazione utilizzata dall'effetto per ridimensionare l'immagine in base alla lunghezza di unità del kernel corrispondente. Esistono sei modalità di scalabilità che variano in qualità e velocità.<br/> Il tipo è D2D1 \_ DISTANTSPECULAR \_ SCALE \_ MODE.<br/> Il valore predefinito è D2D1 \_ DISTANTSPECULAR \_ SCALE \_ MODE \_ LINEAR.<br/>                                                                                                                                 |



 

## <a name="scale-modes"></a>Modalità di scalabilità



| Enumerazione                                               | Descrizione                                                                                                                                                                                          |
|-----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ DISTANTSPECULAR \_ SCALE \_ MODE \_ NEAREST \_ NEIGHBOR     | Campioni il singolo punto più vicino e lo usa. Questa modalità usa meno tempo di elaborazione, ma restituisce l'immagine di qualità più bassa.                                                                           |
| D2D1 \_ DISTANTSPECULAR \_ SCALE \_ MODE \_ LINEAR                | Usa un campione di quattro punti e l'interpolazione lineare. Questa modalità restituisce un'immagine di qualità superiore a quella del vicino più vicino.                                                                                   |
| D2D1 \_ DISTANTSPECULAR \_ SCALE \_ MODE \_ CUBIC                 | Usa un kernel cubico di 16 campioni per l'interpolazione. Questa modalità usa la maggior parte del tempo di elaborazione, ma restituisce un'immagine di qualità superiore.                                                                        |
| D2D1 \_ DISTANTSPECULAR \_ SCALE \_ MODE \_ MULTI \_ SAMPLE \_ LINEAR | Usa 4 campioni lineari all'interno di un singolo pixel per un anti-aliasing dei bordi valido. Questa modalità è buona per ridurre di piccole quantità le immagini con pochi pixel.                                              |
| D2D1 \_ DISTANTSPECULAR \_ SCALE MODE \_ \_ ANISO STANDBY           | Usa un filtro anisotropo per campionare un criterio in base alla forma trasformata della bitmap.                                                                                                     |
| D2D1 \_ DISTANTSPECULAR \_ SCALE \_ MODE \_ HIGH \_ QUALITY \_ CUBIC  | Usa un kernel cubico di alta qualità di dimensioni variabili per eseguire una scalabilità pre-ridimensionata dell'immagine se la scalabilità è coinvolta nella matrice di trasformazione. Usa quindi la modalità di interpolazione cubica per l'output finale. |



 

> [!Note]  
> Se non si seleziona una modalità, l'effetto predefinito è D2D1 \_ DISTANTSPECULAR \_ SCALE \_ MODE \_ LINEAR.

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

 

