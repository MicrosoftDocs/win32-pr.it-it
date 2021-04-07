---
title: Effetto sfumatura
description: Usare l'effetto Blend per combinare 2 immagini. Questo effetto presenta 26 modalità di Blend.
ms.assetid: 39D8BAA3-8FF3-4F10-99A0-B26FCA3018AE
keywords:
- effetto Blend
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e248d1f7f41721d173510b8d10feac9be2e08f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874470"
---
# <a name="blend-effect"></a>Effetto sfumatura

Usare l'effetto Blend per combinare 2 immagini. Questo effetto presenta 26 modalità di Blend.

Il CLSID per questo effetto è CLSID \_ D2D1Blend.

-   [Esempi di fusione](#blending-examples)
-   [Proprietà effetto](#effect-properties)
-   [Modalità di Blend](#blend-modes)
-   [Conversioni dello spazio dei colori HSL](#hsl-color-space-conversions)
    -   [Conversione da RGB a HSL](#converting-from-rgb-to-hsl)
    -   [Conversione da HSL a RGB](#converting-from-hsl-to-rgb)
-   [Bitmap di output](#output-bitmap)
-   [Codice di esempio](#sample-code)
-   [Requisiti](#requirements)
-   [Argomenti correlati](#related-topics)

## <a name="blending-examples"></a>Esempi di fusione

Ecco un'immagine di esempio di ogni modalità di Blend dell'effetto Blend. Un elenco completo delle modalità di Blend e delle proprietà della modalità corrispondenti si trova nella sezione successiva

![schermata di esempio effetto di tutte le modalità di Blend disponibili.](images/blend-modes.png)

Di seguito è riportato un altro esempio che usa la modalità di esclusione.



| Prima dell'immagine 1                                                             |
|----------------------------------------------------------------------------|
| ![prima immagine di origine prima dell'effetto.](images/default-before.jpg)    |
| Prima dell'immagine 2                                                             |
| ![seconda immagine prima dell'effetto.](images/4-arthimetic-composite2.jpg) |
| After                                                                      |
| ![immagine dopo la trasformazione.](images/5-blend.png)                      |



 


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



## <a name="effect-properties"></a>Proprietà effetto



| Nome visualizzato e enumerazione dell'indice                 | Descrizione                                                                                                                                                                               |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Mode<br/> \_ \_ Modalità prop di Blend d2d1 \_<br/> | Modalità di Blend utilizzata per l'effetto. Per altre informazioni, vedere [modalità di Blend](#blend-modes) . Il tipo è D2D1 \_ Blend \_ mode.<br/> Il valore predefinito è D2D1 \_ Blend \_ mode \_ Multiply.<br/> |



 

## <a name="blend-modes"></a>Modalità di Blend

La tabella seguente mostra tutte le modalità di combinazione di questo effetto. Le funzioni di supporto necessarie per calcolare l'output dell'effetto sono disponibili nella sezione successiva.

Colore: O <sub>PRGB</sub>  =  *f*(f <sub>RGB</sub>, B <sub>RGB</sub>) \* f <sub>a</sub> \* B <sub>a</sub> + f <sub>RGB</sub> \* f <sub>a</sub> \* (1-B <sub>a</sub>) + b <sub>RGB</sub> \* b <sub>a</sub> \* (1-f <sub>a</sub>)

Alfa: O<sub>a</sub> = F<sub>a</sub> \* (1-b<sub>a</sub>) + B<sub>a</sub>

Dove:

-   O<sub>PRGB</sub> è il colore di output pre-moltiplicato
-   O<sub>A è l'</sub> output alfa
-   B<sub>RGB</sub> è il colore di destinazione non pre-moltiplicato
-   B<sub>A</sub> è Alpha di destinazione
-   F<sub>RGB</sub> è il colore di origine non pre-moltiplicato
-   F<sub>A è un Alpha di</sub> origine
-   *f*(S <sub>RGB</sub>, D <sub>RGB</sub>) è una funzione Blend che varia in base alla modalità per Blend

Per alcune delle modalità di Blend è necessario eseguire la conversione da e verso lo spazio dei colori Hue, Saturation, luminosità (HSL) in RGB.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Enumerazione</th>
<th>Equazione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D2D1_BLEND_MODE_DARKEN</td>
<td>Formula di Blend di base solo per Alpha. <img src="images/blend-mode-darken-1.png" alt="mathematical formula for a darken effect." /></td>
</tr>
<tr class="even">
<td>D2D1_BLEND_MODE_MULTIPLY</td>
<td>Formula di Blend di base solo per Alpha. <img src="images/blend-mode-multiply-1.png" alt="Mathematical formula for a mutiply effect." /></td>
</tr>
<tr class="odd">
<td>D2D1_BLEND_MODE_COLOR_BURN</td>
<td>Formule di Blend di base con <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) = <img src="images/blend-mode-colorburn-1.png" alt="Mathematical formula for a coor burn effect." /></td>
</tr>
<tr class="even">
<td>D2D1_BLEND_MODE_LINEAR_BURN</td>
<td>Formule di Blend di base con <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) = <img src="images/blend-mode-linearburn-1.png" alt="Mathematical formula for a linear burn effect." /></td>
</tr>
<tr class="odd">
<td>D2D1_BLEND_MODE_DARKER_COLOR</td>
<td>Formula di Blend di base solo per Alpha. <img src="images/blend-mode-darkencolor-1.png" alt="Mathematical formla for a darken color effect." /></td>
</tr>
<tr class="even">
<td>D2D1_BLEND_MODE_LIGHTEN</td>
<td>Formula di Blend di base solo per Alpha. <img src="images/blend-mode-lighten-1.png" alt="Mathematical formula for a lighten effect." /></td>
</tr>
<tr class="odd">
<td>D2D1_BLEND_MODE_SCREEN</td>
<td>Formula di Blend di base solo per Alpha. <img src="images/blend-mode-screen-1.png" alt="Mathematical formula for a screen effect." /></td>
</tr>
<tr class="even">
<td>D2D1_BLEND_MODE_COLOR_DODGE</td>
<td>Formule di Blend di base con <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) = <img src="images/blend-mode-colordodge-1.png" alt="Mathematical formula for a color dodge effect." /></td>
</tr>
<tr class="odd">
<td>D2D1_BLEND_MODE_LINEAR_DODGE</td>
<td>Formule di Blend di base con <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) = <img src="images/blend-mode-lineardodge-1.png" alt="Mathematical formula for a linear dodge effect." /></td>
</tr>
<tr class="even">
<td>D2D1_BLEND_MODE_LIGHTER_COLOR</td>
<td>Formula di Blend di base solo per Alpha. <img src="images/blend-mode-lightercolor-1.png" alt="Mathematical formula for a lighter color effect." /></td>
</tr>
<tr class="odd">
<td>D2D1_BLEND_MODE_OVERLAY</td>
<td>Formule di Blend di base con <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) = <img src="images/blend-mode-overlay-1.png" alt="Mathematical formula for an overlay effect." /></td>
</tr>
<tr class="even">
<td>D2D1_BLEND_MODE_SOFT_LIGHT</td>
<td>Formule di Blend di base con <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) = <img src="images/blend-mode-softlight-1.png" alt="Mathematical formula for a soft light effect." /></td>
</tr>
<tr class="odd">
<td>D2D1_BLEND_MODE_HARD_LIGHT</td>
<td>Formule di Blend di base con <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) = <img src="images/blend-mode-hardlight-1.png" alt="Mathematical formula for a hard light effect." /></td>
</tr>
<tr class="even">
<td>D2D1_BLEND_MODE_VIVID_LIGHT</td>
<td>Formule di Blend di base con <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) = <img src="images/blend-mode-vividlight-1.png" alt="Mathematical formula for a vivid light effect." /></td>
</tr>
<tr class="odd">
<td>D2D1_BLEND_MODE_LINEAR_LIGHT</td>
<td>Formule di Blend di base con <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) = <img src="images/blend-mode-linearlight-1.png" alt="Mathematical formula for a linear light effect." /></td>
</tr>
<tr class="even">
<td>D2D1_BLEND_MODE_PIN_LIGHT</td>
<td>Formule di Blend di base con <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) = <img src="images/blend-mode-pinlight-1.png" alt="Mathematical formula for a pin light effect." /></td>
</tr>
<tr class="odd">
<td>D2D1_BLEND_MODE_HARD_MIX</td>
<td>Formule di Blend di base con <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) = <img src="images/blend-mode-hardmix-1.png" alt="Mathematical formula for a hard mix effect." /></td>
</tr>
<tr class="even">
<td>D2D1_BLEND_MODE_DIFFERENCE</td>
<td>Formule di Blend di base con <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) = ABS (f<sub>RGB</sub> - B<sub>RGB</sub>)</td>
</tr>
<tr class="odd">
<td>D2D1_BLEND_MODE_EXCLUSION</td>
<td>Formule di base di Blend con <em>f</em>(f<sub>RGB</sub>, B<sub>RGB</sub>) = F<sub>RGB</sub> + b<sub>RGB</sub> 2 * f<sub>RGB</sub> * b<sub></sub> RGB</td>
</tr>
<tr class="even">
<td>D2D1_BLEND_MODE_HUE</td>
<td>Formula di Blend di base solo per Alpha. <img src="images/blend-mode-hue-1.png" alt="Mathematical formula for a hue blend effect." /></td>
</tr>
<tr class="odd">
<td>D2D1_BLEND_MODE_SATURATION</td>
<td>Formula di Blend di base solo per Alpha. <img src="images/blend-mode-saturation-1.png" alt="Mathematical formula for a sturation blend effect." /></td>
</tr>
<tr class="even">
<td>D2D1_BLEND_MODE_COLOR</td>
<td>Formula di Blend di base solo per Alpha. <img src="images/blend-mode-color-1.png" alt="Mathematical formula for a color blend effect." /></td>
</tr>
<tr class="odd">
<td>D2D1_BLEND_MODE_LUMINOSITY</td>
<td>Formula di Blend di base solo per Alpha. <img src="images/blend-mode-luminosity-1.png" alt="Mathematical formula for a luminosity blend effect." /></td>
</tr>
<tr class="even">
<td>D2D1_BLEND_MODE_DISSOLVE</td>
<td>Si consideri quanto segue:
<ul>
<li>Coordinata XY del pixel corrente</li>
<li>Un generatore di numeri pseudo-casuali deterministico (XY) basato su una coordinata XY con una distribuzione non distorta dei valori da [0,1]</li>
</ul>
<br/> <img src="images/blend-mode-dissolve-1.png" alt="Mathematical formula for a dissolve blend effect." /><br/></td>
</tr>
<tr class="odd">
<td>D2D1_BLEND_MODE_SUBTRACT</td>
<td>Formula di Blend di base solo per Alpha. <img src="images/blend-mode-subtract-1.png" alt="Mathematical formula for a subtract blend effect." /></td>
</tr>
<tr class="even">
<td>D2D1_BLEND_MODE_DIVISION</td>
<td>Formula di Blend di base solo per Alpha. <img src="images/blend-mode-division-1.png" alt="Mathematical formula for a division blend effect." /></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> Per tutte le modalità di Blend, il valore di output è premoltiplicato e viene premuto per l'intervallo compreso tra \[ 0 e 1 \] .

 

## <a name="hsl-color-space-conversions"></a>Conversioni dello spazio dei colori HSL

Il componente luminosità viene calcolato usando i pesi RGB qui:

-   *k*<sub>R</sub> = 0,30
-   *k*<sub>G</sub> = 0,59
-   *k*<sub>B</sub> = 0,11

### <a name="converting-from-rgb-to-hsl"></a>Conversione da RGB a HSL

![formula matematica che descrive la trasformazione dal colore RGB al colore HSL.](images/blend-rgb-to-hsl-1.png)

Questo inserisce *S* e *L* nell'intervallo \[ 0,0, 1,0 \] e *H* nell'intervallo \[ 1,0, 5,0 \] .

### <a name="converting-from-hsl-to-rgb"></a>Conversione da HSL a RGB

Per convertire l'altro modo si usa l'inverso dei calcoli precedenti.

Se *S* = 0, *R*  =  *G*  =  *B*  =  *L*

In caso contrario, sono presenti sei casi di Hue:

Se *H* è maggiore di 0, i valori si trovano nel settore rosso/magenta dove *R*  >  *B*  >  *G*.

![equaiton matematico passaggio uno di sei conversione del colore HSL in RGB.](images/blend-hsl-to-rgb-1rm.png)

Se *H* è maggiore o uguale a 0 e minore di 1, i valori sono nel settore rosso/giallo dove *R*  >  *G*  >  *B*.

![equaiton matematico-passaggio due di sei conversione del colore HSL in RGB.](images/blend-hsl-to-rgb-1ry.png)

Se *H* è maggiore o uguale a 1 e minore di 2, i valori sono nel settore giallo/verde dove *G*  >  *R*  >  *B*.

![equaiton matematico 3 di sei conversione del colore HSL in RGB.](images/blend-hsl-to-rgb-1yg.png)

Se *H* è maggiore o uguale a 2 e minore di 3, i valori sono nel settore verde/ciano dove *G*  >  *B*  >  *R*.

![equaiton matematico-passaggio quattro di sei conversione del colore HSL in RGB.](images/blend-hsl-to-rgb-1gc.png)

Se *H* è maggiore o uguale a 3 e minore di 4, i valori si trovano nel settore cyan/blue dove *B*  >  *G*  >  *R*.

![equaiton matematico-passaggio cinque di sei conversione del colore HSL in RGB.](images/blend-hsl-to-rgb-1cb.png)

Se *H* è maggiore o uguale a 4, i valori si trovano nel settore blu/Magenta dove *B*  >  *R*  >  *G*.

![equaiton matematico 6 di sei conversione del colore HSL in RGB.](images/blend-hsl-to-rgb-1bm.png)

Poiché le modalità di fusione consentono di combinare arbitrariamente i componenti HSL da due colori diversi, il valore RGB convertito non è compreso nell'intervallo, ovvero uno o più componenti del canale potrebbero non essere compresi nell'intervallo valido \[ 0,0, 1,0 \] . Questi colori vengono restituiti in gamut riducendo al minimo la saturazione, mantenendo al tempo stesso tonalità e luminosità:

![formula matematica che descrive le correzioni necessarie per le istanze out-of-gamut.](images/blend-gamut-correction.png)

## <a name="output-bitmap"></a>Bitmap di output

La bitmap di output per questo effetto è sempre la dimensione dell'Unione delle due immagini di input.

## <a name="sample-code"></a>Codice di esempio

Per un esempio di questo effetto, scaricare l' [esempio Direct2D composite Effect modes](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20composite%20effect%20modes%20sample).

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

 

