---
description: Dopo aver regolato l'intensità della luce per qualsiasi effetto di attenuazione, il motore di illuminazione calcola la quantità di luce rimanente riflessa da un vertice, in base all'angolo della normale del vertice e alla direzione della luce dell'evento imprevisto.
ms.assetid: 29280a02-1c26-4b54-8468-707dd96dea1d
title: Illuminazione diffusa (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9906742b47b959336fd882748388a2f10776b6adb06eb98bc23effb6576793be
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119675776"
---
# <a name="diffuse-lighting-direct3d-9"></a>Illuminazione diffusa (Direct3D 9)

Dopo aver regolato l'intensità della luce per qualsiasi effetto di attenuazione, il motore di illuminazione calcola la quantità di luce rimanente riflessa da un vertice, in base all'angolo della normale del vertice e alla direzione della luce dell'evento imprevisto. Il motore di illuminazione passa a questo passaggio per le luci direzionali perché non si attenuano sulla distanza. Il sistema considera due tipi di reflection, diffusi e speculari, e usa una formula diversa per determinare la quantità di luce riflessa per ognuno. Dopo aver calcolato le quantità di luce riflessa, Direct3D applica questi nuovi valori alle proprietà di riflessione diffuse e speculari del materiale corrente. I valori di colore risultanti sono i componenti diffusi e speculari utilizzati dal rasterizzatore per produrre l'ombreggiatura Gouraud e l'evidenziazione speculare.

L'illuminazione diffusa è descritta dall'equazione seguente.

Illuminazione diffusa = somma \[ C<sub>d</sub> \* L<sub>d</sub> \* (N<sup>.</sup> L<sub>dir</sub>) \* Atten \* Spot\]



| Parametro       | Valore predefinito | Tipo          | Descrizione                                                                                                   |
|-----------------|---------------|---------------|---------------------------------------------------------------------------------------------------------------|
| Sum             | N/D           | N/D           | Somma del componente diffuso di ogni luce.                                                                  |
| C<sub>d</sub>   | (0,0,0,0)     | D3DCOLORVALUE | Colore diffuso.                                                                                                |
| L<sub>d</sub>   | (0,0,0,0)     | D3DCOLORVALUE | Colore diffuso chiaro.                                                                                          |
| N               | N/A           | D3DVECTOR     | Normale vertice                                                                                                 |
| L<sub>dir</sub> | N/A           | D3DVECTOR     | Vettore di direzione dal vertice dell'oggetto alla luce.                                                             |
| Atten           | N/A           | FLOAT         | Attenuazione leggera. Vedere [Attenuazione e fattore spotlight (Direct3D 9).](attenuation-and-spotlight-factor.md) |
| Spot (Contante)            | N/A           | FLOAT         | Fattore Spotlight. Vedere [Attenuazione e fattore spotlight (Direct3D 9).](attenuation-and-spotlight-factor.md)  |



 

Il valore per C<sub>d</sub> è:

-   vertex color1, se DIFFUSEMATERIALSOURCE = D3DMCS COLOR1 e il primo colore del vertice viene \_ specificato nella dichiarazione del vertice.
-   vertex color2, se DIFFUSEMATERIALSOURCE = D3DMCS COLOR2 e il secondo colore del vertice viene \_ specificato nella dichiarazione del vertice.
-   colore diffuso del materiale

> [!Note]  
> Se si usa l'opzione DIFFUSEMATERIALSOURCE e non viene specificato il colore del vertice, viene usato il colore diffuso del materiale.

 

Per calcolare l'attenuazione (Atten) o le caratteristiche spotlight (Spot), vedere Attenuazione e fattore spotlight [(Direct3D 9).](attenuation-and-spotlight-factor.md)

I componenti diffusi vengono confissi da 0 a 255, dopo che tutte le luci vengono elaborate e interpolate separatamente. Il valore di illuminazione diffusa risultante è una combinazione dei valori di luce ambientale, diffusa ed emissiva.

## <a name="example"></a>Esempio

In questo esempio l'oggetto viene colorato usando il colore diffuso chiaro e un colore diffuso del materiale. Il codice è illustrato di seguito.


```
D3DMATERIAL9 mtrl;
ZeroMemory( &mtrl, sizeof(mtrl) );

D3DLIGHT9 light;
ZeroMemory( &light, sizeof(light) );
light.Type = D3DLIGHT_DIRECTIONAL;

D3DXVECTOR3 vecDir;
vecDir = D3DXVECTOR3(0.5f, 0.0f, -0.5f);
D3DXVec3Normalize( (D3DXVECTOR3*)&light.Direction, &vecDir );

// set directional light diffuse color
light.Diffuse.r = 1.0f;
light.Diffuse.g = 1.0f;
light.Diffuse.b = 1.0f;
light.Diffuse.a = 1.0f;
m_pd3dDevice->SetLight( 0, &light );
m_pd3dDevice->LightEnable( 0, TRUE );

// if a material is used, SetRenderState must be used
// vertex color = light diffuse color * material diffuse color
mtrl.Diffuse.r = 0.75f;
mtrl.Diffuse.g = 0.0f;
mtrl.Diffuse.b = 0.0f;
mtrl.Diffuse.a = 0.0f;
m_pd3dDevice->SetMaterial( &mtrl );
m_pd3dDevice->SetRenderState(D3DRS_DIFFUSEMATERIALSOURCE, D3DMCS_MATERIAL);
```



In base all'equazione, il colore risultante per i vertici dell'oggetto è una combinazione del colore del materiale e del colore chiaro.

Le due illustrazioni seguenti mostrano il colore del materiale, che è grigio, e il colore chiaro, rosso brillante.

![illustrazione di una sfera grigia](images/amb1.jpg)![illustrazione di una sfera rossa](images/lightred.jpg)

La scena risultante è illustrata nella figura seguente. L'unico oggetto nella scena è una sfera. Il calcolo dell'illuminazione diffusa accetta il colore diffuso del materiale e della luce e lo modifica in base all'angolo tra la direzione della luce e la normale del vertice usando il prodotto punto. Di conseguenza, il lato posteriore della sfera diventa più scuro quando la superficie della sfera si allontana dalla luce.

![illustrazione di una sfera con illuminazione diffusa](images/lightd.jpg)

Combinando l'illuminazione diffusa con l'illuminazione ambientale dell'esempio precedente, l'intera superficie dell'oggetto viene ombreggiata. La luce ambientale sfumatura l'intera superficie e la luce diffusa consente di rivelare la forma 3D dell'oggetto, come illustrato nella figura seguente.

![illustrazione di una sfera con illuminazione diffusa e illuminazione ambientale](images/lightad.jpg)

L'illuminazione diffusa è più intensiva da calcolare rispetto all'illuminazione ambientale. Poiché dipende dalle normali dei vertici e dalla direzione della luce, è possibile visualizzare la geometria degli oggetti nello spazio 3D, che produce un'illuminazione più realistica rispetto all'illuminazione ambientale. È possibile usare le evidenziazioni speculari per ottenere un aspetto più realistico.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Matematica dell'illuminazione](mathematics-of-lighting.md)
</dt> </dl>

 

 



