---
description: I componenti di illuminazione diffusa e speculare dell'equazione di illuminazione globale contengono termini che descrivono l'attenuazione della luce e il cono dei riflettori. Questi termini sono descritti di seguito.
ms.assetid: 960b5fc2-3074-4e51-b3de-5ed370379b01
title: Attenuazione e fattore spotlight (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb80fff287749e2979a89f2e20c830fdad3961d90ec05bf90a4ee2f6a51f8bcf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119850617"
---
# <a name="attenuation-and-spotlight-factor-direct3d-9"></a>Attenuazione e fattore spotlight (Direct3D 9)

I componenti di illuminazione diffusa e speculare dell'equazione di illuminazione globale contengono termini che descrivono l'attenuazione della luce e il cono dei riflettori. Questi termini sono descritti di seguito.

## <a name="attenuation"></a>Attenuazione

L'attenuazione di una luce dipende dal tipo di luce e dalla distanza tra la luce e la posizione dei vertici. Per calcolare l'attenuazione, usare una delle equazioni seguenti.

Atten = 1/( att0<sub>i</sub> + att1<sub>i</sub> \* d + att2<sub>i</sub> \* d²)

Dove:



| Parametro        | Valore predefinito | Tipo  | Descrizione                                     | Range          |
|------------------|---------------|-------|-------------------------------------------------|----------------|
| att0<sub>i</sub> | 0,0           | FLOAT | Fattore di attenuazione costante                     | Da 0 a +infinito |
| att1<sub>i</sub> | 0,0           | FLOAT | Fattore di attenuazione lineare                       | Da 0 a +infinito |
| att2<sub>i</sub> | 0,0           | FLOAT | Fattore di attenuazione quadratica                    | Da 0 a +infinito |
| d                | N/A           | FLOAT | Distanza dalla posizione del vertice alla posizione della luce | N/A            |



 

-   Atten = 1, se la luce è una luce direzionale.
-   Atten = 0, se la distanza tra la luce e il vertice supera l'intervallo della luce.

I valori att0, att1, att2 vengono specificati dai membri Attenuation0, Attenuation1 e Attenuation2 di [**D3DLIGHT9.**](d3dlight9.md)

La distanza tra la luce e la posizione del vertice è sempre positiva.

d = \| L<sub>dir</sub>\|

Dove:



| Parametro       | Valore predefinito | Tipo      | Descrizione                                                 |
|-----------------|---------------|-----------|-------------------------------------------------------------|
| L<sub>dir</sub> | N/A           | D3DVECTOR | Vettore di direzione dalla posizione del vertice alla posizione della luce |



 

Se d è maggiore dell'intervallo della luce, vale a vedere il membro Range di una struttura [**D3DLIGHT9,**](d3dlight9.md) Direct3D non esegue ulteriori calcoli di attenuazione e non applica alcun effetto dalla luce al vertice.

Le costanti di attenuazione fungono da coefficienti nella formula: è possibile produrre un'ampia gamma di curve di attenuazione apportando semplici modifiche. È possibile impostare Attenuation1 su 1.0 per creare una luce che non si attenua ma è ancora limitata in base all'intervallo oppure è possibile sperimentare valori diversi per ottenere vari effetti di attenuazione.

L'attenuazione all'intervallo massimo della luce non è 0,0. Per evitare che le luci si presentino improvvisamente quando si trova al raggio di luce, un'applicazione può aumentare la gamma di luce. In caso contrario, l'applicazione può impostare costanti di attenuazione in modo che il fattore di attenuazione sia vicino a 0,0 alla gamma di luce. Il valore di attenuazione viene moltiplicato per i componenti rosso, verde e blu del colore della luce per ridimensionare l'intensità della luce come fattore della distanza che la luce viaggia verso un vertice.

## <a name="spotlight-factor"></a>Fattore Spotlight

L'equazione seguente specifica il fattore spotlight.

![equazione del fattore spotlight](images/dx8light9.png)



| Parametro         | Valore predefinito | Tipo  | Descrizione                              | Range                    |
|-------------------|---------------|-------|------------------------------------------|--------------------------|
| rho<sub>i</sub>   | N/A           | FLOAT | coseno (angolo) per spotlight i            | N/A                      |
| phi<sub>i</sub>   | 0,0           | FLOAT | Angolo penumbra del riflettore i in radianti | \[theta<sub>i</sub>, pi greco) |
| theta<sub>i</sub> | 0,0           | FLOAT | Angolo umbra di riflettore i in radianti    | \[0, pi greco)                 |
| Falloff           | 0,0           | FLOAT | Fattore di falloff                           | (-infinity, +infinito)   |



 

Dove:

rho = norm(L<sub>dcs</sub>)<sup>.</sup> norm(L<sub>dir</sub>)

e:



| Parametro       | Valore predefinito | Tipo      | Descrizione                                                 |
|-----------------|---------------|-----------|-------------------------------------------------------------|
| L<sub>dcs</sub> | N/A           | D3DVECTOR | Negativo della direzione della luce nello spazio della fotocamera         |
| L<sub>dir</sub> | N/A           | D3DVECTOR | Vettore di direzione dalla posizione del vertice alla posizione della luce |



 

Dopo aver calcolato l'attenuazione della luce, Direct3D considera anche gli effetti in evidenza, se applicabile, l'angolo che la luce riflette da una superficie e la riflettenza del materiale corrente per calcolare i componenti diffusa e speculare per tale vertice. Per altre informazioni, vedere [SpotLight.](light-types.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Matematica dell'illuminazione](mathematics-of-lighting.md)
</dt> </dl>

 

 



