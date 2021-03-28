---
title: Fase pixel shader
description: La fase pixel shader (PS) consente tecniche di ombreggiatura avanzate, ad esempio l'illuminazione per pixel e la post-elaborazione.
ms.assetid: 09831B10-4FD1-41E7-8D81-5AA63DC90020
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57142e9c32919a6959a7fac14bf544cca1dacd79
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118194"
---
# <a name="pixel-shader-stage"></a>Fase pixel shader

La fase pixel shader (PS) consente tecniche di ombreggiatura avanzate, ad esempio l'illuminazione per pixel e la post-elaborazione. Un pixel shader è un programma che combina variabili costanti, dati di trama, valori interpolati per vertice e altri dati per produrre output per pixel. La fase di rasterizzazione richiama una pixel shader una volta per ogni pixel coperto da una primitiva, ma è possibile specificare uno shader **null** per evitare l'esecuzione di uno shader.

## <a name="the-pixel-shader"></a>Pixel shader

Quando si esegue il multicampionamento di una trama, viene richiamata una pixel shader una volta per ogni pixel, mentre si verifica un test di profondità/stencil per ogni multisample coperto. Gli esempi che superano il test di profondità/stencil vengono aggiornati con il colore di output del pixel shader.

Le funzioni intrinseche pixel shader producono o usano derivati di quantità rispetto allo spazio dello schermo x e y. L'uso più comune per i derivati consiste nel calcolare i calcoli del livello di dettaglio per il campionamento della trama e, nel caso del filtro anisotropico, selezionando esempi lungo l'asse di anisotropia. In genere, un'implementazione hardware esegue contemporaneamente un pixel shader su più pixel (ad esempio una griglia 2x2), in modo che i derivati delle quantità calcolate nel pixel shader possano essere ragionevolmente approssimati come Delta dei valori nello stesso punto di esecuzione in pixel adiacenti.

### <a name="inputs"></a>Input

Quando la pipeline viene configurata senza un geometry shader, un pixel shader è limitato a 16 input a 32 bit e a 4 componenti. In caso contrario, un pixel shader può richiedere fino a 32 input a 32 bit e a 4 componenti.

I dati di input del pixel shader includono attributi di vertice (che possono essere interpolati con o senza correzione della prospettiva) oppure possono essere considerati come costanti per primitive. Gli input del pixel shader vengono interpolati dagli attributi dei vertici della primitiva in fase di rasterizzazione, in base alla modalità di interpolazione dichiarata. Se una primitiva viene ritagliata prima della rasterizzazione, la modalità di interpolazione viene rispettata anche durante il processo di ritaglio.

Gli attributi vertici vengono interpolati (o valutati) in pixel shader Center Locations. Le modalità di interpolazione degli attributi pixel shader sono dichiarate in una dichiarazione di registro di input, in base a ogni elemento in un [argomento](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-function-parameters) o una [struttura di input](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-struct). Gli attributi possono essere interpolati in modo lineare o con [campionamento](https://msdn.microsoft.com/library/Ee415231(v=VS.85).aspx)del centro. La valutazione del centro è pertinente solo durante il campionamento multiplo per coprire i casi in cui un pixel è coperto da una primitiva, ma un pixel Center potrebbe non essere; la valutazione del baricentro si verifica il più vicino possibile al centro pixel (non coperto).

Gli input possono anche essere dichiarati con una [semantica del valore di sistema](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics), che contrassegna un parametro utilizzato da altre fasi della pipeline. Ad esempio, la posizione di un pixel deve essere contrassegnata con la \_ semantica di posizione SV. La fase IA può produrre un valore scalare per un pixel shader (usando SV \_ PrimitiveID); la fase di rasterizzazione può anche generare un valore scalare per una pixel shader (usando SV \_ IsFrontFace).

### <a name="outputs"></a>Output

Un pixel shader può restituire colori fino a 8, a 32 bit, a 4 componenti o nessun colore se il pixel viene ignorato. I componenti del registro di output di pixel shader devono essere dichiarati prima di poter essere usati. a ogni registro è consentita una maschera di scrittura output distinta.

Utilizzare lo stato Depth-Write-Enable (nella fase merge output) per controllare se i dati di profondità vengono scritti in un buffer di profondità (oppure utilizzare l'istruzione di eliminazione per eliminare i dati per tale pixel). Un pixel shader può anche restituire un valore facoltativo a virgola mobile a 32 bit, a 1 componente, a virgola mobile e di profondità per i test di profondità (usando la \_ semantica di profondità SV). Il valore depth viene restituito nel registro oDepth e sostituisce il valore di profondità interpolato per il test di profondità (presupponendo che i test di profondità siano abilitati). Non esiste alcun modo per cambiare dinamicamente tra l'uso della profondità della funzione fissa o dello shader oDepth.

Un pixel shader non può restituire un valore di stencil.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pipeline grafica](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[Fasi della pipeline (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

 