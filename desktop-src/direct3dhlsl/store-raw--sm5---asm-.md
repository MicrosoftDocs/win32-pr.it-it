---
title: store_raw (SM5-ASM)
description: Scrittura ad accesso casuale di componenti a 32 bit 1-4 nella memoria di tipo.
ms.assetid: D166116A-CF4E-4020-9F6A-F9CEEFCDAB21
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c44b4d22a576853fb8b7d2c43fcb6a2d7fc9a448
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398286"
---
# <a name="store_raw-sm5---asm"></a>archivio \_ RAW (SM5-ASM)

Scrittura ad accesso casuale di componenti a 32 bit 1-4 nella memoria di tipo.



| archiviare una \_ maschera dst0. Write non elaborata \[ \_ \] , dstByteOffset \[ . Select \_ Component \] , src0 \[ . Swizzle\] |
|----------------------------------------------------------------------------------------|



 



| Elemento                                                                                                                       | Descrizione                                |
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                                            | \[nell' \] indirizzo di memoria.<br/>      |
| <span id="dstByteOffset"></span><span id="dstbyteoffset"></span><span id="DSTBYTEOFFSET"></span>*dstByteOffset*<br/> | \[nell' \] offset.<br/>              |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                            | \[nei \] componenti da scrivere.<br/> |



 

## <a name="remarks"></a>Commenti

Questa istruzione esegue i componenti a 1-4 bit del componente \* 32 scritti da *src0* a *dst0* in corrispondenza dell'offset in *dstByteOffset*. Nessuna conversione di formato.

il valore di *dst0* deve essere un UAV (u \# ) o nel compute shader. può anche essere una memoria condivisa del gruppo di thread (g \# ).

*dstByteOffset* specifica il valore di base a 32 bit in memoria per una finestra di 4 valori sequenziali a 32 bit in cui è possibile scrivere i dati, a seconda di swizzle e maschera su altri parametri.

Il percorso dei dati scritti equivale al seguente pseudocodice che mostra l'indirizzo, il puntatore al contenuto del buffer e i dati archiviati in modo lineare.

``` syntax
                    BYTE *BufferContents;          // from src0
                    UINT dstByteOffset;            // source register
                    BYTE *WriteLocation;           // value to calculate

                    // calculate writing location
                    WriteLocation = BufferContents 
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
                             WriteComponents * sizeof(UINT32));
```

Questo pseudocodice Mostra come funziona l'operazione, ma i dati effettivi non devono essere archiviati in modo lineare. *dst0* può avere solo una maschera di scrittura che è una delle seguenti:. x,. XY,. xyz,. xyzw. La maschera di scrittura determina il numero di componenti a 32 bit da scrivere senza gap.

All'esterno dei limiti di indirizzamento su u \# significa che non viene scritto nulla nella memoria fuori limite; qualsiasi parte che si trova nei limiti viene scritta correttamente.

All'esterno dei limiti \# che puntano a g (i limiti di tale particolare g \# , anziché di tutta la memoria condivisa) per qualsiasi componente a 32 bit, l'intero contenuto di tutta la memoria condivisa diventerà indefinito.

cs \_ 4 \_ 0 e cs \_ 4 \_ 1 supportano questa istruzione per UAV.

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

 

 





