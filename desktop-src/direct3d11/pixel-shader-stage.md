---
title: Fase pixel shader
description: La fase pixel shader consente tecniche di ombreggiatura avanzate, ad esempio l'illuminazione per pixel e la post-elaborazione.
ms.assetid: 09831B10-4FD1-41E7-8D81-5AA63DC90020
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dd58bbc55bbc2fb7d590036bceb061f2a304c0be16ff058d04f226021dfe3cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119988161"
---
# <a name="pixel-shader-stage"></a>Fase pixel shader

La fase pixel shader consente tecniche di ombreggiatura avanzate, ad esempio l'illuminazione per pixel e la post-elaborazione. Un pixel shader è un programma che combina variabili costanti, dati di trama, valori interpolati per vertice e altri dati per produrre output per pixel. La fase di rasterizzazione richiama un pixel shader una volta per ogni pixel coperto da una primitiva, tuttavia è possibile specificare uno shader **NULL** per evitare l'esecuzione di uno shader.

## <a name="the-pixel-shader"></a>The Pixel Shader

Quando si esegue il multicampionamento di una trama, un pixel shader viene richiamato una volta per ogni pixel coperto, mentre viene eseguito un test di profondità/stencil per ogni multicampionamento coperto. Gli esempi che superano il test di profondità/stencil vengono aggiornati con il colore pixel shader di output.

Le pixel shader funzioni intrinseche producono o usano derivati delle quantità rispetto allo spazio dello schermo x e y. L'uso più comune per i derivati consiste nel calcolare i calcoli del livello di dettaglio per il campionamento delle trame e, nel caso di filtri anisotropi, selezionando i campioni lungo l'asse dell'anisotropia. In genere, un'implementazione hardware esegue un pixel shader su più pixel (ad esempio una griglia 2x2) contemporaneamente, in modo che i derivati delle quantità calcolate nel pixel shader possano essere ragionevolmente approssimati come delta dei valori nello stesso punto di esecuzione in pixel adiacenti.

### <a name="inputs"></a>Input

Quando la pipeline è configurata senza geometry shader, un pixel shader è limitato a 16 input a 32 bit a 4 componenti. In caso contrario, pixel shader può richiedere fino a 32 input a 32 bit a 4 componenti.

I dati di input del pixel shader includono attributi dei vertici (che possono essere interpolati con o senza correzione della prospettiva) o possono essere trattati come costanti in base a primitive. Gli input del pixel shader vengono interpolati dagli attributi vertice della primitiva in fase di rasterizzazione, in base alla modalità di interpolazione dichiarata. Se una primitiva viene ritagliata prima della rasterizzazione, la modalità di interpolazione viene rispettata anche durante il processo di ritaglio.

Gli attributi dei vertici vengono interpolati (o valutati) pixel shader posizioni del centro. Le modalità di interpolazione degli attributi pixel shader vengono dichiarate in una dichiarazione di registro di input, per ogni elemento in un argomento [o](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-function-parameters) in una struttura [di input.](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-struct) Gli attributi possono essere interpolati in modo lineare o con [il campionamento centroide.](https://msdn.microsoft.com/library/Ee415231(v=VS.85).aspx) La valutazione centroide è rilevante solo durante il multicampionamento per coprire i casi in cui un pixel è coperto da una primitiva, ma un centro pixel potrebbe non essere; la valutazione centroide si verifica il più vicino possibile al centro pixel (non coperto).

Gli input possono anche essere dichiarati con una [semantica di valore](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)di sistema , che contrassegna un parametro utilizzato da altre fasi della pipeline. Ad esempio, una posizione in pixel deve essere contrassegnata con la semantica SV \_ Position. La fase IA può produrre un valore scalare per un pixel shader (usando PrimitiveID SV). La fase di rasterizzazione può anche generare un scalare per un \_ pixel shader (usando \_ SV IsFrontFace).

### <a name="outputs"></a>Output

Un pixel shader può ottenere fino a 8, 32 bit, colori a 4 componenti o nessun colore se il pixel viene eliminato. I componenti del registro di output del pixel shader devono essere dichiarati prima di poter essere usati. a ogni registro è consentita una maschera di output/scrittura distinta.

Usare lo stato depth-write-enable (nella fase di unione dell'output) per controllare se i dati di profondità vengono scritti in un buffer di profondità (o usare l'istruzione discard per eliminare i dati per quel pixel). Un pixel shader anche un valore facoltativo a 32 bit, a 1 componente, a virgola mobile e profondità per il test di profondità (usando la semantica SV \_ Depth). Il valore di profondità viene restituito nel registro oDepth e sostituisce il valore di profondità interpolata per il test di profondità (presupponendo che il test di profondità sia abilitato). Non è possibile passare in modo dinamico dall'uso della profondità a funzione fissa o dell'oDepth dello shader.

Un pixel shader non può eseguire l'output di un valore di stencil.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pipeline grafica](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[Fasi della pipeline (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

 