---
description: La modellazione della reflection speculare richiede che il sistema non solo sappia in quale direzione viaggia la luce, ma anche la direzione verso l'occhio dello visualizzatore.
ms.assetid: 35da0ac3-4e68-4d37-a987-405fc15d0cbf
title: Illuminazione speculare (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b16d71bd8d814e104cf8a90d1d1fe9b15ba10f3
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343676"
---
# <a name="specular-lighting-direct3d-9"></a>Illuminazione speculare (Direct3D 9)

La modellazione della reflection speculare richiede che il sistema non solo sappia in quale direzione viaggia la luce, ma anche la direzione verso l'occhio dello visualizzatore. Il sistema usa una versione semplificata del modello phong specular-reflection, che usa un vettore a metà per approssimare l'intensità della reflection speculare.

Lo stato di illuminazione predefinito non calcola le evidenziazioni speculari. Per abilitare l'illuminazione speculare, assicurarsi di impostare D3DRS \_ SPECULARENABLE su **TRUE**.

## <a name="specular-lighting-equation"></a>Equazione di illuminazione speculare

L'illuminazione speculare è descritta dall'equazione seguente:

**Illuminazione speculare = Cs \* sum \[ Ls \* (N · H)<sup>P</sup> \* Atten \* Spot\]**



 

La tabella seguente identifica le variabili, i relativi tipi e i relativi intervalli.



| Parametro    | Valore predefinito | Tipo          | Descrizione                                                                                                         |
|--------------|---------------|---------------|---------------------------------------------------------------------------------------------------------------------|
| Cs           | (0,0,0,0)     | D3DCOLORVALUE | Colore speculare.                                                                                                     |
| Sum          | N/D           | N/D           | Somma del componente speculare di ogni luce.                                                                       |
| N            | N/D           | D3DVECTOR     | Normale vertice.                                                                                                      |
| H            | N/D           | D3DVECTOR     | Vettore a metà strada. Vedere la sezione sul vettore a metà.                                                             |
| <sup>P</sup> | 0,0           | FLOAT         | Potenza di reflection speculare. L'intervallo è compreso tra 0 e +infinito                                                                  |
| Ls           | (0,0,0,0)     | D3DCOLORVALUE | Colore speculare chiaro.                                                                                               |
| Atten        | N/D           | FLOAT         | Valore di attenuazione della luce. Vedere [Attenuazione e fattore spotlight (Direct3D 9).](attenuation-and-spotlight-factor.md) |
| Spot (Contante)         | N/D           | FLOAT         | Fattore Spotlight. Vedere [Attenuazione e fattore spotlight (Direct3D 9).](attenuation-and-spotlight-factor.md)        |



 

Il valore per Cs è:


```
if(SPECULARMATERIALSOURCE == D3DMCS_COLOR1)
  C = color1;
```



-   vertex color1, se l'origine del materiale speculare è D3DMCS COLOR1 e il primo colore del vertice viene \_ fornito nella dichiarazione del vertice.
-   vertex color2, se l'origine del materiale speculare è D3DMCS COLOR2 e il secondo colore del vertice viene \_ fornito nella dichiarazione del vertice.
-   colore speculare materiale

> [!Note]  
> Se si usa una delle due opzioni di origine del materiale speculare e non viene specificato il colore del vertice, viene usato il colore speculare del materiale.

 

I componenti speculari sono definiti in modo da essere da 0 a 255, dopo che tutte le luci vengono elaborate e interpolate separatamente.

## <a name="the-halfway-vector"></a>Vettore a metà strada

Il vettore intermedio (H) si trova a metà tra due vettori: il vettore da un vertice dell'oggetto alla sorgente di luce e il vettore da un vertice dell'oggetto alla posizione della fotocamera. Direct3D offre due modi per calcolare il vettore a metà. Quando D3DRS LOCALVIEWER è impostato su TRUE, il sistema calcola il vettore a metà strada usando la posizione della fotocamera e la posizione del vertice, insieme al vettore di direzione della \_ luce.  La formula seguente illustra questa operazione.

**H = norm(norm(Cp - Vp) + L <sub>dir</sub>)**



 



| Parametro       | Valore predefinito | Tipo      | Descrizione                                                  |
|-----------------|---------------|-----------|--------------------------------------------------------------|
| Cp              | N/D           | D3DVECTOR | Posizione della fotocamera.                                             |
| Vp              | N/D           | D3DVECTOR | Posizione del vertice.                                             |
| L<sub>dir</sub> | N/D           | D3DVECTOR | Vettore di direzione dalla posizione del vertice alla posizione della luce. |



 

Determinare il vettore a metà strada in questo modo può essere intensivo dal punto di vista del calcolo. In alternativa, l'impostazione di D3DRS LOCALVIEWER = FALSE indica al sistema di agire come se il punto di vista \_ fosse infinitamente distante sull'asse z.  Ciò si riflette nella formula seguente.

**H = norm((0,0,1) + L <sub>dir</sub>)**



 

Questa impostazione è meno intensiva dal punto di vista del calcolo, ma molto meno accurata, quindi viene usata meglio dalle applicazioni che usano la proiezione ortogonale.

## <a name="example"></a>Esempio

In questo esempio l'oggetto viene colorato usando il colore della luce speculare della scena e un colore speculare materiale. Il codice è illustrato di seguito.


```
D3DMATERIAL9 mtrl;
ZeroMemory( &mtrl, sizeof(mtrl) );

D3DLIGHT9 light;
ZeroMemory( &light, sizeof(light) );
light.Type = D3DLIGHT_DIRECTIONAL;

D3DXVECTOR3 vecDir;
vecDir = D3DXVECTOR3(0.5f, 0.0f, -0.5f);
D3DXVec3Normalize( (D3DXVECTOR3*)&light.Direction, &vecDir );

light.Specular.r = 1.0f;
light.Specular.g = 1.0f;
light.Specular.b = 1.0f;
light.Specular.a = 1.0f;

light.Range = 1000;
light.Falloff = 0;
light.Attenuation0 = 1;
light.Attenuation1 = 0;
light.Attenuation2 = 0;
m_pd3dDevice->SetLight( 0, &light );
m_pd3dDevice->LightEnable( 0, TRUE );
m_pd3dDevice->SetRenderState( D3DRS_SPECULARENABLE, TRUE );

mtrl.Specular.r = 0.5f;
mtrl.Specular.g = 0.5f;
mtrl.Specular.b = 0.5f;
mtrl.Specular.a = 0.5f;
mtrl.Power = 20;
m_pd3dDevice->SetMaterial( &mtrl );
m_pd3dDevice->SetRenderState(D3DRS_SPECULARMATERIALSOURCE, D3DMCS_MATERIAL);
```



In base all'equazione, il colore risultante per i vertici dell'oggetto è una combinazione del colore del materiale e del colore chiaro.

Nella figura seguente vengono illustrati il colore del materiale speculare, ovvero il grigio, e il colore chiaro speculare, ovvero il bianco.

![illustrazione di una sfera grigia](images/amb1.jpg)![illustrazione di una sfera bianca](images/lightwhite.jpg)

L'evidenziazione speculare risultante è illustrata nella figura seguente.

![illustrazione dell'evidenziazione speculare](images/lights.jpg)

La combinazione dell'evidenziazione speculare con l'illuminazione ambientale e diffusa produce la figura seguente. Con tutti e tre i tipi di illuminazione applicati, questo oggetto è più chiaramente simile a un oggetto realistico.

![illustrazione della combinazione dell'evidenziazione speculare, dell'illuminazione ambientale e dell'illuminazione diffusa](images/lightads.jpg)

L'illuminazione speculare è più intensiva da calcolare rispetto all'illuminazione diffusa. Viene in genere usato per fornire indicazioni visive sul materiale della superficie. L'evidenziazione speculare varia in base alle dimensioni e al colore del materiale della superficie.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Matematica dell'illuminazione](mathematics-of-lighting.md)
</dt> </dl>

 

 



