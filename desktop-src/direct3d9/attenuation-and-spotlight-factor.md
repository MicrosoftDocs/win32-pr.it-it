---
description: I componenti di illuminazione diffusa e speculare dell'equazione di illuminazione globale contengono termini che descrivono l'attenuazione chiara e il cono Spotlight. Questi termini sono descritti di seguito.
ms.assetid: 960b5fc2-3074-4e51-b3de-5ed370379b01
title: Attenuazione e fattore Spotlight (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 623bb3cb2b1c2a3ee9e0e5d9419ff71dd9a303b6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104564255"
---
# <a name="attenuation-and-spotlight-factor-direct3d-9"></a>Attenuazione e fattore Spotlight (Direct3D 9)

I componenti di illuminazione diffusa e speculare dell'equazione di illuminazione globale contengono termini che descrivono l'attenuazione chiara e il cono Spotlight. Questi termini sono descritti di seguito.

## <a name="attenuation"></a>Attenuazione

L'attenuazione di una luce dipende dal tipo di luce e dalla distanza tra la luce e la posizione del vertice. Per calcolare l'attenuazione, usare una delle equazioni seguenti.

Atten = 1/(att0<sub>i</sub> + Att1<sub>i</sub> \* d + ATT2<sub>i</sub> \* d ²)

Dove:



| Parametro        | Valore predefinito | Tipo  | Descrizione                                     | Range          |
|------------------|---------------|-------|-------------------------------------------------|----------------|
| att0<sub></sub> | 0,0           | FLOAT | Fattore di attenuazione costante                     | da 0 a + infinito |
| Att1<sub></sub> | 0,0           | FLOAT | Fattore di attenuazione lineare                       | da 0 a + infinito |
| ATT2<sub></sub> | 0,0           | FLOAT | Fattore di attenuazione quadratica                    | da 0 a + infinito |
| d                | N/D           | FLOAT | Distanza dalla posizione del vertice alla posizione chiara | N/D            |



 

-   Atten = 1, se la luce è una luce direzionale.
-   Atten = 0, se la distanza tra la luce e il vertice supera l'intervallo della luce.

I valori att0, att1, att2 sono specificati dai membri Attenuation0, Attenuation1 e Attenuation2 di [**D3DLIGHT9**](d3dlight9.md).

La distanza tra la luce e la posizione del vertice è sempre positiva.

d = \| L<sub>dir</sub>\|

Dove:



| Parametro       | Valore predefinito | Tipo      | Descrizione                                                 |
|-----------------|---------------|-----------|-------------------------------------------------------------|
| <sub>Dir</sub> | N/D           | D3DVECTOR | Vettore direzione dalla posizione vertice alla posizione chiara |



 

Se d è maggiore dell'intervallo della luce, ovvero il membro di intervallo di una struttura [**D3DLIGHT9**](d3dlight9.md) , Direct3D non esegue ulteriori calcoli di attenuazione e non applica alcun effetto dalla luce al vertice.

Le costanti di attenuazione agiscono come coefficienti nella formula: è possibile produrre una serie di curve di attenuazione apportando semplici regolazioni. È possibile impostare Attenuation1 su 1,0 per creare una luce che non si attenua, ma che sia ancora limitata da intervallo, oppure è possibile sperimentare valori diversi per ottenere vari effetti di attenuazione.

L'attenuazione nell'intervallo massimo della luce non è 0,0. Per evitare che le luci vengano visualizzate improvvisamente quando si trovano nell'intervallo di luce, un'applicazione può aumentare l'intervallo di luce. In alternativa, l'applicazione può impostare costanti di attenuazione in modo che il fattore di attenuazione si avvicini a 0,0 nell'intervallo chiaro. Il valore di attenuazione viene moltiplicato per i componenti rosso, verde e blu del colore della luce per ridimensionare l'intensità della luce come fattore della luce della distanza che passa a un vertice.

## <a name="spotlight-factor"></a>Fattore Spotlight

L'equazione seguente specifica il fattore Spotlight.

![equazione del fattore Spotlight](images/dx8light9.png)



| Parametro         | Valore predefinito | Tipo  | Descrizione                              | Range                    |
|-------------------|---------------|-------|------------------------------------------|--------------------------|
| Rho<sub>i</sub>   | N/D           | FLOAT | coseno (angolo) per Spotlight i            | N/D                      |
| <sub>i</sub>   | 0,0           | FLOAT | Angolo penombra del faretto i in radianti | \[Theta<sub>i</sub>, pi) |
| Theta<sub>i</sub> | 0,0           | FLOAT | Angolo umbra del faretto i in radianti    | \[0, pi greco)                 |
| falloff           | 0,0           | FLOAT | Fattore di interruzione                           | (-infinito, + infinito)   |



 

Dove:

Rho = Norm (L<sub>DCS</sub>)<sup>.</sup> norma (L<sub>dir</sub>)

e:



| Parametro       | Valore predefinito | Tipo      | Descrizione                                                 |
|-----------------|---------------|-----------|-------------------------------------------------------------|
| <sub>Controller di dominio</sub> L | N/D           | D3DVECTOR | Il negativo della direzione della luce nello spazio della fotocamera         |
| <sub>Dir</sub> | N/D           | D3DVECTOR | Vettore direzione dalla posizione vertice alla posizione chiara |



 

Una volta calcolata l'attenuazione della luce, Direct3D Considera anche gli effetti Spotlight, se applicabile, l'angolo che la luce riflette da una superficie e la reflection del materiale corrente per calcolare i componenti diffusi e speculari per il vertice. Per altre informazioni, vedere [Spotlight](light-types.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Matematica dell'illuminazione](mathematics-of-lighting.md)
</dt> </dl>

 

 



