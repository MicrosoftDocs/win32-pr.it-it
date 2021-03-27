---
title: ld_structured (SM5-ASM)
description: Lettura ad accesso casuale di componenti a 32 bit 1-4 da un buffer strutturato.
ms.assetid: ED572B76-FF6C-405E-9110-4B12AD5E5AE6
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00a34bafdcfbe0658723dd83d62507e255ff4bfa
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398260"
---
# <a name="ld_structured-sm5---asm"></a>LD \_ strutturato (SM5-ASM)

Lettura ad accesso casuale di componenti a 32 bit 1-4 da un buffer strutturato.



| : LD \_ strutturato dst0 \[ . mask \] , srcAddress \[ . Select \_ Component \] , srcByteOffset \[ . Select \_ Component \] , src0 \[ . Swizzle\] |
|-------------------------------------------------------------------------------------------------------------------------|



 



| Elemento                                                                                                                       | Descrizione                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                                            | \[nell' \] indirizzo dei risultati dell'operazione.<br/>                                                                                             |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>             | \[in \] specifica l'indice della struttura da leggere.<br/>                                                                                            |
| <span id="srcByteOffset"></span><span id="srcbyteoffset"></span><span id="SRCBYTEOFFSET"></span>*srcByteOffset*<br/> | \[in \] specifica l'offset di byte nella struttura da cui iniziare la lettura. <br/>                                                                       |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                            | Il buffer da cui eseguire la lettura. Questo parametro deve essere un SRV (t \# ), UAV (u \# ). Nel compute shader può anche essere la memoria condivisa del gruppo di thread (g \# ). <br/> |



 

## <a name="remarks"></a>Commenti

I dati letti dalla struttura sono equivalenti al seguente pseudocodice: dove abbiamo l'offset, l'indirizzo, il puntatore al contenuto del buffer, lo stride dell'origine e i dati archiviati in modo lineare.

``` syntax
                    BYTE *BufferContents;         // from SRV or UAV
                    UINT BufferStride;            // from base resource
                    UINT srcAddress, srcByteOffset;   // from source registers
                    BYTE *ReadLocation;           // value to calculate
                    ReadLocation = BufferContents 
                                + BufferStride * srcByteOffset
                                + srcOffset;

                    UINT32 Temp[4];  // used to make code shorter

                    // apply the source resource swizzle on source data
                    Temp = read_and_swizzle(ReadLocation, srcSwizzle);

                    // write the components to the output based on mask
                    ApplyWriteMask(dstRegister, dstWriteMask, Temp);
```

Questo pseudocodice Mostra come funziona l'operazione, ma i dati effettivi non devono essere archiviati in modo lineare. Se i dati non vengono archiviati in modo lineare, l'operazione effettiva dell'istruzione deve corrispondere al comportamento dell'operazione precedente.

Il superamento dei limiti per u \# /t \# di un determinato componente a 32 bit restituisce 0 per quel componente, tranne nel caso in cui *srcByteOffset*, oltre a swizzle sia il risultato che impedisce l'accesso all'utente \# /t \# , il valore restituito per tutti i componenti non è definito.

All'esterno dei limiti \# che puntano a g (i limiti di tale particolare g \# , anziché di tutta la memoria condivisa) per qualsiasi componente a 32 bit, restituiscono un risultato non definito.

*srcByteOffset* è un argomento separato da *srcAddress* perché si tratta in genere di un valore letterale. Questa separazione di parametri non è stata eseguita per gli atomici sulla memoria strutturata.

cs \_ 4 \_ 0 e cs \_ 4 \_ 1 supportano questa istruzione per UAV, SRV e TGSM.

Questa istruzione si applica alle fasi dello shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

Poiché UAV sono disponibili in tutte le fasi dello shader per Direct3D 11,1, questa istruzione si applica a tutte le fasi dello shader per UAV per il runtime Direct3D 11,1, disponibile a partire da Windows 8.



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



 

cs \_ 4 \_ 0 e cs \_ 4 \_ 1 supportano questa istruzione per UAV, SRV e TGSM.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Assembly Shader Model 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





