---
title: Topologie primitive
description: Direct3D 10 e versioni successive supporta diversi tipi primitivi (o topologie) rappresentati dal \_ \_ tipo enumerato della topologia primitiva D3D. Questi tipi definiscono il modo in cui i vertici vengono interpretati e sottoposti a rendering dalla pipeline.
ms.assetid: 357ad085-fd91-4420-abc3-1c57e8cbb517
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e83f901d4d91d01a3cffedddb343fde7b50c20e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337583"
---
# <a name="primitive-topologies"></a>Topologie primitive

Direct3D 10 e versioni successive supporta diversi tipi primitivi (o topologie) rappresentati dal tipo enumerato della [**\_ \_ topologia primitiva D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_primitive_topology) . Questi tipi definiscono il modo in cui i vertici vengono interpretati e sottoposti a rendering dalla pipeline.

-   [Tipi primitivi di base](#basic-primitive-types)
-   [Adiacenza primitive](#primitive-adjacency)
-   [Direzione di avvolgimento e posizioni vertice iniziali](#winding-direction-and-leading-vertex-positions)
-   [Generazione di più strisce](#generating-multiple-strips)
-   [Argomenti correlati](#related-topics)

## <a name="basic-primitive-types"></a>Tipi primitivi di base

Sono supportati i tipi primitivi di base seguenti:

-   [Elenco punti](/windows/desktop/direct3d9/point-lists)
-   [Elenco linee](/windows/desktop/direct3d9/line-lists)
-   [Striscia di linea](/windows/desktop/direct3d9/line-strips)
-   [Elenco di triangolo](/windows/desktop/direct3d9/triangle-lists)
-   [Strip Triange](/windows/desktop/direct3d9/triangle-strips)

Per una visualizzazione di ogni tipo primitivo, vedere il diagramma più avanti in questo argomento in [direzione di avvolgimento e posizioni dei vertici iniziali](#winding-direction-and-leading-vertex-positions).

La fase input-assembler legge i dati dai buffer dei vertici e degli indici, assembla i dati in queste primitive e quindi invia i dati alle fasi della pipeline rimanenti. È possibile usare il metodo [**sul ID3D11DeviceContext:: IASetPrimitiveTopology**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetprimitivetopology) per specificare il tipo primitivo per la fase input-assembler.

## <a name="primitive-adjacency"></a>Adiacenza primitive

Tutti i tipi primitivi Direct3D 10 e versioni successive, ad eccezione dell'elenco di punti, sono disponibili in due versioni: un tipo primitivo con adiacenza e un tipo primitivo senza adiacenza. Le primitive con adiacenza contengono alcuni vertici circostanti, mentre le primitive senza adiacenza contengono solo i vertici della primitiva di destinazione. Ad esempio, la primitiva dell'elenco di righe (rappresentata dal valore di **\_ \_ \_ linea della topologia primitiva D3D** ) dispone di una primitiva dell'elenco di righe corrispondente che include adiacenza (rappresentato dal valore ADJ per la **\_ \_ topologia \_ \_ primitiva D3D** ).

Le primitive adiacenti hanno lo scopo di fornire altre informazioni sulla geometria e sono visibili solo tramite un geometry shader. Adiacenza è utile per i geometry shader che usano il rilevamento della siluetta, l'estrusione del volume shadow e così via.

Si supponga, ad esempio, di voler creare un elenco di triangolo con adiacenza. Un elenco di triangolo che contiene 36 vertici (con adiacenza) produrrà 6 primitive completate. Le primitive con adiacenza (eccetto le strisce di riga) contengono esattamente il doppio dei vertici della primitiva equivalente senza adiacenza, dove ogni vertice aggiuntivo è un vertice adiacente.

## <a name="winding-direction-and-leading-vertex-positions"></a>Direzione di avvolgimento e posizioni vertice iniziali

Come illustrato nella figura seguente, un vertice iniziale è il primo vertice non adiacente in una primitiva. Un tipo primitivo può avere più vertici iniziali definiti, purché ognuno di essi venga usato per una primitiva diversa. Per una striscia di triangolo con adiacenza, i vertici iniziali sono 0, 2, 4, 6 e così via. Per una striscia di righe con adiacenza, i vertici iniziali sono 1, 2, 3 e così via. Una primitiva adiacente, d'altra parte, non ha un vertice principale.

Nella figura seguente viene illustrato l'ordinamento dei vertici per tutti i tipi primitivi che l'assembler di input può produrre.

![diagramma dell'ordinamento dei vertici per i tipi primitivi](images/d3d10-primitive-topologies.png)

I simboli nell'illustrazione precedente sono descritti nella tabella seguente.



| Simbolo                                                                                   | Nome              | Descrizione                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ![simbolo per un vertice](images/d3d10-primitive-topologies-vertex.png)                     | Vertice            | Punto nello spazio 3D.                                                                                                                                                                               |
| ![simbolo per la direzione di avvolgimento](images/d3d10-primitive-topologies-winding-direction.png) | Direzione di avvolgimento | Ordine del vertice durante l'assemblaggio di una primitiva. Può essere in senso orario o in senso antiorario; per specificare questo problema, chiamare [**ID3D11Device1:: CreateRasterizerState1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createrasterizerstate1). |
| ![simbolo per i vertici iniziali](images/d3d10-primitive-topologies-leading-vertex.png)       | Vertice principale    | Primo vertice non adiacente in una primitiva che contiene dati per ogni costante.                                                                                                                      |



 

## <a name="generating-multiple-strips"></a>Generazione di più strisce

È possibile generare più strisce tramite il taglio della striscia. È possibile eseguire uno striping chiamando in modo esplicito la funzione HLSL [RestartStrip](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-so-restartstrip) o inserendo un valore di indice speciale nel buffer dell'indice. Questo valore è-1, ovvero 0xFFFFFFFF per gli indici a 32 bit o 0xFFFF per gli indici a 16 bit. Un indice di-1 indica un'Cut ' o ' restart ' esplicito della striscia corrente. L'indice precedente completa la primitiva o la striscia precedente e l'indice successivo avvia una nuova primitiva o una nuova striscia. Per altre informazioni sulla generazione di più strisce, vedere [fase geometry-shader](/previous-versions//bb205146(v=vs.85)).

> [!Note]  
> È necessario un hardware di [livello funzionalità](overviews-direct3d-11-devices-downlevel-intro.md) 10,0 o superiore perché non tutti i componenti hardware di 10level9 implementano questa funzionalità.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Introduzione con la fase di Input-Assembler](d3d10-graphics-programming-guide-input-assembler-stage-getting-started.md)
</dt> <dt>

[Fasi della pipeline (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

 