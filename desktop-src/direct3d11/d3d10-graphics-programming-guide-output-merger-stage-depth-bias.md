---
title: Distorsione profondità
description: È possibile fare in modo che i poligoni complanari nello spazio 3D vengano visualizzati come se non fossero complanari aggiungendo a ognuno una distorsione z (o una distorsione di profondità).
ms.assetid: ee904316-dc6d-48a4-bdb7-0f7dcdb9d9d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d6f9a3850b03e033a90b358d0c6ffd1ceef830f
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "103734935"
---
# <a name="depth-bias"></a>Distorsione profondità

È possibile fare in modo che i poligoni complanari nello spazio 3D vengano visualizzati come se non fossero complanari aggiungendo a ognuno una distorsione z (o una distorsione di profondità).

Si tratta di una tecnica comunemente utilizzata per garantire che le ombre in una scena vengano visualizzate correttamente. Ad esempio, un'ombreggiatura su una parete avrà probabilmente lo stesso valore di profondità della parete. Se un'applicazione esegue il rendering di un muro prima e poi un'ombreggiatura, l'ombreggiatura potrebbe non essere visibile oppure gli artefatti di profondità potrebbero essere visibili.


Un'applicazione può garantire il rendering corretto dei poligoni complanari aggiungendo la distorsione (dal membro **DepthBias** di [**d3d11 \_ rasterizzator \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1)) ai valori z usati dal sistema durante il rendering dei set di poligoni complanari. I poligoni con un valore z maggiore verranno disegnati davanti ai poligoni con un valore z inferiore.

Sono disponibili due opzioni per il calcolo della distorsione della profondità.

1.  Se il buffer di profondità attualmente associato alla fase di Unione dell'output ha un formato **UNORM** o non è associato alcun buffer di profondità, il valore di distorsione viene calcolato in questo modo:
    ```
    Bias = (float)DepthBias * r + SlopeScaledDepthBias * MaxDepthSlope;
    ```

    

    dove *r* è il valore minimo rappresentabile > 0 nel formato del buffer di profondità convertito in **float32**. I valori **DepthBias** e **SlopeScaledDepthBias** sono membri della struttura [**d3d11 \_ rasterizzator \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1) . Il valore **MaxDepthSlope** è il numero massimo di pendii orizzontali e verticali del valore di profondità al pixel.
2.  Se un buffer di profondità a virgola mobile è associato alla fase di Unione dell'output, il valore della distorsione viene calcolato in questo modo:
    ```
    Bias = (float)DepthBias * 2**(exponent(max z in primitive) - r) +
                SlopeScaledDepthBias * MaxDepthSlope;
    ```

    

    dove *r* è il numero di mantissa bit nella rappresentazione a virgola mobile (escluso il bit nascosto); ad esempio, 23 per **float32**.

Il valore di distorsione viene quindi bloccato come segue:


```
if(DepthBiasClamp > 0)
    Bias = min(DepthBiasClamp, Bias)
else if(DepthBiasClamp < 0)
    Bias = max(DepthBiasClamp, Bias)
```



Il valore di distorsione viene quindi utilizzato per calcolare la profondità dei pixel.


```
if ( (DepthBias != 0) || (SlopeScaledDepthBias != 0) )
    z = z + Bias
```



Le operazioni di distorsione della profondità si verificano sui vertici dopo il ritaglio, quindi la distorsione della profondità non ha alcun effetto sul ritaglio geometrico. Il valore di distorsione è costante per una determinata primitiva e viene aggiunto al valore z per ogni vertice prima del programma di installazione dell'interpolatore. Quando si usano i [livelli di funzionalità](overviews-direct3d-11-devices-downlevel-intro.md) 10,0 e versioni successive, tutti i calcoli di distorsione vengono eseguiti usando l'aritmetica a virgola mobile a 32 bit. La distorsione non viene applicata ad alcuna primitiva di punti o righe, ad eccezione delle linee disegnate in modalità wireframe.

Uno degli artefatti con ombreggiature basate su buffer ombreggiatura è Shadow acne o una superficie ombreggiatura stessa a causa di differenze minime tra il calcolo della profondità in uno shader e la profondità della stessa superficie nel buffer di ombreggiatura. Un modo per risolvere questo problema consiste nell'usare **DepthBias** e **SlopeScaledDepthBias** durante il rendering di un buffer Shadow. L'idea è di effettuare il push delle superfici in modo sufficiente durante il rendering di un buffer di ombreggiatura, in modo che il risultato del confronto (tra il buffer di ombreggiatura z e lo shader z) sia coerente sulla superficie ed eviti l'ombreggiatura automatica locale.

Tuttavia, l'uso di **DepthBias** e **SlopeScaledDepthBias** può introdurre nuovi problemi di rendering quando un poligono visualizzato a un angolo estremamente acuto causa la generazione di un valore z molto grande nell'equazione di distorsione. Questa operazione effettua il push del poligono molto lontano dalla superficie originale nella mappa Shadow. Un modo per risolvere questo particolare problema consiste nell'usare **DepthBiasClamp**, che fornisce un limite superiore (positivo o negativo) sulla grandezza della distorsione z calcolata.

> [!Note]  
> Per i [livelli di funzionalità](overviews-direct3d-11-devices-downlevel-intro.md) 9,1, 9,2, 9,3, **DepthBiasClamp** non è supportato.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Output-fase di Unione](d3d10-graphics-programming-guide-output-merger-stage.md)
</dt> </dl>

 

 




