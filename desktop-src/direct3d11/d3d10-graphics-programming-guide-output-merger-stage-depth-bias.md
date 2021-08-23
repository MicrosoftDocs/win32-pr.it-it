---
title: Distorsione della profondità
description: I poligoni coplanari nello spazio 3D possono essere visualizzati come se non fossero coplanari aggiungendo una distorsione z (o distorsione della profondità) a ognuno di essi.
ms.assetid: ee904316-dc6d-48a4-bdb7-0f7dcdb9d9d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1f707a038a2da8ebe9c1adc21f6081c85f5a63fbbc1c360a4dfbbf5765d845d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990161"
---
# <a name="depth-bias"></a>Distorsione della profondità

I poligoni coplanari nello spazio 3D possono essere visualizzati come se non fossero coplanari aggiungendo una distorsione z (o distorsione della profondità) a ognuno di essi.

Si tratta di una tecnica comunemente usata per garantire che le ombreggiature in una scena siano visualizzate correttamente. Ad esempio, un'ombreggiatura su una parete avrà probabilmente lo stesso valore di profondità della parete. Se un'applicazione esegue prima il rendering di un muro e quindi di un'ombreggiatura, l'ombreggiatura potrebbe non essere visibile o gli artefatti di profondità potrebbero essere visibili.


Un'applicazione può garantire che il rendering dei poligoni coplanari venga eseguito correttamente aggiungendo la distorsione (dal membro **DepthBias** di [**D3D11 \_ RASTERIZER \_ DESC1)**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1)ai valori z utilizzati dal sistema durante il rendering dei set di poligoni coplanari. I poligoni con un valore z più grande verranno disegnati davanti ai poligoni con un valore z più piccolo.

Esistono due opzioni per calcolare la distorsione della profondità.

1.  Se il buffer di profondità attualmente associato alla fase di unione di output ha un formato **UNORM** o non è associato alcun buffer di profondità, il valore di distorsione viene calcolato nel modo seguente:
    ```
    Bias = (float)DepthBias * r + SlopeScaledDepthBias * MaxDepthSlope;
    ```

    

    dove *r* è il valore minimo rappresentabile > 0 nel formato depth-buffer convertito in **float32**. I **valori DepthBias** e **SlopeScaledDepthBias** sono membri della struttura [**D3D11 \_ RASTERIZER \_ DESC1.**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1) Il **valore MaxDepthSlope** è il massimo delle inclinazioni orizzontali e verticali del valore di profondità in pixel.
2.  Se un buffer di profondità a virgola mobile è associato alla fase di unione di output, il valore di distorsione viene calcolato nel modo seguente:
    ```
    Bias = (float)DepthBias * 2**(exponent(max z in primitive) - r) +
                SlopeScaledDepthBias * MaxDepthSlope;
    ```

    

    dove *r* è il numero di bit mantissa nella rappresentazione a virgola mobile (escluso il bit nascosto); ad esempio 23 per **float32**.

Il valore di distorsione viene quindi impostato in modo simile al seguente:


```
if(DepthBiasClamp > 0)
    Bias = min(DepthBiasClamp, Bias)
else if(DepthBiasClamp < 0)
    Bias = max(DepthBiasClamp, Bias)
```



Il valore di distorsione viene quindi usato per calcolare la profondità dei pixel.


```
if ( (DepthBias != 0) || (SlopeScaledDepthBias != 0) )
    z = z + Bias
```



Le operazioni di distorsione della profondità si verificano sui vertici dopo il ritaglio, pertanto la distorsione della profondità non ha alcun effetto sul ritaglio geometrico. Il valore di distorsione è costante per una determinata primitiva e viene aggiunto al valore z per ogni vertice prima della configurazione dell'interpolatore. Quando si usano [livelli di](overviews-direct3d-11-devices-downlevel-intro.md) funzionalità 10.0 e versioni successive, tutti i calcoli di distorsione vengono eseguiti usando l'aritmetica a virgola mobile a 32 bit. La distorsione non viene applicata ad alcuna primitiva di punto o linea, ad eccezione delle linee disegnate in modalità wireframe.

Uno degli artefatti con ombreggiature basate su buffer ombreggiatura è l'ombreggiatura o una superficie che si nasconde a causa di piccole differenze tra il calcolo della profondità in uno shader e la profondità della stessa superficie nel buffer dell'ombreggiatura. Un modo per attenuare questo problema è usare **DepthBias** e **SlopeScaledDepthBias quando** si esegue il rendering di un buffer ombreggiato. L'idea è quella di eseguire il push delle superfici sufficientemente fuori durante il rendering di un buffer ombreggiatura in modo che il risultato del confronto (tra il buffer di ombreggiatura z e lo shader z) sia coerente sulla superficie ed evitare l'auto shadowing locale.

Tuttavia, l'uso di **DepthBias** e **SlopeScaledDepthBias** può introdurre nuovi problemi di rendering quando un poligono visualizzato con un angolo estremamente acuto fa sì che l'equazione di distorsione generi un valore z molto grande. Questo in effetti spinge il poligono molto lontano dalla superficie originale nella mappa delle ombreggiatura. Un modo per attenuare questo particolare problema è usare **DepthBiasClamp**, che fornisce un limite superiore (positivo o negativo) sulla grandezza della distorsione z calcolata.

> [!Note]  
> Per [i livelli](overviews-direct3d-11-devices-downlevel-intro.md) di funzionalità 9.1, 9.2, 9.3, **DepthBiasClamp** non è supportato.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Fase di unione dell'output](d3d10-graphics-programming-guide-output-merger-stage.md)
</dt> </dl>

 

 




