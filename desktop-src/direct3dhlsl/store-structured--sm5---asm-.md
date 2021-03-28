---
title: store_structured (SM5-ASM)
description: Scrittura ad accesso casuale di componenti a 1-4 32 bit in una visualizzazione di accesso non ordinato (UAV) del buffer strutturato.
ms.assetid: 8080B2CA-5BDA-4F01-8B2B-B85BDD58C5AF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5890d30fac57923365f0bdea89fcce55f7922c7
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104046078"
---
# <a name="store_structured-sm5---asm"></a>archivio \_ strutturato (SM5-ASM)

Scrittura ad accesso casuale di componenti a 1-4 32 bit in una visualizzazione di accesso non ordinato (UAV) del buffer strutturato.



| archivio \_ strutturato dst0 \[ . Write \_ mask \] , dstAddress \[ . Select \_ Component \] , dstByteOffset \[ . Select \_ Component \] , src0 \[ . Swizzle\] |
|---------------------------------------------------------------------------------------------------------------------------------|



 



| Elemento                                                                                                                       | Descrizione                                                    |
|----------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                                            | \[nell' \] indirizzo dei risultati dell'operazione.<br/> |
| <span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*<br/>             | \[nell' \] indirizzo in cui scrivere.<br/>               |
| <span id="dstByteOffset"></span><span id="dstbyteoffset"></span><span id="DSTBYTEOFFSET"></span>*dstByteOffset*<br/> | \[nell' \] indice della struttura da scrivere.<br/>         |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                            | \[nei \] componenti da scrivere.<br/>                     |



 

## <a name="remarks"></a>Commenti

Questa istruzione esegue 1-4 \* componenti a 32 bit del componente scritti da *src0* a *Dst0* all'indirizzo in *dstAddress* e *dstByteOffset*. Nessuna conversione di formato.

*dst0* deve essere un UAV (u \# ). Nel compute shader può anche essere la memoria condivisa del gruppo di thread (g \# ).

*dstAddress* specifica l'indice della struttura da scrivere.

Il percorso dei dati scritti equivale allo pseudocodice seguente che mostra l'offset, l'indirizzo, il puntatore al contenuto del buffer, lo stride dell'origine e i dati archiviati in modo lineare.

``` syntax
                    BYTE *BufferContents;             // from dst0
                    UINT BufferStride;                // from dst0
                    UINT dstAddress, dstByteOffset;   // source registers
                    BYTE *WriteLocation;              // value to calculate

                    // calculate writing location
                     WriteLocation = BufferContents 
                                + BufferStride * dstAddress 
                                + dstByteOffset;

                    // calculate the number of components to write
                    switch (dstWriteMask)
                    {
                        x:    WriteComponents = 1; break;
                        xy:   WriteComponents = 2; break;
                        xyz:  WriteComponents = 3; break;
                        xyzw: WriteComponents = 4; break;
                        default:  // only these masks are valid                              
                    }

                    // copy the data from the source register with
                    //    the swizzle applied
                    memcpy(WriteLocation, swizzle(src0, src0.swizzle), 
                             WriteComponents * sizeof(INT32));
```

Questo pseudocodice Mostra come funziona l'operazione, ma i dati effettivi non devono essere archiviati in modo lineare. Se i dati non vengono archiviati in modo lineare, l'operazione effettiva dell'istruzione deve corrispondere al comportamento dell'operazione precedente.

*dst0* può avere solo una maschera di scrittura che è una delle seguenti:. x,. XY,. xyz,. xyzw. La maschera di scrittura determina il numero di componenti a 32 bit da scrivere senza gap.

Il superamento dei limiti in u \# cacitato da *dstAddress* significa che non viene scritto alcun elemento nella memoria fuori limite.

Se il *dstByteOffset*, incluso *dstWriteMask*, è ciò che causa l'accesso all'utente \# , l'intero contenuto del UAV diventa indefinito.

All'esterno dei limiti \# che puntano a g (i limiti di tale particolare g \# , anziché di tutta la memoria condivisa) per qualsiasi componente a 32 bit, l'intero contenuto di tutta la memoria condivisa diventerà indefinito.

*dstByteOffset* è un argomento separato da *dstAddress* perché si tratta in genere di un valore letterale. Questa separazione di parametri non è stata eseguita per gli atomici sulla memoria strutturata.

cs \_ 4 \_ 0 e cs \_ 4 \_ 1 supportano questa istruzione per UAV e TGSM.

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     | X       |



 

Poiché UAV sono disponibili in tutte le fasi dello shader per Direct3D 11,1, questa istruzione si applica a tutte le fasi dello shader per il runtime Direct3D 11,1, disponibile a partire da Windows 8.



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modello Shader minimo

Questa istruzione è supportata nei modelli shader seguenti:



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello Shader 5](d3d11-graphics-reference-sm5.md)        | sì       |
| [Modello Shader 4,1](dx-graphics-hlsl-sm4.md)              | no        |
| [Modello Shader 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly Shader Model 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





