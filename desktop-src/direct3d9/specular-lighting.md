---
description: Per la modellazione della reflection speculare è necessario che il sistema non conosca solo la direzione della luce che è in viaggio, ma anche la direzione dell'occhio del visualizzatore.
ms.assetid: 35da0ac3-4e68-4d37-a987-405fc15d0cbf
title: Illuminazione speculare (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ab378d4ca3f00ef81c5048e6ad6cc85eaeb18ad
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104568387"
---
# <a name="specular-lighting-direct3d-9"></a>Illuminazione speculare (Direct3D 9)

Per la modellazione della reflection speculare è necessario che il sistema non conosca solo la direzione della luce che è in viaggio, ma anche la direzione dell'occhio del visualizzatore. Il sistema usa una versione semplificata del modello Phong specularità-Reflection, che usa un vettore a metà per approssimare l'intensità della reflection speculare.

Lo stato di illuminazione predefinito non calcola le evidenziazioni speculari. Per abilitare l'illuminazione speculare, assicurarsi di impostare D3DRS \_ SPECULARENABLE su **true**.

## <a name="specular-lighting-equation"></a>Equazione di illuminazione speculare

L'illuminazione speculare è descritta dall'equazione seguente.



|                                                                             |
|-----------------------------------------------------------------------------|
| Illuminazione speculare = cs \* Sum \[ ls \* (N · H)<sup>P</sup> \* atten \* spot\] |



 

La tabella seguente identifica le variabili, i relativi tipi e i relativi intervalli.



| Parametro    | Valore predefinito | Tipo          | Descrizione                                                                                                         |
|--------------|---------------|---------------|---------------------------------------------------------------------------------------------------------------------|
| CS           | (0, 0, 0, 0)     | D3DCOLORVALUE | Colore speculare.                                                                                                     |
| Sum          | N/D           | N/D           | Sommatoria del componente speculare di ogni luce.                                                                       |
| N            | N/D           | D3DVECTOR     | Normale vertice.                                                                                                      |
| H            | N/D           | D3DVECTOR     | Vettore a metà strada. Vedere la sezione sul vettore a metà.                                                             |
| <sup>P</sup> | 0,0           | FLOAT         | Potenza Reflection speculare. L'intervallo è compreso tra 0 e + infinito                                                                  |
| LS           | (0, 0, 0, 0)     | D3DCOLORVALUE | Colore speculare chiaro.                                                                                               |
| Atten        | N/D           | FLOAT         | Valore di attenuazione chiaro. Vedere [attenuazione e fattore di Spotlight (Direct3D 9)](attenuation-and-spotlight-factor.md). |
| Spot (Contante)         | N/D           | FLOAT         | Fattore Spotlight. Vedere [attenuazione e fattore di Spotlight (Direct3D 9)](attenuation-and-spotlight-factor.md).        |



 

Il valore per CS è:


```
if(SPECULARMATERIALSOURCE == D3DMCS_COLOR1)
  C = color1;
```



-   color1 vertice, se l'origine del materiale speculare è D3DMCS \_ color1 e il primo colore del vertice viene specificato nella dichiarazione del vertice.
-   color2 vertice, se l'origine del materiale speculare è D3DMCS \_ color2 e il secondo colore del vertice viene specificato nella dichiarazione del vertice.
-   colore speculare materiale

> [!Note]  
> Se viene usata l'opzione origine materiale speculare e il colore del vertice non è specificato, viene usato il colore speculare Material.

 

I componenti speculari vengono fissati da 0 a 255, dopo che tutte le luci vengono elaborate e interpolate separatamente.

## <a name="the-halfway-vector"></a>Vettore a metà

Il vettore a metà (H) esiste a metà tra due vettori: il vettore da un vertice dell'oggetto alla sorgente di luce e il vettore da un vertice dell'oggetto alla posizione della camera. Direct3D offre due modi per calcolare il vettore a metà. Quando D3DRS \_ LOCALVIEWER è impostato su **true**, il sistema calcola il vettore a metà usando la posizione della fotocamera e la posizione del vertice, insieme al vettore di direzione della luce. Questa operazione viene illustrata nella formula seguente.



|                                           |
|-------------------------------------------|
| H = Norm (Norm (CP-VP) + L<sub>dir</sub>) |



 



| Parametro       | Valore predefinito | Tipo      | Descrizione                                                  |
|-----------------|---------------|-----------|--------------------------------------------------------------|
| CP              | N/D           | D3DVECTOR | Posizione della fotocamera.                                             |
| VP              | N/D           | D3DVECTOR | Posizione vertice.                                             |
| <sub>Dir</sub> | N/D           | D3DVECTOR | Vettore di direzione dalla posizione del vertice alla posizione di luce. |



 

La determinazione del vettore a metà in questo modo può essere a elevato utilizzo di calcolo. In alternativa, \_ l'impostazione di D3DRS LOCALVIEWER = **false** indica al sistema di agire come se il punto di vista fosse infinitamente distante sull'asse z. Questa operazione si riflette nella formula seguente.



|                                     |
|-------------------------------------|
| H = Norm ((0, 0, 1) + L<sub>dir</sub>) |



 

Questa impostazione è meno complessa dal punto di vista del calcolo, ma è molto meno precisa, quindi è consigliabile usarla per le applicazioni che usano la proiezione ortogonale.

## <a name="example"></a>Esempio

In questo esempio, l'oggetto è colorato utilizzando il colore di luce speculare della scena e un colore speculare materiale. Il codice è illustrato di seguito.


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

Nella figura seguente vengono illustrati il colore del materiale speculare, che è grigio, e il colore chiaro speculare, che è bianco.

![illustrazione di una sfera grigia](images/amb1.jpg)![illustrazione di una sfera bianca](images/lightwhite.jpg)

L'evidenziazione speculare risultante è illustrata nella figura seguente.

![illustrazione dell'evidenziazione speculare](images/lights.jpg)

La combinazione dell'evidenziazione speculare con l'illuminazione ambiente e diffusa produce la figura seguente. Con tutti e tre i tipi di illuminazione applicati, questo è più chiaramente simile a un oggetto realistico.

![illustrazione della combinazione dell'evidenziazione speculare, dell'illuminazione ambientale e della luce diffusa](images/lightads.jpg)

L'illuminazione speculare è più impegnativa da calcolare rispetto all'illuminazione diffusa. Viene in genere usato per fornire indizi visivi sul materiale della superficie. L'evidenziazione speculare varia a seconda della dimensione e del colore del materiale della superficie.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Matematica dell'illuminazione](mathematics-of-lighting.md)
</dt> </dl>

 

 



