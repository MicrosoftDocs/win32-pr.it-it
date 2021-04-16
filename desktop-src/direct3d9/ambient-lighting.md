---
description: Illuminazione ambientale fornisce illuminazione costante per una scena.
ms.assetid: 327095a7-f4e0-48c2-9e4d-bec8493fe37e
title: Illuminazione ambiente (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e991981a9c1d7d24714e7014d08cefeaa94fe20f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523841"
---
# <a name="ambient-lighting-direct3d-9"></a>Illuminazione ambiente (Direct3D 9)

Illuminazione ambientale fornisce illuminazione costante per una scena. Illumina tutti i vertici degli oggetti allo stesso modo perché non dipende da altri fattori di illuminazione quali le normali dei vertici, la direzione della luce, la posizione della luce, l'intervallo o l'attenuazione. Si tratta del tipo di illuminazione più veloce, ma produce i risultati meno realistici. Direct3D contiene una singola proprietà di ambiente chiaro globale che è possibile usare senza creare alcuna luce. In alternativa, è possibile impostare qualsiasi oggetto chiaro per fornire l'illuminazione ambientale. L'illuminazione ambientale per una scena è descritta dall'equazione seguente.

Illuminazione ambiente = C ₐ \* \[ g ₐ + Sum (atten<sub>io</sub> \* spot<sub>i</sub> \* L<sub>ai</sub>)\]

Dove:



| Parametro         | Valore predefinito | Tipo          | Descrizione                                                                                                                    |
|-------------------|---------------|---------------|--------------------------------------------------------------------------------------------------------------------------------|
| C ₐ                | (0, 0, 0, 0)     | D3DCOLORVALUE | Colore ambiente materiale                                                                                                         |
| G ₐ                | (0, 0, 0, 0)     | D3DCOLORVALUE | Colore ambiente globale                                                                                                           |
| Atten<sub></sub> | (0, 0, 0, 0)     | D3DCOLORVALUE | Attenuazione chiara della luce del ith. Vedere [attenuazione e fattore di Spotlight (Direct3D 9)](attenuation-and-spotlight-factor.md). |
| Spot<sub>i</sub>  | (0, 0, 0, 0)     | D3DVECTOR     | Fattore di Spotlight della luce di Ith. Vedere [attenuazione e fattore di Spotlight (Direct3D 9)](attenuation-and-spotlight-factor.md).  |
| Sum               | N/D           | N/D           | Somma della luce di ambiente                                                                                                       |
| L<sub>ai</sub>    | (0, 0, 0, 0)     | D3DVECTOR     | Colore di ambiente chiaro della luce del ith                                                                                           |



 

Il valore per C ₐ è:

-   Vertex color1, se AMBIENTMATERIALSOURCE = D3DMCS \_ color1 e il primo colore del vertice viene specificato nella dichiarazione del vertice.
-   Vertex color2, se AMBIENTMATERIALSOURCE = D3DMCS \_ color2, e il secondo colore del vertice viene specificato nella dichiarazione del vertice.
-   colore ambiente materiale.

> [!Note]  
> Se si usa l'opzione AMBIENTMATERIALSOURCE e il colore del vertice non viene specificato, viene usato il colore di ambiente Material.

 

Per utilizzare il colore di ambiente Material, utilizzare sematerial come illustrato nel codice di esempio riportato di seguito.

G ₐ è il colore di ambiente globale. Viene impostato mediante SetRenderState (D3DRS \_ Ambient). In una scena Direct3D esiste un solo colore di ambiente globale. Questo parametro non è associato a un oggetto Direct3D Light.

L<sub>ai</sub> è il colore di ambiente della luce del ith nella scena. Ogni Direct3D Light ha un set di proprietà, uno dei quali è il colore di ambiente. Il termine Sum (L<sub>ai</sub>) è una somma di tutti i colori di ambiente nella scena.

## <a name="example"></a>Esempio

In questo esempio, l'oggetto è colorato usando la luce ambientale della scena e un colore di ambiente di materiale.


```
#define GRAY_COLOR  0x00bfbfbf

// create material
D3DMATERIAL9 mtrl;
ZeroMemory(&mtrl, sizeof(mtrl));
mtrl.Ambient.r = 0.75f;
mtrl.Ambient.g = 0.0f;
mtrl.Ambient.b = 0.0f;
mtrl.Ambient.a = 0.0f;
m_pd3dDevice->SetMaterial(&mtrl);
m_pd3dDevice->SetRenderState(D3DRS_AMBIENT, GRAY_COLOR);
```



In base all'equazione, il colore risultante per i vertici dell'oggetto è una combinazione del colore del materiale e del colore chiaro.

Le due illustrazioni seguenti mostrano il colore del materiale, che è grigio, e il colore chiaro, che è rosso chiaro.

![illustrazione di una sfera grigia](images/amb1.jpg)![illustrazione di una sfera rossa](images/lightred.jpg)

La scena risultante è illustrata nella figura seguente. L'unico oggetto nella scena è una sfera. La luce di ambiente illumina tutti i vertici degli oggetti con lo stesso colore. Non dipende dal vertice normale o dalla direzione della luce. Di conseguenza, la sfera appare come un cerchio 2D perché non esiste alcuna differenza nell'ombreggiatura intorno alla superficie dell'oggetto.

![illustrazione di una sfera con illuminazione ambientale](images/lighta.jpg)

Per fornire agli oggetti un aspetto più realistico, applicare un'illuminazione diffusa o speculare oltre all'illuminazione ambientale.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Matematica dell'illuminazione](mathematics-of-lighting.md)
</dt> </dl>

 

 



