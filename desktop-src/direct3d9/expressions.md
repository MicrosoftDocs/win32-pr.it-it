---
description: Le espressioni sono istruzioni matematiche o logiche usate sul lato destro di un segno di uguale. Esistono molti tipi di espressioni.
ms.assetid: 642aa188-5dd7-49fc-b6cc-845f8fc22530
title: Espressioni (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: daeffeb09a2c2f496f73d492581cb2b51ac2e518e176bbbc848889bef5716b25
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985701"
---
# <a name="expressions-direct3d-9"></a>Espressioni (Direct3D 9)

Le espressioni sono istruzioni matematiche o logiche usate sul lato destro di un segno di uguale. Esistono molti tipi di espressioni.

## <a name="expressions"></a>Espressioni

1.  Informazioni di riferimento sulla variabile
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

    

    Tutte le espressioni HLL numeriche standard sono supportate qui.

4.  Costruttore
    ```
    type ( constructor arguments )
    ```

    

5.  Elenco di inizializzatori

    ```
    { scalar value [, scalar value ...  ] }
    
    ```

    

    Gli scalari devono essere valori scalari letterali.

    Il numero di inizializzatori deve essere compatibile con la variabile (stato) sul lato sinistro del segno di uguale.

6.  Espressione OR

    ```
    token [ | token ... ]
    ```

    

    I token devono essere compatibili con la variabile (stato) sul lato sinistro del segno di uguale.

    Per i token non viene fatto distinzione tra maiuscole e minuscole.

7.  NULL

    ```
    NULL
    ```

    

    NULL può essere assegnato solo a uno shader, a un campionatore o a un oggetto trama.

8.  Blocco di assembly

    ```
    asm { code }
    ```

    

    I blocchi di assembly PS devono essere assegnati allo stato PIXELSHADER.

    I blocchi di assembly vs devono essere assegnati allo stato VERTEXSHADER.

9.  Blocco di stato del campionatore

    ```
    sampler_state { [ state = expression ; [ state = ... ] ] }
    ```

    

    I blocchi di stato del campionatore sono sequenze di stato della fase del campionatore non indicizzato o assegnazioni di trama.

    I blocchi di stato del campionatore devono essere assegnati allo stato dell'effetto SAMPLER.

10. Blocco stato dell'effetto

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

    

    La destinazione vertex shader e \_ m n indica la versione del \_ vertex shader D3DVS \_ VERSION(m, n). La pixel shader ps \_ m \_ n indica D3DPS \_ VERSION(m, n) pixel shader versione.

    Le espressioni di compilazione del linguaggio di alto livello di vertex shader possono essere assegnate solo allo stato dell'effetto VERTEXSHADER. Le espressioni di compilazione del linguaggio di alto livello pixel shader possono essere assegnate solo allo stato dell'effetto PIXELSHADER.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Formato effetto](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



