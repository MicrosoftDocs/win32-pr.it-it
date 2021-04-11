---
description: Dopo aver modificato l'intensità di luce per qualsiasi effetto di attenuazione, il motore di illuminazione calcola la quantità di luce rimanente riflessa da un vertice, dato l'angolo della normale del vertice e la direzione della luce dell'evento imprevisto.
ms.assetid: 29280a02-1c26-4b54-8468-707dd96dea1d
title: Illuminazione diffusa (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f51e45093786348aaa115ec38c420acec471f718
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123375"
---
# <a name="diffuse-lighting-direct3d-9"></a>Illuminazione diffusa (Direct3D 9)

Dopo aver modificato l'intensità di luce per qualsiasi effetto di attenuazione, il motore di illuminazione calcola la quantità di luce rimanente riflessa da un vertice, dato l'angolo della normale del vertice e la direzione della luce dell'evento imprevisto. Il motore di illuminazione passa a questo passaggio per le spie direzionali perché non attenuano la distanza. Il sistema considera due tipi di reflection, diffusi e speculari, e usa una formula diversa per determinare la quantità di luce che viene riflessa per ciascuna di esse. Dopo aver calcolato la quantità di luce riflessa, Direct3D applica questi nuovi valori alle proprietà di Reflection diffusa e speculare del materiale corrente. I valori dei colori risultanti sono i componenti di diffusione e speculare usati dal rasterizzatore per produrre l'ombreggiatura Gouraud e l'evidenziazione speculare.

L'illuminazione diffusa è descritta dalla seguente equazione.

Illuminazione diffusa = somma \[ C<sub>d</sub> \* L<sub>d</sub> \* (N<sup>.</sup> L<sub>dir</sub>) \* atten \* spot\]



| Parametro       | Valore predefinito | Tipo          | Descrizione                                                                                                   |
|-----------------|---------------|---------------|---------------------------------------------------------------------------------------------------------------|
| Sum             | N/D           | N/D           | Sommatoria del componente diffuso di ogni luce.                                                                  |
| C<sub>d</sub>   | (0, 0, 0, 0)     | D3DCOLORVALUE | Colore diffuso.                                                                                                |
| L<sub>d</sub>   | (0, 0, 0, 0)     | D3DCOLORVALUE | Colore diffuso chiaro.                                                                                          |
| N               | N/D           | D3DVECTOR     | Normale vertice                                                                                                 |
| <sub>Dir</sub> | N/D           | D3DVECTOR     | Vettore di direzione dal vertice dell'oggetto alla luce.                                                             |
| Atten           | N/D           | FLOAT         | Attenuazione chiara. Vedere [attenuazione e fattore di Spotlight (Direct3D 9)](attenuation-and-spotlight-factor.md). |
| Spot (Contante)            | N/D           | FLOAT         | Fattore Spotlight. Vedere [attenuazione e fattore di Spotlight (Direct3D 9)](attenuation-and-spotlight-factor.md).  |



 

Il valore per C<sub>d</sub> è uno dei seguenti:

-   Vertex color1, se DIFFUSEMATERIALSOURCE = D3DMCS \_ color1 e il primo colore del vertice viene specificato nella dichiarazione del vertice.
-   Vertex color2, se DIFFUSEMATERIALSOURCE = D3DMCS \_ color2, e il secondo colore del vertice viene specificato nella dichiarazione del vertice.
-   colore diffuso materiale

> [!Note]  
> Se viene usata l'opzione DIFFUSEMATERIALSOURCE e il colore del vertice non viene specificato, viene usato il colore di materiale diffuso.

 

Per calcolare l'attenuazione (atten) o le caratteristiche Spotlight (spot), vedere [attenuazione e fattore di Spotlight (Direct3D 9)](attenuation-and-spotlight-factor.md).

I componenti diffusi vengono fissati da 0 a 255, dopo che tutte le luci vengono elaborate e interpolate separatamente. Il valore di illuminazione diffusa risultante è una combinazione dei valori di ambiente, diffusione e luce emissivo.

## <a name="example"></a>Esempio

In questo esempio, l'oggetto è colorato usando il colore chiaro e un colore diffuso di materiale. Il codice è illustrato di seguito.


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

Le due illustrazioni seguenti mostrano il colore del materiale, che è grigio, e il colore chiaro, che è rosso chiaro.

![illustrazione di una sfera grigia](images/amb1.jpg)![illustrazione di una sfera rossa](images/lightred.jpg)

La scena risultante è illustrata nella figura seguente. L'unico oggetto nella scena è una sfera. Il calcolo di illuminazione diffusa prende il colore del materiale e della luce diffusa e lo modifica in base all'angolo tra la direzione della luce e la normale del vertice usando il prodotto punto. Di conseguenza, il lato posteriore della sfera diventa più scuro come la superficie delle curve della sfera fuori dalla luce.

![illustrazione di una sfera con illuminazione diffusa](images/lightd.jpg)

Combinando l'illuminazione diffusa con l'illuminazione ambientale dell'esempio precedente, viene ombreggiata l'intera superficie dell'oggetto. La luce di ambiente sfuma l'intera superficie e la luce diffusa consente di rivelare la forma 3D dell'oggetto, come illustrato nella figura seguente.

![illustrazione di una sfera con illuminazione diffusa e illuminazione ambientale](images/lightad.jpg)

L'illuminazione diffusa è più impegnativa per il calcolo rispetto all'illuminazione ambientale. Poiché dipende dalle normali dei vertici e dalla direzione della luce, è possibile visualizzare la geometria degli oggetti nello spazio 3D, che produce un'illuminazione più realistica rispetto all'illuminazione ambientale. Per ottenere un aspetto più realistico, è possibile usare le evidenziazioni speculari.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Matematica dell'illuminazione](mathematics-of-lighting.md)
</dt> </dl>

 

 



