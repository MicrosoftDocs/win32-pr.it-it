---
description: Le espressioni sono istruzioni matematiche o logiche che vengono usate sul lato destro di un segno di uguale. Sono disponibili molti tipi di espressioni.
ms.assetid: 642aa188-5dd7-49fc-b6cc-845f8fc22530
title: Espressioni (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3aa574069094853eb506f7a1b38cdb6cd4379d3b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303726"
---
# <a name="expressions-direct3d-9"></a>Espressioni (Direct3D 9)

Le espressioni sono istruzioni matematiche o logiche che vengono usate sul lato destro di un segno di uguale. Sono disponibili molti tipi di espressioni.

## <a name="expressions"></a>Espressioni

1.  Riferimento a una variabile
    ```
    ( variable ) or<variable >
    ```

    

2.  Scalare numerico
    ```
    scalar 
    ```

    

3.  Espressione numerica

    ```
    ( numeric expression )
    ```

    

    Qui sono supportate tutte le espressioni HLL numeriche standard.

4.  Costruttore
    ```
    type ( constructor arguments )
    ```

    

5.  Elenco di inizializzatori

    ```
    { scalar value [, scalar value ...  ] }
    
    ```

    

    I valori scalari devono essere valori scalari letterali.

    Il numero di inizializzatori deve essere compatibile con la variabile (stato) sul lato sinistro del segno di uguale.

6.  Espressione OR

    ```
    token [ | token ... ]
    ```

    

    I token devono essere compatibili con la variabile (stato) sul lato sinistro del segno di uguale.

    I token non fanno distinzione tra maiuscole e minuscole.

7.  NULL

    ```
    NULL
    ```

    

    NULL può essere assegnato solo a uno shader, un campionatore o un oggetto trama.

8.  Blocco assembly

    ```
    asm { code }
    ```

    

    È necessario assegnare i blocchi di assembly PS allo stato PIXELSHADER.

    I blocchi di assembly di Visual Studio devono essere assegnati allo stato VERTEXSHADER.

9.  Blocco dello stato del campionatore

    ```
    sampler_state { [ state = expression ; [ state = ... ] ] }
    ```

    

    I blocchi di stato del campionatore sono sequenze di assegnazioni di trame o stato della fase del campionatore non indicizzato.

    I blocchi di stato del campionatore devono essere assegnati allo stato dell'effetto CAMPIONATOre.

10. Blocco dello stato di stato dell'effetto

    ```
    stateblock_state { [ state [ [index] ] = expression; 
        [ state [ [index] ] = ... ] ] }
    ```

    

    I blocchi di stato sono sequenze di stato generale. I blocchi di stato possono essere annidati, ma non possono contenere riferimenti circolari.

    I blocchi di stato devono essere assegnati allo stato dell'effetto STATEBLOCK.

11. Compilazione HLSL

    ```
    compile target entrypoint ( [ arguments ] )
    ```

    

    La destinazione vertex shader \_ e m \_ n indica D3DVS \_ versione (m, n) vertex shader Version. La destinazione pixel shader PS m n indica che la versione di \_ \_ D3DPS \_ (m, n) pixel shader.

    Le espressioni di compilazione del linguaggio di alto livello del vertex shader possono essere assegnate solo allo stato dell'effetto VERTEXSHADER. Le espressioni di compilazione del linguaggio di alto livello del pixel shader possono essere assegnate solo allo stato dell'effetto PIXELSHADER.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Formato effetto](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



