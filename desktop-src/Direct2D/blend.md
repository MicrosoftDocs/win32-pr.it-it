---
title: Effetto sfumatura
description: Usare l'effetto di fusione per combinare 2 immagini. Questo effetto ha 26 modalità di fusione.
ms.assetid: 39D8BAA3-8FF3-4F10-99A0-B26FCA3018AE
keywords:
- Effetto blend
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 853043123c6eea9a87656a7450b1295236ed5d6a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478197"
---
# <a name="blend-effect"></a>Effetto sfumatura

Usare l'effetto di fusione per combinare 2 immagini. Questo effetto ha 26 modalità di fusione.

Il CLSID per questo effetto è CLSID \_ D2D1Blend.

-   [Esempi di fusione](#blending-examples)
-   [Proprietà degli effetti](#effect-properties)
-   [Fusione](#blend-modes)
-   [Conversioni dello spazio colori HSL](#hsl-color-space-conversions)
    -   [Conversione da RGB a HSL](#converting-from-rgb-to-hsl)
    -   [Conversione da HSL a RGB](#converting-from-hsl-to-rgb)
-   [Bitmap di output](#output-bitmap)
-   [Codice di esempio](#sample-code)
-   [Requisiti](#requirements)
-   [Argomenti correlati](#related-topics)

## <a name="blending-examples"></a>Esempi di fusione

Ecco un'immagine di esempio di ogni modalità di fusione dell'effetto di fusione. Nella sezione successiva è riportato un elenco completo delle modalità di fusione e delle proprietà della modalità corrispondenti

![Screenshot di esempio dell'effetto di tutte le modalità di fusione disponibili.](images/blend-modes.png)

Ecco un altro esempio che usa la modalità di esclusione.



| Prima dell'immagine 1                                                             |
|----------------------------------------------------------------------------|
| ![prima dell'effetto.](images/default-before.jpg)    |
| Prima dell'immagine 2                                                             |
| ![la seconda immagine prima dell'effetto.](images/4-arthimetic-composite2.jpg) |
| After                                                                      |
| ![l'immagine dopo la trasformazione.](images/5-blend.png)                      |



 


```C++
ComPtr<ID2D1Effect> blendEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Blend, &blendEffect);

blendEffect->SetInput(0, bitmap);
blendEffect->SetInput(1, bitmapTwo);
blendEffect->SetValue(D2D1_BLEND_PROP_MODE, D2D1_BLEND_MODE_EXCLUSION);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(blendEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Proprietà degli effetti



| Nome visualizzato ed enumerazione dell'indice                 | Descrizione                                                                                                                                                                               |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Mode<br/> MODALITÀ BLEND PROP D2D1 \_ \_ \_<br/> | Modalità di fusione usata per l'effetto. Per [altre informazioni, vedere Modalità](#blend-modes) di fusione. Il tipo è D2D1 \_ BLEND \_ MODE.<br/> Il valore predefinito è D2D1 \_ BLEND \_ MODE \_ MULTIPLY.<br/> |



 

## <a name="blend-modes"></a>Fusione

La tabella seguente mostra tutte le modalità di fusione di questo effetto. Le funzioni helper necessarie per calcolare l'output dell'effetto sono disponibili nella sezione successiva.

Colore: O <sub>PRGB</sub>  =  *f*(F <sub>RGB,</sub>B <sub>RGB</sub>) \* F <sub>A</sub> \* B <sub>A</sub> + F <sub>RGB</sub> \* F <sub>A</sub> \* (1 - B <sub>A</sub>) + B <sub>RGB</sub> \* B <sub>A</sub> \* (1 - F <sub>A</sub>)

Alfa: O<sub>A</sub> = F<sub>A</sub> \* (1 - B<sub>A</sub>) + B<sub>A</sub>

Dove:

-   O<sub>PRGB</sub> è il colore di output pre-moltiplicato
-   O<sub>A è</sub> Alfa di output
-   B<sub>RGB</sub> è il colore di destinazione non moltiplicato
-   B<sub>A è</sub> il carattere alfa di destinazione
-   F<sub>RGB</sub> è il colore di origine non moltiplicato
-   F<sub>A è</sub> alfa di origine
-   *f*(S <sub>RGB,</sub>D <sub>RGB</sub>) è una funzione di blend che varia in base alla modalità di blend

Alcune modalità di fusione richiedono la conversione da e verso lo spazio colori di tonalità, saturazione, luminosità (HSL) in RGB.




| Enumerazione | Equazione | 
|-------------|----------|
| D2D1_BLEND_MODE_DARKEN | Formula di blend di base solo per alfa. <img src="images/blend-mode-darken-1.png" alt="mathematical formula for a darken effect." /> | 
| D2D1_BLEND_MODE_MULTIPLY | Formula di blend di base solo per alfa. <img src="images/blend-mode-multiply-1.png" alt="Mathematical formula for a mutiply effect." /> | 
| D2D1_BLEND_MODE_COLOR_BURN | Formule di blend di base <em>con f</em>(F<sub>RGB,</sub>B<sub>RGB</sub>) = <img src="images/blend-mode-colorburn-1.png" alt="Mathematical formula for a coor burn effect." /> | 
| D2D1_BLEND_MODE_LINEAR_BURN | Formule di blend di base <em>con f</em>(F<sub>RGB,</sub>B<sub>RGB</sub>) = <img src="images/blend-mode-linearburn-1.png" alt="Mathematical formula for a linear burn effect." /> | 
| D2D1_BLEND_MODE_DARKER_COLOR | Formula di blend di base solo per alfa. <img src="images/blend-mode-darkencolor-1.png" alt="Mathematical formla for a darken color effect." /> | 
| D2D1_BLEND_MODE_LIGHTEN | Formula di blend di base solo per alfa. <img src="images/blend-mode-lighten-1.png" alt="Mathematical formula for a lighten effect." /> | 
| D2D1_BLEND_MODE_SCREEN | Formula di blend di base solo per alfa. <img src="images/blend-mode-screen-1.png" alt="Mathematical formula for a screen effect." /> | 
| D2D1_BLEND_MODE_COLOR_DODGE | Formule di blend di base <em>con f</em>(F<sub>RGB,</sub>B<sub>RGB</sub>) = <img src="images/blend-mode-colordodge-1.png" alt="Mathematical formula for a color dodge effect." /> | 
| D2D1_BLEND_MODE_LINEAR_DODGE | Formule di blend di base <em>con f</em>(F<sub>RGB,</sub>B<sub>RGB</sub>) = <img src="images/blend-mode-lineardodge-1.png" alt="Mathematical formula for a linear dodge effect." /> | 
| D2D1_BLEND_MODE_LIGHTER_COLOR | Formula di blend di base solo per alfa. <img src="images/blend-mode-lightercolor-1.png" alt="Mathematical formula for a lighter color effect." /> | 
| D2D1_BLEND_MODE_OVERLAY | Formule di blend di base <em>con f</em>(F<sub>RGB,</sub>B<sub>RGB</sub>) = <img src="images/blend-mode-overlay-1.png" alt="Mathematical formula for an overlay effect." /> | 
| D2D1_BLEND_MODE_SOFT_LIGHT | Formule di blend di base <em>con f</em>(F<sub>RGB,</sub>B<sub>RGB</sub>) = <img src="images/blend-mode-softlight-1.png" alt="Mathematical formula for a soft light effect." /> | 
| D2D1_BLEND_MODE_HARD_LIGHT | Formule di blend di base <em>con f</em>(F<sub>RGB,</sub>B<sub>RGB</sub>) = <img src="images/blend-mode-hardlight-1.png" alt="Mathematical formula for a hard light effect." /> | 
| D2D1_BLEND_MODE_VIVID_LIGHT | Formule di blend di base <em>con f</em>(F<sub>RGB,</sub>B<sub>RGB</sub>) = <img src="images/blend-mode-vividlight-1.png" alt="Mathematical formula for a vivid light effect." /> | 
| D2D1_BLEND_MODE_LINEAR_LIGHT | Formule di blend di base <em>con f</em>(F<sub>RGB,</sub>B<sub>RGB</sub>) = <img src="images/blend-mode-linearlight-1.png" alt="Mathematical formula for a linear light effect." /> | 
| D2D1_BLEND_MODE_PIN_LIGHT | Formule di blend di base <em>con f</em>(F<sub>RGB,</sub>B<sub>RGB</sub>) = <img src="images/blend-mode-pinlight-1.png" alt="Mathematical formula for a pin light effect." /> | 
| D2D1_BLEND_MODE_HARD_MIX | Formule di blend di base <em>con f</em>(F<sub>RGB,</sub>B<sub>RGB</sub>) = <img src="images/blend-mode-hardmix-1.png" alt="Mathematical formula for a hard mix effect." /> | 
| D2D1_BLEND_MODE_DIFFERENCE | Formule di blend di base <em>con f</em>(F<sub>RGB,</sub>B<sub>RGB</sub>) = abs(F<sub>RGB</sub> - B<sub>RGB</sub>) | 
| D2D1_BLEND_MODE_EXCLUSION | Formule di blend di base <em>con f</em>(F<sub>RGB,</sub>B<sub>RGB</sub>) = F<sub>RGB</sub> + B<sub>RGB</sub>   2 * F<sub>RGB</sub> * B<sub>RGB</sub> | 
| D2D1_BLEND_MODE_HUE | Formula di blend di base solo per alfa. <img src="images/blend-mode-hue-1.png" alt="Mathematical formula for a hue blend effect." /> | 
| D2D1_BLEND_MODE_SATURATION | Formula di blend di base solo per alfa. <img src="images/blend-mode-saturation-1.png" alt="Mathematical formula for a sturation blend effect." /> | 
| D2D1_BLEND_MODE_COLOR | Formula di blend di base solo per alfa. <img src="images/blend-mode-color-1.png" alt="Mathematical formula for a color blend effect." /> | 
| D2D1_BLEND_MODE_LUMINOSITY | Formula di blend di base solo per alfa. <img src="images/blend-mode-luminosity-1.png" alt="Mathematical formula for a luminosity blend effect." /> | 
| D2D1_BLEND_MODE_DISSOLVE | Si consideri quanto segue:<ul><li>Coordinata XY della scena per il pixel corrente</li><li>Generatore di numeri pseudo-casuali deterministico rand(XY) basato sulla coordinata di seed XY, con distribuzione imparziale dei valori da [0, 1]</li></ul><br /><img src="images/blend-mode-dissolve-1.png" alt="Mathematical formula for a dissolve blend effect." /><br /> | 
| D2D1_BLEND_MODE_SUBTRACT | Formula di blend di base solo per alfa. <img src="images/blend-mode-subtract-1.png" alt="Mathematical formula for a subtract blend effect." /> | 
| D2D1_BLEND_MODE_DIVISION | Formula di blend di base solo per alfa. <img src="images/blend-mode-division-1.png" alt="Mathematical formula for a division blend effect." /> | 




 

> [!Note]  
> Per tutte le modalità blend, il valore di output è premoltimulliato e impostato sull'intervallo \[ 0, \] 1.

 

## <a name="hsl-color-space-conversions"></a>Conversioni dello spazio colori HSL

Il componente luminosità viene calcolato usando i pesi RGB qui:

-   *k*<sub>R</sub> = 0,30
-   *k*<sub>G</sub> = 0,59
-   *k*<sub>B</sub> = 0,11

### <a name="converting-from-rgb-to-hsl"></a>Conversione da RGB a HSL

![formula matematica che descrive la trasformazione dal colore rgb al colore hsl.](images/blend-rgb-to-hsl-1.png)

In questo *modo S* e *L vengono* posti nell'intervallo \[ 0.0, 1.0 \] e *H* nell'intervallo \[ -1.0, 5.0 \] .

### <a name="converting-from-hsl-to-rgb"></a>Conversione da HSL a RGB

Per convertire l'altro modo si usa l'inverso dei calcoli precedenti.

Se *S* = 0, *R*  =  *G*  =  *B*  =  *L*

In caso contrario, sono presenti sei casi dipendenti dalla tonalità:

Se *H* è maggiore di 0, i valori si trova nel settore rosso/magenta in cui *R*  >  *B*  >  *G*.

![passaggio matematico dell'equaiton uno dei sei che convertono il colore hsl in rgb.](images/blend-hsl-to-rgb-1rm.png)

Se *H* è maggiore o uguale a 0 e minore di 1, i valori sono nel settore rosso/giallo dove *R*  >  *G*  >  *B*.

![matematico equaiton passaggio 2 di sei conversione del colore hsl in rgb.](images/blend-hsl-to-rgb-1ry.png)

Se *H* è maggiore o uguale a 1 e minore di 2, i valori sono nel settore giallo/verde dove *G*  >  *R*  >  *B*.

![matematico equaiton passaggio 3 di sei conversione del colore hsl in rgb.](images/blend-hsl-to-rgb-1yg.png)

Se *H* è maggiore o uguale a 2 e minore di 3, i valori sono nel settore verde/ciano dove *G*  >  *B*  >  *R*.

![matematico equaiton passaggio quattro di sei convertendo il colore hsl in rgb.](images/blend-hsl-to-rgb-1gc.png)

Se *H* è maggiore o uguale a 3 e minore di 4, i valori sono nel settore ciano/blu dove *B*  >  *G*  >  *R*.

![matematico equaiton passaggio 5 di sei conversione del colore hsl in rgb.](images/blend-hsl-to-rgb-1cb.png)

Se *H* è maggiore o uguale a 4, i valori sono nel settore blu/magenta in cui *B*  >  *R*  >  *G*.

![matematico equaiton passaggio sei di sei conversione del colore hsl in rgb.](images/blend-hsl-to-rgb-1bm.png)

Poiché le modalità di fusione fanno combinazioni arbitrarie di componenti HSL di due colori diversi, è comune che il valore RGB convertito non sia disponibile nella gamma, ad esempio uno o più componenti del canale potrebbero non rientrare nell'intervallo valido \[ di 0,0, 1,0 \] . Questi colori vengono riattivati riducendo al minimo la saturazione, mantenendo sia la tonalità che la luminosità:

![formula matematica che descrive le correzioni necessarie per le istanze fuori gamma.](images/blend-gamut-correction.png)

## <a name="output-bitmap"></a>Bitmap di output

La bitmap di output per questo effetto è sempre la dimensione dell'unione delle due immagini di input.

## <a name="sample-code"></a>Codice di esempio

Per un esempio di questo effetto, scaricare l'esempio [di modalità effetto composito Direct2D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20composite%20effect%20modes%20sample).

## <a name="requirements"></a>Requisiti



| Requisito | valore |
|--------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato | Windows 8 e l'aggiornamento della piattaforma Windows 7 \[ app desktop \| Windows Store\] |
| Server minimo supportato | Windows 8 e l'aggiornamento della piattaforma Windows 7 \[ app desktop \| Windows Store\] |
| Intestazione                   | d2d1effects.h                                                                      |
| Libreria                  | d2d1.lib, dxguid.lib                                                               |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

